## [L-01] Missing Checks Allow Collateral Balance to be Drained via Flash Loans

The ActivePool contract allows flash loans to be taken out of the collateral token (stETH) held by the contract. However, there are no checks to prevent multiple flash loans from being taken out simultaneously that could drain the entire collateral balance.

The maxFlashLoan() function returns the full collateral balance without accounting for any outstanding loans. And the flashLoan() function does not track the amount loaned out or decrement it from the available balance.

```solidity
File: contracts/contracts/ActivePool.sol

    function maxFlashLoan(address token) public view override returns (uint256) {
        if (token != address(collateral)) {
            return 0;
        }

        if (flashLoansPaused) {
            return 0;
        }

        return collateral.balanceOf(address(this));
    }

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L328-L339

This means if two or more flash loans are taken at the same time for the full balance amount, they could both succeed even though together they exceed the actual available balance. When the loans are repaid, there may be an insufficient balance to return one or both of the principal+fee amounts.

This is a security issue as an attacker could theoretically empty out the contract's collateral reserves by taking out multiple flash loans in quick succession before repayments are processed.

To remedy this, the contract should track the amount of loans outstanding and deduct that from the max loan amount reported. Individual loan origination should also fail if it would exceed the updated remaining balance amount.

## [L-02] Lack of Validation Allows Unauthorized Accounts to Take Out Flash Loans

The flashLoan() function in the ActivePool contract does not validate or restrict the flash loan receiver address in any way. Any external account is able to be passed as the receiver and have the loan sent to them.

```solidity
File: contracts/contracts/ActivePool.sol

    function flashLoan(
        IERC3156FlashBorrower receiver,
        address token,
        uint256 amount,
        bytes calldata data
    ) external override returns (bool) {
        require(amount > 0, "ActivePool: 0 Amount");
        uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused
        require(amount <= maxFlashLoan(token), "ActivePool: Too much");

        uint256 amountWithFee = amount + fee;
        uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

        collateral.transfer(address(receiver), amount);

        // Callback
        require(
            receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
            "ActivePool: IERC3156: Callback failed"
        );

        // Transfer of (principal + Fee) from flashloan receiver
        collateral.transferFrom(address(receiver), address(this), amountWithFee);

        // Send earned fee to designated recipient
        collateral.transfer(feeRecipientAddress, fee);

        // Check new balance
        // NOTE: Invariant Check, technically breaks CEI but I think we must use it
        // NOTE: This means any balance > systemCollShares is stuck, this is also present in LUSD as is

        // NOTE: This check effectively prevents running 2 FL at the same time
        //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert
        require(
            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
            "ActivePool: Must repay Balance"
        );
        require(
            collateral.sharesOf(address(this)) >= systemCollShares,
            "ActivePool: Must repay Share"
        );
        require(
            collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
            "ActivePool: Should keep same collateral share rate"
        );

        emit FlashLoanSuccess(address(receiver), token, amount, fee);

        return true;
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310
There are no checks that the receiver is a known and authorized smart contract. An attacker could potentially call flashLoan() and have the tokens sent directly to their own account without needing to interact with a receiver contract at all.

Normally flash loan protocols maintain a whitelist of approved receiver contracts that are known to follow the required callback interface. By not having any validation, the ActivePool makes its flash loans vulnerable to misuse and theft.

An unauthorized actor could drain the collateral reserves by taking out multiple flash loans to their own account without properly repaying the loan plus fee. Or a receiver contract could behave maliciously, like not returning the full funds owed.

The flash Loan receiver should be restricted to a whitelist of authorized contracts, and the receiver address should be validated as a smart contract implementing the needed interface. This would prevent attacks and theft of loaned assets.

## [L-03] Unlimited Token Approvals Allow Amount Exploitation

The LeverageMacroBase contract approves tokens for swapping with unlimited/maximum amounts without setting approvals back to zero after the swap is completed.

The `_doSwap` function approves the swap target for the exact amount passed in, but does not revoke this approval later on. This means any approved third party could still transfer the authorized tokens even after the intended swap.

```solidity
File:  contracts/contracts/LeverageMacroBase.sol

    function _doSwaps(SwapOperation[] memory swapData) internal {
        uint256 swapLength = swapData.length;

        for (uint256 i; i < swapLength; ) {
            _doSwap(swapData[i]);
            unchecked {
                ++i;
            }
        }
    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382-L391

An attacker could call into this contract with a high approval amount, let the swap execute, then collect the remaining approved funds from the approved target. Or a compromised target could misuse approved funds after the fact.

To prevent token amounts from being exploited in this way, approvals should be limited to the exact needed values and explicitly revoked back to zero after each swap is concluded successfully. Unlimited open approvals pose a security risk.

## [L-04] SortedCdps contract vulnerable to state bloat DoS attack

The SortedCdps contract is vulnerable to a denial of service attack via state bloat. An attacker could insert many nodes into the sorted list stored in the contract by calling the insert function with bogus cdp data. This would consume all the contract's storage by adding unnecessary nodes to the list.

```solidity
File:  contracts/contracts/SortedCdps.sol

    function insert(
        address owner,
        uint256 _NICR,
        bytes32 _prevId,
        bytes32 _nextId
    ) external override returns (bytes32) {
        _requireCallerIsBOorCdpM();
        bytes32 _id = toCdpId(owner, block.number, nextCdpNonce);
        require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

        _insert(_id, _NICR, _prevId, _nextId);

        unchecked {
            ++nextCdpNonce;
        }

        return _id;
    }

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L362

The insert function does not validate the cdp data passed in nor does it limit the number of nodes that can be added. Additionally, there are no gas costs or limits implemented to prevent an attacker from inserting a huge number of nodes.

This state bloat would eventually exhausted the contract's storage allocation on the blockchain, preventing any further inserts or lookups on the sorted list. This would deny service to other users of the contract's functionality.

The contract needs appropriate input validation on the insert function to prevent junk data being added. Gas costs or limits also need implementing to disincentivize this type of attack. Otherwise an adversarial actor could spam bogus insertions to consume storage and degrade the contract's usability.
