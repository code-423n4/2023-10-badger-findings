#  Low Risk Issues

| Number | Issue |
|--------|--------|
|[L-01]| Redundant requirement `require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");` in function `_openCdp()` |
|[L-02]| Unused array `_liqFlags`  |
|[L-03]| Function `LiquidationLibrary._redistributeDebt()` shouldn't return if `_debt == 0`  |
|[L-04]| Typo in comments  |
|[L-05]| Inappropriate check in function `ActivePool.flashLoan()`  |

### [L-01] Redundant requirement `require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");` in function `_openCdp()`

In the function `BorrowerOperations._openCdp()`, the requirement `vars.netStEthBalance > 0` in line 463 is redundant due to the check in [line 454](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L454):

```solidity
454        _requireAtLeastMinNetStEthBalance(vars.netStEthBalance);
```

Therefore, the requirement `vars.netStEthBalance > 0` in [line 463](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L463C17-L463C37) is redundant.

### [L-02] Unused array `_liqFlags`

In the function `LiquidationLibrary._getTotalFromBatchLiquidate_RecoveryMode()`, the array `_liqFlags` is created to denote which iterations are liquidated successfully. However, this array is neither used to return a value nor utilized for event emission, resulting in unnecessary gas consumption for users.

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L751
```solidity
751        bool[] memory _liqFlags = new bool[](_cnt);
```

### [L-03] Function `LiquidationLibrary._redistributeDebt()` shouldn't return if `_debt == 0`

In the function `LiquidationLibrary._redistributeDebt()`, when `_debt == 0`, the function immediately returns, assuming there is no debt to distribute. However, before this function call, the `totalStake` can possibly decrease, causing the value of `lastEBTCDebtErrorRedistribution >= _totalStakes` and allowing redistribution even when `_debt = 0`.

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L862C1-L865
```solidity
862    function _redistributeDebt(uint256 _debt) internal {
863        if (_debt == 0) {
864            return;
865        }
```

### [L-04] Typos in comments

* "recieved" should be corrected to "received" in [ActivePool.sol#L239](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L239):

```solidity
239    /// @notice Notify that stETH collateral shares have been received, updating internal accounting accordingly
```

* "duratin" should be corrected to "duration" in [CdpManagerStorage.sol#L108](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L108):

```solidity
108     /// @notice Set grace period duration
```

### [L-05] Inappropriate check in function `ActivePool.flashLoan()`

Function `ActivePool.flashLoan()` incorporates two checks to ensure the correct processing of the flash loan method:

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L294-L301

```solidity
294        require(
295            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296            "ActivePool: Must repay Balance"
297        );
298        require(
299            collateral.sharesOf(address(this)) >= systemCollShares,
300            "ActivePool: Must repay Share"
301        );
```

However, using the value of `systemCollShares` for these two checks doesn't make sense because the amount of `stETH` present in the ActivePool is not solely represented by `systemCollShares`. It also includes the liquidator reward and the value of `feeRecipientCollShares`. Therefore, these checks should be replaced by verifying the balance of stETH before and after the flash loan's callback. 