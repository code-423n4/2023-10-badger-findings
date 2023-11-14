#  LOW IMPACT VULNERABILITIES

## 1: More updated version of solidity can be used

Vulnerability details

### Context:

Using the more updated version of solidity can add new features and enhance security. Version 0.8.23 is the latest version of solidity. Which includes support for Shangai. If Optimism does not support PUSH0 at this moment, Version 0.8.19, which “contains a fix for a long-standing bug that can result in code that is only used in creation code to also be included in runtime bytecode”, can also be used. 

For reference, see https://github.com/ethereum/solidity/releases

### Proof of Concept

All contracts in scope

## Tools Used

Manual Analysis

**Recommended Mitigation Steps**

To be more secured and future-proofed, please consider using the more updated version of Solidity for all contracts in scope.


## 2: receive()/payable fallback() function does not authorize requests

Vulnerability details

### Context:

Having no access control on the ```function (e.g. require(msg.sender == address(weth)))``` means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue mistakenlysent Ether. 

### Proof of Concept

> ***File: SimplifiedDiamondLike.sol***
```
160:    receive() external payable {
161:        // PHP is my favourite language
162:    }
```

### Tools Used

Manual Analysis

***Recommended Mitigation Steps***

The code should at least have a mechanism to rescue mistakenlysent Ether. 

## 3: Empty receive()/fallback() function

Vulnerability details

### Context:

If the intention is for Ether sent by a caller to be used for an actual purpose (i.e. the function is not just a WETH withdraw() handler), the function should call another function (e.g. call weth.deposit() and use the token on the caller's behalf) or at least emit an event to track that funds were sent directly to it.

### Proof of Concept

> ***File: SimplifiedDiamondLike.sol***
```
160:    receive() external payable {
161:        // PHP is my favourite language
162:    }
```

## Tools Used

Manual Analysis

***Recommended Mitigation Steps***

Function should not be empty

## 4: Missing checks for address(0x0) in the constructor/initializer

### Proof of Concept

> ***File: Sortedcdps.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L96

```
96:	borrowerOperationsAddress = _borrowerOperationsAddress;
```

> ***File: EBTCToken.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L68-L69

```
68:	cdpManagerAddress = _cdpManagerAddress;
69:	borrowerOperationsAddress = _borrowerOperationsAddress;
```

> ***File: collsurpluspool.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L48-L50

```
48:	borrowerOperationsAddress = _borrowerOperationsAddress;
49:	cdpManagerAddress = _cdpManagerAddress;
50: 	activePoolAddress = _activePoolAddress;
```

> ***File: cdpManagerStorage.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L233

```
233:	borrowerOperationsAddress = _borrowerOperationsAddress;
```

> ***File: BorrowOperations.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L121

```
121:	feeRecipientAddress = _feeRecipientAddress;
```

> ***File: ActivePool.sol***

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L53-54
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L56-57

```solidity
53:	borrowerOperationsAddress = _borrowerOperationsAddress;
54:	cdpManagerAddress = _cdpManagerAddress;

56:	collSurplusPoolAddress = _collSurplusAddress;
57:	feeRecipientAddress = _feeRecipientAddress;
```

### Tools Used

Manual Analysis


#  NON CRITICAL VULNERABILITIES

## 1: File is missing NatSpec

Vulnerability details

### Proof of Concept

**File: ISortedCdps.sol**

**File: IBorrowerOperations.sol**

**File: ICdpManager.sol**

**File: ICdpManagerData.sol**

**File: ICollSurplusPool.sol**

**File: IEbtcBase.sol**

**File: IEBTCToken.sol**

**File: IPermitNonce.sol**

**File: IPool.sol**

**File: IPositionManagers.sol**

**File: IPriceFeed.sol**

**File: IRecoveryModeGracePeriod.sol**

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Add NatSpec comments where necessary.


## 2: Misleading “events” discriptive header 

Vulnerability details

### Context:

The “events” discriptive header is misleading as it is not acctually followed by events but a struct.

### Proof of Concept

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L17

**File: HintHelpers.sol**

```
17:	    // --- Events ---
```

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Use appropriate (matching) discriptive headers to describe code

## 3: Import declarations should import specific identifiers, rather than the whole file

Vulnerability details

### Context:

Using import declarations of the form import {<identifier_name>} from "some/file.sol" avoids polluting the symbol namespace making flattened files smaller, and speeds up compilation (but does not save any gas)

### Proof of Concept

**File: IERC3156FlashLender.sol**

```
5:	 import "./IERC3156FlashBorrower.sol";
```

**File: IEBTCToken.sol**

```
5:	import "../Dependencies/IERC20.sol";
6:	import "../Dependencies/IERC2612.sol";

```

**File: IEbtcBase.sol**

```
5:	import "./IPriceFeed.sol";
```

**File: ICdpManagerData.sol**

```
5:	import "./ICollSurplusPool.sol";
6:	import "./IEBTCToken.sol";
7:	import "./ISortedCdps.sol";
8:	import "./IActivePool.sol";
9:	import "./IRecoveryModeGracePeriod.sol";
10:	import "../Dependencies/ICollateralTokenOracle.sol";
```

**File: ICdpManager.sol**

```
5:	import "./IEbtcBase.sol";
6:	import "./ICdpManagerData.sol";

```

**File: IBorrowerOperations.sol**

```
4:	import "./IPositionManagers.sol";

```

**File: IActivePool.sol**

```
5:	import "./IPool.sol";
```

**File: SortedCdps.sol**

```
5:	import "./Interfaces/ISortedCdps.sol";
6:	import "./Interfaces/ICdpManager.sol";
7:	import "./Interfaces/IBorrowerOperations.sol";
```


**File: RolesAuthority.sol**

```
4:	import {IRolesAuthority} from "./IRolesAuthority.sol";
5:	import {Auth, Authority} from "./Auth.sol";
6:	import "./EnumerableSet.sol";
```


**File: PriceFeed.sol**

```
5:	import "./Interfaces/IPriceFeed.sol";
6:	import "./Interfaces/IFallbackCaller.sol";
7:	import "./Dependencies/AggregatorV3Interface.sol";
8:	import "./Dependencies/BaseMath.sol";
9:	import "./Dependencies/EbtcMath.sol";
10:	import "./Dependencies/AuthNoOwner.sol";
```

**File: LiquidationLibrary.sol**

```
4:	import "./Interfaces/ICdpManagerData.sol";
5:	import "./Interfaces/ICollSurplusPool.sol";
6:	import "./Interfaces/IEBTCToken.sol";
7:	import "./Interfaces/ISortedCdps.sol";
8:	import "./Dependencies/ICollateralTokenOracle.sol";
9:	import "./CdpManagerStorage.sol";
```



**File: LeverageMacroFactory.sol**

```
5:	import "./Dependencies/ICollateralToken.sol";
6:	import "./Interfaces/IEBTCToken.sol";
```


**File: LeverageMacroBase.sol**

```
4:	import "./Interfaces/IBorrowerOperations.sol";
5:	import "./Interfaces/IERC3156FlashLender.sol";
6:	import "./Interfaces/IEBTCToken.sol";
7:	import "./Interfaces/ICdpManager.sol";
8:	import "./Interfaces/ISortedCdps.sol";
9:	import "./Interfaces/IPriceFeed.sol";
10:	import "./Dependencies/ICollateralToken.sol";
```

```
12:	import "./Dependencies/SafeERC20.sol";
```


**File: HintHelpers.sol**

```
5:	import "./Interfaces/ICdpManager.sol";
6:	import "./Interfaces/ISortedCdps.sol";
7:	import "./Dependencies/EbtcBase.sol";
```


**File: ERC3156FlashLender.sol**

```
5:	import "../Interfaces/IERC3156FlashLender.sol";
6:	import "../Interfaces/IWETH.sol";
```


**File: EBTCToken.sol**

```
5:	import "./Interfaces/IEBTCToken.sol";

7:	import "./Dependencies/AuthNoOwner.sol";
8:	import "./Dependencies/PermitNonce.sol";
```


**File: EbtcBase.sol**

```
5:	import "./BaseMath.sol";
6:	import "./EbtcMath.sol";
7:	import "../Interfaces/IActivePool.sol";
8:	import "../Interfaces/IPriceFeed.sol";
9:	import "../Interfaces/IEbtcBase.sol";
10:	import "../Dependencies/ICollateralToken.sol";
```

**File: CollSurplusPool.sol**

```
5:	import "./Interfaces/ICollSurplusPool.sol";
6:	import "./Dependencies/ICollateralToken.sol";
7:	import "./Dependencies/SafeERC20.sol";
8:	import "./Dependencies/ReentrancyGuard.sol";
9:	import "./Dependencies/AuthNoOwner.sol";
10:	import "./Interfaces/IActivePool.sol";
```

**File: CdpManagerStorage.sol**

```
5:	import "./Interfaces/ICdpManager.sol";
6:	import "./Interfaces/ICollSurplusPool.sol";
7:	import "./Interfaces/IEBTCToken.sol";
8:	import "./Interfaces/ISortedCdps.sol";
9:	import "./Dependencies/EbtcBase.sol";
10:	import "./Dependencies/ReentrancyGuard.sol";
11:	import "./Dependencies/ICollateralTokenOracle.sol";
12:	import "./Dependencies/AuthNoOwner.sol";
```

**File: CdpManager.sol**

```
5:	import "./Interfaces/ICdpManager.sol";
6:	import "./Interfaces/ICollSurplusPool.sol";
7:	import "./Interfaces/IEBTCToken.sol";
8:	import "./Interfaces/ISortedCdps.sol";
9:	import "./Dependencies/ICollateralTokenOracle.sol";
10:	import "./CdpManagerStorage.sol";
11:	import "./Dependencies/Proxy.sol";
```

**File: BorrowerOperations.sol**

```
5:	import "./Interfaces/IBorrowerOperations.sol";
6:	import "./Interfaces/ICdpManager.sol";
7:	import "./Interfaces/ICdpManagerData.sol";
8:	import "./Interfaces/IEBTCToken.sol";
9:	import "./Interfaces/ICollSurplusPool.sol";
10:	import "./Interfaces/ISortedCdps.sol";
11:	import "./Dependencies/EbtcBase.sol";
12:	import "./Dependencies/ReentrancyGuard.sol";
13:	import "./Dependencies/Ownable.sol";
14:	import "./Dependencies/AuthNoOwner.sol";
15:	import "./Dependencies/ERC3156FlashLender.sol";
16:	import "./Dependencies/PermitNonce.sol";
```

**File: ActivePool.sol**

```
5:	import "./Interfaces/IActivePool.sol";
6:	import "./Interfaces/ICollSurplusPool.sol";
7:	import "./Dependencies/ICollateralToken.sol";
8:	import "./Interfaces/ICdpManagerData.sol";
9:	import "./Dependencies/ERC3156FlashLender.sol";
10:	import "./Dependencies/SafeERC20.sol";
11:	import "./Dependencies/ReentrancyGuard.sol";
12:	import "./Dependencies/AuthNoOwner.sol";
13:	import "./Dependencies/BaseMath.sol";
```

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Use specific identifiers for Import declarations

## 4: Assembly blocks should have extensive comments

Vulnerability details

### Context:

Assembly blocks take a lot more time to audit than normal Solidity code, and often have gotchas
and side-effects that the Solidity versions of the same code do not. Consider adding more
comments explaining what is being done in every step of the assembly code, and describe why
assembly is being used instead of Solidity.

### Proof of Concept

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L85-L87 

https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L189-L200 

**File: SimplifiedDiamondLike.sol**

```
85:	assembly {
86:            ds.slot := position
87:        }

```

```
189:        assembly {
190:            calldatacopy(0, 0, calldatasize())
191:            let result := delegatecall(gas(), facet, 0, calldatasize(), 0, 0)
192:            returndatacopy(0, 0, returndatasize())
193:            switch result
194:            case 0 {
195:                revert(0, returndatasize())
196:            }
197:            default {
198:                return(0, returndatasize())
199:            }
200:        }
```

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Add extensive comments to assembly blocks

## 5: Contracts should have full test coverage

Vulnerability details

### Context:

While 100% code coverage does not guarantee that there are no bugs, it often will catch easyto-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. Furthermore, in order to get full coverage, code authors will often have to re-organize their code so that it is more modular, so that each component can be tested separately, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.


### Proof of Concept

**File: Various Files**

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Make sure project contracts have full test coverage.

## 6: Large or complicated code bases should implement invariant tests

Vulnerability details

### Context:

Large code bases, or code with lots of inline-assembly, complicated math, or complicated
interactions between multiple contracts, should implement invariant fuzzing tests. Invariant
fuzzers such as Echidna require the test writer to come up with invariants which should not be
violated under any circumstances, and the fuzzer tests various inputs and function calls to
ensure that the invariants always hold. Even code with 100% code coverage can still have bugs
due to the order of the operations a user performs, and invariant fuzzers, with properly and
extensively-written invariants, can close this testing gap significantly.

For reference, see https://medium.com/coinmonks/smart-contract-fuzzing-d9b88e0b0a05

### Proof of Concept

**File: Various Files**

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Implement apropriate invarient tests

## 7: Consider adding formal verification proofs

Vulnerability details

### Context:

Consider using formal verification to mathematically prove that your code does what is intended, and does not have any edge cases with unexpected behavior. The solidity compiler itself has this functionality built in.

For reference, see https://docs.soliditylang.org/en/latest/smtchecker.html#smtchecker-and-formal-verification

### Proof of Concept

**File: Various Files**

### Tools Used

Manual Analysis

**Recommended Mitigation Steps**

Add apropriate formal verification proofs 

## 8: Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, for readability

Vulnerability details

### Context:

Well-organized data structures make code reviews easier, which may lead to fewer bugs. Consider combining related mappings into mappings to structs, so it's clear what data is related.

### Proof of Concept

**File: CdpManagerStorage.sol**

```
168:	mapping(bytes32 => Cdp) public Cdps;
```
```
190:	mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;
```
```
202:	mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;
```

**File: EBTCToken.sol**

```
51:	mapping(address => uint256) private _balances;
52:	mapping(address => mapping(address => uint256)) private _allowances;
```


**File: RolesAuthority.sol**

```
28:	mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;
```
```
32:	mapping(address => bytes32) public getUserRoles;
33:
34:	mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;
35:
36:	mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;
```

### Tools Used

Manual Analysis
