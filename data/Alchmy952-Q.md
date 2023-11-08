Line of Code
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol

Impact
There is a missing check or error handling for potential division by zero(line 804) in PriceFeed.sol. Absence of this can lead to a runtime error upon execution of a contract transaction.
 
Proof of Concept
   function _formatClAggregateAnswer(
        int256 _ethBtcAnswer,
        int256 _stEthEthAnswer,
        uint8 _ethBtcDecimals,
        uint8 _stEthEthDecimals
    ) internal view returns (uint256) {
        uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals
            ? _stEthEthDecimals
            : _ethBtcDecimals;
        uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
            ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
            : 10 ** (_ethBtcDecimals - _stEthEthDecimals);
        return
            (_scaledDecimal *
                uint256(_ethBtcAnswer) *
                uint256(_stEthEthAnswer) *
                EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);
    }
}

Mitigation
To remediate this, import "@openzeppelin/contracts/utils/math/SafeMath.sol"; should be included in the smart contract