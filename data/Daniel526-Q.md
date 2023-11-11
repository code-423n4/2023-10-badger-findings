## A. Possible underflow when decreasing system Debt:
[Link](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L207-L214)
If `_amount` is greater than `systemDebt` and not properly handled elsewhere in the code, it could lead to an underflow. Underflows can potentially be exploited to manipulate balances and disrupt the functioning of the contract.
## Impact:
Incorrect accounting of system debt could distort the protocol's financial health and risk assessments. It may provide an inaccurate representation of the protocol's ability to manage and cover its debt, potentially leading to suboptimal decisions by protocol users or administrators.
## Mitigation:
```solidity
function decreaseSystemDebt(uint256 _amount) external override {
    _requireCallerIsBOorCdpM();

    require(_amount <= systemDebt, "ActivePool: Amount exceeds systemDebt");

    uint256 cachedSystemDebt = systemDebt - _amount;

    systemDebt = cachedSystemDebt;
    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
}
```
## B. Unverified Collateral Token Transfer in 'flashLoan' Function
[Link](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L261-L310)
The `flashLoan` function allows borrowers to borrow stETH tokens through a flash loan. In this function, `collateral` tokens are transferred to the `receiver` address using the `collateral.transfer(address(receiver), amount);` statement. However, the code does not verify whether the transfer was successful. If the transfer fails for any reason, such as an out-of-gas condition or insufficient token balance, the contract will proceed with the remaining operations, potentially leading to unexpected behavior or loss of funds.
## Impact:
 If the collateral token transfer to the `receiver` address fails, it may result in the loss of funds for the flash loan borrower. This can lead to unexpected financial consequences for the borrower, potentially disrupting their intended operations
## Mitigation:
```
// ...
// Use a require statement to check the success of the transfer
require(collateral.transfer(address(receiver), amount), "ActivePool: Transfer failed");
// ...

```
## C. Duplicate `_feeRecipientAddress`
[Link](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150)
The `setFeeRecipientAddress` function in the provided contract allows for the setting of a new `_feeRecipientAddress` without verifying that it is different from the current one. Here is the relevant code snippet:

```solidity
function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
    require(
        _feeRecipientAddress != address(0),
        "BorrowerOperations: Cannot set feeRecipient to zero address"
    );

    cdpManager.syncGlobalAccounting();

    feeRecipientAddress = _feeRecipientAddress;
    emit FeeRecipientAddressChanged(_feeRecipientAddress);
}
```
The function correctly checks that the new `_feeRecipientAddress` is not the zero address, but it does not include a check to ensure that it is not the same as the current `feeRecipientAddress`. Without this check, the contract allows setting the same fee recipient address again, which may not be intended and could lead to unintended behavior.
## Impact:
The impact of this issue is that it may allow for the accidental or intentional setting of the same fee recipient address multiple times. This could lead to unexpected behavior in the contract and disrupt its intended governance or fee distribution mechanisms.

Mitigation:
Check in the `setFeeRecipientAddress` function to verify that the new address is different from the current `feeRecipientAddress`.
## D. Array Out-of-Bounds Access in _getCdpIdsToRemove Function
[Link](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L288-L485)
## Impact
In this scenario, the `_getCdpIdsToRemove` function attempts to access 5 CDPs, but there are only 3 CDPs in the specified range. As a result, the function may access non-existent CDPs, leading to array out-of-bounds access. This can cause runtime errors, unexpected behavior, and potential inconsistencies in the state of the protocol.

## Proof of Concept
The `_getCdpIdsToRemove` function is designed to retrieve an array of CDP IDs within a specified range. However, it lacks sufficient bounds checking for the parameter `_total`, which represents the number of CDPs to be retrieved. If `_total` exceeds the actual count of CDPs in the specified range, the function may attempt to access non-existent CDPs, leading to array out-of-bounds access. This can result in runtime errors and inconsistencies in the state of the protocol.
```solidity
function _getCdpIdsToRemove(
    bytes32 _start,
    uint256 _total,
    bytes32 _end
) internal view returns (bytes32[] memory) {
    uint256 _cnt = _total;
    bytes32 _id = _start;
    bytes32[] memory _toRemoveIds = new bytes32[](_total);
    while (_cnt > 0 && _id != bytes32(0)) {
        _toRemoveIds[_total - _cnt] = _id;
        _cnt = _cnt - 1;
        _id = sortedCdps.getNext(_id);
    }
    require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");
    require(
        _toRemoveIds[_total - 1] == _end,
        "CdpManager: batchRemoveSortedCdpIds check end error"
    );
    return _toRemoveIds;
}
```
Let's consider a scenario where the `_getCdpIdsToRemove` function is called with an incorrectly specified `_total` parameter. An attacker intentionally provides a value greater than the actual number of CDPs in the specified range, leading to array out-of-bounds access.
```solidity
// Assume there are 3 CDPs in the specified range: Cdp1, Cdp2, Cdp3

// Incorrectly specifying _total as 5, which is greater than the actual number of CDPs
bytes32[] memory result = _getCdpIdsToRemove(Cdp1, 5, Cdp3);

// The _getCdpIdsToRemove function attempts to access 5 CDPs, but there are only 3
// This can lead to array out-of-bounds access, causing unexpected behavior
```

## Mitigation
Ensure that the value of _total is always within the valid range of existing CDPs in the specified range.

