
### Low Issues
|Title|Issue|Instances|
|-|:-|:-:|
|[L-1] Require Should Used Instead of Assert | [Require Should Used Instead of Assert](#require-should-used-instead-of-assert) | 1 |
|[L-2] Burn functions must be protected with a modifier | [Burn functions must be protected with a modifier](#burn-functions-must-be-protected-with-a-modifier) | 2 |
|[L-3] Casting block.timestamp can reduce the lifespan of a contract | [Casting block.timestamp can reduce the lifespan of a contract](#casting-blocktimestamp-can-reduce-the-lifespan-of-a-contract) | 1 |
|[L-4] Code does not follow the best practice of check-effects-interaction | [Code does not follow the best practice of check-effects-interaction](#code-does-not-follow-the-best-practice-of-check-effects-interaction) | 11 |
|[L-5] Divide before multiply | [Divide before multiply](#divide-before-multiply) | 4 |
|[L-6] Some tokens may not consider type(uint256).max as an infinite approval | [Some tokens may not consider type(uint256).max as an infinite approval](#some-tokens-may-not-consider-typeuint256max-as-an-infinite-approval) | 6 |
|[L-7] ERC20 Approve Call is Not Safe | [ERC20 Approve Call is Not Safe](#erc20-approve-call-is-not-safe) | 6 |
|[L-8] Empty Uncontrolled Ether Flow in receive()/payable fallback() | [Empty Uncontrolled Ether Flow in receive()/payable fallback()](#empty-uncontrolled-ether-flow-in-receivepayable-fallback) | 1 |
|[L-9] Local variable shadowing | [Local variable shadowing](#local-variable-shadowing) | 1 |
|[L-10] Loss of Precision in Division by Large Numbers | [Loss of Precision in Division by Large Numbers](#loss-of-precision-in-division-by-large-numbers) | 9 |
|[L-11] Missing zero address validation in constructor | [Missing zero address validation in constructor](#missing-zero-address-validation-in-constructor) | 42 |
|[L-12] External calls in an un-bounded for-loop may result in a DOS | [External calls in an un-bounded for-loop may result in a DOS](#external-calls-in-an-un-bounded-for-loop-may-result-in-a-dos) | 31 |
|[L-13] Payable Function Without Ether Transfer | [Payable Function Without Ether Transfer](#payable-function-without-ether-transfer) | 3 |
|[L-14] Potential Division by Zero | [Potential Division by Zero](#potential-division-by-zero) | 3 |
|[L-15] Reentrancy vulnerabilities | [Reentrancy vulnerabilities](#reentrancy-vulnerabilities-2) | 22 |
|[L-16] SafeApprove Deprecated | [SafeApprove Deprecated](#safeapprove-deprecated) | 2 |
|[L-17] Setter No Initial Value Check Detection | [Setter No Initial Value Check Detection](#setter-no-initial-value-check-detection) | 1 |
|[L-18] receive()/payable fallback() function does not authorize requests | [receive()/payable fallback() function does not authorize requests](#receivepayable-fallback-function-does-not-authorize-requests) | 1 |
|[L-19] Unsafe Cast Unsigned to Signed | [Unsafe Cast Unsigned to Signed](#unsafe-cast-unsigned-to-signed) | 2 |
|[L-20] Unsafe Downcast  | [Unsafe Downcast ](#unsafe-downcast) | 2 |
|[L-21] Approve/SafeApprove Without Zero Check | [Approve/SafeApprove Without Zero Check](#approvesafeapprove-without-zero-check) | 1 |
|[L-22] Check Oracle Data Freshness | [Check Oracle Data Freshness](#check-oracle-data-freshness) | 2 |
|[M-23] Missing Sequencer Check | [Missing Sequencer Check](#missing-sequencer-check) | 2 |
|[M-24] Unchecked transfer | [Unchecked transfer](#unchecked-transfer) | 6 |
|[M-25] Calls transfer()/transferFrom() With IERC20 | [Calls transfer()/transferFrom() With IERC20](#calls-transfertransferfrom-with-ierc20) | 6 |
|[M-26] Zero-value transfers may revert | [Zero-value transfers may revert](#zero-value-transfers-may-revert) | 7 |

Total: 175 instances over 26 issues

### Non-Critical Issues
|Title|Issue|Instances|
|-|:-|:-:|
|[N-1] Variables with all caps names that are not constants or immutables | [Variables with all caps names that are not constants or immutables](#variables-with-all-caps-names-that-are-not-constants-or-immutables) | 16 |
|[N-2] Avoid Magic Numbers | [Avoid Magic Numbers](#avoid-magic-numbers) | 8 |
|[N-3] Cast to bytes or bytes32 for clearer semantic meaning | [Cast to bytes or bytes32 for clearer semantic meaning](#cast-to-bytes-or-bytes32-for-clearer-semantic-meaning) | 1 |
|[N-4] Complex math in a single line | [Complex math in a single line](#complex-math-in-a-single-line) | 9 |
|[N-5] Improving Code Readability with Named Mappings  | [Improving Code Readability with Named Mappings ](#improving-code-readability-with-named-mappings ) | 8 |
|[N-6] Consider Using 'delete' Rather than Assigning Zero/False to Clear Values | [Consider Using 'delete' Rather than Assigning Zero/False to Clear Values](#consider-using-delete-rather-than-assigning-zerofalse-to-clear-values) | 21 |
|[N-7] Do not calculate constants | [Do not calculate constants](#do-not-calculate-constants) | 1 |
|[N-8] Constants in Comparisons on Left Side | [Constants in Comparisons on Left Side](#constants-in-comparisons-on-left-side) | 72 |
|[N-9] constant/immutable variable names should use capital letters and underscore | [constant/immutable variable names should use capital letters and underscore](#constantimmutable-variable-names-should-use-capital-letters-and-underscore) | 62 |
|[N-10] Contract Ordering Violation Style Guide | [Contract Ordering Violation Style Guide](#contract-ordering-violation-style-guide) | 1 |
|[N-11] Control structures do not follow the Solidity Style Guide | [Control structures do not follow the Solidity Style Guide](#control-structures-do-not-follow-the-solidity-style-guide) | 22 |
|[N-12] Costly operations inside a loop | [Costly operations inside a loop](#costly-operations-inside-a-loop) | 8 |
|[N-13] Dead-code | [Dead-code](#dead-code) | 2 |
|[N-14] Avoid double casting | [Avoid double casting](#avoid-double-casting) | 5 |
|[N-15] Duplicated require()/revert() checks should be refactored to a modifier or function | [Duplicated require()/revert() checks should be refactored to a modifier or function](#duplicated-requirerevert-checks-should-be-refactored-to-a-modifier-or-function) | 4 |
|[N-16] Else block not required | [Else block not required](#else-block-not-required) | 6 |
|[N-17] Events should use parameters to convey information | [Events should use parameters to convey information](#events-should-use-parameters-to-convey-information) | 2 |
|[N-18] Function Length Too Long | [Function Length Too Long](#function-length-too-long) | 16 |
|[N-19] Lack of Explicit Visibility Declaration in State Variables | [Lack of Explicit Visibility Declaration in State Variables](#lack-of-explicit-visibility-declaration-in-state-variables) | 6 |
|[N-20] Functions not called by the contract should be declared as external instead of public | [Functions not called by the contract should be declared as external instead of public](#functions-not-called-by-the-contract-should-be-declared-as-external-instead-of-public) | 3 |
|[N-21] Codebase should implement formal verification testing | [Codebase should implement formal verification testing](#codebase-should-implement-formal-verification-testing) | 1 |
|[N-22] Contracts should have full test coverage | [Contracts should have full test coverage](#contracts-should-have-full-test-coverage) | 1 |
|[N-23] Function names should differ | [Function names should differ](#function-names-should-differ) | 2 |
|[N-24] Conformance to Solidity function naming conventions | [Conformance to Solidity function naming conventions](#conformance-to-solidity-function-naming-conventions) | 5 |
|[N-25] Enum values should be used in place of constant array indexes | [Enum values should be used in place of constant array indexes](#enum-values-should-be-used-in-place-of-constant-array-indexes) | 2 |
|[N-26] If-statement can be converted to a ternary | [If-statement can be converted to a ternary](#if-statement-can-be-converted-to-a-ternary) | 3 |
|[N-27] Avoid the use of sensitive terms | [Avoid the use of sensitive terms](#avoid-the-use-of-sensitive-terms) | 3 |
|[N-28] Inconsistency Spacing in Comments | [Inconsistency Spacing in Comments](#inconsistency-spacing-in-comments) | 1 |
|[N-29] Inconsistent Usage of Integer Types | [Inconsistent Usage of Integer Types](#inconsistent-usage-of-integer-types) | 37 |
|[N-30] Inconsistent usage of require/error | [Inconsistent usage of require/error](#inconsistent-usage-of-requireerror) | 1 |
|[N-31] Interfaces Should Be Defined in Separate Files From Their Usage | [Interfaces Should Be Defined in Separate Files From Their Usage](#interfaces-should-be-defined-in-separate-files-from-their-usage) | 2 |
|[N-32] Invariant Tests | [Invariant Tests](#invariant-tests) | 1 |
|[N-33] Lack of Descriptive Reason Strings in require/revert Statements | [Lack of Descriptive Reason Strings in require/revert Statements](#lack-of-descriptive-reason-strings-in-requirerevert-statements) | 10 |
|[N-34] Excessive Line Length in Code | [Excessive Line Length in Code](#excessive-line-length-in-code) | 10 |
|[N-35] Token contract should have a blacklist function or modifier | [Token contract should have a blacklist function or modifier](#token-contract-should-have-a-blacklist-function-or-modifier) | 1 |
|[N-36] Contracts missing NatSpec comments | [Contracts missing NatSpec comments](#contracts-missing-natspec-comments) | 22 |
|[N-37] Missing events in sensitive functions | [Missing events in sensitive functions](#missing-events-in-sensitive-functions) | 4 |
|[N-38] Missing events arithmetic | [Missing events arithmetic](#missing-events-arithmetic) | 1 |
|[N-39] Contract Missing NatSpec @author | [Contract Missing NatSpec @author](#contract-missing-natspec-author) | 24 |
|[N-40] Functions missing NatSpec comments | [Functions missing NatSpec comments](#functions-missing-natspec-comments) | 308 |
|[N-41] Missing function parameter in NatSpec comments | [Missing function parameter in NatSpec comments](#missing-function-parameter-in-natspec-comments) | 22 |
|[N-42] Missing function return values in NatSpec comments | [Missing function return values in NatSpec comments](#missing-function-return-values-in-natspec-comments) | 7 |
|[N-43] Contract Missing NatSpec @title | [Contract Missing NatSpec @title](#contract-missing-natspec-title) | 15 |
|[N-44] Public variable declarations should have NatSpec descriptions | [Public variable declarations should have NatSpec descriptions](#public-variable-declarations-should-have-natspec-descriptions) | 57 |
|[N-45] Events are missing sender information | [Events are missing sender information](#events-are-missing-sender-information) | 37 |
|[N-46] Large numeric literals should use underscores for readability | [Large numeric literals should use underscores for readability](#large-numeric-literals-should-use-underscores-for-readability) | 5 |
|[N-47] Consider move Msg.sender checks to modifier | [Consider move Msg.sender checks to modifier](#consider-move-msgsender-checks-to-modifier) | 21 |
|[N-48] Functions Not Implementing an Interface | [Functions Not Implementing an Interface](#functions-not-implementing-an-interface) | 51 |
|[N-49] Use of old Solidity version | [Use of old Solidity version](#use-of-old-solidity-version) | 34 |
|[N-50] Override function arguments that are unused should have the variable name removed or commented out | [Override function arguments that are unused should have the variable name removed or commented out](#override-function-arguments-that-are-unused-should-have-the-variable-name-removed-or-commented-out) | 6 |
|[N-51] Use return statement when there is a named return variable is redundant | [Use return statement when there is a named return variable is redundant](#use-return-statement-when-there-is-a-name-return-variable-is-redundant) | 3 |
|[N-52] Event Emission Preceding External Calls: A Best Practice | [Event Emission Preceding External Calls: A Best Practice](#event-emission-preceding-external-calls-a-best-practice) | 38 |
|[N-53] Variable names too similar | [Variable names too similar](#variable-names-too-similar) | 90 |
|[N-54] Constant redefined elsewhere | [Constant redefined elsewhere](#constant-redefined-elsewhere) | 2 |
|[N-55] Typo and Spelling Error | [Typo and Spelling Error](#typo-and-spelling-error) | 14 |
|[N-56] Functions that alter state should emit events | [Functions that alter state should emit events](#functions-that-alter-state-should-emit-events) | 5 |
|[N-57] Conformance to Solidity struct naming conventions | [Conformance to Solidity struct naming conventions](#conformance-to-solidity-struct-naming-conventions) | 3 |
|[N-58] TODO comments | [TODO comments](#todo-comments) | 1 |
|[N-59] Too many digits | [Too many digits](#too-many-digits) | 1 |
|[N-60] Top level declarations should be separated by two blank lines | [Top level declarations should be separated by two blank lines](#top-level-declarations-should-be-separated-by-two-blank-lines) | 14 |
|[N-61] Enforce Underscore Prefix for Non-External Variable and Function Names | [Enforce Underscore Prefix for Non-External Variable and Function Names](#enforce-underscore-prefix-for-non-external-variable-and-function-names) | 16 |
|[N-62] Unnecessary Casting of Variables | [Unnecessary Casting of Variables](#unnecessary-casting-of-variables) | 2 |
|[N-63] Import declarations should import specific identifiers, rather than the whole file | [Import declarations should import specific identifiers, rather than the whole file](#import-declarations-should-import-specific-identifiers-rather-than-the-whole-file) | 87 |
|[N-64] Unused function arguments | [Unused function arguments](#unused-function-arguments) | 3 |
|[N-65] Unused event definition | [Unused event definition](#unused-event-definition) | 4 |
|[N-66] Event is missing indexed fields | [Event is missing indexed fields](#event-is-missing-indexed-fields) | 42 |
|[N-67] Unused imports | [Unused imports](#unused-imports) | 11 |
|[N-68] Unused modifier definition | [Unused modifier definition](#unused-modifier-definition) | 1 |
|[N-69] Unused return | [Unused return](#unused-return) | 16 |
|[N-70] Unused struct definition | [Unused struct definition](#unused-struct-definition) | 2 |
|[N-71] Use bytes.concat() over abi.encodePacked() for clearer semantic meaning | [Use bytes.concat() over abi.encodePacked() for clearer semantic meaning](#use-bytesconcat-over-abiencodepacked-for-clearer-semantic-meaning) | 2 |
|[N-72] Use Immutable for Constant Expressions | [Use Immutable for Constant Expressions](#use-immutable-for-constant-expressions) | 3 |
|[N-73] Conformance to Solidity local and state variable naming conventions | [Conformance to Solidity local and state variable naming conventions](#conformance-to-solidity-local-and-state-variable-naming-conventions) | 365 |
|[N-74] Whitespace in Expressions | [Whitespace in Expressions](#whitespace-in-expressions) | 5 |
|[N-75] Use of 0 as a function argument | [Use of 0 as a function argument](#use-of-0-as-a-function-argument) | 14 |

Total: 1711 instances over 75 issues

#


<br><br>
# Low Issues



## Require Should Used Instead of Assert
- Severity: Low
- Confidence: High

### Description
Solidity has two error handling functions: require() and assert(). require() is used for validating user input and other conditions that must be met for the code to execute successfully. When a require() statement fails, the transaction is reverted and gas is consumed. assert() is used for checking internal errors in the code, and when it fails, all gas is consumed and the transaction is reverted. However, assert() is discouraged as it can cause serious problems, such as wasted gas and denial of service attacks. Therefore, it's recommended to use require() instead of assert() in most cases.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/LiquidationLibrary.sol

564    assert(toLiquidator < _totalColToSend)
```
 use require instead

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L564)


</details>

# 


## Burn functions must be protected with a modifier
- Severity: Low
- Confidence: High

### Description
If burn functions are not protected by a modifier, any address may be able to burn tokens, potentially leading to financial loss. A common modifier to use is `onlyOwner`.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/EBTCToken.sol

95    function burn(address _account, uint256 _amount) external override 
```
Burn function without a protective modifier.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L95-L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L95-L98)


#

```
File: contracts/EBTCToken.sol

104    function burn(uint256 _amount) external 
```
Burn function without a protective modifier.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104-L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104-L107)


</details>

# 


## Casting block.timestamp can reduce the lifespan of a contract
- Severity: Low
- Confidence: High

### Description
Casting `block.timestamp` to smaller integer types can reduce the effective lifespan of a contract. `block.timestamp` returns the current block timestamp as seconds since the unix epoch as `uint`. When it's cast to a smaller integer type, this effectively reduces the maximum timestamp value the contract can handle. As a result, the contract might stop functioning correctly after a certain point in time, even though `block.timestamp` itself will continue to increase with each block.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

53    lastGracePeriodStartTimestamp = uint128(block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L53)


</details>

# 


## Code does not follow the best practice of check-effects-interaction
- Severity: Low
- Confidence: Medium

### Description

Code should follow the best-practice of 
[check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), 
where state variables are updated before any external calls are made. 
Doing so prevents a large class of reentrancy bugs.


<details>

<summary>
There are 11 instances of this issue:

</summary>

###
#

```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```


```
File: contracts/CdpManagerStorage.sol

479    CdpIds[index] = idToMove
```


```
File: contracts/CdpManagerStorage.sol

483    CdpIds.pop()
```


```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

479    CdpIds[index] = idToMove
```


```
File: contracts/CdpManagerStorage.sol

483    CdpIds.pop()
```


```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

600    Cdps[_cdpId].coll = _newColl
```


```
File: contracts/CdpManagerStorage.sol

386    _cdp.debt = _newDebt
```


```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```


```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```


```
File: contracts/CdpManagerStorage.sol

271    Cdps[_cdpId].status = closedStatus
```


```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```


```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```


```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```


```
File: contracts/CdpManagerStorage.sol

480    Cdps[idToMove].arrayIndex = index
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

600    Cdps[_cdpId].coll = _newColl
```


```
File: contracts/CdpManagerStorage.sol

386    _cdp.debt = _newDebt
```


```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```


```
File: contracts/CdpManagerStorage.sol

271    Cdps[_cdpId].status = closedStatus
```


```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```


```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```


```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```


```
File: contracts/CdpManagerStorage.sol

480    Cdps[idToMove].arrayIndex = index
```


```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

339    cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex
```


```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```


```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

339    cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex
```


```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

405    cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex
```


```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```


```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

405    cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex
```


```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#

```
File: contracts/LiquidationLibrary.sol

807    function _getTotalsFromBatchLiquidate_NormalMode(
808            uint256 _price,
809            uint256 _TCR,
810            bytes32[] memory _cdpArray
811        ) internal returns (LiquidationTotals memory totals) 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

479    CdpIds[index] = idToMove
```


```
File: contracts/CdpManagerStorage.sol

483    CdpIds.pop()
```


```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

600    Cdps[_cdpId].coll = _newColl
```


```
File: contracts/CdpManagerStorage.sol

386    _cdp.debt = _newDebt
```


```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```


```
File: contracts/CdpManagerStorage.sol

271    Cdps[_cdpId].status = closedStatus
```


```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```


```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```


```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```


```
File: contracts/CdpManagerStorage.sol

480    Cdps[idToMove].arrayIndex = index
```


```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

339    cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex
```


```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

405    cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex
```


```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


#

```
File: contracts/LiquidationLibrary.sol

61    function _liquidateIndividualCdpSetup(
62            bytes32 _cdpId,
63            uint256 _partialAmount,
64            bytes32 _upperPartialHint,
65            bytes32 _lowerPartialHint
66        ) internal 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

69    _syncAccounting(_cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

71    uint256 _price = priceFeed.fetchPrice()
```


```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```


```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```


```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```


```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```


```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```


```
File: contracts/LiquidationLibrary.sol

460    _cdp.coll = _coll - _partialColl
```


```
File: contracts/CdpManagerStorage.sol

435    _cdp.stake = newStake
```


```
File: contracts/LiquidationLibrary.sol

461    _cdp.debt = _debt - _partialDebt
```


```
File: contracts/CdpManagerStorage.sol

271    Cdps[_cdpId].status = closedStatus
```


```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```


```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```


```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```


```
File: contracts/CdpManagerStorage.sol

480    Cdps[idToMove].arrayIndex = index
```


```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


```
File: contracts/LiquidationLibrary.sol

889    systemDebtRedistributionIndex = systemDebtRedistributionIndex + EBTCDebtRewardPerUnitStaked
```


```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


```
File: contracts/CdpManagerStorage.sol

423    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131)


#

```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

153    (
154                    liquidationValues.debtToBurn,
155                    liquidationValues.totalCollToSendToLiquidator
156                ) = _liquidateCDPPartially(_liqState)
```


```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```


```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```


```
File: contracts/CdpManagerStorage.sol

271    Cdps[_cdpId].status = closedStatus
```


```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```


```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```


```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```


```
File: contracts/CdpManagerStorage.sol

480    Cdps[idToMove].arrayIndex = index
```


```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```


```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#

```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

145    (
146                    liquidationValues.debtToBurn,
147                    liquidationValues.totalCollToSendToLiquidator,
148                    liquidationValues.debtToRedistribute,
149                    liquidationValues.liquidatorCollSharesReward,
150                    liquidationValues.collSurplus
151                ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```


```
File: contracts/LiquidationLibrary.sol

153    (
154                    liquidationValues.debtToBurn,
155                    liquidationValues.totalCollToSendToLiquidator
156                ) = _liquidateCDPPartially(_liqState)
```


```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```


```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```


```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```


```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```


```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```


```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```


```
File: contracts/LiquidationLibrary.sol

889    systemDebtRedistributionIndex = systemDebtRedistributionIndex + EBTCDebtRewardPerUnitStaked
```


```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```


```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```


```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```


```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
External calls:

```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

State variables written after the call(s):

```
File: contracts/CdpManager.sol

216    Cdps[_redeemColFromCdp.cdpId].debt = newDebt
```


```
File: contracts/CdpManager.sol

217    Cdps[_redeemColFromCdp.cdpId].coll = newColl
```


```
File: contracts/CdpManager.sol

218    _updateStakeAndTotalStakes(_redeemColFromCdp.cdpId)
```


```
File: contracts/CdpManagerStorage.sol

435    _cdp.stake = newStake
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```


```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#

```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```


```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#

```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
External calls:

```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```


```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```


```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/LiquidationLibrary.sol

714    activePool.transferSystemCollShares(address(collSurplusPool), totals.totalCollSurplus)
```


```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```


```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```


```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```


```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```

State variables written after the call(s):

```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```


```
File: contracts/CdpManagerStorage.sol

53    lastGracePeriodStartTimestamp = uint128(block.timestamp)
```


```
File: contracts/CdpManagerStorage.sol

67    lastGracePeriodStartTimestamp = UNSET_TIMESTAMP
```


```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```


```
File: contracts/LiquidationLibrary.sol

889    systemDebtRedistributionIndex = systemDebtRedistributionIndex + EBTCDebtRewardPerUnitStaked
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
External calls:

```
File: contracts/CdpManager.sol

336    _syncGlobalAccounting()
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/CdpManager.sol

338    totals.price = priceFeed.fetchPrice()
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


```
File: contracts/CdpManager.sol

254    activePool.decreaseSystemDebt(_EBTC)
```


```
File: contracts/CdpManager.sol

257    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares)
```


```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```


```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

State variables written after the call(s):

```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


```
File: contracts/CdpManagerStorage.sol

479    CdpIds[index] = idToMove
```


```
File: contracts/CdpManagerStorage.sol

483    CdpIds.pop()
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

600    Cdps[_cdpId].coll = _newColl
```


```
File: contracts/CdpManagerStorage.sol

386    _cdp.debt = _newDebt
```


```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```


```
File: contracts/CdpManagerStorage.sol

435    _cdp.stake = newStake
```


```
File: contracts/CdpManagerStorage.sol

271    Cdps[_cdpId].status = closedStatus
```


```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```


```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```


```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```


```
File: contracts/CdpManagerStorage.sol

480    Cdps[idToMove].arrayIndex = index
```


```
File: contracts/CdpManager.sol

216    Cdps[_redeemColFromCdp.cdpId].debt = newDebt
```


```
File: contracts/CdpManager.sol

217    Cdps[_redeemColFromCdp.cdpId].coll = newColl
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

339    cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex
```


```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

405    cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex
```


```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```


```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


```
File: contracts/CdpManagerStorage.sol

423    totalStakes = _newTotalStakes
```


```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```


```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManager.sol

773    function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth 
```
External calls:

```
File: contracts/CdpManager.sol

779    syncGlobalAccountingAndGracePeriod()
```


```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```


```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

State variables written after the call(s):

```
File: contracts/CdpManager.sol

781    stakingRewardSplit = _stakingRewardSplit
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773-L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773-L783)


</details>

# 


## Divide before multiply
- Severity: Low
- Confidence: Medium

### Description
Solidity's integer division truncates. Thus, performing division before multiplication can lead to precision loss.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

552    function calcFeeUponStakingReward(
553            uint256 _newIndex,
554            uint256 _prevIndex
555        ) public view returns (uint256, uint256, uint256) 
```
 performs a multiplication on the result of a division:
	- 
```
File: contracts/CdpManagerStorage.sol

558    uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT
```

	- 
```
File: contracts/CdpManagerStorage.sol

561    uint256 _deltaFeeSplit = deltaIndexFees * getSystemCollShares()
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570)


#

```
File: contracts/CdpManagerStorage.sol

552    function calcFeeUponStakingReward(
553            uint256 _newIndex,
554            uint256 _prevIndex
555        ) public view returns (uint256, uint256, uint256) 
```
 performs a multiplication on the result of a division:
	- 
```
File: contracts/CdpManagerStorage.sol

564    uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION
```

	- 
```
File: contracts/CdpManagerStorage.sol

565    uint256 _deltaFeeSplitShare = (_feeTaken * DECIMAL_PRECISION) +
566                systemStEthFeePerUnitIndexError
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570)


#

```
File: contracts/CdpManagerStorage.sol

552    function calcFeeUponStakingReward(
553            uint256 _newIndex,
554            uint256 _prevIndex
555        ) public view returns (uint256, uint256, uint256) 
```
 performs a multiplication on the result of a division:
	- 
```
File: contracts/CdpManagerStorage.sol

567    uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes
```

	- 
```
File: contracts/CdpManagerStorage.sol

568    uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570)


#

```
File: contracts/LiquidationLibrary.sol

862    function _redistributeDebt(uint256 _debt) internal 
```
 performs a multiplication on the result of a division:
	- 
```
File: contracts/LiquidationLibrary.sol

882    uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes
```

	- 
```
File: contracts/LiquidationLibrary.sol

884    lastEBTCDebtErrorRedistribution =
885                EBTCDebtNumerator -
886                (EBTCDebtRewardPerUnitStaked * _totalStakes)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892)


</details>

# 


## Some tokens may not consider type(uint256).max as an infinite approval
- Severity: Low
- Confidence: High

### Description
Some tokens such as [COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L89-L91) downcast such approvals to `uint96` and use that as a raw value rather than interpreting it as an infinite approval. Eventually these approvals will reach zero, at which point the calling contract will no longer function properly.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroReference.sol

39    ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max)
```
This variable might be zero: `type()(uint256).max` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39)


#

```
File: contracts/LeverageMacroReference.sol

40    stETH.approve(_borrowerOperationsAddress, type(uint256).max)
```
This variable might be zero: `type()(uint256).max` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40)


#

```
File: contracts/LeverageMacroReference.sol

41    stETH.approve(_activePool, type(uint256).max)
```
This variable might be zero: `type()(uint256).max` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L41)


#

```
File: contracts/LeverageMacroReference.sol

53    ebtcToken.approve(address(borrowerOperations), type(uint256).max)
```
This variable might be zero: `type()(uint256).max` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)


#

```
File: contracts/LeverageMacroReference.sol

54    stETH.approve(address(borrowerOperations), type(uint256).max)
```
This variable might be zero: `type()(uint256).max` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L54)


#

```
File: contracts/LeverageMacroReference.sol

55    stETH.approve(address(activePool), type(uint256).max)
```
This variable might be zero: `type()(uint256).max` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L55)


</details>

# 


## ERC20 Approve Call is Not Safe
- Severity: Low
- Confidence: High

### Description
This detector identifies instances where the approve() method is used on ERC20 tokens. The approve() function can be vulnerable to a specific attack, where a malicious actor can double spend tokens. This scenario occurs when the owner changes the approved allowance from N to M (N>0, M>0). The malicious spender can observe this change and quickly transfer the original N tokens before the change is mined, and then spend the additional M tokens afterwards. This could result in a total transfer of N+M tokens, which is not what the owner intended. More info you can see in this [link](https://docs.google.com/document/d/1YLPtQxZu1UAvO9cZ1O2RPXBbT0mooh4DYKjA_jp-RLM/edit).

For this reason, it's recommended to use `safeIncreaseAllowance()` or `safeDecreaseAllowance()` for better control. If these methods are not available, using `safeApprove()` is also an option as it reverts if the current approval is not zero, providing an additional layer of security.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroReference.sol

39    ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39)


#

```
File: contracts/LeverageMacroReference.sol

40    stETH.approve(_borrowerOperationsAddress, type(uint256).max)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40)


#

```
File: contracts/LeverageMacroReference.sol

41    stETH.approve(_activePool, type(uint256).max)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L41)


#

```
File: contracts/LeverageMacroReference.sol

53    ebtcToken.approve(address(borrowerOperations), type(uint256).max)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)


#

```
File: contracts/LeverageMacroReference.sol

54    stETH.approve(address(borrowerOperations), type(uint256).max)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L54)


#

```
File: contracts/LeverageMacroReference.sol

55    stETH.approve(address(activePool), type(uint256).max)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L55)


</details>

# 


## Empty Uncontrolled Ether Flow in receive()/payable fallback()
- Severity: Low
- Confidence: Medium

### Description
This detector flags contracts with empty receive()/payable fallback() functions that do not contain an authorization check. This can potentially lead to loss of funds, as anyone can send Ether to the contract without a way of getting it back out.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/SimplifiedDiamondLike.sol

160    receive() external payable 
```
 don't keep `receive` empty.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162)


</details>

# 


## Local variable shadowing
- Severity: Low
- Confidence: High

### Description
Detection of shadowing using local variables.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

680    bytes32 version
```
 shadows:
	- 
```
File: contracts/BorrowerOperations.sol

687    function version() external pure override returns (string memory) 
```
 (function)
	- 
```
File: contracts/Interfaces/IPositionManagers.sol

42    function version() external view returns (string memory);
```
 (function)

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L680](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L680)


</details>

# 


## Loss of Precision in Division by Large Numbers
- Severity: Low
- Confidence: High

### Description
When dividing by large numbers in Solidity. Due to Solidity not supporting fractions, division by large numbers may result in the quotient being zero. To mitigate this risk and ensure accurate results, consider requiring a minimum amount for the numerator, ensuring it is always larger than the denominator. By enforcing a minimum numerator, you can prevent unintended zero quotients and maintain precision in your division operations.

<details>

<summary>
There are 9 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

321    (amount * feeBps) / MAX_BPS
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L321](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L321)


#

```
File: contracts/BorrowerOperations.sol

1118    (amount * feeBps) / MAX_BPS
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1118)


#

```
File: contracts/CdpManagerStorage.sol

558    (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L558)


#

```
File: contracts/CdpManager.sol

621    (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622                _totalEBTCSupply
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621-L622](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621-L622)


#

```
File: contracts/HintHelpers.sol

145    (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L145)


#

```
File: contracts/LiquidationLibrary.sol

592    (_incentiveColl * _price) / LICR
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L592](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L592)


#

```
File: contracts/LiquidationLibrary.sol

558    (_totalDebtToBurn * LICR) / _price
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558)


#

```
File: contracts/LiquidationLibrary.sol

555    (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555)


#

```
File: contracts/LiquidationLibrary.sol

579    (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price
```
 should be checked first

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L579](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L579)


</details>

# 


## Missing zero address validation in constructor
- Severity: Low
- Confidence: Medium

### Description
Detect missing zero address validation in the constructor.

<details>

<summary>
There are 42 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

53    borrowerOperationsAddress = _borrowerOperationsAddress
```
 state variable `borrowerOperationsAddress` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53)


#

```
File: contracts/ActivePool.sol

54    cdpManagerAddress = _cdpManagerAddress
```
 state variable `cdpManagerAddress` assign with `_cdpManagerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54)


#

```
File: contracts/ActivePool.sol

55    collateral = ICollateralToken(_collTokenAddress)
```
 state variable `collateral` assign with `_collTokenAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L55)


#

```
File: contracts/ActivePool.sol

56    collSurplusPoolAddress = _collSurplusAddress
```
 state variable `collSurplusPoolAddress` assign with `_collSurplusAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L56)


#

```
File: contracts/ActivePool.sol

57    feeRecipientAddress = _feeRecipientAddress
```
 state variable `feeRecipientAddress` assign with `_feeRecipientAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57)


#

```
File: contracts/BorrowerOperations.sol

117    cdpManager = ICdpManager(_cdpManagerAddress)
```
 state variable `cdpManager` assign with `_cdpManagerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L117)


#

```
File: contracts/BorrowerOperations.sol

118    collSurplusPool = ICollSurplusPool(_collSurplusPoolAddress)
```
 state variable `collSurplusPool` assign with `_collSurplusPoolAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L118)


#

```
File: contracts/BorrowerOperations.sol

119    sortedCdps = ISortedCdps(_sortedCdpsAddress)
```
 state variable `sortedCdps` assign with `_sortedCdpsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L119)


#

```
File: contracts/BorrowerOperations.sol

120    ebtcToken = IEBTCToken(_ebtcTokenAddress)
```
 state variable `ebtcToken` assign with `_ebtcTokenAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L120)


#

```
File: contracts/BorrowerOperations.sol

121    feeRecipientAddress = _feeRecipientAddress
```
 state variable `feeRecipientAddress` assign with `_feeRecipientAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121)


#

```
File: contracts/CdpManagerStorage.sol

229    liquidationLibrary = _liquidationLibraryAddress
```
 state variable `liquidationLibrary` assign with `_liquidationLibraryAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229)


#

```
File: contracts/CdpManagerStorage.sol

233    borrowerOperationsAddress = _borrowerOperationsAddress
```
 state variable `borrowerOperationsAddress` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233)


#

```
File: contracts/CdpManagerStorage.sol

234    collSurplusPool = ICollSurplusPool(_collSurplusPool)
```
 state variable `collSurplusPool` assign with `_collSurplusPool` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L234)


#

```
File: contracts/CdpManagerStorage.sol

235    ebtcToken = IEBTCToken(_ebtcToken)
```
 state variable `ebtcToken` assign with `_ebtcToken` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L235)


#

```
File: contracts/CdpManagerStorage.sol

236    sortedCdps = ISortedCdps(_sortedCdps)
```
 state variable `sortedCdps` assign with `_sortedCdps` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L236)


#

```
File: contracts/CollSurplusPool.sol

48    borrowerOperationsAddress = _borrowerOperationsAddress
```
 state variable `borrowerOperationsAddress` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48)


#

```
File: contracts/CollSurplusPool.sol

49    cdpManagerAddress = _cdpManagerAddress
```
 state variable `cdpManagerAddress` assign with `_cdpManagerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L49)


#

```
File: contracts/CollSurplusPool.sol

50    activePoolAddress = _activePoolAddress
```
 state variable `activePoolAddress` assign with `_activePoolAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L50)


#

```
File: contracts/CollSurplusPool.sol

51    collateral = ICollateralToken(_collTokenAddress)
```
 state variable `collateral` assign with `_collTokenAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L51)


#

```
File: contracts/EBTCToken.sol

68    cdpManagerAddress = _cdpManagerAddress
```
 state variable `cdpManagerAddress` assign with `_cdpManagerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68)


#

```
File: contracts/EBTCToken.sol

69    borrowerOperationsAddress = _borrowerOperationsAddress
```
 state variable `borrowerOperationsAddress` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L69)


#

```
File: contracts/HintHelpers.sol

34    sortedCdps = ISortedCdps(_sortedCdpsAddress)
```
 state variable `sortedCdps` assign with `_sortedCdpsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L34)


#

```
File: contracts/HintHelpers.sol

35    cdpManager = ICdpManager(_cdpManagerAddress)
```
 state variable `cdpManager` assign with `_cdpManagerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L35)


#

```
File: contracts/LeverageMacroBase.sol

60    borrowerOperations = IBorrowerOperations(_borrowerOperationsAddress)
```
 state variable `borrowerOperations` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L60)


#

```
File: contracts/LeverageMacroBase.sol

61    activePool = IActivePool(_activePool)
```
 state variable `activePool` assign with `_activePool` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L61)


#

```
File: contracts/LeverageMacroBase.sol

62    cdpManager = ICdpCdps(_cdpManager)
```
 state variable `cdpManager` assign with `_cdpManager` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L62)


#

```
File: contracts/LeverageMacroBase.sol

63    ebtcToken = IEBTCToken(_ebtc)
```
 state variable `ebtcToken` assign with `_ebtc` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L63)


#

```
File: contracts/LeverageMacroBase.sol

64    stETH = ICollateralToken(_coll)
```
 state variable `stETH` assign with `_coll` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L64)


#

```
File: contracts/LeverageMacroBase.sol

65    sortedCdps = ISortedCdps(_sortedCdps)
```
 state variable `sortedCdps` assign with `_sortedCdps` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L65)


#

```
File: contracts/LeverageMacroFactory.sol

29    borrowerOperations = _borrowerOperationsAddress
```
 state variable `borrowerOperations` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29)


#

```
File: contracts/LeverageMacroFactory.sol

30    activePool = _activePool
```
 state variable `activePool` assign with `_activePool` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L30)


#

```
File: contracts/LeverageMacroFactory.sol

31    cdpManager = _cdpManager
```
 state variable `cdpManager` assign with `_cdpManager` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L31)


#

```
File: contracts/LeverageMacroFactory.sol

32    ebtcToken = _ebtc
```
 state variable `ebtcToken` assign with `_ebtc` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L32)


#

```
File: contracts/LeverageMacroFactory.sol

33    stETH = _coll
```
 state variable `stETH` assign with `_coll` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L33)


#

```
File: contracts/LeverageMacroFactory.sol

34    sortedCdps = _sortedCdps
```
 state variable `sortedCdps` assign with `_sortedCdps` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L34)


#

```
File: contracts/LeverageMacroReference.sol

36    theOwner = _owner
```
 state variable `theOwner` assign with `_owner` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36)


#

```
File: contracts/PriceFeed.sol

63    fallbackCaller = IFallbackCaller(_fallbackCallerAddress)
```
 state variable `fallbackCaller` assign with `_fallbackCallerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L63)


#

```
File: contracts/PriceFeed.sol

69    ETH_BTC_CL_FEED = AggregatorV3Interface(_ethBtcCLFeed)
```
 state variable `ETH_BTC_CL_FEED` assign with `_ethBtcCLFeed` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L69)


#

```
File: contracts/PriceFeed.sol

70    STETH_ETH_CL_FEED = AggregatorV3Interface(_collEthCLFeed)
```
 state variable `STETH_ETH_CL_FEED` assign with `_collEthCLFeed` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L70](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L70)


#

```
File: contracts/SimplifiedDiamondLike.sol

45    owner = _owner
```
 state variable `owner` assign with `_owner` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45)


#

```
File: contracts/SortedCdps.sol

95    cdpManager = ICdpManager(_cdpManagerAddress)
```
 state variable `cdpManager` assign with `_cdpManagerAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L95)


#

```
File: contracts/SortedCdps.sol

96    borrowerOperationsAddress = _borrowerOperationsAddress
```
 state variable `borrowerOperationsAddress` assign with `_borrowerOperationsAddress` without checking

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L96)


</details>

# 


## External calls in an un-bounded for-loop may result in a DOS
- Severity: Low
- Confidence: Medium

### Description
Calls inside a loop might lead to a denial-of-service attack.

<details>

<summary>
There are 31 instances of this issue:

</summary>

###
#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

69    vars.currentCdpUser != address(0) &&
70                    cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

72    vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

73    vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

90    uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

133    function _calculateCdpStateAfterPartialRedemption(
134            LocalVariables_getRedemptionHints memory vars,
135            uint256 currentCdpDebt,
136            uint256 _price
137        ) internal view returns (uint256, uint256) 
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

141    uint256 newCollShare = cdpManager.getSyncedCdpCollShares(vars.currentCdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153)


#

```
File: contracts/HintHelpers.sol

133    function _calculateCdpStateAfterPartialRedemption(
134            LocalVariables_getRedemptionHints memory vars,
135            uint256 currentCdpDebt,
136            uint256 _price
137        ) internal view returns (uint256, uint256) 
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

144    uint256 collShareToReceive = collateral.getSharesByPooledEth(
145                (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
146            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

102    collateral.getPooledEthByShares(partialRedemptionNewColl) <
103                            MIN_NET_STETH_BALANCE
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

116    vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

117    vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

164    function getApproxHint(
165            uint256 _CR,
166            uint256 _numTrials,
167            uint256 _inputRandomSeed
168        ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) 
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

185    bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197)


#

```
File: contracts/HintHelpers.sol

164    function getApproxHint(
165            uint256 _CR,
166            uint256 _numTrials,
167            uint256 _inputRandomSeed
168        ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) 
```
 has external calls inside a loop: 
```
File: contracts/HintHelpers.sol

186    uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197)


#

```
File: contracts/CdpManagerStorage.sol

534    function _readStEthIndex() internal view returns (uint256, uint256) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

535    return (stEthIndex, collateral.getPooledEthByShares(DECIMAL_PRECISION))
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L534-L536](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L534-L536)


#

```
File: contracts/CdpManagerStorage.sol

552    function calcFeeUponStakingReward(
553            uint256 _newIndex,
554            uint256 _prevIndex
555        ) public view returns (uint256, uint256, uint256) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

564    uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570)


#

```
File: contracts/CdpManagerStorage.sol

574    function _takeSplitAndUpdateFeePerUnit(
575            uint256 _feeTaken,
576            uint256 _newPerUnit,
577            uint256 _newErrorPerUnit
578        ) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

584    require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big")
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588)


#

```
File: contracts/CdpManagerStorage.sol

574    function _takeSplitAndUpdateFeePerUnit(
575            uint256 _feeTaken,
576            uint256 _newPerUnit,
577            uint256 _newErrorPerUnit
578        ) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588)


#

```
File: contracts/CdpManagerStorage.sol

293    function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

297    uint256 _totalCollateralSnapshot = activePool.getSystemCollShares() - _collRemainder
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301)


#

```
File: contracts/CdpManagerStorage.sol

344    function _syncAccounting(bytes32 _cdpId) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

145    singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth(
146                (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price
147            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

163    address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManagerStorage.sol

652    function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652-L657](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652-L657)


#

```
File: contracts/CdpManager.sol

244    function _closeCdpByRedemption(
245            bytes32 _cdpId,
246            uint256 _EBTC,
247            uint256 _collSurplus,
248            uint256 _liquidatorRewardShares,
249            address _borrower
250        ) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

254    activePool.decreaseSystemDebt(_EBTC)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265)


#

```
File: contracts/CdpManager.sol

244    function _closeCdpByRedemption(
245            bytes32 _cdpId,
246            uint256 _EBTC,
247            uint256 _collSurplus,
248            uint256 _liquidatorRewardShares,
249            address _borrower
250        ) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

257    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265)


#

```
File: contracts/CdpManager.sol

244    function _closeCdpByRedemption(
245            bytes32 _cdpId,
246            uint256 _EBTC,
247            uint256 _collSurplus,
248            uint256 _liquidatorRewardShares,
249            address _borrower
250        ) internal 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

202    newNICR != _redeemColFromCdp.partialRedemptionHintNICR ||
203                    collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

220    emit CdpUpdated(
221                    _redeemColFromCdp.cdpId,
222                    ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223                    msg.sender,
224                    _oldDebtAndColl.debt,
225                    _oldDebtAndColl.collShares,
226                    newDebt,
227                    newColl,
228                    Cdps[_redeemColFromCdp.cdpId].stake,
229                    CdpOperation.redeemCollateral
230                )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

424    bytes32 _nextId = sortedCdps.getPrev(_cId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

425    address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManagerStorage.sol

707    function _calculateCR(
708            uint256 currentCollShare,
709            uint256 currentDebt,
710            uint256 _price
711        ) internal view returns (uint256) 
```
 has external calls inside a loop: 
```
File: contracts/CdpManagerStorage.sol

712    uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L707-L714](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L707-L714)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

370    _cId = sortedCdps.getPrev(_cId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
 has external calls inside a loop: 
```
File: contracts/CdpManager.sol

371    currentBorrower = sortedCdps.getOwnerAddress(_cId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


</details>

# 


## Payable Function Without Ether Transfer
- Severity: Low
- Confidence: High

### Description
Payable functions are designed to receive Ether. If a payable function doesn't transfer or store the Ether it receives, the funds can become stuck in the contract, leading to potential loss of funds. This detector identifies functions that are `payable` but lack a mechanism to transfer or store the Ether, warning developers of the potential issue.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/SimplifiedDiamondLike.sol

110    function execute(Operation[] calldata ops) external payable 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126)


#

```
File: contracts/SimplifiedDiamondLike.sol

160    receive() external payable 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162)


#

```
File: contracts/SimplifiedDiamondLike.sol

164    fallback() external payable 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L166)


</details>

# 


## Potential Division by Zero
- Severity: Low
- Confidence: Medium

### Description
identifies potential division by zero operations in the code. It checks for scenarios where a divisor can be zero, leading to a potential division by zero error.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

621    uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622                _totalEBTCSupply
```
 could be division by zero

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621-L622](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621-L622)


#

```
File: contracts/HintHelpers.sol

144    uint256 collShareToReceive = collateral.getSharesByPooledEth(
145                (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
146            )
```
 could be division by zero

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L144-L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L144-L146)


#

```
File: contracts/LiquidationLibrary.sol

558    _incentiveColl = (_totalDebtToBurn * LICR) / _price
```
 could be division by zero

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558)


</details>

# 


## Reentrancy vulnerabilities
- Severity: Low
- Confidence: Medium

### Description

Detection of the [reentrancy bug](https://github.com/trailofbits/not-so-smart-contracts/tree/master/reentrancy).
Only report reentrancy that acts as a double call (see `reentrancy-eth`, `reentrancy-no-eth`).

<details>

<summary>
There are 22 instances of this issue:

</summary>

###
#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	State variables written after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

807    function _getTotalsFromBatchLiquidate_NormalMode(
808            uint256 _price,
809            uint256 _TCR,
810            bytes32[] memory _cdpArray
811        ) internal returns (LiquidationTotals memory totals) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	State variables written after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManager.sol

218    _updateStakeAndTotalStakes(_redeemColFromCdp.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

423    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

344    function _syncAccounting(bytes32 _cdpId) internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

348    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

370    _applyAccumulatedFeeSplit(
371                        _cdpId,
372                        _newColl,
373                        _feeSplitDistributed,
374                        _oldPerUnitCdp,
375                        _systemStEthFeePerUnitIndex
376                    )
```

		- 
```
File: contracts/CdpManagerStorage.sol

600    Cdps[_cdpId].coll = _newColl
```

	- 
```
File: contracts/CdpManagerStorage.sol

386    _cdp.debt = _newDebt
```

	- 
```
File: contracts/CdpManagerStorage.sol

381    _updateRedistributedDebtIndex(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

339    cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex
```

	- 
```
File: contracts/CdpManagerStorage.sol

405    cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

509    function _syncGlobalAccounting() internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

518    _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

519    _updateSystemSnapshotsExcludeCollRemainder(0)
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/CdpManagerStorage.sol

519    _updateSystemSnapshotsExcludeCollRemainder(0)
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

73    function _syncGracePeriod() internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

79    _startGracePeriod(tcr)
```

		- 
```
File: contracts/CdpManagerStorage.sol

53    lastGracePeriodStartTimestamp = uint128(block.timestamp)
```

	- 
```
File: contracts/CdpManagerStorage.sol

81    _endGracePeriod(tcr)
```

		- 
```
File: contracts/CdpManagerStorage.sol

67    lastGracePeriodStartTimestamp = UNSET_TIMESTAMP
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73-L83)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	State variables written after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

714    activePool.transferSystemCollShares(address(collSurplusPool), totals.totalCollSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```

	State variables written after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

		- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```

	- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

		- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

346    function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

347    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	State variables written after the call(s):
	- 
```
File: contracts/ActivePool.sol

359    feeRecipientCollShares = cachedFeeRecipientCollShares
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346-L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346-L363)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

336    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManager.sol

338    totals.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

		- 
```
File: contracts/CdpManager.sol

254    activePool.decreaseSystemDebt(_EBTC)
```

		- 
```
File: contracts/CdpManager.sol

257    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares)
```

		- 
```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```

		- 
```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

	- 
```
File: contracts/CdpManager.sol

435    sortedCdps.remove(_firstRedeemed)
```

	- 
```
File: contracts/CdpManager.sol

442    sortedCdps.batchRemove(_toRemoveIds)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManager.sol

447    _updateBaseRateFromRedemption(
448                totals.collSharesDrawn,
449                totals.price,
450                totals.systemDebtAtStart
451            )
```

		- 
```
File: contracts/CdpManager.sol

629    baseRate = newBaseRate
```

	- 
```
File: contracts/CdpManager.sol

460    _syncGracePeriodForGivenValues(
461                totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
462                totals.systemDebtAtStart - totals.debtToRedeem,
463                totals.price
464            )
```

		- 
```
File: contracts/CdpManagerStorage.sol

53    lastGracePeriodStartTimestamp = uint128(block.timestamp)
```

		- 
```
File: contracts/CdpManagerStorage.sol

67    lastGracePeriodStartTimestamp = UNSET_TIMESTAMP
```

	- 
```
File: contracts/CdpManager.sol

447    _updateBaseRateFromRedemption(
448                totals.collSharesDrawn,
449                totals.price,
450                totals.systemDebtAtStart
451            )
```

		- 
```
File: contracts/CdpManager.sol

697    lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

830    function setBeta(uint256 _beta) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

831    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManager.sol

833    _decayBaseRate()
```

		- 
```
File: contracts/CdpManager.sol

680    baseRate = decayedBaseRate
```

	- 
```
File: contracts/CdpManager.sol

835    beta = _beta
```

	- 
```
File: contracts/CdpManager.sol

833    _decayBaseRate()
```

		- 
```
File: contracts/CdpManager.sol

697    lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

404    function setFeeBps(uint256 _newFee) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

405    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	State variables written after the call(s):
	- 
```
File: contracts/ActivePool.sol

411    feeBps = uint16(_newFee)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404-L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404-L413)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1154    function setFeeBps(uint256 _newFee) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1157    cdpManager.syncGlobalAccounting()
```

	State variables written after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1161    feeBps = uint16(_newFee)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154-L1163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154-L1163)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

390    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

391    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	State variables written after the call(s):
	- 
```
File: contracts/ActivePool.sol

398    feeRecipientAddress = _feeRecipientAddress
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390-L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390-L400)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1140    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1146    cdpManager.syncGlobalAccounting()
```

	State variables written after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1148    feeRecipientAddress = _feeRecipientAddress
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

417    function setFlashLoansPaused(bool _paused) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

418    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	State variables written after the call(s):
	- 
```
File: contracts/ActivePool.sol

420    flashLoansPaused = _paused
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417-L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417-L422)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1167    function setFlashLoansPaused(bool _paused) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1168    cdpManager.syncGlobalAccounting()
```

	State variables written after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1170    flashLoansPaused = _paused
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167-L1172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167-L1172)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

111    function setGracePeriod(uint128 _gracePeriod) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

117    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

118    recoveryModeGracePeriodDuration = _gracePeriod
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111-L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111-L120)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

807    function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

817    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManager.sol

820    _decayBaseRate()
```

		- 
```
File: contracts/CdpManager.sol

680    baseRate = decayedBaseRate
```

	- 
```
File: contracts/CdpManager.sol

820    _decayBaseRate()
```

		- 
```
File: contracts/CdpManager.sol

697    lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE
```

	- 
```
File: contracts/CdpManager.sol

823    minuteDecayFactor = _minuteDecayFactor
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807-L825](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807-L825)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

788    function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

798    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManager.sol

800    redemptionFeeFloor = _redemptionFeeFloor
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788-L802](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788-L802)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

843    function setRedemptionsPaused(bool _paused) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

844    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	State variables written after the call(s):
	- 
```
File: contracts/CdpManager.sol

845    _decayBaseRate()
```

		- 
```
File: contracts/CdpManager.sol

680    baseRate = decayedBaseRate
```

	- 
```
File: contracts/CdpManager.sol

845    _decayBaseRate()
```

		- 
```
File: contracts/CdpManager.sol

697    lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE
```

	- 
```
File: contracts/CdpManager.sol

847    redemptionsPaused = _paused
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843-L849)


</details>

# 


## SafeApprove Deprecated
- Severity: Low
- Confidence: High

### Description
The `safeApprove()` method is deprecated and has been replaced with `safeIncreaseAllowance()` and `safeDecreaseAllowance()`. This detector identifies instances where the deprecated `safeApprove()` method is used.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

405    IERC20(swapData.tokenForSwap).safeApprove(
406                swapData.addressForApprove,
407                swapData.exactApproveAmount
408            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405-L408](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405-L408)


#

```
File: contracts/LeverageMacroBase.sol

427    IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)


</details>

# 


## Setter No Initial Value Check Detection
- Severity: Low
- Confidence: Medium

### Description
This detector flags setter functions that lack an initial value check. Lack of such a check can lead to assigning wrong values to the variable, causing unexpected contract behavior.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

830    function setBeta(uint256 _beta) external requiresAuth 
```
 Setter lacks an initial value check
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837)


</details>

# 


## receive()/payable fallback() function does not authorize requests
- Severity: Low
- Confidence: High

### Description

Having no access control on the function (e.g. `require(msg.sender == address(weth))`) means that someone may send Ether to the contract, 
and have no way to get anything back out, which is a loss of funds. 
If the concern is having to spend a small amount of gas to check the sender against an immutable address, 
the code should at least have a function to rescue mistakenly-sent Ether.


<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/SimplifiedDiamondLike.sol

160    receive() external payable 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162)


</details>

# 


## Unsafe Cast Unsigned to Signed
- Severity: Low
- Confidence: High

### Description
An unsafe cast occurs when a variable or expression of an unsigned/signed integer is converted to a signed/unsigned integer without proper checks. This type of cast can lead to unexpected behavior and vulnerabilities in the code.

When an unsigned integer is cast to a signed integer, the underlying bit representation remains the same, but the interpretation of the value changes. This can result in overflow or wraparound issues, leading to incorrect calculations or security vulnerabilities.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

802    uint256(_ethBtcAnswer)
```
 usafe cast from int256 to uint256 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L802](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L802)


#

```
File: contracts/PriceFeed.sol

803    uint256(_stEthEthAnswer)
```
 usafe cast from int256 to uint256 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L803](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L803)


</details>

# 


## Unsafe Downcast 
- Severity: Low
- Confidence: High

### Description
When a type is downcast to a smaller type, the higher-order bits are truncated, effectively applying a modulo operation to the original value. This can introduce vulnerabilities and cause the program to behave unexpectedly. 

If you intend to perform an unchecked modulo operation, it is advisable to use the syntax uncheck{ x % y}. This not only makes the code clearer but also helps prevent potential bugs and ensures the intended behavior of the operation.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

559    uint128(CdpIds.length - 1)
```
 usafe downcast size from - 256 to size 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L559](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L559)


#

```
File: contracts/SortedCdps.sol

125    uint160(_tmp)
```
 usafe downcast size from - 256 to size 160

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L125)


</details>

# 


## Approve/SafeApprove Without Zero Check
- Severity: Low
- Confidence: Medium

### Description
Detects calls to approve() or safeApprove() without ensuring the current allowance is zero.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

405    IERC20(swapData.tokenForSwap).safeApprove(
406                swapData.addressForApprove,
407                swapData.exactApproveAmount
408            )
```
This variable might be zero: `swapData.exactApproveAmount` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405-L408](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405-L408)


</details>

# 



## Check Oracle Data Freshness
- Severity: LOW
- Confidence: High

### Description
Detect contracts that do not appear to be checking the freshness of their oracle data. Contracts relying on oracle data, especially when using Chainlink's Off-Chain Reporting (OCR), should regularly check that the data is fresh, i.e., that it has been updated recently enough to be reliable. Without these checks, old prices may be used if OCR was unable to push an update in time, leading to potential inaccuracies or manipulations. It is essential for operations relying on time-sensitive or price-sensitive data to ensure the freshness of their oracle data.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

634    try ETH_BTC_CL_FEED.latestRoundData() returns (
635                uint80 roundId,
636                int256 answer,
637                uint256,
638                /* startedAt */
639                uint256 timestamp,
640                uint80 /* answeredInRound */
641            ) {
642                ethBtcAnswer = answer;
643                chainlinkResponse.roundEthBtcId = roundId;
644                chainlinkResponse.timestampEthBtc = timestamp;
645            } catch {
646                // If call to Chainlink aggregator reverts, return a zero response with success = false
647                return chainlinkResponse;
648            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634-L648](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634-L648)


#

```
File: contracts/PriceFeed.sol

650    try STETH_ETH_CL_FEED.latestRoundData() returns (
651                uint80 roundId,
652                int256 answer,
653                uint256,
654                /* startedAt */
655                uint256 timestamp,
656                uint80 /* answeredInRound */
657            ) {
658                stEthEthAnswer = answer;
659                chainlinkResponse.roundStEthEthId = roundId;
660                chainlinkResponse.timestampStEthEth = timestamp;
661            } catch {
662                // If call to Chainlink aggregator reverts, return a zero response with success = false
663                return chainlinkResponse;
664            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650-L664](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650-L664)


</details>

# 


## Missing Sequencer Check
- Severity: Low
- Confidence: High

### Description
Chainlink recommends that users using price oracles, check whether the Arbitrum Sequencer is active. If the sequencer goes down, the Chainlink oracles will have stale prices from before the downtime, until a new L2 OCR transaction goes through. Users who submit their transactions via the L1 Dealyed Inbox will be able to take advantage of these stale prices. Use a Chainlink oracle to determine whether the sequencer is offline or not, and don't allow operations to take place while the sequencer is offline. 

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

634    try ETH_BTC_CL_FEED.latestRoundData() returns (
635                uint80 roundId,
636                int256 answer,
637                uint256,
638                /* startedAt */
639                uint256 timestamp,
640                uint80 /* answeredInRound */
641            ) {
642                ethBtcAnswer = answer;
643                chainlinkResponse.roundEthBtcId = roundId;
644                chainlinkResponse.timestampEthBtc = timestamp;
645            } catch {
646                // If call to Chainlink aggregator reverts, return a zero response with success = false
647                return chainlinkResponse;
648            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634-L648](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634-L648)


#

```
File: contracts/PriceFeed.sol

650    try STETH_ETH_CL_FEED.latestRoundData() returns (
651                uint80 roundId,
652                int256 answer,
653                uint256,
654                /* startedAt */
655                uint256 timestamp,
656                uint80 /* answeredInRound */
657            ) {
658                stEthEthAnswer = answer;
659                chainlinkResponse.roundStEthEthId = roundId;
660                chainlinkResponse.timestampStEthEth = timestamp;
661            } catch {
662                // If call to Chainlink aggregator reverts, return a zero response with success = false
663                return chainlinkResponse;
664            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650-L664](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650-L664)


</details>

# 


## Unchecked transfer
- Severity: Low
- Confidence: Medium

### Description
The return value of an external transfer/transferFrom call is not checked

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

224    ebtcToken.transfer(msg.sender, ebtcBal)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224)


#

```
File: contracts/ActivePool.sol

274    collateral.transfer(address(receiver), amount)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274)


#

```
File: contracts/ActivePool.sol

283    collateral.transferFrom(address(receiver), address(this), amountWithFee)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283)


#

```
File: contracts/ActivePool.sol

286    collateral.transfer(feeRecipientAddress, fee)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286)


#

```
File: contracts/BorrowerOperations.sol

785    collateral.transferFrom(msg.sender, address(activePool), _stEthBalance)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785)


#

```
File: contracts/BorrowerOperations.sol

1100    ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)


</details>

# 


## Calls transfer()/transferFrom() With IERC20
- Severity: Low
- Confidence: High

### Description
The transfer() and transferFrom() methods are part of the ERC-20 standard, designed for transferring tokens between accounts. However, these methods could be risky when transferring tokens to smart contracts because they don't guarantee that the receiving smart contract will handle the transferred tokens correctly, potentially leading to permanent token loss. ERC-20 standard doesn't include a 'onTokenReceived' function or similar to alert the recipient about incoming transfers. Therefore, the 'transfer' and 'transferFrom' functions are not reliable for interactions with arbitrary contracts. A safer alternative is to use safeTransfer() and safeTransferFrom() methods provided by libraries like OpenZeppelin's SafeERC20. These methods add a layer of protection by checking if the recipient is a contract and if it has a function to handle incoming tokens. If these checks are not passed, the transfer operation is not executed, hence preventing potential token loss.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

274    collateral.transfer(address(receiver), amount)
```
 use safeTransferFrom instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274)


#

```
File: contracts/ActivePool.sol

283    collateral.transferFrom(address(receiver), address(this), amountWithFee)
```
 use safeTransferFrom instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283)


#

```
File: contracts/ActivePool.sol

286    collateral.transfer(feeRecipientAddress, fee)
```
 use safeTransferFrom instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286)


#

```
File: contracts/BorrowerOperations.sol

785    collateral.transferFrom(msg.sender, address(activePool), _stEthBalance)
```
 use safeTransferFrom instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785)


#

```
File: contracts/BorrowerOperations.sol

1100    ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount)
```
 use safeTransferFrom instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)


#

```
File: contracts/LeverageMacroBase.sol

224    ebtcToken.transfer(msg.sender, ebtcBal)
```
 use safeTransferFrom instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224)


</details>

# 


## Zero-value transfers may revert
- Severity: Low
- Confidence: High

### Description
This detector identifies instances where zero-valued ERC20 token transfers are made. Even though EIP-20 states that zero-valued transfers must be treated as normal transfers and events must be triggered, some tokens may revert if this is attempted, which can cause transactions that involve other tokens (such as batch operations) to fully revert. Therefore, it may be safer and more gas-efficient to skip the transfer if the amount is zero.

<details>

<summary>
There are 7 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

283    collateral.transferFrom(address(receiver), address(this), amountWithFee)
```
This variable might be zero: `amountWithFee` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283)


#

```
File: contracts/ActivePool.sol

286    collateral.transfer(feeRecipientAddress, fee)
```
This variable might be zero: `fee` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286)


#

```
File: contracts/ActivePool.sol

381    IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount)
```
This variable might be zero: `amount` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381)


#

```
File: contracts/BorrowerOperations.sol

785    collateral.transferFrom(msg.sender, address(activePool), _stEthBalance)
```
This variable might be zero: `_stEthBalance` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785)


#

```
File: contracts/BorrowerOperations.sol

1100    ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount)
```
This variable might be zero: `fee + amount` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)


#

```
File: contracts/CollSurplusPool.sol

148    IERC20(token).safeTransfer(feeRecipientAddress, amount)
```
This variable might be zero: `amount` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)


#

```
File: contracts/LeverageMacroBase.sol

237    IERC20(token).safeTransfer(msg.sender, amount)
```
This variable might be zero: `amount` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237)


</details>

# 

<br><br>
# Non-Critical Issues



## Variables with all caps names that are not constants or immutables
- Severity: Non-Critical
- Confidence: Medium

### Description
This detector flags variable declarations where the variable name is in all capital letters but the variable is not declared as a 'constant' or 'immutable'. In solidity, it is a convention to reserve variable names in all capital letters for constants and immutables. Variable names that need to be different based on the class they come from should be returned by a 'view' or 'pure' function instead.

<details>

<summary>
There are 16 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

600    uint256 TCR = _computeTCRWithGivenSystemValues(_systemCollShares, _systemDebt, _price)
```

#

```
File: contracts/CdpManagerStorage.sol

676    uint256 NICR = EbtcMath._computeNominalCR(currentCollShares, currentEBTCDebt)
```

#

```
File: contracts/CdpManagerStorage.sol

693    uint256 NICR = EbtcMath._computeNominalCR(_newColl, _newDebt)
```

#

```
File: contracts/CdpManagerStorage.sol

703    uint256 ICR = _calculateCR(currentCollShares, currentEBTCDebt, _price)
```

#

```
File: contracts/Governor.sol

17    bytes32 NO_ROLES = bytes32(0)
```

#

```
File: contracts/LiquidationLibrary.sol

74    uint256 _ICR = getCachedICR(_cdpId, _price)
```

#

```
File: contracts/LiquidationLibrary.sol

75    uint256 _TCR
```

#

```
File: contracts/LiquidationLibrary.sol

692    uint256 _TCR
```

#

```
File: contracts/LiquidationLibrary.sol

745    uint256 _TCR = _computeTCRWithGivenSystemValues(
746                vars.entireSystemColl,
747                vars.entireSystemDebt,
748                _price
749            )
```

#

```
File: contracts/LiquidationSequencer.sol

53    uint256 _TCR
```

#

```
File: contracts/Proxy/BorrowerWrappersScript.sol

116    uint256 ICR = cdpManager.getCachedICR(_cdpId, price)
```

#

```
File: contracts/SyncedLiquidationSequencer.sol

49    uint256 _TCR
```

#

```
File: contracts/SyncedLiquidationSequencer.sol

69    uint256 _TCR = cdpManager.getSyncedTCR(_price)
```

#

```
File: contracts/TestContracts/EBTCTokenCaller.sol

8    IEBTCToken EBTC
```

#

```
File: contracts/TestContracts/invariants/Properties.sol

204    uint256 NICR_ERROR_THRESHOLD = 1e8
```

#

```
File: contracts/TestContracts/invariants/Properties.sol

163    uint256 _TCR = cdpManager.getCachedTCR(_price)
```

</details>

# 


## Avoid Magic Numbers
- Severity: Non-Critical
- Confidence: High

### Description
Magic numbers are hard-coded numeric values that are not explicitly defined or explained in the code. They can make the code difficult to read, understand, and maintain. Additionally, if the values of magic numbers are changed unintentionally, it can lead to unexpected behavior or bugs in the smart contract logic.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

531    returndatacopy(add(_returnData, 0x20), 0, _toCopy)
```
 dont use a magic number @ **0x20**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L531](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L531)


#

```
File: contracts/LeverageMacroBase.sol

514    _success := call(
515                    _gas, // gas
516                    _target, // recipient
517                    _value, // ether value
518                    add(_calldata, 0x20), // inloc
519                    mload(_calldata), // inlen
520                    0, // outloc
521                    0 // outlen
522                )
```
 dont use a magic number @ **0x20**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L514-L522](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L514-L522)


#

```
File: contracts/PriceFeed.sol

800    return
801                (_scaledDecimal *
802                    uint256(_ethBtcAnswer) *
803                    uint256(_stEthEthAnswer) *
804                    EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2)
```
 dont use a magic number @ **2**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804)


#

```
File: contracts/PriceFeed.sol

800    return
801                (_scaledDecimal *
802                    uint256(_ethBtcAnswer) *
803                    uint256(_stEthEthAnswer) *
804                    EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2)
```
 dont use a magic number @ **10**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804)


#

```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
 dont use a magic number @ **10**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799)


#

```
File: contracts/SimplifiedDiamondLike.sol

56    require(sig != 0x94b24d09)
```
 dont use a magic number @ **0x94b24d09**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56)


#

```
File: contracts/SimplifiedDiamondLike.sol

144    success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)
```
 dont use a magic number @ **0x20**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144)


#

```
File: contracts/SimplifiedDiamondLike.sol

149    success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)
```
 dont use a magic number @ **0x20**
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L149)


</details>

# 


## Cast to bytes or bytes32 for clearer semantic meaning
- Severity: Non-Critical
- Confidence: High

### Description
Using a cast on a single argument, rather than abi.encodePacked() makes the intended operation more clear, leading to less reviewer confusion.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/HintHelpers.sol

182    abi.encodePacked(latestRandomSeed)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)


</details>

# 


## Complex math in a single line
- Severity: Non-Critical
- Confidence: Medium

### Description
Complex arithmetic calculations in a single line can reduce code readability. It's often beneficial to split these into multiple lines or separate operations.

<details>

<summary>
There are 9 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

818    require(
819                _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820                "BorrowerOperations: There must be either a collateral change or a debt change"
821            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821)


#

```
File: contracts/CdpManager.sol

389    currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389)


#

```
File: contracts/CdpManagerStorage.sol

624    _cdpStEthFeePerUnitIndex == 0 ||
625                _cdpCol == 0 ||
626                _cdpStEthFeePerUnitIndex == _systemStEthFeePerUnitIndex
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L624-L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L624-L626)


#

```
File: contracts/HintHelpers.sol

85    vars.currentCdpUser != address(0) &&
86                    vars.remainingEbtcToRedeem > 0 &&
87                    _maxIterations-- > 0
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L85-L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L85-L87)


#

```
File: contracts/PriceFeed.sol

420    _response.timestampEthBtc == 0 ||
421                _response.timestampEthBtc > block.timestamp ||
422                _response.timestampStEthEth == 0 ||
423                _response.timestampStEthEth > block.timestamp
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L420-L423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L420-L423)


#

```
File: contracts/PriceFeed.sol

800    return
801                (_scaledDecimal *
802                    uint256(_ethBtcAnswer) *
803                    uint256(_stEthEthAnswer) *
804                    EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804)


#

```
File: contracts/SortedCdps.sol

520    bool _exist = _id != dummyId && (data.head == _id || data.tail == _id)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L520](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L520)


#

```
File: contracts/SortedCdps.sol

523    _exist = _id != dummyId && (_node.nextId != dummyId && _node.prevId != dummyId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L523](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L523)


#

```
File: contracts/SortedCdps.sol

607    return
608                    data.nodes[_prevId].nextId == _nextId &&
609                    cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610                    _NICR >= cdpManager.getCachedNominalICR(_nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610)


</details>

# 


## Improving Code Readability with Named Mappings 
- Severity: Non-Critical
- Confidence: High

### Description
In Solidity, starting from version 0.8.18, you have the ability to provide explicit names to mappings. This feature allows you to improve code readability and make it easier for developers to understand the purpose of each mapping used in your smart contract.

By upgrading to Solidity version 0.8.18 or later and utilizing named mappings, you can enhance the clarity and maintainability of your codebase. Giving meaningful names to mappings helps other developers (including your future self) to quickly grasp the intention and usage of each mapping within your contract, thereby reducing potential confusion or errors.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L65)


#

```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168)


#

```
File: contracts/CdpManagerStorage.sol

190    mapping(bytes32 => uint256) public cdpDebtRedistributionIndex
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L190)


#

```
File: contracts/CdpManagerStorage.sol

202    mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L202)


#

```
File: contracts/CollSurplusPool.sol

30    mapping(address => uint256) internal balances
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L30)


#

```
File: contracts/EBTCToken.sol

51    mapping(address => uint256) private _balances
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51)


#

```
File: contracts/EBTCToken.sol

52    mapping(address => mapping(address => uint256)) private _allowances
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L52)


#

```
File: contracts/Governor.sol

30    mapping(uint8 => string) internal roleNames
```
 consider add name for the mapping arguments

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30)


</details>

# 


## Consider Using 'delete' Rather than Assigning Zero/False to Clear Values
- Severity: Non-Critical
- Confidence: High

### Description
Detects instances where 'delete' could be used instead of assigning zero/false to clear values

<details>

<summary>
There are 21 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

690    block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692)


#

```
File: contracts/CdpManagerStorage.sol

272    Cdps[_cdpId].coll = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L272)


#

```
File: contracts/CdpManagerStorage.sol

273    Cdps[_cdpId].debt = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L273](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L273)


#

```
File: contracts/CdpManagerStorage.sol

274    Cdps[_cdpId].liquidatorRewardShares = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L274)


#

```
File: contracts/CdpManagerStorage.sol

276    cdpDebtRedistributionIndex[_cdpId] = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L276](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L276)


#

```
File: contracts/CdpManagerStorage.sol

277    cdpStEthFeePerUnitIndex[_cdpId] = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L277](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L277)


#

```
File: contracts/CdpManagerStorage.sol

413    Cdps[_cdpId].stake = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L413)


#

```
File: contracts/CollSurplusPool.sol

94    balances[_account] = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L94)


#

```
File: contracts/HintHelpers.sol

105    partialRedemptionHintNICR = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105)


#

```
File: contracts/HintHelpers.sol

106    partialRedemptionNewColl = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L106)


#

```
File: contracts/HintHelpers.sol

109    vars.remainingEbtcToRedeem = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L109)


#

```
File: contracts/LiquidationLibrary.sol

100    _TCR < CCR ? true : false
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100)


#

```
File: contracts/LiquidationLibrary.sol

264    _collSurplus = 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L264)


#

```
File: contracts/LiquidationLibrary.sol

358    _recoveryState.entireSystemDebt = _recoveryState.entireSystemDebt > _totalDebtToBurn
359                ? _recoveryState.entireSystemDebt - _totalDebtToBurn
360                : 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L358-L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L358-L360)


#

```
File: contracts/LiquidationLibrary.sol

361    _recoveryState.entireSystemColl = _recoveryState.entireSystemColl > _totalColToSend
362                ? _recoveryState.entireSystemColl - _totalColToSend
363                : 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L361-L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L361-L363)


#

```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596)


#

```
File: contracts/LiquidationLibrary.sol

603    collSurplus = (toLiquidator == _totalColToSend) ? 0 : _totalColToSend - toLiquidator
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L603](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L603)


#

```
File: contracts/LiquidationLibrary.sol

695    vars.recoveryModeAtStart = _TCR < CCR ? true : false
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L695](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L695)


#

```
File: contracts/LiquidationLibrary.sol

742    vars.backToNormalMode = false
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L742](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L742)


#

```
File: contracts/LiquidationLibrary.sol

788    vars.backToNormalMode = _TCR < CCR ? false : true
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788)


#

```
File: contracts/PriceFeed.sol

457    maxPrice > 0
458                ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice
459                : 0
```
  Consider using 'delete' to clear the value.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457-L459](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457-L459)


</details>

# 


## Do not calculate constants
- Severity: Non-Critical
- Confidence: High

### Description
Due to how constant variables are implemented in Solidity (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas. While in most cases, the compiler will optimize these computations away, it is considered a best practice to write code that does not rely on the compiler optimization.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)


</details>

# 


## Constants in Comparisons on Left Side
- Severity: Non-Critical
- Confidence: High

### Description
Where constants are not placed on the left side in comparison operations. In many programming languages, it is considered a best practice to place constants on the left side of comparisons to improve code readability and reduce the likelihood of accidental assignment bugs.

<details>

<summary>
There are 72 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

278    receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L278)


#

```
File: contracts/BorrowerOperations.sol

831    status == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831)


#

```
File: contracts/BorrowerOperations.sol

145    locked == OPEN
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)


#

```
File: contracts/BorrowerOperations.sol

147    ReentrancyGuard(address(cdpManager)).locked() == OPEN
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L147)


#

```
File: contracts/BorrowerOperations.sol

826    status == 1
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826)


#

```
File: contracts/BorrowerOperations.sol

847    _stEthBalanceDecrease == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L847](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L847)


#

```
File: contracts/BorrowerOperations.sol

808    _stEthBalanceIncrease == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L808](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L808)


#

```
File: contracts/BorrowerOperations.sol

819    _stEthBalanceIncrease != 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L819)


#

```
File: contracts/BorrowerOperations.sol

748    _collReceived != 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L748](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L748)


#

```
File: contracts/BorrowerOperations.sol

1092    receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1092](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1092)


#

```
File: contracts/CdpManager.sol

159    newDebt == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L159)


#

```
File: contracts/CdpManagerStorage.sol

443    totalCollateralSnapshot == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L443](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L443)


#

```
File: contracts/CdpManagerStorage.sol

624    _cdpStEthFeePerUnitIndex == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L624)


#

```
File: contracts/CdpManagerStorage.sol

625    _cdpCol == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L625](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L625)


#

```
File: contracts/CdpManager.sol

332    redemptionsPaused == false
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)


#

```
File: contracts/CdpManager.sol

377    _maxIterations == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L377)


#

```
File: contracts/CdpManagerStorage.sol

52    lastGracePeriodStartTimestamp == UNSET_TIMESTAMP
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L52)


#

```
File: contracts/CdpManagerStorage.sol

66    lastGracePeriodStartTimestamp != UNSET_TIMESTAMP
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L66)


#

```
File: contracts/CdpManager.sol

434    _numCdpsFullyRedeemed == 1
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L434](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L434)


#

```
File: contracts/CdpManagerStorage.sol

242    locked == OPEN
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)


#

```
File: contracts/CdpManagerStorage.sol

244    ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L244)


#

```
File: contracts/CdpManagerStorage.sol

899    cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L899](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L899)


#

```
File: contracts/Governor.sol

99    (uint256(byteMap >> i) & 1) != 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L99)


#

```
File: contracts/Governor.sol

108    (uint256(byteMap >> i) & 1) != 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L108)


#

```
File: contracts/HintHelpers.sol

78    _maxIterations == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L78)


#

```
File: contracts/HintHelpers.sol

171    arrayLength == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L171)


#

```
File: contracts/LiquidationLibrary.sol

90    cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L90)


#

```
File: contracts/LiquidationLibrary.sol

863    _debt == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L863](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L863)


#

```
File: contracts/LiquidationLibrary.sol

144    _liqState.partialAmount == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L144)


#

```
File: contracts/LiquidationLibrary.sol

158    liquidationValues.totalCollToSendToLiquidator == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L158)


#

```
File: contracts/LiquidationLibrary.sol

159    liquidationValues.debtToBurn == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L159)


#

```
File: contracts/LiquidationLibrary.sol

417    newColl == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L417)


#

```
File: contracts/LiquidationLibrary.sol

56    _partialAmount != 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)


#

```
File: contracts/LiquidationLibrary.sol

681    _cdpArray.length != 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L681)


#

```
File: contracts/PriceFeed.sol

695    _currentRoundStEthEthId == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L695](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L695)


#

```
File: contracts/PriceFeed.sol

420    _response.timestampEthBtc == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L420)


#

```
File: contracts/PriceFeed.sol

422    _response.timestampStEthEth == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L422)


#

```
File: contracts/PriceFeed.sol

777    _roundId == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L777)


#

```
File: contracts/PriceFeed.sol

471    _response.timestamp == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L471)


#

```
File: contracts/PriceFeed.sol

475    _response.answer == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L475)


#

```
File: contracts/PriceFeed.sol

532    minPrice == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L532](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L532)


#

```
File: contracts/SimplifiedDiamondLike.sol

56    sig != 0x94b24d09
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56)


#

```
File: contracts/SimplifiedDiamondLike.sol

194    case 0 {
195                    revert(0, returndatasize())
196                }
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L194-L196](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L194-L196)


#

```
File: contracts/SortedCdps.sol

89    _size == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L89)


#

```
File: contracts/SortedCdps.sol

185    _currentCdpId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185)


#

```
File: contracts/SortedCdps.sol

181    startNodeId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L181](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L181)


#

```
File: contracts/SortedCdps.sol

248    _currentCdpId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248)


#

```
File: contracts/SortedCdps.sol

244    startNodeId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L244)


#

```
File: contracts/SortedCdps.sol

316    startNodeId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L316](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L316)


#

```
File: contracts/SortedCdps.sol

305    maxArraySize == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L305)


#

```
File: contracts/SortedCdps.sol

318    _currentCdpId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318)


#

```
File: contracts/SortedCdps.sol

696    prevId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L696](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L696)


#

```
File: contracts/SortedCdps.sol

596    _nextId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L596)


#

```
File: contracts/SortedCdps.sol

520    _id != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L520](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L520)


#

```
File: contracts/SortedCdps.sol

599    _prevId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L599](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L599)


#

```
File: contracts/SortedCdps.sol

369    _id != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369)


#

```
File: contracts/SortedCdps.sol

699    prevId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L699](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L699)


#

```
File: contracts/SortedCdps.sol

602    _nextId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L602)


#

```
File: contracts/SortedCdps.sol

382    prevId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L382](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L382)


#

```
File: contracts/SortedCdps.sol

702    nextId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L702](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L702)


#

```
File: contracts/SortedCdps.sol

523    _id != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L523](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L523)


#

```
File: contracts/SortedCdps.sol

386    prevId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L386](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L386)


#

```
File: contracts/SortedCdps.sol

652    nextId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652)


#

```
File: contracts/SortedCdps.sol

537    data.size == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L537](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L537)


#

```
File: contracts/SortedCdps.sol

391    nextId == dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L391](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L391)


#

```
File: contracts/SortedCdps.sol

682    prevId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L682)


#

```
File: contracts/SortedCdps.sol

689    nextId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L689](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L689)


#

```
File: contracts/SortedCdps.sol

629    prevId != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629)


#

```
File: contracts/SortedCdps.sol

352    cdpManager.getCdpStatus(_id) == 0
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352)


#

```
File: contracts/SortedCdps.sol

442    _lastNext != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L442](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L442)


#

```
File: contracts/SortedCdps.sol

428    _firstPrev != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L428](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L428)


#

```
File: contracts/SortedCdps.sol

437    _firstPrev != dummyId
```
 placed the const on the left

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L437)


</details>

# 


## constant/immutable variable names should use capital letters and underscore
- Severity: Non-Critical
- Confidence: High

### Description
Solidity defines a [naming convention](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#constants) that should be followed for constant/immutable variable names.According to the convention, constant/immutable variable names should be in capital and underscore.

<details>

<summary>
There are 62 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

26    address public immutable borrowerOperationsAddress
```

#

```
File: contracts/ActivePool.sol

27    address public immutable cdpManagerAddress
```

#

```
File: contracts/ActivePool.sol

28    address public immutable collSurplusPoolAddress
```

#

```
File: contracts/ActivePool.sol

34    ICollateralToken public immutable collateral
```

#

```
File: contracts/BorrowerOperations.sol

53    ICdpManager public immutable cdpManager
```

#

```
File: contracts/BorrowerOperations.sol

55    ICollSurplusPool public immutable collSurplusPool
```

#

```
File: contracts/BorrowerOperations.sol

59    IEBTCToken public immutable ebtcToken
```

#

```
File: contracts/BorrowerOperations.sol

62    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/CRLens.sol

11    ICdpManager public immutable cdpManager
```

#

```
File: contracts/CRLens.sol

12    IPriceFeed public immutable priceFeed
```

#

```
File: contracts/CdpManagerStorage.sol

126    address public immutable borrowerOperationsAddress
```

#

```
File: contracts/CdpManagerStorage.sol

128    ICollSurplusPool immutable collSurplusPool
```

#

```
File: contracts/CdpManagerStorage.sol

130    IEBTCToken public immutable override ebtcToken
```

#

```
File: contracts/CdpManagerStorage.sol

132    address public immutable liquidationLibrary
```

#

```
File: contracts/CdpManagerStorage.sol

135    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/CdpManagerStorage.sol

152    uint256 internal immutable deploymentStartTime
```

#

```
File: contracts/CollSurplusPool.sol

21    address public immutable borrowerOperationsAddress
```

#

```
File: contracts/CollSurplusPool.sol

22    address public immutable cdpManagerAddress
```

#

```
File: contracts/CollSurplusPool.sol

23    address public immutable activePoolAddress
```

#

```
File: contracts/CollSurplusPool.sol

24    address public immutable feeRecipientAddress
```

#

```
File: contracts/CollSurplusPool.sol

25    ICollateralToken public immutable collateral
```

#

```
File: contracts/Dependencies/EbtcBase.sol

41    IActivePool public immutable activePool
```

#

```
File: contracts/Dependencies/EbtcBase.sol

43    IPriceFeed public immutable override priceFeed
```

#

```
File: contracts/Dependencies/EbtcBase.sol

46    ICollateralToken public immutable collateral
```

#

```
File: contracts/EBTCDeployer.sol

9    string public constant name = "eBTC Deployer"
```

#

```
File: contracts/EBTCToken.sol

55    address public immutable cdpManagerAddress
```

#

```
File: contracts/EBTCToken.sol

56    address public immutable borrowerOperationsAddress
```

#

```
File: contracts/HintHelpers.sol

14    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/HintHelpers.sol

15    ICdpManager public immutable cdpManager
```

#

```
File: contracts/LeverageMacroBase.sol

29    IBorrowerOperations public immutable borrowerOperations
```

#

```
File: contracts/LeverageMacroBase.sol

30    IActivePool public immutable activePool
```

#

```
File: contracts/LeverageMacroBase.sol

31    ICdpCdps public immutable cdpManager
```

#

```
File: contracts/LeverageMacroBase.sol

32    IEBTCToken public immutable ebtcToken
```

#

```
File: contracts/LeverageMacroBase.sol

33    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/LeverageMacroBase.sol

34    ICollateralToken public immutable stETH
```

#

```
File: contracts/LeverageMacroBase.sol

35    bool internal immutable willSweep
```

#

```
File: contracts/LeverageMacroFactory.sol

12    address public immutable borrowerOperations
```

#

```
File: contracts/LeverageMacroFactory.sol

13    address public immutable activePool
```

#

```
File: contracts/LeverageMacroFactory.sol

14    address public immutable cdpManager
```

#

```
File: contracts/LeverageMacroFactory.sol

15    address public immutable ebtcToken
```

#

```
File: contracts/LeverageMacroFactory.sol

16    address public immutable stETH
```

#

```
File: contracts/LeverageMacroFactory.sol

17    address public immutable sortedCdps
```

#

```
File: contracts/LeverageMacroReference.sol

12    address internal immutable theOwner
```

#

```
File: contracts/LiquidationSequencer.sol

18    ICdpManager public immutable cdpManager
```

#

```
File: contracts/LiquidationSequencer.sol

19    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/MultiCdpGetter.sol

18    CdpManager public immutable cdpManager
```

#

```
File: contracts/MultiCdpGetter.sol

19    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/Proxy/BorrowerOperationsScript.sol

8    IBorrowerOperations immutable borrowerOperations
```

#

```
File: contracts/Proxy/BorrowerWrappersScript.sol

22    ICdpManager immutable cdpManager
```

#

```
File: contracts/Proxy/BorrowerWrappersScript.sol

23    IPriceFeed immutable priceFeed
```

#

```
File: contracts/Proxy/BorrowerWrappersScript.sol

24    IERC20 immutable ebtcToken
```

#

```
File: contracts/Proxy/BorrowerWrappersScript.sol

26    ICollateralToken immutable collToken
```

#

```
File: contracts/Proxy/CdpManagerScript.sol

10    ICdpManager immutable cdpManager
```

#

```
File: contracts/Proxy/TokenScript.sol

10    IERC20 immutable token
```

#

```
File: contracts/SimplifiedDiamondLike.sol

42    address public immutable owner
```

#

```
File: contracts/SortedCdps.sol

54    address public immutable borrowerOperationsAddress
```

#

```
File: contracts/SortedCdps.sol

56    ICdpManager public immutable cdpManager
```

#

```
File: contracts/SortedCdps.sol

58    uint256 public immutable maxSize
```

#

```
File: contracts/SortedCdps.sol

80    bytes32 public constant dummyId =
81            0x0000000000000000000000000000000000000000000000000000000000000000
```

#

```
File: contracts/SyncedLiquidationSequencer.sol

13    ICdpManager public immutable cdpManager
```

#

```
File: contracts/SyncedLiquidationSequencer.sol

14    ISortedCdps public immutable sortedCdps
```

#

```
File: contracts/TestContracts/BaseStorageVariables.sol

57    uint internal constant diff_tolerance = 0.000000000002e18
```

</details>

# 


## Contract Ordering Violation Style Guide
- Severity: Non-Critical
- Confidence: High

### Description
The contract ordering detector identifies cases where the order of contract layout in a Solidity contract does not follow the recommended style guide. According to the Solidity style guide, contract should be laid out in a specific order: 1) Type declarations, 2) State variables, 3) Events, 4) Modifiers, and 5) Functions.

By adhering to the recommended contract ordering, code readability and maintainability can be improved.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```
-	This function `notifyStartGracePeriod`  should come after state variable `CdpIds`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


</details>

# 


## Control structures do not follow the Solidity Style Guide
- Severity: Non-Critical
- Confidence: High

### Description
Control structures should follow the One True Brace [OTB style](https://docs.soliditylang.org/en/latest/style-guide.html#control-structures). This means: 1. Opening braces should be on the same line as the declaration. 
2. Closing braces should be on their own line, at the same indentation level as the beginning of the declaration. 
3. The opening brace should be preceded by a single space.

<details>

<summary>
There are 22 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

328    function _adjustCdpInternal(
329            bytes32 _cdpId,
330            uint256 _stEthBalanceDecrease,
331            uint256 _debtChange,
332            bool _isDebtIncrease,
333            bytes32 _upperHint,
334            bytes32 _lowerHint,
335            uint256 _stEthBalanceIncrease
336        ) internal 
```
 These control structures in the function `_adjustCdpInternal` should follow the One True Brace (OTB) style:

    - Line: 420:         {
    - Line: 426:         {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328-L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328-L437)


#

```
File: contracts/BorrowerOperations.sol

439    function _openCdp(
440            uint256 _debt,
441            bytes32 _upperHint,
442            bytes32 _lowerHint,
443            uint256 _stEthBalance,
444            address _borrower
445        ) internal returns (bytes32) 
```
 These control structures in the function `_openCdp` should follow the One True Brace (OTB) style:

    - Line: 501:             }

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439-L547](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439-L547)


#

```
File: contracts/BorrowerOperations.sol

852    function _requireValidAdjustmentInCurrentMode(
853            bool _isRecoveryMode,
854            uint256 _stEthBalanceDecrease,
855            bool _isDebtIncrease,
856            AdjustCdpLocals memory _vars
857        ) internal 
```
 These control structures in the function `_requireValidAdjustmentInCurrentMode` should follow the One True Brace (OTB) style:

    - Line: 897:             }

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852-L908](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852-L908)


#

```
File: contracts/CdpManager.sol

30    constructor(
31            address _liquidationLibraryAddress,
32            address _authorityAddress,
33            address _borrowerOperationsAddress,
34            address _collSurplusPoolAddress,
35            address _ebtcTokenAddress,
36            address _sortedCdpsAddress,
37            address _activePoolAddress,
38            address _priceFeedAddress,
39            address _collTokenAddress
40        )
41            CdpManagerStorage(
42                _liquidationLibraryAddress,
43                _authorityAddress,
44                _borrowerOperationsAddress,
45                _collSurplusPoolAddress,
46                _ebtcTokenAddress,
47                _sortedCdpsAddress,
48                _activePoolAddress,
49                _priceFeedAddress,
50                _collTokenAddress
51            )
52        
```
 These control structures in the function `constructor` should follow the One True Brace (OTB) style:

    - Line: 52:     {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30-L60)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 These control structures in the function `_redeemCollateralFromCdp` should follow the One True Brace (OTB) style:

    - Line: 162:             {
    - Line: 190:             }

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
 These control structures in the function `redeemCollateral` should follow the One True Brace (OTB) style:

    - Line: 339:         {
    - Line: 392:             {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManagerStorage.sol

344    function _syncAccounting(bytes32 _cdpId) internal 
```
 These control structures in the function `_syncAccounting` should follow the One True Brace (OTB) style:

    - Line: 384:                     {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407)


#

```
File: contracts/Governor.sol

36    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) 
```
 These control structures in the function `constructor` should follow the One True Brace (OTB) style:

    - Line: 36: constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
 These control structures in the function `getRedemptionHints` should follow the One True Brace (OTB) style:

    - Line: 61:     {
    - Line: 63:         {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

41    constructor(
42            address _borrowerOperationsAddress,
43            address _activePool,
44            address _cdpManager,
45            address _ebtc,
46            address _coll,
47            address _sortedCdps
48        )
49            LeverageMacroBase(
50                _borrowerOperationsAddress,
51                _activePool,
52                _cdpManager,
53                _ebtc,
54                _coll,
55                _sortedCdps,
56                false // Do not sweep to caller
57            )
58        
```
 These control structures in the function `constructor` should follow the One True Brace (OTB) style:

    - Line: 58:     {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60)


#

```
File: contracts/LeverageMacroReference.sol

17    constructor(
18            address _borrowerOperationsAddress,
19            address _activePool,
20            address _cdpManager,
21            address _ebtc,
22            address _coll,
23            address _sortedCdps,
24            address _owner
25        )
26            LeverageMacroBase(
27                _borrowerOperationsAddress,
28                _activePool,
29                _cdpManager,
30                _ebtc,
31                _coll,
32                _sortedCdps,
33                true // Sweep to caller since this is not supposed to hold funds
34            )
35        
```
 These control structures in the function `constructor` should follow the One True Brace (OTB) style:

    - Line: 35:     {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17-L42)


#

```
File: contracts/LiquidationLibrary.sol

14    constructor(
15            address _borrowerOperationsAddress,
16            address _collSurplusPool,
17            address _ebtcToken,
18            address _sortedCdps,
19            address _activePool,
20            address _priceFeed,
21            address _collateral
22        )
23            CdpManagerStorage(
24                address(0),
25                address(0),
26                _borrowerOperationsAddress,
27                _collSurplusPool,
28                _ebtcToken,
29                _sortedCdps,
30                _activePool,
31                _priceFeed,
32                _collateral
33            )
34        
```
 These control structures in the function `constructor` should follow the One True Brace (OTB) style:

    - Line: 34:     {}

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34)


#

```
File: contracts/LiquidationLibrary.sol

61    function _liquidateIndividualCdpSetup(
62            bytes32 _cdpId,
63            uint256 _partialAmount,
64            bytes32 _upperPartialHint,
65            bytes32 _lowerPartialHint
66        ) internal 
```
 These control structures in the function `_liquidateIndividualCdpSetup` should follow the One True Brace (OTB) style:

    - Line: 98:         } // Implicit Else Case, Implies ICR < MRC, meaning the CDP is liquidatable

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131)


#

```
File: contracts/LiquidationLibrary.sol

223    function _liquidateIndividualCdpSetupCDPInNormalMode(
224            LiquidationLocals memory _liqState
225        ) private returns (LiquidationLocals memory) 
```
 These control structures in the function `_liquidateIndividualCdpSetupCDPInNormalMode` should follow the One True Brace (OTB) style:

    - Line: 250:         {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293)


#

```
File: contracts/LiquidationLibrary.sol

295    function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296            LiquidationRecoveryModeLocals memory _recoveryState
297        ) private returns (LiquidationRecoveryModeLocals memory) 
```
 These control structures in the function `_liquidateIndividualCdpSetupCDPInRecoveryMode` should follow the One True Brace (OTB) style:

    - Line: 325:         {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379)


#

```
File: contracts/LiquidationLibrary.sol

397    function _liquidateCDPPartially(
398            LiquidationLocals memory _partialState
399        ) private returns (uint256, uint256) 
```
 These control structures in the function `_liquidateCDPPartially` should follow the One True Brace (OTB) style:

    - Line: 428:         {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448)


#

```
File: contracts/PriceFeed.sol

358    function setFallbackCaller(address _fallbackCaller) external requiresAuth 
```
 These control structures in the function `setFallbackCaller` should follow the One True Brace (OTB) style:

    - Line: 380:             } catch {
    - Line: 382:             }

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358-L389](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358-L389)


#

```
File: contracts/PriceFeed.sol

582    function _getCurrentFallbackResponse()
583            internal
584            view
585            returns (FallbackResponse memory fallbackResponse)
586        
```
 These control structures in the function `_getCurrentFallbackResponse` should follow the One True Brace (OTB) style:

    - Line: 586:     {
    - Line: 596:             } catch {
    - Line: 599:         } // If unset we return a zero response with success = false

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602)


#

```
File: contracts/PriceFeed.sol

606    function _getCurrentChainlinkResponse()
607            internal
608            view
609            returns (ChainlinkResponse memory chainlinkResponse)
610        
```
 These control structures in the function `_getCurrentChainlinkResponse` should follow the One True Brace (OTB) style:

    - Line: 610:     {
    - Line: 618:         } catch {
    - Line: 626:         } catch {
    - Line: 645:         } catch {
    - Line: 661:         } catch {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606-L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606-L681)


#

```
File: contracts/PriceFeed.sol

687    function _getPrevChainlinkResponse(
688            uint80 _currentRoundEthBtcId,
689            uint80 _currentRoundStEthEthId
690        ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) 
```
 These control structures in the function `_getPrevChainlinkResponse` should follow the One True Brace (OTB) style:

    - Line: 706:         } catch {
    - Line: 714:         } catch {
    - Line: 733:         } catch {
    - Line: 749:         } catch {

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L769](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L769)


#

```
File: contracts/SimplifiedDiamondLike.sol

134    function _executeOne(Operation calldata op) internal 
```
 These control structures in the function `_executeOne` should follow the One True Brace (OTB) style:

    - Line: 145:             }

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156)


#

```
File: contracts/SortedCdps.sol

456    function _remove(bytes32 _id) internal 
```
 These control structures in the function `_remove` should follow the One True Brace (OTB) style:

    - Line: 480:             }

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491)


</details>

# 


## Costly operations inside a loop
- Severity: Non-Critical
- Confidence: Medium

### Description
Costly operations inside a loop might waste gas, so optimizations are justified.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

539    function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

541    stEthIndex = _newIndex
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L539-L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L539-L544)


#

```
File: contracts/CdpManagerStorage.sol

574    function _takeSplitAndUpdateFeePerUnit(
575            uint256 _feeTaken,
576            uint256 _newPerUnit,
577            uint256 _newErrorPerUnit
578        ) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

581    systemStEthFeePerUnitIndex = _newPerUnit
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588)


#

```
File: contracts/CdpManagerStorage.sol

574    function _takeSplitAndUpdateFeePerUnit(
575            uint256 _feeTaken,
576            uint256 _newPerUnit,
577            uint256 _newErrorPerUnit
578        ) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

582    systemStEthFeePerUnitIndexError = _newErrorPerUnit
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588)


#

```
File: contracts/CdpManagerStorage.sol

293    function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

295    totalStakesSnapshot = _totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301)


#

```
File: contracts/CdpManagerStorage.sol

293    function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

298    totalCollateralSnapshot = _totalCollateralSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301)


#

```
File: contracts/CdpManagerStorage.sol

410    function _removeStake(bytes32 _cdpId) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

412    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415)


#

```
File: contracts/CdpManagerStorage.sol

463    function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

483    CdpIds.pop()
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484)


#

```
File: contracts/CdpManagerStorage.sol

419    function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) 
```
 has costly operations inside a loop:
	- 
```
File: contracts/CdpManagerStorage.sol

423    totalStakes = _newTotalStakes
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L419-L428](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L419-L428)


</details>

# 


## Dead-code
- Severity: Non-Critical
- Confidence: Medium

### Description
Functions that are not sued.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/EBTCToken.sol

306    function _requireCallerIsBorrowerOperations() internal view 
```
 is never used and should be removed

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311)


#

```
File: contracts/EBTCToken.sol

323    function _requireCallerIsCdpM() internal view 
```
 is never used and should be removed

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325)


</details>

# 


## Avoid double casting
- Severity: Non-Critical
- Confidence: High

### Description
This detector identifies instances where values are double casted in Solidity. Double casting can introduce unexpected truncations and/or rounding issues. Additionally, it reduces the readability of the code and can make it harder to maintain. It's recommended to avoid double casting to ensure clearer, safer, and more maintainable smart contracts.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

36    RolesAuthority(_owner, Authority(address(this)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)


#

```
File: contracts/LeverageMacroBase.sol

148    IERC3156FlashLender(address(borrowerOperations)).flashLoan(
149                    IERC3156FlashBorrower(address(this)),
150                    address(ebtcToken),
151                    borrowAmount,
152                    abi.encode(operation)
153                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148-L153)


#

```
File: contracts/LeverageMacroBase.sol

155    IERC3156FlashLender(address(activePool)).flashLoan(
156                    IERC3156FlashBorrower(address(this)),
157                    address(stETH),
158                    borrowAmount,
159                    abi.encode(operation)
160                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160)


#

```
File: contracts/SortedCdps.sol

114    serialized |= bytes32(uint256(uint160(owner))) << ADDRESS_SHIFT
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L114)


#

```
File: contracts/SortedCdps.sol

125    return address(uint160(_tmp))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L125)


</details>

# 


## Duplicated require()/revert() checks should be refactored to a modifier or function
- Severity: Non-Critical
- Confidence: High

### Description
This detector checks for instances where the same require() or revert() condition is repeated in multiple places within the same contract. Such duplicate checks can often be refactored into a modifier or function, reducing code redundancy and increasing maintainability.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

137    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
Has duplicate:<br>
```
File: contracts/ActivePool.sol

162    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
Has duplicate:<br>
```
File: contracts/BorrowerOperations.sol

1155    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/SimplifiedDiamondLike.sol

52    require(msg.sender == owner)
```
Has duplicate:<br>
```
File: contracts/SimplifiedDiamondLike.sol

67    require(msg.sender == owner)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52)


#

```
File: contracts/SortedCdps.sol

458    require(contains(_id), "SortedCdps: List does not contain the id")
```
Has duplicate:<br>
```
File: contracts/SortedCdps.sol

506    require(contains(_id), "SortedCdps: List does not contain the id")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458)


</details>

# 


## Else block not required
- Severity: Non-Critical
- Confidence: High

### Description
This detector identifies unnecessary else blocks in the code. When an if-statement block ends with a return statement, any subsequent else block becomes superfluous and can be eliminated to reduce code complexity. 

Note that this check also applies to single-line else conditions. For instance, in 'return a > b ? a : b', the else condition is not needed.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

315    if (_debtIndexDiff > 0) {
316                pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;
317            } else {
318                return (0, 0);
319            }
```
No nees to declare else block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315-L319](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315-L319)


#

```
File: contracts/HintHelpers.sol

93    if (currentCdpDebt > vars.remainingEbtcToRedeem) {
94                        uint256 _cachedEbtcToRedeem = vars.remainingEbtcToRedeem;
95                        (
96                            partialRedemptionNewColl,
97                            partialRedemptionHintNICR
98                        ) = _calculateCdpStateAfterPartialRedemption(vars, currentCdpDebt, _price);
99    
100                        // If the partial redemption would leave the CDP with less than the minimum allowed coll, bail out of partial redemption and return only the fully redeemable
101                        if (
102                            collateral.getPooledEthByShares(partialRedemptionNewColl) <
103                            MIN_NET_STETH_BALANCE
104                        ) {
105                            partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case
106                            partialRedemptionNewColl = 0;
107                            vars.remainingEbtcToRedeem = _cachedEbtcToRedeem;
108                        } else {
109                            vars.remainingEbtcToRedeem = 0;
110                        }
111                        break;
112                    } else {
113                        vars.remainingEbtcToRedeem = vars.remainingEbtcToRedeem - currentCdpDebt;
114                    }
```
No nees to declare else block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L93-L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L93-L114)


#

```
File: contracts/LeverageMacroBase.sol

245    if (check.operator == Operator.skip) {
246                // Early return
247                return;
248            } else if (check.operator == Operator.gte) {
249                require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");
250            } else if (check.operator == Operator.lte) {
251                require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");
252            } else if (check.operator == Operator.equal) {
253                require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");
254            } else {
255                revert("Operator not found");
256            }
```
No nees to declare else block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L245-L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L245-L256)


#

```
File: contracts/PriceFeed.sol

666    if (
667                _checkHealthyCLResponse(chainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
668                _checkHealthyCLResponse(chainlinkResponse.roundStEthEthId, stEthEthAnswer)
669            ) {
670                chainlinkResponse.answer = _formatClAggregateAnswer(
671                    ethBtcAnswer,
672                    stEthEthAnswer,
673                    ethBtcDecimals,
674                    stEthEthDecimals
675                );
676            } else {
677                return chainlinkResponse;
678            }
```
No nees to declare else block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L666-L678](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L666-L678)


#

```
File: contracts/PriceFeed.sol

754    if (
755                _checkHealthyCLResponse(prevChainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
756                _checkHealthyCLResponse(prevChainlinkResponse.roundStEthEthId, stEthEthAnswer)
757            ) {
758                prevChainlinkResponse.answer = _formatClAggregateAnswer(
759                    ethBtcAnswer,
760                    stEthEthAnswer,
761                    ethBtcDecimals,
762                    stEthEthDecimals
763                );
764            } else {
765                return prevChainlinkResponse;
766            }
```
No nees to declare else block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L754-L766](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L754-L766)


#

```
File: contracts/SortedCdps.sol

189    if (_currentIndex == index) {
190                        return (_currentCdpId, true);
191                    } else {
192                        // if not, increment the owner index as we've seen a CDP owned by them
193                        _currentIndex = _currentIndex + 1;
194                    }
```
No nees to declare else block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L189-L194](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L189-L194)


</details>

# 


## Events should use parameters to convey information
- Severity: Non-Critical
- Confidence: High

### Description
Events in smart contracts are crucial for logging various state changes and significant actions. Utilizing parameters within events provides detailed context about the event, enhancing transparency and ease of debugging. This detector ensures all events declared in a contract use parameters, thereby ensuring better context provision for events logged.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55)


#

```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69)


</details>

# 


## Function Length Too Long
- Severity: Non-Critical
- Confidence: High

### Description
Identifies functions that exceed 50 lines of code. Long functions can be harder to understand and maintain. It is often beneficial to split these into smaller, more manageable functions.

<details>

<summary>
There are 16 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

328    function _adjustCdpInternal(
329            bytes32 _cdpId,
330            uint256 _stEthBalanceDecrease,
331            uint256 _debtChange,
332            bool _isDebtIncrease,
333            bytes32 _upperHint,
334            bytes32 _lowerHint,
335            uint256 _stEthBalanceIncrease
336        ) internal 
```
_adjustCdpInternal has more than 50 lines. Start line 328, end line 437.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328-L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328-L437)


#

```
File: contracts/BorrowerOperations.sol

439    function _openCdp(
440            uint256 _debt,
441            bytes32 _upperHint,
442            bytes32 _lowerHint,
443            uint256 _stEthBalance,
444            address _borrower
445        ) internal returns (bytes32) 
```
_openCdp has more than 50 lines. Start line 439, end line 547.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439-L547](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439-L547)


#

```
File: contracts/BorrowerOperations.sol

852    function _requireValidAdjustmentInCurrentMode(
853            bool _isRecoveryMode,
854            uint256 _stEthBalanceDecrease,
855            bool _isDebtIncrease,
856            AdjustCdpLocals memory _vars
857        ) internal 
```
_requireValidAdjustmentInCurrentMode has more than 50 lines. Start line 852, end line 908.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852-L908](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852-L908)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
_redeemCollateralFromCdp has more than 50 lines. Start line 135, end line 234.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
redeemCollateral has more than 50 lines. Start line 320, end line 485.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManagerStorage.sol

344    function _syncAccounting(bytes32 _cdpId) internal 
```
_syncAccounting has more than 50 lines. Start line 344, end line 407.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```
getRedemptionHints has more than 50 lines. Start line 48, end line 122.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/LeverageMacroBase.sol

118    function doOperation(
119            FlashLoanType flType,
120            uint256 borrowAmount,
121            LeverageMacroOperation calldata operation,
122            PostOperationCheck postCheckType,
123            PostCheckParams calldata checkParams
124        ) external 
```
doOperation has more than 50 lines. Start line 118, end line 211.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L211](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L211)


#

```
File: contracts/LiquidationLibrary.sol

61    function _liquidateIndividualCdpSetup(
62            bytes32 _cdpId,
63            uint256 _partialAmount,
64            bytes32 _upperPartialHint,
65            bytes32 _lowerPartialHint
66        ) internal 
```
_liquidateIndividualCdpSetup has more than 50 lines. Start line 61, end line 131.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131)


#

```
File: contracts/LiquidationLibrary.sol

223    function _liquidateIndividualCdpSetupCDPInNormalMode(
224            LiquidationLocals memory _liqState
225        ) private returns (LiquidationLocals memory) 
```
_liquidateIndividualCdpSetupCDPInNormalMode has more than 50 lines. Start line 223, end line 293.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293)


#

```
File: contracts/LiquidationLibrary.sol

295    function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296            LiquidationRecoveryModeLocals memory _recoveryState
297        ) private returns (LiquidationRecoveryModeLocals memory) 
```
_liquidateIndividualCdpSetupCDPInRecoveryMode has more than 50 lines. Start line 295, end line 379.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379)


#

```
File: contracts/LiquidationLibrary.sol

397    function _liquidateCDPPartially(
398            LiquidationLocals memory _partialState
399        ) private returns (uint256, uint256) 
```
_liquidateCDPPartially has more than 50 lines. Start line 397, end line 448.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448)


#

```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```
_getTotalFromBatchLiquidate_RecoveryMode has more than 50 lines. Start line 733, end line 805.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#

```
File: contracts/PriceFeed.sol

98    function fetchPrice() external override returns (uint256) 
```
fetchPrice has more than 50 lines. Start line 98, end line 352.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98-L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98-L352)


#

```
File: contracts/PriceFeed.sol

606    function _getCurrentChainlinkResponse()
607            internal
608            view
609            returns (ChainlinkResponse memory chainlinkResponse)
610        
```
_getCurrentChainlinkResponse has more than 50 lines. Start line 606, end line 681.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606-L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606-L681)


#

```
File: contracts/PriceFeed.sol

687    function _getPrevChainlinkResponse(
688            uint80 _currentRoundEthBtcId,
689            uint80 _currentRoundStEthEthId
690        ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) 
```
_getPrevChainlinkResponse has more than 50 lines. Start line 687, end line 769.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L769](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L769)


</details>

# 


## Lack of Explicit Visibility Declaration in State Variables
- Severity: Non-Critical
- Confidence: High

### Description
This detector identifies state variables that are missing explicit visibility declarations. By default, without explicit declaration, the visibility of such variables is set to 'internal'. While this does not necessarily lead to vulnerabilities, explicitly declaring the visibility of each state variable can improve code readability and maintainability. Therefore, it is recommended to always specify the visibility, even when it's the default 'internal'.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

128    ICollSurplusPool immutable collSurplusPool
```
State variable lacks explicit visibility.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128)


#

```
File: contracts/Governor.sol

17    bytes32 NO_ROLES = bytes32(0)
```
State variable lacks explicit visibility.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)


#

```
File: contracts/LeverageMacroBase.sol

37    bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan")
```
State variable lacks explicit visibility.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)


#

```
File: contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage")
```
State variable lacks explicit visibility.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)


#

```
File: contracts/SortedCdps.sol

60    uint256 constant ADDRESS_SHIFT = 96
```
State variable lacks explicit visibility.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60)


#

```
File: contracts/SortedCdps.sol

61    uint256 constant BLOCK_SHIFT = 64
```
State variable lacks explicit visibility.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L61)


</details>

# 


## Functions not called by the contract should be declared as external instead of public
- Severity: Non-Critical
- Confidence: High

### Description
Contracts [are allowed](https://docs.soliditylang.org/en/latest/contracts.html#function-overriding) to override their parents' functions and change the visibility from `external` to `public`.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroDelegateTarget.sol

63    function owner() public override returns (address) 
```
should be declared external:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L66)


#

```
File: contracts/LeverageMacroReference.sol

44    function owner() public override returns (address) 
```
should be declared external:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44-L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44-L46)


#

```
File: contracts/SortedCdps.sol

130    function nonExistId() public pure override returns (bytes32) 
```
should be declared external:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130-L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130-L132)


</details>

# 


## Codebase should implement formal verification testing
- Severity: Non-Critical
- Confidence: High

### Description
Formal verification is the act of proving or disproving the correctness of intended algorithms underlying a system with respect to a certain formal specification/property/invariant, using formal methods of mathematics.Some tools that are currently available to perform these tests on smart contracts are [SMTChecker](https://docs.soliditylang.org/en/latest/smtchecker.html) and [Certora Prover](https://www.certora.com/).

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: Various Files
```

</details>

# 


## Contracts should have full test coverage
- Severity: Non-Critical
- Confidence: High

### Description
While 100% code coverage does not guarantee that there are no bugs, it often will catch easy-to-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. In order to get full coverage, code authors will often have to re-organize their code so that it is more modular, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: Various Files
```

</details>

# 


## Function names should differ
- Severity: Non-Critical
- Confidence: High

### Description
In Solidity, while function overriding allows for functions with the same name to coexist, it is advisable to avoid this practice to enhance code readability and maintainability. Having multiple functions with the same name, even with different parameters or in inherited contracts, can cause confusion and increase the likelihood of errors during development, testing, and debugging.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/EBTCToken.sol

104    function burn(uint256 _amount) external 
```
```
/// @audit: function used on lines  95
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104-L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104-L107)


#

```
File: contracts/LeverageMacroFactory.sol

43    function deployNewMacro(address _owner) public returns (address) 
```
```
/// @audit: function used on lines  38
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59)


</details>

# 


## Conformance to Solidity function naming conventions
- Severity: Non-Critical
- Confidence: High

### Description
Solidity defines a [naming convention](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#function-names) that should be followed for function names. According to the convention, function names should be in mixedCase.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#
Function 
```
File: contracts/BorrowerOperations.sol

659    function DOMAIN_SEPARATOR() external view returns (bytes32) 
```
 DOMAIN_SEPARATOR is not in mixedCase

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L659-L661](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L659-L661)


#
Function 
```
File: contracts/EBTCToken.sol

176    function DOMAIN_SEPARATOR() external view returns (bytes32) 
```
 DOMAIN_SEPARATOR is not in mixedCase

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L176-L178](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L176-L178)


#
Function 
```
File: contracts/LeverageMacroBase.sol

15    function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);
```
 Cdps is not in mixedCase

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L15)


#
Function 
```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```
 _getTotalFromBatchLiquidate_RecoveryMode is not in mixedCase

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#
Function 
```
File: contracts/LiquidationLibrary.sol

807    function _getTotalsFromBatchLiquidate_NormalMode(
808            uint256 _price,
809            uint256 _TCR,
810            bytes32[] memory _cdpArray
811        ) internal returns (LiquidationTotals memory totals) 
```
 _getTotalsFromBatchLiquidate_NormalMode is not in mixedCase

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


</details>

# 


## Enum values should be used in place of constant array indexes
- Severity: Non-Critical
- Confidence: High

### Description
It is considered good practice in Solidity to replace constant array indices with enum values. Hardcoded array indices can make the code harder to read and maintain, as they do not provide any context or meaning on their own. By defining an enum with descriptive names for each index, the code becomes more self-explanatory and easier to understand. This detector will identify instances where hardcoded array indices are used, and suggest to replace them with enum values.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

502    require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502)


#

```
File: contracts/SortedCdps.sol

424    bytes32 _firstPrev = data.nodes[_ids[0]].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L424)


</details>

# 


## If-statement can be converted to a ternary
- Severity: Non-Critical
- Confidence: High

### Description
The code can be made more compact while also increasing readability by converting the following `if`-statements to ternaries (e.g. `foo += (x > y) ? a : b`)

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/LiquidationLibrary.sol

698    if (vars.recoveryModeAtStart) {
699                totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                );
705            } else {
706                //  if !vars.recoveryModeAtStart
707                totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray);
708            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L698-L708](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L698-L708)


#

```
File: contracts/SortedCdps.sol

437    if (_firstPrev != dummyId) {
438                data.nodes[_firstPrev].nextId = _lastNext;
439            } else {
440                data.head = _lastNext;
441            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L437-L441](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L437-L441)


#

```
File: contracts/SortedCdps.sol

442    if (_lastNext != dummyId) {
443                data.nodes[_lastNext].prevId = _firstPrev;
444            } else {
445                data.tail = _firstPrev;
446            }
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L442-L446](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L442-L446)


</details>

# 


## Avoid the use of sensitive terms
- Severity: Non-Critical
- Confidence: High

### Description
Use alternative variants, e.g. allowlist/denylist instead of whitelist/blacklist

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```solidity
File contracts/EBTCToken.sol:

// @audit: use `main` instead of `master`
Line 13:  * https://github.com/openzeppelin/openzeppelin-contracts/blob/master/contracts/token/erc20/erc20.sol

```
#

```solidity
File contracts/Governor.sol:

// @audit: use `main` instead of `master`
Line 12: /// @author modified from dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)

```
#

```solidity
File contracts/SortedCdps.sol:

// @audit: use `main` instead of `master`
Line 30:  * https://github.com/livepeer/protocol/blob/master/contracts/libraries/sorteddoublyll.sol

```
</details>

# 


## Inconsistency Spacing in Comments
- Severity: Non-Critical
- Confidence: High

### Description
Consistent and well-formatted comments contribute to code readability and maintainability. The 'InconsistencyCommentSpacing' detector helps enforce a uniform spacing convention within comments, ensuring a standardized and easily understandable commenting style. According to the style guide, it is recommended to add a space after the double forward slash (//) when commenting.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

16    contract CdpManager is CdpManagerStorage, ICdpManager, Proxy 
```

-    `//`
-    `//`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987)


</details>

# 


## Inconsistent Usage of Integer Types
- Severity: Non-Critical
- Confidence: High

### Description
This detector flags contracts that mix usage of int/uint and int256/uint256 types. The preferred type names for function signatures are int256 and uint256, so they should be used consistently.

<details>

<summary>
There are 37 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

830    uint status = cdpManager.getCdpStatus(_cdpId)
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L830)


#

```
File: contracts/BorrowerOperations.sol

834    uint _debtChange
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L834](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L834)


#

```
File: contracts/CdpManagerStorage.sol

357    uint _pendingDebt
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L357](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L357)


#

```
File: contracts/CdpManagerStorage.sol

365    uint prevCollShares = _cdp.coll
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L365)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

28    uint _EBTCAmount
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L28)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

31    uint _collAmount
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L31)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

45    uint _debt
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L45)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

46    uint _collShares
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L46)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

49    uint _premiumToLiquidator
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L49)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

58    uint _premiumToLiquidator
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L58)


#

```
File: contracts/Interfaces/IPositionManagers.sol

36    uint _deadline
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L36)


#

```
File: contracts/Interfaces/ISortedCdps.sol

9    uint _NICR
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9)


#

```
File: contracts/Interfaces/ISortedCdps.sol

66    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L66)


#

```
File: contracts/Interfaces/ISortedCdps.sol

74    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L74)


#

```
File: contracts/Interfaces/ISortedCdps.sol

83    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L83)


#

```
File: contracts/LiquidationLibrary.sol

278    uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L278)


#

```
File: contracts/LiquidationLibrary.sol

279    uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward)
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L279](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L279)


#

```
File: contracts/LiquidationLibrary.sol

365    uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L365)


#

```
File: contracts/LiquidationLibrary.sol

366    uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward)
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L366](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L366)


#

```
File: contracts/LiquidationLibrary.sol

435    uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L435)


#

```
File: contracts/LiquidationLibrary.sol

436    uint _cappedColl = collateral.getPooledEthByShares(_partialColl)
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L436](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L436)


#

```
File: contracts/SortedCdps.sol

159    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L159)


#

```
File: contracts/SortedCdps.sol

177    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L177](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L177)


#

```
File: contracts/SortedCdps.sol

182    uint _currentIndex = 0
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182)


#

```
File: contracts/SortedCdps.sol

183    uint i
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L183](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L183)


#

```
File: contracts/SortedCdps.sol

230    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L230)


#

```
File: contracts/SortedCdps.sol

240    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L240)


#

```
File: contracts/SortedCdps.sol

245    uint _ownedCount = 0
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245)


#

```
File: contracts/SortedCdps.sol

246    uint i = 0
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246)


#

```
File: contracts/SortedCdps.sol

273    uint _ownedCount
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L273](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L273)


#

```
File: contracts/SortedCdps.sol

289    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L289](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L289)


#

```
File: contracts/SortedCdps.sol

293    uint _ownedCount
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L293)


#

```
File: contracts/SortedCdps.sol

302    uint maxNodes
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L302)


#

```
File: contracts/SortedCdps.sol

303    uint maxArraySize
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L303)


#

```
File: contracts/SortedCdps.sol

311    uint i = 0
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311)


#

```
File: contracts/SortedCdps.sol

312    uint _cdpRetrieved
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L312](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L312)


#

```
File: contracts/SortedCdps.sol

449    uint i = 0
```
 should no use `int/uint`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449)


</details>

# 


## Inconsistent usage of require/error
- Severity: Non-Critical
- Confidence: High

### Description
Some parts of the codebase use require statements, while others use custom errors. Consider refactoring the code to use the same approach: the following findings represent the minority of require vs error, and they show one occurrence in each contract, for brevity.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

26    contract LeverageMacroBase 
```

```
File: contracts/LeverageMacroBase.sol

40    revert("Must be overridden")
```
The contract `LeverageMacroBase` uses both `require` and custom `revert` for error handling.

There are 17 `require` statement(s) and 2 custom `revert` statement(s).

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535)


</details>

# 


## Interfaces Should Be Defined in Separate Files From Their Usage
- Severity: Non-Critical
- Confidence: High

### Description
Interfaces should be defined in separate files, so that it's easier for future projects to import them, and to avoid duplication later on if they need to be used elsewhere in the project.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

14    interface ICdpCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8)


</details>

# 


## Invariant Tests
- Severity: Non-Critical
- Confidence: Medium

### Description
Large code bases, or code with lots of inline-assembly, complicated math, or complicated interactions between multiple contracts, should implement invariant fuzzing tests. Even code with 100% code coverage can still have bugs due to the order of the operations a user performs, and invariant fuzzers, with properly and extensively-written invariants, can close this testing gap significantly.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: Various Files 
```

</details>

# 


## Lack of Descriptive Reason Strings in require/revert Statements
- Severity: Non-Critical
- Confidence: High

### Description
By enforcing the use of descriptive reason strings, you can make it easier for developers and users to identify the specific condition or requirement that caused the failure. This can be particularly helpful in cases where contracts are interacting with each other or when external systems are relying on contract behavior.

<details>

<summary>
There are 10 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

452    require(addy != address(borrowerOperations))
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452)


#

```
File: contracts/LeverageMacroBase.sol

453    require(addy != address(sortedCdps))
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453)


#

```
File: contracts/LeverageMacroBase.sol

454    require(addy != address(activePool))
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454)


#

```
File: contracts/LeverageMacroBase.sol

455    require(addy != address(cdpManager))
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455)


#

```
File: contracts/LeverageMacroBase.sol

456    require(addy != address(this))
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456)


#

```
File: contracts/SimplifiedDiamondLike.sol

52    require(msg.sender == owner)
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52)


#

```
File: contracts/SimplifiedDiamondLike.sol

56    require(sig != 0x94b24d09)
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56)


#

```
File: contracts/SimplifiedDiamondLike.sol

67    require(msg.sender == owner)
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67)


#

```
File: contracts/SimplifiedDiamondLike.sol

77    require(msg.sender == address(this))
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77)


#

```
File: contracts/SimplifiedDiamondLike.sol

154    require(success)
```
 add descriptive reason strings 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154)


</details>

# 


## Excessive Line Length in Code
- Severity: Non-Critical
- Confidence: High

### Description
Excessive line lengths can make code harder to read and understand, negatively impacting code maintainability and collaboration. By detecting and highlighting lines that are too long, developers can adhere to coding style guidelines and improve code readability. The threshold for what is considered 'too long' can be customized based on project requirements or coding standards. The solidity style guide recommends a maximum line length of 120 characters. The detector helps promote clean and well-formatted code by identifying and addressing instances where lines exceed the specified length threshold.

<details>

<summary>
There are 10 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

22    contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner 
```
Have those long line:
```Line: 39  /// @dev Initializes the contract with the borrowerOperationsAddress, cdpManagerAddress, collateral token address, collSurplusAddress, and feeRecipientAddress```

```Line: 71  /// @dev Not necessarily equal to the the contract's raw systemCollShares balance - tokens can be forcibly sent to contracts```

```Line: 79  /// @dev The amount of EBTC debt in the pool. Like systemCollShares, this is not necessarily equal to the contract's EBTC token balance - tokens can be forcibly sent to contracts```

```Line: 119  /// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager```

```Line: 121  /// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares```

```Line: 123  /// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.```

```Line: 154  /// @dev If the fee recipient address is changed while outstanding claimable coll is available, only the new fee recipient will be able to claim the outstanding coll```

```Line: 177  /// @notice Helper function to transfer stETH shares to another address, ensuring to call hooks into other system pools if they are the recipient```

```Line: 268  uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused```

```Line: 293  //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert```

```Line: 347  ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423)


#

```
File: contracts/BorrowerOperations.sol

21    contract BorrowerOperations is
22        EbtcBase,
23        ReentrancyGuard,
24        IBorrowerOperations,
25        ERC3156FlashLender,
26        AuthNoOwner,
27        PermitNonce
28    
```
Have those long line:
```Line: 31  // keccak256("permitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)");```

```Line: 34  "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"```

```Line: 64  // Mapping of borrowers to approved position managers, by approval status: cdpOwner(borrower) -> positionManager -> PositionManagerApproval (None, OneTime, Persistent)```

```Line: 140  @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation```

```Line: 141  @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.```

```Line: 160  /// @notice Function that creates a Cdp for the caller with the requested debt, and the stETH received as collateral.```

```Line: 161  /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.```

```Line: 177  /// @notice Function that creates a Cdp for the specified _borrower by caller with the requested debt, and the stETH received as collateral.```

```Line: 179  /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.```

```Line: 214  /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR```

```Line: 228  /// @notice Function that withdraws `_debt` amount of eBTC token from the specified Cdp, thus increasing its debt accounting```

```Line: 230  /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR```

```Line: 267  /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)```

```Line: 296  /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)```

```Line: 392  // When the adjustment is a debt repayment, check it's a valid amount, that the caller has enough EBTC, and that the resulting debt is >0```

```Line: 451  // ICR is based on the net stEth balance, i.e. the specified stEth balance amount - fixed liquidator incentive gas comp.```

```Line: 533  The static liqudiation incentive is stored in the gas pool and can be considered a deposit / voucher to be returned upon Cdp close, to the closer.```

```Line: 537  // CEI: Move the collateral and liquidator gas compensation to the Active Pool. Track only net collateral for TCR purposes.```

```Line: 597  /// @notice when a Cdp has been fully redeemed from and closed, or liquidated in Recovery Mode with a collateralization ratio higher enough (like over MCR)```

```Line: 624  /// @notice Position managers with 'OneTIme' status will be able to take a single action on one Cdp. Approval will be automatically revoked after one Cdp-related action.```

```Line: 625  /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.```

```Line: 627  /// @param _approval PositionManagerApproval (None/OneTime/Persistent) status set to the specified _positionManager for caller's Cdp```

```Line: 645  /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.```

```Line: 782  /// @dev These number of liquidator shares associated with each Cdp are stored in the Cdp, while the actual tokens float in the active pool```

```Line: 977  /// @dev If the PositionManagerApproval was none, we should have failed with the check in _requireBorrowerOrPositionManagerAndUpdateManagerApproval```

```Line: 1084  uint256 fee = flashFee(token, amount); // NOTE: Check for `eBTCToken` is implicit here // NOTE: Pause check is here```

```Line: 1122  /// @param token The address of the token to get the maximum flash loan amount for, exclusively used here for eBTC token```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173)


#

```
File: contracts/CdpManager.sol

16    contract CdpManager is CdpManagerStorage, ICdpManager, Proxy 
```
Have those long line:
```Line: 96  /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).```

```Line: 122  /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.```

```Line: 271  /// @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.```

```Line: 291  /// @notice Note that if _debt is very large, this function can run out of gas, specially if traversed cdps are small (meaning many small Cdps are redeemed against).```

```Line: 292  /// @notice This can be easily avoided by splitting the total _debt in appropriate chunks and calling the function multiple times.```

```Line: 294  b'/// @notice There is a optional parameter `_maxIterations` which can also be provided, so the loop through Cdps is capped (if it\xe2\x80\x99s zero, it will be ignored).'```

```Line: 295  /// @notice This makes it easier to avoid OOG for the frontend, as only knowing approximately the average cost of an iteration is enough,```

```Line: 296  /// @notice without needing to know the "topology" of the cdp list. It also avoids the need to set the cap in stone in the contract,```

```Line: 299  /// @notice All Cdps that are redeemed from -- with the likely exception of the last one -- will end up with no debt left,```

```Line: 301  /// @notice If the last Cdp does have some remaining debt & collateral (it has a valid meaningful ICR) then reinsertion of the CDP```

```Line: 304  /// @notice A frontend should use HintHelper.getRedemptionHints() to calculate what the ICR of this Cdp will be after redemption,```

```Line: 305  /// @notice and pass a hint for its position in the SortedCdps list along with the ICR value that the hint was found for.```

```Line: 311  /// @notice In this case, the redemption will stop after the last completely redeemed Cdp and the sender will keep the```

```Line: 314  /// @param _firstRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getRedemptionHints()```

```Line: 315  /// @param _upperPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)```

```Line: 316  /// @param _lowerPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)```

```Line: 317  /// @param _partialRedemptionHintNICR The new Nominal Collateral Ratio (NICR) of the last redeemed CDP after partial redemption, could get from HintHelper.getRedemptionHints()```

```Line: 515  /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps```

```Line: 579  /// @return TCR The cached total collateralization ratio (TCR) of the system (does not take into account pending global state)```

```Line: 919  cdpStEthFeePerUnitIndex[_cdpId] = systemStEthFeePerUnitIndex; /// @audit We critically assume global accounting is synced here```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987)


#

```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```
Have those long line:
```Line: 27  /// @notice Start the recovery mode grace period, if the system is in RM and the grace period timestamp has not already been set```

```Line: 150  uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme```

```Line: 175  // Snapshot of the total collateral across the ActivePool, immediately after the latest liquidation and split fee claim```

```Line: 197  /* Global Fee accumulator (never decreasing) per stake unit in CDPManager, similar to systemDebtRedistributionIndex */```

```Line: 239  /// @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation```

```Line: 240  /// @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.```

```Line: 303  /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake```

```Line: 613  /// @param _systemStEthFeePerUnitIndex The fee-per-stake-unit value to be used in fee split calculation, could be result of calcFeeUponStakingReward()```

```Line: 683  /// @return The Nominal Collateral Ratio (NICR) of the specified Cdp with fee split and debt redistribution considered.```

```Line: 716  /// @notice Return the pending extra debt assigned to the Cdp from liquidation redistribution, calcualted by Cdp's stake```

```Line: 726  /// @return Whether the debt redistribution tracking index of the specified Cdp is less than the global tracking one (meaning it might get pending debt redistribution)```

```Line: 740  /// @notice Calculate the Cdps entire debt and coll, including pending debt redistributions and collateral reduction from split fee.```

```Line: 781  /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#

```
File: contracts/CollSurplusPool.sol

16    contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner 
```
Have those long line:
```Line: 36  * @dev One-time initialization function. Can only be called by the owner as a security measure. Ownership is renounced after the function is called.```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152)


#

```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```
Have those long line:
```Line: 100  // If the partial redemption would leave the CDP with less than the minimum allowed coll, bail out of partial redemption and return only the fully redeemable```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219)


#

```
File: contracts/LeverageMacroBase.sol

26    contract LeverageMacroBase 
```
Have those long line:
```Line: 233  /// @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)```

```Line: 413  // But technically you could approve w/e you want here, this is fine because the contract is a router and will not hold user funds```

```Line: 426  // val -> 0 -> 0 -> val means this is safe to repeat since even if full approve is unused, we always go back to 0 after```

```Line: 496  /// @dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535)


#

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```
Have those long line:
```Line: 37  /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).```

```Line: 134  // For partial liquidation, caller should use HintHelper smart contract to get correct hints for reinsertion into sorted CDP list```

```Line: 311  // I don't see an issue emitting the CdpUpdated() event up here and avoiding an extra cache of the values, any objections?```

```Line: 675  /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#

```
File: contracts/PriceFeed.sol

21    contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner 
```
Have those long line:
```Line: 31  // Maximum time period allowed since Chainlink's latest round data timestamp, beyond which Chainlink is considered frozen.```

```Line: 96  /// @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.```

```Line: 97  /// @dev The fallback oracle address can be swapped by the Authority. The fallback oracle must conform to the IFallbackCaller interface.```

```Line: 166  * If Fallback is live and both oracles have a similar price, conclude that Chainlink's large price deviation between```

```Line: 173  // If Fallback is live but the oracles differ too much in price, conclude that Chainlink's initial price deviation was```

```Line: 296  // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison```

```Line: 308  // Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price```

```Line: 326  // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price```

```Line: 345  // Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,```

```Line: 394  /// @dev Chainlink is considered broken if its current or previous round data is in any way bad. We check the previous round for two reasons.```

```Line: 396  /// @dev 2. Chainlink is the PriceFeed's preferred primary oracle - having two consecutive valid round responses adds peace of mind when using or returning to Chainlink.```

```Line: 408  /// @dev A response is considered bad if the success value reports failure, or if the timestamp is invalid (0 or in the future)```

```Line: 432  /// @dev The oracle is considered frozen if either of the feed timestamps are older than the threshold specified by the static timeout thresholds```

```Line: 444  /// @return A boolean indicating whether the price change from Chainlink oracle is above the maximum threshold allowed```

```Line: 521  /// @notice Checks if the prices reported by the Chainlink and fallback oracles are similar, within the maximum deviation specified by MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES.```

```Line: 530  // Get the relative price difference between the oracles. Use the lower price as the denominator, i.e. the reference for the calculation.```

```Line: 538  * Return true if the relative price difference is <= MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES: if so, we assume both oracles are probably reporting```

```Line: 579  /// @notice Retrieves the latest response from the fallback oracle. If the fallback oracle address is set to the zero address, it returns a failing struct.```

```Line: 605  /// @return chainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.```

```Line: 686  /// @return prevChainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.```

```Line: 771  /// @notice Returns if the CL feed is healthy or not, based on: negative value and null round id. For price aggregation```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806)


#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```
Have those long line:
```Line: 100  /// @dev Inspired https://github.com/balancer-labs/balancer-v2-monorepo/blob/18bd5fb5d87b451cc27fbd30b276d1fb2987b529/pkg/vault/contracts/PoolRegistry.sol```

```Line: 134  /// @notice Find a specific CDP for a given owner, indexed by it's place in the linked list relative to other Cdps owned by the same address```

```Line: 148  /// @dev a pagination-flavor search (from least ICR to biggest ICR) for CDP owned by given owner and specified index (starting at given CDP)```

```Line: 171  /// @return cdpId The CDP Id if found, otherwise return current lastly-visited CDP as the startNode for next pagination```

```Line: 280  /// @dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)```

```Line: 283  /// @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count```

```Line: 309  // Two-pass strategy, halving the amount of Cdps we can process before relying on pagination or off-chain methods```

```Line: 606  // `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Token contract should have a blacklist function or modifier
- Severity: Non-Critical
- Confidence: Medium

### Description
NFT thefts have increased recently, so with the addition of stolen NFTs to the platform, NFTs can be converted into liquidity. To prevent this, we recommend adding a blacklist function.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/EBTCToken.sol

26    contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce 
```
Token contract does not contain a blacklist. Consider adding one for increased security.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358)


</details>

# 


## Contracts missing NatSpec comments
- Severity: Non-Critical
- Confidence: High

### Description
NatSpec is Ethereum's natural language specification format. It enables developers to provide descriptions for functions, return variables, and more, improving readability and understanding of the contract.

<details>

<summary>
There are 22 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

21    contract BorrowerOperations is
22        EbtcBase,
23        ReentrancyGuard,
24        IBorrowerOperations,
25        ERC3156FlashLender,
26        AuthNoOwner,
27        PermitNonce
28    
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173)


#

```
File: contracts/EBTCToken.sol

26    contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358)


#

```
File: contracts/Interfaces/IActivePool.sol

7    interface IActivePool is IPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L42)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

7    interface IBorrowerOperations is IPositionManagers 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L87)


#

```
File: contracts/Interfaces/ICdpManager.sol

9    interface ICdpManager is IEbtcBase, ICdpManagerData 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L78)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

13    interface ICdpManagerData is IRecoveryModeGracePeriod 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L264)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

5    interface ICollSurplusPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L24)


#

```
File: contracts/Interfaces/IEBTCToken.sol

8    interface IEBTCToken is IERC20, IERC2612 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L14)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

5    interface IERC3156FlashBorrower 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L22)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

7    interface IERC3156FlashLender 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L34)


#

```
File: contracts/Interfaces/IEbtcBase.sol

7    interface IEbtcBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

5    interface IFallbackCaller 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L22)


#

```
File: contracts/Interfaces/IPermitNonce.sol

5    interface IPermitNonce 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L10)


#

```
File: contracts/Interfaces/IPool.sol

6    interface IPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L6-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L6-L22)


#

```
File: contracts/Interfaces/IPositionManagers.sol

5    interface IPositionManagers 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L47)


#

```
File: contracts/Interfaces/IPriceFeed.sol

5    interface IPriceFeed 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L44)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

5    interface IRecoveryModeGracePeriod 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L16)


#

```
File: contracts/Interfaces/ISortedCdps.sol

6    interface ISortedCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L85)


#

```
File: contracts/LeverageMacroBase.sol

14    interface ICdpCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8)


#

```
File: contracts/PriceFeed.sol

21    contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806)


#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Missing events in sensitive functions
- Severity: Non-Critical
- Confidence: High

### Description
Events should be emitted when sensitive changes are made to the contracts, but some functions lack them. 

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

977    function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L977-L979](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L977-L979)


#

```
File: contracts/CdpManager.sol

984    function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L984-L986](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L984-L986)


#

```
File: contracts/CdpManagerStorage.sol

431    function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431-L438](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431-L438)


#

```
File: contracts/CollSurplusPool.sol

130    function increaseTotalSurplusCollShares(uint256 _value) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130-L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130-L133)


</details>

# 


## Missing events arithmetic
- Severity: Non-Critical
- Confidence: Medium

### Description
Detect missing events for critical arithmetic parameters.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CollSurplusPool.sol

130    function increaseTotalSurplusCollShares(uint256 _value) external override 
```
 should emit an event for: 
	- 
```
File: contracts/CollSurplusPool.sol

132    totalSurplusCollShares = totalSurplusCollShares + _value
```
 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130-L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130-L133)


</details>

# 


## Contract Missing NatSpec @author
- Severity: Non-Critical
- Confidence: High

### Description
Some contract definitions have an incomplete NatSpec: add a @author notation to improve the code documentation.

<details>

<summary>
There are 24 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

22    contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423)


#

```
File: contracts/BorrowerOperations.sol

21    contract BorrowerOperations is
22        EbtcBase,
23        ReentrancyGuard,
24        IBorrowerOperations,
25        ERC3156FlashLender,
26        AuthNoOwner,
27        PermitNonce
28    
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173)


#

```
File: contracts/CdpManager.sol

16    contract CdpManager is CdpManagerStorage, ICdpManager, Proxy 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987)


#

```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#

```
File: contracts/CollSurplusPool.sol

16    contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152)


#

```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219)


#

```
File: contracts/Interfaces/IActivePool.sol

7    interface IActivePool is IPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L42)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

5    interface ICollSurplusPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L24)


#

```
File: contracts/Interfaces/IEBTCToken.sol

8    interface IEBTCToken is IERC20, IERC2612 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L14)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

5    interface IERC3156FlashBorrower 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L22)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

7    interface IERC3156FlashLender 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L34)


#

```
File: contracts/Interfaces/IEbtcBase.sol

7    interface IEbtcBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

5    interface IFallbackCaller 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L22)


#

```
File: contracts/Interfaces/IPermitNonce.sol

5    interface IPermitNonce 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L10)


#

```
File: contracts/Interfaces/IPositionManagers.sol

5    interface IPositionManagers 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L47)


#

```
File: contracts/Interfaces/IPriceFeed.sol

5    interface IPriceFeed 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L44)


#

```
File: contracts/LeverageMacroBase.sol

14    interface ICdpCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16)


#

```
File: contracts/LeverageMacroBase.sol

26    contract LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

40    contract LeverageMacroDelegateTarget is LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40-L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40-L67)


#

```
File: contracts/LeverageMacroFactory.sol

11    contract LeverageMacroFactory 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11-L60)


#

```
File: contracts/LeverageMacroReference.sol

11    contract LeverageMacroReference is LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57)


#

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#

```
File: contracts/SimplifiedDiamondLike.sol

25    contract SimplifiedDiamondLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202)


</details>

# 


## Functions missing NatSpec comments
- Severity: Non-Critical
- Confidence: High

### Description
NatSpec is Ethereum's natural language specification format. It enables developers to provide descriptions for functions, return variables, and more, improving readability and understanding of the contract.

<details>

<summary>
There are 308 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

129    function transferSystemCollSharesAndLiquidatorReward(
130            address _account,
131            uint256 _shares,
132            uint256 _liquidatorRewardShares
133        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L129-L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L129-L149)


#

```
File: contracts/ActivePool.sol

261    function flashLoan(
262            IERC3156FlashBorrower receiver,
263            address token,
264            uint256 amount,
265            bytes calldata data
266        ) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310)


#

```
File: contracts/ActivePool.sol

22    contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423)


#

```
File: contracts/BorrowerOperations.sol

168    function openCdp(
169            uint256 _debt,
170            bytes32 _upperHint,
171            bytes32 _lowerHint,
172            uint256 _stEthBalance
173        ) external override nonReentrantSelfAndCdpM returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L168-L175](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L168-L175)


#

```
File: contracts/BorrowerOperations.sol

187    function openCdpFor(
188            uint256 _debt,
189            bytes32 _upperHint,
190            bytes32 _lowerHint,
191            uint256 _stEthBalance,
192            address _borrower
193        ) external override nonReentrantSelfAndCdpM returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187-L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187-L195)


#

```
File: contracts/BorrowerOperations.sol

203    function addColl(
204            bytes32 _cdpId,
205            bytes32 _upperHint,
206            bytes32 _lowerHint,
207            uint256 _stEthBalanceIncrease
208        ) external override nonReentrantSelfAndCdpM 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L203-L210](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L203-L210)


#

```
File: contracts/BorrowerOperations.sol

219    function withdrawColl(
220            bytes32 _cdpId,
221            uint256 _stEthBalanceDecrease,
222            bytes32 _upperHint,
223            bytes32 _lowerHint
224        ) external override nonReentrantSelfAndCdpM 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L219-L226](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L219-L226)


#

```
File: contracts/BorrowerOperations.sol

235    function withdrawDebt(
236            bytes32 _cdpId,
237            uint256 _debt,
238            bytes32 _upperHint,
239            bytes32 _lowerHint
240        ) external override nonReentrantSelfAndCdpM 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L235-L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L235-L242)


#

```
File: contracts/BorrowerOperations.sol

250    function repayDebt(
251            bytes32 _cdpId,
252            uint256 _debt,
253            bytes32 _upperHint,
254            bytes32 _lowerHint
255        ) external override nonReentrantSelfAndCdpM 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L250-L257](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L250-L257)


#

```
File: contracts/BorrowerOperations.sol

270    function adjustCdp(
271            bytes32 _cdpId,
272            uint256 _stEthBalanceDecrease,
273            uint256 _debtChange,
274            bool _isDebtIncrease,
275            bytes32 _upperHint,
276            bytes32 _lowerHint
277        ) external override nonReentrantSelfAndCdpM 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L270-L287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L270-L287)


#

```
File: contracts/BorrowerOperations.sol

300    function adjustCdpWithColl(
301            bytes32 _cdpId,
302            uint256 _stEthBalanceDecrease,
303            uint256 _debtChange,
304            bool _isDebtIncrease,
305            bytes32 _upperHint,
306            bytes32 _lowerHint,
307            uint256 _stEthBalanceIncrease
308        ) external override nonReentrantSelfAndCdpM 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L300-L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L300-L318)


#

```
File: contracts/BorrowerOperations.sol

328    function _adjustCdpInternal(
329            bytes32 _cdpId,
330            uint256 _stEthBalanceDecrease,
331            uint256 _debtChange,
332            bool _isDebtIncrease,
333            bytes32 _upperHint,
334            bytes32 _lowerHint,
335            uint256 _stEthBalanceIncrease
336        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328-L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L328-L437)


#

```
File: contracts/BorrowerOperations.sol

439    function _openCdp(
440            uint256 _debt,
441            bytes32 _upperHint,
442            bytes32 _lowerHint,
443            uint256 _stEthBalance,
444            address _borrower
445        ) internal returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439-L547](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439-L547)


#

```
File: contracts/BorrowerOperations.sol

608    function getPositionManagerApproval(
609            address _borrower,
610            address _positionManager
611        ) external view override returns (PositionManagerApproval) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L608-L613](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L608-L613)


#

```
File: contracts/BorrowerOperations.sol

615    function _getPositionManagerApproval(
616            address _borrower,
617            address _positionManager
618        ) internal view returns (PositionManagerApproval) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L615-L620](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L615-L620)


#

```
File: contracts/BorrowerOperations.sol

628    function setPositionManagerApproval(
629            address _positionManager,
630            PositionManagerApproval _approval
631        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L628-L633](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L628-L633)


#

```
File: contracts/BorrowerOperations.sol

635    function _setPositionManagerApproval(
636            address _borrower,
637            address _positionManager,
638            PositionManagerApproval _approval
639        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L635-L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L635-L642)


#

```
File: contracts/BorrowerOperations.sol

673    function _chainID() private view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L673-L675](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L673-L675)


#

```
File: contracts/BorrowerOperations.sol

677    function _buildDomainSeparator(
678            bytes32 typeHash,
679            bytes32 name,
680            bytes32 version
681        ) private view returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L677-L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L677-L683)


#

```
File: contracts/BorrowerOperations.sol

706    function permitPositionManagerApproval(
707            address _borrower,
708            address _positionManager,
709            PositionManagerApproval _approval,
710            uint256 _deadline,
711            uint8 v,
712            bytes32 r,
713            bytes32 s
714        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L706-L740](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L706-L740)


#

```
File: contracts/BorrowerOperations.sol

744    function _getCollSharesChangeFromStEthChange(
745            uint256 _collReceived,
746            uint256 _requestedCollWithdrawal
747        ) internal view returns (uint256 collSharesChange, bool isCollIncrease) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744-L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744-L754)


#

```
File: contracts/BorrowerOperations.sol

796    function _repayDebt(address _account, uint256 _debt) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L796-L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L796-L799)


#

```
File: contracts/BorrowerOperations.sol

803    function _requireSingularCollChange(
804            uint256 _stEthBalanceIncrease,
805            uint256 _stEthBalanceDecrease
806        ) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L803-L811](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L803-L811)


#

```
File: contracts/BorrowerOperations.sol

813    function _requireNonZeroAdjustment(
814            uint256 _stEthBalanceIncrease,
815            uint256 _debtChange,
816            uint256 _stEthBalanceDecrease
817        ) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L813-L822](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L813-L822)


#

```
File: contracts/BorrowerOperations.sol

824    function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L824-L827](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L824-L827)


#

```
File: contracts/BorrowerOperations.sol

829    function _requireCdpIsNonExistent(bytes32 _cdpId) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L829-L832](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L829-L832)


#

```
File: contracts/BorrowerOperations.sol

834    function _requireNonZeroDebtChange(uint _debtChange) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L834-L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L834-L836)


#

```
File: contracts/BorrowerOperations.sol

838    function _requireNotInRecoveryMode(uint256 _tcr) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L838-L843](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L838-L843)


#

```
File: contracts/BorrowerOperations.sol

845    function _requireNoStEthBalanceDecrease(uint256 _stEthBalanceDecrease) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845-L850](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845-L850)


#

```
File: contracts/BorrowerOperations.sol

852    function _requireValidAdjustmentInCurrentMode(
853            bool _isRecoveryMode,
854            uint256 _stEthBalanceDecrease,
855            bool _isDebtIncrease,
856            AdjustCdpLocals memory _vars
857        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852-L908](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852-L908)


#

```
File: contracts/BorrowerOperations.sol

910    function _requireICRisNotBelowMCR(uint256 _newICR) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L910-L915](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L910-L915)


#

```
File: contracts/BorrowerOperations.sol

917    function _requireICRisNotBelowCCR(uint256 _newICR) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L917-L919](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L917-L919)


#

```
File: contracts/BorrowerOperations.sol

921    function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L921-L926](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L921-L926)


#

```
File: contracts/BorrowerOperations.sol

928    function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L928-L933](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L928-L933)


#

```
File: contracts/BorrowerOperations.sol

935    function _requireNonZeroDebt(uint256 _debt) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L935-L937](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L935-L937)


#

```
File: contracts/BorrowerOperations.sol

939    function _requireAtLeastMinNetStEthBalance(uint256 _stEthBalance) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L939-L944](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L939-L944)


#

```
File: contracts/BorrowerOperations.sol

946    function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L946-L951](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L946-L951)


#

```
File: contracts/BorrowerOperations.sol

953    function _requireSufficientEbtcTokenBalance(
954            address _account,
955            uint256 _debtRepayment
956        ) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L953-L961](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L953-L961)


#

```
File: contracts/BorrowerOperations.sol

963    function _requireBorrowerOrPositionManagerAndUpdateManagerApproval(address _borrower) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L963-L981](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L963-L981)


#

```
File: contracts/BorrowerOperations.sol

986    function _getNewNominalICRFromCdpChange(
987            AdjustCdpLocals memory vars,
988            bool _isDebtIncrease
989        ) internal pure returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986-L1001](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986-L1001)


#

```
File: contracts/BorrowerOperations.sol

1004    function _getNewICRFromCdpChange(
1005            uint256 _collShares,
1006            uint256 _debt,
1007            uint256 _collSharesChange,
1008            bool _isCollIncrease,
1009            uint256 _debtChange,
1010            bool _isDebtIncrease,
1011            uint256 _price
1012        ) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1004-L1028](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1004-L1028)


#

```
File: contracts/BorrowerOperations.sol

1030    function _getNewCdpAmounts(
1031            uint256 _collShares,
1032            uint256 _debt,
1033            uint256 _collSharesChange,
1034            bool _isCollIncrease,
1035            uint256 _debtChange,
1036            bool _isDebtIncrease
1037        ) internal pure returns (uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1030-L1047](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1030-L1047)


#

```
File: contracts/BorrowerOperations.sol

1049    function _getNewTCRFromCdpChange(
1050            uint256 _stEthBalanceChange,
1051            bool _isCollIncrease,
1052            uint256 _debtChange,
1053            bool _isDebtIncrease,
1054            uint256 _price
1055        ) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1049-L1067](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1049-L1067)


#

```
File: contracts/BorrowerOperations.sol

1077    function flashLoan(
1078            IERC3156FlashBorrower receiver,
1079            address token,
1080            uint256 amount,
1081            bytes calldata data
1082        ) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108)


#

```
File: contracts/BorrowerOperations.sol

21    contract BorrowerOperations is
22        EbtcBase,
23        ReentrancyGuard,
24        IBorrowerOperations,
25        ERC3156FlashLender,
26        AuthNoOwner,
27        PermitNonce
28    
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173)


#

```
File: contracts/CdpManager.sol

109    function partiallyLiquidate(
110            bytes32 _cdpId,
111            uint256 _partialAmount,
112            bytes32 _upperPartialHint,
113            bytes32 _lowerPartialHint
114        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L109-L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L109-L116)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

244    function _closeCdpByRedemption(
245            bytes32 _cdpId,
246            uint256 _EBTC,
247            uint256 _collSurplus,
248            uint256 _liquidatorRewardShares,
249            address _borrower
250        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244-L265)


#

```
File: contracts/CdpManager.sol

272    function _isValidFirstRedemptionHint(
273            bytes32 _firstRedemptionHint,
274            uint256 _price
275        ) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L272-L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L272-L286)


#

```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#

```
File: contracts/CdpManager.sol

489    function _getCdpIdsToRemove(
490            bytes32 _start,
491            uint256 _total,
492            bytes32 _end
493        ) internal view returns (bytes32[] memory) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L489-L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L489-L508)


#

```
File: contracts/CdpManager.sol

538    function closeCdp(
539            bytes32 _cdpId,
540            address _borrower,
541            uint256 _debt,
542            uint256 _coll
543        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L538-L547](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L538-L547)


#

```
File: contracts/CdpManager.sol

550    function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563)


#

```
File: contracts/CdpManager.sol

595    function _checkPotentialRecoveryMode(
596            uint256 _systemCollShares,
597            uint256 _systemDebt,
598            uint256 _price
599        ) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L595-L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L595-L602)


#

```
File: contracts/CdpManager.sol

612    function _updateBaseRateFromRedemption(
613            uint256 _ETHDrawn,
614            uint256 _price,
615            uint256 _totalEBTCSupply
616        ) internal returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L612-L635](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L612-L635)


#

```
File: contracts/CdpManager.sol

647    function _calcRedemptionRate(uint256 _baseRate) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L647-L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L647-L653)


#

```
File: contracts/CdpManager.sol

655    function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L655-L657](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L655-L657)


#

```
File: contracts/CdpManager.sol

661    function getRedemptionFeeWithDecay(
662            uint256 _stETHToRedeem
663        ) external view override returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L661-L665](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L661-L665)


#

```
File: contracts/CdpManager.sol

667    function _calcRedemptionFee(
668            uint256 _redemptionRate,
669            uint256 _ETHDrawn
670        ) internal pure returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L667-L674](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L667-L674)


#

```
File: contracts/CdpManager.sol

676    function _decayBaseRate() internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L676-L684](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L676-L684)


#

```
File: contracts/CdpManager.sol

689    function _updateLastRedemptionTimestamp() internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689-L700](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689-L700)


#

```
File: contracts/CdpManager.sol

702    function _calcDecayedBaseRate() internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L702-L707](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L702-L707)


#

```
File: contracts/CdpManager.sol

709    function _minutesPassedSinceLastRedemption() internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709-L714](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709-L714)


#

```
File: contracts/CdpManager.sol

727    function checkPotentialRecoveryMode(
728            uint256 _systemCollShares,
729            uint256 _systemDebt,
730            uint256 _price
731        ) external view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L727-L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L727-L733)


#

```
File: contracts/CdpManager.sol

737    function _requireEbtcBalanceCoversRedemptionAndWithinSupply(
738            address _redeemer,
739            uint256 _amount,
740            uint256 _totalSupply
741        ) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L737-L751](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L737-L751)


#

```
File: contracts/CdpManager.sol

753    function _requireAmountGreaterThanZero(uint256 _amount) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L753-L755](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L753-L755)


#

```
File: contracts/CdpManager.sol

757    function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757-L759](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757-L759)


#

```
File: contracts/CdpManager.sol

761    function _requireValidMaxFeePercentage(uint256 _maxFeePercentage) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L761-L766](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L761-L766)


#

```
File: contracts/CdpManager.sol

905    function initializeCdp(
906            bytes32 _cdpId,
907            uint256 _debt,
908            uint256 _coll,
909            uint256 _liquidatorRewardShares,
910            address _borrower
911        ) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L936)


#

```
File: contracts/CdpManager.sol

946    function updateCdp(
947            bytes32 _cdpId,
948            address _borrower,
949            uint256 _coll,
950            uint256 _debt,
951            uint256 _newColl,
952            uint256 _newDebt
953        ) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946-L972](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946-L972)


#

```
File: contracts/CdpManager.sol

16    contract CdpManager is CdpManagerStorage, ICdpManager, Proxy 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987)


#

```
File: contracts/CdpManagerStorage.sol

73    function _syncGracePeriod() internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73-L83)


#

```
File: contracts/CdpManagerStorage.sol

87    function _syncGracePeriodForGivenValues(
88            uint256 systemCollShares,
89            uint256 systemDebt,
90            uint256 price
91        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L87-L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L87-L106)


#

```
File: contracts/CdpManagerStorage.sol

255    function _closeCdp(bytes32 _cdpId, Status closedStatus) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L255-L258](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L255-L258)


#

```
File: contracts/CdpManagerStorage.sol

260    function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280)


#

```
File: contracts/CdpManagerStorage.sol

293    function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293-L301)


#

```
File: contracts/CdpManagerStorage.sol

304    function _getPendingRedistributedDebt(
305            bytes32 _cdpId
306        ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L304-L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L304-L320)


#

```
File: contracts/CdpManagerStorage.sol

327    function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L327-L333](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L327-L333)


#

```
File: contracts/CdpManagerStorage.sol

410    function _removeStake(bytes32 _cdpId) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415)


#

```
File: contracts/CdpManagerStorage.sol

419    function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L419-L428](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L419-L428)


#

```
File: contracts/CdpManagerStorage.sol

431    function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431-L438](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431-L438)


#

```
File: contracts/CdpManagerStorage.sol

441    function _computeNewStake(uint256 _coll) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441-L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441-L457)


#

```
File: contracts/CdpManagerStorage.sol

463    function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484)


#

```
File: contracts/CdpManagerStorage.sol

489    function _computeTCRWithGivenSystemValues(
490            uint256 _systemCollShares,
491            uint256 _systemDebt,
492            uint256 _price
493        ) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L489-L496](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L489-L496)


#

```
File: contracts/CdpManagerStorage.sol

509    function _syncGlobalAccounting() internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521)


#

```
File: contracts/CdpManagerStorage.sol

539    function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L539-L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L539-L544)


#

```
File: contracts/CdpManagerStorage.sol

552    function calcFeeUponStakingReward(
553            uint256 _newIndex,
554            uint256 _prevIndex
555        ) public view returns (uint256, uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552-L570)


#

```
File: contracts/CdpManagerStorage.sol

574    function _takeSplitAndUpdateFeePerUnit(
575            uint256 _feeTaken,
576            uint256 _newPerUnit,
577            uint256 _newErrorPerUnit
578        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588)


#

```
File: contracts/CdpManagerStorage.sol

592    function _applyAccumulatedFeeSplit(
593            bytes32 _cdpId,
594            uint256 _newColl,
595            uint256 _feeSplitDistributed,
596            uint256 _oldPerUnitCdp,
597            uint256 _systemStEthFeePerUnitIndex
598        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L592-L609](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L592-L609)


#

```
File: contracts/CdpManagerStorage.sol

616    function getAccumulatedFeeSplitApplied(
617            bytes32 _cdpId,
618            uint256 _systemStEthFeePerUnitIndex
619        ) public view returns (uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616-L645](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616-L645)


#

```
File: contracts/CdpManagerStorage.sol

648    function _requireCdpIsActive(bytes32 _cdpId) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648-L650](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648-L650)


#

```
File: contracts/CdpManagerStorage.sol

652    function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652-L657](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652-L657)


#

```
File: contracts/CdpManagerStorage.sol

659    function _requireCallerIsBorrowerOperations() internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L659-L664](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L659-L664)


#

```
File: contracts/CdpManagerStorage.sol

707    function _calculateCR(
708            uint256 currentCollShare,
709            uint256 currentDebt,
710            uint256 _price
711        ) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L707-L714](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L707-L714)


#

```
File: contracts/CdpManagerStorage.sol

719    function getPendingRedistributedDebt(
720            bytes32 _cdpId
721        ) public view returns (uint256 pendingEBTCDebtReward) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719-L724](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719-L724)


#

```
File: contracts/CdpManagerStorage.sol

733    function _getSyncedDebtAndCollShares(
734            bytes32 _cdpId
735        ) internal view returns (CdpDebtAndCollShares memory) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733-L738](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733-L738)


#

```
File: contracts/CdpManagerStorage.sol

745    function getSyncedDebtAndCollShares(
746            bytes32 _cdpId
747        ) public view returns (uint256 debt, uint256 coll) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L745-L755](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L745-L755)


#

```
File: contracts/CdpManagerStorage.sol

761    function _calcSyncedGlobalAccounting(
762            uint256 _newIndex,
763            uint256 _oldIndex
764        ) internal view returns (uint256, uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761-L779](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761-L779)


#

```
File: contracts/CdpManagerStorage.sol

787    function _calcSyncedAccounting(
788            bytes32 _cdpId,
789            uint256 _cdpPerUnitIdx,
790            uint256 _systemStEthFeePerUnitIndex
791        ) internal view returns (uint256, uint256, uint256, uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L787-L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L787-L819)


#

```
File: contracts/CdpManagerStorage.sol

822    function _getSyncedCdpDebtAndRedistribution(
823            bytes32 _cdpId
824        ) internal view returns (uint256, uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L822-L833](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L822-L833)


#

```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#

```
File: contracts/CollSurplusPool.sol

112    function _requireCallerIsBorrowerOperations() internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112-L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112-L117)


#

```
File: contracts/CollSurplusPool.sol

119    function _requireCallerIsCdpManager() internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L119-L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L119-L121)


#

```
File: contracts/CollSurplusPool.sol

123    function _requireCallerIsActivePool() internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L123-L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L123-L125)


#

```
File: contracts/CollSurplusPool.sol

16    contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152)


#

```
File: contracts/EBTCToken.sol

111    function totalSupply() external view override returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L111-L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L111-L113)


#

```
File: contracts/EBTCToken.sol

115    function balanceOf(address account) external view override returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L115-L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L115-L117)


#

```
File: contracts/EBTCToken.sol

119    function transfer(address recipient, uint256 amount) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L119-L123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L119-L123)


#

```
File: contracts/EBTCToken.sol

125    function allowance(address owner, address spender) external view override returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L125-L127](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L125-L127)


#

```
File: contracts/EBTCToken.sol

129    function approve(address spender, uint256 amount) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L129-L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L129-L132)


#

```
File: contracts/EBTCToken.sol

134    function transferFrom(
135            address sender,
136            address recipient,
137            uint256 amount
138        ) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L134-L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L134-L150)


#

```
File: contracts/EBTCToken.sol

152    function increaseAllowance(
153            address spender,
154            uint256 addedValue
155        ) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L152-L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L152-L158)


#

```
File: contracts/EBTCToken.sol

160    function decreaseAllowance(
161            address spender,
162            uint256 subtractedValue
163        ) external override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L160-L170](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L160-L170)


#

```
File: contracts/EBTCToken.sol

199    function permit(
200            address owner,
201            address spender,
202            uint256 amount,
203            uint256 deadline,
204            uint8 v,
205            bytes32 r,
206            bytes32 s
207        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L199-L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L199-L221)


#

```
File: contracts/EBTCToken.sol

231    function _chainID() private view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L231-L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L231-L233)


#

```
File: contracts/EBTCToken.sol

235    function _buildDomainSeparator(
236            bytes32 typeHash,
237            bytes32 name,
238            bytes32 version
239        ) private view returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L235-L241](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L235-L241)


#

```
File: contracts/EBTCToken.sol

246    function _transfer(address sender, address recipient, uint256 amount) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260)


#

```
File: contracts/EBTCToken.sol

262    function _mint(address account, uint256 amount) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L262-L268](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L262-L268)


#

```
File: contracts/EBTCToken.sol

270    function _burn(address account, uint256 amount) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L270-L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L270-L283)


#

```
File: contracts/EBTCToken.sol

285    function _approve(address owner, address spender, uint256 amount) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L285-L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L285-L291)


#

```
File: contracts/EBTCToken.sol

295    function _requireValidRecipient(address _recipient) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L295-L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L295-L304)


#

```
File: contracts/EBTCToken.sol

306    function _requireCallerIsBorrowerOperations() internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311)


#

```
File: contracts/EBTCToken.sol

323    function _requireCallerIsCdpM() internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325)


#

```
File: contracts/EBTCToken.sol

26    contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358)


#

```
File: contracts/Governor.sol

131    function getEnabledFunctionsInTarget(
132            address _target
133        ) public view returns (bytes4[] memory _funcs) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131-L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131-L141)


#

```
File: contracts/Governor.sol

13    contract Governor is RolesAuthority 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13-L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13-L159)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

133    function _calculateCdpStateAfterPartialRedemption(
134            LocalVariables_getRedemptionHints memory vars,
135            uint256 currentCdpDebt,
136            uint256 _price
137        ) internal view returns (uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153)


#

```
File: contracts/HintHelpers.sol

164    function getApproxHint(
165            uint256 _CR,
166            uint256 _numTrials,
167            uint256 _inputRandomSeed
168        ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197)


#

```
File: contracts/HintHelpers.sol

212    function computeCR(
213            uint256 _coll,
214            uint256 _debt,
215            uint256 _price
216        ) external pure returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L212-L218](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L212-L218)


#

```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219)


#

```
File: contracts/Interfaces/IActivePool.sol

23    function transferSystemCollShares(address _account, uint256 _amount) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L23)


#

```
File: contracts/Interfaces/IActivePool.sol

25    function increaseSystemCollShares(uint256 _value) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L25)


#

```
File: contracts/Interfaces/IActivePool.sol

27    function transferSystemCollSharesAndLiquidatorReward(
28            address _account,
29            uint256 _shares,
30            uint256 _liquidatorRewardShares
31        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L27-L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L27-L31)


#

```
File: contracts/Interfaces/IActivePool.sol

33    function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L33)


#

```
File: contracts/Interfaces/IActivePool.sol

35    function claimFeeRecipientCollShares(uint256 _shares) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L35)


#

```
File: contracts/Interfaces/IActivePool.sol

37    function feeRecipientAddress() external view returns (address);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L37)


#

```
File: contracts/Interfaces/IActivePool.sol

39    function getFeeRecipientClaimableCollShares() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L39)


#

```
File: contracts/Interfaces/IActivePool.sol

41    function setFeeRecipientAddress(address _feeRecipientAddress) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L41)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

20    function openCdp(
21            uint256 _EBTCAmount,
22            bytes32 _upperHint,
23            bytes32 _lowerHint,
24            uint256 _stEthBalance
25        ) external returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L20-L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L20-L25)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

27    function openCdpFor(
28            uint _EBTCAmount,
29            bytes32 _upperHint,
30            bytes32 _lowerHint,
31            uint _collAmount,
32            address _borrower
33        ) external returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27-L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L27-L33)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

35    function addColl(
36            bytes32 _cdpId,
37            bytes32 _upperHint,
38            bytes32 _lowerHint,
39            uint256 _stEthBalanceIncrease
40        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L35-L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L35-L40)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

42    function withdrawColl(
43            bytes32 _cdpId,
44            uint256 _stEthBalanceDecrease,
45            bytes32 _upperHint,
46            bytes32 _lowerHint
47        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L42-L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L42-L47)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

49    function withdrawDebt(
50            bytes32 _cdpId,
51            uint256 _amount,
52            bytes32 _upperHint,
53            bytes32 _lowerHint
54        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L49-L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L49-L54)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

56    function repayDebt(
57            bytes32 _cdpId,
58            uint256 _amount,
59            bytes32 _upperHint,
60            bytes32 _lowerHint
61        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L56-L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L56-L61)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

63    function closeCdp(bytes32 _cdpId) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L63)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

65    function adjustCdp(
66            bytes32 _cdpId,
67            uint256 _stEthBalanceDecrease,
68            uint256 _debtChange,
69            bool isDebtIncrease,
70            bytes32 _upperHint,
71            bytes32 _lowerHint
72        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L65-L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L65-L72)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

74    function adjustCdpWithColl(
75            bytes32 _cdpId,
76            uint256 _stEthBalanceDecrease,
77            uint256 _debtChange,
78            bool isDebtIncrease,
79            bytes32 _upperHint,
80            bytes32 _lowerHint,
81            uint256 _stEthBalanceIncrease
82        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L74-L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L74-L82)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

84    function claimSurplusCollShares() external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L84)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

86    function feeRecipientAddress() external view returns (address);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L86](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L86)


#

```
File: contracts/Interfaces/ICdpManager.sol

11    function getActiveCdpsCount() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L11)


#

```
File: contracts/Interfaces/ICdpManager.sol

13    function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L13)


#

```
File: contracts/Interfaces/ICdpManager.sol

15    function liquidate(bytes32 _cdpId) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L15)


#

```
File: contracts/Interfaces/ICdpManager.sol

17    function partiallyLiquidate(
18            bytes32 _cdpId,
19            uint256 _partialAmount,
20            bytes32 _upperPartialHint,
21            bytes32 _lowerPartialHint
22        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L17-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L17-L22)


#

```
File: contracts/Interfaces/ICdpManager.sol

24    function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L24)


#

```
File: contracts/Interfaces/ICdpManager.sol

26    function redeemCollateral(
27            uint256 _EBTCAmount,
28            bytes32 _firstRedemptionHint,
29            bytes32 _upperPartialRedemptionHint,
30            bytes32 _lowerPartialRedemptionHint,
31            uint256 _partialRedemptionHintNICR,
32            uint256 _maxIterations,
33            uint256 _maxFee
34        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L26-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L26-L34)


#

```
File: contracts/Interfaces/ICdpManager.sol

36    function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L36)


#

```
File: contracts/Interfaces/ICdpManager.sol

38    function syncAccounting(bytes32 _cdpId) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L38)


#

```
File: contracts/Interfaces/ICdpManager.sol

40    function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L40)


#

```
File: contracts/Interfaces/ICdpManager.sol

42    function getRedemptionRate() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L42)


#

```
File: contracts/Interfaces/ICdpManager.sol

44    function getRedemptionRateWithDecay() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L44)


#

```
File: contracts/Interfaces/ICdpManager.sol

46    function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L46)


#

```
File: contracts/Interfaces/ICdpManager.sol

48    function getCdpStatus(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L48)


#

```
File: contracts/Interfaces/ICdpManager.sol

50    function getCdpStake(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L50)


#

```
File: contracts/Interfaces/ICdpManager.sol

52    function getCdpDebt(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L52)


#

```
File: contracts/Interfaces/ICdpManager.sol

54    function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L54)


#

```
File: contracts/Interfaces/ICdpManager.sol

56    function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L56)


#

```
File: contracts/Interfaces/ICdpManager.sol

58    function initializeCdp(
59            bytes32 _cdpId,
60            uint256 _debt,
61            uint256 _coll,
62            uint256 _liquidatorRewardShares,
63            address _borrower
64        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L58-L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L58-L64)


#

```
File: contracts/Interfaces/ICdpManager.sol

66    function updateCdp(
67            bytes32 _cdpId,
68            address _borrower,
69            uint256 _coll,
70            uint256 _debt,
71            uint256 _newColl,
72            uint256 _newDebt
73        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L66-L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L66-L73)


#

```
File: contracts/Interfaces/ICdpManager.sol

75    function getCachedTCR(uint256 _price) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L75)


#

```
File: contracts/Interfaces/ICdpManager.sol

77    function checkRecoveryMode(uint256 _price) external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L77)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

217    function totalStakes() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L217)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

219    function ebtcToken() external view returns (IEBTCToken);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L219)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

221    function systemStEthFeePerUnitIndex() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L221)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

223    function systemStEthFeePerUnitIndexError() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L223)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

225    function stEthIndex() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L225](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L225)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

227    function calcFeeUponStakingReward(
228            uint256 _newIndex,
229            uint256 _prevIndex
230        ) external view returns (uint256, uint256, uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L227-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L227-L230)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

232    function syncGlobalAccounting() external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L232](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L232)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

234    function syncGlobalAccountingAndGracePeriod() external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L234)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

236    function getAccumulatedFeeSplitApplied(
237            bytes32 _cdpId,
238            uint256 _systemStEthFeePerUnitIndex
239        ) external view returns (uint256, uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L236-L239](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L236-L239)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

241    function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L241](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L241)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

243    function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L243](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L243)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

245    function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L245](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L245)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

247    function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L247)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

249    function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L249)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

251    function getSyncedTCR(uint256 _price) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L251)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

253    function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L253)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

255    function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L255)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

257    function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L257](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L257)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

259    function getSyncedDebtAndCollShares(
260            bytes32 _cdpId
261        ) external view returns (uint256 debt, uint256 collShares);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259-L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259-L261)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

263    function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L263)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

15    function getTotalSurplusCollShares() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L15)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

17    function getSurplusCollShares(address _account) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L17)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

19    function increaseSurplusCollShares(address _account, uint256 _amount) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L19)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

21    function claimSurplusCollShares(address _account) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L21)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

23    function increaseTotalSurplusCollShares(uint256 _value) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L23)


#

```
File: contracts/Interfaces/IEBTCToken.sol

11    function mint(address _account, uint256 _amount) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L11)


#

```
File: contracts/Interfaces/IEBTCToken.sol

13    function burn(address _account, uint256 _amount) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L13)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

15    function onFlashLoan(
16            address initiator,
17            address token,
18            uint256 amount,
19            uint256 fee,
20            bytes calldata data
21        ) external returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L15-L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L15-L21)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

28    function flashLoan(
29            IERC3156FlashBorrower receiver,
30            address token,
31            uint256 amount,
32            bytes calldata data
33        ) external returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28-L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28-L33)


#

```
File: contracts/Interfaces/IEbtcBase.sol

8    function priceFeed() external view returns (IPriceFeed);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L8)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

13    function getFallbackResponse() external view returns (uint256, uint256, bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L13)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

17    function fallbackTimeout() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L17)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

21    function setFallbackTimeout(uint256 newFallbackTimeout) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L21)


#

```
File: contracts/Interfaces/IPermitNonce.sol

7    function increasePermitNonce() external returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L7)


#

```
File: contracts/Interfaces/IPermitNonce.sol

9    function nonces(address owner) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L9)


#

```
File: contracts/Interfaces/IPool.sol

15    function getSystemCollShares() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L15)


#

```
File: contracts/Interfaces/IPool.sol

17    function getSystemDebt() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L17)


#

```
File: contracts/Interfaces/IPool.sol

19    function increaseSystemDebt(uint256 _amount) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L19)


#

```
File: contracts/Interfaces/IPool.sol

21    function decreaseSystemDebt(uint256 _amount) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L21)


#

```
File: contracts/Interfaces/IPositionManagers.sol

18    function getPositionManagerApproval(
19            address _borrower,
20            address _positionManager
21        ) external view returns (PositionManagerApproval);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L18-L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L18-L21)


#

```
File: contracts/Interfaces/IPositionManagers.sol

23    function setPositionManagerApproval(
24            address _positionManager,
25            PositionManagerApproval _approval
26        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L23-L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L23-L26)


#

```
File: contracts/Interfaces/IPositionManagers.sol

28    function revokePositionManagerApproval(address _positionManager) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L28)


#

```
File: contracts/Interfaces/IPositionManagers.sol

30    function renouncePositionManagerApproval(address _borrower) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L30)


#

```
File: contracts/Interfaces/IPositionManagers.sol

32    function permitPositionManagerApproval(
33            address _borrower,
34            address _positionManager,
35            PositionManagerApproval _approval,
36            uint _deadline,
37            uint8 v,
38            bytes32 r,
39            bytes32 s
40        ) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32-L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L32-L40)


#

```
File: contracts/Interfaces/IPositionManagers.sol

42    function version() external view returns (string memory);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L42)


#

```
File: contracts/Interfaces/IPositionManagers.sol

44    function permitTypeHash() external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L44)


#

```
File: contracts/Interfaces/IPositionManagers.sol

46    function domainSeparator() external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L46)


#

```
File: contracts/Interfaces/IPriceFeed.sol

43    function fetchPrice() external returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L43)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

13    function notifyStartGracePeriod(uint256 tcr) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L13)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

15    function notifyEndGracePeriod(uint256 tcr) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L15)


#

```
File: contracts/Interfaces/ISortedCdps.sol

14    function remove(bytes32 _id) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L14)


#

```
File: contracts/Interfaces/ISortedCdps.sol

16    function batchRemove(bytes32[] memory _ids) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16)


#

```
File: contracts/Interfaces/ISortedCdps.sol

18    function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L18)


#

```
File: contracts/Interfaces/ISortedCdps.sol

20    function contains(bytes32 _id) external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L20)


#

```
File: contracts/Interfaces/ISortedCdps.sol

22    function isFull() external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L22)


#

```
File: contracts/Interfaces/ISortedCdps.sol

24    function isEmpty() external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L24)


#

```
File: contracts/Interfaces/ISortedCdps.sol

26    function getSize() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L26)


#

```
File: contracts/Interfaces/ISortedCdps.sol

28    function getMaxSize() external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L28)


#

```
File: contracts/Interfaces/ISortedCdps.sol

30    function getFirst() external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L30)


#

```
File: contracts/Interfaces/ISortedCdps.sol

32    function getLast() external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L32)


#

```
File: contracts/Interfaces/ISortedCdps.sol

34    function getNext(bytes32 _id) external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L34)


#

```
File: contracts/Interfaces/ISortedCdps.sol

36    function getPrev(bytes32 _id) external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L36)


#

```
File: contracts/Interfaces/ISortedCdps.sol

38    function validInsertPosition(
39            uint256 _ICR,
40            bytes32 _prevId,
41            bytes32 _nextId
42        ) external view returns (bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L38-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L38-L42)


#

```
File: contracts/Interfaces/ISortedCdps.sol

44    function findInsertPosition(
45            uint256 _ICR,
46            bytes32 _prevId,
47            bytes32 _nextId
48        ) external view returns (bytes32, bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L44-L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L44-L48)


#

```
File: contracts/Interfaces/ISortedCdps.sol

50    function insert(
51            address owner,
52            uint256 _ICR,
53            bytes32 _prevId,
54            bytes32 _nextId
55        ) external returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L50-L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L50-L55)


#

```
File: contracts/Interfaces/ISortedCdps.sol

57    function getOwnerAddress(bytes32 _id) external pure returns (address);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L57)


#

```
File: contracts/Interfaces/ISortedCdps.sol

59    function nonExistId() external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L59)


#

```
File: contracts/Interfaces/ISortedCdps.sol

61    function cdpCountOf(address owner) external view returns (uint256);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L61)


#

```
File: contracts/Interfaces/ISortedCdps.sol

63    function getCdpCountOf(
64            address owner,
65            bytes32 startNodeId,
66            uint maxNodes
67        ) external view returns (uint256, bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63-L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L63-L67)


#

```
File: contracts/Interfaces/ISortedCdps.sol

69    function getCdpsOf(address owner) external view returns (bytes32[] memory);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L69)


#

```
File: contracts/Interfaces/ISortedCdps.sol

71    function getAllCdpsOf(
72            address owner,
73            bytes32 startNodeId,
74            uint maxNodes
75        ) external view returns (bytes32[] memory, uint256, bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71-L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L71-L75)


#

```
File: contracts/Interfaces/ISortedCdps.sol

77    function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L77)


#

```
File: contracts/Interfaces/ISortedCdps.sol

79    function cdpOfOwnerByIdx(
80            address owner,
81            uint256 index,
82            bytes32 startNodeId,
83            uint maxNodes
84        ) external view returns (bytes32, bool);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79-L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L79-L84)


#

```
File: contracts/LeverageMacroBase.sol

15    function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L15)


#

```
File: contracts/LeverageMacroBase.sol

39    function owner() public virtual returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L39-L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L39-L41)


#

```
File: contracts/LeverageMacroBase.sol

43    function _assertOwner() internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L43-L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L43-L46)


#

```
File: contracts/LeverageMacroBase.sol

118    function doOperation(
119            FlashLoanType flType,
120            uint256 borrowAmount,
121            LeverageMacroOperation calldata operation,
122            PostOperationCheck postCheckType,
123            PostCheckParams calldata checkParams
124        ) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L211](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L211)


#

```
File: contracts/LeverageMacroBase.sol

344    function onFlashLoan(
345            address initiator,
346            address token,
347            uint256 amount,
348            uint256 fee,
349            bytes calldata data
350        ) external returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L344-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L344-L379)


#

```
File: contracts/LeverageMacroBase.sol

498    function excessivelySafeCall(
499            address _target,
500            uint256 _gas,
501            uint256 _value,
502            uint16 _maxCopy,
503            bytes memory _calldata
504        ) internal returns (bool, bytes memory) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498-L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498-L534)


#

```
File: contracts/LeverageMacroBase.sol

26    contract LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

7    function owner() external view returns (address);
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L7)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

40    contract LeverageMacroDelegateTarget is LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40-L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40-L67)


#

```
File: contracts/LeverageMacroReference.sol

44    function owner() public override returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44-L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44-L46)


#

```
File: contracts/LeverageMacroReference.sol

11    contract LeverageMacroReference is LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57)


#

```
File: contracts/LiquidationLibrary.sol

50    function partiallyLiquidate(
51            bytes32 _cdpId,
52            uint256 _partialAmount,
53            bytes32 _upperPartialHint,
54            bytes32 _lowerPartialHint
55        ) external nonReentrantSelfAndBOps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L50-L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L50-L58)


#

```
File: contracts/LiquidationLibrary.sol

61    function _liquidateIndividualCdpSetup(
62            bytes32 _cdpId,
63            uint256 _partialAmount,
64            bytes32 _upperPartialHint,
65            bytes32 _lowerPartialHint
66        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131)


#

```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#

```
File: contracts/LiquidationLibrary.sol

186    function _liquidateCdpInGivenMode(
187            LiquidationLocals memory _liqState,
188            LiquidationRecoveryModeLocals memory _recoveryState
189        ) private returns (uint256, uint256, uint256, uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186-L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186-L221)


#

```
File: contracts/LiquidationLibrary.sol

223    function _liquidateIndividualCdpSetupCDPInNormalMode(
224            LiquidationLocals memory _liqState
225        ) private returns (LiquidationLocals memory) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293)


#

```
File: contracts/LiquidationLibrary.sol

295    function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296            LiquidationRecoveryModeLocals memory _recoveryState
297        ) private returns (LiquidationRecoveryModeLocals memory) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379)


#

```
File: contracts/LiquidationLibrary.sol

384    function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L384-L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L384-L393)


#

```
File: contracts/LiquidationLibrary.sol

397    function _liquidateCDPPartially(
398            LiquidationLocals memory _partialState
399        ) private returns (uint256, uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448)


#

```
File: contracts/LiquidationLibrary.sol

450    function _partiallyReduceCdpDebt(
451            bytes32 _cdpId,
452            uint256 _partialDebt,
453            uint256 _partialColl
454        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450-L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450-L463)


#

```
File: contracts/LiquidationLibrary.sol

466    function _reInsertPartialLiquidation(
467            LiquidationLocals memory _partialState,
468            uint256 _newNICR,
469            uint256 _oldDebt,
470            uint256 _oldColl
471        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501)


#

```
File: contracts/LiquidationLibrary.sol

503    function _finalizeLiquidation(
504            uint256 totalDebtToBurn,
505            uint256 totalCollSharesToSend,
506            uint256 totalDebtToRedistribute,
507            uint256 totalLiquidatorRewardCollShares,
508            uint256 totalSurplusCollShares,
509            uint256 systemInitialCollShares,
510            uint256 systemInitialDebt,
511            uint256 price
512        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L503-L541](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L503-L541)


#

```
File: contracts/LiquidationLibrary.sol

544    function _calculatePartialLiquidationSurplusAndCap(
545            uint256 _ICR,
546            uint256 _price,
547            uint256 _totalDebtToBurn,
548            uint256 _totalColToSend
549        ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568)


#

```
File: contracts/LiquidationLibrary.sol

570    function _calculateFullLiquidationSurplusAndCap(
571            uint256 _ICR,
572            uint256 _price,
573            uint256 _totalDebtToBurn,
574            uint256 _totalColToSend
575        ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L570-L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L570-L604)


#

```
File: contracts/LiquidationLibrary.sol

608    function _getLiquidationValuesNormalMode(
609            uint256 _price,
610            uint256 _TCR,
611            LocalVariables_LiquidationSequence memory vars,
612            LiquidationValues memory singleLiquidation
613        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L608-L640](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L608-L640)


#

```
File: contracts/LiquidationLibrary.sol

642    function _getLiquidationValuesRecoveryMode(
643            uint256 _price,
644            uint256 _systemDebt,
645            uint256 _systemCollShares,
646            LocalVariables_LiquidationSequence memory vars,
647            LiquidationValues memory singleLiquidation
648        ) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642-L671](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642-L671)


#

```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#

```
File: contracts/LiquidationLibrary.sol

807    function _getTotalsFromBatchLiquidate_NormalMode(
808            uint256 _price,
809            uint256 _TCR,
810            bytes32[] memory _cdpArray
811        ) internal returns (LiquidationTotals memory totals) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


#

```
File: contracts/LiquidationLibrary.sol

839    function _addLiquidationValuesToTotals(
840            LiquidationTotals memory oldTotals,
841            LiquidationValues memory singleLiquidation
842        ) internal pure returns (LiquidationTotals memory newTotals) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839-L860](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839-L860)


#

```
File: contracts/LiquidationLibrary.sol

862    function _redistributeDebt(uint256 _debt) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892)


#

```
File: contracts/LiquidationLibrary.sol

896    function _requirePartialLiqDebtSize(
897            uint256 _partialDebt,
898            uint256 _entireDebt,
899            uint256 _price
900        ) internal view 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906)


#

```
File: contracts/LiquidationLibrary.sol

908    function _requirePartialLiqCollSize(uint256 _entireColl) internal pure 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908-L913](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908-L913)


#

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#

```
File: contracts/PriceFeed.sol

400    function _chainlinkIsBroken(
401            ChainlinkResponse memory _currentResponse,
402            ChainlinkResponse memory _prevResponse
403        ) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L400-L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L400-L405)


#

```
File: contracts/PriceFeed.sol

445    function _chainlinkPriceChangeAboveMax(
446            ChainlinkResponse memory _currentResponse,
447            ChainlinkResponse memory _prevResponse
448        ) internal pure returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L445-L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L445-L463)


#

```
File: contracts/PriceFeed.sol

465    function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465-L480](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465-L480)


#

```
File: contracts/PriceFeed.sol

485    function _fallbackIsFrozen(
486            FallbackResponse memory _fallbackResponse
487        ) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L485-L491](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L485-L491)


#

```
File: contracts/PriceFeed.sol

493    function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L493-L495](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L493-L495)


#

```
File: contracts/PriceFeed.sol

503    function _bothOraclesLiveAndUnbrokenAndSimilarPrice(
504            ChainlinkResponse memory _chainlinkResponse,
505            ChainlinkResponse memory _prevChainlinkResponse,
506            FallbackResponse memory _fallbackResponse
507        ) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L503-L519](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L503-L519)


#

```
File: contracts/PriceFeed.sol

526    function _bothOraclesSimilarPrice(
527            ChainlinkResponse memory _chainlinkResponse,
528            FallbackResponse memory _fallbackResponse
529        ) internal pure returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L526-L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L526-L542)


#

```
File: contracts/PriceFeed.sol

561    function _storeFallbackPrice(
562            FallbackResponse memory _fallbackResponse
563        ) internal returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L561-L566](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L561-L566)


#

```
File: contracts/PriceFeed.sol

582    function _getCurrentFallbackResponse()
583            internal
584            view
585            returns (FallbackResponse memory fallbackResponse)
586        
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602)


#

```
File: contracts/PriceFeed.sol

606    function _getCurrentChainlinkResponse()
607            internal
608            view
609            returns (ChainlinkResponse memory chainlinkResponse)
610        
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606-L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606-L681)


#

```
File: contracts/PriceFeed.sol

687    function _getPrevChainlinkResponse(
688            uint80 _currentRoundEthBtcId,
689            uint80 _currentRoundStEthEthId
690        ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L769](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687-L769)


#

```
File: contracts/PriceFeed.sol

788    function _formatClAggregateAnswer(
789            int256 _ethBtcAnswer,
790            int256 _stEthEthAnswer,
791            uint8 _ethBtcDecimals,
792            uint8 _stEthEthDecimals
793        ) internal view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L788-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L788-L805)


#

```
File: contracts/PriceFeed.sol

21    contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806)


#

```
File: contracts/SimplifiedDiamondLike.sol

25    contract SimplifiedDiamondLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202)


#

```
File: contracts/SortedCdps.sol

105    function toCdpId(
106            address owner,
107            uint256 blockHeight,
108            uint256 nonce
109        ) public pure returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L105-L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L105-L117)


#

```
File: contracts/SortedCdps.sol

140    function cdpOfOwnerByIndex(
141            address owner,
142            uint256 index
143        ) external view override returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L140-L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L140-L146)


#

```
File: contracts/SortedCdps.sol

155    function cdpOfOwnerByIdx(
156            address owner,
157            uint256 index,
158            bytes32 startNodeId,
159            uint maxNodes
160        ) external view override returns (bytes32, bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155-L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155-L162)


#

```
File: contracts/SortedCdps.sol

173    function _cdpOfOwnerByIndex(
174            address owner,
175            uint256 index,
176            bytes32 startNodeId,
177            uint maxNodes
178        ) internal view returns (bytes32, bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173-L210](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173-L210)


#

```
File: contracts/SortedCdps.sol

227    function getCdpCountOf(
228            address owner,
229            bytes32 startNodeId,
230            uint maxNodes
231        ) external view override returns (uint256, bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227-L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227-L233)


#

```
File: contracts/SortedCdps.sol

237    function _cdpCountOf(
238            address owner,
239            bytes32 startNodeId,
240            uint maxNodes
241        ) internal view returns (uint256, bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237-L264)


#

```
File: contracts/SortedCdps.sol

286    function getAllCdpsOf(
287            address owner,
288            bytes32 startNodeId,
289            uint maxNodes
290        ) external view override returns (bytes32[] memory, uint256, bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286-L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286-L295)


#

```
File: contracts/SortedCdps.sol

299    function _getCdpsOf(
300            address owner,
301            bytes32 startNodeId,
302            uint maxNodes,
303            uint maxArraySize
304        ) internal view returns (bytes32[] memory, uint256, bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L299-L336](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L299-L336)


#

```
File: contracts/SortedCdps.sol

344    function insert(
345            address owner,
346            uint256 _NICR,
347            bytes32 _prevId,
348            bytes32 _nextId
349        ) external override returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L361](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L361)


#

```
File: contracts/SortedCdps.sol

363    function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406)


#

```
File: contracts/SortedCdps.sol

456    function _remove(bytes32 _id) internal 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491)


#

```
File: contracts/SortedCdps.sol

498    function reInsert(
499            bytes32 _id,
500            uint256 _newNICR,
501            bytes32 _prevId,
502            bytes32 _nextId
503        ) external override 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L498-L514](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L498-L514)


#

```
File: contracts/SortedCdps.sol

583    function validInsertPosition(
584            uint256 _NICR,
585            bytes32 _prevId,
586            bytes32 _nextId
587        ) external view override returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L583-L589](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L583-L589)


#

```
File: contracts/SortedCdps.sol

591    function _validInsertPosition(
592            uint256 _NICR,
593            bytes32 _prevId,
594            bytes32 _nextId
595        ) internal view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591-L612](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591-L612)


#

```
File: contracts/SortedCdps.sol

666    function findInsertPosition(
667            uint256 _NICR,
668            bytes32 _prevId,
669            bytes32 _nextId
670        ) external view override returns (bytes32, bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L666-L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L666-L672)


#

```
File: contracts/SortedCdps.sol

674    function _findInsertPosition(
675            uint256 _NICR,
676            bytes32 _prevId,
677            bytes32 _nextId
678        ) internal view returns (bytes32, bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L674-L709](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L674-L709)


#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Missing function parameter in NatSpec comments
- Severity: Non-Critical
- Confidence: High

### Description
NatSpec comments should include all function parameters to improve the clarity and understanding of the contract.

<details>

<summary>
There are 22 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

760    function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal 
```
Missing the following  parameters: <br> `_varMvTokens`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760-L776](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760-L776)


#

```
File: contracts/BorrowerOperations.sol

790    function _withdrawDebt(address _account, uint256 _debt) internal 
```
Missing the following  parameters: <br> `_account``_debt`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L790-L793](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L790-L793)


#

```
File: contracts/CdpManagerStorage.sol

49    function _startGracePeriod(uint256 _tcr) internal 
```
Missing the following  parameters: <br> `_tcr`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L49-L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L49-L57)


#

```
File: contracts/CdpManagerStorage.sol

63    function _endGracePeriod(uint256 _tcr) internal 
```
Missing the following  parameters: <br> `_tcr`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L63-L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L63-L71)


#

```
File: contracts/CdpManagerStorage.sol

336    function _updateRedistributedDebtIndex(bytes32 _cdpId) internal 
```
Missing the following  parameters: <br> `_cdpId`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L336-L341](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L336-L341)


#

```
File: contracts/CdpManagerStorage.sol

344    function _syncAccounting(bytes32 _cdpId) internal 
```
Missing the following  parameters: <br> `_cdpId`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407)


#

```
File: contracts/CdpManagerStorage.sol

701    function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) 
```
Missing the following  parameters: <br> `_price`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L701-L705](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L701-L705)


#

```
File: contracts/LeverageMacroBase.sol

234    function sweepToken(address token, uint256 amount) public 
```
Missing the following  parameters: <br> `amount`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234-L238](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234-L238)


#

```
File: contracts/LeverageMacroBase.sol

244    function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal 
```
Missing the following  parameters: <br> `check``valueToCheck`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244-L257](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244-L257)


#

```
File: contracts/LeverageMacroBase.sol

291    function _handleOperation(LeverageMacroOperation memory operation) internal 
```
Missing the following  parameters: <br> `operation`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291-L310)


#

```
File: contracts/LeverageMacroBase.sol

382    function _doSwaps(SwapOperation[] memory swapData) internal 
```
Missing the following  parameters: <br> `swapData`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382-L391](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382-L391)


#

```
File: contracts/LeverageMacroBase.sol

398    function _doSwap(SwapOperation memory swapData) internal 
```
Missing the following  parameters: <br> `swapData`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398-L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398-L431)


#

```
File: contracts/LeverageMacroBase.sol

435    function _doSwapChecks(SwapCheck[] memory swapChecks) internal 
```
Missing the following  parameters: <br> `swapChecks`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435-L447](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435-L447)


#

```
File: contracts/LeverageMacroBase.sol

450    function _ensureNotSystem(address addy) internal 
```
Missing the following  parameters: <br> `addy`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L450-L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L450-L457)


#

```
File: contracts/LeverageMacroBase.sol

460    function _openCdpCallback(bytes memory data) internal 
```
Missing the following  parameters: <br> `data`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L460-L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L460-L471)


#

```
File: contracts/LeverageMacroBase.sol

474    function _closeCdpCallback(bytes memory data) internal 
```
Missing the following  parameters: <br> `data`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L474-L479](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L474-L479)


#

```
File: contracts/LeverageMacroBase.sol

482    function _adjustCdpCallback(bytes memory data) internal 
```
Missing the following  parameters: <br> `data`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L482-L494](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L482-L494)


#

```
File: contracts/LeverageMacroFactory.sol

43    function deployNewMacro(address _owner) public returns (address) 
```
Missing the following  parameters: <br> `_owner`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59)


#

```
File: contracts/SimplifiedDiamondLike.sol

66    function setAllowAnyCall(bool allowNonCallbacks) external 
```
Missing the following  parameters: <br> `allowNonCallbacks`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L71)


#

```
File: contracts/SimplifiedDiamondLike.sol

110    function execute(Operation[] calldata ops) external payable 
```
Missing the following  parameters: <br> `ops`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126)


#

```
File: contracts/SimplifiedDiamondLike.sol

129    function _setCallbackEnabledForCall(DiamondLikeStorage storage ds, bool _enabled) internal 
```
Missing the following  parameters: <br> `ds``_enabled`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L129-L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L129-L131)


#

```
File: contracts/SimplifiedDiamondLike.sol

134    function _executeOne(Operation calldata op) internal 
```
Missing the following  parameters: <br> `op`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156)


</details>

# 


## Missing function return values in NatSpec comments
- Severity: Non-Critical
- Confidence: High

### Description
NatSpec comments should include all function return values to improve the clarity and understanding of the contract.

<details>

<summary>
There are 7 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

523    function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L523-L526](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L523-L526)


#

```
File: contracts/CdpManagerStorage.sol

895    function _recoveryModeGracePeriodPassed() internal view returns (bool) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L895-L901](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L895-L901)


#

```
File: contracts/LeverageMacroBase.sol

338    function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L338-L341](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L338-L341)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

63    function owner() public override returns (address) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L66)


#

```
File: contracts/LeverageMacroFactory.sol

38    function deployNewMacro() external returns (address) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38-L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38-L40)


#

```
File: contracts/LeverageMacroFactory.sol

43    function deployNewMacro(address _owner) public returns (address) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59)


#

```
File: contracts/SimplifiedDiamondLike.sol

83    function _getStorage() internal pure returns (DiamondLikeStorage storage ds) 
```
Missing return values
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L83-L88](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L83-L88)


</details>

# 


## Contract Missing NatSpec @title
- Severity: Non-Critical
- Confidence: High

### Description
Some contract definitions have an incomplete NatSpec: add a @title notation to improve the code documentation.

<details>

<summary>
There are 15 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

21    contract BorrowerOperations is
22        EbtcBase,
23        ReentrancyGuard,
24        IBorrowerOperations,
25        ERC3156FlashLender,
26        AuthNoOwner,
27        PermitNonce
28    
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173)


#

```
File: contracts/CollSurplusPool.sol

16    contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152)


#

```
File: contracts/Governor.sol

13    contract Governor is RolesAuthority 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13-L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13-L159)


#

```
File: contracts/Interfaces/IActivePool.sol

7    interface IActivePool is IPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L42)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

5    interface ICollSurplusPool 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L24)


#

```
File: contracts/Interfaces/IEBTCToken.sol

8    interface IEBTCToken is IERC20, IERC2612 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L14)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

5    interface IERC3156FlashBorrower 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L22)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

7    interface IERC3156FlashLender 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L34)


#

```
File: contracts/Interfaces/IEbtcBase.sol

7    interface IEbtcBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L9)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

5    interface IFallbackCaller 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L22)


#

```
File: contracts/Interfaces/IPermitNonce.sol

5    interface IPermitNonce 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L10)


#

```
File: contracts/Interfaces/IPositionManagers.sol

5    interface IPositionManagers 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L47)


#

```
File: contracts/Interfaces/IPriceFeed.sol

5    interface IPriceFeed 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L44)


#

```
File: contracts/LeverageMacroBase.sol

14    interface ICdpCdps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8)


</details>

# 


## Public variable declarations should have NatSpec descriptions
- Severity: Non-Critical
- Confidence: High

### Description
NatSpec provides documentation for public state variables, improving code readability and understanding.

<details>

<summary>
There are 57 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

24    string public constant NAME = "ActivePool"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)


#

```
File: contracts/ActivePool.sol

26    address public immutable borrowerOperationsAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L26)


#

```
File: contracts/ActivePool.sol

27    address public immutable cdpManagerAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L27)


#

```
File: contracts/ActivePool.sol

28    address public immutable collSurplusPoolAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L28)


#

```
File: contracts/ActivePool.sol

29    address public feeRecipientAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L29)


#

```
File: contracts/ActivePool.sol

34    ICollateralToken public immutable collateral
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L34)


#

```
File: contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)


#

```
File: contracts/BorrowerOperations.sol

55    ICollSurplusPool public immutable collSurplusPool
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L55)


#

```
File: contracts/BorrowerOperations.sol

57    address public feeRecipientAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L57)


#

```
File: contracts/BorrowerOperations.sol

59    IEBTCToken public immutable ebtcToken
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L59)


#

```
File: contracts/CdpManagerStorage.sol

22    uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22)


#

```
File: contracts/CdpManagerStorage.sol

24    uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24)


#

```
File: contracts/CdpManagerStorage.sol

25    uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25)


#

```
File: contracts/CdpManagerStorage.sol

122    string public constant NAME = "CdpManager"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122)


#

```
File: contracts/CdpManagerStorage.sol

130    IEBTCToken public immutable override ebtcToken
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L130)


#

```
File: contracts/CdpManagerStorage.sol

132    address public immutable liquidationLibrary
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L132)


#

```
File: contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)


#

```
File: contracts/CdpManagerStorage.sol

142    uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142)


#

```
File: contracts/CdpManagerStorage.sol

143    bool public redemptionsPaused
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)


#

```
File: contracts/CdpManagerStorage.sol

149    uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149)


#

```
File: contracts/CdpManagerStorage.sol

150    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)


#

```
File: contracts/CdpManagerStorage.sol

161    uint256 public baseRate
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161)


#

```
File: contracts/CdpManagerStorage.sol

163    uint256 public stakingRewardSplit
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163)


#

```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168)


#

```
File: contracts/CdpManagerStorage.sol

170    uint256 public override totalStakes
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L170](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L170)


#

```
File: contracts/CollSurplusPool.sol

19    string public constant NAME = "CollSurplusPool"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)


#

```
File: contracts/CollSurplusPool.sol

21    address public immutable borrowerOperationsAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L21)


#

```
File: contracts/CollSurplusPool.sol

22    address public immutable cdpManagerAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L22)


#

```
File: contracts/CollSurplusPool.sol

23    address public immutable activePoolAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L23)


#

```
File: contracts/CollSurplusPool.sol

24    address public immutable feeRecipientAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L24)


#

```
File: contracts/CollSurplusPool.sol

25    ICollateralToken public immutable collateral
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L25)


#

```
File: contracts/EBTCToken.sol

56    address public immutable borrowerOperationsAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L56)


#

```
File: contracts/HintHelpers.sol

12    string public constant NAME = "HintHelpers"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)


#

```
File: contracts/HintHelpers.sol

14    ISortedCdps public immutable sortedCdps
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L14)


#

```
File: contracts/HintHelpers.sol

15    ICdpManager public immutable cdpManager
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L15)


#

```
File: contracts/LeverageMacroBase.sol

29    IBorrowerOperations public immutable borrowerOperations
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L29)


#

```
File: contracts/LeverageMacroBase.sol

30    IActivePool public immutable activePool
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L30)


#

```
File: contracts/LeverageMacroBase.sol

31    ICdpCdps public immutable cdpManager
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L31)


#

```
File: contracts/LeverageMacroBase.sol

32    IEBTCToken public immutable ebtcToken
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L32)


#

```
File: contracts/LeverageMacroBase.sol

33    ISortedCdps public immutable sortedCdps
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L33)


#

```
File: contracts/LeverageMacroBase.sol

34    ICollateralToken public immutable stETH
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L34)


#

```
File: contracts/LeverageMacroFactory.sol

12    address public immutable borrowerOperations
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12)


#

```
File: contracts/LeverageMacroFactory.sol

13    address public immutable activePool
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L13)


#

```
File: contracts/LeverageMacroFactory.sol

14    address public immutable cdpManager
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L14)


#

```
File: contracts/LeverageMacroFactory.sol

15    address public immutable ebtcToken
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L15)


#

```
File: contracts/LeverageMacroFactory.sol

16    address public immutable stETH
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L16)


#

```
File: contracts/LeverageMacroFactory.sol

17    address public immutable sortedCdps
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L17)


#

```
File: contracts/PriceFeed.sol

22    string public constant NAME = "PriceFeed"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22)


#

```
File: contracts/PriceFeed.sol

26    AggregatorV3Interface public immutable STETH_ETH_CL_FEED
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L26)


#

```
File: contracts/PriceFeed.sol

33    uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33)


#

```
File: contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps"
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52)


#

```
File: contracts/SortedCdps.sol

54    address public immutable borrowerOperationsAddress
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L54)


#

```
File: contracts/SortedCdps.sol

56    ICdpManager public immutable cdpManager
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L56)


#

```
File: contracts/SortedCdps.sol

58    uint256 public immutable maxSize
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L58)


#

```
File: contracts/SortedCdps.sol

77    Data public data
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L77)


#

```
File: contracts/SortedCdps.sol

79    uint256 public nextCdpNonce
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L79)


#

```
File: contracts/SortedCdps.sol

80    bytes32 public constant dummyId =
81            0x0000000000000000000000000000000000000000000000000000000000000000
```
Public state variable lacks comment.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81)


</details>

# 


## Events are missing sender information
- Severity: Non-Critical
- Confidence: High

### Description
When an action is triggered based on a user's action, not being able to filter based on who triggered the action makes event processing a lot more cumbersome. Including the msg.sender in the events of these types of action will make events much more useful to end users, especially when msg.sender is not tx.origin.

<details>

<summary>
There are 37 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

112    emit SystemCollSharesUpdated(cachedSystemCollShares)
```
  The event `SystemCollSharesUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112)


#

```
File: contracts/ActivePool.sol

145    emit SystemCollSharesUpdated(cachedSystemCollShares)
```
  The event `SystemCollSharesUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145)


#

```
File: contracts/ActivePool.sol

173    emit SystemCollSharesUpdated(cachedSystemCollShares)
```
  The event `SystemCollSharesUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173)


#

```
File: contracts/ActivePool.sol

174    emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares)
```
  The event `FeeRecipientClaimableCollSharesIncreased` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174)


#

```
File: contracts/ActivePool.sol

200    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt)
```
  The event `ActivePoolEBTCDebtUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200)


#

```
File: contracts/ActivePool.sol

213    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt)
```
  The event `ActivePoolEBTCDebtUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213)


#

```
File: contracts/ActivePool.sol

247    emit SystemCollSharesUpdated(cachedSystemCollShares)
```
  The event `SystemCollSharesUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247)


#

```
File: contracts/ActivePool.sol

360    emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares)
```
  The event `FeeRecipientClaimableCollSharesDecreased` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360)


#

```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```
  The event `TCRNotified` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50)


#

```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```
  The event `GracePeriodStart` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55)


#

```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```
  The event `GracePeriodEnd` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69)


#

```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```
  The event `TCRNotified` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64)


#

```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```
  The event `SystemSnapshotsUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300)


#

```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```
  The event `CollateralFeePerUnitUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587)


#

```
File: contracts/CdpManagerStorage.sol

119    emit GracePeriodDurationSet(_gracePeriod)
```
  The event `GracePeriodDurationSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119)


#

```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```
  The event `StEthIndexUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542)


#

```
File: contracts/CdpManager.sol

55    emit StakingRewardSplitSet(stakingRewardSplit)
```
  The event `StakingRewardSplitSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55)


#

```
File: contracts/CdpManager.sol

630    emit BaseRateUpdated(newBaseRate)
```
  The event `BaseRateUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630)


#

```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```
  The event `LastRedemptionTimestampUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698)


#

```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```
  The event `CdpFeeSplitApplied` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602-L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602-L608)


#

```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```
  The event `TotalStakesUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414)


#

```
File: contracts/CdpManagerStorage.sol

425    emit TotalStakesUpdated(_newTotalStakes)
```
  The event `TotalStakesUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425)


#

```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```
  The event `CdpArrayIndexUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481)


#

```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```
  The event `CdpDebtRedistributionIndexUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340)


#

```
File: contracts/CdpManager.sol

782    emit StakingRewardSplitSet(_stakingRewardSplit)
```
  The event `StakingRewardSplitSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782)


#

```
File: contracts/CdpManager.sol

801    emit RedemptionFeeFloorSet(_redemptionFeeFloor)
```
  The event `RedemptionFeeFloorSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801)


#

```
File: contracts/CdpManager.sol

681    emit BaseRateUpdated(decayedBaseRate)
```
  The event `BaseRateUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681)


#

```
File: contracts/CdpManager.sol

824    emit MinuteDecayFactorSet(_minuteDecayFactor)
```
  The event `MinuteDecayFactorSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824)


#

```
File: contracts/CdpManager.sol

836    emit BetaSet(_beta)
```
  The event `BetaSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836)


#

```
File: contracts/CdpManager.sol

848    emit RedemptionsPaused(_paused)
```
  The event `RedemptionsPaused` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848)


#

```
File: contracts/Governor.sol

157    emit RoleNameSet(role, roleName)
```
  The event `RoleNameSet` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)


#

```
File: contracts/LiquidationLibrary.sol

516    emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares)
```
  The event `Liquidation` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516)


#

```
File: contracts/LiquidationLibrary.sol

891    emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex)
```
  The event `SystemDebtRedistributionIndexUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891)


#

```
File: contracts/PriceFeed.sol

555    emit LastGoodPriceUpdated(_currentPrice)
```
  The event `LastGoodPriceUpdated` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555)


#

```
File: contracts/SortedCdps.sol

405    emit NodeAdded(_id, _NICR)
```
  The event `NodeAdded` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405)


#

```
File: contracts/SortedCdps.sol

490    emit NodeRemoved(_id)
```
  The event `NodeRemoved` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490)


#

```
File: contracts/SortedCdps.sol

451    emit NodeRemoved(_ids[i])
```
  The event `NodeRemoved` emits an event without including the sender's address:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451)


</details>

# 


## Large numeric literals should use underscores for readability
- Severity: Non-Critical
- Confidence: High

### Description
In Solidity, it is common to work with large number literals to represent values such as timestamps, amounts, or other numerical data. However, when dealing with large numbers, readability can be improved by explicitly indicating the magnitude of the value.

By prefixing large number literals with an underscore, it provides a visual indication to developers and auditors that the value is intentionally large and not a typographical error. It helps prevent misinterpretation or confusion regarding the intended value and promotes code comprehension.

For example, instead of writing uint256 balance = 1000000000000000000;, the convention suggests writing uint256 balance = 1_000_000_000_000_000_000;. The underscores act as separators and improve readability without affecting the actual value.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

148    uint256 public minuteDecayFactor = 999037758833783000
```
 use `_` for 999037758833783000

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148)


#

```
File: contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000
```
 use `_` for 1000

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)


#

```
File: contracts/CdpManagerStorage.sol

150    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999
```
 use `_` for 999999999999999999

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)


#

```
File: contracts/PriceFeed.sol

33    uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000
```
 use `_` for 90000

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33)


#

```
File: contracts/PriceFeed.sol

32    uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800
```
 use `_` for 4800

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32)


</details>

# 


## Consider move Msg.sender checks to modifier
- Severity: Non-Critical
- Confidence: Medium

### Description
This detector identifies functions where checks for `msg.sender` authorization are not made in a modifier. Using modifiers for authorization checks can improve code readability and maintainability.

<details>

<summary>
There are 21 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

220    require(
221                msg.sender == borrowerOperationsAddress,
222                "ActivePool: Caller is not BorrowerOperations"
223            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223)


#

```
File: contracts/ActivePool.sol

228    require(
229                msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230                "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231)


#

```
File: contracts/ActivePool.sol

236    require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236)


#

```
File: contracts/ActivePool.sol

277    require(
278                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279                "ActivePool: IERC3156: Callback failed"
280            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280)


#

```
File: contracts/BorrowerOperations.sol

1091    require(
1092                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
1093                "IERC3156: Callback failed"
1094            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094)


#

```
File: contracts/CdpManagerStorage.sol

660    require(
661                msg.sender == borrowerOperationsAddress,
662                "CdpManager: Caller is not the BorrowerOperations contract"
663            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663)


#

```
File: contracts/CollSurplusPool.sol

113    require(
114                msg.sender == borrowerOperationsAddress,
115                "CollSurplusPool: Caller is not Borrower Operations"
116            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116)


#

```
File: contracts/CollSurplusPool.sol

120    require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120)


#

```
File: contracts/CollSurplusPool.sol

124    require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124)


#

```
File: contracts/EBTCToken.sol

307    require(
308                msg.sender == borrowerOperationsAddress,
309                "EBTCToken: Caller is not BorrowerOperations"
310            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307-L310)


#

```
File: contracts/EBTCToken.sol

315    require(
316                msg.sender == borrowerOperationsAddress ||
317                    msg.sender == cdpManagerAddress ||
318                    isAuthorized(msg.sender, msg.sig),
319                "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
320            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320)


#

```
File: contracts/EBTCToken.sol

324    require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324)


#

```
File: contracts/LeverageMacroBase.sol

45    require(owner() == msg.sender, "Must be owner")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45)


#

```
File: contracts/LeverageMacroBase.sol

356    require(
357                    msg.sender == address(borrowerOperations),
358                    "LeverageMacroReference: wrong lender for eBTC flashloan"
359                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359)


#

```
File: contracts/LeverageMacroBase.sol

362    require(
363                    msg.sender == address(activePool),
364                    "LeverageMacroReference: wrong lender for stETH flashloan"
365                )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365)


#

```
File: contracts/SimplifiedDiamondLike.sol

52    require(msg.sender == owner)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52)


#

```
File: contracts/SimplifiedDiamondLike.sol

67    require(msg.sender == owner)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67)


#

```
File: contracts/SimplifiedDiamondLike.sol

77    require(msg.sender == address(this))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77)


#

```
File: contracts/SimplifiedDiamondLike.sol

111    require(msg.sender == owner, "Must be owner")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111)


#

```
File: contracts/SortedCdps.sol

715    require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715)


#

```
File: contracts/SortedCdps.sol

720    require(
721                msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722                "SortedCdps: Caller is neither BO nor CdpM"
723            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723)


</details>

# 


## Functions Not Implementing an Interface
- Severity: Non-Critical
- Confidence: High

### Description
Contracts with public or external functions should typically implement an interface for clarity and modularity. If they do not, it could lead to issues with understanding the contract's intended API and maintainability concerns.

<details>

<summary>
There are 51 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

371    function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371-L384](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371-L384)


#

```
File: contracts/ActivePool.sol

404    function setFeeBps(uint256 _newFee) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404-L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404-L413)


#

```
File: contracts/ActivePool.sol

417    function setFlashLoansPaused(bool _paused) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417-L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417-L422)


#

```
File: contracts/BorrowerOperations.sol

659    function DOMAIN_SEPARATOR() external view returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L659-L661](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L659-L661)


#

```
File: contracts/BorrowerOperations.sol

1140    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150)


#

```
File: contracts/BorrowerOperations.sol

1154    function setFeeBps(uint256 _newFee) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154-L1163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154-L1163)


#

```
File: contracts/BorrowerOperations.sol

1167    function setFlashLoansPaused(bool _paused) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167-L1172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167-L1172)


#

```
File: contracts/CdpManager.sol

570    function getSystemDebt() public view returns (uint256 entireSystemDebt) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570-L572](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570-L572)


#

```
File: contracts/CdpManager.sol

717    function getDeploymentStartTime() public view returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L717-L719](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L717-L719)


#

```
File: contracts/CdpManager.sol

727    function checkPotentialRecoveryMode(
728            uint256 _systemCollShares,
729            uint256 _systemDebt,
730            uint256 _price
731        ) external view returns (bool) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L727-L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L727-L733)


#

```
File: contracts/CdpManager.sol

773    function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773-L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773-L783)


#

```
File: contracts/CdpManager.sol

788    function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788-L802](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788-L802)


#

```
File: contracts/CdpManager.sol

807    function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807-L825](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807-L825)


#

```
File: contracts/CdpManager.sol

830    function setBeta(uint256 _beta) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837)


#

```
File: contracts/CdpManager.sol

843    function setRedemptionsPaused(bool _paused) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843-L849)


#

```
File: contracts/CdpManagerStorage.sol

111    function setGracePeriod(uint128 _gracePeriod) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111-L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111-L120)


#

```
File: contracts/CollSurplusPool.sol

142    function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142-L151](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142-L151)


#

```
File: contracts/EBTCToken.sol

104    function burn(uint256 _amount) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104-L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104-L107)


#

```
File: contracts/EBTCToken.sol

176    function DOMAIN_SEPARATOR() external view returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L176-L178](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L176-L178)


#

```
File: contracts/Governor.sol

43    function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L43-L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L43-L66)


#

```
File: contracts/Governor.sol

73    function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73-L91](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73-L91)


#

```
File: contracts/Governor.sol

96    function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96-L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96-L115)


#

```
File: contracts/Governor.sol

120    function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120-L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120-L126)


#

```
File: contracts/Governor.sol

131    function getEnabledFunctionsInTarget(
132            address _target
133        ) public view returns (bytes4[] memory _funcs) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131-L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131-L141)


#

```
File: contracts/Governor.sol

146    function getRoleName(uint8 role) external view returns (string memory roleName) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146-L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146-L148)


#

```
File: contracts/Governor.sol

154    function setRoleName(uint8 role, string memory roleName) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154-L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154-L158)


#

```
File: contracts/HintHelpers.sol

48    function getRedemptionHints(
49            uint256 _EBTCamount,
50            uint256 _price,
51            uint256 _maxIterations
52        )
53            external
54            view
55            returns (
56                bytes32 firstRedemptionHint,
57                uint256 partialRedemptionHintNICR,
58                uint256 truncatedEBTCamount,
59                uint256 partialRedemptionNewColl
60            )
61        
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48-L122)


#

```
File: contracts/HintHelpers.sol

164    function getApproxHint(
165            uint256 _CR,
166            uint256 _numTrials,
167            uint256 _inputRandomSeed
168        ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164-L197)


#

```
File: contracts/HintHelpers.sol

203    function computeNominalCR(uint256 _coll, uint256 _debt) external pure returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L203-L205](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L203-L205)


#

```
File: contracts/HintHelpers.sol

212    function computeCR(
213            uint256 _coll,
214            uint256 _debt,
215            uint256 _price
216        ) external pure returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L212-L218](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L212-L218)


#

```
File: contracts/LeverageMacroBase.sol

39    function owner() public virtual returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L39-L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L39-L41)


#

```
File: contracts/LeverageMacroBase.sol

118    function doOperation(
119            FlashLoanType flType,
120            uint256 borrowAmount,
121            LeverageMacroOperation calldata operation,
122            PostOperationCheck postCheckType,
123            PostCheckParams calldata checkParams
124        ) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L211](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118-L211)


#

```
File: contracts/LeverageMacroBase.sol

214    function sweepToCaller() public 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L214-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L214-L230)


#

```
File: contracts/LeverageMacroBase.sol

234    function sweepToken(address token, uint256 amount) public 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234-L238](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234-L238)


#

```
File: contracts/LeverageMacroBase.sol

338    function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L338-L341](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L338-L341)


#

```
File: contracts/LeverageMacroBase.sol

344    function onFlashLoan(
345            address initiator,
346            address token,
347            uint256 amount,
348            uint256 fee,
349            bytes calldata data
350        ) external returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L344-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L344-L379)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

63    function owner() public override returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L63-L66)


#

```
File: contracts/LeverageMacroFactory.sol

38    function deployNewMacro() external returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38-L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38-L40)


#

```
File: contracts/LeverageMacroFactory.sol

43    function deployNewMacro(address _owner) public returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59)


#

```
File: contracts/LeverageMacroReference.sol

44    function owner() public override returns (address) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44-L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44-L46)


#

```
File: contracts/LeverageMacroReference.sol

50    function resetApprovals() external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L50-L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L50-L56)


#

```
File: contracts/LiquidationLibrary.sol

40    function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L40-L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L40-L42)


#

```
File: contracts/LiquidationLibrary.sol

50    function partiallyLiquidate(
51            bytes32 _cdpId,
52            uint256 _partialAmount,
53            bytes32 _upperPartialHint,
54            bytes32 _lowerPartialHint
55        ) external nonReentrantSelfAndBOps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L50-L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L50-L58)


#

```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#

```
File: contracts/PriceFeed.sol

358    function setFallbackCaller(address _fallbackCaller) external requiresAuth 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358-L389](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358-L389)


#

```
File: contracts/SimplifiedDiamondLike.sol

51    function setFallbackHandler(bytes4 sig, address handler) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L51-L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L51-L61)


#

```
File: contracts/SimplifiedDiamondLike.sol

66    function setAllowAnyCall(bool allowNonCallbacks) external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L66-L71)


#

```
File: contracts/SimplifiedDiamondLike.sol

76    function enableCallbackForCall() external 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L76-L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L76-L79)


#

```
File: contracts/SimplifiedDiamondLike.sol

110    function execute(Operation[] calldata ops) external payable 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110-L126)


#

```
File: contracts/SimplifiedDiamondLike.sol

164    fallback() external payable 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L164-L166)


#

```
File: contracts/SortedCdps.sol

105    function toCdpId(
106            address owner,
107            uint256 blockHeight,
108            uint256 nonce
109        ) public pure returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L105-L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L105-L117)


</details>

# 


## Use of old Solidity version
- Severity: Non-Critical
- Confidence: High

### Description
Using an old version of Solidity may result in missing bug fixes and features. Consider upgrading to a more recent version of Solidity. As of writing, the latest version is 0.8.20.

<details>

<summary>
There are 34 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3)


#

```
File: contracts/BorrowerOperations.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3)


#

```
File: contracts/CdpManager.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3)


#

```
File: contracts/CdpManagerStorage.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3)


#

```
File: contracts/CollSurplusPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3)


#

```
File: contracts/EBTCToken.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3)


#

```
File: contracts/Governor.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2)


#

```
File: contracts/HintHelpers.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3)


#

```
File: contracts/Interfaces/IActivePool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3)


#

```
File: contracts/Interfaces/ICdpManager.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3)


#

```
File: contracts/Interfaces/IEBTCToken.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3)


#

```
File: contracts/Interfaces/IEbtcBase.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3)


#

```
File: contracts/Interfaces/IPermitNonce.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3)


#

```
File: contracts/Interfaces/IPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3)


#

```
File: contracts/Interfaces/IPositionManagers.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3)


#

```
File: contracts/Interfaces/IPriceFeed.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2)


#

```
File: contracts/Interfaces/ISortedCdps.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3)


#

```
File: contracts/LeverageMacroBase.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2)


#

```
File: contracts/LeverageMacroFactory.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2)


#

```
File: contracts/LeverageMacroReference.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2)


#

```
File: contracts/LiquidationLibrary.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3)


#

```
File: contracts/PriceFeed.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3)


#

```
File: contracts/SimplifiedDiamondLike.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2)


#

```
File: contracts/SortedCdps.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.20`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3)


#
solc-0.8.17 is not recommended for deployment

#
solc-0.4.26 is not recommended for deployment

</details>

# 


## Override function arguments that are unused should have the variable name removed or commented out
- Severity: Non-Critical
- Confidence: High

### Description
Unused arguments in overridden functions can lead to compiler warnings andcan make the code less readable. It is a good practice to remove or comment outunused arguments in these cases.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

99    bytes32 _cdpId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L99)


#

```
File: contracts/CdpManager.sol

110    bytes32 _cdpId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L110)


#

```
File: contracts/CdpManager.sol

111    uint256 _partialAmount
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L111)


#

```
File: contracts/CdpManager.sol

112    bytes32 _upperPartialHint
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L112)


#

```
File: contracts/CdpManager.sol

113    bytes32 _lowerPartialHint
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L113)


#

```
File: contracts/CdpManager.sol

126    bytes32[] memory _cdpArray
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126)


</details>

# 


## Use return statement when there is a named return variable is redundant
- Severity: Non-Critical
- Confidence: High

### Description
In Solidity, when you define a named return variable for a function, it is not necessary to use a return statement to return a value from the function. The named return variable will automatically be assigned the return value when the function exits.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

233    return singleRedemption
```
 redundant return statements
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L233)


#

```
File: contracts/CdpManager.sol

562    return index
```
 redundant return statements
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L562](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L562)


#

```
File: contracts/LiquidationLibrary.sol

859    return newTotals
```
 redundant return statements
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L859](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L859)


</details>

# 


## Event Emission Preceding External Calls: A Best Practice
- Severity: Non-Critical
- Confidence: Medium

### Description

Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls


<details>

<summary>
There are 38 instances of this issue:

</summary>

###
#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

733    function _getTotalFromBatchLiquidate_RecoveryMode(
734            uint256 _price,
735            uint256 _systemCollShares,
736            uint256 _systemDebt,
737            bytes32[] memory _cdpArray
738        ) internal returns (LiquidationTotals memory totals) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

	- 
```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

		- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

		- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

764    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

791    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

765    _getLiquidationValuesRecoveryMode(
766                            _price,
767                            vars.entireSystemDebt,
768                            vars.entireSystemColl,
769                            vars,
770                            singleLiquidation
771                        )
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

792    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733-L805)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

807    function _getTotalsFromBatchLiquidate_NormalMode(
808            uint256 _price,
809            uint256 _TCR,
810            bytes32[] memory _cdpArray
811        ) internal returns (LiquidationTotals memory totals) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

		- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

823    _syncAccounting(vars.cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

824    _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

397    function _liquidateCDPPartially(
398            LiquidationLocals memory _partialState
399        ) private returns (uint256, uint256) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

429    _reInsertPartialLiquidation(
430                    _partialState,
431                    EbtcMath._computeNominalCR(newColl, newDebt),
432                    _debtAndColl.debt,
433                    _debtAndColl.collShares
434                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```

	Event emitted after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397-L448)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

61    function _liquidateIndividualCdpSetup(
62            bytes32 _cdpId,
63            uint256 _partialAmount,
64            bytes32 _upperPartialHint,
65            bytes32 _lowerPartialHint
66        ) internal 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

69    _syncAccounting(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

71    uint256 _price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```

		- 
```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

437    emit CdpPartiallyLiquidated(
438                    _cdpId,
439                    sortedCdps.getOwnerAddress(_cdpId),
440                    _partialDebt,
441                    _partialColl,
442                    CdpOperation.partiallyLiquidate,
443                    msg.sender,
444                    _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

490    emit CdpUpdated(
491                _cdpId,
492                sortedCdps.getOwnerAddress(_cdpId),
493                msg.sender,
494                _oldDebt,
495                _oldColl,
496                Cdps[_cdpId].debt,
497                Cdps[_cdpId].coll,
498                Cdps[_cdpId].stake,
499                CdpOperation.partiallyLiquidate
500            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

516    emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/LiquidationLibrary.sol

891    emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```

	- 
```
File: contracts/CdpManagerStorage.sol

425    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

130    _liquidateIndividualCdpSetupCDP(_liqState, _rs)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L61-L131)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

153    (
154                    liquidationValues.debtToBurn,
155                    liquidationValues.totalCollToSendToLiquidator
156                ) = _liquidateCDPPartially(_liqState)
```

		- 
```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

145    (
146                    liquidationValues.debtToBurn,
147                    liquidationValues.totalCollToSendToLiquidator,
148                    liquidationValues.debtToRedistribute,
149                    liquidationValues.liquidatorCollSharesReward,
150                    liquidationValues.collSurplus
151                ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

153    (
154                    liquidationValues.debtToBurn,
155                    liquidationValues.totalCollToSendToLiquidator
156                ) = _liquidateCDPPartially(_liqState)
```

		- 
```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

162    (
163                        liquidationValues.debtToBurn,
164                        liquidationValues.totalCollToSendToLiquidator,
165                        liquidationValues.debtToRedistribute,
166                        liquidationValues.liquidatorCollSharesReward,
167                        liquidationValues.collSurplus
168                    ) = _liquidateCdpInGivenMode(_liqState, _recoveryState)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/LiquidationLibrary.sol

196    activePool.transferSystemCollShares(
197                        address(collSurplusPool),
198                        _outputState.totalSurplusCollShares
199                    )
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

516    emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares)
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

891    emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/LiquidationLibrary.sol

172    _finalizeLiquidation(
173                liquidationValues.debtToBurn,
174                liquidationValues.totalCollToSendToLiquidator,
175                liquidationValues.debtToRedistribute,
176                liquidationValues.liquidatorCollSharesReward,
177                liquidationValues.collSurplus,
178                startingSystemColl,
179                startingSystemDebt,
180                _liqState.price
181            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

223    function _liquidateIndividualCdpSetupCDPInNormalMode(
224            LiquidationLocals memory _liqState
225        ) private returns (LiquidationLocals memory) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

227    (
228                uint256 _totalDebtToBurn,
229                uint256 _totalColToSend,
230                uint256 _liquidatorReward
231            ) = _closeCdpByLiquidation(_liqState.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	Event emitted after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L223-L293)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

295    function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296            LiquidationRecoveryModeLocals memory _recoveryState
297        ) private returns (LiquidationRecoveryModeLocals memory) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

299    (
300                uint256 _totalDebtToBurn,
301                uint256 _totalColToSend,
302                uint256 _liquidatorReward
303            ) = _closeCdpByLiquidation(_recoveryState.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	Event emitted after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

295    function _liquidateIndividualCdpSetupCDPInRecoveryMode(
296            LiquidationRecoveryModeLocals memory _recoveryState
297        ) private returns (LiquidationRecoveryModeLocals memory) 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

299    (
300                uint256 _totalDebtToBurn,
301                uint256 _totalColToSend,
302                uint256 _liquidatorReward
303            ) = _closeCdpByLiquidation(_recoveryState.cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

	- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	Event emitted after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L295-L379)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

466    function _reInsertPartialLiquidation(
467            LiquidationLocals memory _partialState,
468            uint256 _newNICR,
469            uint256 _oldDebt,
470            uint256 _oldColl
471        ) internal 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

484    sortedCdps.reInsert(
485                _cdpId,
486                _newNICR,
487                _partialState.upperPartialHint,
488                _partialState.lowerPartialHint
489            )
```

	Event emitted after the call(s):
	- 
```
File: contracts/LiquidationLibrary.sol

490    emit CdpUpdated(
491                _cdpId,
492                sortedCdps.getOwnerAddress(_cdpId),
493                msg.sender,
494                _oldDebt,
495                _oldColl,
496                Cdps[_cdpId].debt,
497                Cdps[_cdpId].coll,
498                Cdps[_cdpId].stake,
499                CdpOperation.partiallyLiquidate
500            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

171    _closeCdpByRedemption(
172                        _redeemColFromCdp.cdpId,
173                        0,
174                        newColl,
175                        _liquidatorRewardShares,
176                        _borrower
177                    )
```

		- 
```
File: contracts/CdpManager.sol

254    activePool.decreaseSystemDebt(_EBTC)
```

		- 
```
File: contracts/CdpManager.sol

257    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares)
```

		- 
```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

179    emit CdpUpdated(
180                        _redeemColFromCdp.cdpId,
181                        _borrower,
182                        msg.sender,
183                        _oldDebtAndColl.debt,
184                        _oldDebtAndColl.collShares,
185                        0,
186                        0,
187                        0,
188                        CdpOperation.redeemCollateral
189                    )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

220    emit CdpUpdated(
221                    _redeemColFromCdp.cdpId,
222                    ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223                    msg.sender,
224                    _oldDebtAndColl.debt,
225                    _oldDebtAndColl.collShares,
226                    newDebt,
227                    newColl,
228                    Cdps[_redeemColFromCdp.cdpId].stake,
229                    CdpOperation.redeemCollateral
230                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

425    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/CdpManager.sol

218    _updateStakeAndTotalStakes(_redeemColFromCdp.cdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

344    function _syncAccounting(bytes32 _cdpId) internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

348    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/CdpManagerStorage.sol

381    _updateRedistributedDebtIndex(_cdpId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/CdpManagerStorage.sol

370    _applyAccumulatedFeeSplit(
371                        _cdpId,
372                        _newColl,
373                        _feeSplitDistributed,
374                        _oldPerUnitCdp,
375                        _systemStEthFeePerUnitIndex
376                    )
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344-L407)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

509    function _syncGlobalAccounting() internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

518    _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/CdpManagerStorage.sol

519    _updateSystemSnapshotsExcludeCollRemainder(0)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L509-L521)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

73    function _syncGracePeriod() internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

		- 
```
File: contracts/CdpManagerStorage.sol

81    _endGracePeriod(tcr)
```

	- 
```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

		- 
```
File: contracts/CdpManagerStorage.sol

79    _startGracePeriod(tcr)
```

	- 
```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/CdpManagerStorage.sol

81    _endGracePeriod(tcr)
```

	- 
```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/CdpManagerStorage.sol

79    _startGracePeriod(tcr)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73-L83)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

574    function _takeSplitAndUpdateFeePerUnit(
575            uint256 _feeTaken,
576            uint256 _newPerUnit,
577            uint256 _newErrorPerUnit
578        ) internal 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574-L588)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

367    emit CdpLiquidated(
368                _recoveryState.cdpId,
369                _borrower,
370                _totalDebtToBurn,
371                // please note this is the collateral share of the liquidated CDP
372                _cappedColPortion,
373                CdpOperation.liquidateInRecoveryMode,
374                msg.sender,
375                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/LiquidationLibrary.sol

312    emit CdpUpdated(
313                _recoveryState.cdpId,
314                _borrower,
315                msg.sender,
316                _totalDebtToBurn,
317                _totalColToSend,
318                0,
319                0,
320                0,
321                CdpOperation.liquidateInRecoveryMode
322            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/LiquidationLibrary.sol

281    emit CdpLiquidated(
282                _liqState.cdpId,
283                _borrower,
284                _totalDebtToBurn,
285                // please note this is the collateral share of the liquidated CDP
286                _cappedColPortion,
287                CdpOperation.liquidateInNormalMode,
288                msg.sender,
289                _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/LiquidationLibrary.sol

238    emit CdpUpdated(
239                _liqState.cdpId,
240                _borrower,
241                msg.sender,
242                _totalDebtToBurn,
243                _totalColToSend,
244                0,
245                0,
246                0,
247                CdpOperation.liquidateInNormalMode
248            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#
Reentrancy in 
```
File: contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/LiquidationLibrary.sol

689    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

691    vars.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/LiquidationLibrary.sol

699    totals = _getTotalFromBatchLiquidate_RecoveryMode(
700                    vars.price,
701                    systemColl,
702                    systemDebt,
703                    _cdpArray
704                )
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

		- 
```
File: contracts/LiquidationLibrary.sol

337    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

707    totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray)
```

		- 
```
File: contracts/CdpManagerStorage.sol

257    sortedCdps.remove(_cdpId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/LiquidationLibrary.sol

714    activePool.transferSystemCollShares(address(collSurplusPool), totals.totalCollSurplus)
```

	- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

		- 
```
File: contracts/LiquidationLibrary.sol

530    ebtcToken.burn(msg.sender, totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

533    activePool.decreaseSystemDebt(totalDebtToBurn)
```

		- 
```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

516    emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares)
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

	- 
```
File: contracts/LiquidationLibrary.sol

891    emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex)
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/LiquidationLibrary.sol

717    _finalizeLiquidation(
718                totals.totalDebtToBurn,
719                totals.totalCollToSendToLiquidator,
720                totals.totalDebtToRedistribute,
721                totals.totalCollReward,
722                totals.totalCollSurplus,
723                systemColl,
724                systemDebt,
725                vars.price
726            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679-L727)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

346    function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

347    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	Event emitted after the call(s):
	- 
```
File: contracts/ActivePool.sol

360    emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346-L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346-L363)


#
Reentrancy in 
```
File: contracts/LeverageMacroFactory.sol

43    function deployNewMacro(address _owner) public returns (address) 
```
:
	External calls:
	- 
```
File: contracts/LeverageMacroFactory.sol

44    address addy = address(
45                new LeverageMacroReference(
46                    borrowerOperations,
47                    activePool,
48                    cdpManager,
49                    ebtcToken,
50                    stETH,
51                    sortedCdps,
52                    _owner
53                )
54            )
```

	Event emitted after the call(s):
	- 
```
File: contracts/LeverageMacroFactory.sol

56    emit DeployNewMacro(_owner, addy)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43-L59)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

261    function flashLoan(
262            IERC3156FlashBorrower receiver,
263            address token,
264            uint256 amount,
265            bytes calldata data
266        ) external override returns (bool) 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

274    collateral.transfer(address(receiver), amount)
```

	- 
```
File: contracts/ActivePool.sol

277    require(
278                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279                "ActivePool: IERC3156: Callback failed"
280            )
```

	- 
```
File: contracts/ActivePool.sol

283    collateral.transferFrom(address(receiver), address(this), amountWithFee)
```

	- 
```
File: contracts/ActivePool.sol

286    collateral.transfer(feeRecipientAddress, fee)
```

	Event emitted after the call(s):
	- 
```
File: contracts/ActivePool.sol

307    emit FlashLoanSuccess(address(receiver), token, amount, fee)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1077    function flashLoan(
1078            IERC3156FlashBorrower receiver,
1079            address token,
1080            uint256 amount,
1081            bytes calldata data
1082        ) external override returns (bool) 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1088    ebtcToken.mint(address(receiver), amount)
```

	- 
```
File: contracts/BorrowerOperations.sol

1091    require(
1092                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
1093                "IERC3156: Callback failed"
1094            )
```

	- 
```
File: contracts/BorrowerOperations.sol

1100    ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount)
```

	- 
```
File: contracts/BorrowerOperations.sol

1103    ebtcToken.burn(feeRecipientAddress, amount)
```

	Event emitted after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1105    emit FlashLoanSuccess(address(receiver), token, amount, fee)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

336    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManager.sol

338    totals.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

		- 
```
File: contracts/CdpManager.sol

254    activePool.decreaseSystemDebt(_EBTC)
```

		- 
```
File: contracts/CdpManager.sol

257    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares)
```

		- 
```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```

		- 
```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

		- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

	- 
```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

		- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

602    emit CdpFeeSplitApplied(
603                _cdpId,
604                _oldPerUnitCdp,
605                _systemStEthFeePerUnitIndex,
606                _feeSplitDistributed,
607                _newColl
608            )
```

		- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

	- 
```
File: contracts/CdpManager.sol

179    emit CdpUpdated(
180                        _redeemColFromCdp.cdpId,
181                        _borrower,
182                        msg.sender,
183                        _oldDebtAndColl.debt,
184                        _oldDebtAndColl.collShares,
185                        0,
186                        0,
187                        0,
188                        CdpOperation.redeemCollateral
189                    )
```

		- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

	- 
```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```

		- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

	- 
```
File: contracts/CdpManager.sol

220    emit CdpUpdated(
221                    _redeemColFromCdp.cdpId,
222                    ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223                    msg.sender,
224                    _oldDebtAndColl.debt,
225                    _oldDebtAndColl.collShares,
226                    newDebt,
227                    newColl,
228                    Cdps[_redeemColFromCdp.cdpId].stake,
229                    CdpOperation.redeemCollateral
230                )
```

		- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

	- 
```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

		- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

		- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

		- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

	- 
```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

	- 
```
File: contracts/CdpManagerStorage.sol

425    emit TotalStakesUpdated(_newTotalStakes)
```

		- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

320    function redeemCollateral(
321            uint256 _debt,
322            bytes32 _firstRedemptionHint,
323            bytes32 _upperPartialRedemptionHint,
324            bytes32 _lowerPartialRedemptionHint,
325            uint256 _partialRedemptionHintNICR,
326            uint256 _maxIterations,
327            uint256 _maxFeePercentage
328        ) external override nonReentrantSelfAndBOps 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

336    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManager.sol

338    totals.price = priceFeed.fetchPrice()
```

	- 
```
File: contracts/CdpManager.sol

393    _syncAccounting(_cId)
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManager.sol

403    SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404                        _redeemColFromCdp
405                    )
```

		- 
```
File: contracts/CdpManager.sol

254    activePool.decreaseSystemDebt(_EBTC)
```

		- 
```
File: contracts/CdpManager.sol

257    collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares)
```

		- 
```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```

		- 
```
File: contracts/CdpManager.sol

209    sortedCdps.reInsert(
210                    _redeemColFromCdp.cdpId,
211                    newNICR,
212                    _redeemColFromCdp.upperPartialRedemptionHint,
213                    _redeemColFromCdp.lowerPartialRedemptionHint
214                )
```

	- 
```
File: contracts/CdpManager.sol

435    sortedCdps.remove(_firstRedeemed)
```

	- 
```
File: contracts/CdpManager.sol

442    sortedCdps.batchRemove(_toRemoveIds)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

630    emit BaseRateUpdated(newBaseRate)
```

		- 
```
File: contracts/CdpManager.sol

447    _updateBaseRateFromRedemption(
448                totals.collSharesDrawn,
449                totals.price,
450                totals.systemDebtAtStart
451            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

		- 
```
File: contracts/CdpManager.sol

460    _syncGracePeriodForGivenValues(
461                totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
462                totals.systemDebtAtStart - totals.debtToRedeem,
463                totals.price
464            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

		- 
```
File: contracts/CdpManager.sol

460    _syncGracePeriodForGivenValues(
461                totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
462                totals.systemDebtAtStart - totals.debtToRedeem,
463                totals.price
464            )
```

	- 
```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```

		- 
```
File: contracts/CdpManager.sol

447    _updateBaseRateFromRedemption(
448                totals.collSharesDrawn,
449                totals.price,
450                totals.systemDebtAtStart
451            )
```

	- 
```
File: contracts/CdpManager.sol

466    emit Redemption(
467                _debt,
468                totals.debtToRedeem,
469                totals.collSharesDrawn,
470                totals.feeCollShares,
471                msg.sender
472            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/CdpManager.sol

460    _syncGracePeriodForGivenValues(
461                totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
462                totals.systemDebtAtStart - totals.debtToRedeem,
463                totals.price
464            )
```

	- 
```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/CdpManager.sol

460    _syncGracePeriodForGivenValues(
461                totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
462                totals.systemDebtAtStart - totals.debtToRedeem,
463                totals.price
464            )
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320-L485)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

830    function setBeta(uint256 _beta) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

831    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

681    emit BaseRateUpdated(decayedBaseRate)
```

		- 
```
File: contracts/CdpManager.sol

833    _decayBaseRate()
```

	- 
```
File: contracts/CdpManager.sol

836    emit BetaSet(_beta)
```

	- 
```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```

		- 
```
File: contracts/CdpManager.sol

833    _decayBaseRate()
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830-L837)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

404    function setFeeBps(uint256 _newFee) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

405    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	Event emitted after the call(s):
	- 
```
File: contracts/ActivePool.sol

412    emit FlashFeeSet(msg.sender, _oldFee, _newFee)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404-L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404-L413)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1154    function setFeeBps(uint256 _newFee) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1157    cdpManager.syncGlobalAccounting()
```

	Event emitted after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1162    emit FlashFeeSet(msg.sender, _oldFee, _newFee)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154-L1163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154-L1163)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

390    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

391    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	Event emitted after the call(s):
	- 
```
File: contracts/ActivePool.sol

399    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390-L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390-L400)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1140    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1146    cdpManager.syncGlobalAccounting()
```

	Event emitted after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1149    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140-L1150)


#
Reentrancy in 
```
File: contracts/ActivePool.sol

417    function setFlashLoansPaused(bool _paused) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/ActivePool.sol

418    ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod()
```

	Event emitted after the call(s):
	- 
```
File: contracts/ActivePool.sol

421    emit FlashLoansPaused(msg.sender, _paused)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417-L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417-L422)


#
Reentrancy in 
```
File: contracts/BorrowerOperations.sol

1167    function setFlashLoansPaused(bool _paused) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/BorrowerOperations.sol

1168    cdpManager.syncGlobalAccounting()
```

	Event emitted after the call(s):
	- 
```
File: contracts/BorrowerOperations.sol

1171    emit FlashLoansPaused(msg.sender, _paused)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167-L1172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167-L1172)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

111    function setGracePeriod(uint128 _gracePeriod) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

117    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

119    emit GracePeriodDurationSet(_gracePeriod)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111-L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111-L120)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

807    function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

817    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

681    emit BaseRateUpdated(decayedBaseRate)
```

		- 
```
File: contracts/CdpManager.sol

820    _decayBaseRate()
```

	- 
```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```

		- 
```
File: contracts/CdpManager.sol

820    _decayBaseRate()
```

	- 
```
File: contracts/CdpManager.sol

824    emit MinuteDecayFactorSet(_minuteDecayFactor)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807-L825](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807-L825)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

788    function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

798    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

801    emit RedemptionFeeFloorSet(_redemptionFeeFloor)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788-L802](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788-L802)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

843    function setRedemptionsPaused(bool _paused) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

844    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

681    emit BaseRateUpdated(decayedBaseRate)
```

		- 
```
File: contracts/CdpManager.sol

845    _decayBaseRate()
```

	- 
```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```

		- 
```
File: contracts/CdpManager.sol

845    _decayBaseRate()
```

	- 
```
File: contracts/CdpManager.sol

848    emit RedemptionsPaused(_paused)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843-L849)


#
Reentrancy in 
```
File: contracts/CdpManager.sol

773    function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth 
```
:
	External calls:
	- 
```
File: contracts/CdpManager.sol

779    syncGlobalAccountingAndGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManager.sol

782    emit StakingRewardSplitSet(_stakingRewardSplit)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773-L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773-L783)


#
Reentrancy in 
```
File: contracts/CdpManagerStorage.sol

527    function syncGlobalAccountingAndGracePeriod() public 
```
:
	External calls:
	- 
```
File: contracts/CdpManagerStorage.sol

528    _syncGlobalAccounting()
```

		- 
```
File: contracts/CdpManagerStorage.sol

585    activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken)
```

	- 
```
File: contracts/CdpManagerStorage.sol

529    _syncGracePeriod()
```

		- 
```
File: contracts/CdpManagerStorage.sol

74    uint256 price = priceFeed.fetchPrice()
```

	Event emitted after the call(s):
	- 
```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

		- 
```
File: contracts/CdpManagerStorage.sol

529    _syncGracePeriod()
```

	- 
```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

		- 
```
File: contracts/CdpManagerStorage.sol

529    _syncGracePeriod()
```

	- 
```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/CdpManagerStorage.sol

529    _syncGracePeriod()
```

	- 
```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

		- 
```
File: contracts/CdpManagerStorage.sol

529    _syncGracePeriod()
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L527-L530](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L527-L530)


</details>

# 


## Variable names too similar
- Severity: Non-Critical
- Confidence: Medium

### Description
Detect variables with names that are too similar.

<details>

<summary>
There are 90 instances of this issue:

</summary>

###
#
Variable 
```
File: contracts/BorrowerOperations.sol

708    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L708](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L708)


#
Variable 
```
File: contracts/BorrowerOperations.sol

637    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L637](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L637)


#
Variable 
```
File: contracts/BorrowerOperations.sol

629    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L629](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L629)


#
Variable 
```
File: contracts/BorrowerOperations.sol

647    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L647](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L647)


#
Variable 
```
File: contracts/BorrowerOperations.sol

617    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L617](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L617)


#
Variable 
```
File: contracts/BorrowerOperations.sol

610    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L610](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L610)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

81    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/BorrowerOperations.sol

272    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L272)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/BorrowerOperations.sol

302    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L302)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/BorrowerOperations.sol

221    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L221)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/BorrowerOperations.sol

805    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L805)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

330    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L330)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

814    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

67    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/Interfaces/IBorrowerOperations.sol

39    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L67)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

76    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

307    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L76)


#
Variable 
```
File: contracts/Interfaces/IBorrowerOperations.sol

44    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L44)


#
Variable 
```
File: contracts/BorrowerOperations.sol

854    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

207    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L854)


#
Variable 
```
File: contracts/BorrowerOperations.sol

816    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

804    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L816)


#
Variable 
```
File: contracts/BorrowerOperations.sol

845    uint256 _stEthBalanceDecrease
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

335    uint256 _stEthBalanceIncrease
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845)


#
Variable 
```
File: contracts/Interfaces/IPositionManagers.sol

20    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L20)


#
Variable 
```
File: contracts/Interfaces/IPositionManagers.sol

24    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L24)


#
Variable 
```
File: contracts/Interfaces/IPositionManagers.sol

34    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L34)


#
Variable 
```
File: contracts/Interfaces/IPositionManagers.sol

28    address _positionManager
```
 is too similar to 
```
File: contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L28)


#
Variable 
```
File: contracts/CdpManagerStorage.sol

150    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999
```
 is too similar to 
```
File: contracts/CdpManagerStorage.sol

149    uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)


#
Variable 
```
File: contracts/CdpManagerStorage.sol

878    uint256 _systemCollShare = activePool.getSystemCollShares()
```
 is too similar to 
```
File: contracts/CdpManagerStorage.sol

88    uint256 systemCollShares
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L878](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L878)


#
Variable 
```
File: contracts/LeverageMacroBase.sol

187    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 is too similar to 
```
File: contracts/LeverageMacroBase.sol

199    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187)


</details>

# 


## Constant redefined elsewhere
- Severity: Non-Critical
- Confidence: High

### Description
It suggests that constants should be defined in only one contract to prevent values from becoming out of sync when updates are made in different locations.

Consider consolidating constant definitions in a single contract or using a centralized approach, such as creating an internal constant in a library. This ensures that all references to the constant retrieve the same value, eliminating inconsistencies and the potential for errors caused by mismatched values.

Additionally, if a variable is used as a local cache of another contract's value, it is recommended to make the cache variable internal or private. By doing so, external users are required to query the contract with the source of truth, ensuring that callers always obtain the most up-to-date and accurate information.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#
bytes32 private constant _TYPE_HASH =
        0x8b73c3c69bb8fe3d512ecc4cf759cc79239f7b179b0ffacaa9a75d522b39400f is redefines:
-    
```
File: contracts/BorrowerOperations.sol

38    bytes32 private constant _TYPE_HASH =
39            0x8b73c3c69bb8fe3d512ecc4cf759cc79239f7b179b0ffacaa9a75d522b39400f
```

-    
```
File: contracts/EBTCToken.sol

39    bytes32 private constant _TYPE_HASH =
40            0x8b73c3c69bb8fe3d512ecc4cf759cc79239f7b179b0ffacaa9a75d522b39400f
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L38-L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L38-L39)


#
string internal constant _VERSION = "1" is redefines:
-    
```
File: contracts/BorrowerOperations.sol

41    string internal constant _VERSION = "1"
```

-    
```
File: contracts/EBTCToken.sol

30    string internal constant _VERSION = "1"
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41)


</details>

# 


## Typo and Spelling Error
- Severity: Non-Critical
- Confidence: Low

### Description
Consistently maintaining correct spelling and grammar is essential for code readability and comprehension. This detector helps ensure code quality by detecting and reporting potential typos and spelling errors, enabling developers to address and correct them promptly.

<details>

<summary>
There are 14 instances of this issue:

</summary>

###
#
in contract 
```
File: contracts/ActivePool.sol

22    contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner 
```
:

```
 @audit getters
// --- Getters for public variables. Required by IPool interface ---
 @audit sload
cachedSystemCollShares -= _shares; // Updating here avoids an SLOAD
 @audit boroweroperations
/// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager
 @audit liqudations
/// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares
 @audit redemptions
/// @dev Redemptions result in the shares being sent to the coll surplus pool for claiming by the CDP owner
 @audit cr
/// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.
 @audit flashloans
// === Flashloans === //
 @audit cei
// NOTE: Invariant Check, technically breaks CEI but I think we must use it
 @audit lusd
// NOTE: This means any balance > systemCollShares is stuck, this is also present in LUSD as is
 @audit calcualted
/// @return The flashloan fee calcualted for given token and loan amount
 @audit permissinos
/// @dev Call permissinos are managed via authority for flexibility, rather than gating call to just feeRecipient.
 @audit sload
address cachedFeeRecipientAddress = feeRecipientAddress; // Saves an SLOAD
 @audit flashloans
/// @notice Sets new Fee for FlashLoans
 @audit flashloans
/// @notice Should Flashloans be paused?
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22-L423)


#
in contract 
```
File: contracts/BorrowerOperations.sol

21    contract BorrowerOperations is
22        EbtcBase,
23        ReentrancyGuard,
24        IBorrowerOperations,
25        ERC3156FlashLender,
26        AuthNoOwner,
27        PermitNonce
28    
```
:

```
 @audit positionmanager
// Mapping of borrowers to approved position managers, by approval status: cdpOwner(borrower) -> positionManager -> PositionManagerApproval (None, OneTime, Persistent)
 @audit collateralization
/// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.
 @audit collateralization
/// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.
 @audit collateralization
/// @notice when a Cdp has been fully redeemed from and closed, or liquidated in Recovery Mode with a collateralization ratio higher enough (like over MCR)
 @audit positon
/// @return EIP712 compatible hash of Positon Manager permit
 @audit cr
/// @dev Liquidator reward shares are not considered as part of the system for CR purposes.
 @audit getters
// --- ICR and TCR getters ---
 @audit sstore
// Gas: Repay from user balance, so we don't trigger a new SSTORE
 @audit calcualted
/// @return The flashloan fee calcualted for given token and loan amount
 @audit flashloans
/// @notice Sets new Fee for FlashLoans
 @audit flashloans
/// @notice Should Flashloans be paused?
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21-L1173)


#
in contract 
```
File: contracts/CdpManager.sol

16    contract CdpManager is CdpManagerStorage, ICdpManager, Proxy 
```
:

```
 @audit getters
// --- Getters ---
 @audit liquidatable
//  > MCR & < TCR |  only liquidatable in Recovery Mode (TCR < CCR)
 @audit oog
/// @notice This makes it easier to avoid OOG for the frontend, as only knowing approximately the average cost of an iteration is enough,
 @audit frontend
/// @notice A frontend should use HintHelper.getRedemptionHints() to calculate what the ICR of this Cdp will be after redemption,
 @audit synchorize
/// @notice Synchorize the accounting for the specified Cdp
 @audit cdpowner
// Push the Cdpowner to the array
 @audit cdpowner
// Record the index of the new Cdpowner on their Cdp struct
 @audit collateralization
/// @notice The total collateralization ratio (TCR) of the system as a cached "view" (maybe outdated)
 @audit collateralization
/// @return TCR The cached total collateralization ratio (TCR) of the system (does not take into account pending global state)
 @audit redemptions
/// @notice Pause or unpause redemptions
 @audit getters
// --- Cdp property getters ---
 @audit redistributions
/// @notice Cached value - does not include pending changes from redistributions
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987)


#
in contract 
```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```
:

```
 @audit cei
/// @dev To maintain CEI compliance we use this trusted function
 @audit cei
/// @dev To maintain CEI compliance we use this trusted function
 @audit redemptions
/// @dev Internal notify called by Redemptions and Liquidations
 @audit pruposes
/// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
 @audit pruposes
/// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
 @audit redemptions
/// @dev Internal notify called by Redemptions and Liquidations
 @audit redemptions
/// @dev Variant for internal use in redemptions and liquidations
 @audit duratin
/// @notice Set grace period duratin
 @audit permissioned
/// @notice Permissioned governance function, must set grace period duration above hardcoded minimum
 @audit liquity
* Corresponds to (1 / ALPHA) in the Liquity white paper.
 @audit rewardsnapshot
// Map active cdps to their RewardSnapshot (eBTC debt redistributed)
 @audit reentrancy
/// @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation
 @audit reentrancy
/// @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.
 @audit occured
* this indicates that redistributions have occured since the snapshot was made, and the user therefore has
 @audit occured
// If any collShares or debt changes occured
 @audit cdpowners
* Remove a Cdp owner from the CdpOwners array, not preserving array order. Removing owner 'B' does the following:
 @audit redistributions
/// @dev Takes a cdp's pending coll and debt rewards from redistributions into account.
 @audit calcualted
/// @notice Return the pending extra debt assigned to the Cdp from liquidation redistribution, calcualted by Cdp's stake
 @audit gloabl
/// @param _cdpId The CdpId whose debt redistribution tracking index to be queried against the gloabl one
 @audit redistributions
/// @notice Calculate the Cdps entire debt and coll, including pending debt redistributions and collateral reduction from split fee.
 @audit rebase
/// @audit-ok We don't take the fee if we had a negative rebase
 @audit liquidatable
/// @param icr The ICR of a Cdp to check if liquidatable
 @audit liquidatable
/// @return whether the Cdp of specified icr is liquidatable with specified tcr
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#
in contract 
```
File: contracts/CollSurplusPool.sol

16    contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner 
```
:

```
 @audit collateraltoken
* @param _collTokenAddress The address of the CollateralToken
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16-L152)


#
in contract 
```
File: contracts/EBTCToken.sol

26    contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce 
```
:

```
 @audit eip
// --- EIP 2612 Functionality (https://eips.ethereum.org/EIPS/eip-2612) ---
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358)


#
in contract 
```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```
:

```
 @audit maxreemable
// maxReemable = min(remainingToRedeem, currentDebt)
 @audit numtrials
Submitting numTrials = k * sqrt(length), with k = 15 makes it very, very likely that the ouput address will
 @audit cr
/// @notice Compute nominal CR for a specified collateral and debt amount
 @audit cr
/// @return The computed nominal CR for the given collateral and debt
 @audit cr
/// @notice Compute CR for a specified collateral, debt amount, and price
 @audit cr
/// @return The computed CR for the given parameters
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219)


#
in contract 
```
File: contracts/Interfaces/ICdpManagerData.sol

13    interface ICdpManagerData is IRecoveryModeGracePeriod 
```
:

```
 @audit redemptions
// --- Variable container structs for redemptions ---
 @audit stethfeesplit
function syncGlobalAccounting() external; // Accrues StEthFeeSplit without influencing Grace Period
 @audit stethfeesplit
function syncGlobalAccountingAndGracePeriod() external; // Accrues StEthFeeSplit and influences Grace Period
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L264)


#
in contract 
```
File: contracts/LeverageMacroBase.sol

26    contract LeverageMacroBase 
```
:

```
 @audit noflashloan
noFlashloan // Use this to not perform a FL and just `doOperation`
 @audit cdpstats
// Used only if cdpStats || isClosed
 @audit swapsbefore
*         - SwapsBefore
 @audit swapsafter
*         - SwapsAfter
 @audit delegatecall
/// @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)
 @audit minout
///     A minOut Check
 @audit memcopying
// we call via assembly to avoid memcopying a very large returndata
 @audit inloc
add(_calldata, 0x20), // inloc
 @audit inlen
mload(_calldata), // inlen
 @audit outloc
0, // outloc
 @audit outlen
0 // outlen
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535)


#
in contract 
```
File: contracts/LeverageMacroDelegateTarget.sol

40    contract LeverageMacroDelegateTarget is LeverageMacroBase 
```
:

```
 @audit delegatecall
// Approves are done via `execute` since this is a contract you delegatecall into
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40-L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L40-L67)


#
in contract 
```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```
:

```
 @audit guarenteed
uint256 _ICR = getCachedICR(_cdpId, _price); // @audit syncAccounting already called, guarenteed to be synced
 @audit liquidatable
} // Implicit Else Case, Implies ICR < MRC, meaning the CDP is liquidatable
 @audit hinthelper
// For partial liquidation, caller should use HintHelper smart contract to get correct hints for reinsertion into sorted CDP list
 @audit emmiting
// without emmiting events
 @audit liqudiation
// early return: if new collateral is zero, we have a full liqudiation
 @audit sortedcdp
// Re-Insertion into SortedCdp list after partial liquidation
 @audit althought
: 0; // Else 0 (note we may underpay per the comment above, althought that may be imaginary)
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#
in contract 
```
File: contracts/PriceFeed.sol

21    contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner 
```
:

```
 @audit mainnet
// Chainlink oracles in mainnet
 @audit chainlink
// Maximum time period allowed since Chainlink's latest round data timestamp, beyond which Chainlink is considered frozen.
 @audit chainlink
// Maximum deviation allowed between two consecutive Chainlink oracle prices. 18-digit precision.
 @audit chainlink
* to return to using the Chainlink oracle. 18-digit precision.
 @audit chainlink
/// @param _collEthCLFeed The address of the collateral-ETH ChainLink feed
 @audit chainlink
/// @param _ethBtcCLFeed The address of the ETH-BTC ChainLink feed
 @audit chainlink
// Get an initial price from Chainlink to serve as first reference for lastGoodPrice
 @audit chainlink
/// @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.
 @audit chainlink
// --- CASE 1: System fetched last price from Chainlink  ---
 @audit chainlink
// If Chainlink is broken, try Fallback
 @audit chainlink
// If Chainlink is broken and Fallback is working, switch to Fallback and return current Fallback price
 @audit chainlink
// If Chainlink is frozen, try Fallback
 @audit chainlink
// If Fallback is frozen or working, remember Chainlink froze, and switch to Fallback
 @audit chainlink
// If Chainlink price has changed by > 50% between two consecutive rounds, compare it to Fallback's price
 @audit chainlink
* two consecutive rounds was likely a legitmate market price movement, and so continue using Chainlink
 @audit chainlink
// If Chainlink is working and Fallback is broken, remember Fallback is broken
 @audit chainlink
// If Chainlink is working, return Chainlink current price (no status change)
 @audit chainlink
// If both Fallback and Chainlink are live, unbroken, and reporting similar prices, switch back to Chainlink
 @audit untrusted
// --- CASE 3: Both oracles were untrusted at the last price fetch ---
 @audit chainlink
* If there's no fallback, only use Chainlink
 @audit untrusted
// Otherwise, return the last good price - both oracles are still untrusted (no status change)
 @audit chainlink
// --- CASE 4: Using Fallback, and Chainlink is frozen ---
 @audit chainlink
// If Chainlink is broken, remember it and switch to using Fallback
 @audit chainlink
// if Chainlink is frozen and Fallback is broken, remember Fallback broke, and return last good price
 @audit chainlink
// if Chainlink is frozen and Fallback is working, keep using Fallback (no status change)
 @audit chainlink
// if Chainlink is live and Fallback is broken, remember Fallback broke, and return Chainlink price
 @audit chainlink
// If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison
 @audit chainlink
// If Chainlink is live and Fallback is working, compare prices. Switch to Chainlink
 @audit chainlink
// if prices are within 5%, and return Chainlink price.
 @audit chainlink
// Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price
 @audit untrusted
// --- CASE 5: Using Chainlink, Fallback is untrusted ---
 @audit untrusted
// If Chainlink breaks, now both oracles are untrusted
 @audit chainlink
// If Chainlink is frozen, return last good price (no status change)
 @audit chainlinkworking
// If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price
 @audit chainlink
// If Chainlink is live but deviated >50% from it's previous price and Fallback is still untrusted, switch
 @audit bothoraclesuntrusted
// to bothOraclesUntrusted and return last good price
 @audit chainlink
// Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,
 @audit chainlink
// return Chainlink price (no status change)
 @audit prover
/// @audit This should never be used, but we added it for the Certora Prover
 @audit chainlink
/// @notice Checks if Chainlink oracle is broken by checking both the current and previous responses
 @audit chainlink
/// @dev Chainlink is considered broken if its current or previous round data is in any way bad. We check the previous round for two reasons.
 @audit chainlink
/// @dev 2. Chainlink is the PriceFeed's preferred primary oracle - having two consecutive valid round responses adds peace of mind when using or returning to Chainlink.
 @audit chainlink
/// @param _currentResponse The latest response from the Chainlink oracle
 @audit chainlink
/// @param _prevResponse The previous response from the Chainlink oracle
 @audit chainlink
/// @return A boolean indicating whether the Chainlink oracle is broken
 @audit chainlink
/// @notice Checks for a bad response from the Chainlink oracle
 @audit chainlink
/// @param _response The response from the Chainlink oracle to evaluate
 @audit chainlink
/// @return A boolean indicating whether the Chainlink oracle response is bad
 @audit chainlink
/// @notice Checks if the Chainlink oracle is frozen
 @audit chainlink
/// @param _response The response from the Chainlink oracle to evaluate
 @audit chainlink
/// @return A boolean indicating whether the Chainlink oracle is frozen
 @audit chainlink
/// @notice Checks if the price change between Chainlink oracle rounds is above the maximum threshold allowed
 @audit chainlink
/// @param _currentResponse The latest response from the Chainlink oracle
 @audit chainlink
/// @param _prevResponse The previous response from the Chainlink oracle
 @audit chainlink
/// @return A boolean indicating whether the price change from Chainlink oracle is above the maximum threshold allowed
 @audit chainlink
/// @notice Checks if both the Chainlink and fallback oracles are live, unbroken, and reporting similar prices.
 @audit chainlink
/// @param _chainlinkResponse The latest response from the Chainlink oracle.
 @audit chainlink
/// @param _prevChainlinkResponse The previous response from the Chainlink oracle.
 @audit chainlink
/// @notice Checks if the prices reported by the Chainlink and fallback oracles are similar, within the maximum deviation specified by MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES.
 @audit chainlink
/// @param _chainlinkResponse The response from the Chainlink oracle.
 @audit chainlink
/// @notice Stores the price reported by the Chainlink oracle.
 @audit chainlink
/// @param _answer The latest price reported by the Chainlink oracle.
 @audit chainlink
/// @return The price reported by the Chainlink oracle.
 @audit chainlink
/// @notice Fetches Chainlink responses for the current round of data for both ETH-BTC and stETH-ETH price feeds.
 @audit chainlink
// If call to Chainlink succeeds, record the current decimal precision
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit chainlink
// If call to Chainlink succeeds, record the current decimal precision
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit chainlink
/// @notice Fetches Chainlink responses for the previous round of data for both ETH-BTC and stETH-ETH price feeds.
 @audit indentical
// Behavior should be indentical to following block if this revert was caught
 @audit chainlink
// If call to Chainlink succeeds, record the current decimal precision
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit chainlink
// If call to Chainlink succeeds, record the current decimal precision
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit prev
// Try to get latest prices data from prev round:
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit chainlink
// If call to Chainlink aggregator reverts, return a zero response with success = false
 @audit decimalss
// @param _stEthEthDecimals stETH:BTC feed decimalss
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806)


#
in contract 
```
File: contracts/SimplifiedDiamondLike.sol

25    contract SimplifiedDiamondLike 
```
:

```
 @audit simplfiied
// SIMPLFIIED STORAGE POS
 @audit hardcoded
/// === HARDCODED SETTERS === ///
 @audit funsig
/// @notice Given a funsig and a implementation address
 @audit delegatecall
///     Set the handler to the logic we will delegatecall to
 @audit hardcoded
// Hardcoded Generic Function
 @audit impl
// NOTE: We could check calldata to see if this has to be done, but this is fine for a reference impl
 @audit callbackenabledforcall
/// @dev toggle callbackEnabledForCall in OurSetting
 @audit tx
/// @dev Execute one tx
 @audit php
// PHP is my favourite language
 @audit diamondlike
/// @dev DiamondLike Fallback
 @audit delegatecall
/// - If it exists, delegatecall to it, forwarding the data
 @audit reentrancy
// NOTE: May also act as reEntrancy guard
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202)


#
in contract 
```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```
:

```
 @audit accommendate
serialized |= bytes32(blockHeight) << BLOCK_SHIFT; // to accommendate more than 4.2 billion blocks
 @audit seach
/// @param startNodeId the seach traversal will start at this given CDP instead of the tail of the list
 @audit startnode
/// @dev current lastly-visited CDP as the startNode for next pagination with a false indicator
 @audit startnode
/// @return cdpId The CDP Id if found, otherwise return current lastly-visited CDP as the startNode for next pagination
 @audit startnode
/// @return last seen CDP for the startNode for next pagination
 @audit startnode
/// @dev current lastly-visited CDP as the startNode for next pagination
 @audit startnode
/// @dev current lastly-visited CDP as the startNode for next pagination
 @audit storages
// delete node & owner storages to get gas refund
 @audit prev
// Set prev pointer of new head to null
 @audit prev
// Set prev pointer of next node to the previous node
 @audit nicrs
// `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs
 @audit nicrs
/// @dev Descend the list (larger NICRs to smaller NICRs) to find a valid insert position
 @audit nicrs
/// @dev Ascend the list (smaller NICRs to larger NICRs) to find a valid insert position
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Functions that alter state should emit events
- Severity: Non-Critical
- Confidence: Medium

### Description
Functions that alter the state of the contract should emit an event to inform external observers of the change.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

431    function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) 
```
 The function `_updateStakeForCdp` changes state but does not emit an event.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431-L438](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431-L438)


#

```
File: contracts/CdpManager.sol

550    function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) 
```
 The function `_addCdpIdToArray` changes state but does not emit an event.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563)


#

```
File: contracts/CdpManager.sol

977    function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal 
```
 The function `_setCdpCollShares` changes state but does not emit an event.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L977-L979](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L977-L979)


#

```
File: contracts/CdpManager.sol

984    function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal 
```
 The function `_setCdpDebt` changes state but does not emit an event.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L984-L986](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L984-L986)


#

```
File: contracts/CollSurplusPool.sol

130    function increaseTotalSurplusCollShares(uint256 _value) external override 
```
 The function `increaseTotalSurplusCollShares` changes state but does not emit an event.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130-L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130-L133)


</details>

# 


## Conformance to Solidity struct naming conventions
- Severity: Non-Critical
- Confidence: High

### Description
Solidity defines a [naming convention](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#struct-names) that should be followed for struct names. According to the convention, struct names should be in CapWords.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#
Struct 
```
File: contracts/HintHelpers.sol

19    struct LocalVariables_getRedemptionHints {
20            uint256 remainingEbtcToRedeem;
21            uint256 minNetDebtInBTC;
22            bytes32 currentCdpId;
23            address currentCdpUser;
24        }
```
 LocalVariables_getRedemptionHints is not in CapWords

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L19-L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L19-L24)


#
Struct 
```
File: contracts/Interfaces/ICdpManagerData.sol

147    struct LocalVariables_OuterLiquidationFunction {
148            uint256 price;
149            bool recoveryModeAtStart;
150            uint256 liquidatedDebt;
151            uint256 liquidatedColl;
152        }
```
 LocalVariables_OuterLiquidationFunction is not in CapWords

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L147-L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L147-L152)


#
Struct 
```
File: contracts/Interfaces/ICdpManagerData.sol

154    struct LocalVariables_LiquidationSequence {
155            uint256 i;
156            uint256 ICR;
157            bytes32 cdpId;
158            bool backToNormalMode;
159            uint256 entireSystemDebt;
160            uint256 entireSystemColl;
161            uint256 price;
162            uint256 TCR;
163        }
```
 LocalVariables_LiquidationSequence is not in CapWords

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L154-L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L154-L163)


</details>

# 


## TODO comments
- Severity: Non-Critical
- Confidence: High

### Description
TODO comments may signal that a feature is missing or not ready for audit, consider resolving the issue and removing the TODO comment.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

16    contract CdpManager is CdpManagerStorage, ICdpManager, Proxy 
```
  The contract CdpManager has a TODO comment:
     //    Cdp ICR     |       Liquidation Behavior (TODO gas compensation?)
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16-L987)


</details>

# 


## Too many digits
- Severity: Non-Critical
- Confidence: Medium

### Description

Literals with many digits are difficult to read and review.


<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```
 uses literals with too many digits:
	- 
```
File: contracts/SortedCdps.sol

80    bytes32 public constant dummyId =
81            0x0000000000000000000000000000000000000000000000000000000000000000
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Top level declarations should be separated by two blank lines
- Severity: Non-Critical
- Confidence: High

### Description
Detects when top-level declarations are not separated by two blank lines.

<details>

<summary>
There are 14 instances of this issue:

</summary>

###
#

```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```

```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

8    import "./IActivePool.sol";
```

```
File: contracts/Interfaces/ICdpManager.sol

9    interface ICdpManager is IEbtcBase, ICdpManagerData 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

5    import "./ICollSurplusPool.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

5    import "./IERC3156FlashBorrower.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5)


#

```
File: contracts/Interfaces/IEBTCToken.sol

5    import "../Dependencies/IERC20.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5)


#

```
File: contracts/Interfaces/ICdpManager.sol

5    import "./IEbtcBase.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L5)


#

```
File: contracts/Interfaces/IActivePool.sol

5    import "./IPool.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L5)


#

```
File: contracts/LeverageMacroBase.sol

5    import "./Interfaces/IERC3156FlashLender.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L5)


#

```
File: contracts/Interfaces/IEbtcBase.sol

5    import "./IPriceFeed.sol";
```

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5)


#

```
File: contracts/LeverageMacroBase.sol

10    import "./Dependencies/ICollateralToken.sol";
```

```
File: contracts/LeverageMacroFactory.sol

11    contract LeverageMacroFactory 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```

```
File: contracts/LeverageMacroFactory.sol

11    contract LeverageMacroFactory 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)


#

```
File: contracts/LeverageMacroBase.sol

10    import "./Dependencies/ICollateralToken.sol";
```

```
File: contracts/LeverageMacroReference.sol

11    contract LeverageMacroReference is LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```

```
File: contracts/LeverageMacroReference.sol

11    contract LeverageMacroReference is LeverageMacroBase 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)


#

```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12)


</details>

# 


## Enforce Underscore Prefix for Non-External Variable and Function Names
- Severity: Non-Critical
- Confidence: High

### Description
Non external variables and functions play an internal role within the contract and are not intended to be accessed directly from outside the contract or by other contracts. By prefixing them with an underscore, it provides a visual cue to developers and auditors that these entities are meant for internal use only.

Using an underscore prefix for non-external entities promotes consistency and helps prevent accidental access or confusion between internal and external entities. This convention enhances code maintainability and reduces the risk of unintended behavior or vulnerabilities caused by incorrect access to these variables and functions.

<details>

<summary>
There are 16 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

31    uint256 internal systemCollShares
```
 systemCollShares should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L31)


#

```
File: contracts/ActivePool.sol

32    uint256 internal systemDebt
```
 systemDebt should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L32)


#

```
File: contracts/ActivePool.sol

33    uint256 internal feeRecipientCollShares
```
 feeRecipientCollShares should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L33)


#

```
File: contracts/CdpManagerStorage.sol

128    ICollSurplusPool immutable collSurplusPool
```
 collSurplusPool should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L128)


#

```
File: contracts/CdpManagerStorage.sol

152    uint256 internal immutable deploymentStartTime
```
 deploymentStartTime should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L152)


#

```
File: contracts/CollSurplusPool.sol

28    uint256 internal totalSurplusCollShares
```
 totalSurplusCollShares should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L28)


#

```
File: contracts/CollSurplusPool.sol

30    mapping(address => uint256) internal balances
```
 balances should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L30)


#

```
File: contracts/Governor.sol

17    bytes32 NO_ROLES = bytes32(0)
```
 NO_ROLES should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)


#

```
File: contracts/Governor.sol

30    mapping(uint8 => string) internal roleNames
```
 roleNames should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30)


#

```
File: contracts/LeverageMacroBase.sol

35    bool internal immutable willSweep
```
 willSweep should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35)


#

```
File: contracts/LeverageMacroBase.sol

37    bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan")
```
 FLASH_LOAN_SUCCESS should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)


#

```
File: contracts/LeverageMacroBase.sol

498    function excessivelySafeCall(
499            address _target,
500            uint256 _gas,
501            uint256 _value,
502            uint16 _maxCopy,
503            bytes memory _calldata
504        ) internal returns (bool, bytes memory) 
```
 excessivelySafeCall(address,uint256,uint256,uint16,bytes) should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498-L534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498-L534)


#

```
File: contracts/LeverageMacroReference.sol

12    address internal immutable theOwner
```
 theOwner should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L12)


#

```
File: contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage")
```
 DIAMOND_STORAGE_POSITION should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)


#

```
File: contracts/SortedCdps.sol

60    uint256 constant ADDRESS_SHIFT = 96
```
 ADDRESS_SHIFT should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L60)


#

```
File: contracts/SortedCdps.sol

61    uint256 constant BLOCK_SHIFT = 64
```
 BLOCK_SHIFT should start with '_' prefix.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L61)


</details>

# 


## Unnecessary Casting of Variables
- Severity: Non-Critical
- Confidence: High

### Description
This detector scans for instances where a variable is casted to its own type. This is unnecessary and can be safely removed to improve code readability.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

220    emit CdpUpdated(
221                    _redeemColFromCdp.cdpId,
222                    ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223                    msg.sender,
224                    _oldDebtAndColl.debt,
225                    _oldDebtAndColl.collShares,
226                    newDebt,
227                    newColl,
228                    Cdps[_redeemColFromCdp.cdpId].stake,
229                    CdpOperation.redeemCollateral
230                )
```
Unnecessary cast: `ISortedCdps(sortedCdps)` it cast to the same type.<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230)


#

```
File: contracts/CdpManagerStorage.sol

390    emit CdpUpdated(
391                    _cdpId,
392                    ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393                    msg.sender,
394                    prevDebt,
395                    prevCollShares,
396                    _newDebt,
397                    _newColl,
398                    _cdp.stake,
399                    CdpOperation.syncAccounting
400                )
```
Unnecessary cast: `ISortedCdps(sortedCdps)` it cast to the same type.<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390-L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390-L400)


</details>

# 


## Import declarations should import specific identifiers, rather than the whole file
- Severity: Non-Critical
- Confidence: High

### Description
Import declarations should import specific identifiers, rather than the whole file, in order to avoid polluting the symbol namespace and to make flattened files smaller, which can speed up compilation.Using import declarations of the form import {< identifier_name >} from 'some/file.sol' can help achieve this by only importing the necessary identifiers from the external file.By following this convention, Solidity developers can improve code readability and reduce the size of compiled contracts, which can improve contract performance and reduce transaction costs on the blockchain

<details>

<summary>
There are 87 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

5    import "./Interfaces/IActivePool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L5)


#

```
File: contracts/ActivePool.sol

6    import "./Interfaces/ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L6)


#

```
File: contracts/ActivePool.sol

7    import "./Dependencies/ICollateralToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L7)


#

```
File: contracts/ActivePool.sol

8    import "./Interfaces/ICdpManagerData.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L8)


#

```
File: contracts/ActivePool.sol

9    import "./Dependencies/ERC3156FlashLender.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L9)


#

```
File: contracts/ActivePool.sol

10    import "./Dependencies/SafeERC20.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L10)


#

```
File: contracts/ActivePool.sol

11    import "./Dependencies/ReentrancyGuard.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L11)


#

```
File: contracts/ActivePool.sol

12    import "./Dependencies/AuthNoOwner.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L12)


#

```
File: contracts/ActivePool.sol

13    import "./Dependencies/BaseMath.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L13)


#

```
File: contracts/BorrowerOperations.sol

5    import "./Interfaces/IBorrowerOperations.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L5)


#

```
File: contracts/BorrowerOperations.sol

6    import "./Interfaces/ICdpManager.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L6)


#

```
File: contracts/BorrowerOperations.sol

7    import "./Interfaces/ICdpManagerData.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L7)


#

```
File: contracts/BorrowerOperations.sol

8    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L8)


#

```
File: contracts/BorrowerOperations.sol

9    import "./Interfaces/ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L9)


#

```
File: contracts/BorrowerOperations.sol

10    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L10)


#

```
File: contracts/BorrowerOperations.sol

11    import "./Dependencies/EbtcBase.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L11)


#

```
File: contracts/BorrowerOperations.sol

12    import "./Dependencies/ReentrancyGuard.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L12)


#

```
File: contracts/BorrowerOperations.sol

13    import "./Dependencies/Ownable.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L13)


#

```
File: contracts/BorrowerOperations.sol

14    import "./Dependencies/AuthNoOwner.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L14)


#

```
File: contracts/BorrowerOperations.sol

15    import "./Dependencies/ERC3156FlashLender.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L15)


#

```
File: contracts/BorrowerOperations.sol

16    import "./Dependencies/PermitNonce.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L16)


#

```
File: contracts/CdpManager.sol

5    import "./Interfaces/ICdpManager.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L5)


#

```
File: contracts/CdpManager.sol

6    import "./Interfaces/ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L6)


#

```
File: contracts/CdpManager.sol

7    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L7)


#

```
File: contracts/CdpManager.sol

8    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L8)


#

```
File: contracts/CdpManager.sol

9    import "./Dependencies/ICollateralTokenOracle.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L9)


#

```
File: contracts/CdpManager.sol

10    import "./CdpManagerStorage.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L10)


#

```
File: contracts/CdpManager.sol

11    import "./Dependencies/Proxy.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L11)


#

```
File: contracts/CdpManagerStorage.sol

5    import "./Interfaces/ICdpManager.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L5)


#

```
File: contracts/CdpManagerStorage.sol

6    import "./Interfaces/ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L6)


#

```
File: contracts/CdpManagerStorage.sol

7    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L7)


#

```
File: contracts/CdpManagerStorage.sol

8    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L8)


#

```
File: contracts/CdpManagerStorage.sol

9    import "./Dependencies/EbtcBase.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L9)


#

```
File: contracts/CdpManagerStorage.sol

10    import "./Dependencies/ReentrancyGuard.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L10)


#

```
File: contracts/CdpManagerStorage.sol

11    import "./Dependencies/ICollateralTokenOracle.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L11)


#

```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12)


#

```
File: contracts/CollSurplusPool.sol

5    import "./Interfaces/ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L5)


#

```
File: contracts/CollSurplusPool.sol

6    import "./Dependencies/ICollateralToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L6)


#

```
File: contracts/CollSurplusPool.sol

7    import "./Dependencies/SafeERC20.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L7)


#

```
File: contracts/CollSurplusPool.sol

8    import "./Dependencies/ReentrancyGuard.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L8)


#

```
File: contracts/CollSurplusPool.sol

9    import "./Dependencies/AuthNoOwner.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L9)


#

```
File: contracts/CollSurplusPool.sol

10    import "./Interfaces/IActivePool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L10)


#

```
File: contracts/EBTCToken.sol

5    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L5)


#

```
File: contracts/EBTCToken.sol

7    import "./Dependencies/AuthNoOwner.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L7)


#

```
File: contracts/EBTCToken.sol

8    import "./Dependencies/PermitNonce.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L8)


#

```
File: contracts/HintHelpers.sol

5    import "./Interfaces/ICdpManager.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L5)


#

```
File: contracts/HintHelpers.sol

6    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L6)


#

```
File: contracts/HintHelpers.sol

7    import "./Dependencies/EbtcBase.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L7)


#

```
File: contracts/Interfaces/IActivePool.sol

5    import "./IPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L5)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

4    import "./IPositionManagers.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L4)


#

```
File: contracts/Interfaces/ICdpManager.sol

5    import "./IEbtcBase.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L5)


#

```
File: contracts/Interfaces/ICdpManager.sol

6    import "./ICdpManagerData.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L6)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

5    import "./ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L5)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

6    import "./IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L6)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

7    import "./ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L7)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

8    import "./IActivePool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L8)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

9    import "./IRecoveryModeGracePeriod.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L9)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)


#

```
File: contracts/Interfaces/IEBTCToken.sol

5    import "../Dependencies/IERC20.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L5)


#

```
File: contracts/Interfaces/IEBTCToken.sol

6    import "../Dependencies/IERC2612.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L6)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

5    import "./IERC3156FlashBorrower.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L5)


#

```
File: contracts/Interfaces/IEbtcBase.sol

5    import "./IPriceFeed.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L5)


#

```
File: contracts/LeverageMacroBase.sol

4    import "./Interfaces/IBorrowerOperations.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L4)


#

```
File: contracts/LeverageMacroBase.sol

5    import "./Interfaces/IERC3156FlashLender.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L5)


#

```
File: contracts/LeverageMacroBase.sol

6    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L6)


#

```
File: contracts/LeverageMacroBase.sol

7    import "./Interfaces/ICdpManager.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L7)


#

```
File: contracts/LeverageMacroBase.sol

8    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L8)


#

```
File: contracts/LeverageMacroBase.sol

9    import "./Interfaces/IPriceFeed.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L9)


#

```
File: contracts/LeverageMacroBase.sol

10    import "./Dependencies/ICollateralToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L10)


#

```
File: contracts/LeverageMacroBase.sol

12    import "./Dependencies/SafeERC20.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L12)


#

```
File: contracts/LeverageMacroFactory.sol

5    import "./Dependencies/ICollateralToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L5)


#

```
File: contracts/LeverageMacroFactory.sol

6    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6)


#

```
File: contracts/LiquidationLibrary.sol

4    import "./Interfaces/ICdpManagerData.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L4](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L4)


#

```
File: contracts/LiquidationLibrary.sol

5    import "./Interfaces/ICollSurplusPool.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L5)


#

```
File: contracts/LiquidationLibrary.sol

6    import "./Interfaces/IEBTCToken.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L6)


#

```
File: contracts/LiquidationLibrary.sol

7    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L7)


#

```
File: contracts/LiquidationLibrary.sol

8    import "./Dependencies/ICollateralTokenOracle.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L8)


#

```
File: contracts/LiquidationLibrary.sol

9    import "./CdpManagerStorage.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L9)


#

```
File: contracts/PriceFeed.sol

5    import "./Interfaces/IPriceFeed.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L5)


#

```
File: contracts/PriceFeed.sol

6    import "./Interfaces/IFallbackCaller.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L6)


#

```
File: contracts/PriceFeed.sol

7    import "./Dependencies/AggregatorV3Interface.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L7)


#

```
File: contracts/PriceFeed.sol

8    import "./Dependencies/BaseMath.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L8)


#

```
File: contracts/PriceFeed.sol

9    import "./Dependencies/EbtcMath.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L9)


#

```
File: contracts/PriceFeed.sol

10    import "./Dependencies/AuthNoOwner.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L10)


#

```
File: contracts/SortedCdps.sol

5    import "./Interfaces/ISortedCdps.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L5)


#

```
File: contracts/SortedCdps.sol

6    import "./Interfaces/ICdpManager.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L6)


#

```
File: contracts/SortedCdps.sol

7    import "./Interfaces/IBorrowerOperations.sol";
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7)


</details>

# 


## Unused function arguments
- Severity: Non-Critical
- Confidence: High

### Description
Unused function arguments can be removed to save gas.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

757    uint256 _price
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757)


#

```
File: contracts/LeverageMacroBase.sol

347    uint256 amount
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L347](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L347)


#

```
File: contracts/LeverageMacroBase.sol

348    uint256 fee
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L348](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L348)


</details>

# 


## Unused event definition
- Severity: Non-Critical
- Confidence: High

### Description
There may be cases where a event superficially appears to be used, but this is only because there are multiple definitions of the event in different files. In such cases, the event definition should be moved into a separate file. 

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/Interfaces/ICdpManagerData.sol

16    event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);
```
 The event `FeeRecipientAddressChanged` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L16)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

9    event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);
```
 The event `MaxFlashFeeSet` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L9)


#

```
File: contracts/Interfaces/IPool.sol

9    event ETHBalanceUpdated(uint256 _newBalance);
```
 The event `ETHBalanceUpdated` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L9)


#

```
File: contracts/Interfaces/IPool.sol

10    event EBTCBalanceUpdated(uint256 _newBalance);
```
 The event `EBTCBalanceUpdated` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L10)


</details>

# 


## Event is missing indexed fields
- Severity: Non-Critical
- Confidence: High

### Description
Indexing event fields enhances the accessibility and efficiency of event data for off-chain tools that parse events. Indexing is particularly beneficial for filtering events based on specific criteria, such as address filtering. However, it's important to consider the additional gas cost associated with indexing. Indexing all fields may not be the best approach if gas usage is a concern. To properly index event fields, the following guidelines are recommended:

 - If an event has three or more applicable fields and gas usage is not a significant concern for the events in question, it is recommended to index all three applicable fields. This ensures efficient filtering based on multiple criteria.

 - If an event has fewer than three applicable fields, all of the applicable fields should be indexed to provide accessibility for filtering, even if there are fewer fields to consider.

By following these guidelines, you can optimize the accessibility and usability of your contract's events while considering the associated gas costs.

<details>

<summary>
There are 42 instances of this issue:

</summary>

###
#

```
File: contracts/Interfaces/IActivePool.sol

9    event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L9)


#

```
File: contracts/Interfaces/IActivePool.sol

10    event SystemCollSharesUpdated(uint256 _coll);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L10)


#

```
File: contracts/Interfaces/IActivePool.sol

12    event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L12)


#

```
File: contracts/Interfaces/IActivePool.sol

13    event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L13)


#

```
File: contracts/Interfaces/IActivePool.sol

14    event FlashLoanSuccess(
15            address indexed _receiver,
16            address indexed _token,
17            uint256 _amount,
18            uint256 _fee
19        );
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L14-L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L14-L19)


#

```
File: contracts/Interfaces/IActivePool.sol

20    event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L20)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

11    event FlashLoanSuccess(
12            address indexed _receiver,
13            address indexed _token,
14            uint256 _amount,
15            uint256 _fee
16        );
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L11-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L11-L16)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

17    event StakingRewardSplitSet(uint256 _stakingRewardSplit);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

18    event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L18)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

19    event MinuteDecayFactorSet(uint256 _minuteDecayFactor);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L19)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

20    event BetaSet(uint256 _beta);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L20)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

21    event RedemptionsPaused(bool _paused);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L21)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

23    event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L23)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

24    event Redemption(
25            uint256 _debtToRedeemExpected,
26            uint256 _debtToRedeemActual,
27            uint256 _collSharesSent,
28            uint256 _feeCollShares,
29            address indexed _redeemer
30        );
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L24-L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L24-L30)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

60    event BaseRateUpdated(uint256 _baseRate);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L60)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

61    event LastRedemptionTimestampUpdated(uint256 _lastFeeOpTime);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L61)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

62    event TotalStakesUpdated(uint256 _newTotalStakes);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L62)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

63    event SystemSnapshotsUpdated(uint256 _totalStakesSnapshot, uint256 _totalCollateralSnapshot);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L63)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

64    event SystemDebtRedistributionIndexUpdated(uint256 _systemDebtRedistributionIndex);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L64)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

65    event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L65)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

66    event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L66)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

67    event StEthIndexUpdated(uint256 _oldIndex, uint256 _newIndex, uint256 _updTimestamp);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L67)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

68    event CollateralFeePerUnitUpdated(uint256 _oldPerUnit, uint256 _newPerUnit, uint256 _feeTaken);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L68)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

69    event CdpFeeSplitApplied(
70            bytes32 _cdpId,
71            uint256 _oldPerUnitCdp,
72            uint256 _newPerUnitCdp,
73            uint256 _collReduced,
74            uint256 _collLeft
75        );
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L69-L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L69-L75)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

8    event SurplusCollSharesUpdated(address indexed _account, uint256 _newBalance);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L8)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

9    event CollSharesTransferred(address indexed _to, uint256 _amount);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L9)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

11    event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L11)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

8    event FlashFeeSet(address indexed _setter, uint256 _oldFee, uint256 _newFee);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L8)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

9    event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L9)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

10    event FlashLoansPaused(address indexed _setter, bool _paused);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L10)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

7    event FallbackTimeOutChanged(uint256 _oldTimeOut, uint256 _newTimeOut);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L7)


#

```
File: contracts/Interfaces/IPool.sol

9    event ETHBalanceUpdated(uint256 _newBalance);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L9)


#

```
File: contracts/Interfaces/IPool.sol

10    event EBTCBalanceUpdated(uint256 _newBalance);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L10)


#

```
File: contracts/Interfaces/IPool.sol

11    event CollSharesTransferred(address indexed _to, uint256 _amount);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L11)


#

```
File: contracts/Interfaces/IPositionManagers.sol

12    event PositionManagerApprovalSet(
13            address indexed _borrower,
14            address indexed _positionManager,
15            PositionManagerApproval _approval
16        );
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L12-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L12-L16)


#

```
File: contracts/Interfaces/IPriceFeed.sol

7    event LastGoodPriceUpdated(uint256 _lastGoodPrice);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L7)


#

```
File: contracts/Interfaces/IPriceFeed.sol

8    event PriceFeedStatusChanged(Status newStatus);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L8)


#

```
File: contracts/Interfaces/IPriceFeed.sol

13    event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

6    event TCRNotified(uint256 TCR);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L6)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

11    event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L11)


#

```
File: contracts/Interfaces/ISortedCdps.sol

9    event NodeAdded(bytes32 _id, uint _NICR);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9)


#

```
File: contracts/Interfaces/ISortedCdps.sol

10    event NodeRemoved(bytes32 _id);
```
event is not indexed properly.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L10)


</details>

# 


## Unused imports
- Severity: Non-Critical
- Confidence: High

### Description
Identify unused imports in source files that can be safely removed. Please note that this detector does not support files with cyclic imports or files that use 'import {...} from' directives.

<details>

<summary>
There are 11 instances of this issue:

</summary>

###
#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/ActivePool.sol.
Consider removing the following imports:

    - 
```
File: contracts/ActivePool.sol

13    import "./Dependencies/BaseMath.sol";
```
contracts/Interfaces/ICollSurplusPool.sol 
    - 
```
File: contracts/ActivePool.sol

13    import "./Dependencies/BaseMath.sol";
```
contracts/Interfaces/IActivePool.sol 
contracts/Interfaces/IActivePool.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L13)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/BorrowerOperations.sol.
Consider removing the following imports:

    - 
```
File: contracts/BorrowerOperations.sol

16    import "./Dependencies/PermitNonce.sol";
```
contracts/Interfaces/ICollSurplusPool.sol 
    - 
```
File: contracts/BorrowerOperations.sol

16    import "./Dependencies/PermitNonce.sol";
```
contracts/Interfaces/ICdpManagerData.sol 
    - 
```
File: contracts/BorrowerOperations.sol

16    import "./Dependencies/PermitNonce.sol";
```
contracts/Dependencies/Ownable.sol 
    - 
```
File: contracts/BorrowerOperations.sol

16    import "./Dependencies/PermitNonce.sol";
```
contracts/Interfaces/IEBTCToken.sol 
    - 
```
File: contracts/BorrowerOperations.sol

16    import "./Dependencies/PermitNonce.sol";
```
contracts/Interfaces/ISortedCdps.sol 
contracts/Interfaces/ISortedCdps.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L16)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/CdpManager.sol.
Consider removing the following imports:

    - 
```
File: contracts/CdpManager.sol

11    import "./Dependencies/Proxy.sol";
```
contracts/Interfaces/ICollSurplusPool.sol 
    - 
```
File: contracts/CdpManager.sol

11    import "./Dependencies/Proxy.sol";
```
contracts/Dependencies/ICollateralTokenOracle.sol 
    - 
```
File: contracts/CdpManager.sol

11    import "./Dependencies/Proxy.sol";
```
contracts/Interfaces/IEBTCToken.sol 
    - 
```
File: contracts/CdpManager.sol

11    import "./Dependencies/Proxy.sol";
```
contracts/Interfaces/ISortedCdps.sol 
    - 
```
File: contracts/CdpManager.sol

11    import "./Dependencies/Proxy.sol";
```
contracts/Interfaces/ICdpManager.sol 
contracts/Interfaces/ICdpManager.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L11)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/CdpManagerStorage.sol.
Consider removing the following imports:

    - 
```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```
contracts/Interfaces/ICollSurplusPool.sol 
    - 
```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```
contracts/Dependencies/ICollateralTokenOracle.sol 
    - 
```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```
contracts/Interfaces/IEBTCToken.sol 
    - 
```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```
contracts/Interfaces/ISortedCdps.sol 
    - 
```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```
contracts/Interfaces/ICdpManager.sol 
and adding the following:

    - 
```
File: contracts/CdpManagerStorage.sol

12    import "./Dependencies/AuthNoOwner.sol";
```
contracts/Interfaces/ICdpManagerData.sol 
contracts/Interfaces/ICdpManagerData.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L12)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/Governor.sol.
Consider removing the following imports:

    - 
```
File: contracts/Governor.sol

6    import {RolesAuthority} from "./Dependencies/RolesAuthority.sol";
```
contracts/Dependencies/Auth.sol 
    - 
```
File: contracts/Governor.sol

6    import {RolesAuthority} from "./Dependencies/RolesAuthority.sol";
```
contracts/Dependencies/EnumerableSet.sol 
contracts/Dependencies/EnumerableSet.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L6)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/HintHelpers.sol.
Consider removing the following imports:

    - 
```
File: contracts/HintHelpers.sol

7    import "./Dependencies/EbtcBase.sol";
```
contracts/Interfaces/ISortedCdps.sol 
contracts/Interfaces/ISortedCdps.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L7)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/Interfaces/ICdpManagerData.sol.
Consider removing the following imports:

    - 
```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```
contracts/Dependencies/ICollateralTokenOracle.sol 
    - 
```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```
contracts/Interfaces/ISortedCdps.sol 
    - 
```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```
contracts/Interfaces/ICollSurplusPool.sol 
    - 
```
File: contracts/Interfaces/ICdpManagerData.sol

10    import "../Dependencies/ICollateralTokenOracle.sol";
```
contracts/Interfaces/IActivePool.sol 
contracts/Interfaces/IActivePool.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L10)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/LeverageMacroBase.sol.
Consider removing the following imports:

    - 
```
File: contracts/LeverageMacroBase.sol

12    import "./Dependencies/SafeERC20.sol";
```
contracts/Interfaces/IEBTCToken.sol 
    - 
```
File: contracts/LeverageMacroBase.sol

12    import "./Dependencies/SafeERC20.sol";
```
contracts/Interfaces/ISortedCdps.sol 
    - 
```
File: contracts/LeverageMacroBase.sol

12    import "./Dependencies/SafeERC20.sol";
```
contracts/Interfaces/ICdpManager.sol 
    - 
```
File: contracts/LeverageMacroBase.sol

12    import "./Dependencies/SafeERC20.sol";
```
contracts/Interfaces/IPriceFeed.sol 
contracts/Interfaces/IPriceFeed.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L12)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/LeverageMacroFactory.sol.
Consider removing the following imports:

    - 
```
File: contracts/LeverageMacroFactory.sol

6    import "./Interfaces/IEBTCToken.sol";
```
contracts/Interfaces/IEBTCToken.sol 
    - 
```
File: contracts/LeverageMacroFactory.sol

6    import "./Interfaces/IEBTCToken.sol";
```
contracts/Dependencies/ICollateralToken.sol 
contracts/Dependencies/ICollateralToken.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L6)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/LiquidationLibrary.sol.
Consider removing the following imports:

    - 
```
File: contracts/LiquidationLibrary.sol

9    import "./CdpManagerStorage.sol";
```
contracts/Interfaces/ICollSurplusPool.sol 
    - 
```
File: contracts/LiquidationLibrary.sol

9    import "./CdpManagerStorage.sol";
```
contracts/Dependencies/ICollateralTokenOracle.sol 
    - 
```
File: contracts/LiquidationLibrary.sol

9    import "./CdpManagerStorage.sol";
```
contracts/Interfaces/ICdpManagerData.sol 
    - 
```
File: contracts/LiquidationLibrary.sol

9    import "./CdpManagerStorage.sol";
```
contracts/Interfaces/IEBTCToken.sol 
    - 
```
File: contracts/LiquidationLibrary.sol

9    import "./CdpManagerStorage.sol";
```
contracts/Interfaces/ISortedCdps.sol 
contracts/Interfaces/ISortedCdps.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L9)


#
Unused imports found in /home/david/Documents/code4rena/2023-10-badger/packages/contracts/contracts/SortedCdps.sol.
Consider removing the following imports:

    - 
```
File: contracts/SortedCdps.sol

7    import "./Interfaces/IBorrowerOperations.sol";
```
contracts/Interfaces/ISortedCdps.sol 
    - 
```
File: contracts/SortedCdps.sol

7    import "./Interfaces/IBorrowerOperations.sol";
```
contracts/Interfaces/IBorrowerOperations.sol 
contracts/Interfaces/IBorrowerOperations.sol

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L7)


</details>

# 


## Unused modifier definition
- Severity: Non-Critical
- Confidence: High

### Description
There may be cases where a modifier superficially appears to be used, but this is only because there are multiple definitions of the modifier in different files. In such cases, the modifier definition should be moved into a separate file. 

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

241    modifier nonReentrantSelfAndBOps() 
```
The modifier `nonReentrantSelfAndBOps` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L241-L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L241-L253)


</details>

# 


## Unused return
- Severity: Non-Critical
- Confidence: Medium

### Description
The return value of an external call is not stored in a local or state variable.

<details>

<summary>
There are 16 instances of this issue:

</summary>

###
#

```
File: contracts/LeverageMacroBase.sol

148    IERC3156FlashLender(address(borrowerOperations)).flashLoan(
149                    IERC3156FlashBorrower(address(this)),
150                    address(ebtcToken),
151                    borrowAmount,
152                    abi.encode(operation)
153                )
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148-L153)


#

```
File: contracts/LeverageMacroBase.sol

155    IERC3156FlashLender(address(activePool)).flashLoan(
156                    IERC3156FlashBorrower(address(this)),
157                    address(stETH),
158                    borrowAmount,
159                    abi.encode(operation)
160                )
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160)


#

```
File: contracts/LeverageMacroBase.sol

228    stETH.transferShares(msg.sender, collateralBal)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L228)


#

```
File: contracts/LeverageMacroReference.sol

39    ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39)


#

```
File: contracts/LeverageMacroReference.sol

40    stETH.approve(_borrowerOperationsAddress, type(uint256).max)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L40)


#

```
File: contracts/LeverageMacroReference.sol

41    stETH.approve(_activePool, type(uint256).max)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L41)


#

```
File: contracts/LeverageMacroReference.sol

53    ebtcToken.approve(address(borrowerOperations), type(uint256).max)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)


#

```
File: contracts/LeverageMacroReference.sol

54    stETH.approve(address(borrowerOperations), type(uint256).max)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L54)


#

```
File: contracts/LeverageMacroReference.sol

55    stETH.approve(address(activePool), type(uint256).max)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L55)


#

```
File: contracts/ActivePool.sol

183    collateral.transferShares(_account, _shares)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L183](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L183)


#

```
File: contracts/ActivePool.sol

362    collateral.transferShares(feeRecipientAddress, _shares)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L362)


#

```
File: contracts/CollSurplusPool.sol

107    collateral.transferShares(_account, claimableColl)
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L107)


#

```
File: contracts/PriceFeed.sol

634    try ETH_BTC_CL_FEED.latestRoundData() returns (
635                uint80 roundId,
636                int256 answer,
637                uint256,
638                /* startedAt */
639                uint256 timestamp,
640                uint80 /* answeredInRound */
641            ) {
642                ethBtcAnswer = answer;
643                chainlinkResponse.roundEthBtcId = roundId;
644                chainlinkResponse.timestampEthBtc = timestamp;
645            } catch {
646                // If call to Chainlink aggregator reverts, return a zero response with success = false
647                return chainlinkResponse;
648            }
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634-L648](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L634-L648)


#

```
File: contracts/PriceFeed.sol

650    try STETH_ETH_CL_FEED.latestRoundData() returns (
651                uint80 roundId,
652                int256 answer,
653                uint256,
654                /* startedAt */
655                uint256 timestamp,
656                uint80 /* answeredInRound */
657            ) {
658                stEthEthAnswer = answer;
659                chainlinkResponse.roundStEthEthId = roundId;
660                chainlinkResponse.timestampStEthEth = timestamp;
661            } catch {
662                // If call to Chainlink aggregator reverts, return a zero response with success = false
663                return chainlinkResponse;
664            }
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650-L664](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L650-L664)


#

```
File: contracts/PriceFeed.sol

722    try ETH_BTC_CL_FEED.getRoundData(_currentRoundEthBtcId - 1) returns (
723                uint80 roundId,
724                int256 answer,
725                uint256,
726                /* startedAt */
727                uint256 timestamp,
728                uint80 /* answeredInRound */
729            ) {
730                ethBtcAnswer = answer;
731                prevChainlinkResponse.roundEthBtcId = roundId;
732                prevChainlinkResponse.timestampEthBtc = timestamp;
733            } catch {
734                // If call to Chainlink aggregator reverts, return a zero response with success = false
735                return prevChainlinkResponse;
736            }
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L722-L736](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L722-L736)


#

```
File: contracts/PriceFeed.sol

738    try STETH_ETH_CL_FEED.getRoundData(_currentRoundStEthEthId - 1) returns (
739                uint80 roundId,
740                int256 answer,
741                uint256,
742                /* startedAt */
743                uint256 timestamp,
744                uint80 /* answeredInRound */
745            ) {
746                stEthEthAnswer = answer;
747                prevChainlinkResponse.roundStEthEthId = roundId;
748                prevChainlinkResponse.timestampStEthEth = timestamp;
749            } catch {
750                // If call to Chainlink aggregator reverts, return a zero response with success = false
751                return prevChainlinkResponse;
752            }
```
 ignores return value 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L738-L752](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L738-L752)


</details>

# 


## Unused struct definition
- Severity: Non-Critical
- Confidence: High

### Description
There may be cases where a struct superficially appears to be used, but this is only because there are multiple definitions of the struct in different files. In such cases, the struct definition should be moved into a separate file. 

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

19    struct Role {
20            uint8 roleId;
21            string roleName;
22        }
```
 The struct `Role` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L19-L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L19-L22)


#

```
File: contracts/Governor.sol

24    struct Capability {
25            address target;
26            bytes4 functionSig;
27            uint8[] roles;
28        }
```
 The struct `Capability` is defined but never used:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L24-L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L24-L28)


</details>

# 


## Use bytes.concat() over abi.encodePacked() for clearer semantic meaning
- Severity: Non-Critical
- Confidence: High

### Description
Starting with Solidity version 0.8.4, bytes.concat() function allows concatenating bytes/strings, without extra padding. It has clearer semantic meaning than abi.encodePacked().

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

717    bytes32 digest = keccak256(
718                abi.encodePacked(
719                    "\x19\x01",
720                    domainSeparator(),
721                    keccak256(
722                        abi.encode(
723                            _PERMIT_POSITION_MANAGER_TYPEHASH,
724                            _borrower,
725                            _positionManager,
726                            _approval,
727                            _nonces[_borrower]++,
728                            _deadline
729                        )
730                    )
731                )
732            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717-L732](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717-L732)


#

```
File: contracts/EBTCToken.sol

209    bytes32 digest = keccak256(
210                abi.encodePacked(
211                    "\x19\x01",
212                    domainSeparator(),
213                    keccak256(
214                        abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
215                    )
216                )
217            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217)


</details>

# 


## Use Immutable for Constant Expressions
- Severity: Non-Critical
- Confidence: High

### Description
This detector checks for expressions for constant values such as a call to keccak256(), which should use 'immutable' rather than 'constant'. While it doesn't save any gas because the compiler knows that developers often make this mistake, it's still best to use the right tool for the task at hand. Constants should be used for literal values written into the code, and immutable variables should be used for expressions, or values calculated in, or passed into the constructor.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

32    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33            keccak256(
34                "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35)


#

```
File: contracts/LeverageMacroBase.sol

37    bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)


#

```
File: contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)


</details>

# 


## Conformance to Solidity local and state variable naming conventions
- Severity: Non-Critical
- Confidence: High

### Description
Solidity defines a [naming convention](https://solidity.readthedocs.io/en/v0.4.25/style-guide.html#local-and-state-variable-names) that should be followed for local and state variable names. According to the convention, variable names should be in mixedCase.

<details>

<summary>
There are 365 instances of this issue:

</summary>

###
#
Local variable 
```
File: contracts/ActivePool.sol

60    address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority())
```
 _authorityAddress is not in mixedCase

#
Local variable 
```
File: contracts/ActivePool.sol

410    uint256 _oldFee = feeBps
```
 _oldFee is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

123    address _authorityAddress = address(AuthNoOwner(_cdpManagerAddress).authority())
```
 _authorityAddress is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

338    address _borrower = sortedCdps.getOwnerAddress(_cdpId)
```
 _borrower is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

427    MoveTokensParams memory _varMvTokens = MoveTokensParams(
428                    msg.sender,
429                    vars.collSharesChange,
430                    (vars.isCollIncrease ? _stEthBalanceIncrease : 0),
431                    vars.isCollIncrease,
432                    _debtChange,
433                    _isDebtIncrease
434                )
```
 _varMvTokens is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

367    uint256 _cdpStEthBalance = collateral.getPooledEthByShares(vars.collShares)
```
 _cdpStEthBalance is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

513    bytes32 _cdpId = sortedCdps.insert(_borrower, vars.NICR, _upperHint, _lowerHint)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

466    uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD)
```
 _liquidatorRewardShares is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

465    uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance)
```
 _netCollAsShares is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

554    address _borrower = sortedCdps.getOwnerAddress(_cdpId)
```
 _borrower is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

968    PositionManagerApproval _approval = _getPositionManagerApproval(_borrower, msg.sender)
```
 _approval is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

1056    uint256 _systemCollShares = getSystemCollShares()
```
 _systemCollShares is not in mixedCase

#
Local variable 
```
File: contracts/BorrowerOperations.sol

1160    uint256 _oldFee = feeBps
```
 _oldFee is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

57    uint256 _newIndex
```
 _newIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

57    uint256 _oldIndex
```
 _oldIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

164    uint256 _liquidatorRewardShares = Cdps[_redeemColFromCdp.cdpId]
165                        .liquidatorRewardShares
```
 _liquidatorRewardShares is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

150    CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
151                Cdps[_redeemColFromCdp.cdpId].debt,
152                Cdps[_redeemColFromCdp.cdpId].coll
153            )
```
 _oldDebtAndColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

163    address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId)
```
 _borrower is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

383    uint256 _numCdpsFullyRedeemed
```
 _numCdpsFullyRedeemed is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

381    bytes32 _firstRedeemed = _cId
```
 _firstRedeemed is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

382    bytes32 _lastRedeemed = _cId
```
 _lastRedeemed is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

424    bytes32 _nextId = sortedCdps.getPrev(_cId)
```
 _nextId is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

395    SingleRedemptionInputs memory _redeemColFromCdp = SingleRedemptionInputs(
396                        _cId,
397                        totals.remainingDebtToRedeem,
398                        totals.price,
399                        _upperPartialRedemptionHint,
400                        _lowerPartialRedemptionHint,
401                        _partialRedemptionHintNICR
402                    )
```
 _redeemColFromCdp is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

361    bytes32 _cId = _firstRedemptionHint
```
 _cId is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

437    bytes32[] memory _toRemoveIds = _getCdpIdsToRemove(
438                    _lastRedeemed,
439                    _numCdpsFullyRedeemed,
440                    _firstRedeemed
441                )
```
 _toRemoveIds is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

495    bytes32 _id = _start
```
 _id is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

494    uint256 _cnt = _total
```
 _cnt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManager.sol

496    bytes32[] memory _toRemoveIds = new bytes32[](_total)
```
 _toRemoveIds is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

294    uint256 _totalStakesSnapshot = totalStakes
```
 _totalStakesSnapshot is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

297    uint256 _totalCollateralSnapshot = activePool.getSystemCollShares() - _collRemainder
```
 _totalCollateralSnapshot is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

337    uint256 _systemDebtRedistributionIndex = systemDebtRedistributionIndex
```
 _systemDebtRedistributionIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

356    uint256 _feeSplitDistributed
```
 _feeSplitDistributed is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

358    uint256 _debtIndexDelta
```
 _debtIndexDelta is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

355    uint256 _newDebt
```
 _newDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

351    uint256 _systemStEthFeePerUnitIndex = systemStEthFeePerUnitIndex
```
 _systemStEthFeePerUnitIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

354    uint256 _newColl
```
 _newColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

357    uint _pendingDebt
```
 _pendingDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

363    Cdp storage _cdp = Cdps[_cdpId]
```
 _cdp is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

350    uint256 _oldPerUnitCdp = cdpStEthFeePerUnitIndex[_cdpId]
```
 _oldPerUnitCdp is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

411    uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake
```
 _newTotalStakes is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

422    uint256 _newTotalStakes = totalStakes + newStake - oldStake
```
 _newTotalStakes is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

432    Cdp storage _cdp = Cdps[_cdpId]
```
 _cdp is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

494    uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares)
```
 _totalColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

514    uint256 _feeTaken
```
 _feeTaken is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

516    uint256 _perUnitError
```
 _perUnitError is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

510    uint256 _oldIndex
```
 _oldIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

515    uint256 _newFeePerUnit
```
 _newFeePerUnit is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

510    uint256 _newIndex
```
 _newIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

568    uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes)
```
 _perUnitError is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

564    uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION
```
 _feeTaken is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

567    uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes
```
 _deltaFeePerUnit is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

562    uint256 _cachedAllStakes = totalStakes
```
 _cachedAllStakes is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

565    uint256 _deltaFeeSplitShare = (_feeTaken * DECIMAL_PRECISION) +
566                systemStEthFeePerUnitIndexError
```
 _deltaFeeSplitShare is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

561    uint256 _deltaFeeSplit = deltaIndexFees * getSystemCollShares()
```
 _deltaFeeSplit is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

579    uint256 _oldPerUnit = systemStEthFeePerUnitIndex
```
 _oldPerUnit is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

631    uint256 _feeSplitDistributed = Cdps[_cdpId].stake *
632                (_systemStEthFeePerUnitIndex - _cdpStEthFeePerUnitIndex)
```
 _feeSplitDistributed is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

620    uint256 _cdpStEthFeePerUnitIndex = cdpStEthFeePerUnitIndex[_cdpId]
```
 _cdpStEthFeePerUnitIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

634    uint256 _scaledCdpColl = _cdpCol * DECIMAL_PRECISION
```
 _scaledCdpColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

621    uint256 _cdpCol = Cdps[_cdpId].coll
```
 _cdpCol is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

687    uint256 _newDebt
```
 _newDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

685    uint256 _newIndex
```
 _newIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

686    uint256 _newGlobalSplitIdx
```
 _newGlobalSplitIdx is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

687    uint256 _newColl
```
 _newColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

685    uint256 _oldIndex
```
 _oldIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

687    uint256 _pendingDebt
```
 _pendingDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

712    uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare)
```
 _underlyingCollateral is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

722    uint256 _pendingDebt
```
 _pendingDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

748    uint256 _newDebt
```
 _newDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

748    uint256 _newColl
```
 _newColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

769    uint256 _deltaFeePerUnit
```
 _deltaFeePerUnit is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

768    uint256 _feeTaken
```
 _feeTaken is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

774    uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit
```
 _newPerUnit is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

770    uint256 _perUnitError
```
 _perUnitError is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

807    uint256 _newDebt
```
 _newDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

798    uint256 _feeSplitDistributed
```
 _feeSplitDistributed is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

793    uint256 _newCollShare = Cdps[_cdpId].coll
```
 _newCollShare is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

809    uint256 _debtIndexDelta
```
 _debtIndexDelta is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

792    uint256 _feeSplitApplied
```
 _feeSplitApplied is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

799    uint256 _newCollShareAfter
```
 _newCollShareAfter is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

828    uint256 _newDebt = Cdps[_cdpId].debt
```
 _newDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

825    uint256 _debtIndexDelta
```
 _debtIndexDelta is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

840    uint256 _newDebt
```
 _newDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

849    uint256 _oldIndex
```
 _oldIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

851    uint256 _newColl
```
 _newColl is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

849    uint256 _newIndex
```
 _newIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

850    uint256 _newGlobalSplitIdx
```
 _newGlobalSplitIdx is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

866    uint256 _collShare = getSyncedCdpCollShares(_cdpId)
```
 _collShare is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

865    uint256 _debt = getSyncedCdpDebt(_cdpId)
```
 _debt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

875    uint256 _oldIndex
```
 _oldIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

882    uint256 _systemDebt = activePool.getSystemDebt()
```
 _systemDebt is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

878    uint256 _systemCollShare = activePool.getSystemCollShares()
```
 _systemCollShare is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

875    uint256 _newIndex
```
 _newIndex is not in mixedCase

#
Local variable 
```
File: contracts/CdpManagerStorage.sol

876    uint256 _feeTaken
```
 _feeTaken is not in mixedCase

#
Local variable 
```
File: contracts/CollSurplusPool.sol

54    address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority())
```
 _authorityAddress is not in mixedCase

#
Local variable 
```
File: contracts/Dependencies/EbtcBase.sol

89    uint256 _systemStEthBalance = collateral.getPooledEthByShares(systemCollShares)
```
 _systemStEthBalance is not in mixedCase

#
Local variable 
```
File: contracts/Dependencies/EbtcMath.sol

36    uint256 prod_xy = x * y
```
 prod_xy is not in mixedCase

#
Local variable 
```
File: contracts/Dependencies/TellorCaller.sol

45    bytes memory _value
```
 _value is not in mixedCase

#
Local variable 
```
File: contracts/Dependencies/TellorCaller.sol

45    bool _ifRetrieve
```
 _ifRetrieve is not in mixedCase

#
Local variable 
```
File: contracts/Dependencies/TellorCaller.sol

45    uint256 _timestampRetrieved
```
 _timestampRetrieved is not in mixedCase

#
Local variable 
```
File: contracts/Dependencies/TellorCaller.sol

49    uint256 _val = abi.decode(_value, (uint256))
```
 _val is not in mixedCase

#
Local variable 
```
File: contracts/EBTCDeployer.sol

92    bytes32 _salt = keccak256(abi.encodePacked(_saltString))
```
 _salt is not in mixedCase

#
Local variable 
```
File: contracts/EBTCDeployer.sol

102    bytes memory _data = abi.encodePacked(creationCode, constructionArgs)
```
 _data is not in mixedCase

#
Local variable 
```
File: contracts/EBTCDeployer.sol

114    bytes32 _salt = keccak256(abi.encodePacked(_saltString))
```
 _salt is not in mixedCase

#
Local variable 
```
File: contracts/FeeRecipient.sol

36    address _owner = owner()
```
 _owner is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

57    uint256 i = 0
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

48    bool _canCall = doesUserHaveRole(user, role)
```
 _canCall is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

59    bool _canCall = doesUserHaveRole(user, role)
```
 _canCall_scope_2 is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

56    address[] memory _usrs = users.values()
```
 _usrs is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

58    address user = _usrs[i]
```
 user_scope_1 is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

84    uint8 i = 0
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

108    bool roleEnabled = (uint256(byteMap >> i) & 1) != 0
```
 roleEnabled_scope_1 is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

107    uint8 i = 0
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

121    bytes32 _data
```
 _data is not in mixedCase

#
Local variable 
```
File: contracts/Governor.sol

134    bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values()
```
 _sigs is not in mixedCase

#
Local variable 
```
File: contracts/HintHelpers.sol

94    uint256 _cachedEbtcToRedeem = vars.remainingEbtcToRedeem
```
 _cachedEbtcToRedeem is not in mixedCase

#
Local variable 
```
File: contracts/HintHelpers.sol

148    uint256 _newCollShareAfter = newCollShare - collShareToReceive
```
 _newCollShareAfter is not in mixedCase

#
Local variable 
```
File: contracts/HintHelpers.sol

185    bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex)
```
 _cId is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroBase.sol

199    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 cdpInfo_scope_1 is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroBase.sol

187    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 cdpInfo_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroBase.sol

465    bytes32 _cdpId = borrowerOperations.openCdp(
466                flData.eBTCToMint,
467                flData._upperHint,
468                flData._lowerHint,
469                flData.stETHToDeposit
470            )
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroBase.sol

506    uint256 _toCopy
```
 _toCopy is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroBase.sol

508    bytes memory _returnData = new bytes(_maxCopy)
```
 _returnData is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroBase.sol

507    bool _success
```
 _success is not in mixedCase

#
Local variable 
```
File: contracts/LeverageMacroDelegateTarget.sol

64    address _owner = IOwnerLike(address(this)).owner()
```
 _owner is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

101    LiquidationLocals memory _liqState = LiquidationLocals(
102                _cdpId,
103                _partialAmount,
104                _price,
105                _ICR,
106                _upperPartialHint,
107                _lowerPartialHint,
108                (_recoveryModeAtStart),
109                _TCR,
110                0,
111                0,
112                0,
113                0,
114                0
115            )
```
 _liqState is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

100    bool _recoveryModeAtStart = _TCR < CCR ? true : false
```
 _recoveryModeAtStart is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

71    uint256 _price = priceFeed.fetchPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

117    LiquidationRecoveryModeLocals memory _rs = LiquidationRecoveryModeLocals(
118                systemDebt,
119                systemColl,
120                0,
121                0,
122                0,
123                _cdpId,
124                _price,
125                _ICR,
126                0,
127                0
128            )
```
 _rs is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

191    LiquidationRecoveryModeLocals
192                    memory _outputState = _liquidateIndividualCdpSetupCDPInRecoveryMode(_recoveryState)
```
 _outputState is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

210    LiquidationLocals memory _outputState = _liquidateIndividualCdpSetupCDPInNormalMode(
211                    _liqState
212                )
```
 _outputState_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

235    address _borrower = sortedCdps.getOwnerAddress(_liqState.cdpId)
```
 _borrower is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

228    uint256 _totalDebtToBurn
```
 _totalDebtToBurn is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

279    uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward)
```
 _cappedColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

234    uint256 _debtToRedistribute
```
 _debtToRedistribute is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

230    uint256 _liquidatorReward
```
 _liquidatorReward is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

278    uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price
```
 _debtToColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

232    uint256 _cappedColPortion
```
 _cappedColPortion is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

233    uint256 _collSurplus
```
 _collSurplus is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

229    uint256 _totalColToSend
```
 _totalColToSend is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

306    uint256 _cappedColPortion
```
 _cappedColPortion is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

365    uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price
```
 _debtToColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

300    uint256 _totalDebtToBurn
```
 _totalDebtToBurn is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

308    uint256 _debtToRedistribute
```
 _debtToRedistribute is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

302    uint256 _liquidatorReward
```
 _liquidatorReward is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

307    uint256 _collSurplus
```
 _collSurplus is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

366    uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward)
```
 _cappedColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

309    address _borrower = sortedCdps.getOwnerAddress(_recoveryState.cdpId)
```
 _borrower is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

301    uint256 _totalColToSend
```
 _totalColToSend is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

389    uint256 _liquidatorReward = Cdps[_cdpId].liquidatorRewardShares
```
 _liquidatorReward is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

435    uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price
```
 _debtToColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

400    bytes32 _cdpId = _partialState.cdpId
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

404    CdpDebtAndCollShares memory _debtAndColl = _getSyncedDebtAndCollShares(_cdpId)
```
 _debtAndColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

436    uint _cappedColl = collateral.getPooledEthByShares(_partialColl)
```
 _cappedColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

409    uint256 _partialColl
```
 _partialColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

401    uint256 _partialDebt = _partialState.partialAmount
```
 _partialDebt is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

457    uint256 _coll = _cdp.coll
```
 _coll is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

455    Cdp storage _cdp = Cdps[_cdpId]
```
 _cdp is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

458    uint256 _debt = _cdp.debt
```
 _debt is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

472    bytes32 _cdpId = _partialState.cdpId
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

550    uint256 _incentiveColl
```
 _incentiveColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

592    uint256 _debtToRepay = (_incentiveColl * _price) / LICR
```
 _debtToRepay is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

576    uint256 _incentiveColl
```
 _incentiveColl is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

614    LiquidationLocals memory _liqState = LiquidationLocals(
615                vars.cdpId,
616                0,
617                _price,
618                vars.ICR,
619                vars.cdpId,
620                vars.cdpId,
621                (false),
622                _TCR,
623                0,
624                0,
625                0,
626                0,
627                0
628            )
```
 _liqState is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

630    LiquidationLocals memory _outputState = _liquidateIndividualCdpSetupCDPInNormalMode(
631                _liqState
632            )
```
 _outputState is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

649    LiquidationRecoveryModeLocals memory _recState = LiquidationRecoveryModeLocals(
650                _systemDebt,
651                _systemCollShares,
652                0,
653                0,
654                0,
655                vars.cdpId,
656                _price,
657                vars.ICR,
658                0,
659                0
660            )
```
 _recState is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

662    LiquidationRecoveryModeLocals
663                memory _outputState = _liquidateIndividualCdpSetupCDPInRecoveryMode(_recState)
```
 _outputState is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

752    uint256 _start
```
 _start is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

751    bool[] memory _liqFlags = new bool[](_cnt)
```
 _liqFlags is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

750    uint256 _cnt = _cdpArray.length
```
 _cnt is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

814    uint256 _cnt = _cdpArray.length
```
 _cnt is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

815    uint256 _start
```
 _start is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

878    uint256 EBTCDebtNumerator = (_debt * DECIMAL_PRECISION) + lastEBTCDebtErrorRedistribution
```
 EBTCDebtNumerator is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

882    uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes
```
 EBTCDebtRewardPerUnitStaked is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationLibrary.sol

881    uint256 _totalStakes = totalStakes
```
 _totalStakes is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

38    uint256 _price = priceFeed.fetchPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

69    uint256 _j
```
 _j is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

66    uint256 _cnt
```
 _cnt is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

69    bytes32[] memory _returnedArray
```
 _returnedArray is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

95    bytes32 _cdpId = _last
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

98    bool _liquidatable = _checkICRAgainstLiqThreshold(
99                    cdpManager.getSyncedICR(_cdpId, _price),
100                    _TCR
101                )
```
 _liquidatable is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

94    bytes32 _first = sortedCdps.getFirst()
```
 _first is not in mixedCase

#
Local variable 
```
File: contracts/LiquidationSequencer.sol

93    bytes32 _last = sortedCdps.getLast()
```
 _last is not in mixedCase

#
Local variable 
```
File: contracts/MultiCdpGetter.sol

84    uint256 idx = 0
```
 idx_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/MultiCdpGetter.sol

120    uint256 idx = 0
```
 idx_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

384    address oldFallbackCaller = address(fallbackCaller)
```
 oldFallbackCaller_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

623    uint8 decimals
```
 decimals_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

651    uint80 roundId
```
 roundId_scope_1 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

652    int256 answer
```
 answer_scope_2 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

655    uint256 timestamp
```
 timestamp_scope_3 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

739    uint80 roundId
```
 roundId_scope_1 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

740    int256 answer
```
 answer_scope_2 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

743    uint256 timestamp
```
 timestamp_scope_3 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

711    uint8 decimals
```
 decimals_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

794    uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals
795                ? _stEthEthDecimals
796                : _ethBtcDecimals
```
 _decimalDenominator is not in mixedCase

#
Local variable 
```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
 _scaledDecimal is not in mixedCase

#
Local variable 
```
File: contracts/Proxy/BorrowerWrappersScript.sol

118    uint256 EBTCAmount = _collateral.mul(price).div(ICR)
```
 EBTCAmount is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

124    uint256 _tmp = uint256(cdpId) >> ADDRESS_SHIFT
```
 _tmp is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

144    bytes32 _cdpId
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

181    bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId)
```
 _currentCdpId is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

182    uint _currentIndex = 0
```
 _currentIndex is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

217    uint256 _cnt
```
 _cnt is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

245    uint _ownedCount = 0
```
 _ownedCount is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

244    bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId)
```
 _currentCdpId is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

273    uint _ownedCount
```
 _ownedCount is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

275    bytes32[] memory _allCdps
```
 _allCdps is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

293    uint _ownedCount
```
 _ownedCount is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

316    bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId)
```
 _currentCdpId is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

312    uint _cdpRetrieved
```
 _cdpRetrieved is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

351    bytes32 _id = toCdpId(owner, block.number, nextCdpNonce)
```
 _id is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

425    bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId
```
 _lastNext is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

449    uint i = 0
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

421    uint256 _len = _ids.length
```
 _len is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

424    bytes32 _firstPrev = data.nodes[_ids[0]].prevId
```
 _firstPrev is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

522    Node memory _node = data.nodes[_id]
```
 _node is not in mixedCase

#
Local variable 
```
File: contracts/SortedCdps.sol

520    bool _exist = _id != dummyId && (data.head == _id || data.tail == _id)
```
 _exist is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

37    uint256 _price = priceFeed.fetchPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

50    bool _recoveryModeAtStart = _TCR < CCR ? true : false
```
 _recoveryModeAtStart is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

67    bytes32 _cdpId = _last
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

76    bool _liquidatable = _canLiquidateInCurrentMode(_recoveryModeAtStart, _icr, _TCR)
```
 _liquidatable is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

90    bool _liquidatable = _canLiquidateInCurrentMode(_recoveryModeAtStart, _icr, _TCR)
```
 _liquidatable_scope_3 is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

65    bytes32 _last = sortedCdps.getLast()
```
 _last is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

74    uint256 _icr = cdpManager.getSyncedICR(_cdpId, _price)
```
 _icr is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

88    uint256 _icr = cdpManager.getSyncedICR(_cdpId, _price)
```
 _icr_scope_1 is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

87    uint256 i = 0
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

72    uint256 _cnt
```
 _cnt is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

66    bytes32 _first = sortedCdps.getFirst()
```
 _first is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

75    uint256 _cdpStatus = cdpManager.getCdpStatus(_cdpId)
```
 _cdpStatus is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

89    uint256 _cdpStatus = cdpManager.getCdpStatus(_cdpId)
```
 _cdpStatus_scope_2 is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

86    uint256 _j
```
 _j is not in mixedCase

#
Local variable 
```
File: contracts/SyncedLiquidationSequencer.sol

113    bool _liquidatable = _recovery ? (_icr < MCR || _icr < _TCR) : _icr < MCR
```
 _liquidatable is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CDPManagerTester.sol

55    uint256 _tcr = _getCachedTCR(_price)
```
 _tcr is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CDPManagerTester.sol

61    uint256 _splitIndex = (_currentIndex * MAX_REWARD_SPLIT) / _stakingRewardSplit
```
 _splitIndex is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CDPManagerTester.sol

88    uint256 _mulFactor = EbtcMath._decPow(minuteDecayFactor, minutesPassed)
```
 _mulFactor is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CDPManagerTester.sol

109    uint256 _totalEBTCSupply = _getSystemDebt()
```
 _totalEBTCSupply is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

47    uint256 _share = getSharesByPooledEth(msg.value)
```
 _share is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

64    uint256 _share = getSharesByPooledEth(ethToDeposit)
```
 _share is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

71    uint256 _share = getSharesByPooledEth(wad)
```
 _share is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

80    uint _tmp = _mul(_ethPerShare, _totalBalance)
```
 _tmp is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

127    uint256 _share = getSharesByPooledEth(wad)
```
 _share is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

153    uint256 _tmp = _mul(1e18, _ethAmount)
```
 _tmp is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

158    uint256 _tmp = _mul(_ethPerShare, _sharesAmount)
```
 _tmp is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

166    uint256 _tknAmt = getPooledEthByShares(_sharesAmount)
```
 _tknAmt is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

213    uint256 _tmp = _mul(_ethPerShare, balances[_usr])
```
 _tmp is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/Mock1Inch.sol

36    uint256 amt = (amountIn * 1e18) / price
```
 amt_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/MultipleCdpsTester.sol

48    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), _idx)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/MultipleCdpsTester.sol

40    uint256 _singleCol = msg.value / _count
```
 _singleCol is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/MultipleCdpsTester.sol

38    uint256 _idx
```
 _idx is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/Pretty.sol

13    string memory _tmpValue = new string(_baseBytes.length + _valueBytes.length)
```
 _tmpValue is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/Pretty.sol

11    bytes memory _valueBytes = bytes(_value)
```
 _valueBytes is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/Pretty.sol

14    bytes memory _newValue = bytes(_tmpValue)
```
 _newValue is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/Pretty.sol

10    bytes memory _baseBytes = bytes(_base)
```
 _baseBytes is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/SimpleLiquidatorTester.sol

64    uint256 _ppfs = abi.decode(data, (uint256))
```
 _ppfs is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/StETHMock.sol

343    uint256 _sharesToTransfer = getSharesByPooledEth(_amount)
```
 _sharesToTransfer is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Actor.sol

53    address[] memory _targets
```
 _targets is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Actor.sol

57    uint256 i = 0
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Actor.sol

53    bytes[] memory _calldatas
```
 _calldatas is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Asserts.sol

51    uint i = 4
```
 i_scope_0 is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

49    uint256 _cdpCount = cdpManager.getActiveCdpsCount()
```
 _cdpCount is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

56    uint256 _diff = _sum > _activeColl ? (_sum - _activeColl) : (_activeColl - _sum)
```
 _diff is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

52    uint256 _coll
```
 _coll is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

55    uint256 _activeColl = activePool.getSystemCollShares()
```
 _activeColl is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

50    uint256 _sum
```
 _sum is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

67    uint256 _debt
```
 _debt is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

64    uint256 _cdpCount = cdpManager.getActiveCdpsCount()
```
 _cdpCount is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

65    uint256 _sum
```
 _sum is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

86    uint256 _cdpCount = cdpManager.getActiveCdpsCount()
```
 _cdpCount is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

87    uint256 _sum
```
 _sum is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

95    uint256 _cdpCount = cdpManager.getActiveCdpsCount()
```
 _cdpCount is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

160    bytes32 _first = sortedCdps.getFirst()
```
 _first is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

162    uint256 _firstICR = cdpManager.getCachedICR(_first, _price)
```
 _firstICR is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

161    uint256 _price = priceFeedMock.getPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

182    uint256 _price = priceFeedMock.getPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/Properties.sol

369    uint256 _price = priceFeedMock.getPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetContractSetup.sol

387    uint256 _EBTCAmount = (_col * price) / cdpManager.CCR()
```
 _EBTCAmount is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetContractSetup.sol

384    uint256 _col = INITIAL_COLL_BALANCE / 2
```
 _col is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

44    uint256 _price = priceFeedMock.getPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

62    uint256 _price = priceFeedMock.getPrice()
```
 _price is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

91    uint _cdpIdx = _i % cdpManager.getActiveCdpsCount()
```
 _cdpIdx is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

101    uint256 _n = between(value, 1, cdpManager.getActiveCdpsCount())
```
 _n is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

98    uint256 _actions = between(value, 1, MAX_FLASHLOAN_ACTIONS)
```
 _actions is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

110    bytes[] memory _calldatas = new bytes[](_actions)
```
 _calldatas is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

100    uint256 _col = between(value, 1, cdpManager.getSystemCollShares() / 2)
```
 _col is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

106    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

109    address[] memory _targets = new address[](_actions)
```
 _targets is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

113    bytes[] memory _allCalldatas = new bytes[](6)
```
 _allCalldatas is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

163    uint256 _j = 0
```
 _j is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

99    uint256 _EBTCAmount = between(value, 1, eBTCToken.totalSupply() / 2)
```
 _EBTCAmount is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

105    uint256 _i = between(value, 0, numberOfCdps - 1)
```
 _i is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

112    address[] memory _allTargets = new address[](6)
```
 _allTargets is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

175    bytes32 _cId = sortedCdps.getLast()
```
 _cId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

213    bytes32 _cdpId = _getRandomCdp(_i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

283    bytes32 _cdpId = _getRandomCdp(_i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

456    bytes32 _cdpId = _getFirstCdpWithIcrGteMcr()
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

551    uint _balAfter = collateral.balanceOf(activePool.feeRecipientAddress())
```
 _balAfter is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

530    uint _fee = activePool.flashFee(address(collateral), _amount)
```
 _fee is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

535    uint _balBefore = collateral.balanceOf(activePool.feeRecipientAddress())
```
 _balBefore is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

611    uint _balAfter = eBTCToken.balanceOf(borrowerOperations.feeRecipientAddress())
```
 _balAfter is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

589    uint _fee = borrowerOperations.flashFee(address(eBTCToken), _amount)
```
 _fee is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

594    uint _balBefore = eBTCToken.balanceOf(borrowerOperations.feeRecipientAddress())
```
 _balBefore is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

735    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

839    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

913    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

984    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

1058    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: contracts/TestContracts/invariants/TargetFunctions.sol

1143    bytes32 _cdpId = sortedCdps.cdpOfOwnerByIndex(address(actor), _i)
```
 _cdpId is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

67    uint256 balance_sender = token.balanceOf(msg.sender)
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

84    uint256 balance_sender = token.balanceOf(msg.sender)
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

106    uint256 balance_sender = token.balanceOf(address(this))
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

123    uint256 balance_receiver = token.balanceOf(target)
```
 balance_receiver is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

122    uint256 balance_sender = token.balanceOf(msg.sender)
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

146    uint256 balance_sender = token.balanceOf(address(this))
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

147    uint256 balance_receiver = token.balanceOf(target)
```
 balance_receiver is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

169    uint256 balance_sender = token.balanceOf(address(this))
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

170    uint256 balance_receiver = token.balanceOf(target)
```
 balance_receiver is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

190    uint256 balance_receiver = token.balanceOf(target)
```
 balance_receiver is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

189    uint256 balance_sender = token.balanceOf(msg.sender)
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

215    uint256 balance_receiver = token.balanceOf(target)
```
 balance_receiver is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

217    uint256 transfer_value = (amount % balance_sender) + 1
```
 transfer_value is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

214    uint256 balance_sender = token.balanceOf(address(this))
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

241    uint256 balance_receiver = token.balanceOf(target)
```
 balance_receiver is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

240    uint256 balance_sender = token.balanceOf(msg.sender)
```
 balance_sender is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

244    uint256 transfer_value = (amount % balance_sender) + 1
```
 transfer_value is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

304    uint256 current_allowance = token.allowance(msg.sender, address(this))
```
 current_allowance is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

306    uint256 transfer_value = (amount % balance_sender) + 1
```
 transfer_value is not in mixedCase

#
Local variable 
```
File: node_modules/@crytic/properties/contracts/ERC20/external/properties/ERC20ExternalBasicProperties.sol

303    uint256 balance_sender = token.balanceOf(msg.sender)
```
 balance_sender is not in mixedCase

#
Variable 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```
 Cdps is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/CdpManagerStorage.sol

205    bytes32[] public CdpIds
```
 CdpIds is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/Dependencies/AuthNoOwner.sol

13    Authority private _authority
```
 _authority is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/Dependencies/AuthNoOwner.sol

14    bool private _authorityInitialized
```
 _authorityInitialized is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/Dependencies/Ownable.sol

21    address private _owner
```
 _owner is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/Dependencies/PermitNonce.sol

10    mapping(address => uint256) internal _nonces
```
 _nonces is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/EBTCToken.sol

27    uint256 private _totalSupply
```
 _totalSupply is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/EBTCToken.sol

51    mapping(address => uint256) private _balances
```
 _balances is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/EBTCToken.sol

52    mapping(address => mapping(address => uint256)) private _allowances
```
 _allowances is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/Migrations.sol

7    uint256 public last_completed_migration
```
 last_completed_migration is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/Proxy/LQTYStakingScript.sol

8    IFeeRecipient FeeRecipient
```
 FeeRecipient is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/BaseStorageVariables.sol

57    uint internal constant diff_tolerance = 0.000000000002e18
```
 diff_tolerance is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

35    uint256 private _ethPerShare = 1e18
```
 _ethPerShare is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/CollateralTokenTester.sol

36    uint256 private _totalBalance
```
 _totalBalance is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

27    bytes public authority_creationCode = type(Governor).creationCode
```
 authority_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

28    bytes public liquidationLibrary_creationCode = type(LiquidationLibrary).creationCode
```
 liquidationLibrary_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

30    bytes public cdpManager_creationCode = type(CdpManager).creationCode
```
 cdpManager_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

31    bytes public borrowerOperations_creationCode = type(BorrowerOperations).creationCode
```
 borrowerOperations_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

32    bytes public sortedCdps_creationCode = type(SortedCdps).creationCode
```
 sortedCdps_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

33    bytes public activePool_creationCode = type(ActivePool).creationCode
```
 activePool_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

34    bytes public collSurplusPool_creationCode = type(CollSurplusPool).creationCode
```
 collSurplusPool_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

35    bytes public hintHelpers_creationCode = type(HintHelpers).creationCode
```
 hintHelpers_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

36    bytes public ebtcToken_creationCode = type(EBTCToken).creationCode
```
 ebtcToken_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

37    bytes public feeRecipient_creationCode = type(FeeRecipient).creationCode
```
 feeRecipient_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

38    bytes public multiCdpGetter_creationCode = type(MultiCdpGetter).creationCode
```
 multiCdpGetter_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

41    bytes public cdpManagerTester_creationCode = type(CdpManagerTester).creationCode
```
 cdpManagerTester_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

42    bytes public borrowerOperationsTester_creationCode = type(BorrowerOperationsTester).creationCode
```
 borrowerOperationsTester_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

43    bytes public priceFeedTestnet_creationCode = type(PriceFeedTestnet).creationCode
```
 priceFeedTestnet_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

44    bytes public activePoolTester_creationCode = type(ActivePoolTester).creationCode
```
 activePoolTester_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/EBTCDeployerTester.sol

45    bytes public ebtcTokenTester_creationCode = type(EBTCTokenTester).creationCode
```
 ebtcTokenTester_creationCode is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/MockFallbackCaller.sol

8    uint256 public _answer
```
 _answer is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/MockFallbackCaller.sol

9    uint256 public _timestampRetrieved
```
 _timestampRetrieved is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/MockFallbackCaller.sol

10    uint256 public _fallbackTimeout
```
 _fallbackTimeout is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/MockFallbackCaller.sol

11    bool public _success
```
 _success is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/MultipleCdpsTester.sol

21    bytes32 _dummyId
```
 _dummyId is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/SimpleLiquidatorTester.sol

16    uint256 public _onReceiveType
```
 _onReceiveType is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/SimpleLiquidatorTester.sol

17    ICdpManager public _cdpManager
```
 _cdpManager is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/SimpleLiquidatorTester.sol

18    bytes32 public _reEnterLiqCdpId = bytes32(0)
```
 _reEnterLiqCdpId is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/testnet/PriceFeedTestnet.sol

18    uint256 private _price = 7428 * 1e13
```
 _price is single letter l, O, or I, which should not be used

#
Variable 
```
File: contracts/TestContracts/testnet/PriceFeedTestnet.sol

19    bool public _useFallback
```
 _useFallback is single letter l, O, or I, which should not be used

</details>

# 


## Whitespace in Expressions
- Severity: Non-Critical
- Confidence: High

### Description
Detects when whitespace usage in expressions does not conform to the Solidity style guide.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```

```
// @audit: whitespace inside parenthesis
Line: 648            (, uint256 _newGlobalSplitIdx, ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);


// @audit: whitespace inside parenthesis
Line: 649            (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(


// @audit: whitespace inside parenthesis
Line: 684            (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);


// @audit: whitespace inside parenthesis
Line: 710            (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(


// @audit: whitespace inside parenthesis
Line: 802            (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);


// @audit: whitespace inside parenthesis
Line: 812            (, uint256 _newGlobalSplitIdx, ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);


// @audit: whitespace inside parenthesis
Line: 813            (uint256 _newColl, , , , ) = _calcSyncedAccounting(


// @audit: whitespace inside parenthesis
Line: 838            (uint256 _feeTaken, , ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);


```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#

```
File: contracts/LeverageMacroBase.sol

26    contract LeverageMacroBase 
```

```
// @audit: whitespace inside parenthesis
Line: 366            for (uint256 i; i < swapLength; ) {


// @audit: whitespace inside parenthesis
Line: 395            (bool success, ) = excessivelySafeCall(


```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26-L535)


#

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```

```
// @audit: whitespace inside parenthesis
Line: 409            (uint256 _partialColl, uint256 newColl, ) = _calculatePartialLiquidationSurplusAndCap(


// @audit: whitespace before a semicolon
Line: 750            for (vars.i = _start; ; ) {


// @audit: whitespace before a semicolon
Line: 813            for (vars.i = _start; ; ) {


```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#

```
File: contracts/SimplifiedDiamondLike.sol

25    contract SimplifiedDiamondLike 
```

```
// @audit: whitespace inside parenthesis
Line: 114            for (uint256 i; i < length; ) {


```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202)


#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```

```
// @audit: whitespace inside parenthesis
Line: 144            (bytes32 _cdpId, ) = _cdpOfOwnerByIndex(owner, index, dummyId, 0);


// @audit: whitespace inside parenthesis
Line: 217            (uint256 _cnt, ) = _cdpCountOf(owner, dummyId, 0);


// @audit: whitespace inside parenthesis
Line: 273            (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);


// @audit: whitespace inside parenthesis
Line: 275                (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);


// @audit: whitespace inside parenthesis
Line: 293            (uint _ownedCount, ) = _cdpCountOf(owner, startNodeId, maxNodes);


```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Use of 0 as a function argument
- Severity: Non-Critical
- Confidence: High

### Description
Using 0 directly as an argument in function calls may be error-prone and does not fully describe the caller's intention. Consider using descriptive constants or an enum instead.

<details>

<summary>
There are 14 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

209    _adjustCdpInternal(_cdpId, 0, 0, false, _upperHint, _lowerHint, _stEthBalanceIncrease)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L209](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L209)


#

```
File: contracts/BorrowerOperations.sol

225    _adjustCdpInternal(_cdpId, _stEthBalanceDecrease, 0, false, _upperHint, _lowerHint, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L225](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L225)


#

```
File: contracts/BorrowerOperations.sol

241    _adjustCdpInternal(_cdpId, 0, _debt, true, _upperHint, _lowerHint, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L241](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L241)


#

```
File: contracts/BorrowerOperations.sol

256    _adjustCdpInternal(_cdpId, 0, _debt, false, _upperHint, _lowerHint, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L256)


#

```
File: contracts/BorrowerOperations.sol

278    _adjustCdpInternal(
279                _cdpId,
280                _stEthBalanceDecrease,
281                _debtChange,
282                _isDebtIncrease,
283                _upperHint,
284                _lowerHint,
285                0
286            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L278-L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L278-L286)


#

```
File: contracts/CdpManager.sol

171    _closeCdpByRedemption(
172                        _redeemColFromCdp.cdpId,
173                        0,
174                        newColl,
175                        _liquidatorRewardShares,
176                        _borrower
177                    )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L171-L177](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L171-L177)


#

```
File: contracts/CdpManagerStorage.sol

519    _updateSystemSnapshotsExcludeCollRemainder(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L519](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L519)


#

```
File: contracts/LeverageMacroBase.sol

414    (bool success, ) = excessivelySafeCall(
415                swapData.addressForSwap,
416                gasleft(),
417                0,
418                0,
419                swapData.calldataForSwap
420            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L414-L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L414-L420)


#

```
File: contracts/LeverageMacroBase.sol

427    IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)


#

```
File: contracts/LiquidationLibrary.sol

41    _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L41)


#

```
File: contracts/SortedCdps.sol

144    (bytes32 _cdpId, ) = _cdpOfOwnerByIndex(owner, index, dummyId, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L144)


#

```
File: contracts/SortedCdps.sol

217    (uint256 _cnt, ) = _cdpCountOf(owner, dummyId, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L217)


#

```
File: contracts/SortedCdps.sol

273    (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L273](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L273)


#

```
File: contracts/SortedCdps.sol

275    (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L275](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L275)


</details>

# 