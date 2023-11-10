# Gas Optimization

## Gas 01: In contract/BorrowOperations.sol
[Link to code](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L564C3-L569)
> Gas can be optimized if the call `_requireSufficientEbtcTokenBalance` is made first before `getCdpCollShares` and `getCdpLiquidatorRewardShares` as those two values may not be needed until after the check. If the `_requireSufficientEbtcTokenBalance` call fails, the gas spent on making those calls will be lost. This can save about 82,864 gas if the check fails.
```
       uint256 collShares = cdpManager.getCdpCollShares(_cdpId);
       uint256 debt = cdpManager.getCdpDebt(_cdpId);
       uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

       _requireSufficientEbtcTokenBalance(msg.sender, debt)
```

> The code can be optimized thus:
```
  function decreaseSystemDebt(uint256 _amount) external override { 
       _requireCallerIsBOorCdpM();
       uint256 debt = cdpManager.getCdpDebt(_cdpId);
       
       _requireSufficientEbtcTokenBalance(msg.sender, debt)
       
       uint256 collShares = cdpManager.getCdpCollShares(_cdpId);
       uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

```

## Gas 02: In contracts/ActivePool.sol
[Link to code](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L207-L214)
> In the code below, assigning systemDebt as `systemDebt -= _amount` would save gas and a variable.

> So this is recommended:
```
function decreaseSystemDebt(uint256 _amount) external override {
   _requireCallerIsBOorCdpM();
   systemDebt -= _amount
   emit ActivePoolEBTCDebtUpdated(systemDebt);
```

Instead of this: 
```
   function decreaseSystemDebt(uint256 _amount) external override { 
       _requireCallerIsBOorCdpM();

       uint256 cachedSystemDebt = systemDebt - _amount;

       systemDebt = cachedSystemDebt;
       emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
   }
```