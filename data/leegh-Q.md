## [N-01] Function names should be camelCase.
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

824:    function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {
```
[[L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L824)]

## [N-02] Use enum values instead of numerics.
CDP status are defined in an enum. Use the enum values instead of numerics when using CDP status.
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

826:        require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831:        require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");
```
[[L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826), [L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831)]