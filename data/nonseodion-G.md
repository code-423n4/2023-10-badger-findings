G-1 `_formatClAggregateAnswer` can be completely replaced to save gas

The function `_formatClAggregateAnswer` can be completely replaced with:

```
    function _formatClAggregateAnswer(
        int256 _ethBtcAnswer,
        int256 _stEthEthAnswer,
        uint8 _ethBtcDecimals,
        uint8 _stEthEthDecimals
    ) internal view returns (uint256) {

        return
            (
                uint256(_ethBtcAnswer) *
                uint256(_stEthEthAnswer) *
                EbtcMath.DECIMAL_PRECISION) / 10 ** (_ethBtcDecimals + _stEthEthDecimals);
    }
```

The function above simply scales the price first with `EbtcMath.DECIMAL_PRECISION` and eliminates the decimals of the stEthEth and ethBtc prices with `10 ** (_ethBtcDecimals + _stEthEthDecimals)` leaving the price to have only `EbtcMath.DECIMAL_PRECISION` decimal points.

Gas usage of old implementation: 4519
Gas usage of suggested implementation: 3910

G-2 