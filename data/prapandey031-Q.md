**Low Risk Issues**
----------------------------------

**[LOW-1] No default value available for the ```Cdps[cdpId].arrayIndex``` in CdpManagerStorage.sol:**
There is no default value for the ```Cdps[cdpId].arrayIndex``` in CdpManagerStorage.sol. Zero(0) cannot be considered a default value for this as it would be the value for the 1st CDP in the ```CdpIds[]``` array. 

***Recommended Mitigation Steps:***
Start valuing ```Cdps[cdpId].arrayIndex``` by 1 and not zero(0). This would let it get the zero(0) value as a default.


**[LOW-2] No proper set of ```Cdps[_cdpId].arrayIndex``` in ```_removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength)```:**
The ```Cdps[_cdpId].arrayIndex``` is not set to default in ```_removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength)```.

**Proof of Concept:**
In the ```_removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength)``` function of CdpManagerStorage.sol, the ```Cdps[_cdpId].arrayIndex``` is not set to zero(0) (the default value) after popping it out of the ```CdpIds[]``` array:
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463
```
function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
        Status cdpStatus = Cdps[_cdpId].status;
        // It’s set in caller function `_closeCdp`
        require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );

        uint128 index = Cdps[_cdpId].arrayIndex;
        uint256 length = cdpIdsArrayLength;
        uint256 idxLast = length - 1;

        require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

        bytes32 idToMove = CdpIds[idxLast];

        CdpIds[index] = idToMove;
        Cdps[idToMove].arrayIndex = index;
        emit CdpArrayIndexUpdated(idToMove, index);

        CdpIds.pop();
    }
```
The ```_cdpId``` is the id of the cdp to be removed from the ```CdpIds[]``` array. After removing it from the array, ```Cdps[_cdpId].arrayIndex``` is not set to the default. 
The problem is that there is no default value to set for the ```Cdps[_cdpId].arrayIndex``` as setting it to zero(0) is not a solution (since zero(0) is the index of the 1st cdp in the ```CdpIds[]``` array).

***Recommended Mitigation Steps:***
Choose a default value for ```Cdps[_cdpId].arrayIndex``` and set it in the ```_removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength)``` function.


**[LOW-3] ```_requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR)``` has an unused parameter:**
The ```_requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR)``` function has an unused paramater ```_price```. 

**Proof of Concept:**
The ```_price``` parameter in the ```_requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR)``` function of CdpManager.sol is unused (LOC-757):
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757
```
function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {
        require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");
    }
```

***Recommended Mitigation Steps:***
Avoid using ```_price``` if not required.


**[LOW-4] Wrong implementation in the ```_requireValidAdjustmentInCurrentMode()``` function of BorrowerOperations.sol:**
There is an instance of incorrect implementation in BorrowerOperations.sol.

**Proof of Concept:**
In the ```_requireValidAdjustmentInCurrentMode()``` function of BorrowerOperations.sol:
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852
```
function _requireValidAdjustmentInCurrentMode(
        bool _isRecoveryMode,
        uint256 _stEthBalanceDecrease,
        bool _isDebtIncrease,
        AdjustCdpLocals memory _vars
    ) internal {
        /*
         *In Recovery Mode, only allow:
         *
         * - Pure collateral top-up
         * - Pure debt repayment
         * - Collateral top-up with debt repayment
         * - A debt increase combined with a collateral top-up which makes the
         * ICR >= 150% and improves the ICR (and by extension improves the TCR).
         *
         * In Normal Mode, ensure:
         *
         * - The new ICR is above MCR
         * - The adjustment won't pull the TCR below CCR
         */

        _vars.newTCR = _getNewTCRFromCdpChange(
            collateral.getPooledEthByShares(_vars.collSharesChange),
            _vars.isCollIncrease,
            _vars.netDebtChange,
            _isDebtIncrease,
            _vars.price
        );

        if (_isRecoveryMode) {
            _requireNoStEthBalanceDecrease(_stEthBalanceDecrease);
            if (_isDebtIncrease) {
                _requireICRisNotBelowCCR(_vars.newICR);
                _requireNoDecreaseOfICR(_vars.newICR, _vars.oldICR);
            }

            // == Grace Period == //
            // We are in RM, Edge case is Depositing Coll could exit RM
            // We check with newTCR
            if (_vars.newTCR < CCR) {
                // Notify RM
                cdpManager.notifyStartGracePeriod(_vars.newTCR);
            } else {
                // Notify Back to Normal Mode
                cdpManager.notifyEndGracePeriod(_vars.newTCR);
            }
        } else {
            // if Normal Mode
            _requireICRisNotBelowMCR(_vars.newICR);
            _requireNewTCRisNotBelowCCR(_vars.newTCR);

            // == Grace Period == //
            // We are not in RM, no edge case, we always stay above RM
            // Always Notify Back to Normal Mode
            cdpManager.notifyEndGracePeriod(_vars.newTCR);
        }
    }
```

In the comments (LOC-858-865), it is mentioned:
```
/*
         *In Recovery Mode, only allow:
         *
         * - Pure collateral top-up
         * - Pure debt repayment
         * - Collateral top-up with debt repayment
         * - A debt increase combined with a collateral top-up which makes the
         * ICR >= 150% and improves the ICR (and by extension improves the TCR).
```
That is, in recovery mode, ICR must improve and be >= 150%. However, during implementation (LOC-884), ICR is compared to CCR (=125%) and not 150%:
```
if (_isRecoveryMode) {
            _requireNoStEthBalanceDecrease(_stEthBalanceDecrease);
            if (_isDebtIncrease) {
                _requireICRisNotBelowCCR(_vars.newICR);
                _requireNoDecreaseOfICR(_vars.newICR, _vars.oldICR);
            }
```

***Recommended Mitigation Steps:***
Compare ICR with 150% in the above function during recovery mode.

**[LOW-5] Redundant check in BorrowerOperations.sol:**
There are 2 instances of this:

**Instance-1:**

**Proof of Concept:**
In LOC-517, there is an unnecessary check in ```_openCdp()``` function:
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L517
```
// Collision check: collisions should never occur
        // Explicitly prevent it by checking for `nonExistent`
        _requireCdpIsNonExistent(_cdpId);
```
This check has already been performed by ```sortedCdps.insert()``` at LOC-513:
```
bytes32 _cdpId = sortedCdps.insert(_borrower, vars.NICR, _upperHint, _lowerHint);
```
```
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
```
**Instance-2:**

**Proof of Concept:**
In the LOC-463 of BorrowerOperations.sol, there is an unnecessary check:
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463
```
require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");
```
This check has already been performed at LOC-454:
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L454
```
_requireAtLeastMinNetStEthBalance(vars.netStEthBalance);
```

***Recommended Mitigation Steps:***
Consider removing the mentioned redundant check.


**[LOW-6] Non-compliance with OZ ERC-20 standard:**

**Proof of Concept:**
In the ```transferFrom()``` function of EBTCToken.sol, first the transfer happens and then the allowance is spent:
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L134
```
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
However, the opposite happens in the OZ ERC-20 standard; the allowance is spent and then the transfer happens:
https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol#L154
```
function transferFrom(address from, address to, uint256 value) public virtual returns (bool) {
        address spender = _msgSender();
        _spendAllowance(from, spender, value);
        _transfer(from, to, value);
        return true;
    }
```

***Recommended Mitigation Steps:***
Consider complying with the OZ ERC-20 standard in case of the above mentioned function in EBTCToken.sol.




**Non Critical Issues**
----------------------------------

**[NC-1] Wrong comments:**
1) LOC-784, PriceFeed.sol:
Correct comment: 
```
_stEthEthAnswer CL price retrieve from stETH:ETH feed
```

2) LOC-786, PriceFeed.sol:
Correct comment: 
```
_stEthEthDecimals stETH:ETH feed decimals
```

