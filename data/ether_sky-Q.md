I believe this is an incorrect check for `partial debt size`. 
Partial `liquidation` or `redemption` should reserve `collateral` of at least 2 `stEth`. 
We have below check for this.
```
function _requirePartialLiqCollSize(uint256 _entireColl) internal pure {
    require(
        _entireColl >= MIN_NET_STETH_BALANCE,
        "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
    );
}
```
However, this check adds another `limitation` to the `debt size`.
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906
```
require(
     (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
           _entireDebt,
     "LiquidationLibrary: Partial debt liquidated must be less than total debt"
);
```