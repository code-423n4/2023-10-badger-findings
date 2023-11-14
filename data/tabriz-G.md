## [GAS-1] Splitting require() statements that use && saves gas

```
 require(
            recoveredAddress != address(0) && recoveredAddress == _borrower,
            "BorrowerOperations: Invalid signature"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734C8-L737C11

```
 require(
            _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
            "Max fee percentage must be between redemption fee floor and 100%"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762C8-L765C11

```
 require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261C8-L264C11

```
  require(
            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
            "CdpManagerStorage: remove non-exist or non-active CDP!"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466C7-L470C1

```
  require(
            CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
            "CdpManager: Only one cdp in the system"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653C7-L656C11

```
 require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );
        require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296C8-L303C11

```
   require(
            !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                !_chainlinkIsFrozen(chainlinkResponse),
            "PriceFeed: Chainlink must be working and current"
        );
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79C6-L83C11

## [G-02] Use double if statements instead of &&
If the if statement has a logical AND and is not followed by an else statement, it can be replaced with 2
if statements.

```
 if (!_isDebtIncrease && _debtChange > 0) {
            _requireValidDebtRepayment(vars.debt, vars.netDebtChange);
            _requireSufficientEbtcTokenBalance(msg.sender, vars.netDebtChange);
            _requireNonZeroDebt(vars.debt - vars.netDebtChange);
        }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393C8-L397C10

```
 // only for active cdps
            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
                vars.ICR = getSyncedICR(vars.cdpId, _price);

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L818C12-L821C1

```
if (_newIndex > _oldIndex && totalStakes > 0) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512C9-L512C56

```
  if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
            (
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796C7-L797C14

```
 if (
                    !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                    !_chainlinkIsFrozen(chainlinkResponse)
                ) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226C16-L229C20

```
 if (maxNodes > 0 && i >= maxNodes) {
             
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259C12-L261C14

```
  if (maxNodes > 0 && i >= maxNodes) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330C11-L330C49

```
 if (!_exist) {
            Node memory _node = data.nodes[_id];
            _exist = _id != dummyId && (_node.nextId != dummyId && _node.prevId != dummyId);
        }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L521C8-L524C10

```
 if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {
            return (dummyId, _startId);
        }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621C8-L623C10

```
 if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
            return (_startId, dummyId);
        }
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644C8-L646C10

## [G‑03] Use a more recent version of Solidity
Use a Solidity version of at least 0.8.2 to get simple compiler automatic inlining.
Use a Solidity version of at least 0.8.3 to get better struct packing and cheaper multiple storage reads.
Use a Solidity version of at least 0.8.4 to get custom errors, which are cheaper at deployment than
revert()/require() strings.
Use a Solidity version of at least 0.8.10 to have external calls skip contract existence checks if the external call has a return value.

```
pragma solidity 0.8.17;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3C24-L3C24

```
pragma solidity 0.8.17;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3C1-L3C24

```
pragma solidity 0.8.17;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762C8-L765C11