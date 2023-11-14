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

G-2 Price Feed decimal calls can be reduced to 2 from 4
The Price Feed checks the decimals of the two Chainlink price feeds when it tries to get the current and previous round values from the price feeds. This amount to four calls altogether. 

`decimals()` called twice when previous round data is fetched

```
    function _getPrevChainlinkResponse(
        uint80 _currentRoundEthBtcId,
        uint80 _currentRoundStEthEthId
    ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) {
        // If first round, early return
        // Handles revert from underflow in _currentRoundEthBtcId - 1
        // and _currentRoundStEthEthId - 1
        // Behavior should be indentical to following block if this revert was caught
        if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {
            return prevChainlinkResponse;
        }

        // Fetch decimals for both feeds:
        uint8 ethBtcDecimals;
        uint8 stEthEthDecimals;

        try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {
            // If call to Chainlink succeeds, record the current decimal precision
            ethBtcDecimals = decimals;
        } catch {
            // If call to Chainlink aggregator reverts, return a zero response with success = false
            return prevChainlinkResponse;
        }

        try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {
            // If call to Chainlink succeeds, record the current decimal precision
            stEthEthDecimals = decimals;
        } catch {
            // If call to Chainlink aggregator reverts, return a zero response with success = false
            return prevChainlinkResponse;
        }
```

`decimals()` called twice  when current round data is fetched

```
    function _getCurrentChainlinkResponse()
        internal
        view
        returns (ChainlinkResponse memory chainlinkResponse)
    {
        // Fetch decimals for both feeds:
        uint8 ethBtcDecimals;
        uint8 stEthEthDecimals;

        try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {
            // If call to Chainlink succeeds, record the current decimal precision
            ethBtcDecimals = decimals;
        } catch {
            // If call to Chainlink aggregator reverts, return a zero response with success = false
            return chainlinkResponse;
        }

        try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {
            // If call to Chainlink succeeds, record the current decimal precision
            stEthEthDecimals = decimals;
        } catch {
            // If call to Chainlink aggregator reverts, return a zero response with success = false
            return chainlinkResponse;
        }
```

Since two of the calls will certainly return the same values the call can be done once and cached to save gas spent on the unnecessary static calls