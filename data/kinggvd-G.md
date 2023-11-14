The code below may produce timeouts even if the response did not actually timeout and returned a valid response due to ms difference, thus wasting resources. Consider adding a small buffer when _response.success == true.

```
    function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {
        return block.timestamp - _timestamp > _timeout;
    }

to

    function _responseTimeout(uint256 _timestamp, uint256 _timeout, uint256 _eps) internal view returns (bool) {
        return block.timestamp - _timestamp > _timeout + _eps;
    }
```

in e.g
```
    function _chainlinkIsFrozen(ChainlinkResponse memory _response) internal view returns (bool) {
        return
            _responseTimeout(_response.timestampEthBtc, TIMEOUT_ETH_BTC_FEED) ||
            _responseTimeout(_response.timestampStEthEth, TIMEOUT_STETH_ETH_FEED);
    }

    function _fallbackIsFrozen(
        FallbackResponse memory _fallbackResponse
    ) internal view returns (bool) {
        return
            _fallbackResponse.timestamp > 0 &&
            _responseTimeout(_fallbackResponse.timestamp, fallbackCaller.fallbackTimeout());
    }
```