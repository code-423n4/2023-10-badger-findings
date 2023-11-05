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