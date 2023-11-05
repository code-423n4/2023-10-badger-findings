### Report 1:
Typographical Error in L48 & L61 of CdpManagerStorage.sol contract, It should be "purposes" not "pruposes"
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L48
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L61
```solidity
  /// @dev Internal notify called by Redemptions and Liquidations
>>>    /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
    function _startGracePeriod(uint256 _tcr) internal {
```
```solidity
>>>   /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
    /// @dev Internal notify called by Redemptions and Liquidations
    function _endGracePeriod(uint256 _tcr) internal {
```
###  Report 2:
## Title 
Code Reversion due to improper Validation
## Impact
Missing Validation to ensure prevChainlinkResponse is not zero would allow reversion and Denial of Service if  _currentRoundEthBtcId or _currentRoundStEthEthId is equal 1 in the _getPrevChainlinkResponse(...) function of the PriceFeed.sol contract.
## Proof of Concept
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L722

As seen in the code provided below and as noted by the arrows, subtraction is done for _currentRoundEthBtcId and _currentRoundStEthEthId i.e minus 1, the problem is id for prevChainlinkResponse would be zero which opens up reversion since this zero value is used to interact with external contracts as noted in the "getRoundData(...)" function, thereby causing denial of service.
```solidity
   function _getPrevChainlinkResponse(
>>>        uint80 _currentRoundEthBtcId,
>>>        uint80 _currentRoundStEthEthId
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
            ...
        }

        // Try to get latest prices data from prev round:
        int256 ethBtcAnswer;
        int256 stEthEthAnswer;
>>>        try ETH_BTC_CL_FEED.getRoundData(_currentRoundEthBtcId - 1) returns (
            uint80 roundId,
            int256 answer,
            uint256,
            /* startedAt */
            uint256 timestamp,
            uint80 /* answeredInRound */
        ) {
            ethBtcAnswer = answer;
            prevChainlinkResponse.roundEthBtcId = roundId;
            prevChainlinkResponse.timestampEthBtc = timestamp;
        } catch {
            // If call to Chainlink aggregator reverts, return a zero response with success = false
            return prevChainlinkResponse;
        }

>>>        try STETH_ETH_CL_FEED.getRoundData(_currentRoundStEthEthId - 1) returns (
            uint80 roundId,
            int256 answer,
            uint256,
            /* startedAt */
            uint256 timestamp,
            uint80 /* answeredInRound */
        ) {
            stEthEthAnswer = answer;
            prevChainlinkResponse.roundStEthEthId = roundId;
            prevChainlinkResponse.timestampStEthEth = timestamp;
        } catch {
            // If call to Chainlink aggregator reverts, return a zero response with success = false
            return prevChainlinkResponse;
        }
```
## Tools Used
Manual Review
## Recommended Mitigation Steps
The _getPrevChainlinkResponse(...) function should be adjusted to ensure return of prevChainlinkResponse if _currentRoundStEthEthId or _currentRoundEthBtcId is one instead of reversion as edited below.
```solidity
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
+++     if (_currentRoundEthBtcId == 1 || _currentRoundStEthEthId == 1) {
+++         return prevChainlinkResponse;
+++     }
 ...
```