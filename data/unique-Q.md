## \[L-01\] Stop Using Solidity's transfer() Now

**Proof Of Concept**  
[https://consensys.io/diligence/blog/2019/09/stop-using-soliditys-transfer-now/\[\](https://github.com/Tapioca-DAO/tapioca-bar-audit/blob/master/contracts/markets/singularity/SGLCommon.sol#L215)](https://consensys.io/diligence/blog/2019/09/stop-using-soliditys-transfer-now/%5B%5D%28https://github.com/Tapioca-DAO/tapioca-bar-audit/blob/master/contracts/markets/singularity/SGLCommon.sol#L215%29 "https://consensys.io/diligence/blog/2019/09/stop-using-soliditys-transfer-now/%5B%5D(https://github.com/Tapioca-DAO/tapioca-bar-audit/blob/master/contracts/markets/singularity/SGLCommon.sol#L215)")

```
collateral.transfer(address(receiver), amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274

```
collateral.transfer(feeRecipientAddress, fee);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286

## \[L-02\] Function Calls in Loop Could Lead to Denial of Service

Function calls made in unbounded loop are error-prone with potential resource exhaustion as it can trap the contract due to the gas limitations or failed transactions. Here are some of the instances entailed:

```
function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {
```

&nbsp;https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73

Consider bounding the loop where possible to avoid unnecessary gas wastage and denial of service.

## \[L-03\] Insufficient coverage

Description  
The test coverage rate of the project is ~99%. Testing all functions is best practice in terms of security criteria.

Due to its capacity, test coverage is expected to be 100%.

# Non- Critical

## \[N-01\] For modern and more readable code; update import usages

Solidity code is also cleaner in another way that might not be noticeable: the struct Point. We were importing it previously with global import but not using it. The Point struct polluted the source code with an unnecessary object we were not using because we did not need it.  
This was breaking the rule of modularity and modular programming: only import what you need Specific imports with curly braces allow us to apply this rule better.  
*Recommendation*  
`import {contract1 , contract2} from "filename.sol";`

```
import "./Interfaces/IActivePool.sol";
import "./Interfaces/ICollSurplusPool.sol";
import "./Dependencies/ICollateralToken.sol";
import "./Interfaces/ICdpManagerData.sol";
import "./Dependencies/ERC3156FlashLender.sol";
import "./Dependencies/SafeERC20.sol";
import "./Dependencies/ReentrancyGuard.sol";
import "./Dependencies/AuthNoOwner.sol";
import "./Dependencies/BaseMath.sol";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L5C1-L13C38

> all contest have this issue

## \[N-2\] Showing the actual values of numbers in NatSpec comments makes checking and reading code easier

```
28:    uint256 public constant LIQUIDATOR_REWARD = 2e17; // 	200_000_000_000_000_000

    // Minimum amount of stETH collateral a CDP must have
31:    uint256 public constant MIN_NET_STETH_BALANCE = 2e18; //	2_000_000_000_000_000_000
```

```
uint256 internal constant DECIMAL_PRECISION = 1e18;  // 1_000_000_000_000_000_000
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L6

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L28C4-L31C58

## \[N-03\] Use a single file for all system-wide constants

There are many addresses and constants used in the system. It is recommended to put the most used ones in one file (for example constants.sol, use inheritance to access these values).

This will help with readability and easier maintenance for future changes. This also helps with any issues, as some of these hard-coded values are admin addresses.

constants.sol  
Use and import this file in contracts that require access to these values. This is just a suggestion, in some use cases this may result in higher gas usage in the distribution.

## \[N-04\] Use SMTChecker

The highest tier of smart contract behavior assurance is formal mathematical verification. All assertions that are made are guaranteed to be true across all inputs → The quality of your asserts is the quality of your verification.

https://twitter.com/0xOwenThurm/status/1614359896350425088?t=dbG9gHFigBX85Rv29lOjIQ&s=19

## \[N-05\] Use underscores for number literals

```
uint256 public constant LICR = 1030000000000000000; // 103%


    // Minimum collateral ratio for individual cdps
    uint256 public constant MCR = 1100000000000000000; // 110%


    // Critical system collateral ratio. If the system's total collateral ratio (TCR) falls below the CCR, Recovery Mode is triggered.
    uint256 public constant CCR = 1250000000000000000; // 125%
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19C4-L25C63

## \[N-06\] NatSpec comments should be increased in contracts

> all contest

It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI). It is clearly stated in the Solidity Official documentation

in complext project such as Defi, the interpretation of all functions and their arguments and returns is important for code readability and auditability.  
https://docs.soliditylang.org/en/v0.8.15/natspec-format.html

## \[N-07\] Use the delete keyword instead of assigning a value of 0

Using the ‘delete’ keyword instead of assigning a ‘0’ value is a detailed optimization that increases code readability and audit quality, and clearly indicates the intent.

Other hand, if use delete instead 0 value assign , it will be gas saved.

## \[N-08\] Generate perfect code headers every time

Description:  
I recommend using header for Solidity code layout and readability

```
/*//////////////////////////////////////////////////////////////
                           TESTING 123
//////////////////////////////////////////////////////////////*/
```

## \[S-01\] You can explain the operation of critical functions in NatSpec with an infographic.