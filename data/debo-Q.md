## [L-01] Lengthy numerals
Utilising big numerals that have a lot of precisions is within the file and this can be bettered by utilising scientific numerals.

**Locations**
```sol
// The number 525600000 is seen on line 60.
// contracts/Dependencies/EbtcMath.sol#L60-L60
if (_minutes > 525600000) {

// The number 525600000 is seen on line 61.
// contracts/Dependencies/EbtcMath.sol#L61-L61
_minutes = 525600000;

// The number 1030000000000000000 is seen on line 19.
// contracts/Dependencies/EbtcBase.sol#L19-L19
    uint256 public constant LICR = 1030000000000000000; // 103%

// The number 1100000000000000000 is seen on line 22.
// contracts/Dependencies/EbtcBase.sol#L22-L22
    uint256 public constant MCR = 1100000000000000000; // 110%

// The number 1250000000000000000 is seen on line 25.
// contracts/Dependencies/EbtcBase.sol#L25-L25
    uint256 public constant CCR = 1250000000000000000; // 125%
```
**Remediation**
Change the number 525600000 to scientific notation of `5256e5`.
Change the number 1030000000000000000 to scientific notation of `103e16`.
Change the number 1100000000000000000 to scientific notation of `11e17`.
Change the number 1250000000000000000 to scientific notation of `125e16`.
## [L-02] Unchecked Transfer
## Impact
If the transferFrom does not go through or responds with 0 then sometimes the transfer does not roll back.
So when calling the transferFrom method one should check it in the code.

## Proof of Concept
**Vulnerable flash loan function**
```sol
// line 261-310
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
**Exploit unchecked transfer flash loan**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./ActivePool.sol";

contract tActivePool {

   ActivePool public x1;

   address token = address(0x9Aa69Db8c53E504EF22615390EE9Eb72cb8bE498);

   constructor(ActivePool _x1) {

      x1 = ActivePool(_x1);

   }

   function testUncheck(ActivePool _x1) external payable {
      bytes calldata data = bytes("0x1e18");
      x1.flashLoan(
         address(_x1),
         address(0x9Aa69Db8c53E504EF22615390EE9Eb72cb8bE498),
         uint256(1e18),
         data);
   }

   }
```
The flashLoan function performs an unchecked transfer of amount to the receiver contract. 
An attacker can manipulate the receiver contract to exploit this vulnerability, for example, by implementing a malicious onFlashLoan function that doesn't return the expected FLASH_SUCCESS_VALUE. 
This allows the attacker to manipulate the flow of the flash loan and potentially exploit it.
## Tools Used
VS Code.
## Recommended Mitigation Steps
Utilise OpenZeppelin SafeERC20's safetransfer & safetransferFrom methods.

## [L-03] Approve front running attack in EBTCToken contract
## Impact
Losses to Users: The main linked impact is upon users who may be victim to front running. 
Users might be affected by economic shortfall while users' transactions get front-run by hackers, making them to pay more gas fees or get incorrect prices.
There is no way to safely decrease or increase the amount of the token as the owner can only be the contract.
The recipient can exploit this by pretending to be the sender and sending token as the sender to themselves, the attacker or malicious recipient. 
Also, if the sender updates the amount they are trying to send then the malicious recipient can withdraw both amounts from the sender's account.
Hencefotrh a front-running attack on the ERC20 token.
Hence the function can front-run by manipulating the approve function.

## Proof of Concept
**Vulnerable approve function**
```sol
// ln 129-132
    function approve(address spender, uint256 amount) external override returns (bool) {
        _approve(msg.sender, spender, amount);
        return true;
    }
```
**Exploit approve function**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testApprove(EBTCToken _x1) external payable {
      
      x1.approve(address(0xPublicSpenderAddress), uint256(1e18));

   }

   }
```
**Vulnerable transferFrom function with approve**
```sol
// ln 134-150
    function transferFrom(
        address sender,
        address recipient,
        uint256 amount
    ) external override returns (bool) {
        _requireValidRecipient(recipient);
        _transfer(sender, recipient, amount);


        uint256 cachedAllowance = _allowances[sender][msg.sender];
        if (cachedAllowance != type(uint256).max) {
            require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");
            unchecked {
                _approve(sender, msg.sender, cachedAllowance - amount);
            }
        }
        return true;
    }
```
**Exploit transferFrom with approve function**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testTransfer(EBTCToken _x1) external payable {
      
      x1.transferFrom(address(0xPublicSpenderAddress), address(_x1), uint256(1e18));

   }

   }
```
**Vulnerable permit function**
```sol
// ln 199-221
    function permit(
        address owner,
        address spender,
        uint256 amount,
        uint256 deadline,
        uint8 v,
        bytes32 r,
        bytes32 s
    ) external override {
        require(deadline >= block.timestamp, "EBTC: expired deadline");
        bytes32 digest = keccak256(
            abi.encodePacked(
                "\x19\x01",
                domainSeparator(),
                keccak256(
                    abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
                )
            )
        );
        address recoveredAddress = ecrecover(digest, v, r, s);
        require(recoveredAddress == owner, "EBTC: invalid signature");
        _approve(owner, spender, amount);
    }
```
**Exploit permit with approve function**
```sol
// SPDX-License-Identifier: MIT

pragma solidity >=0.8.17;

import "./EBTCToken.sol";

contract tEBTCToken {

   EBTCToken public x1;

   bytes32 r = bytes32("0x10000000000000000000000000000");
   bytes32 s = bytes32("0x7FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF5D576E7357A4501DDFE92F46681B20A0");
   uint8 v = uint8(27);

   constructor(EBTCToken _x1) {

      x1 = EBTCToken(_x1);

   }

   function testPermit(EBTCToken _x1) external payable {
      
      x1.permit(
         address(_x1),
         address(0xPublicSpenderAddress),
         uint256(1e18),
         uint256(1e14),
         uint8(27),
         bytes32("0x10000000000000000000000000000"),
         bytes32("0x7FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF5D576E7357A4501DDFE92F46681B20A0"));
   }

   }
```

**Manual POC**
**Approve Function**
The approve() function takes control of the current funds even if the customer already utilised it or didn't, hence no chance to elevate or reduce funds by a particular value holistically but only in the case that the token possessor is the smart contract, not the account address.
Which potentially leads to misconduct by a token recipient when the malicious recipient attempt the transfer of particular tokens out of the victim's account who is sending it.
At the same time, it is possible that the sender makes a decision to update the amount and calls an extra approve transaction, and then the recipient is able to see this transaction prior to it's being mined and has the ability to take the tokens from the two transactions, hence, illegally taking tokens from the pending and non pending transactions. 
This is called front-running attack within the ERC20 Approve method.
The method approve is possibly front-run by misuising the _approve method.

**transferFrom with Approve function**
The transferFrom() functions can trump the current available fund even if the sender has previously sent it or not, hence there isn't a method to send more or send less funds by a specific amount atomically as the token possessor needs to be smart contract, and not a user address.
This can be misused by the token recipient when he/she attempts to transfer certain tokens from the spender's account.
In the mean time, if the spender makes a decision to update the value and calls a second approve transaction, the recipient can see the pending transaction and can take tokens from the pending transactions, hence, getting tokens from the two transactions. 
Known as a front-running attack within the ERC20 Approve method.
The method transferFrom is misused in a front-run by misusing the _approve method.

**Permit with approve function**
The permit function trumps the existing allowance even if the spender used it before or not, hence having no chance to increment or decrement the allowance with a certain value atomically but only in the case that the token owner is the smart contract.
Which can be manipulated by one token receiver whilst they attempt to extract tokens from the sender's account address.
All the while, let us say the sender tries to update the amount and sends a second permit or approve transfer, the receiver would see the transfer prior to its mining and can take tokens from the two transactions, hence, taking tokens from the two transfers. Being a front-running attack on the ERC20 Approve method.
The method permit is potentially front-run by manipulating the _approve method.

## Tools Used
VS Code.
## Recommended Mitigation Steps
Just utilise the approve method of the ERC/BEP standard to update the allowed value to 0 or from 0 (wait until the transaction is committed and approved).
Token possessor must confirm the first transaction has been mined from N to 0, that is, that the sender did not transfer a part of N allowed tokens prior to the first transaction was committed. 
These checks are doable utilising complicated blockchain explorers like `[Etherscan.io](https://etherscan.io/)`
Alternative ways to avoid the vulnerability is to approve token transfers solely to smart contracts that are verified code which do not contain business logic for carrying front running attacks also to accounts owned by users you know well.