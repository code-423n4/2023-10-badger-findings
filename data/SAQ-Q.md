
## Summary

### Low Risk Issues

no | Issue |Instances|
|-|:-|:-:|
| [L-01] | Loss of precision | 3 | 
| [L-02] | Consider implementing two-step procedure for updating protocol addresses | 1 | 
| [L-03] | Missing checks for address(0x0) in the constructor | 15 | 
| [L-04] | receive()/payable fallback() function does not authorize requests | 1 | 
| [L-05] | Empty receive() function | 1 | 


## Low Risk Issues

### [L-1] Loss of precision

Division by large numbers may result in the result being zero, due to solidity not supporting fractions. Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator

```solidity
file: /contracts/contracts/LiquidationLibrary.sol
 
882        uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882


```solidity
file: contracts/contracts/CdpManagerStorage.sol

564        uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

567        uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L564


```solidity
file: /contracts/contracts/PriceFeed.sol

801            (_scaledDecimal *
                uint256(_ethBtcAnswer) *
                uint256(_stEthEthAnswer) *
                EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L801-L804


### [L-2] Consider implementing two-step procedure for updating protocol addresses

A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must 'accept' the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement EIP-165, and to have the 'set' functions ensure that the recipient is of the right interface type.

```solidity
file: /contracts/contracts/CdpManager.sol

946    function updateCdp(
        bytes32 _cdpId,
        address _borrower,
        uint256 _coll,
        uint256 _debt,
        uint256 _newColl,
        uint256 _newDebt
    ) external {
        _requireCallerIsBorrowerOperations();

        _setCdpCollShares(_cdpId, _newColl);
        _setCdpDebt(_cdpId, _newDebt);

        uint256 stake = _updateStakeAndTotalStakes(_cdpId);

        emit CdpUpdated(
            _cdpId,
            _borrower,
            msg.sender,
            _debt,
            _coll,
            _newDebt,
            _newColl,
            stake,
            CdpOperation.adjustCdp
        );
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946-L973


### [L-3] Missing checks for address(0x0) in the constructor

```solidity
file: /contracts/contracts/ActivePool.sol

54        cdpManagerAddress = _cdpManagerAddress;
55        collateral = ICollateralToken(_collTokenAddress);
56        collSurplusPoolAddress = _collSurplusAddress;
57        feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54-L57C


```solidity
file: /contracts/contracts/BorrowerOperations.sol

117        cdpManager = ICdpManager(_cdpManagerAddress);
118        collSurplusPool = ICollSurplusPool(_collSurplusPoolAddress);
119        sortedCdps = ISortedCdps(_sortedCdpsAddress);
120        ebtcToken = IEBTCToken(_ebtcTokenAddress);
121        feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L117-L121


```solidity
file: /contracts/contracts/LeverageMacroFactory.sol

29        borrowerOperations = _borrowerOperationsAddress;
        activePool = _activePool;
        cdpManager = _cdpManager;
        ebtcToken = _ebtc;
        stETH = _coll;
        sortedCdps = _sortedCdps;
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29-L35





### [L-4] receive()/payable fallback() function does not authorize requests

Having no access control on the function (e.g. require(msg.sender == address(weth))) means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue mistakenly-sent Ether.

```solidity
file: /contracts/contracts/SimplifiedDiamondLike.sol

160   receive() external payable {
        // PHP is my favourite language
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162


### [L-5] Empty receive() function

If the intention is for Ether sent by a caller to be used for an actual purpose (i.e. the function is not just a WETH withdraw() handler), the function should call another function (e.g. call weth.deposit() and use the token on the caller's behalf) or at least emit an event to track that funds were sent directly to it.


```solidity
file: /contracts/contracts/SimplifiedDiamondLike.sol

160   receive() external payable {
        // PHP is my favourite language
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162

