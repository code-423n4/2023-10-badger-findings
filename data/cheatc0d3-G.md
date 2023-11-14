## Gas Optimization Report Badger eBTC

### Minimize State Variable Storage

Using smaller integer types for state variables can significantly reduce gas costs. In `ActivePool.sol`, the state variables `systemCollShares` and `feeRecipientCollShares` are declared as `uint256`. If the range of these variables permits, changing them to `uint128` can save gas.

**Instances:**

```solidity
File: https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L31

uint256 internal systemCollShares;
uint256 internal feeRecipientCollShares;
```

**Proposed Changes:**
```solidity
uint128 internal systemCollShares;
uint128 internal feeRecipientCollShares;
```

### Caching Results of External Functions

Multiple calls to the same external function can be optimized by caching the function's result in a local variable and reusing it.

**Instances:**
```
File: https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104

Multiple calls to collateral.getPooledEthByShares(DECIMAL_PRECISION);
```

**Proposed Changes:**

```solidity
uint256 cachedResult = collateral.getPooledEthByShares(DECIMAL_PRECISION);
uint256 result1 = cachedResult;
uint256 result2 = cachedResult;
```

### Using Custom Errors Instead of Revert Strings

Using custom errors instead of revert strings can save gas, as strings consume more gas.

**Instances:**
```
File: https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104

require(cachedSystemCollShares >= _shares, "!ActivePoolBal");
```

**Proposed Changes:**
```solidity
error InsufficientBalance();

require(cachedSystemCollShares >= _shares, InsufficientBalance());
```

### Use Immutable for Constant Values

Immutable variables are more gas-efficient than regular state variables. In `LeverageMacroReference.sol`, the `theOwner` variable is set once in the constructor and never changed, making it a candidate for immutable.

**Instances:**
```solidity
File: LeverageMacroReference.sol

address internal immutable theOwner;
```

**Proposed Changes:**
```solidity
address internal immutable theOwner;
```
(Note: This is already optimized as the variable is declared immutable.)

### Minimize External Contract Calls

The contract makes several external calls to set approvals. These calls can be optimized by checking if the approval is necessary (i.e., not already set to the desired amount).

**Instances:**
```solidity
File: LeverageMacroReference.sol

ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
stETH.approve(_borrowerOperationsAddress, type(uint256).max);
stETH.approve(_activePool, type(uint256).max);
```

**Proposed Changes:**
```solidity
if (ebtcToken.allowance(address(this), _borrowerOperationsAddress) < type(uint256).max) {
    ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
}
// Similar checks for other approve calls
```

### Efficient Use of Storage Types

The contract uses `uint256` for token allowances. If the expected range of these values is within the limits of a smaller integer type, using a smaller type like `uint128` could save gas.

**Instances:**
```solidity
File: LeverageMacroReference.sol

ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
stETH.approve(_borrowerOperationsAddress, type(uint256).max);
stETH.approve(_activePool, type(uint256).max);
```

**Proposed Changes:**
```solidity
// If the maximum expected allowance is within uint128 range
ebtcToken.approve(_borrowerOperationsAddress, type(uint128).max);
stETH.approve(_borrowerOperationsAddress, type(uint128).max);
stETH.approve(_activePool, type(uint128).max);
```

### Avoid Redundant State Changes

The contract sets token allowances to their maximum in the constructor and provides a function to reset them. It's important to ensure that these allowances are not set redundantly, as state changes are costly.

**Instances:**
```solidity
File: LeverageMacroReference.sol

// In constructor and resetApprovals function
ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
stETH.approve(_borrowerOperationsAddress, type(uint256).max);
stETH.approve(_activePool, type(uint256).max);
```

**Proposed Changes:**
```solidity
// Before setting the approval, check if it's already set to the desired amount
if (ebtcToken.allowance(address(this), _borrowerOperationsAddress) < type(uint256).max) {
    ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
}

```
## Gas Optimization Report for `LeverageMacroFactory.sol`

### Use Immutable for Constant Values

Immutable variables are more gas-efficient than regular state variables. In `LeverageMacroFactory.sol`, the contract uses immutable variables for contract addresses, which is an efficient practice.

**Instances:**
```solidity
File: LeverageMacroFactory.sol

address public immutable borrowerOperations;
address public immutable activePool;
address public immutable cdpManager;
address public immutable ebtcToken;
address public immutable stETH;
address public immutable sortedCdps;
```

**Proposed Changes:**
None required. The contract already uses immutable variables efficiently.

### Efficient Contract Deployment

The `deployNewMacro` function creates a new instance of `LeverageMacroReference`. It's important to ensure that the deployment is as efficient as possible, especially in terms of gas usage.

**Instances:**
```solidity
File: LeverageMacroFactory.sol

function deployNewMacro(address _owner) public returns (address) {
    address addy = address(new LeverageMacroReference(...));
    emit DeployNewMacro(_owner, addy);
    return addy;
}
```

**Proposed Changes:**
Consider using a proxy pattern for deploying `LeverageMacroReference` instances to save gas on deployment if the contract logic does not change frequently.

### Event Optimization

The `DeployNewMacro` event is emitted every time a new macro is deployed. Ensure that the data included in the event is necessary and optimized for gas.

**Instances:**
```solidity
File: LeverageMacroFactory.sol

event DeployNewMacro(address indexed sender, address indexed newContractAddress);
```

**Proposed Changes:**
Review the event parameters to ensure they are necessary. If the `sender` is always the transaction sender (`msg.sender`), it might not be needed in the event.

### Function Visibility and Gas

The `deployNewMacro` function is public, which is more expensive in terms of gas than external. Consider changing the visibility to external if the function is only meant to be called externally.

**Instances:**
```solidity
File: LeverageMacroFactory.sol

function deployNewMacro(address _owner) public returns (address) {
    // Function logic
}
```

**Proposed Changes:**
```solidity
function deployNewMacro(address _owner) external returns (address) {
    // Function logic
}
```

These recommendations aim to optimize the gas usage of the `LeverageMacroFactory` contract by using efficient contract deployment methods, optimizing events, and adjusting function visibility for better gas efficiency.

## Gas Optimization Report for `LeverageMacroDelegateTarget.sol`

### Minimize State Variable Storage

The contract `LeverageMacroDelegateTarget` inherits from `LeverageMacroBase`. It's important to review the state variables in the base contract to ensure they are optimized for gas usage.

**Instances:**
```solidity
File: LeverageMacroBase.sol

// Review state variables for optimization.
```

**Proposed Changes:**
Ensure state variables are of the smallest suitable types and consider packing multiple small variables into a single storage slot.

### Efficient Function Calls

The `owner` function in `LeverageMacroDelegateTarget` makes an external call to get the owner's address. This can be optimized if the owner's address is unlikely to change.

**Instances:**
```solidity
File: LeverageMacroDelegateTarget.sol

function owner() public override returns (address) {
    address _owner = IOwnerLike(address(this)).owner();
    return _owner;
}
```

**Proposed Changes:**
If the owner's address is static, consider using an immutable state variable to store the owner's address, reducing the need for an external call.

### Delegate Call Optimization

Since `LeverageMacroDelegateTarget` is designed for delegate calls, ensure that the functions being delegate called are optimized for gas usage.

**Instances:**
```solidity
File: LeverageMacroDelegateTarget.sol

// Functions intended for delegate call.
```

**Proposed Changes:**
Review the functions intended for delegate call to ensure they are as gas-efficient as possible. This includes minimizing state changes and optimizing logic.

### Constructor Optimization

The constructor sets up the contract but does not perform any state variable assignments. Ensure that any necessary initializations are gas-efficient.

**Instances:**
```solidity
File: LeverageMacroDelegateTarget.sol

constructor(...) {
    // Constructor logic.
}
```

**Proposed Changes:**
No specific changes needed unless the base contract's constructor requires optimization.

### Using Custom Errors Instead of Revert Strings

Custom errors are more gas-efficient than revert strings. Ensure that any revert conditions use custom errors instead of strings.

**Instances:**
```solidity
File: LeverageMacroDelegateTarget.sol
```

**Proposed Changes:**
Replace revert strings with custom errors where applicable.

### Reducing State Variable Visibility

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L29

State variables such as `borrowerOperations`, `activePool`, etc., are declared as `public`. This automatically generates getter functions, which may not be necessary if these variables are not accessed externally.

**Instances:**
```solidity
File: [Contract File]

public state variables like `borrowerOperations`, `activePool`, etc.
```

**Proposed Changes:**
```solidity
// Change visibility to internal if external access is not needed
address internal borrowerOperations;
address internal activePool;
```

### Loop Unrolling in `_doSwaps`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382

The function `_doSwaps` uses a loop to iterate over swap operations. If the number of swaps is fixed or small, unrolling the loop can save gas.

**Instances:**
```solidity
File: [Contract File]

for (uint256 i; i < swapLength; ) {
    _doSwap(swapData[i]);
    unchecked { ++i; }
}
```

**Proposed Changes:**
```solidity
// If swapLength is fixed or small, manually write out each swap operation
_doSwap(swapData[0]);
_doSwap(swapData[1]);
// Continue for known number of swaps
```

### Avoiding Redundant Checks

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249

In `_doCheckValueType`, checks are performed even if the operator is `skip`. This can be optimized by immediately returning if the operator is `skip`.

**Instances:**
```solidity
File: [Contract File]

if (check.operator == Operator.skip) {
    // Early return
    return;
} else if (check.operator == Operator.gte) {
    require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");
}
// Other checks...
```

**Proposed Changes:**
```solidity
// Immediately return if operator is skip
if (check.operator == Operator.skip) {
    return;
}
// Continue with other checks
```

### Optimizing `excessivelySafeCall`

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L508

The `excessivelySafeCall` function uses assembly for low-level call handling. While this is efficient, the setup for return data copying can be optimized by avoiding the creation of a new bytes array if the return data size is zero.

**Instances:**
```solidity
File: [Contract File]

bytes memory _returnData = new bytes(_maxCopy);
```

**Proposed Changes:**
```solidity
// Only allocate memory for return data if there is return data
if (_toCopy > 0) {
    bytes memory _returnData = new bytes(_maxCopy);
    // Copy return data
}
```