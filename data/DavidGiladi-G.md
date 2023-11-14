
### Gas Optimization Issues
|Title|Issue|Instances|Total Gas Saved|
|-|:-|:-:|:-:|
|[G-1] Inefficient use of abi.encode() | [Inefficient use of abi.encode()](#inefficient-use-of-abiencode) | 6 | 600 |
|[G-2] Use assembly to emit events | [Use assembly to emit events](#use-assembly-to-emit-events) | 78 | 2964 |
|[G-3] Avoid unnecessary storage updates | [Avoid unnecessary storage updates](#avoid-unnecessary-storage-updates) | 5 | 4000 |
|[G-4] Multiplication and Division by 2 Should use in Bit Shifting | [Multiplication and Division by 2 Should use in Bit Shifting](#multiplication-and-division-by-2-should-use-in-bit-shifting) | 1 | 20 |
|[G-5] Using bools for storage incurs overhead | [Using bools for storage incurs overhead](#using-bools-for-storage-incurs-overhead) | 2 | 34200 |
|[G-6] Optimizing Small Data Storage with Bytes32 | [Optimizing Small Data Storage with Bytes32](#optimizing-small-data-storage-with-bytes32) | 11 | 4158 |
|[G-7] Check Arguments Early | [Check Arguments Early](#check-arguments-early) | 4 | - |
|[G-8] Division operations between unsigned could be unchecked | [Division operations between unsigned could be unchecked](#division-operations-between-unsigned-could-be-unchecked) | 3 | 255 |
|[G-9] Modulus operations that could be unchecked | [Modulus operations that could be unchecked](#modulus-operations-that-could-be-unchecked) | 1 | 85 |
|[G-10] Potential Optimization by Combining Multiple Mappings into a Struct | [Potential Optimization by Combining Multiple Mappings into a Struct](#potential-optimization-by-combining-multiple-mappings-into-a-struct) | 2 | 1000 |
|[G-11] Constants Variable Should Be Private for Gas Optimization | [Constants Variable Should Be Private for Gas Optimization](#constants-variable-should-be-private-for-gas-optimization) | 18 | 61200 |
|[G-12] State variables that could be declared constant | [State variables that could be declared constant](#state-variables-that-could-be-declared-constant) | 10 | 20970 |
|[G-13] Use of emit inside a loop | [Use of emit inside a loop](#use-of-emit-inside-a-loop) | 5 | 5130 |
|[G-14] Empty Block | [Empty Block](#empty-block) | 2 | - |
|[G-15] Identical Deployments Should be Replaced with Clone | [Identical Deployments Should be Replaced with Clone](#identical-deployments-should-be-replaced-with-clone) | 1 | - |
|[G-16] Use a More Recent Version of Solidity | [Use a More Recent Version of Solidity](#use-a-more-recent-version-of-solidity) | 34 | - |
|[G-17] Inefficient assignments to state variables | [Inefficient assignments to state variables](#inefficient-assignments-to-state-variables) | 1 | 113 |
|[G-18] Greater or Equal Comparison Costs Less Gas than Greater Comparison | [Greater or Equal Comparison Costs Less Gas than Greater Comparison](#greater-or-equal-comparison-costs-less-gas-than-greater-comparison) | 9 | 27 |
|[G-19] Inefficient Parameter Storage | [Inefficient Parameter Storage](#inefficient-parameter-storage) | 35 | 1750 |
|[G-20] Using Storage Instead of Memory for structs/arrays Saves Gas | [Using Storage Instead of Memory for structs/arrays Saves Gas](#using-storage-instead-of-memory-for-structsarrays-saves-gas) | 7 | 29400 |
|[G-21] Internal or Private Function that Called Once Should Be Inlined to Save Gas | [Internal or Private Function that Called Once Should Be Inlined to Save Gas](#internal-or-private-function-that-called-once-should-be-inlined-to-save-gas) | 19 | 380 |
|[G-22] Inefficient Gas Usage in Solidity Smart Contracts Due to Long Error Messages | [Inefficient Gas Usage in Solidity Smart Contracts Due to Long Error Messages](#inefficient-gas-usage-in-solidity-smart-contracts-due-to-long-error-messages) | 111 | 1998 |
|[G-23] Consider Merge Sequential For-Loops | [Consider Merge Sequential For-Loops](#consider-merge-sequential-for-loops) | 1 | - |
|[G-24] Declare Constructor Function as Payable to Save Gas | [Declare Constructor Function as Payable to Save Gas](#declare-constructor-function-as-payable-to-save-gas) | 16 | 336 |
|[G-25] Optimize address(0) Checks Using Assembly | [Optimize address(0) Checks Using Assembly](#optimize-address0-checks-using-assembly) | 6 | 348 |
|[G-26] Optimize Names to Save Gas | [Optimize Names to Save Gas](#optimize-names-to-save-gas) | 8 | 176 |
|[G-27] Optimal State Variable Order | [Optimal State Variable Order](#optimal-state-variable-order) | 3 | 15000 |
|[G-28] Optimal Struct Variable Order | [Optimal Struct Variable Order](#optimal-struct-variable-order) | 4 | 20000 |
|[G-29] Postfix operations that could be replaced with prefix operations | [Postfix operations that could be replaced with prefix operations](#Postfix-operations-that-could-be-replaced-with-prefix-operations) | 12 | 60 |
|[G-30] Redundant Bool Comparison | [Redundant Bool Comparison](#redundant-bool-comparison) | 1 | 9 |
|[G-31] Redundant state variable getters | [Redundant state variable getters](#redundant-state-variable-getters) | 2 | - |
|[G-32] Consider activating via-ir for deploying | [Consider activating via-ir for deploying](#consider-activating-via-ir-for-deploying) | 1 | - |
|[G-33] Short-circuit rules can be used to optimize some gas usage | [Short-circuit rules can be used to optimize some gas usage](#short-circuit-rules-can-be-used-to-optimize-some-gas-usage) | 7 | 14700 |
|[G-34] Use Small Integer For Efficiency | [Use Small Integer For Efficiency](#use-small-integer-for-efficiency) | 5 | 30 |
|[G-35] Splitting Require Assert Statements | [Splitting Require Assert Statements](#splitting-require-assert-statements) | 8 | 24 |
|[G-36] State variable access within a loop | [State variable access within a loop](#state-variable-access-within-a-loop) | 33 | 8745 |
|[G-37] Superfluous event fields | [Superfluous event fields](#superfluous-event-fields) | 1 | - |
|[G-38] Cache Array Length Outside of Loop | [Cache Array Length Outside of Loop](#cache-array-length-outside-of-loop) | 3 | 9 |
|[G-39] State variables should be cached in stack variables rather than re-reading them from storage | [State variables should be cached in stack variables rather than re-reading them from storage](#state-variables-should-be-cached-in-stack-variables-rather-than-re-reading-them-from-storage) | 29 | 2813 |
|[G-40] Safe Subtraction Should Be Unchecked | [Safe Subtraction Should Be Unchecked](#safe-subtraction-should-be-unchecked) | 11 | 935 |
|[G-41] Detection of Unnecessary Checked Increments in Solidity Loop Statements | [Detection of Unnecessary Checked Increments in Solidity Loop Statements](#detection-of-unnecessary-checked-increments-in-solidity-loop-statements) | 10 | 600 |
|[G-42] Avoid Unnecessary Computation Inside Loops | [Avoid Unnecessary Computation Inside Loops](#avoid-unnecessary-computation-inside-loops) | 3 | - |
|[G-43] Redundant Contract Existence Check in Consecutive External Calls | [Redundant Contract Existence Check in Consecutive External Calls](#redundant-contract-existence-check-in-consecutive-external-calls) | 8 | 800 |
|[G-44] Initialize Variables With Default Value | [Initialize Variables With Default Value](#initialize-variables-with-default-value) | 17 | 102 |
|[G-45] Unused Named Return Variables | [Unused Named Return Variables](#unused-named-return-variables) | 4 | - |
|[G-46] Use assembly to write address storage values | [Use assembly to write address storage values](#use-assembly-to-write-address-storage-values) | 24 | 1848 |
|[G-47] Use Assembly for Hash Calculation | [Use Assembly for Hash Calculation](#use-assembly-for-hash-calculation) | 12 | 960 |
|[G-48] Usage of Custom Errors for Gas Efficiency | [Usage of Custom Errors for Gas Efficiency](#usage-of-custom-errors-for-gas-efficiency) | 152 | 41952 |

Total: 746 instances over 48 issues



## Inefficient use of abi.encode()
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 600

### Description
The `abi.encode()` function is less gas efficient than `abi.encodePacked()`, especially when encoding only static types. This detector identifies instances where `abi.encode()` is used and all arguments are static, suggesting that `abi.encodePacked()` could potentially be used instead for better gas efficiency. Note: `abi.encodePacked()` should not be used if any of the arguments are dynamic types, as it could lead to hash collisions.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

682    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682)


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
 use  abi.encodepacked() instead.

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
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209-L217)


#

```
File: contracts/EBTCToken.sol

240    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)


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
 use  abi.encodepacked() instead.

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
 use  abi.encodepacked() instead.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155-L160)


</details>

# 


## Use assembly to emit events
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 2964

### Description
This detector checks for instances where a contract uses assembly code to emit events. While it's technically possible to emit events using inline assembly in Solidity, it's generally discouraged due to readability concerns and potential for errors. Events should usually be emitted using higher-level Solidity constructs.

<details>

<summary>
There are 78 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

65    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65)


#

```
File: contracts/ActivePool.sol

112    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112)


#

```
File: contracts/ActivePool.sol

113    emit CollSharesTransferred(_account, _shares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L113)


#

```
File: contracts/ActivePool.sol

145    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145)


#

```
File: contracts/ActivePool.sol

146    emit CollSharesTransferred(_account, totalShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L146)


#

```
File: contracts/ActivePool.sol

173    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173)


#

```
File: contracts/ActivePool.sol

174    emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174)


#

```
File: contracts/ActivePool.sol

200    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200)


#

```
File: contracts/ActivePool.sol

213    emit ActivePoolEBTCDebtUpdated(cachedSystemDebt)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213)


#

```
File: contracts/ActivePool.sol

247    emit SystemCollSharesUpdated(cachedSystemCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247)


#

```
File: contracts/ActivePool.sol

307    emit FlashLoanSuccess(address(receiver), token, amount, fee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307)


#

```
File: contracts/ActivePool.sol

360    emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360)


#

```
File: contracts/ActivePool.sol

383    emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383)


#

```
File: contracts/ActivePool.sol

399    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399)


#

```
File: contracts/ActivePool.sol

412    emit FlashFeeSet(msg.sender, _oldFee, _newFee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L412)


#

```
File: contracts/ActivePool.sol

421    emit FlashLoansPaused(msg.sender, _paused)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421)


#

```
File: contracts/BorrowerOperations.sol

136    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136)


#

```
File: contracts/BorrowerOperations.sol

641    emit PositionManagerApprovalSet(_borrower, _positionManager, _approval)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641)


#

```
File: contracts/BorrowerOperations.sol

1105    emit FlashLoanSuccess(address(receiver), token, amount, fee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105)


#

```
File: contracts/BorrowerOperations.sol

1149    emit FeeRecipientAddressChanged(_feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149)


#

```
File: contracts/BorrowerOperations.sol

1162    emit FlashFeeSet(msg.sender, _oldFee, _newFee)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1162)


#

```
File: contracts/BorrowerOperations.sol

1171    emit FlashLoansPaused(msg.sender, _paused)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171)


#

```
File: contracts/CdpManager.sol

55    emit StakingRewardSplitSet(stakingRewardSplit)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55)


#

```
File: contracts/CdpManagerStorage.sol

542    emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542)


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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L179-L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L179-L189)


#

```
File: contracts/CdpManagerStorage.sol

481    emit CdpArrayIndexUpdated(idToMove, index)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481)


#

```
File: contracts/CdpManagerStorage.sol

414    emit TotalStakesUpdated(_newTotalStakes)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414)


#

```
File: contracts/CdpManagerStorage.sol

425    emit TotalStakesUpdated(_newTotalStakes)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425)


#

```
File: contracts/CdpManager.sol

630    emit BaseRateUpdated(newBaseRate)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630)


#

```
File: contracts/CdpManager.sol

698    emit LastRedemptionTimestampUpdated(block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698)


#

```
File: contracts/CdpManagerStorage.sol

50    emit TCRNotified(_tcr)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50)


#

```
File: contracts/CdpManagerStorage.sol

55    emit GracePeriodStart()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55)


#

```
File: contracts/CdpManagerStorage.sol

64    emit TCRNotified(_tcr)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64)


#

```
File: contracts/CdpManagerStorage.sol

69    emit GracePeriodEnd()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69)


#

```
File: contracts/CdpManagerStorage.sol

587    emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587)


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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390-L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390-L400)


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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602-L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602-L608)


#

```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L466-L472](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L466-L472)


#

```
File: contracts/CdpManagerStorage.sol

340    emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340)


#

```
File: contracts/CdpManager.sol

545    emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L545](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L545)


#

```
File: contracts/CdpManager.sol

681    emit BaseRateUpdated(decayedBaseRate)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681)


#

```
File: contracts/CdpManager.sol

782    emit StakingRewardSplitSet(_stakingRewardSplit)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782)


#

```
File: contracts/CdpManager.sol

801    emit RedemptionFeeFloorSet(_redemptionFeeFloor)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801)


#

```
File: contracts/CdpManager.sol

824    emit MinuteDecayFactorSet(_minuteDecayFactor)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824)


#

```
File: contracts/CdpManager.sol

836    emit BetaSet(_beta)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836)


#

```
File: contracts/CdpManager.sol

848    emit RedemptionsPaused(_paused)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848)


#

```
File: contracts/CdpManager.sol

925    emit CdpUpdated(
926                _cdpId,
927                _borrower,
928                msg.sender,
929                0,
930                0,
931                _debt,
932                _coll,
933                stake,
934                CdpOperation.openCdp
935            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L925-L935](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L925-L935)


#

```
File: contracts/CdpManager.sol

961    emit CdpUpdated(
962                _cdpId,
963                _borrower,
964                msg.sender,
965                _debt,
966                _coll,
967                _newDebt,
968                _newColl,
969                stake,
970                CdpOperation.adjustCdp
971            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L961-L971](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L961-L971)


#

```
File: contracts/CdpManagerStorage.sol

119    emit GracePeriodDurationSet(_gracePeriod)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119)


#

```
File: contracts/CollSurplusPool.sol

83    emit SurplusCollSharesUpdated(_account, newAmount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83)


#

```
File: contracts/CollSurplusPool.sol

104    emit CollSharesTransferred(_account, claimableColl)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104)


#

```
File: contracts/CollSurplusPool.sol

95    emit SurplusCollSharesUpdated(_account, 0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L95)


#

```
File: contracts/CollSurplusPool.sol

150    emit SweepTokenSuccess(token, amount, feeRecipientAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150)


#

```
File: contracts/EBTCToken.sol

267    emit Transfer(address(0), account, amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267)


#

```
File: contracts/EBTCToken.sol

282    emit Transfer(account, address(0), amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282)


#

```
File: contracts/EBTCToken.sol

259    emit Transfer(sender, recipient, amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259)


#

```
File: contracts/EBTCToken.sol

290    emit Approval(owner, spender, amount)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L290)


#

```
File: contracts/Governor.sol

157    emit RoleNameSet(role, roleName)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)


#

```
File: contracts/LeverageMacroFactory.sol

56    emit DeployNewMacro(_owner, addy)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238-L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238-L248)


#

```
File: contracts/LiquidationLibrary.sol

516    emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490-L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490-L500)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376)


#

```
File: contracts/LiquidationLibrary.sol

891    emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445)


#

```
File: contracts/PriceFeed.sol

555    emit LastGoodPriceUpdated(_currentPrice)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555)


#

```
File: contracts/PriceFeed.sol

67    emit FallbackCallerChanged(address(0), _fallbackCallerAddress)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67)


#

```
File: contracts/PriceFeed.sol

548    emit PriceFeedStatusChanged(_status)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548)


#

```
File: contracts/PriceFeed.sol

378    emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378)


#

```
File: contracts/PriceFeed.sol

381    emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381)


#

```
File: contracts/PriceFeed.sol

387    emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387)


#

```
File: contracts/SortedCdps.sol

405    emit NodeAdded(_id, _NICR)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405)


#

```
File: contracts/SortedCdps.sol

490    emit NodeRemoved(_id)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490)


#

```
File: contracts/SortedCdps.sol

451    emit NodeRemoved(_ids[i])
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451)


</details>

# 


## Avoid unnecessary storage updates
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 4000

### Description
Avoid updating storage when the value hasn't changed. If the old value is equal to the new value, not re-storing the value will avoid a `SSTORE` operation (costing 2900 gas), potentially at the expense of a `SLOAD` operation (2100 gas) or a `WARMACCESS` operation (100 gas).

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#
The function `setBeta()` changes the state variable without first verifying if the values are different.


```
File: contracts/CdpManager.sol

835    beta = _beta
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L835)


#
The function `setFlashLoansPaused()` changes the state variable without first verifying if the values are different.


```
File: contracts/ActivePool.sol

420    flashLoansPaused = _paused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L420)


#
The function `setFlashLoansPaused()` changes the state variable without first verifying if the values are different.


```
File: contracts/BorrowerOperations.sol

1170    flashLoansPaused = _paused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1170](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1170)


#
The function `setRedemptionsPaused()` changes the state variable without first verifying if the values are different.


```
File: contracts/CdpManager.sol

847    redemptionsPaused = _paused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L847](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L847)


#
The function `setRoleName()` changes the state variable without first verifying if the values are different.


```
File: contracts/Governor.sol

155    roleNames[role] = roleName
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L155)


</details>

# 


## Multiplication and Division by 2 Should use in Bit Shifting
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 20

### Description
The expressions 'x * 2' and 'x / 2' can be optimized for gas efficiency by utilizing bitwise operations. In Solidity, you can achieve the same results by using bitwise left shift (x << 1) for multiplication and bitwise right shift (x >> 1) for division.

Using bitwise shift operations (SHL and SHR) instead of multiplication (MUL) and division (DIV) opcodes can lead to significant gas savings. The MUL and DIV opcodes cost 5 gas, while the SHL and SHR opcodes incur a lower cost of only 3 gas.

By leveraging these more efficient bitwise operations, you can reduce the gas consumption of your smart contracts and enhance their overall performance.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

800    return
801                (_scaledDecimal *
802                    uint256(_ethBtcAnswer) *
803                    uint256(_stEthEthAnswer) *
804                    EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2)
```
 instead `2` use bit shifting `1` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800-L804)


</details>

# 


## Using bools for storage incurs overhead
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 34200

### Description
Booleans are more expensive than uint256 or any type that takes up a full word because each write operation emits an extra SLOAD to first read the slot's contents, replace the bits taken up by the boolean, and then write back. This is the compiler's defense against contract upgrades and pointer aliasing, and it cannot be disabled.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

143    bool public redemptionsPaused
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)


#

```
File: contracts/LeverageMacroBase.sol

35    bool internal immutable willSweep
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35)


</details>

# 


## Optimizing Small Data Storage with Bytes32
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 4158

### Description
This detector flags contracts that inefficiently use bytes and strings for small data that could fit into bytes32. Using bytes32 is cheaper in Solidity when the data can fit into 32 bytes.

<details>

<summary>
There are 11 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

24    string public constant NAME = "ActivePool"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)


#

```
File: contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)


#

```
File: contracts/BorrowerOperations.sol

41    string internal constant _VERSION = "1"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L41)


#

```
File: contracts/CdpManagerStorage.sol

122    string public constant NAME = "CdpManager"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122)


#

```
File: contracts/CollSurplusPool.sol

19    string public constant NAME = "CollSurplusPool"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)


#

```
File: contracts/EBTCToken.sol

28    string internal constant _NAME = "EBTC Stablecoin"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L28)


#

```
File: contracts/EBTCToken.sol

29    string internal constant _SYMBOL = "EBTC"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L29)


#

```
File: contracts/EBTCToken.sol

30    string internal constant _VERSION = "1"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L30)


#

```
File: contracts/HintHelpers.sol

12    string public constant NAME = "HintHelpers"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)


#

```
File: contracts/PriceFeed.sol

22    string public constant NAME = "PriceFeed"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22)


#

```
File: contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps"
```
 should be convert to `bytes32`
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52)


</details>

# 


## Check Arguments Early
- Severity: Gas Optimization
- Confidence: High

### Description
Checks that require() or revert() statements that check input arguments are at the top of the function. Checks that involve constants should come before checks that involve state variables, function calls, and calculations. By doing these checks first, the function is able to revert before wasting a gas load in a function that may ultimately revert in the unhappy case.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

374    require(token != address(collateral), "ActivePool: Cannot Sweep Collateral")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374)


#

```
File: contracts/ActivePool.sol

393    require(
394                _feeRecipientAddress != address(0),
395                "ActivePool: Cannot set fee recipient to zero address"
396            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/SortedCdps.sol

508    require(_newNICR > 0, "SortedCdps: NICR must be positive")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)


</details>

# 


## Division operations between unsigned could be unchecked
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 255

### Description
Division operations on unsigned integers should be unchecked to save gas since they cannot overflow or underflow. Because unsigned integers cannot have negative values, execution of division operations outside `unchecked` blocks adds nothing but overhead. Saves about 85 gas.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

567    uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes
```
 Should be unchecked - _deltaFeeSplitShare / _cachedAllStakes.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L567)


#

```
File: contracts/CdpManager.sol

624    uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta)
```
 Should be unchecked - redeemedEBTCFraction / beta.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624)


#

```
File: contracts/LiquidationLibrary.sol

882    uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes
```
 Should be unchecked - EBTCDebtNumerator / _totalStakes.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882)


</details>

# 


## Modulus operations that could be unchecked
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 85

### Description
Modulus operations should be unchecked to save gas since they cannot overflow or underflow. Execution of modulus operations outside `unchecked` blocks adds nothing but overhead. Saves about 30 gas.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/HintHelpers.sol

184    latestRandomSeed % arrayLength
```
 should be unchecked

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L184](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L184)


</details>

# 


## Potential Optimization by Combining Multiple Mappings into a Struct
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 1000

### Description
This detector identifies instances where multiple mappings of an address or ID could be combined into a single mapping to a struct. This optimisation not only saves a storage slot for each mapping that is combined, but also makes the contract more efficient in terms of gas usage. Depending on the circumstances and sizes of types, it can avoid a 20000 gas cost (Gsset) per combined mapping. Also, it can make reads and subsequent writes cheaper when a function requires both values and they both fit in the same storage slot. Lastly, if both fields are accessed in the same function, it can save approximately 42 gas per access due to not having to recalculate the key's keccak256 hash and its associated stack operations.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```
Consider to combine with <br>-    ```Line: 190 mapping(bytes32 => uint256) public cdpDebtRedistributionIndex```<br>-    ```Line: 202 mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex```<br><br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168)


#

```
File: contracts/EBTCToken.sol

51    mapping(address => uint256) private _balances
```
Consider to combine with <br>-    ```Line: 52 mapping(address => mapping(address => uint256)) private _allowances```<br><br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51)


</details>

# 


## Constants Variable Should Be Private for Gas Optimization
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 61200

### Description
This detector flags contracts that inefficiently use `public` for constant variables. Using `private` for constant variables is cheaper in terms of gas usage. If the value of the constant variable is needed, it can be accessed via a getter function. In case of multiple constant variables, a single getter function could be used to return a tuple of the values of all currently-private constants.

<details>

<summary>
There are 18 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

24    string public constant NAME = "ActivePool"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)


#

```
File: contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)


#

```
File: contracts/CdpManagerStorage.sol

21    uint128 public constant UNSET_TIMESTAMP = type(uint128).max
```
 `UNSET_TIMESTAMP` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21)


#

```
File: contracts/CdpManagerStorage.sol

22    uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes
```
 `MINIMUM_GRACE_PERIOD` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22)


#

```
File: contracts/CdpManagerStorage.sol

122    string public constant NAME = "CdpManager"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122)


#

```
File: contracts/CdpManagerStorage.sol

139    uint256 public constant SECONDS_IN_ONE_MINUTE = 60
```
 `SECONDS_IN_ONE_MINUTE` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139)


#

```
File: contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000
```
 `MIN_REDEMPTION_FEE_FLOOR` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)


#

```
File: contracts/CdpManagerStorage.sol

149    uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1
```
 `MIN_MINUTE_DECAY_FACTOR` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149)


#

```
File: contracts/CdpManagerStorage.sol

150    uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999
```
 `MAX_MINUTE_DECAY_FACTOR` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)


#

```
File: contracts/CollSurplusPool.sol

19    string public constant NAME = "CollSurplusPool"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)


#

```
File: contracts/HintHelpers.sol

12    string public constant NAME = "HintHelpers"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)


#

```
File: contracts/PriceFeed.sol

22    string public constant NAME = "PriceFeed"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22)


#

```
File: contracts/PriceFeed.sol

32    uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800
```
 `TIMEOUT_ETH_BTC_FEED` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32)


#

```
File: contracts/PriceFeed.sol

33    uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000
```
 `TIMEOUT_STETH_ETH_FEED` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33)


#

```
File: contracts/PriceFeed.sol

36    uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17
```
 `MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36)


#

```
File: contracts/PriceFeed.sol

42    uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16
```
 `MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42)


#

```
File: contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps"
```
 `NAME` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52)


#

```
File: contracts/SortedCdps.sol

80    bytes32 public constant dummyId =
81            0x0000000000000000000000000000000000000000000000000000000000000000
```
 `dummyId` is a public. Consider making it private to save gas.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80-L81)


</details>

# 


## State variables that could be declared constant
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 20970

### Description
State variables that are not updated following deployment should be declared constant to save gas.

<details>

<summary>
There are 10 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

161    uint256 public baseRate
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161)


#

```
File: contracts/CdpManagerStorage.sol

159    uint256 public beta = 2
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L159)


#

```
File: contracts/CdpManagerStorage.sol

193    uint256 public lastEBTCDebtErrorRedistribution
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L193](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L193)


#

```
File: contracts/CdpManagerStorage.sol

166    uint256 public lastRedemptionTimestamp
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L166)


#

```
File: contracts/CdpManagerStorage.sol

148    uint256 public minuteDecayFactor = 999037758833783000
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148)


#

```
File: contracts/CdpManagerStorage.sol

142    uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142)


#

```
File: contracts/CdpManagerStorage.sol

143    bool public redemptionsPaused
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)


#

```
File: contracts/CdpManagerStorage.sol

163    uint256 public stakingRewardSplit
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163)


#

```
File: contracts/CdpManagerStorage.sol

187    uint256 public systemDebtRedistributionIndex
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L187)


#

```
File: contracts/Governor.sol

17    bytes32 NO_ROLES = bytes32(0)
```
 should be constant 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)


</details>

# 


## Use of emit inside a loop
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 5130

### Description
Emitting an event inside a loop performs a LOG op N times, where N is the loop length. This can lead to significant gas costs.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

300    emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300)


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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220-L230)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312-L322)


#

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290)


#

```
File: contracts/SortedCdps.sol

451    emit NodeRemoved(_ids[i])
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451)


</details>

# 


## Empty Block
- Severity: Gas Optimization
- Confidence: High

### Description
The code should be refactored such that they no longer exist, or the block should do something useful, such as emitting an event or reverting. If the contract is meant to be extended, the contract should be abstract and the function signatures be added without any default implementation. If the block is an empty if-statement block to avoid doing subsequent checks in the else-if/else conditions, the else-if/else conditions should be nested under the negation of the if-statement, because they involve different classes of checks, which may lead to the introduction of errors when the code is later modified.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/PriceFeed.sol

588    try fallbackCaller.getFallbackResponse() returns (
589                    uint256 answer,
590                    uint256 timestampRetrieved,
591                    bool success
592                ) {
593                    fallbackResponse.answer = answer;
594                    fallbackResponse.timestamp = timestampRetrieved;
595                    fallbackResponse.success = success;
596                } catch {
597                    // If call to Fallback reverts, return a zero response with success = false
598                }
```
  contains an empty block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L588-L598](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L588-L598)


#

```
File: contracts/PriceFeed.sol

587    if (address(fallbackCaller) != address(0)) {
588                try fallbackCaller.getFallbackResponse() returns (
589                    uint256 answer,
590                    uint256 timestampRetrieved,
591                    bool success
592                ) {
593                    fallbackResponse.answer = answer;
594                    fallbackResponse.timestamp = timestampRetrieved;
595                    fallbackResponse.success = success;
596                } catch {
597                    // If call to Fallback reverts, return a zero response with success = false
598                }
599            }
```
  contains an empty block.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587-L599](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587-L599)


</details>

# 


## Identical Deployments Should be Replaced with Clone
- Severity: Gas Optimization
- Confidence: High

### Description
Detects instances where the same contract is deployed multiple times. Such cases might benefit from the clone factory pattern (EIP-1167), which can significantly reduce deployment gas costs.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#
    - LeverageMacroReference is deployed in multiple functions:

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

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L44-L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L44-L54)


</details>

# 


## Use a More Recent Version of Solidity
- Severity: Gas Optimization
- Confidence: High

### Description

`solc` frequently releases new compiler versions. Using an old version prevents access to new Solidity security checks.
Addition new version gain some gas boost.
We also recommend avoiding complex `pragma` statement.

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
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3)


#

```
File: contracts/BorrowerOperations.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3)


#

```
File: contracts/CdpManager.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3)


#

```
File: contracts/CdpManagerStorage.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3)


#

```
File: contracts/CollSurplusPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3)


#

```
File: contracts/EBTCToken.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3)


#

```
File: contracts/Governor.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2)


#

```
File: contracts/HintHelpers.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3)


#

```
File: contracts/Interfaces/IActivePool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3)


#

```
File: contracts/Interfaces/IBorrowerOperations.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3)


#

```
File: contracts/Interfaces/ICdpManager.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3)


#

```
File: contracts/Interfaces/ICdpManagerData.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3)


#

```
File: contracts/Interfaces/ICollSurplusPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3)


#

```
File: contracts/Interfaces/IEBTCToken.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3)


#

```
File: contracts/Interfaces/IERC3156FlashBorrower.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3)


#

```
File: contracts/Interfaces/IERC3156FlashLender.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3)


#

```
File: contracts/Interfaces/IEbtcBase.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3)


#

```
File: contracts/Interfaces/IFallbackCaller.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3)


#

```
File: contracts/Interfaces/IPermitNonce.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3)


#

```
File: contracts/Interfaces/IPool.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3)


#

```
File: contracts/Interfaces/IPositionManagers.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3)


#

```
File: contracts/Interfaces/IPriceFeed.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3)


#

```
File: contracts/Interfaces/IRecoveryModeGracePeriod.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2)


#

```
File: contracts/Interfaces/ISortedCdps.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3)


#

```
File: contracts/LeverageMacroBase.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2)


#

```
File: contracts/LeverageMacroFactory.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2)


#

```
File: contracts/LeverageMacroReference.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2)


#

```
File: contracts/LiquidationLibrary.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3)


#

```
File: contracts/PriceFeed.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3)


#

```
File: contracts/SimplifiedDiamondLike.sol

2    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2)


#

```
File: contracts/SortedCdps.sol

3    pragma solidity 0.8.17;
```
 instead use `0.8.19`

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3)


#
solc-0.8.17 is not recommended for deployment

#
solc-0.4.26 is not recommended for deployment

</details>

# 


## Inefficient assignments to state variables
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 113

### Description
Assignment operations that involve calculations, like add-assigment (`+=`), for state variables, should be replaced with the appropriate calculation operation, like add (`+`), followed by an assignment operation (`=`), to save gas. Avoids a `Gwarmaccess` (100 gas).

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

697    lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE
```
 should use the appropriate calculation operation (`+`), followed by an assignment operation (`=`)

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L697](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L697)


</details>

# 


## Greater or Equal Comparison Costs Less Gas than Greater Comparison
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 27

### Description
In Solidity, the >= operator costs less gas than the > operator. This is because the Solidity compiler uses the LT opcode for >= comparisons, which requires less gas than the combination of GT and ISZERO opcodes used for > comparisons. Therefore, replacing > with >= when possible can reduce the gas cost of your contract.

<details>

<summary>
There are 9 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

690    uint256 timePassed = block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692)


#

```
File: contracts/CdpManagerStorage.sol

99    newTCR < CCR
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L99)


#

```
File: contracts/LiquidationLibrary.sol

100    bool _recoveryModeAtStart = _TCR < CCR ? true : false
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100)


#

```
File: contracts/LiquidationLibrary.sol

358    _recoveryState.entireSystemDebt = _recoveryState.entireSystemDebt > _totalDebtToBurn
359                ? _recoveryState.entireSystemDebt - _totalDebtToBurn
360                : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L358-L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L358-L360)


#

```
File: contracts/LiquidationLibrary.sol

361    _recoveryState.entireSystemColl = _recoveryState.entireSystemColl > _totalColToSend
362                ? _recoveryState.entireSystemColl - _totalColToSend
363                : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L361-L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L361-L363)


#

```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596)


#

```
File: contracts/LiquidationLibrary.sol

602    toLiquidator = toLiquidator < _totalColToSend ? toLiquidator : _totalColToSend
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L602)


#

```
File: contracts/PriceFeed.sol

794    uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals
795                ? _stEthEthDecimals
796                : _ethBtcDecimals
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L794-L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L794-L796)


#

```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
 using GREATER_EQUAL/LESS_EQUAL in this case is identical therefore should be use.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799)


</details>

# 


## Inefficient Parameter Storage
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 1750

### Description
When passing function parameters, using the `calldata` area instead of `memory` can improve gas efficiency. Calldata is a read-only area where function arguments and external function calls' parameters are stored.

By using `calldata` for function parameters, you avoid unnecessary gas costs associated with copying data from `calldata` to memory. This is particularly beneficial when the parameter is read-only and doesn't require modification within the contract.

Using `calldata` for function parameters can help optimize gas usage, especially when making external function calls or when the parameter values are provided externally and don't need to be stored persistently within the contract.

<details>

<summary>
There are 35 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

760    MoveTokensParams memory _varMvTokens
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760)


#

```
File: contracts/BorrowerOperations.sol

987    AdjustCdpLocals memory vars
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L987](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L987)


#

```
File: contracts/CdpManager.sol

126    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126)


#

```
File: contracts/CdpManager.sol

136    SingleRedemptionInputs memory _redeemColFromCdp
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L136](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L136)


#

```
File: contracts/Governor.sol

120    uint8[] memory roleIds
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120)


#

```
File: contracts/Interfaces/ISortedCdps.sol

16    bytes32[] memory _ids
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16)


#

```
File: contracts/LeverageMacroBase.sol

244    CheckValueAndType memory check
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244)


#

```
File: contracts/LeverageMacroBase.sol

291    LeverageMacroOperation memory operation
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291)


#

```
File: contracts/LeverageMacroBase.sol

382    SwapOperation[] memory swapData
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382)


#

```
File: contracts/LeverageMacroBase.sol

398    SwapOperation memory swapData
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398)


#

```
File: contracts/LeverageMacroBase.sol

435    SwapCheck[] memory swapChecks
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435)


#

```
File: contracts/LiquidationLibrary.sol

398    LiquidationLocals memory _partialState
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L398)


#

```
File: contracts/LiquidationLibrary.sol

467    LiquidationLocals memory _partialState
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L467](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L467)


#

```
File: contracts/LiquidationLibrary.sol

611    LocalVariables_LiquidationSequence memory vars
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L611](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L611)


#

```
File: contracts/LiquidationLibrary.sol

646    LocalVariables_LiquidationSequence memory vars
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L646](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L646)


#

```
File: contracts/LiquidationLibrary.sol

679    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679)


#

```
File: contracts/LiquidationLibrary.sol

737    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L737)


#

```
File: contracts/LiquidationLibrary.sol

810    bytes32[] memory _cdpArray
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L810](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L810)


#

```
File: contracts/LiquidationLibrary.sol

840    LiquidationTotals memory oldTotals
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L840](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L840)


#

```
File: contracts/LiquidationLibrary.sol

841    LiquidationValues memory singleLiquidation
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L841](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L841)


#

```
File: contracts/PriceFeed.sol

401    ChainlinkResponse memory _currentResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L401](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L401)


#

```
File: contracts/PriceFeed.sol

402    ChainlinkResponse memory _prevResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L402](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L402)


#

```
File: contracts/PriceFeed.sol

412    ChainlinkResponse memory _response
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L412)


#

```
File: contracts/PriceFeed.sol

435    ChainlinkResponse memory _response
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L435)


#

```
File: contracts/PriceFeed.sol

446    ChainlinkResponse memory _currentResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L446](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L446)


#

```
File: contracts/PriceFeed.sol

447    ChainlinkResponse memory _prevResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L447](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L447)


#

```
File: contracts/PriceFeed.sol

465    FallbackResponse memory _response
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465)


#

```
File: contracts/PriceFeed.sol

486    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L486](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L486)


#

```
File: contracts/PriceFeed.sol

504    ChainlinkResponse memory _chainlinkResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L504](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L504)


#

```
File: contracts/PriceFeed.sol

505    ChainlinkResponse memory _prevChainlinkResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L505](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L505)


#

```
File: contracts/PriceFeed.sol

506    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L506)


#

```
File: contracts/PriceFeed.sol

527    ChainlinkResponse memory _chainlinkResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L527](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L527)


#

```
File: contracts/PriceFeed.sol

528    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L528](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L528)


#

```
File: contracts/PriceFeed.sol

562    FallbackResponse memory _fallbackResponse
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L562](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L562)


#

```
File: contracts/SortedCdps.sol

419    bytes32[] memory _ids
```
 should be declared as `calldata` instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419)


</details>

# 


## Using Storage Instead of Memory for structs/arrays Saves Gas
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 29400

### Description
When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct / array to be read from storage. This incurs a Gcoldsload (2100 gas) for each field of the struct / array. If the fields are read from the new memory variable, they incur an additional MLOAD, which is more expensive than a simple stack read.

Instead of declaring the variable with the memory keyword, a more cost-effective approach is to declare the variable with the storage keyword. In this case, you can cache any fields that need to be re-read in stack variables. This approach significantly reduces gas costs, as you only incur the Gcoldsload for the fields actually read.

The only scenario where it makes sense to read the whole struct / array into a memory variable is if the full struct / array is being returned by the function or passed to a function that requires memory. Additionally, if the array / struct is being read from another memory array / struct, using a memory variable may be appropriate.

By carefully considering the storage and memory usage in your contract, you can optimize gas costs and improve the efficiency of your smart contract operations.

<details>

<summary>
There are 7 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

150    CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
151                Cdps[_redeemColFromCdp.cdpId].debt,
152                Cdps[_redeemColFromCdp.cdpId].coll
153            )
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L150-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L150-L153)


#

```
File: contracts/Governor.sol

56    address[] memory _usrs = users.values()
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56)


#

```
File: contracts/Governor.sol

134    bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values()
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L134)


#

```
File: contracts/LeverageMacroBase.sol

176    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId)
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176)


#

```
File: contracts/LeverageMacroBase.sol

187    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187)


#

```
File: contracts/LeverageMacroBase.sol

199    ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId)
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199)


#

```
File: contracts/SortedCdps.sol

522    Node memory _node = data.nodes[_id]
```
 should be declared as `storage` 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522)


</details>

# 


## Internal or Private Function that Called Once Should Be Inlined to Save Gas
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 380

### Description
Setting the internal/private function that called once to inline would save gas

<details>

<summary>
There are 19 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

648    function _requireCdpIsActive(bytes32 _cdpId) internal view 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648-L650](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648-L650)


#

```
File: contracts/CdpManagerStorage.sol

733    function _getSyncedDebtAndCollShares(
734            bytes32 _cdpId
735        ) internal view returns (CdpDebtAndCollShares memory) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733-L738](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733-L738)


#

```
File: contracts/EBTCToken.sol

306    function _requireCallerIsBorrowerOperations() internal view 
```
 this function can be delete, the function is never called:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306-L311)


#

```
File: contracts/EBTCToken.sol

323    function _requireCallerIsCdpM() internal view 
```
 this function can be delete, the function is never called:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323-L325)


#

```
File: contracts/HintHelpers.sol

133    function _calculateCdpStateAfterPartialRedemption(
134            LocalVariables_getRedemptionHints memory vars,
135            uint256 currentCdpDebt,
136            uint256 _price
137        ) internal view returns (uint256, uint256) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133-L153)


#

```
File: contracts/LiquidationLibrary.sol

135    function _liquidateIndividualCdpSetupCDP(
136            LiquidationLocals memory _liqState,
137            LiquidationRecoveryModeLocals memory _recoveryState
138        ) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135-L182)


#

```
File: contracts/LiquidationLibrary.sol

397    function _liquidateCDPPartially(
398            LiquidationLocals memory _partialState
399        ) private returns (uint256, uint256) 
```
 should be inline to save gas:

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
 should be inline to save gas:

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
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466-L501)


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
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568)


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
 should be inline to save gas:

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
 should be inline to save gas:

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
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807-L835)


#

```
File: contracts/LiquidationLibrary.sol

862    function _redistributeDebt(uint256 _debt) internal 
```
 should be inline to save gas:

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
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896-L906)


#

```
File: contracts/LiquidationLibrary.sol

908    function _requirePartialLiqCollSize(uint256 _entireColl) internal pure 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908-L913](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908-L913)


#

```
File: contracts/SimplifiedDiamondLike.sol

134    function _executeOne(Operation calldata op) internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L156)


#

```
File: contracts/SimplifiedDiamondLike.sol

174    function _fallback() internal 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L174-L201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L174-L201)


#

```
File: contracts/SortedCdps.sol

642    function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) 
```
 should be inline to save gas:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658)


</details>

# 


## Inefficient Gas Usage in Solidity Smart Contracts Due to Long Error Messages
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 1998

### Description
If the string parameter of a require() or revert() function is longer than 32 bytes, it can lead to inefficiencies. This is because each extra memory word of bytes past the original 32 incurs an MSTORE operation, which costs 3 gas.

<details>

<summary>
There are 111 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

137    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137)


#

```
File: contracts/ActivePool.sol

162    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162)


#

```
File: contracts/ActivePool.sol

220    require(
221                msg.sender == borrowerOperationsAddress,
222                "ActivePool: Caller is not BorrowerOperations"
223            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223)


#

```
File: contracts/ActivePool.sol

228    require(
229                msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230                "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231)


#

```
File: contracts/ActivePool.sol

236    require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236)


#

```
File: contracts/ActivePool.sol

277    require(
278                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279                "ActivePool: IERC3156: Callback failed"
280            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280)


#

```
File: contracts/ActivePool.sol

302    require(
303                collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304                "ActivePool: Should keep same collateral share rate"
305            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305)


#

```
File: contracts/ActivePool.sol

350    require(
351                cachedFeeRecipientCollShares >= _shares,
352                "ActivePool: Insufficient fee recipient coll"
353            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353)


#

```
File: contracts/ActivePool.sol

374    require(token != address(collateral), "ActivePool: Cannot Sweep Collateral")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374)


#

```
File: contracts/ActivePool.sol

377    require(amount <= balance, "ActivePool: Attempt to sweep more than balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377)


#

```
File: contracts/ActivePool.sol

393    require(
394                _feeRecipientAddress != address(0),
395                "ActivePool: Cannot set fee recipient to zero address"
396            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/BorrowerOperations.sol

368    require(
369                _stEthBalanceDecrease <= _cdpStEthBalance,
370                "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371)


#

```
File: contracts/BorrowerOperations.sol

463    require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463)


#

```
File: contracts/BorrowerOperations.sol

541    require(
542                vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543                "BorrowerOperations: deposited collateral mismatch!"
544            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544)


#

```
File: contracts/BorrowerOperations.sol

715    require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715)


#

```
File: contracts/BorrowerOperations.sol

734    require(
735                recoveredAddress != address(0) && recoveredAddress == _borrower,
736                "BorrowerOperations: Invalid signature"
737            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737)


#

```
File: contracts/BorrowerOperations.sol

807    require(
808                _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809                "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810)


#

```
File: contracts/BorrowerOperations.sol

818    require(
819                _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820                "BorrowerOperations: There must be either a collateral change or a debt change"
821            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821)


#

```
File: contracts/BorrowerOperations.sol

826    require(status == 1, "BorrowerOperations: Cdp does not exist or is closed")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826)


#

```
File: contracts/BorrowerOperations.sol

831    require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831)


#

```
File: contracts/BorrowerOperations.sol

835    require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835)


#

```
File: contracts/BorrowerOperations.sol

839    require(
840                !_checkRecoveryModeForTCR(_tcr),
841                "BorrowerOperations: Operation not permitted during Recovery Mode"
842            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842)


#

```
File: contracts/BorrowerOperations.sol

846    require(
847                _stEthBalanceDecrease == 0,
848                "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849)


#

```
File: contracts/BorrowerOperations.sol

911    require(
912                _newICR >= MCR,
913                "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"
914            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914)


#

```
File: contracts/BorrowerOperations.sol

918    require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918)


#

```
File: contracts/BorrowerOperations.sol

922    require(
923                _newICR >= _oldICR,
924                "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925)


#

```
File: contracts/BorrowerOperations.sol

929    require(
930                _newTCR >= CCR,
931                "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932)


#

```
File: contracts/BorrowerOperations.sol

936    require(_debt > 0, "BorrowerOperations: Debt must be non-zero")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936)


#

```
File: contracts/BorrowerOperations.sol

940    require(
941                _stEthBalance >= MIN_NET_STETH_BALANCE,
942                "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
943            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943)


#

```
File: contracts/BorrowerOperations.sol

947    require(
948                _debtRepayment <= _currentDebt,
949                "BorrowerOperations: Amount repaid must not be larger than the Cdp's debt"
950            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950)


#

```
File: contracts/BorrowerOperations.sol

957    require(
958                ebtcToken.balanceOf(_account) >= _debtRepayment,
959                "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960)


#

```
File: contracts/BorrowerOperations.sol

970    require(
971                _approval != PositionManagerApproval.None,
972                "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"
973            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973)


#

```
File: contracts/BorrowerOperations.sol

1116    require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116)


#

```
File: contracts/BorrowerOperations.sol

1141    require(
1142                _feeRecipientAddress != address(0),
1143                "BorrowerOperations: Cannot set feeRecipient to zero address"
1144            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144)


#

```
File: contracts/BorrowerOperations.sol

1155    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155)


#

```
File: contracts/BorrowerOperations.sol

145    require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)


#

```
File: contracts/BorrowerOperations.sol

146    require(
147                ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148                "CdpManager: Reentrancy in nonReentrant call"
149            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149)


#

```
File: contracts/CdpManager.sol

431    require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431)


#

```
File: contracts/CdpManager.sol

502    require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502)


#

```
File: contracts/CdpManager.sol

503    require(
504                _toRemoveIds[_total - 1] == _end,
505                "CdpManager: batchRemoveSortedCdpIds check end error"
506            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506)


#

```
File: contracts/CdpManager.sol

626    require(newBaseRate > 0, "CdpManager: new baseRate is zero!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626)


#

```
File: contracts/CdpManager.sol

672    require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672)


#

```
File: contracts/CdpManager.sol

743    require(
744                callerBalance >= _amount,
745                "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746)


#

```
File: contracts/CdpManager.sol

747    require(
748                callerBalance <= _totalSupply,
749                "CdpManager: redeemer's EBTC balance exceeds total supply!"
750            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750)


#

```
File: contracts/CdpManager.sol

754    require(_amount > 0, "CdpManager: Amount must be greater than zero")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)


#

```
File: contracts/CdpManager.sol

758    require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758)


#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/CdpManager.sol

774    require(
775                _stakingRewardSplit <= MAX_REWARD_SPLIT,
776                "CDPManager: new staking reward split exceeds max"
777            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777)


#

```
File: contracts/CdpManager.sol

789    require(
790                _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791                "CDPManager: new redemption fee floor is lower than minimum"
792            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792)


#

```
File: contracts/CdpManager.sol

793    require(
794                _redemptionFeeFloor <= DECIMAL_PRECISION,
795                "CDPManager: new redemption fee floor is higher than maximum"
796            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796)


#

```
File: contracts/CdpManager.sol

808    require(
809                _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810                "CDPManager: new minute decay factor out of range"
811            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811)


#

```
File: contracts/CdpManager.sol

812    require(
813                _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814                "CDPManager: new minute decay factor out of range"
815            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815)


#

```
File: contracts/CdpManagerStorage.sol

112    require(
113                _gracePeriod >= MINIMUM_GRACE_PERIOD,
114                "CdpManager: Grace period below minimum duration"
115            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115)


#

```
File: contracts/CdpManagerStorage.sol

261    require(
262                closedStatus != Status.nonExistent && closedStatus != Status.active,
263                "CdpManagerStorage: close non-exist or non-active CDP!"
264            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264)


#

```
File: contracts/CdpManagerStorage.sol

453    require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453)


#

```
File: contracts/CdpManagerStorage.sol

466    require(
467                cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468                "CdpManagerStorage: remove non-exist or non-active CDP!"
469            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469)


#

```
File: contracts/CdpManagerStorage.sol

475    require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475)


#

```
File: contracts/CdpManagerStorage.sol

556    require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556)


#

```
File: contracts/CdpManagerStorage.sol

649    require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649)


#

```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


#

```
File: contracts/CdpManagerStorage.sol

660    require(
661                msg.sender == borrowerOperationsAddress,
662                "CdpManager: Caller is not the BorrowerOperations contract"
663            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663)


#

```
File: contracts/CdpManagerStorage.sol

242    require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)


#

```
File: contracts/CdpManagerStorage.sol

243    require(
244                ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245                "BorrowerOperations: Reentrancy in nonReentrant call"
246            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246)


#

```
File: contracts/CollSurplusPool.sol

92    require(claimableColl > 0, "CollSurplusPool: No collateral available to claim")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)


#

```
File: contracts/CollSurplusPool.sol

113    require(
114                msg.sender == borrowerOperationsAddress,
115                "CollSurplusPool: Caller is not Borrower Operations"
116            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116)


#

```
File: contracts/CollSurplusPool.sol

120    require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120)


#

```
File: contracts/CollSurplusPool.sol

124    require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124)


#

```
File: contracts/CollSurplusPool.sol

143    require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143)


#

```
File: contracts/CollSurplusPool.sol

146    require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146)


#

```
File: contracts/EBTCToken.sol

144    require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)


#

```
File: contracts/EBTCToken.sol

165    require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165)


#

```
File: contracts/EBTCToken.sol

251    require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251)


#

```
File: contracts/EBTCToken.sol

263    require(account != address(0), "EBTCToken: mint to zero recipient!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263)


#

```
File: contracts/EBTCToken.sol

271    require(account != address(0), "EBTCToken: burn from zero account!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271)


#

```
File: contracts/EBTCToken.sol

274    require(cachedBalance >= amount, "ERC20: burn amount exceeds balance")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274)


#

```
File: contracts/EBTCToken.sol

296    require(
297                _recipient != address(0) && _recipient != address(this),
298                "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299)


#

```
File: contracts/EBTCToken.sol

300    require(
301                _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302                "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303)


#

```
File: contracts/EBTCToken.sol

307    require(
308                msg.sender == borrowerOperationsAddress,
309                "EBTCToken: Caller is not BorrowerOperations"
310            )
```
 make the message shorter than 32 bytes

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
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320)


#

```
File: contracts/LeverageMacroBase.sol

179    require(
180                    cdpInfo.status == checkParams.expectedStatus,
181                    "!LeverageMacroReference: openCDP status check"
182                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182)


#

```
File: contracts/LeverageMacroBase.sol

191    require(
192                    cdpInfo.status == checkParams.expectedStatus,
193                    "!LeverageMacroReference: adjustCDP status check"
194                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194)


#

```
File: contracts/LeverageMacroBase.sol

201    require(
202                    cdpInfo.status == checkParams.expectedStatus,
203                    "!LeverageMacroReference: closeCDP status check"
204                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204)


#

```
File: contracts/LeverageMacroBase.sol

249    require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249)


#

```
File: contracts/LeverageMacroBase.sol

251    require(check.value <= valueToCheck, "!LeverageMacroReference: let post check")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251)


#

```
File: contracts/LeverageMacroBase.sol

253    require(check.value == valueToCheck, "!LeverageMacroReference: equal post check")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253)


#

```
File: contracts/LeverageMacroBase.sol

352    require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352)


#

```
File: contracts/LeverageMacroBase.sol

356    require(
357                    msg.sender == address(borrowerOperations),
358                    "LeverageMacroReference: wrong lender for eBTC flashloan"
359                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359)


#

```
File: contracts/LeverageMacroBase.sol

362    require(
363                    msg.sender == address(activePool),
364                    "LeverageMacroReference: wrong lender for stETH flashloan"
365                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365)


#

```
File: contracts/LeverageMacroBase.sol

440    require(
441                        IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442                            swapChecks[i].expectedMinOut,
443                        "LeverageMacroReference: swap check failure!"
444                    )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444)


#

```
File: contracts/LiquidationLibrary.sol

56    require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)


#

```
File: contracts/LiquidationLibrary.sol

82    require(
83                    _checkICRAgainstLiqThreshold(_ICR, _TCR),
84                    "LiquidationLibrary: ICR is not below liquidation threshold in current mode"
85                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85)


#

```
File: contracts/LiquidationLibrary.sol

89    require(
90                    cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP,
91                    "LiquidationLibrary: Recovery Mode grace period not started"
92                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92)


#

```
File: contracts/LiquidationLibrary.sol

93    require(
94                    block.timestamp >
95                        cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96                    "LiquidationLibrary: Recovery mode grace period still in effect"
97                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97)


#

```
File: contracts/LiquidationLibrary.sol

477    require(
478                    getCachedICR(_cdpId, _partialState.price) >= _partialState.ICR,
479                    "LiquidationLibrary: !_newICR>=_ICR"
480                )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480)


#

```
File: contracts/LiquidationLibrary.sol

680    require(
681                _cdpArray.length != 0,
682                "LiquidationLibrary: Calldata address array must not be empty"
683            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683)


#

```
File: contracts/LiquidationLibrary.sol

710    require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710)


#

```
File: contracts/LiquidationLibrary.sol

901    require(
902                (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903                    _entireDebt,
904                "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905)


#

```
File: contracts/LiquidationLibrary.sol

909    require(
910                _entireColl >= MIN_NET_STETH_BALANCE,
911                "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912)


#

```
File: contracts/PriceFeed.sol

79    require(
80                !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                    !_chainlinkIsFrozen(chainlinkResponse),
82                "PriceFeed: Chainlink must be working and current"
83            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83)


#

```
File: contracts/SortedCdps.sol

352    require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352)


#

```
File: contracts/SortedCdps.sol

367    require(!contains(_id), "SortedCdps: List already contains the node")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367)


#

```
File: contracts/SortedCdps.sol

371    require(_NICR > 0, "SortedCdps: NICR must be positive")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371)


#

```
File: contracts/SortedCdps.sol

422    require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422)


#

```
File: contracts/SortedCdps.sol

427    require(
428                _firstPrev != dummyId || _lastNext != dummyId,
429                "SortedCdps: batchRemove() leave ZERO node left!"
430            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430)


#

```
File: contracts/SortedCdps.sol

433    require(contains(_ids[i]), "SortedCdps: List does not contain the id")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433)


#

```
File: contracts/SortedCdps.sol

458    require(contains(_id), "SortedCdps: List does not contain the id")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458)


#

```
File: contracts/SortedCdps.sol

506    require(contains(_id), "SortedCdps: List does not contain the id")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506)


#

```
File: contracts/SortedCdps.sol

508    require(_newNICR > 0, "SortedCdps: NICR must be positive")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)


#

```
File: contracts/SortedCdps.sol

715    require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager")
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715)


#

```
File: contracts/SortedCdps.sol

720    require(
721                msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722                "SortedCdps: Caller is neither BO nor CdpM"
723            )
```
 make the message shorter than 32 bytes

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723)


</details>

# 


## Consider Merge Sequential For-Loops
- Severity: Gas Optimization
- Confidence: High

### Description
Detects instances where multiple for-loops appear sequentially in the same function. This may indicate an opportunity for loop fusion, a code optimization technique that merges multiple loops into a single one.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#
Consider merging those following loops to one loop if appropriate :
```
File: contracts/SortedCdps.sol

432    i < _len
```

```
File: contracts/SortedCdps.sol

449    i < _len
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)


</details>

# 


## Declare Constructor Function as Payable to Save Gas
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 336

### Description
Constructors should be declared `payable` to save gas

<details>

<summary>
There are 16 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

46    constructor(
47            address _borrowerOperationsAddress,
48            address _cdpManagerAddress,
49            address _collTokenAddress,
50            address _collSurplusAddress,
51            address _feeRecipientAddress
52        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46-L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46-L66)


#

```
File: contracts/BorrowerOperations.sol

107    constructor(
108            address _cdpManagerAddress,
109            address _activePoolAddress,
110            address _collSurplusPoolAddress,
111            address _priceFeedAddress,
112            address _sortedCdpsAddress,
113            address _ebtcTokenAddress,
114            address _feeRecipientAddress,
115            address _collTokenAddress
116        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107-L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107-L137)


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
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30-L60)


#

```
File: contracts/CdpManagerStorage.sol

217    constructor(
218            address _liquidationLibraryAddress,
219            address _authorityAddress,
220            address _borrowerOperationsAddress,
221            address _collSurplusPool,
222            address _ebtcToken,
223            address _sortedCdps,
224            address _activePool,
225            address _priceFeed,
226            address _collateral
227        ) EbtcBase(_activePool, _priceFeed, _collateral) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217-L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217-L237)


#

```
File: contracts/CollSurplusPool.sol

42    constructor(
43            address _borrowerOperationsAddress,
44            address _cdpManagerAddress,
45            address _activePoolAddress,
46            address _collTokenAddress
47        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42-L58](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42-L58)


#

```
File: contracts/EBTCToken.sol

61    constructor(
62            address _cdpManagerAddress,
63            address _borrowerOperationsAddress,
64            address _authorityAddress
65        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61-L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61-L78)


#

```
File: contracts/Governor.sol

36    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)


#

```
File: contracts/HintHelpers.sol

27    constructor(
28            address _sortedCdpsAddress,
29            address _cdpManagerAddress,
30            address _collateralAddress,
31            address _activePoolAddress,
32            address _priceFeedAddress
33        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27-L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27-L36)


#

```
File: contracts/LeverageMacroBase.sol

51    constructor(
52            address _borrowerOperationsAddress,
53            address _activePool,
54            address _cdpManager,
55            address _ebtc,
56            address _coll,
57            address _sortedCdps,
58            bool _sweepToCaller
59        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51-L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51-L68)


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
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L60)


#

```
File: contracts/LeverageMacroFactory.sol

21    constructor(
22            address _borrowerOperationsAddress,
23            address _activePool,
24            address _cdpManager,
25            address _ebtc,
26            address _coll,
27            address _sortedCdps
28        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21-L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21-L35)


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
 should be declared payable:

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
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34)


#

```
File: contracts/PriceFeed.sol

57    constructor(
58            address _fallbackCallerAddress,
59            address _authorityAddress,
60            address _collEthCLFeed,
61            address _ethBtcCLFeed
62        ) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57-L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57-L89)


#

```
File: contracts/SimplifiedDiamondLike.sol

44    constructor(address _owner) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L46)


#

```
File: contracts/SortedCdps.sol

88    constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) 
```
 should be declared payable:

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88-L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88-L97)


</details>

# 


## Optimize address(0) Checks Using Assembly
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 348

### Description
Solidity provides `address(0)` as a constant for the zero address. While it is generally safe to use, explicit checks against `address(0)` in your code might be slightly more gas efficient if implemented in inline assembly, due to reduced overhead.

<details>

<summary>
There are 6 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

61    _authorityAddress != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L61)


#

```
File: contracts/BorrowerOperations.sol

124    _authorityAddress != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L124)


#

```
File: contracts/CollSurplusPool.sol

55    _authorityAddress != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L55)


#

```
File: contracts/PriceFeed.sol

224    address(fallbackCaller) == address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L224)


#

```
File: contracts/PriceFeed.sol

587    address(fallbackCaller) != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587)


#

```
File: contracts/PriceFeed.sol

363    _fallbackCaller != address(0)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363)


</details>

# 


## Optimize Names to Save Gas
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 176

### Description
Optimize public/external function names and public member variable names to save gas. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, per sorted position shifted. Note: This detector does not mention special functions like constructors or functions that override other functions which cannot change their names due to the requirements of the overriding process.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/HintHelpers.sol

11    contract HintHelpers is EbtcBase 
```
``` 
/// @audit: getRedemptionHints()  ,getApproxHint()  ,computeNominalCR()  ,computeCR()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11-L219)


#

```
File: contracts/LeverageMacroBase.sol

14    interface ICdpCdps 
```
``` 
/// @audit: Cdps()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L14-L16)


#

```
File: contracts/LeverageMacroDelegateTarget.sol

6    interface IOwnerLike 
```
``` 
/// @audit: owner()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L8)


#

```
File: contracts/LeverageMacroFactory.sol

11    contract LeverageMacroFactory 
```
``` 
/// @audit: deployNewMacro()  ,deployNewMacro()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11-L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11-L60)


#

```
File: contracts/LeverageMacroReference.sol

11    contract LeverageMacroReference is LeverageMacroBase 
```
``` 
/// @audit: resetApprovals()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11-L57)


#

```
File: contracts/LiquidationLibrary.sol

13    contract LiquidationLibrary is CdpManagerStorage 
```
``` 
/// @audit: liquidate()  ,partiallyLiquidate()  ,batchLiquidateCdps()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13-L914)


#

```
File: contracts/SimplifiedDiamondLike.sol

25    contract SimplifiedDiamondLike 
```
``` 
/// @audit: setFallbackHandler()  ,setAllowAnyCall()  ,enableCallbackForCall()  ,execute()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L202)


#

```
File: contracts/SortedCdps.sol

51    contract SortedCdps is ISortedCdps 
```
``` 
/// @audit: toCdpId()  
``` 


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51-L725)


</details>

# 


## Optimal State Variable Order
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 15000

### Description
Detects optimal variable order in contract storage layouts to decrease the number of storage slots used. Each storage slot used can cost at least 5,000 gas for each write operation, and potentially up to 20,000 gas if you're turning a zero value into a non-zero value. Hence, optimizing storage usage can result in significant gas savings. The real-world savings could vary depending on your contract's specific logic and the state of the Ethereum network.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#
Optimization opportunity in storage variable layout of contract 
```
File: contracts/CdpManagerStorage.sol

19    contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner 
```

- original variable order (count: 32 slots)
    - uint128 UNSET_TIMESTAMP
    - uint128 MINIMUM_GRACE_PERIOD
    - uint128 lastGracePeriodStartTimestamp
    - uint128 recoveryModeGracePeriodDuration
    - string NAME
    - address borrowerOperationsAddress
    - ICollSurplusPool collSurplusPool
    - IEBTCToken ebtcToken
    - address liquidationLibrary
    - ISortedCdps sortedCdps
    - uint256 SECONDS_IN_ONE_MINUTE
    - uint256 MIN_REDEMPTION_FEE_FLOOR
    - uint256 redemptionFeeFloor
    - bool redemptionsPaused
    - uint256 minuteDecayFactor
    - uint256 MIN_MINUTE_DECAY_FACTOR
    - uint256 MAX_MINUTE_DECAY_FACTOR
    - uint256 deploymentStartTime
    - uint256 beta
    - uint256 baseRate
    - uint256 stakingRewardSplit
    - uint256 lastRedemptionTimestamp
    - mapping(bytes32 => ICdpManagerData.Cdp) Cdps
    - uint256 totalStakes
    - uint256 totalStakesSnapshot
    - uint256 totalCollateralSnapshot
    - uint256 systemDebtRedistributionIndex
    - mapping(bytes32 => uint256) cdpDebtRedistributionIndex
    - uint256 lastEBTCDebtErrorRedistribution
    - uint256 stEthIndex
    - uint256 systemStEthFeePerUnitIndex
    - uint256 systemStEthFeePerUnitIndexError
    - mapping(bytes32 => uint256) cdpStEthFeePerUnitIndex
    - bytes32[] CdpIds


 - optimized variable order (count: 31 slots)
    - address borrowerOperationsAddress
    - bool redemptionsPaused
    - ICollSurplusPool collSurplusPool
    - IEBTCToken ebtcToken
    - address liquidationLibrary
    - ISortedCdps sortedCdps
    - uint128 UNSET_TIMESTAMP
    - uint128 MINIMUM_GRACE_PERIOD
    - uint128 lastGracePeriodStartTimestamp
    - uint128 recoveryModeGracePeriodDuration
    - string NAME
    - uint256 SECONDS_IN_ONE_MINUTE
    - uint256 MIN_REDEMPTION_FEE_FLOOR
    - uint256 redemptionFeeFloor
    - uint256 minuteDecayFactor
    - uint256 MIN_MINUTE_DECAY_FACTOR
    - uint256 MAX_MINUTE_DECAY_FACTOR
    - uint256 deploymentStartTime
    - uint256 beta
    - uint256 baseRate
    - uint256 stakingRewardSplit
    - uint256 lastRedemptionTimestamp
    - mapping(bytes32 => ICdpManagerData.Cdp) Cdps
    - uint256 totalStakes
    - uint256 totalStakesSnapshot
    - uint256 totalCollateralSnapshot
    - uint256 systemDebtRedistributionIndex
    - mapping(bytes32 => uint256) cdpDebtRedistributionIndex
    - uint256 lastEBTCDebtErrorRedistribution
    - uint256 stEthIndex
    - uint256 systemStEthFeePerUnitIndex
    - uint256 systemStEthFeePerUnitIndexError
    - mapping(bytes32 => uint256) cdpStEthFeePerUnitIndex
    - bytes32[] CdpIds


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19-L902)


#
Optimization opportunity in storage variable layout of contract 
```
File: contracts/EBTCToken.sol

26    contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce 
```

- original variable order (count: 15 slots)
    - uint256 _totalSupply
    - string _NAME
    - string _SYMBOL
    - string _VERSION
    - uint8 _DECIMALS
    - bytes32 _PERMIT_TYPEHASH
    - bytes32 _TYPE_HASH
    - bytes32 _CACHED_DOMAIN_SEPARATOR
    - uint256 _CACHED_CHAIN_ID
    - bytes32 _HASHED_NAME
    - bytes32 _HASHED_VERSION
    - mapping(address => uint256) _balances
    - mapping(address => mapping(address => uint256)) _allowances
    - address cdpManagerAddress
    - address borrowerOperationsAddress


 - optimized variable order (count: 14 slots)
    - address cdpManagerAddress
    - uint8 _DECIMALS
    - address borrowerOperationsAddress
    - uint256 _totalSupply
    - string _NAME
    - string _SYMBOL
    - string _VERSION
    - bytes32 _PERMIT_TYPEHASH
    - bytes32 _TYPE_HASH
    - bytes32 _CACHED_DOMAIN_SEPARATOR
    - uint256 _CACHED_CHAIN_ID
    - bytes32 _HASHED_NAME
    - bytes32 _HASHED_VERSION
    - mapping(address => uint256) _balances
    - mapping(address => mapping(address => uint256)) _allowances


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26-L358)


#
Optimization opportunity in storage variable layout of contract 
```
File: contracts/PriceFeed.sol

21    contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner 
```

- original variable order (count: 10 slots)
    - string NAME
    - AggregatorV3Interface ETH_BTC_CL_FEED
    - AggregatorV3Interface STETH_ETH_CL_FEED
    - IFallbackCaller fallbackCaller
    - uint256 TIMEOUT_ETH_BTC_FEED
    - uint256 TIMEOUT_STETH_ETH_FEED
    - uint256 MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND
    - uint256 MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES
    - uint256 lastGoodPrice
    - IPriceFeed.Status status


 - optimized variable order (count: 9 slots)
    - AggregatorV3Interface ETH_BTC_CL_FEED
    - IPriceFeed.Status status
    - AggregatorV3Interface STETH_ETH_CL_FEED
    - IFallbackCaller fallbackCaller
    - string NAME
    - uint256 TIMEOUT_ETH_BTC_FEED
    - uint256 TIMEOUT_STETH_ETH_FEED
    - uint256 MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND
    - uint256 MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES
    - uint256 lastGoodPrice


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21-L806)


</details>

# 


## Optimal Struct Variable Order
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 20000

### Description
Detect optimal variable order in struct definitions to decrease the number of slots used. Each storage slot used can cost at least 5,000 gas for each write operation, and potentially up to 20,000 gas if you're turning a zero value into a non-zero value. Hence, optimizing storage usage can result in significant gas savings. The real-world savings could vary depending on your contract's specific logic and the state of the Ethereum network.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#
Optimization opportunity in struct 
```
File: contracts/BorrowerOperations.sol

97    struct MoveTokensParams {
98            address user;
99            uint256 collSharesChange;
100            uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101            bool isCollIncrease;
102            uint256 netDebtChange;
103            bool isDebtIncrease;
104        }
```

- original variable order (count: 6 slots)
    - address user
    - uint256 collSharesChange
    - uint256 collAddUnderlying
    - bool isCollIncrease
    - uint256 netDebtChange
    - bool isDebtIncrease


 - optimized variable order (count: 4 slots)
    - address user
    - bool isCollIncrease
    - bool isDebtIncrease
    - uint256 collSharesChange
    - uint256 collAddUnderlying
    - uint256 netDebtChange


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97-L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97-L104)


#
Optimization opportunity in struct 
```
File: contracts/Interfaces/IPriceFeed.sol

17    struct ChainlinkResponse {
18            uint80 roundEthBtcId;
19            uint80 roundStEthEthId;
20            uint256 answer;
21            uint256 timestampEthBtc;
22            uint256 timestampStEthEth;
23            bool success;
24        }
```

- original variable order (count: 5 slots)
    - uint80 roundEthBtcId
    - uint80 roundStEthEthId
    - uint256 answer
    - uint256 timestampEthBtc
    - uint256 timestampStEthEth
    - bool success


 - optimized variable order (count: 4 slots)
    - uint80 roundEthBtcId
    - uint80 roundStEthEthId
    - bool success
    - uint256 answer
    - uint256 timestampEthBtc
    - uint256 timestampStEthEth


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24)


#
Optimization opportunity in struct 
```
File: contracts/LeverageMacroBase.sol

259    struct LeverageMacroOperation {
260            address tokenToTransferIn;
261            uint256 amountToTransferIn;
262            SwapOperation[] swapsBefore; // Empty to skip
263            SwapOperation[] swapsAfter; // Empty to skip
264            OperationType operationType; // Open, Close, etc..
265            bytes OperationData; // Generic Operation Data, which we'll decode to use
266        }
```

- original variable order (count: 6 slots)
    - address tokenToTransferIn
    - uint256 amountToTransferIn
    - LeverageMacroBase.SwapOperation[] swapsBefore
    - LeverageMacroBase.SwapOperation[] swapsAfter
    - LeverageMacroBase.OperationType operationType
    - bytes OperationData


 - optimized variable order (count: 5 slots)
    - address tokenToTransferIn
    - LeverageMacroBase.OperationType operationType
    - uint256 amountToTransferIn
    - LeverageMacroBase.SwapOperation[] swapsBefore
    - LeverageMacroBase.SwapOperation[] swapsAfter
    - bytes OperationData


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L259-L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L259-L266)


#
Optimization opportunity in struct 
```
File: contracts/SimplifiedDiamondLike.sol

99    struct Operation {
100            address to; // Target to call
101            bool checkSuccess; // If false we will ignore a revert
102            uint128 value; // How much ETH to send
103            uint128 gas; // How much gas to send
104            bool capGas; // true to use above "gas" setting or we send gasleft()
105            OperationType opType; // See `OperationType`
106            bytes data; // Calldata to send (funsig + data)
107        }
```

- original variable order (count: 4 slots)
    - address to
    - bool checkSuccess
    - uint128 value
    - uint128 gas
    - bool capGas
    - SimplifiedDiamondLike.OperationType opType
    - bytes data


 - optimized variable order (count: 3 slots)
    - address to
    - bool checkSuccess
    - bool capGas
    - SimplifiedDiamondLike.OperationType opType
    - uint128 value
    - uint128 gas
    - bytes data


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107)


</details>

# 


## Postfix operations that could be replaced with prefix operations
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 60

### Description
Postfix operations should be replaced with prefix operations to save gas, 
    in case the result returned by the operation is ignored.

<details>

<summary>
There are 12 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

429    _maxIterations--
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L429](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L429)


#

```
File: contracts/Governor.sol

46    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

62    j++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62)


#

```
File: contracts/Governor.sol

57    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

87    j++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87)


#

```
File: contracts/Governor.sol

84    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)


#

```
File: contracts/Governor.sol

76    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)


#

```
File: contracts/Governor.sol

98    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)


#

```
File: contracts/Governor.sol

111    j++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111)


#

```
File: contracts/Governor.sol

107    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)


#

```
File: contracts/Governor.sol

122    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/HintHelpers.sol

195    i++
```
 should use a prefix operation

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195)


</details>

# 


## Redundant Bool Comparison
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 9

### Description
This detector checks for instances where a boolean expression is compared to a boolean literal (true or false), which is redundant.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

332    require(redemptionsPaused == false, "CdpManager: Redemptions Paused")
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)


</details>

# 


## Redundant state variable getters
- Severity: Gas Optimization
- Confidence: High

### Description
Detects and reports state variables that have manually coded getters. Getters for public state variables are automatically generated in Solidity. Coding them manually is redundant and a waste of gas.

<details>

<summary>
There are 2 instances of this issue:

</summary>

###
#

```
File: contracts/SortedCdps.sol

130    function nonExistId() public pure override returns (bytes32) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130-L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130-L132)


#

```
File: contracts/SortedCdps.sol

548    function getMaxSize() external view override returns (uint256) 
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L548-L550](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L548-L550)


</details>

# 


## Consider activating via-ir for deploying
- Severity: Gas Optimization
- Confidence: Medium

### Description
The IR-based code generator was developed to make code generation more transparent and auditable, while also enabling powerful optimization passes that can be applied across functions. 

It is possible to activate the IR-based code generator through the command line by using the flag --via-ir or by including the option {'viaIR': true}. 

Keep in mind that compiling with this option may take longer. However, you can simply test it before deploying your code. If you find that it provides better performance, you can add the --via-ir flag to your deploy command.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#
 
</details>

# 


## Short-circuit rules can be used to optimize some gas usage
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 14700

### Description
Some conditions may be reordered to save an SLOAD (2100 gas), as we avoid reading state variables when the first part of the condition fails (with &&), or succeeds (with ||). For instance, consider a scenario where you have a `stateVariable` (a variable stored in contract storage) and a `localVariable` (a variable in memory). 

If you have a condition like `stateVariable > 0 && localVariable > 0`, if `localVariable > 0` is false, the Solidity runtime will still execute `stateVariable > 0`, which costs an SLOAD operation (2100 gas). However, if you reorder the condition to `localVariable > 0 && stateVariable > 0`, the `stateVariable > 0` check won't happen if `localVariable > 0` is false, saving you the SLOAD gas cost.

Similarly, for the `||` operator, if you have a condition like `stateVariable > 0 || localVariable > 0`, and `stateVariable > 0` is true, the Solidity runtime will still execute `localVariable > 0`. But if you reorder the condition to `localVariable > 0 || stateVariable > 0`, and `localVariable > 0` is true, the `stateVariable > 0` check won't happen, again saving you the SLOAD gas cost.

This detector checks for such conditions in the contract and reports if any condition could be optimized by taking advantage of the short-circuiting behavior of `&&` and `||`.

<details>

<summary>
There are 7 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```


```
 // @audit: Switch _maxFeePercentage <= DECIMAL_PRECISION && _maxFeePercentage >= redemptionFeeFloor 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/SortedCdps.sol

601    return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId)
```


```
 // @audit: Switch _NICR >= cdpManager.getCachedNominalICR(_nextId) && data.head == _nextId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L601](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L601)


#

```
File: contracts/SortedCdps.sol

644    data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)
```


```
 // @audit: Switch _NICR <= cdpManager.getCachedNominalICR(_startId) && data.tail == _startId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644)


#

```
File: contracts/SortedCdps.sol

604    return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId)
```


```
 // @audit: Switch _NICR <= cdpManager.getCachedNominalICR(_prevId) && data.tail == _prevId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604)


#

```
File: contracts/SortedCdps.sol

607    return
608                    data.nodes[_prevId].nextId == _nextId &&
609                    cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610                    _NICR >= cdpManager.getCachedNominalICR(_nextId)
```


```
 // @audit: Switch cdpManager.getCachedNominalICR(_prevId) >= _NICR && data.nodes[_prevId].nextId == _nextId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610)


#

```
File: contracts/SortedCdps.sol

607    return
608                    data.nodes[_prevId].nextId == _nextId &&
609                    cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610                    _NICR >= cdpManager.getCachedNominalICR(_nextId)
```


```
 // @audit: Switch _NICR >= cdpManager.getCachedNominalICR(_nextId) && data.nodes[_prevId].nextId == _nextId && cdpManager.getCachedNominalICR(_prevId) >= _NICR 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607-L610)


#

```
File: contracts/SortedCdps.sol

621    data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)
```


```
 // @audit: Switch _NICR >= cdpManager.getCachedNominalICR(_startId) && data.head == _startId 
```
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621)


</details>

# 


## Use Small Integer For Efficiency
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 30

### Description
This detector flags contracts that inefficiently use `uint` or `int` of sizes smaller than 32 bytes. The EVM operates on 32 bytes at a time, thus using elements smaller than this may cause your contract's gas usage to be higher. Refer to the Solidity documentation for more details: https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html.

<details>

<summary>
There are 5 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

21    uint128 public constant UNSET_TIMESTAMP = type(uint128).max
```
 `UNSET_TIMESTAMP` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21)


#

```
File: contracts/CdpManagerStorage.sol

22    uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes
```
 `MINIMUM_GRACE_PERIOD` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22)


#

```
File: contracts/CdpManagerStorage.sol

24    uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP
```
 `lastGracePeriodStartTimestamp` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24)


#

```
File: contracts/CdpManagerStorage.sol

25    uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD
```
 `recoveryModeGracePeriodDuration` use 256 bites instead of 128

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25)


#

```
File: contracts/EBTCToken.sol

31    uint8 internal constant _DECIMALS = 18
```
 `_DECIMALS` use 256 bites instead of 8

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L31)


</details>

# 


## Splitting Require Assert Statements
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 24

### Description
Instead of using operator && in a a single require clause split into multiple clauses to save gas.

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

734    require(
735                recoveredAddress != address(0) && recoveredAddress == _borrower,
736                "BorrowerOperations: Invalid signature"
737            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737)


#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/CdpManagerStorage.sol

261    require(
262                closedStatus != Status.nonExistent && closedStatus != Status.active,
263                "CdpManagerStorage: close non-exist or non-active CDP!"
264            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264)


#

```
File: contracts/CdpManagerStorage.sol

466    require(
467                cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468                "CdpManagerStorage: remove non-exist or non-active CDP!"
469            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469)


#

```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


#

```
File: contracts/EBTCToken.sol

296    require(
297                _recipient != address(0) && _recipient != address(this),
298                "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299)


#

```
File: contracts/EBTCToken.sol

300    require(
301                _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302                "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303)


#

```
File: contracts/PriceFeed.sol

79    require(
80                !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                    !_chainlinkIsFrozen(chainlinkResponse),
82                "PriceFeed: Chainlink must be working and current"
83            )
```
 split the condition:
	-

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83)


</details>

# 


## State variable access within a loop
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 8745

### Description
State variable reads and writes are more expensive than local variable reads and writes. Therefore, it is recommended to replace state variable reads and writes within loops with a local variable. Gas savings should be multiplied by the average loop length.

<details>

<summary>
There are 33 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManager.sol

369    currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369)


#

```
File: contracts/CdpManager.sol

370    _cId = sortedCdps.getPrev(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370)


#

```
File: contracts/CdpManager.sol

371    currentBorrower = sortedCdps.getOwnerAddress(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371)


#

```
File: contracts/CdpManager.sol

424    bytes32 _nextId = sortedCdps.getPrev(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424)


#

```
File: contracts/CdpManager.sol

425    address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L425)


#

```
File: contracts/CdpManager.sol

500    _id = sortedCdps.getNext(_id)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500)


#

```
File: contracts/Governor.sol

46    i < users.length()
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

47    address user = users.at(i)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47)


#

```
File: contracts/HintHelpers.sol

69    vars.currentCdpUser != address(0) &&
70                    cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L69-L70](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L69-L70)


#

```
File: contracts/HintHelpers.sol

72    vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L72)


#

```
File: contracts/HintHelpers.sol

73    vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73)


#

```
File: contracts/HintHelpers.sol

90    uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L90)


#

```
File: contracts/HintHelpers.sol

102    collateral.getPooledEthByShares(partialRedemptionNewColl) <
103                            MIN_NET_STETH_BALANCE
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102-L103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102-L103)


#

```
File: contracts/HintHelpers.sol

116    vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116)


#

```
File: contracts/HintHelpers.sol

117    vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L117)


#

```
File: contracts/HintHelpers.sol

185    bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L185)


#

```
File: contracts/HintHelpers.sol

186    uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L186)


#

```
File: contracts/LiquidationLibrary.sol

756    vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756)


#

```
File: contracts/LiquidationLibrary.sol

788    vars.backToNormalMode = _TCR < CCR ? false : true
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788)


#

```
File: contracts/LiquidationLibrary.sol

819    vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819)


#

```
File: contracts/SortedCdps.sol

185    _currentCdpId != dummyId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185)


#

```
File: contracts/SortedCdps.sol

199    _currentCdpId = data.nodes[_currentCdpId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L199)


#

```
File: contracts/SortedCdps.sol

248    _currentCdpId != dummyId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248)


#

```
File: contracts/SortedCdps.sol

256    _currentCdpId = data.nodes[_currentCdpId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256)


#

```
File: contracts/SortedCdps.sol

318    _currentCdpId != dummyId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318)


#

```
File: contracts/SortedCdps.sol

327    _currentCdpId = data.nodes[_currentCdpId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L327)


#

```
File: contracts/SortedCdps.sol

450    delete data.nodes[_ids[i]]
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L450)


#

```
File: contracts/SortedCdps.sol

629    prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629)


#

```
File: contracts/SortedCdps.sol

630    prevId = data.nodes[prevId].nextId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630)


#

```
File: contracts/SortedCdps.sol

631    nextId = data.nodes[prevId].nextId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L631](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L631)


#

```
File: contracts/SortedCdps.sol

652    nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652)


#

```
File: contracts/SortedCdps.sol

653    nextId = data.nodes[nextId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653)


#

```
File: contracts/SortedCdps.sol

654    prevId = data.nodes[nextId].prevId
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L654](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L654)


</details>

# 


## Superfluous event fields
- Severity: Gas Optimization
- Confidence: High

### Description
Block.timestamp and block.number are added to event information by default so adding them manually wastes gas.

<details>

<summary>
There are 1 instances of this issue:

</summary>

###
#

```
File: contracts/Interfaces/IPriceFeed.sol

13    event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);
```
The event `UnhealthyFallbackCaller` in the contract `IPriceFeed` includes the field `timestamp` which is superfluous:
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L13)


</details>

# 


## Cache Array Length Outside of Loop
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 9

### Description
When using arrays in a for loop, calling .length on every iteration will result in unnecessary gas expenses. Instead, it is recommended to cache the array length beforehand, which saves 3 gas per iteration. For storage arrays, an additional 100 gas per iteration (except the first) can be saved by pre-caching the length

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

57    i < _usrs.length
```
 caching the length of array
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

122    i < roleIds.length
```
 caching the length of array
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/Governor.sol

137    i < _sigs.length
```
 caching the length of array
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)


</details>

# 


## State variables should be cached in stack variables rather than re-reading them from storage
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 2813

### Description
State variables should be cached instead of re-reading them.Subsequent reads incur a 100 gas penalty.Caching such variables replaces the Gwarmaccess with much cheaper stack reads.

<details>

<summary>
There are 29 instances of this issue:

</summary>

###
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
 should cache the following state variables:
	- 
```
File: contracts/ActivePool.sol

31    uint256 internal systemCollShares
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261-L310)


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
 should cache the following state variables:
	- 
```
File: contracts/BorrowerOperations.sol

57    address public feeRecipientAddress
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077-L1108)


#

```
File: contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(
136            SingleRedemptionInputs memory _redeemColFromCdp
137        ) internal returns (SingleRedemptionValues memory singleRedemption) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135-L234)


#

```
File: contracts/CdpManager.sol

550    function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

205    bytes32[] public CdpIds
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550-L563)


#

```
File: contracts/CdpManager.sol

689    function _updateLastRedemptionTimestamp() internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

166    uint256 public lastRedemptionTimestamp
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689-L700](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L689-L700)


#

```
File: contracts/CdpManager.sol

709    function _minutesPassedSinceLastRedemption() internal view returns (uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

166    uint256 public lastRedemptionTimestamp
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709-L714](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L709-L714)


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
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L936)


#

```
File: contracts/CdpManagerStorage.sol

260    function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260-L280)


#

```
File: contracts/CdpManagerStorage.sol

410    function _removeStake(bytes32 _cdpId) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410-L415)


#

```
File: contracts/CdpManagerStorage.sol

441    function _computeNewStake(uint256 _coll) internal view returns (uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

176    uint256 public totalCollateralSnapshot
```

	- 
```
File: contracts/CdpManagerStorage.sol

173    uint256 public totalStakesSnapshot
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441-L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441-L457)


#

```
File: contracts/CdpManagerStorage.sol

463    function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```

	- 
```
File: contracts/CdpManagerStorage.sol

205    bytes32[] public CdpIds
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463-L484)


#

```
File: contracts/CdpManagerStorage.sol

616    function getAccumulatedFeeSplitApplied(
617            bytes32 _cdpId,
618            uint256 _systemStEthFeePerUnitIndex
619        ) public view returns (uint256, uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

168    mapping(bytes32 => Cdp) public Cdps
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616-L645](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616-L645)


#

```
File: contracts/CdpManagerStorage.sol

761    function _calcSyncedGlobalAccounting(
762            uint256 _newIndex,
763            uint256 _oldIndex
764        ) internal view returns (uint256, uint256, uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

198    uint256 public override systemStEthFeePerUnitIndex
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761-L779](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761-L779)


#

```
File: contracts/EBTCToken.sol

246    function _transfer(address sender, address recipient, uint256 amount) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/EBTCToken.sol

51    mapping(address => uint256) private _balances
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L246-L260)


#

```
File: contracts/LiquidationLibrary.sol

862    function _redistributeDebt(uint256 _debt) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/CdpManagerStorage.sol

187    uint256 public systemDebtRedistributionIndex
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862-L892)


#

```
File: contracts/PriceFeed.sol

98    function fetchPrice() external override returns (uint256) 
```
 should cache the following state variables:
	- 
```
File: contracts/PriceFeed.sol

48    Status public status
```

	- 
```
File: contracts/PriceFeed.sol

45    uint256 public lastGoodPrice
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98-L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98-L352)


#

```
File: contracts/PriceFeed.sol

358    function setFallbackCaller(address _fallbackCaller) external requiresAuth 
```
 should cache the following state variables:
	- 
```
File: contracts/PriceFeed.sol

29    IFallbackCaller public fallbackCaller
```


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
 should cache the following state variables:
	- 
```
File: contracts/PriceFeed.sol

29    IFallbackCaller public fallbackCaller
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582-L602)


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
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173-L210](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L173-L210)


#

```
File: contracts/SortedCdps.sol

237    function _cdpCountOf(
238            address owner,
239            bytes32 startNodeId,
240            uint maxNodes
241        ) internal view returns (uint256, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L237-L264)


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
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
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
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

79    uint256 public nextCdpNonce
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L361](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344-L361)


#

```
File: contracts/SortedCdps.sol

363    function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363-L406)


#

```
File: contracts/SortedCdps.sol

419    function batchRemove(bytes32[] memory _ids) external override 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419-L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419-L454)


#

```
File: contracts/SortedCdps.sol

456    function _remove(bytes32 _id) internal 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456-L491)


#

```
File: contracts/SortedCdps.sol

519    function contains(bytes32 _id) public view override returns (bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L519-L526](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L519-L526)


#

```
File: contracts/SortedCdps.sol

591    function _validInsertPosition(
592            uint256 _NICR,
593            bytes32 _prevId,
594            bytes32 _nextId
595        ) internal view returns (bool) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591-L612](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591-L612)


#

```
File: contracts/SortedCdps.sol

619    function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L619-L635](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L619-L635)


#

```
File: contracts/SortedCdps.sol

642    function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) 
```
 should cache the following state variables:
	- 
```
File: contracts/SortedCdps.sol

77    Data public data
```


[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642-L658)


</details>

# 


## Safe Subtraction Should Be Unchecked
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 935

### Description
This detector identifies subtraction operations where the subtraction could safely be unchecked. This occurs when a prior if-statement or require() function ensures that the first operand (minuend) is greater than or equal to the second operand (subtrahend). In these cases, an unchecked subtraction would not result in an underflow error, and can save gas by skipping the redundant check.

<details>

<summary>
There are 11 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

557    uint256 deltaIndex = _newIndex - _prevIndex
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManagerStorage.sol

556    require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index")
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L557](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L557)


#

```
File: contracts/CdpManagerStorage.sol

637    return (
638                    _feeSplitDistributed,
639                    (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
640                )
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManagerStorage.sol

636    _scaledCdpColl > _feeSplitDistributed
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L637-L640](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L637-L640)


#

```
File: contracts/CdpManager.sol

690    uint256 timePassed = block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManager.sol

690    uint256 timePassed = block.timestamp > lastRedemptionTimestamp
691                ? block.timestamp - lastRedemptionTimestamp
692                : 0
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L690-L692)


#

```
File: contracts/CdpManager.sol

710    return
711                block.timestamp > lastRedemptionTimestamp
712                    ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
713                    : 0
```
 should be unchecked because there is check:<br>
```
File: contracts/CdpManager.sol

710    return
711                block.timestamp > lastRedemptionTimestamp
712                    ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
713                    : 0
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L710-L713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L710-L713)


#

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
 should be unchecked because there is check:<br>
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
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367-L376)


#

```
File: contracts/LiquidationLibrary.sol

567    collSurplus = _totalColToSend - toLiquidator
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

564    assert(toLiquidator < _totalColToSend)
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L567)


#

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
 should be unchecked because there is check:<br>
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
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281-L290)


#

```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
 should be unchecked because there is check:<br>
```
File: contracts/LiquidationLibrary.sol

594    debtToRedistribute = _debtToRepay < _totalDebtToBurn
595                    ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)
596                    : 0
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594-L596)


#

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
 should be unchecked because there is check:<br>
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
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437-L445)


#

```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
 should be unchecked because there is check:<br>
```
File: contracts/PriceFeed.sol

797    uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
798                ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)
799                : 10 ** (_ethBtcDecimals - _stEthEthDecimals)
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L797-L799)


#

```
File: contracts/SortedCdps.sol

425    bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId
```
 should be unchecked because there is check:<br>
```
File: contracts/SortedCdps.sol

422    require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!")
```
<br><br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L425)


</details>

# 


## Detection of Unnecessary Checked Increments in Solidity Loop Statements
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 600

### Description
Smart contract code that contains checked increments (++i) within loops.Those operations not require overflow checking. In these cases, it is more efficient to use unchecked{++i} or unchecked{i++} to save on gas costs, as this keyword was introduced in Solidity version 0.8.0. By using unchecked, unnecessary overflow checks can be avoided, resulting in a savings of 30-40 gas per loop iteration.

<details>

<summary>
There are 10 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

46    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

57    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

76    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)


#

```
File: contracts/Governor.sol

84    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)


#

```
File: contracts/Governor.sol

98    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)


#

```
File: contracts/Governor.sol

107    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)


#

```
File: contracts/Governor.sol

122    i++
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/Governor.sol

137    ++i
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)


#

```
File: contracts/SortedCdps.sol

432    ++i
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)


#

```
File: contracts/SortedCdps.sol

449    ++i
```
 should be inside uncheck block
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449)


</details>

# 


## Avoid Unnecessary Computation Inside Loops
- Severity: Gas Optimization
- Confidence: High

### Description
This detector identifies instances of computations being performed inside loops that could be performed outside the loop to save gas.

Unnecessary computation inside loops:

Any computation performed inside a loop that doesn't change with each iteration can be moved outside the loop to save gas.This detector identifies instances where the following unnecessary computations are performed inside loops:

- 1 Local variables are read inside loops but never modified within the same loop, indicating they could be cached outside the loop.

- 2 Computations involving constant expressions (literals) which result in the same output in every loop iteration.

By addressing these issues, gas usage can be optimized.

<details>

<summary>
There are 3 instances of this issue:

</summary>

###
#

```
File: contracts/SortedCdps.sol

202    maxNodes > 0 && i >= maxNodes
```
The following computations can be cached outside of loops for gas optimization `maxNodes > 0`<br>.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202)


#

```
File: contracts/SortedCdps.sol

259    maxNodes > 0 && i >= maxNodes
```
The following computations can be cached outside of loops for gas optimization `maxNodes > 0`<br>.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259)


#

```
File: contracts/SortedCdps.sol

330    maxNodes > 0 && i >= maxNodes
```
The following computations can be cached outside of loops for gas optimization `maxNodes > 0`<br>.
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330)


</details>

# 


## Redundant Contract Existence Check in Consecutive External Calls
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 800

### Description
This detector identifies instances where there are consecutive external calls to the same contract, where the subsequent calls could use a low-level call to save gas.

Note: This detector only triggers if the function call does not return any value. 

Prior to 0.8.10, the compiler inserted extra code, including EXTCODESIZE (100 gas), to check for contract existence for external function calls. In more recent Solidity versions the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low-level calls never check for contract existence. 

<details>

<summary>
There are 8 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

410    cdpManager.updateCdp(
411                _cdpId,
412                _borrower,
413                vars.collShares,
414                vars.debt,
415                vars.newCollShares,
416                vars.newDebt
417            )
```
This call could be replaced with a low-level call because the contract `ICdpManager` has already been checked in <br>`Line: 343    cdpManager.syncAccounting(_cdpId)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L410-L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L410-L417)


#

```
File: contracts/BorrowerOperations.sol

497    cdpManager.notifyStartGracePeriod(newTCR)
```
This call could be replaced with a low-level call because the contract `ICdpManager` has already been checked in <br>`Line: 457    cdpManager.syncGlobalAccounting()`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L497)


#

```
File: contracts/BorrowerOperations.sol

581    cdpManager.notifyEndGracePeriod(newTCR)
```
This call could be replaced with a low-level call because the contract `ICdpManager` has already been checked in <br>`Line: 559    cdpManager.syncAccounting(_cdpId)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L581](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L581)


#

```
File: contracts/BorrowerOperations.sol

1103    ebtcToken.burn(feeRecipientAddress, amount)
```
This call could be replaced with a low-level call because the contract `IEBTCToken` has already been checked in <br>`Line: 1088    ebtcToken.mint(address(receiver), amount)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103)


#

```
File: contracts/CdpManager.sol

260    activePool.transferSystemCollSharesAndLiquidatorReward(
261                address(collSurplusPool),
262                _collSurplus,
263                _liquidatorRewardShares
264            )
```
This call could be replaced with a low-level call because the contract `IActivePool` has already been checked in <br>`Line: 254    activePool.decreaseSystemDebt(_EBTC)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L260-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L260-L264)


#

```
File: contracts/CdpManager.sol

481    activePool.allocateSystemCollSharesToFeeRecipient(totals.feeCollShares)
```
This call could be replaced with a low-level call because the contract `IActivePool` has already been checked in <br>`Line: 478    activePool.decreaseSystemDebt(totals.debtToRedeem)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L481)


#

```
File: contracts/LeverageMacroBase.sol

427    IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0)
```
This call could be replaced with a low-level call because the contract `SafeERC20` has already been checked in <br>`Line: 405    IERC20(swapData.tokenForSwap).safeApprove(
            swapData.addressForApprove,
            swapData.exactApproveAmount
        )`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)


#

```
File: contracts/LiquidationLibrary.sol

536    activePool.transferSystemCollSharesAndLiquidatorReward(
537                msg.sender,
538                totalCollSharesToSend,
539                totalLiquidatorRewardCollShares
540            )
```
This call could be replaced with a low-level call because the contract `IActivePool` has already been checked in <br>`Line: 533    activePool.decreaseSystemDebt(totalDebtToBurn)`<br>
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L536-L540](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L536-L540)


</details>

# 


## Initialize Variables With Default Value
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 102

### Description
It costs more gas to initialize variables to their default values than to let the default be applied.

<details>

<summary>
There are 17 instances of this issue:

</summary>

###
#

```
File: contracts/Governor.sol

46    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)


#

```
File: contracts/Governor.sol

54    uint256 j = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54)


#

```
File: contracts/Governor.sol

57    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57)


#

```
File: contracts/Governor.sol

76    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76)


#

```
File: contracts/Governor.sol

82    uint256 j = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82)


#

```
File: contracts/Governor.sol

84    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84)


#

```
File: contracts/Governor.sol

98    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98)


#

```
File: contracts/Governor.sol

105    uint256 j = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L105)


#

```
File: contracts/Governor.sol

107    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107)


#

```
File: contracts/Governor.sol

122    uint8 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)


#

```
File: contracts/Governor.sol

137    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137)


#

```
File: contracts/SortedCdps.sol

182    uint _currentIndex = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182)


#

```
File: contracts/SortedCdps.sol

245    uint _ownedCount = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245)


#

```
File: contracts/SortedCdps.sol

246    uint i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246)


#

```
File: contracts/SortedCdps.sol

311    uint i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311)


#

```
File: contracts/SortedCdps.sol

432    uint256 i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432)


#

```
File: contracts/SortedCdps.sol

449    uint i = 0
```
 no need to initialized with default value
 
[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449)


</details>

# 


## Unused Named Return Variables
- Severity: Gas Optimization
- Confidence: High

### Description
Named return variables allow for clear and explicit naming of values to be returned from a function. However, when these variables are unused, it can lead to confusion and make the code less maintainable.

<details>

<summary>
There are 4 instances of this issue:

</summary>

###
#

```
File: contracts/CdpManagerStorage.sol

719    function getPendingRedistributedDebt(
720            bytes32 _cdpId
721        ) public view returns (uint256 pendingEBTCDebtReward) 
```
there is not use of this variables:
@ **pendingEBTCDebtReward**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719-L724](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719-L724)


#

```
File: contracts/CdpManager.sol

570    function getSystemDebt() public view returns (uint256 entireSystemDebt) 
```
there is not use of this variables:
@ **entireSystemDebt**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570-L572](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570-L572)


#

```
File: contracts/Governor.sol

146    function getRoleName(uint8 role) external view returns (string memory roleName) 
```
there is not use of this variables:
@ **roleName**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146-L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146-L148)


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
there is not use of this variables:
@ **debtToRedistribute**

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544-L568)


</details>

# 


## Use assembly to write address storage values
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 1848

### Description
Using assembly to write address storage values can potentially save gas costs. This detector flags instances where address storage values are written without using assembly.

<details>

<summary>
There are 24 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

57    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L57)


#

```
File: contracts/ActivePool.sol

53    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53)


#

```
File: contracts/ActivePool.sol

54    cdpManagerAddress = _cdpManagerAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L54)


#

```
File: contracts/ActivePool.sol

56    collSurplusPoolAddress = _collSurplusAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L56)


#

```
File: contracts/ActivePool.sol

398    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398)


#

```
File: contracts/BorrowerOperations.sol

121    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L121)


#

```
File: contracts/BorrowerOperations.sol

1148    feeRecipientAddress = _feeRecipientAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148)


#

```
File: contracts/CdpManagerStorage.sol

229    liquidationLibrary = _liquidationLibraryAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229)


#

```
File: contracts/CdpManagerStorage.sol

233    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233)


#

```
File: contracts/CollSurplusPool.sol

50    activePoolAddress = _activePoolAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L50)


#

```
File: contracts/CollSurplusPool.sol

52    feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress()
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52)


#

```
File: contracts/CollSurplusPool.sol

48    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48)


#

```
File: contracts/CollSurplusPool.sol

49    cdpManagerAddress = _cdpManagerAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L49)


#

```
File: contracts/EBTCToken.sol

68    cdpManagerAddress = _cdpManagerAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68)


#

```
File: contracts/EBTCToken.sol

69    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L69)


#

```
File: contracts/LeverageMacroFactory.sol

31    cdpManager = _cdpManager
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L31)


#

```
File: contracts/LeverageMacroFactory.sol

30    activePool = _activePool
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L30)


#

```
File: contracts/LeverageMacroFactory.sol

32    ebtcToken = _ebtc
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L32)


#

```
File: contracts/LeverageMacroFactory.sol

33    stETH = _coll
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L33)


#

```
File: contracts/LeverageMacroFactory.sol

34    sortedCdps = _sortedCdps
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L34)


#

```
File: contracts/LeverageMacroFactory.sol

29    borrowerOperations = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29)


#

```
File: contracts/LeverageMacroReference.sol

36    theOwner = _owner
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36)


#

```
File: contracts/SimplifiedDiamondLike.sol

45    owner = _owner
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45)


#

```
File: contracts/SortedCdps.sol

96    borrowerOperationsAddress = _borrowerOperationsAddress
```
writes to an address storage value without using assembly.

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L96)


</details>

# 


## Use Assembly for Hash Calculation
- Severity: Gas Optimization
- Confidence: Medium
- Total Gas Saved: 960

### Description
Detects places in the code where hash calculation could be done using inline assembly to optimize gas usage.

<details>

<summary>
There are 12 instances of this issue:

</summary>

###
#

```
File: contracts/BorrowerOperations.sol

129    bytes32 hashedVersion = keccak256(bytes(_VERSION))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129)


#

```
File: contracts/BorrowerOperations.sol

682    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682)


#

```
File: contracts/BorrowerOperations.sol

128    bytes32 hashedName = keccak256(bytes(NAME))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128)


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
File: contracts/BorrowerOperations.sol

32    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33            keccak256(
34                "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35            )
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35)


#

```
File: contracts/EBTCToken.sol

71    bytes32 hashedName = keccak256(bytes(_NAME))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71)


#

```
File: contracts/EBTCToken.sol

72    bytes32 hashedVersion = keccak256(bytes(_VERSION))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72)


#

```
File: contracts/EBTCToken.sol

240    return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)


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


#

```
File: contracts/HintHelpers.sol

182    latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)))
```

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)


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


## Usage of Custom Errors for Gas Efficiency
- Severity: Gas Optimization
- Confidence: High
- Total Gas Saved: 41952

### Description
This detector flags functions that use revert()/require() strings, which are less gas efficient than custom errors. Custom errors, available from Solidity version 0.8.4, save approximately 50 gas each time they're used by avoiding the need to allocate and store the revert string.

<details>

<summary>
There are 152 instances of this issue:

</summary>

###
#

```
File: contracts/ActivePool.sol

104    require(cachedSystemCollShares >= _shares, "!ActivePoolBal")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104)


#

```
File: contracts/ActivePool.sol

137    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137)


#

```
File: contracts/ActivePool.sol

162    require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162)


#

```
File: contracts/ActivePool.sol

220    require(
221                msg.sender == borrowerOperationsAddress,
222                "ActivePool: Caller is not BorrowerOperations"
223            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220-L223)


#

```
File: contracts/ActivePool.sol

228    require(
229                msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230                "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228-L231)


#

```
File: contracts/ActivePool.sol

236    require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236)


#

```
File: contracts/ActivePool.sol

267    require(amount > 0, "ActivePool: 0 Amount")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267)


#

```
File: contracts/ActivePool.sol

269    require(amount <= maxFlashLoan(token), "ActivePool: Too much")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269)


#

```
File: contracts/ActivePool.sol

277    require(
278                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279                "ActivePool: IERC3156: Callback failed"
280            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277-L280)


#

```
File: contracts/ActivePool.sol

294    require(
295                collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296                "ActivePool: Must repay Balance"
297            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294-L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294-L297)


#

```
File: contracts/ActivePool.sol

298    require(
299                collateral.sharesOf(address(this)) >= systemCollShares,
300                "ActivePool: Must repay Share"
301            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L298-L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L298-L301)


#

```
File: contracts/ActivePool.sol

302    require(
303                collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304                "ActivePool: Should keep same collateral share rate"
305            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302-L305)


#

```
File: contracts/ActivePool.sol

318    require(token == address(collateral), "ActivePool: collateral Only")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L318)


#

```
File: contracts/ActivePool.sol

319    require(!flashLoansPaused, "ActivePool: Flash Loans Paused")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L319](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L319)


#

```
File: contracts/ActivePool.sol

350    require(
351                cachedFeeRecipientCollShares >= _shares,
352                "ActivePool: Insufficient fee recipient coll"
353            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350-L353)


#

```
File: contracts/ActivePool.sol

374    require(token != address(collateral), "ActivePool: Cannot Sweep Collateral")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374)


#

```
File: contracts/ActivePool.sol

377    require(amount <= balance, "ActivePool: Attempt to sweep more than balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377)


#

```
File: contracts/ActivePool.sol

393    require(
394                _feeRecipientAddress != address(0),
395                "ActivePool: Cannot set fee recipient to zero address"
396            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393-L396)


#

```
File: contracts/ActivePool.sol

407    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)


#

```
File: contracts/BorrowerOperations.sol

368    require(
369                _stEthBalanceDecrease <= _cdpStEthBalance,
370                "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368-L371)


#

```
File: contracts/BorrowerOperations.sol

463    require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463)


#

```
File: contracts/BorrowerOperations.sol

541    require(
542                vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543                "BorrowerOperations: deposited collateral mismatch!"
544            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541-L544)


#

```
File: contracts/BorrowerOperations.sol

715    require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715)


#

```
File: contracts/BorrowerOperations.sol

734    require(
735                recoveredAddress != address(0) && recoveredAddress == _borrower,
736                "BorrowerOperations: Invalid signature"
737            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737)


#

```
File: contracts/BorrowerOperations.sol

807    require(
808                _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809                "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807-L810)


#

```
File: contracts/BorrowerOperations.sol

818    require(
819                _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820                "BorrowerOperations: There must be either a collateral change or a debt change"
821            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818-L821)


#

```
File: contracts/BorrowerOperations.sol

826    require(status == 1, "BorrowerOperations: Cdp does not exist or is closed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826)


#

```
File: contracts/BorrowerOperations.sol

831    require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831)


#

```
File: contracts/BorrowerOperations.sol

835    require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835)


#

```
File: contracts/BorrowerOperations.sol

839    require(
840                !_checkRecoveryModeForTCR(_tcr),
841                "BorrowerOperations: Operation not permitted during Recovery Mode"
842            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839-L842)


#

```
File: contracts/BorrowerOperations.sol

846    require(
847                _stEthBalanceDecrease == 0,
848                "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846-L849)


#

```
File: contracts/BorrowerOperations.sol

911    require(
912                _newICR >= MCR,
913                "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"
914            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911-L914)


#

```
File: contracts/BorrowerOperations.sol

918    require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918)


#

```
File: contracts/BorrowerOperations.sol

922    require(
923                _newICR >= _oldICR,
924                "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922-L925)


#

```
File: contracts/BorrowerOperations.sol

929    require(
930                _newTCR >= CCR,
931                "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929-L932)


#

```
File: contracts/BorrowerOperations.sol

936    require(_debt > 0, "BorrowerOperations: Debt must be non-zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936)


#

```
File: contracts/BorrowerOperations.sol

940    require(
941                _stEthBalance >= MIN_NET_STETH_BALANCE,
942                "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
943            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940-L943)


#

```
File: contracts/BorrowerOperations.sol

947    require(
948                _debtRepayment <= _currentDebt,
949                "BorrowerOperations: Amount repaid must not be larger than the Cdp's debt"
950            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947-L950)


#

```
File: contracts/BorrowerOperations.sol

957    require(
958                ebtcToken.balanceOf(_account) >= _debtRepayment,
959                "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957-L960)


#

```
File: contracts/BorrowerOperations.sol

970    require(
971                _approval != PositionManagerApproval.None,
972                "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"
973            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970-L973)


#

```
File: contracts/BorrowerOperations.sol

1083    require(amount > 0, "BorrowerOperations: 0 Amount")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083)


#

```
File: contracts/BorrowerOperations.sol

1085    require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085)


#

```
File: contracts/BorrowerOperations.sol

1091    require(
1092                receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
1093                "IERC3156: Callback failed"
1094            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094)


#

```
File: contracts/BorrowerOperations.sol

1115    require(token == address(ebtcToken), "BorrowerOperations: EBTC Only")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1115)


#

```
File: contracts/BorrowerOperations.sol

1116    require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116)


#

```
File: contracts/BorrowerOperations.sol

1141    require(
1142                _feeRecipientAddress != address(0),
1143                "BorrowerOperations: Cannot set feeRecipient to zero address"
1144            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144)


#

```
File: contracts/BorrowerOperations.sol

1155    require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155)


#

```
File: contracts/BorrowerOperations.sol

145    require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145)


#

```
File: contracts/BorrowerOperations.sol

146    require(
147                ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148                "CdpManager: Reentrancy in nonReentrant call"
149            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146-L149)


#

```
File: contracts/CdpManager.sol

332    require(redemptionsPaused == false, "CdpManager: Redemptions Paused")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)


#

```
File: contracts/CdpManager.sol

431    require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431)


#

```
File: contracts/CdpManager.sol

502    require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502)


#

```
File: contracts/CdpManager.sol

503    require(
504                _toRemoveIds[_total - 1] == _end,
505                "CdpManager: batchRemoveSortedCdpIds check end error"
506            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503-L506)


#

```
File: contracts/CdpManager.sol

626    require(newBaseRate > 0, "CdpManager: new baseRate is zero!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626)


#

```
File: contracts/CdpManager.sol

672    require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672)


#

```
File: contracts/CdpManager.sol

678    require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678)


#

```
File: contracts/CdpManager.sol

743    require(
744                callerBalance >= _amount,
745                "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743-L746)


#

```
File: contracts/CdpManager.sol

747    require(
748                callerBalance <= _totalSupply,
749                "CdpManager: redeemer's EBTC balance exceeds total supply!"
750            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747-L750)


#

```
File: contracts/CdpManager.sol

754    require(_amount > 0, "CdpManager: Amount must be greater than zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)


#

```
File: contracts/CdpManager.sol

758    require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758)


#

```
File: contracts/CdpManager.sol

762    require(
763                _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764                "Max fee percentage must be between redemption fee floor and 100%"
765            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762-L765)


#

```
File: contracts/CdpManager.sol

774    require(
775                _stakingRewardSplit <= MAX_REWARD_SPLIT,
776                "CDPManager: new staking reward split exceeds max"
777            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774-L777)


#

```
File: contracts/CdpManager.sol

789    require(
790                _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791                "CDPManager: new redemption fee floor is lower than minimum"
792            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789-L792)


#

```
File: contracts/CdpManager.sol

793    require(
794                _redemptionFeeFloor <= DECIMAL_PRECISION,
795                "CDPManager: new redemption fee floor is higher than maximum"
796            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793-L796)


#

```
File: contracts/CdpManager.sol

808    require(
809                _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810                "CDPManager: new minute decay factor out of range"
811            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808-L811)


#

```
File: contracts/CdpManager.sol

812    require(
813                _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814                "CDPManager: new minute decay factor out of range"
815            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812-L815)


#

```
File: contracts/CdpManagerStorage.sol

112    require(
113                _gracePeriod >= MINIMUM_GRACE_PERIOD,
114                "CdpManager: Grace period below minimum duration"
115            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112-L115)


#

```
File: contracts/CdpManagerStorage.sol

261    require(
262                closedStatus != Status.nonExistent && closedStatus != Status.active,
263                "CdpManagerStorage: close non-exist or non-active CDP!"
264            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264)


#

```
File: contracts/CdpManagerStorage.sol

453    require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453)


#

```
File: contracts/CdpManagerStorage.sol

466    require(
467                cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468                "CdpManagerStorage: remove non-exist or non-active CDP!"
469            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469)


#

```
File: contracts/CdpManagerStorage.sol

475    require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475)


#

```
File: contracts/CdpManagerStorage.sol

556    require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556)


#

```
File: contracts/CdpManagerStorage.sol

584    require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584)


#

```
File: contracts/CdpManagerStorage.sol

649    require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649)


#

```
File: contracts/CdpManagerStorage.sol

653    require(
654                CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655                "CdpManager: Only one cdp in the system"
656            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


#

```
File: contracts/CdpManagerStorage.sol

660    require(
661                msg.sender == borrowerOperationsAddress,
662                "CdpManager: Caller is not the BorrowerOperations contract"
663            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660-L663)


#

```
File: contracts/CdpManagerStorage.sol

242    require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242)


#

```
File: contracts/CdpManagerStorage.sol

243    require(
244                ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245                "BorrowerOperations: Reentrancy in nonReentrant call"
246            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243-L246)


#

```
File: contracts/CollSurplusPool.sol

92    require(claimableColl > 0, "CollSurplusPool: No collateral available to claim")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)


#

```
File: contracts/CollSurplusPool.sol

99    require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99)


#

```
File: contracts/CollSurplusPool.sol

113    require(
114                msg.sender == borrowerOperationsAddress,
115                "CollSurplusPool: Caller is not Borrower Operations"
116            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113-L116)


#

```
File: contracts/CollSurplusPool.sol

120    require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120)


#

```
File: contracts/CollSurplusPool.sol

124    require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124)


#

```
File: contracts/CollSurplusPool.sol

143    require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143)


#

```
File: contracts/CollSurplusPool.sol

146    require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146)


#

```
File: contracts/EBTCToken.sol

144    require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144)


#

```
File: contracts/EBTCToken.sol

165    require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165)


#

```
File: contracts/EBTCToken.sol

208    require(deadline >= block.timestamp, "EBTC: expired deadline")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L208](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L208)


#

```
File: contracts/EBTCToken.sol

219    require(recoveredAddress == owner, "EBTC: invalid signature")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L219)


#

```
File: contracts/EBTCToken.sol

247    require(sender != address(0), "EBTCToken: zero sender!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247)


#

```
File: contracts/EBTCToken.sol

248    require(recipient != address(0), "EBTCToken: zero recipient!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248)


#

```
File: contracts/EBTCToken.sol

251    require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251)


#

```
File: contracts/EBTCToken.sol

263    require(account != address(0), "EBTCToken: mint to zero recipient!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263)


#

```
File: contracts/EBTCToken.sol

271    require(account != address(0), "EBTCToken: burn from zero account!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271)


#

```
File: contracts/EBTCToken.sol

274    require(cachedBalance >= amount, "ERC20: burn amount exceeds balance")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274)


#

```
File: contracts/EBTCToken.sol

286    require(owner != address(0), "EBTCToken: zero approve owner!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286)


#

```
File: contracts/EBTCToken.sol

287    require(spender != address(0), "EBTCToken: zero approve spender!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287)


#

```
File: contracts/EBTCToken.sol

296    require(
297                _recipient != address(0) && _recipient != address(this),
298                "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296-L299)


#

```
File: contracts/EBTCToken.sol

300    require(
301                _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302                "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300-L303)


#

```
File: contracts/EBTCToken.sol

307    require(
308                msg.sender == borrowerOperationsAddress,
309                "EBTCToken: Caller is not BorrowerOperations"
310            )
```
 use custom error instead 

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
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315-L320)


#

```
File: contracts/EBTCToken.sol

324    require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324)


#

```
File: contracts/LeverageMacroBase.sol

40    revert("Must be overridden")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40)


#

```
File: contracts/LeverageMacroBase.sol

45    require(owner() == msg.sender, "Must be owner")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45)


#

```
File: contracts/LeverageMacroBase.sol

179    require(
180                    cdpInfo.status == checkParams.expectedStatus,
181                    "!LeverageMacroReference: openCDP status check"
182                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179-L182)


#

```
File: contracts/LeverageMacroBase.sol

191    require(
192                    cdpInfo.status == checkParams.expectedStatus,
193                    "!LeverageMacroReference: adjustCDP status check"
194                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191-L194)


#

```
File: contracts/LeverageMacroBase.sol

201    require(
202                    cdpInfo.status == checkParams.expectedStatus,
203                    "!LeverageMacroReference: closeCDP status check"
204                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201-L204)


#

```
File: contracts/LeverageMacroBase.sol

249    require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249)


#

```
File: contracts/LeverageMacroBase.sol

251    require(check.value <= valueToCheck, "!LeverageMacroReference: let post check")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251)


#

```
File: contracts/LeverageMacroBase.sol

253    require(check.value == valueToCheck, "!LeverageMacroReference: equal post check")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253)


#

```
File: contracts/LeverageMacroBase.sol

255    revert("Operator not found")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L255)


#

```
File: contracts/LeverageMacroBase.sol

352    require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352)


#

```
File: contracts/LeverageMacroBase.sol

356    require(
357                    msg.sender == address(borrowerOperations),
358                    "LeverageMacroReference: wrong lender for eBTC flashloan"
359                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356-L359)


#

```
File: contracts/LeverageMacroBase.sol

362    require(
363                    msg.sender == address(activePool),
364                    "LeverageMacroReference: wrong lender for stETH flashloan"
365                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362-L365)


#

```
File: contracts/LeverageMacroBase.sol

421    require(success, "Call has failed")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L421)


#

```
File: contracts/LeverageMacroBase.sol

440    require(
441                        IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442                            swapChecks[i].expectedMinOut,
443                        "LeverageMacroReference: swap check failure!"
444                    )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440-L444)


#

```
File: contracts/LeverageMacroBase.sol

452    require(addy != address(borrowerOperations))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452)


#

```
File: contracts/LeverageMacroBase.sol

453    require(addy != address(sortedCdps))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453)


#

```
File: contracts/LeverageMacroBase.sol

454    require(addy != address(activePool))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454)


#

```
File: contracts/LeverageMacroBase.sol

455    require(addy != address(cdpManager))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455)


#

```
File: contracts/LeverageMacroBase.sol

456    require(addy != address(this))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456)


#

```
File: contracts/LiquidationLibrary.sol

56    require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56)


#

```
File: contracts/LiquidationLibrary.sol

82    require(
83                    _checkICRAgainstLiqThreshold(_ICR, _TCR),
84                    "LiquidationLibrary: ICR is not below liquidation threshold in current mode"
85                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82-L85)


#

```
File: contracts/LiquidationLibrary.sol

89    require(
90                    cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP,
91                    "LiquidationLibrary: Recovery Mode grace period not started"
92                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89-L92)


#

```
File: contracts/LiquidationLibrary.sol

93    require(
94                    block.timestamp >
95                        cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96                    "LiquidationLibrary: Recovery mode grace period still in effect"
97                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97)


#

```
File: contracts/LiquidationLibrary.sol

477    require(
478                    getCachedICR(_cdpId, _partialState.price) >= _partialState.ICR,
479                    "LiquidationLibrary: !_newICR>=_ICR"
480                )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477-L480)


#

```
File: contracts/LiquidationLibrary.sol

680    require(
681                _cdpArray.length != 0,
682                "LiquidationLibrary: Calldata address array must not be empty"
683            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680-L683)


#

```
File: contracts/LiquidationLibrary.sol

710    require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710)


#

```
File: contracts/LiquidationLibrary.sol

901    require(
902                (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903                    _entireDebt,
904                "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901-L905)


#

```
File: contracts/LiquidationLibrary.sol

909    require(
910                _entireColl >= MIN_NET_STETH_BALANCE,
911                "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909-L912)


#

```
File: contracts/PriceFeed.sol

79    require(
80                !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                    !_chainlinkIsFrozen(chainlinkResponse),
82                "PriceFeed: Chainlink must be working and current"
83            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79-L83)


#

```
File: contracts/SimplifiedDiamondLike.sol

52    require(msg.sender == owner)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52)


#

```
File: contracts/SimplifiedDiamondLike.sol

56    require(sig != 0x94b24d09)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56)


#

```
File: contracts/SimplifiedDiamondLike.sol

67    require(msg.sender == owner)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67)


#

```
File: contracts/SimplifiedDiamondLike.sol

77    require(msg.sender == address(this))
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77)


#

```
File: contracts/SimplifiedDiamondLike.sol

111    require(msg.sender == owner, "Must be owner")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111)


#

```
File: contracts/SimplifiedDiamondLike.sol

154    require(success)
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154)


#

```
File: contracts/SimplifiedDiamondLike.sol

179    require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179)


#

```
File: contracts/SimplifiedDiamondLike.sol

187    require(facet != address(0), "Diamond: Function does not exist")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187)


#

```
File: contracts/SortedCdps.sol

352    require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352)


#

```
File: contracts/SortedCdps.sol

365    require(!isFull(), "SortedCdps: List is full")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L365)


#

```
File: contracts/SortedCdps.sol

367    require(!contains(_id), "SortedCdps: List already contains the node")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367)


#

```
File: contracts/SortedCdps.sol

369    require(_id != dummyId, "SortedCdps: Id cannot be zero")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369)


#

```
File: contracts/SortedCdps.sol

371    require(_NICR > 0, "SortedCdps: NICR must be positive")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371)


#

```
File: contracts/SortedCdps.sol

422    require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422)


#

```
File: contracts/SortedCdps.sol

427    require(
428                _firstPrev != dummyId || _lastNext != dummyId,
429                "SortedCdps: batchRemove() leave ZERO node left!"
430            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427-L430)


#

```
File: contracts/SortedCdps.sol

433    require(contains(_ids[i]), "SortedCdps: List does not contain the id")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433)


#

```
File: contracts/SortedCdps.sol

458    require(contains(_id), "SortedCdps: List does not contain the id")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458)


#

```
File: contracts/SortedCdps.sol

506    require(contains(_id), "SortedCdps: List does not contain the id")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506)


#

```
File: contracts/SortedCdps.sol

508    require(_newNICR > 0, "SortedCdps: NICR must be positive")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)


#

```
File: contracts/SortedCdps.sol

715    require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager")
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715)


#

```
File: contracts/SortedCdps.sol

720    require(
721                msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722                "SortedCdps: Caller is neither BO nor CdpM"
723            )
```
 use custom error instead 

[https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720-L723)


</details>

# 
