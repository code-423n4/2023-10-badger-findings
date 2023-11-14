# Gas Report

## Gas Optimizations
| |Issue|Instances|Gas Saved|
|:-:|:-|:-:|:-:|
|[[G-01]](#g-01-abiencodepacked-is-more-gas-efficient-than-abiencode)|`abi.encodePacked` is more gas efficient than `abi.encode`|5|-|
|[[G-02]](#g-02-use-assembly-to-emit-events)|Use assembly to emit events|88|3344|
|[[G-03]](#g-03-use-assembly-to-check-for-address0)|Use assembly to check for `address(0)`|24|432|
|[[G-04]](#g-04-use-assembly-to-calculate-hashes)|Use assembly to calculate hashes|11|4114|
|[[G-05]](#g-05--use-assembly-to-write-storage-values)| Use assembly to write storage values|112|8400|
|[[G-06]](#g-06-use-require-instead-of-assert)|Use `require` instead of `assert`|1|-|
|[[G-07]](#g-07-avoid-zero-transfer-to-save-gas)|Avoid zero transfer to save gas|10|1000|
|[[G-08]](#g-08-using-bool-for-storage-incurs-overhead)|Using `bool` for storage incurs overhead|4|68400|
|[[G-09]](#g-09-do-not-compare-boolean-expressions-to-boolean-literals)|Do not compare boolean expressions to boolean literals|4|36|
|[[G-10]](#g-10-cache-multiple-accesses-of-mappingarray-values)|Cache multiple accesses of mapping/array values|39|1638|
|[[G-11]](#g-11-using-constants-directly-rather-than-caching-the-value-saves-gas)|Using `constant`s directly, rather than caching the value, saves gas|2|-|
|[[G-12]](#g-12-function-result-should-be-cached)|Function result should be cached|90|-|
|[[G-13]](#g-13-cache-storage-variables-read-from-more-than-once)|Cache storage variables read from more than once|37|3589|
|[[G-14]](#g-14-use-calldata-instead-of-memory-for-function-arguments-that-are-read-only)|Use `calldata` instead of `memory` for function arguments that are read only|26|-|
|[[G-15]](#g-15-divisionmultiplication-by-powers-of-2-should-use-bit-shifting)|Division/Multiplication by powers of 2 should use bit shifting|4|80|
|[[G-16]](#g-16-initializing-variable-to-default-value-costs-unnecessary-gas)|Initializing variable to default value costs unnecessary gas|7|42|
|[[G-17]](#g-17-same-cast-is-done-multiple-times)|Same cast is done multiple times|96|-|
|[[G-18]](#g-18-avoid-emitting-events-within-loops)|Avoid emitting events within loops|1|750|
|[[G-19]](#g-19-multiple-consecutively-emitted-events-should-be-combined)|Multiple consecutively emitted events should be combined|4|3304|
|[[G-20]](#g-20-requirerevert-strings-longer-than-32-bytes-cost-extra-gas)|`require`/`revert` strings longer than 32 bytes cost extra gas|115|2070|
|[[G-21]](#g-21-cache-length-outside-of-for-loop)|Cache length outside of for loop|4|388|
|[[G-22]](#g-22-using--is-cheaper-than)|Using `>=` is cheaper than `>`|56|168|
|[[G-23]](#g-23-inline-modifiers-that-are-only-used-once-to-save-gas)|Inline `modifier`s that are only used once, to save gas|10|-|
|[[G-24]](#g-24-inline-internal-functions-that-are-only-called-once)|Inline `internal` functions that are only called once|78|2340|
|[[G-25]](#g-25-expressions-for-constant-values-such-as-a-call-to-keccak256-should-use-immutable-rather-than-constant)|Expressions for constant values such as a call to `keccak256` should use `immutable` rather than `constant`|8|800|
|[[G-26]](#g-26-avoid-contract-existence-checks-by-using-low-level-calls)|Avoid contract existence checks by using low level calls|125|12500|
|[[G-27]](#g-27-using-storage-instead-of-memory-for-structsarrays-saves-gas)|Using `storage` instead of `memory` for structs/arrays saves gas|28|-|
|[[G-28]](#g-28-refactor-modifiers-to-call-a-local-function)|Refactor modifiers to call a local function|5|5000|
|[[G-29]](#g-29-combine-multiple-mappings-with-the-same-key-type-where-appropriate)|Combine multiple mappings with the same key type where appropriate|3|60126|
|[[G-30]](#g-30-nesting-if-statements-is-cheaper-than-using)|Nesting `if`-statements is cheaper than using `&&`|13|78|
|[[G-31]](#g-31-use-unchecked-for-operations-that-cannot-overflowunderflow)|Use `unchecked` for operations that cannot overflow/underflow|13|780|
|[[G-32]](#g-32-function-names-can-be-optimized-to-save-gas)|Function names can be optimized to save gas|17|374|
|[[G-33]](#g-33-pack-state-variables-into-fewer-storage-slots)|Pack state variables into fewer storage slots|1|2000|
|[[G-34]](#g-34-use-payable-for-constructor)|Use `payable` for constructor|19|399|
|[[G-35]](#g-35-pre-compute-hashes)|Pre-compute hashes|3|108|
|[[G-36]](#g-36-use-private-rather-than-public-for-constants)|Use `private` rather than `public` for constants|31|105400|
|[[G-37]](#g-37-require-or-revert-statements-that-check-input-arguments-should-be-at-the-top-of-the-function)|`require()` or `revert()` statements that check input arguments should be at the top of the function|5|-|
|[[G-38]](#g-38--split-require-statements-using)| Split `require` statements using `&&`|33|297|
|[[G-39]](#g-39-not-using-the-named-return-variable-is-confusing-and-can-waste-gas)|Not using the named return variable is confusing and can waste gas|21|-|
|[[G-40]](#g-40-use-solidity-version-0819-for-gas-savings)|Use Solidity version `0.8.19` for gas savings|19|-|
|[[G-41]](#g-41-state-variable-read-in-a-loop)|State variable read in a loop|8|776|
|[[G-42]](#g-42-structs-can-be-packed-into-fewer-storage-slots)|Structs can be packed into fewer storage slots|3|-|
|[[G-43]](#g-43-pack-structs-into-fewer-storage-slots-by-truncating-uint256-values-referencing-time)|Pack structs into fewer storage slots by truncating `uint256` values referencing time|2|4000|
|[[G-44]](#g-44-remove-superfluous-event-fields)|Remove superfluous event fields|3|102|
|[[G-45]](#g-45-use--0-instead-of--0-for-uints)|Use `!= 0` instead of `> 0` for uints|50|300|
|[[G-46]](#g-46-usage-of-uint-smaller-than-32-bytes-256-bits-incurs-overhead)|Usage of `uint` smaller than 32 bytes (256 bits) incurs overhead|6|36|
|[[G-47]](#g-47-remove-unused-state-variables)|Remove unused state variables|9|-|
|[[G-48]](#g-48-avoid-updating-storage-when-the-value-hasnt-changed)|Avoid updating storage when the value hasn't changed|6|4800|
|[[G-49]](#g-49-use-assembly-for-integer-zero-checks)|Use assembly for integer zero checks|26|156|
|[[G-50]](#g-50-use-custom-errors)|Use custom errors|163|1956|
|[[G-51]](#g-51-using-storage-instead-of-memory-for-state-variables-saves-gas)|Using `storage` instead of `memory` for state variables saves gas|7|14700|
|[[G-52]](#g-52-use-uint1uint2-instead-of-truefalse)|Use `uint(1)`/`uint(2)` instead of `true`/`false`|4|20000|
|[[G-53]](#g-53-i-costs-less-gas-than-i)|`++i` costs less gas than `i++`|12|72|
|[[G-54]](#g-54-state-variables-only-assigned-to-in-the-constructor-should-be-immutable)|State variables only assigned to in the constructor should be `immutable`|2|4194|
|[[G-55]](#g-55-state-variables-that-do-not-change-should-be-constant-or-immutable)|State variables that do not change should be `constant` or `immutable`|17|-|
|[[G-56]](#g-56-use-via-ir-for-deployment)|Use `via-ir` for deployment|1|-|

Total issues: 56

Total instances: 1491

Total gas saved: 339,049

# Gas Optimizations
## [G-01] `abi.encodePacked` is more gas efficient than `abi.encode`

`abi.encode` pads all elementary types to 32 bytes, whereas `abi.encodePacked` will only use the minimal required memory to encode the data. See [here](https://docs.soliditylang.org/en/v0.8.11/abi-spec.html?highlight=encodepacked#non-standard-packed-mode) for more info.

<details>
<summary>Instances: 5</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

682:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
[L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

214:                     abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)

240:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
[L214](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L214), [L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

152:                 abi.encode(operation)

159:                 abi.encode(operation)

```
[L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L152), [L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L159)

</details>

&nbsp;
## [G-02] Use assembly to emit events

For example `emit ExampleEvent(amount)` (amount is `uint256`) can be re-written
as
```solidity
assembly {
    let memptr := mload(0x40)
    mstore(0x00, calldataload(0x44))
    mstore(0x20, calldataload(0xa4))
    mstore(0x40, amount)
    log1(
        0x00,
        0x60,
        // keccak256("ExampleEvent(uint256)")
        0x12210f92675543a3eee7d9f6cc64eaca8eb1431502f685da3f48e7593e2b7f1e
    )
    mstore(0x40, memptr)
}
```

<details>
<summary>Instances: 88</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

65:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

112:         emit SystemCollSharesUpdated(cachedSystemCollShares);
113:         emit CollSharesTransferred(_account, _shares);

145:         emit SystemCollSharesUpdated(cachedSystemCollShares);
146:         emit CollSharesTransferred(_account, totalShares);

173:         emit SystemCollSharesUpdated(cachedSystemCollShares);
174:         emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);

200:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

213:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);

247:         emit SystemCollSharesUpdated(cachedSystemCollShares);

307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

421:         emit FlashLoansPaused(msg.sender, _paused);

```
[L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65), [L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112), [L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173), [L200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200), [L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213), [L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307), [L360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360), [L383](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L383), [L399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399), [L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L412), [L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1171:         emit FlashLoansPaused(msg.sender, _paused);

```
[L136](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136), [L641](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L641), [L1105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105), [L1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149), [L1162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1162), [L1171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171)

```solidity
File: packages/contracts/contracts/CdpManager.sol

55:         emit StakingRewardSplitSet(stakingRewardSplit);

179:                 emit CdpUpdated(
180:                     _redeemColFromCdp.cdpId,
181:                     _borrower,
182:                     msg.sender,
183:                     _oldDebtAndColl.debt,
184:                     _oldDebtAndColl.collShares,
185:                     0,
186:                     0,
187:                     0,
188:                     CdpOperation.redeemCollateral
189:                 );

220:             emit CdpUpdated(
221:                 _redeemColFromCdp.cdpId,
222:                 ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223:                 msg.sender,
224:                 _oldDebtAndColl.debt,
225:                 _oldDebtAndColl.collShares,
226:                 newDebt,
227:                 newColl,
228:                 Cdps[_redeemColFromCdp.cdpId].stake,
229:                 CdpOperation.redeemCollateral
230:             );

466:         emit Redemption(
467:             _debt,
468:             totals.debtToRedeem,
469:             totals.collSharesDrawn,
470:             totals.feeCollShares,
471:             msg.sender
472:         );

545:         emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);

630:         emit BaseRateUpdated(newBaseRate);

681:         emit BaseRateUpdated(decayedBaseRate);

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);

925:         emit CdpUpdated(
926:             _cdpId,
927:             _borrower,
928:             msg.sender,
929:             0,
930:             0,
931:             _debt,
932:             _coll,
933:             stake,
934:             CdpOperation.openCdp
935:         );

961:         emit CdpUpdated(
962:             _cdpId,
963:             _borrower,
964:             msg.sender,
965:             _debt,
966:             _coll,
967:             _newDebt,
968:             _newColl,
969:             stake,
970:             CdpOperation.adjustCdp
971:         );

```
[L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55), [L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L179), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L466), [L545](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L545), [L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630), [L681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681), [L698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698), [L782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782), [L801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801), [L824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824), [L836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836), [L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848), [L925](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L925), [L961](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L961)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

238:         emit CdpUpdated(
239:             _liqState.cdpId,
240:             _borrower,
241:             msg.sender,
242:             _totalDebtToBurn,
243:             _totalColToSend,
244:             0,
245:             0,
246:             0,
247:             CdpOperation.liquidateInNormalMode
248:         );

281:         emit CdpLiquidated(
282:             _liqState.cdpId,
283:             _borrower,
284:             _totalDebtToBurn,
285:             // please note this is the collateral share of the liquidated CDP
286:             _cappedColPortion,
287:             CdpOperation.liquidateInNormalMode,
288:             msg.sender,
289:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
290:         );

312:         emit CdpUpdated(
313:             _recoveryState.cdpId,
314:             _borrower,
315:             msg.sender,
316:             _totalDebtToBurn,
317:             _totalColToSend,
318:             0,
319:             0,
320:             0,
321:             CdpOperation.liquidateInRecoveryMode
322:         );

367:         emit CdpLiquidated(
368:             _recoveryState.cdpId,
369:             _borrower,
370:             _totalDebtToBurn,
371:             // please note this is the collateral share of the liquidated CDP
372:             _cappedColPortion,
373:             CdpOperation.liquidateInRecoveryMode,
374:             msg.sender,
375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
376:         );

437:             emit CdpPartiallyLiquidated(
438:                 _cdpId,
439:                 sortedCdps.getOwnerAddress(_cdpId),
440:                 _partialDebt,
441:                 _partialColl,
442:                 CdpOperation.partiallyLiquidate,
443:                 msg.sender,
444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0
445:             );

490:         emit CdpUpdated(
491:             _cdpId,
492:             sortedCdps.getOwnerAddress(_cdpId),
493:             msg.sender,
494:             _oldDebt,
495:             _oldColl,
496:             Cdps[_cdpId].debt,
497:             Cdps[_cdpId].coll,
498:             Cdps[_cdpId].stake,
499:             CdpOperation.partiallyLiquidate
500:         );

516:         emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);

891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);

```
[L238](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L238), [L281](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L281), [L312](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L312), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L367), [L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L437), [L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490), [L516](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L516), [L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

50:         emit TCRNotified(_tcr);

55:             emit GracePeriodStart();

64:         emit TCRNotified(_tcr);

69:             emit GracePeriodEnd();

119:         emit GracePeriodDurationSet(_gracePeriod);

300:         emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);

340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

390:             emit CdpUpdated(
391:                 _cdpId,
392:                 ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),
393:                 msg.sender,
394:                 prevDebt,
395:                 prevCollShares,
396:                 _newDebt,
397:                 _newColl,
398:                 _cdp.stake,
399:                 CdpOperation.syncAccounting
400:             );

414:         emit TotalStakesUpdated(_newTotalStakes);

425:         emit TotalStakesUpdated(_newTotalStakes);

481:         emit CdpArrayIndexUpdated(idToMove, index);

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

602:         emit CdpFeeSplitApplied(
603:             _cdpId,
604:             _oldPerUnitCdp,
605:             _systemStEthFeePerUnitIndex,
606:             _feeSplitDistributed,
607:             _newColl
608:         );

```
[L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50), [L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L55), [L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64), [L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L69), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119), [L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300), [L340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340), [L390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L390), [L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414), [L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425), [L481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481), [L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542), [L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587), [L602](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L602)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

83:         emit SurplusCollSharesUpdated(_account, newAmount);

95:         emit SurplusCollSharesUpdated(_account, 0);

104:         emit CollSharesTransferred(_account, claimableColl);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```
[L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L95), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104), [L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L150)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

259:         emit Transfer(sender, recipient, amount);

267:         emit Transfer(address(0), account, amount);

282:         emit Transfer(account, address(0), amount);

290:         emit Approval(owner, spender, amount);

```
[L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L259), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267), [L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282), [L290](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L290)

```solidity
File: packages/contracts/contracts/Governor.sol

157:         emit RoleNameSet(role, roleName);

```
[L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

548:         emit PriceFeedStatusChanged(_status);

555:         emit LastGoodPriceUpdated(_currentPrice);

```
[L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67), [L378](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381), [L387](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387), [L548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548), [L555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

405:         emit NodeAdded(_id, _NICR);

451:             emit NodeRemoved(_ids[i]);

490:         emit NodeRemoved(_id);

```
[L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405), [L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451), [L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

56:         emit DeployNewMacro(_owner, addy);

```
[L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

22:         emit OwnershipTransferred(msg.sender, _owner);
23:         emit AuthorityUpdated(msg.sender, _authority);

49:         emit AuthorityUpdated(msg.sender, newAuthority);

55:         emit OwnershipTransferred(msg.sender, newOwner);

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22), [L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L49), [L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L55)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```
[L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50), [L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140:         emit CapabilityBurned(target, functionSig);

163:         emit UserRoleUpdated(user, role, enabled);

```
[L101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L129), [L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L140), [L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L163)

</details>

&nbsp;
## [G-03] Use assembly to check for `address(0)`

Saves 16000 deployment gas per instance and 6 runtime gas per instance.

```solidity
assembly {
  if iszero(_addr) {
  mstore(0x00, "zero address")
  revert(0x00, 0x20)
  }
}
```

<details>
<summary>Instances: 24</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

61:         if (_authorityAddress != address(0)) {

394:             _feeRecipientAddress != address(0),

```
[L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L61), [L394](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L394)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

124:         if (_authorityAddress != address(0)) {

735:             recoveredAddress != address(0) && recoveredAddress == _borrower,

1142:             _feeRecipientAddress != address(0),

```
[L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L124), [L735](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L735), [L1142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1142)

```solidity
File: packages/contracts/contracts/CdpManager.sol

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

```
[L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369), [L389](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L389)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

55:         if (_authorityAddress != address(0)) {

```
[L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L55)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

247:         require(sender != address(0), "EBTCToken: zero sender!");

248:         require(recipient != address(0), "EBTCToken: zero recipient!");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

271:         require(account != address(0), "EBTCToken: burn from zero account!");

286:         require(owner != address(0), "EBTCToken: zero approve owner!");

287:         require(spender != address(0), "EBTCToken: zero approve spender!");

297:             _recipient != address(0) && _recipient != address(this),

```
[L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247), [L248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248), [L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286), [L287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

224:             if (address(fallbackCaller) == address(0)) {

363:         if (_fallbackCaller != address(0)) {

587:         if (address(fallbackCaller) != address(0)) {

```
[L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L224), [L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L363), [L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L587)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

69:                 vars.currentCdpUser != address(0) &&

85:                 vars.currentCdpUser != address(0) &&

```
[L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L69), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L85)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

187:         require(facet != address(0), "Diamond: Function does not exist");

```
[L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

38:             (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L56)

</details>

&nbsp;
## [G-04] Use assembly to calculate hashes

Saves 5000 deployment gas per instance and 374 runtime gas per instance.

### Unoptimized
```solidity
function solidityHash(uint256 a, uint256 b) public view {
	//unoptimized
	keccak256(abi.encodePacked(a, b));
}
```

### Optimized
```solidity
function assemblyHash(uint256 a, uint256 b) public view {
	//optimized
	assembly {
		mstore(0x00, a)
		mstore(0x20, b)
		let hashedVal := keccak256(0x00, 0x40)
	}
}
```

<details>
<summary>Instances: 11</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

128:         bytes32 hashedName = keccak256(bytes(NAME));

129:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

682:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

717:         bytes32 digest = keccak256(

721:                 keccak256(

```
[L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L128), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129), [L682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682), [L717](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717), [L721](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L721)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

71:         bytes32 hashedName = keccak256(bytes(_NAME));

72:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

209:         bytes32 digest = keccak256(

213:                 keccak256(

240:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

```
[L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L71), [L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72), [L209](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209), [L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L213), [L240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```
[L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182)

</details>

&nbsp;
## [G-05]  Use assembly to write storage values

```
// unoptimized
owner = _newOwner

// optimized
assembly {
sstore(owner.slot, _newOwner)
}
```

<details>
<summary>Instances: 112</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

53:         borrowerOperationsAddress = _borrowerOperationsAddress;
54:         cdpManagerAddress = _cdpManagerAddress;
55:         collateral = ICollateralToken(_collTokenAddress);
56:         collSurplusPoolAddress = _collSurplusAddress;
57:         feeRecipientAddress = _feeRecipientAddress;

110:         systemCollShares = cachedSystemCollShares;

143:         systemCollShares = cachedSystemCollShares;

168:         systemCollShares = cachedSystemCollShares;

171:         feeRecipientCollShares = cachedFeeRecipientCollShares;

199:         systemDebt = cachedSystemDebt;

212:         systemDebt = cachedSystemDebt;

246:         systemCollShares = cachedSystemCollShares;

359:         feeRecipientCollShares = cachedFeeRecipientCollShares;

398:         feeRecipientAddress = _feeRecipientAddress;

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53), [L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L110), [L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L143), [L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L168), [L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L171), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L199), [L212](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L212), [L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L246), [L359](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L359), [L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

117:         cdpManager = ICdpManager(_cdpManagerAddress);
118:         collSurplusPool = ICollSurplusPool(_collSurplusPoolAddress);
119:         sortedCdps = ISortedCdps(_sortedCdpsAddress);
120:         ebtcToken = IEBTCToken(_ebtcTokenAddress);
121:         feeRecipientAddress = _feeRecipientAddress;

131:         _HASHED_NAME = hashedName;
132:         _HASHED_VERSION = hashedVersion;
133:         _CACHED_CHAIN_ID = _chainID();
134:         _CACHED_DOMAIN_SEPARATOR = _buildDomainSeparator(_TYPE_HASH, hashedName, hashedVersion);

640:         positionManagers[_borrower][_positionManager] = _approval;

1148:         feeRecipientAddress = _feeRecipientAddress;

```
[L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L117), [L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L131), [L640](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L640), [L1148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

53:             lastGracePeriodStartTimestamp = uint128(block.timestamp);

67:             lastGracePeriodStartTimestamp = UNSET_TIMESTAMP;

118:         recoveryModeGracePeriodDuration = _gracePeriod;

228:         deploymentStartTime = block.timestamp;
229:         liquidationLibrary = _liquidationLibraryAddress;

233:         borrowerOperationsAddress = _borrowerOperationsAddress;
234:         collSurplusPool = ICollSurplusPool(_collSurplusPool);
235:         ebtcToken = IEBTCToken(_ebtcToken);
236:         sortedCdps = ISortedCdps(_sortedCdps);

276:         cdpDebtRedistributionIndex[_cdpId] = 0;
277:         cdpStEthFeePerUnitIndex[_cdpId] = 0;

295:         totalStakesSnapshot = _totalStakesSnapshot;

298:         totalCollateralSnapshot = _totalCollateralSnapshot;

339:         cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex;

405:             cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex;

412:         totalStakes = _newTotalStakes;

423:         totalStakes = _newTotalStakes;

541:             stEthIndex = _newIndex;

581:         systemStEthFeePerUnitIndex = _newPerUnit;
582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L53), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L67), [L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L118), [L228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L228), [L233](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L233), [L276](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L276), [L295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L295), [L298](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L298), [L339](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L339), [L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L405), [L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L412), [L423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L423), [L541](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L541), [L581](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L581)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

48:         borrowerOperationsAddress = _borrowerOperationsAddress;
49:         cdpManagerAddress = _cdpManagerAddress;
50:         activePoolAddress = _activePoolAddress;
51:         collateral = ICollateralToken(_collTokenAddress);
52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

81:         balances[_account] = newAmount;

94:         balances[_account] = 0;

102:             totalSurplusCollShares = cachedTotalSurplusCollShares - claimableColl;

132:         totalSurplusCollShares = totalSurplusCollShares + _value;

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48), [L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L81), [L94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L94), [L102](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L102), [L132](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L132)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

68:         cdpManagerAddress = _cdpManagerAddress;
69:         borrowerOperationsAddress = _borrowerOperationsAddress;

74:         _HASHED_NAME = hashedName;
75:         _HASHED_VERSION = hashedVersion;
76:         _CACHED_CHAIN_ID = _chainID();
77:         _CACHED_DOMAIN_SEPARATOR = _buildDomainSeparator(_TYPE_HASH, hashedName, hashedVersion);

255:             _balances[sender] = cachedSenderBalances - amount;

258:         _balances[recipient] = _balances[recipient] + amount;

265:         _totalSupply = _totalSupply + amount;
266:         _balances[account] = _balances[account] + amount;

278:             _balances[account] = cachedBalance - amount;

281:         _totalSupply = _totalSupply - amount;

289:         _allowances[owner][spender] = amount;

```
[L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68), [L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L74), [L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L255), [L258](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L258), [L265](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L265), [L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L278), [L281](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L281), [L289](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L289)

```solidity
File: packages/contracts/contracts/Governor.sol

155:         roleNames[role] = roleName;

```
[L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L155)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

63:         fallbackCaller = IFallbackCaller(_fallbackCallerAddress);

69:         ETH_BTC_CL_FEED = AggregatorV3Interface(_ethBtcCLFeed);
70:         STETH_ETH_CL_FEED = AggregatorV3Interface(_collEthCLFeed);

88:         status = Status.chainlinkWorking;

377:                     fallbackCaller = newFallbackCaler;

386:             fallbackCaller = newFallbackCaler;

547:         status = _status;

554:         lastGoodPrice = _currentPrice;

```
[L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L63), [L69](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L69), [L88](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L88), [L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L377), [L386](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L386), [L547](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L547), [L554](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L554)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

93:         maxSize = _size;

95:         cdpManager = ICdpManager(_cdpManagerAddress);
96:         borrowerOperationsAddress = _borrowerOperationsAddress;

```
[L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L93), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L95)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

34:         sortedCdps = ISortedCdps(_sortedCdpsAddress);
35:         cdpManager = ICdpManager(_cdpManagerAddress);

```
[L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L34)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

60:         borrowerOperations = IBorrowerOperations(_borrowerOperationsAddress);
61:         activePool = IActivePool(_activePool);
62:         cdpManager = ICdpCdps(_cdpManager);
63:         ebtcToken = IEBTCToken(_ebtc);
64:         stETH = ICollateralToken(_coll);
65:         sortedCdps = ISortedCdps(_sortedCdps);

67:         willSweep = _sweepToCaller;

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L60), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L67)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

29:         borrowerOperations = _borrowerOperationsAddress;
30:         activePool = _activePool;
31:         cdpManager = _cdpManager;
32:         ebtcToken = _ebtc;
33:         stETH = _coll;
34:         sortedCdps = _sortedCdps;

```
[L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L29)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

36:         theOwner = _owner;

```
[L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L36)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

45:         owner = _owner;

```
[L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

19:         owner = _owner;
20:         authority = _authority;

47:         authority = newAuthority;

53:         owner = newOwner;

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L19), [L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L47), [L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L53)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

43:         _authority = Authority(newAuthority);

47:             _authorityInitialized = true;

59:         _authority = Authority(newAuthority);
60:         _authorityInitialized = true;

```
[L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L43), [L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L47), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L59)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

53:         activePool = IActivePool(_activePoolAddress);
54:         priceFeed = IPriceFeed(_priceFeedAddress);
55:         collateral = ICollateralToken(_collateralAddress);

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L53)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

16:         locked = LOCKED;

20:         locked = OPEN;

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L16), [L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L20)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

96:             capabilityFlag[target][functionSig] = CapabilityFlag.Public;

98:             capabilityFlag[target][functionSig] = CapabilityFlag.None;

138:         capabilityFlag[target][functionSig] = CapabilityFlag.Burned;

```
[L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L96), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L98), [L138](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L138)

</details>

&nbsp;
## [G-06] Use `require` instead of `assert`

Prior to solc 0.8.0, `assert` used the invalid opcode which used up all the remaining gas while `require` used the revert opcode which refunded the gas and therefore the importance of using `require` instead of `assert` was greater.

However, after 0.8.0, `assert` uses revert opcode just like `require` but creates a `Panic(uint256)` error instead of `Error(string)` created by `require`.

Solidity documentation states: 'The `assert` function generates an error of type `Panic(uint256)`. Code that works properly should never Panic, even on invalid external input. If this happens, you need to fix it in your contract. there's a mistake'.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

564:         assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

```
[L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L564)

</details>

&nbsp;
## [G-07] Avoid zero transfer to save gas

In Solidity, unnecessary operations can waste gas. For example, a transfer function
without a zero amount check uses gas even if called with a zero amount, since the
contract state remains unchanged. Implementing a zero amount check avoids these
unnecessary function calls, saving gas and improving efficiency.

<details>
<summary>Instances: 10</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

286:         collateral.transfer(feeRecipientAddress, fee);

381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```
[L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```
[L785](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
[L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );

224:             ebtcToken.transfer(msg.sender, ebtcBal);

237:         IERC20(token).safeTransfer(msg.sender, amount);

```
[L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129), [L224](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224), [L237](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237)

</details>

&nbsp;
## [G-08] Using `bool` for storage incurs overhead

Booleans are more expensive than `uint256` or any type that takes up a full
word because each write operation emits an extra `SLOAD` to first read the
slot's contents, replace the bits taken up by the boolean, and then write
back. This is the compiler's defense against contract upgrades and pointer
aliasing, and it cannot be disabled.

Use `uint256(1)` and `uint256(2)` for true/false to avoid a Gwarmaccess
(100 gas) for the extra `SLOAD`, and to avoid Gsset (20000 gas) when
changing from false to true, after having been true in the past (see
[OpenZeppelin's `ReentrancyGuard`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27)
for reference).

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

143:     bool public redemptionsPaused;

```
[L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

35:     bool internal immutable willSweep;

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

14:     bool private _authorityInitialized;

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

15:     bool public flashLoansPaused;

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15)

</details>

&nbsp;
## [G-09] Do not compare boolean expressions to boolean literals

`<x> == true` <=> `<x>`, also `<x> == false` <=> `!<x>`

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

```
[L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

100:         bool _recoveryModeAtStart = _TCR < CCR ? true : false;

695:         vars.recoveryModeAtStart = _TCR < CCR ? true : false;

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;

```
[L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L100), [L695](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L695), [L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788)

</details>

&nbsp;
## [G-10] Cache multiple accesses of mapping/array values

Caching a mapping's value in a local `storage` or `calldata` variable when the
value is accessed multiple times, saves ~42 gas per access due to not having
to recalculate the key's keccak256 hash (Gkeccak256 - 30 gas) and that
calculation's associated stack operations. Caching an array's struct avoids
recalculating the array offsets into memory/calldata.

<details>
<summary>Instances: 39</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

914:         Cdps[_cdpId].debt = _debt;
915:         Cdps[_cdpId].coll = _coll;
916:         Cdps[_cdpId].status = Status.active;
917:         Cdps[_cdpId].liquidatorRewardShares = _liquidatorRewardShares;

```
[L914](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L914)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

490:         emit CdpUpdated(
491:             _cdpId,
492:             sortedCdps.getOwnerAddress(_cdpId),
493:             msg.sender,
494:             _oldDebt,
495:             _oldColl,
496:             Cdps[_cdpId].debt,
497:             Cdps[_cdpId].coll,
498:             Cdps[_cdpId].stake,
499:             CdpOperation.partiallyLiquidate
500:         );

490:         emit CdpUpdated(
491:             _cdpId,
492:             sortedCdps.getOwnerAddress(_cdpId),
493:             msg.sender,
494:             _oldDebt,
495:             _oldColl,
496:             Cdps[_cdpId].debt,
497:             Cdps[_cdpId].coll,
498:             Cdps[_cdpId].stake,
499:             CdpOperation.partiallyLiquidate
500:         );

```
[L490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L490)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

271:         Cdps[_cdpId].status = closedStatus;
272:         Cdps[_cdpId].coll = 0;
273:         Cdps[_cdpId].debt = 0;
274:         Cdps[_cdpId].liquidatorRewardShares = 0;

350:         uint256 _oldPerUnitCdp = cdpStEthFeePerUnitIndex[_cdpId];

405:             cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex;

411:         uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake;

413:         Cdps[_cdpId].stake = 0;

464:         Status cdpStatus = Cdps[_cdpId].status;

471:         uint128 index = Cdps[_cdpId].arrayIndex;

621:         uint256 _cdpCol = Cdps[_cdpId].coll;

631:         uint256 _feeSplitDistributed = Cdps[_cdpId].stake *
632:             (_systemStEthFeePerUnitIndex - _cdpStEthFeePerUnitIndex);

```
[L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L271), [L350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L350), [L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L405), [L411](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L411), [L413](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L413), [L464](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L464), [L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L471), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L621), [L631](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L631)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

80:         uint256 newAmount = balances[_account] + _amount;
81:         balances[_account] = newAmount;

91:         uint256 claimableColl = balances[_account];

94:         balances[_account] = 0;

```
[L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L80), [L91](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L91), [L94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L94)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

250:         uint256 cachedSenderBalances = _balances[sender];

255:             _balances[sender] = cachedSenderBalances - amount;

258:         _balances[recipient] = _balances[recipient] + amount;
258:         _balances[recipient] = _balances[recipient] + amount;

266:         _balances[account] = _balances[account] + amount;
266:         _balances[account] = _balances[account] + amount;

273:         uint256 cachedBalance = _balances[account];

278:             _balances[account] = cachedBalance - amount;

```
[L250](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L250), [L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L255), [L258](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L258), [L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L266), [L273](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L273), [L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L278)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

388:             data.nodes[_id].nextId = data.head;

393:             data.nodes[_id].prevId = data.tail;

398:             data.nodes[_id].nextId = nextId;
399:             data.nodes[_id].prevId = prevId;

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

450:             delete data.nodes[_ids[i]];
451:             emit NodeRemoved(_ids[i]);

465:                 data.head = data.nodes[_id].nextId;

471:                 data.tail = data.nodes[_id].prevId;

477:                 data.nodes[data.nodes[_id].prevId].nextId = data.nodes[_id].nextId;

479:                 data.nodes[data.nodes[_id].nextId].prevId = data.nodes[_id].prevId;

488:         delete data.nodes[_id];

626:         bytes32 nextId = data.nodes[prevId].nextId;

630:             prevId = data.nodes[prevId].nextId;
631:             nextId = data.nodes[prevId].nextId;

649:         bytes32 prevId = data.nodes[nextId].prevId;

653:             nextId = data.nodes[nextId].prevId;
654:             prevId = data.nodes[nextId].prevId;

```
[L388](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L388), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L393), [L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L398), [L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433), [L450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L450), [L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L465), [L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L471), [L477](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L477), [L479](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L479), [L488](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L488), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L626), [L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630), [L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L649), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

```
[L440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

90:         require(
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
92:             "RolesAuthority: Capability Burned"
93:         );

96:             capabilityFlag[target][functionSig] = CapabilityFlag.Public;

98:             capabilityFlag[target][functionSig] = CapabilityFlag.None;

113:             getRolesWithCapability[target][functionSig] |= bytes32(1 << role);

120:             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);

114:             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

121:             enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));

124:             if (enabledFunctionSigsByTarget[target].length() == 0) {

134:         require(
135:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
136:             "RolesAuthority: Capability Burned"
137:         );
138:         capabilityFlag[target][functionSig] = CapabilityFlag.Burned;

149:             getUserRoles[user] |= bytes32(1 << role);

155:             getUserRoles[user] &= ~bytes32(1 << role);

158:             if (getUserRoles[user] == bytes32(0)) {

```
[L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L96), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L98), [L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L113), [L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L120), [L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L121), [L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L124), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L149), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L155), [L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L158)

</details>

&nbsp;
## [G-11] Using `constant`s directly, rather than caching the value, saves gas

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

84:         bytes32 position = DIAMOND_STORAGE_POSITION;

```
[L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L84)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

68:         uint256 y = DECIMAL_PRECISION;

```
[L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L68)

</details>

&nbsp;
## [G-12] Function result should be cached

The instances below show multiple calls to a single function within the same
function.

<details>
<summary>Instances: 90</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

272:         uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

302:         require(
303:             collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304:             "ActivePool: Should keep same collateral share rate"
305:         );

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

376:         uint256 balance = IERC20(token).balanceOf(address(this));

381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```
[L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L272), [L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371), [L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

439:     function _openCdp(
440:         uint256 _debt,
441:         bytes32 _upperHint,
442:         bytes32 _lowerHint,
443:         uint256 _stEthBalance,
444:         address _borrower
445:     ) internal returns (bytes32) {

500:                 cdpManager.notifyEndGracePeriod(newTCR);

509:             cdpManager.notifyEndGracePeriod(newTCR);

852:     function _requireValidAdjustmentInCurrentMode(
853:         bool _isRecoveryMode,
854:         uint256 _stEthBalanceDecrease,
855:         bool _isDebtIncrease,
856:         AdjustCdpLocals memory _vars
857:     ) internal {

896:                 cdpManager.notifyEndGracePeriod(_vars.newTCR);

906:             cdpManager.notifyEndGracePeriod(_vars.newTCR);

```
[L439](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L439), [L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L500), [L509](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L509), [L852](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852), [L896](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L896), [L906](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L906)

```solidity
File: packages/contracts/contracts/CdpManager.sol

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

367:             currentBorrower = sortedCdps.getOwnerAddress(_cId);

371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);

370:                 _cId = sortedCdps.getPrev(_cId);

424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);

```
[L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L367), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371), [L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

135:     function _liquidateIndividualCdpSetupCDP(
136:         LiquidationLocals memory _liqState,
137:         LiquidationRecoveryModeLocals memory _recoveryState
138:     ) internal {

145:             (
146:                 liquidationValues.debtToBurn,
147:                 liquidationValues.totalCollToSendToLiquidator,
148:                 liquidationValues.debtToRedistribute,
149:                 liquidationValues.liquidatorCollSharesReward,
150:                 liquidationValues.collSurplus
151:             ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);

162:                 (
163:                     liquidationValues.debtToBurn,
164:                     liquidationValues.totalCollToSendToLiquidator,
165:                     liquidationValues.debtToRedistribute,
166:                     liquidationValues.liquidatorCollSharesReward,
167:                     liquidationValues.collSurplus
168:                 ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);

186:     function _liquidateCdpInGivenMode(
187:         LiquidationLocals memory _liqState,
188:         LiquidationRecoveryModeLocals memory _recoveryState
189:     ) private returns (uint256, uint256, uint256, uint256, uint256) {

202:             return (
203:                 _outputState.totalDebtToBurn,
204:                 _outputState.totalCollSharesToSend,
205:                 _outputState.totalDebtToRedistribute,
206:                 _outputState.totalLiquidatorRewardCollShares,
207:                 _outputState.totalSurplusCollShares
208:             );

213:             return (
214:                 _outputState.totalDebtToBurn,
215:                 _outputState.totalCollSharesToSend,
216:                 _outputState.totalDebtToRedistribute,
217:                 _outputState.totalLiquidatorRewardCollShares,
218:                 _outputState.totalSurplusCollShares
219:             );

733:     function _getTotalFromBatchLiquidate_RecoveryMode(
734:         uint256 _price,
735:         uint256 _systemCollShares,
736:         uint256 _systemDebt,
737:         bytes32[] memory _cdpArray
738:     ) internal returns (LiquidationTotals memory totals) {

745:         uint256 _TCR = _computeTCRWithGivenSystemValues(
746:             vars.entireSystemColl,
747:             vars.entireSystemDebt,
748:             _price
749:         );

783:                     _TCR = _computeTCRWithGivenSystemValues(
784:                         vars.entireSystemColl,
785:                         vars.entireSystemDebt,
786:                         _price
787:                     );

759:                 if (
760:                     !vars.backToNormalMode &&
761:                     (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))
762:                 ) {

790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {

764:                     _syncAccounting(vars.cdpId);

791:                     _syncAccounting(vars.cdpId);

781:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135), [L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L145), [L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L162), [L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L202), [L213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L213), [L733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733), [L745](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L745), [L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L783), [L790](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L790), [L791](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L791), [L795](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L795)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

310:             return (0, 0);

318:             return (0, 0);

616:     function getAccumulatedFeeSplitApplied(
617:         bytes32 _cdpId,
618:         uint256 _systemStEthFeePerUnitIndex
619:     ) public view returns (uint256, uint256) {

628:             return (0, _cdpCol);

643:             return (0, _cdpCol);

```
[L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L304), [L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L310), [L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L318), [L616](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616), [L628](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L628), [L643](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L643)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

145:         uint256 balance = IERC20(token).balanceOf(address(this));

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
[L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142), [L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)

```solidity
File: packages/contracts/contracts/Governor.sol

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

48:             bool _canCall = doesUserHaveRole(user, role);

59:                 bool _canCall = doesUserHaveRole(user, role);

49:             if (_canCall) {

60:                 if (_canCall) {

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {

77:             if (doesUserHaveRole(user, i)) {

85:                 if (doesUserHaveRole(user, i)) {

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

100:             if (roleEnabled) {

109:                 if (roleEnabled) {

```
[L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L43), [L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L48), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L59), [L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L60), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L77), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L85), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96), [L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L100), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L109)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

98:     function fetchPrice() external override returns (uint256) {

121:                     _changeStatus(Status.usingFallbackChainlinkUntrusted);

126:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);

112:                 if (_fallbackIsBroken(fallbackResponse)) {

133:                 if (_fallbackIsBroken(fallbackResponse)) {

120:                 if (_fallbackIsFrozen(fallbackResponse)) {

141:                 if (_fallbackIsFrozen(fallbackResponse)) {

127:                 return _storeFallbackPrice(fallbackResponse);

146:                 return _storeFallbackPrice(fallbackResponse);

153:                 if (_fallbackIsBroken(fallbackResponse)) {

113:                     _changeStatus(Status.bothOraclesUntrusted);

154:                     _changeStatus(Status.bothOraclesUntrusted);

160:                 if (_fallbackIsFrozen(fallbackResponse)) {
161:                     _changeStatus(Status.usingFallbackChainlinkUntrusted);

175:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);
176:                 return _storeFallbackPrice(fallbackResponse);

180:             if (_fallbackIsBroken(fallbackResponse)) {

134:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);

181:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);

170:                     return _storeChainlinkPrice(chainlinkResponse.answer);

185:             return _storeChainlinkPrice(chainlinkResponse.answer);

199:                 return _storeChainlinkPrice(chainlinkResponse.answer);

202:             if (_fallbackIsBroken(fallbackResponse)) {
203:                 _changeStatus(Status.bothOraclesUntrusted);

211:             if (_fallbackIsFrozen(fallbackResponse)) {

216:             return _storeFallbackPrice(fallbackResponse);

110:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {

226:                 if (
227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)
229:                 ) {

131:             if (_chainlinkIsFrozen(chainlinkResponse)) {

226:                 if (
227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)
229:                 ) {
230:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
231:                     return _storeChainlinkPrice(chainlinkResponse.answer);

191:             if (
192:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(
193:                     chainlinkResponse,
194:                     prevChainlinkResponse,
195:                     fallbackResponse
196:                 )
197:             ) {

239:             if (
240:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(
241:                     chainlinkResponse,
242:                     prevChainlinkResponse,
243:                     fallbackResponse
244:                 )
245:             ) {

198:                 _changeStatus(Status.chainlinkWorking);

246:                 _changeStatus(Status.chainlinkWorking);
247:                 return _storeChainlinkPrice(chainlinkResponse.answer);

256:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {

258:                 if (_fallbackIsBroken(fallbackResponse)) {
259:                     _changeStatus(Status.bothOraclesUntrusted);

264:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);

266:                 if (_fallbackIsFrozen(fallbackResponse)) {

271:                 return _storeFallbackPrice(fallbackResponse);

274:             if (_chainlinkIsFrozen(chainlinkResponse)) {

276:                 if (_fallbackIsBroken(fallbackResponse)) {
277:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);

282:                 if (_fallbackIsFrozen(fallbackResponse)) {

287:                 return _storeFallbackPrice(fallbackResponse);

291:             if (_fallbackIsBroken(fallbackResponse)) {
292:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);
293:                 return _storeChainlinkPrice(chainlinkResponse.answer);

297:             if (_fallbackIsFrozen(fallbackResponse)) {

169:                 if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {

303:             if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {
304:                 _changeStatus(Status.chainlinkWorking);
305:                 return _storeChainlinkPrice(chainlinkResponse.answer);

309:             _changeStatus(Status.usingFallbackChainlinkUntrusted);
310:             return _storeFallbackPrice(fallbackResponse);

316:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
317:                 _changeStatus(Status.bothOraclesUntrusted);

322:             if (_chainlinkIsFrozen(chainlinkResponse)) {

327:             if (
328:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(
329:                     chainlinkResponse,
330:                     prevChainlinkResponse,
331:                     fallbackResponse
332:                 )
333:             ) {
334:                 _changeStatus(Status.chainlinkWorking);
335:                 return _storeChainlinkPrice(chainlinkResponse.answer);

150:             if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {

340:             if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
341:                 _changeStatus(Status.bothOraclesUntrusted);

347:             return _storeChainlinkPrice(chainlinkResponse.answer);

606:     function _getCurrentChainlinkResponse()
607:         internal
608:         view
609:         returns (ChainlinkResponse memory chainlinkResponse)
610:     {

615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

687:     function _getPrevChainlinkResponse(
688:         uint80 _currentRoundEthBtcId,
689:         uint80 _currentRoundStEthEthId
690:     ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) {

703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

```
[L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98), [L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L121), [L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L126), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L133), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L141), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L146), [L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L153), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L154), [L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L160), [L175](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L175), [L180](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L180), [L181](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L181), [L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L185), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L199), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L202), [L211](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L211), [L216](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L216), [L226](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226), [L226](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226), [L239](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L239), [L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L246), [L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L256), [L258](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L258), [L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L264), [L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L266), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L271), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L274), [L276](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L276), [L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L282), [L287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L287), [L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L291), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L297), [L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L303), [L309](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L309), [L316](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L316), [L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L322), [L327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L327), [L340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L340), [L347](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L347), [L606](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L606), [L615](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L615), [L623](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L623), [L687](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L687), [L703](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L703), [L711](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L711)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

591:     function _validInsertPosition(
592:         uint256 _NICR,
593:         bytes32 _prevId,
594:         bytes32 _nextId
595:     ) internal view returns (bool) {

604:             return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);

607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

601:             return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId);

607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

674:     function _findInsertPosition(
675:         uint256 _NICR,
676:         bytes32 _prevId,
677:         bytes32 _nextId
678:     ) internal view returns (bytes32, bytes32) {

704:             return _descendList(_NICR, prevId);

707:             return _descendList(_NICR, prevId);

```
[L591](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L591), [L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607), [L674](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L674), [L704](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L704), [L707](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L707)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(
49:         uint256 _EBTCamount,
50:         uint256 _price,
51:         uint256 _maxIterations
52:     )
53:         external
54:         view
55:         returns (
56:             bytes32 firstRedemptionHint,
57:             uint256 partialRedemptionHintNICR,
58:             uint256 truncatedEBTCamount,
59:             uint256 partialRedemptionNewColl
60:         )
61:     {

66:             vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

73:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

72:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

116:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48), [L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L66), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73), [L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

177:             _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);

189:             _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);

178:             _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);

190:             _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);

187:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

199:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

398:     function _doSwap(SwapOperation memory swapData) internal {

405:         IERC20(swapData.tokenForSwap).safeApprove(
406:             swapData.addressForApprove,
407:             swapData.exactApproveAmount
408:         );

427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```
[L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118), [L177](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L177), [L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L189), [L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L190), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199), [L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398), [L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

134:     function _executeOne(Operation calldata op) internal {

144:                 success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)

149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)
149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

```
[L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134), [L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L149)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {

43:         _authority = Authority(newAuthority);

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L43), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {

75:                 x = decMul(x, x);

80:                 x = decMul(x, x);

79:                 y = decMul(x, y);

85:         return decMul(x, y);

```
[L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L59), [L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L75), [L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L80), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L85)

</details>

&nbsp;
## [G-13] Cache storage variables read from more than once

If the variable is only accessed once, it's cheaper to use the state
variable directly that one time, and save the 3 gas the extra stack
assignment would spend.

<details>
<summary>Instances: 37</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

294:         require(
295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296:             "ActivePool: Must repay Balance"
297:         );
298:         require(
299:             collateral.sharesOf(address(this)) >= systemCollShares,
300:             "ActivePool: Must repay Share"
301:         );

```
[L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1077:     function flashLoan(
1078:         IERC3156FlashBorrower receiver,
1079:         address token,
1080:         uint256 amount,
1081:         bytes calldata data
1082:     ) external override returns (bool) {

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

1103:         ebtcToken.burn(feeRecipientAddress, amount);

```
[L1077](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100), [L1103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1103)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

761:     function _calcSyncedGlobalAccounting(
762:         uint256 _newIndex,
763:         uint256 _oldIndex
764:     ) internal view returns (uint256, uint256, uint256) {

774:             uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;

777:             return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);

```
[L441](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441), [L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453), [L761](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L761), [L774](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L774), [L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L777)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

98:     function fetchPrice() external override returns (uint256) {

114:                     return lastGoodPrice;

122:                     return lastGoodPrice;

135:                     return lastGoodPrice;

142:                     return lastGoodPrice;

155:                     return lastGoodPrice;

162:                     return lastGoodPrice;

108:         if (status == Status.chainlinkWorking) {

189:         if (status == Status.usingFallbackChainlinkUntrusted) {

204:                 return lastGoodPrice;

212:                 return lastGoodPrice;

220:         if (status == Status.bothOraclesUntrusted) {

251:             return lastGoodPrice;

255:         if (status == Status.usingFallbackChainlinkFrozen) {

260:                     return lastGoodPrice;

267:                     return lastGoodPrice;

278:                     return lastGoodPrice;

283:                     return lastGoodPrice;

298:                 return lastGoodPrice;

314:         if (status == Status.usingChainlinkFallbackUntrusted) {

318:                 return lastGoodPrice;

323:                 return lastGoodPrice;

342:                 return lastGoodPrice;

351:         return lastGoodPrice;

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

376:                     address oldFallbackCaller = address(fallbackCaller);

384:             address oldFallbackCaller = address(fallbackCaller);

```
[L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98), [L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L114), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L122), [L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L135), [L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L142), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L155), [L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L162), [L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L189), [L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L204), [L212](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L212), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L220), [L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L251), [L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L255), [L260](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L260), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L267), [L278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L278), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L283), [L298](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L298), [L314](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L314), [L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L318), [L323](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L323), [L342](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L342), [L351](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L351), [L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358), [L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L376), [L384](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L384)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

344:     function insert(
345:         address owner,
346:         uint256 _NICR,
347:         bytes32 _prevId,
348:         bytes32 _nextId
349:     ) external override returns (bytes32) {

351:         bytes32 _id = toCdpId(owner, block.number, nextCdpNonce);

357:             ++nextCdpNonce;

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

388:             data.nodes[_id].nextId = data.head;
389:             data.nodes[data.head].prevId = _id;

393:             data.nodes[_id].prevId = data.tail;
394:             data.nodes[data.tail].nextId = _id;

419:     function batchRemove(bytes32[] memory _ids) external override {

424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;
425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;

456:     function _remove(bytes32 _id) internal {

465:                 data.head = data.nodes[_id].nextId;

471:                 data.tail = data.nodes[_id].prevId;

477:                 data.nodes[data.nodes[_id].prevId].nextId = data.nodes[_id].nextId;

479:                 data.nodes[data.nodes[_id].nextId].prevId = data.nodes[_id].prevId;

619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

626:         bytes32 nextId = data.nodes[prevId].nextId;

630:             prevId = data.nodes[prevId].nextId;
631:             nextId = data.nodes[prevId].nextId;

642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

649:         bytes32 prevId = data.nodes[nextId].prevId;

653:             nextId = data.nodes[nextId].prevId;
654:             prevId = data.nodes[nextId].prevId;

```
[L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344), [L351](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L351), [L357](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L357), [L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L363), [L388](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L388), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L393), [L419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419), [L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L424), [L456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L456), [L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L465), [L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L471), [L477](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L477), [L479](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L479), [L619](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L619), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L626), [L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630), [L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642), [L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L649), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653)

</details>

&nbsp;
## [G-14] Use `calldata` instead of `memory` for function arguments that are read only

When a function with a `memory` array is called externally, the `abi.decode()` step has to use a for-loop to copy each index of the `calldata` to the `memory` index. Each iteration of this for-loop costs at least 60 gas (i.e. 60 * `<mem_array>.length`). Using calldata directly, obliviates the need for such a loop in the contract code and runtime execution.

If the array is passed to an `internal` function which passes the array to another `internal` function where the array is modified and therefore `memory` is used in the `external` call, it's still more gas-efficient to use `calldata` when the external function uses modifiers, since the modifiers may prevent the `internal` functions from being called. `Structs` have the same overhead as an array of length one

<details>
<summary>Instances: 26</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

760:     function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

986:     function _getNewNominalICRFromCdpChange(
987:         AdjustCdpLocals memory vars,
988:         bool _isDebtIncrease
989:     ) internal pure returns (uint256) {

```
[L760](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760), [L986](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986)

```solidity
File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(
136:         SingleRedemptionInputs memory _redeemColFromCdp
137:     ) internal returns (SingleRedemptionValues memory singleRedemption) {

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

135:     function _liquidateIndividualCdpSetupCDP(
136:         LiquidationLocals memory _liqState,
137:         LiquidationRecoveryModeLocals memory _recoveryState
138:     ) internal {

186:     function _liquidateCdpInGivenMode(
187:         LiquidationLocals memory _liqState,
188:         LiquidationRecoveryModeLocals memory _recoveryState
189:     ) private returns (uint256, uint256, uint256, uint256, uint256) {

397:     function _liquidateCDPPartially(
398:         LiquidationLocals memory _partialState
399:     ) private returns (uint256, uint256) {

466:     function _reInsertPartialLiquidation(
467:         LiquidationLocals memory _partialState,
468:         uint256 _newNICR,
469:         uint256 _oldDebt,
470:         uint256 _oldColl
471:     ) internal {

608:     function _getLiquidationValuesNormalMode(
609:         uint256 _price,
610:         uint256 _TCR,
611:         LocalVariables_LiquidationSequence memory vars,
612:         LiquidationValues memory singleLiquidation
613:     ) internal {

642:     function _getLiquidationValuesRecoveryMode(
643:         uint256 _price,
644:         uint256 _systemDebt,
645:         uint256 _systemCollShares,
646:         LocalVariables_LiquidationSequence memory vars,
647:         LiquidationValues memory singleLiquidation
648:     ) internal {

839:     function _addLiquidationValuesToTotals(
840:         LiquidationTotals memory oldTotals,
841:         LiquidationValues memory singleLiquidation
842:     ) internal pure returns (LiquidationTotals memory newTotals) {

```
[L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135), [L186](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L186), [L397](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466), [L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L608), [L642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L839)

```solidity
File: packages/contracts/contracts/Governor.sol

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```
[L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

400:     function _chainlinkIsBroken(
401:         ChainlinkResponse memory _currentResponse,
402:         ChainlinkResponse memory _prevResponse
403:     ) internal view returns (bool) {

412:     function _badChainlinkResponse(ChainlinkResponse memory _response) internal view returns (bool) {

435:     function _chainlinkIsFrozen(ChainlinkResponse memory _response) internal view returns (bool) {

445:     function _chainlinkPriceChangeAboveMax(
446:         ChainlinkResponse memory _currentResponse,
447:         ChainlinkResponse memory _prevResponse
448:     ) internal pure returns (bool) {

465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

485:     function _fallbackIsFrozen(
486:         FallbackResponse memory _fallbackResponse
487:     ) internal view returns (bool) {

503:     function _bothOraclesLiveAndUnbrokenAndSimilarPrice(
504:         ChainlinkResponse memory _chainlinkResponse,
505:         ChainlinkResponse memory _prevChainlinkResponse,
506:         FallbackResponse memory _fallbackResponse
507:     ) internal view returns (bool) {

526:     function _bothOraclesSimilarPrice(
527:         ChainlinkResponse memory _chainlinkResponse,
528:         FallbackResponse memory _fallbackResponse
529:     ) internal pure returns (bool) {

561:     function _storeFallbackPrice(
562:         FallbackResponse memory _fallbackResponse
563:     ) internal returns (uint256) {

```
[L400](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L400), [L412](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L412), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L435), [L445](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L445), [L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L465), [L485](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L485), [L503](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L503), [L526](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L526), [L561](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L561)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

244:     function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

291:     function _handleOperation(LeverageMacroOperation memory operation) internal {

382:     function _doSwaps(SwapOperation[] memory swapData) internal {

398:     function _doSwap(SwapOperation memory swapData) internal {

435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

```
[L244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L244), [L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L291), [L382](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382), [L398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435)

</details>

&nbsp;
## [G-15] Division/Multiplication by powers of 2 should use bit shifting

`<x> * 2` is equivalent to `<x> << 1` and `<x> / 2` is equivalent to `<x> >> 1`.
In general, `<x> * 2 ** n` is equivalent to `<x> << n`. The `MUL` and `DIV`
opcodes cost 5 gas, whereas `SHL` and `SHR` only cost 3 gas.

Note that using left shifting for multiplication does not protect against overflow
and as such it should be implemented with caution.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/PriceFeed.sol

800:         return
801:             (_scaledDecimal *
802:                 uint256(_ethBtcAnswer) *
803:                 uint256(_stEthEthAnswer) *
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);

```
[L800](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L800)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

76:                 n = n / 2;

81:                 n = (n - 1) / 2;

```
[L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L76), [L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L81)

</details>

&nbsp;
## [G-16] Initializing variable to default value costs unnecessary gas

<details>
<summary>Instances: 7</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

54:             uint256 j = 0;

82:             uint256 j = 0;

105:             uint256 j = 0;

```
[L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L54), [L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L82), [L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L105)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

182:         uint _currentIndex = 0;

245:         uint _ownedCount = 0;

246:         uint i = 0;

311:         uint i = 0;

```
[L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L182), [L245](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L245), [L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L246), [L311](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L311)

</details>

&nbsp;
## [G-17] Same cast is done multiple times

It's cheaper to do it once, and store the result to a variable.

<details>
<summary>Instances: 96</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

274:         collateral.transfer(address(receiver), amount);

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

294:         require(
295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296:             "ActivePool: Must repay Balance"
297:         );
298:         require(
299:             collateral.sharesOf(address(this)) >= systemCollShares,
300:             "ActivePool: Must repay Share"
301:         );

272:         uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

302:         require(
303:             collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304:             "ActivePool: Should keep same collateral share rate"
305:         );

307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

376:         uint256 balance = IERC20(token).balanceOf(address(this));

381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```
[L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274), [L283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283), [L294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294), [L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L307), [L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

500:                 cdpManager.notifyEndGracePeriod(newTCR);

509:             cdpManager.notifyEndGracePeriod(newTCR);

896:                 cdpManager.notifyEndGracePeriod(_vars.newTCR);

906:             cdpManager.notifyEndGracePeriod(_vars.newTCR);

1088:         ebtcToken.mint(address(receiver), amount);

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

```
[L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L500), [L509](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L509), [L896](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L896), [L906](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L906), [L1088](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1088), [L1100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100), [L1105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1105)

```solidity
File: packages/contracts/contracts/CdpManager.sol

163:                 address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId);

220:             emit CdpUpdated(
221:                 _redeemColFromCdp.cdpId,
222:                 ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),
223:                 msg.sender,
224:                 _oldDebtAndColl.debt,
225:                 _oldDebtAndColl.collShares,
226:                 newDebt,
227:                 newColl,
228:                 Cdps[_redeemColFromCdp.cdpId].stake,
229:                 CdpOperation.redeemCollateral
230:             );

367:             currentBorrower = sortedCdps.getOwnerAddress(_cId);

371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

388:         while (
389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
390:         ) {

370:                 _cId = sortedCdps.getPrev(_cId);

424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);

```
[L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L163), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L220), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L367), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371), [L388](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L388), [L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

759:                 if (
760:                     !vars.backToNormalMode &&
761:                     (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))
762:                 ) {

790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {

764:                     _syncAccounting(vars.cdpId);

791:                     _syncAccounting(vars.cdpId);

```
[L759](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L759), [L790](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L790), [L791](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L791)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

145:         uint256 balance = IERC20(token).balanceOf(address(this));

148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
[L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

247:         require(sender != address(0), "EBTCToken: zero sender!");
248:         require(recipient != address(0), "EBTCToken: zero recipient!");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

267:         emit Transfer(address(0), account, amount);

271:         require(account != address(0), "EBTCToken: burn from zero account!");

282:         emit Transfer(account, address(0), amount);

286:         require(owner != address(0), "EBTCToken: zero approve owner!");
287:         require(spender != address(0), "EBTCToken: zero approve spender!");

```
[L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247), [L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L267), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271), [L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286)

```solidity
File: packages/contracts/contracts/Governor.sol

49:             if (_canCall) {

60:                 if (_canCall) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

100:             if (roleEnabled) {

109:                 if (roleEnabled) {

```
[L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L49), [L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L60), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76), [L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98), [L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L109)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

121:                     _changeStatus(Status.usingFallbackChainlinkUntrusted);

126:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);

112:                 if (_fallbackIsBroken(fallbackResponse)) {

133:                 if (_fallbackIsBroken(fallbackResponse)) {

120:                 if (_fallbackIsFrozen(fallbackResponse)) {

141:                 if (_fallbackIsFrozen(fallbackResponse)) {

127:                 return _storeFallbackPrice(fallbackResponse);

146:                 return _storeFallbackPrice(fallbackResponse);

153:                 if (_fallbackIsBroken(fallbackResponse)) {

113:                     _changeStatus(Status.bothOraclesUntrusted);

154:                     _changeStatus(Status.bothOraclesUntrusted);

160:                 if (_fallbackIsFrozen(fallbackResponse)) {
161:                     _changeStatus(Status.usingFallbackChainlinkUntrusted);

175:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);
176:                 return _storeFallbackPrice(fallbackResponse);

180:             if (_fallbackIsBroken(fallbackResponse)) {

134:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);

181:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);

170:                     return _storeChainlinkPrice(chainlinkResponse.answer);

185:             return _storeChainlinkPrice(chainlinkResponse.answer);

199:                 return _storeChainlinkPrice(chainlinkResponse.answer);

202:             if (_fallbackIsBroken(fallbackResponse)) {
203:                 _changeStatus(Status.bothOraclesUntrusted);

211:             if (_fallbackIsFrozen(fallbackResponse)) {

216:             return _storeFallbackPrice(fallbackResponse);

131:             if (_chainlinkIsFrozen(chainlinkResponse)) {

226:                 if (
227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)
229:                 ) {
230:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
231:                     return _storeChainlinkPrice(chainlinkResponse.answer);

198:                 _changeStatus(Status.chainlinkWorking);

246:                 _changeStatus(Status.chainlinkWorking);
247:                 return _storeChainlinkPrice(chainlinkResponse.answer);

258:                 if (_fallbackIsBroken(fallbackResponse)) {
259:                     _changeStatus(Status.bothOraclesUntrusted);

264:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);

266:                 if (_fallbackIsFrozen(fallbackResponse)) {

271:                 return _storeFallbackPrice(fallbackResponse);

274:             if (_chainlinkIsFrozen(chainlinkResponse)) {

276:                 if (_fallbackIsBroken(fallbackResponse)) {
277:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);

282:                 if (_fallbackIsFrozen(fallbackResponse)) {

287:                 return _storeFallbackPrice(fallbackResponse);

291:             if (_fallbackIsBroken(fallbackResponse)) {
292:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);
293:                 return _storeChainlinkPrice(chainlinkResponse.answer);

297:             if (_fallbackIsFrozen(fallbackResponse)) {

304:                 _changeStatus(Status.chainlinkWorking);
305:                 return _storeChainlinkPrice(chainlinkResponse.answer);

309:             _changeStatus(Status.usingFallbackChainlinkUntrusted);
310:             return _storeFallbackPrice(fallbackResponse);

317:                 _changeStatus(Status.bothOraclesUntrusted);

322:             if (_chainlinkIsFrozen(chainlinkResponse)) {

334:                 _changeStatus(Status.chainlinkWorking);
335:                 return _storeChainlinkPrice(chainlinkResponse.answer);

341:                 _changeStatus(Status.bothOraclesUntrusted);

347:             return _storeChainlinkPrice(chainlinkResponse.answer);

376:                     address oldFallbackCaller = address(fallbackCaller);

384:             address oldFallbackCaller = address(fallbackCaller);

615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

```
[L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L121), [L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L126), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L133), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L141), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L146), [L153](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L153), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L154), [L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L160), [L175](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L175), [L180](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L180), [L181](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L181), [L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L185), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L199), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L202), [L211](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L211), [L216](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L216), [L226](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226), [L246](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L246), [L258](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L258), [L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L264), [L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L266), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L271), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L274), [L276](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L276), [L282](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L282), [L287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L287), [L291](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L291), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L297), [L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L304), [L309](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L309), [L317](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L317), [L322](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L322), [L334](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L334), [L341](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L341), [L347](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L347), [L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L376), [L384](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L384), [L615](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L615), [L623](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L623), [L703](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L703), [L711](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L711)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

604:             return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);

607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

601:             return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId);

607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

```
[L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

66:             vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

73:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

68:             while (
69:                 vars.currentCdpUser != address(0) &&
70:                 cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR
71:             ) {

84:             while (
85:                 vars.currentCdpUser != address(0) &&
86:                 vars.remainingEbtcToRedeem > 0 &&
87:                 _maxIterations-- > 0
88:             ) {

72:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

116:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

```
[L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L66), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73), [L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L84), [L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(
130:                 msg.sender,
131:                 address(this),
132:                 operation.amountToTransferIn
133:             );

143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));

148:             IERC3156FlashLender(address(borrowerOperations)).flashLoan(
149:                 IERC3156FlashBorrower(address(this)),
150:                 address(ebtcToken),
151:                 borrowAmount,
152:                 abi.encode(operation)
153:             );

155:             IERC3156FlashLender(address(activePool)).flashLoan(
156:                 IERC3156FlashBorrower(address(this)),
157:                 address(stETH),
158:                 borrowAmount,
159:                 abi.encode(operation)
160:             );

155:             IERC3156FlashLender(address(activePool)).flashLoan(
156:                 IERC3156FlashBorrower(address(this)),
157:                 address(stETH),
158:                 borrowAmount,
159:                 abi.encode(operation)
160:             );

173:             bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

187:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

199:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

220:         uint256 ebtcBal = ebtcToken.balanceOf(address(this));
221:         uint256 collateralBal = stETH.sharesOf(address(this));

405:         IERC20(swapData.tokenForSwap).safeApprove(
406:             swapData.addressForApprove,
407:             swapData.exactApproveAmount
408:         );

427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```
[L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129), [L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L143), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L148), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L155), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L173), [L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L220), [L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L405), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L427)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);
54:         stETH.approve(address(borrowerOperations), type(uint256).max);
54:         stETH.approve(address(borrowerOperations), type(uint256).max);
55:         stETH.approve(address(activePool), type(uint256).max);

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L53)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

144:                 success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)

149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L149)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

43:         _authority = Authority(newAuthority);

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

59:         _authority = Authority(newAuthority);

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```
[L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L43), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50), [L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L59), [L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

114:             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

121:             enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));

```
[L114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L114), [L121](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L121)

</details>

&nbsp;
## [G-18] Avoid emitting events within loops

Emitting an event costs at least 375 base gas plus 375 gas for each indexed
parameter. Instead of emitting one event for each iteration of a loop, emit
one event after the loop containing all of the relevant information instead.
See [here](https://www.rareskills.io/post/ethereum-events#:~:text=Gas%20cost%20to%20emit%20Solidity%20event&text=Each%20event%20costs%20at%20least,words%20written%20to%20the%20chain.)
for more information about the gas cost of events.

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

449:         for (uint i = 0; i < _len; ++i) {

451:             emit NodeRemoved(_ids[i]);

```
[L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449), [L451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451)

</details>

&nbsp;
## [G-19] Multiple consecutively emitted events should be combined

Emitting multiple different events back to back wastes gas. It is more efficient
to combine all of the desired information into a single event and emit that
instead.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

112:         emit SystemCollSharesUpdated(cachedSystemCollShares);
113:         emit CollSharesTransferred(_account, _shares);

145:         emit SystemCollSharesUpdated(cachedSystemCollShares);
146:         emit CollSharesTransferred(_account, totalShares);

173:         emit SystemCollSharesUpdated(cachedSystemCollShares);
174:         emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);

```
[L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112), [L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

22:         emit OwnershipTransferred(msg.sender, _owner);
23:         emit AuthorityUpdated(msg.sender, _authority);

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22)

</details>

&nbsp;
## [G-20] `require`/`revert` strings longer than 32 bytes cost extra gas

Shortening revert strings to fit in 32 bytes will decrease gas costs for deployment and gas costs when the revert condition has been met. If the contract(s) in scope allow using Solidity >=0.8.4, consider using Custom Errors as they are more gas efficient while allowing developers to describe the error in detail using NatSpec.

<details>
<summary>Instances: 115</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

220:         require(
221:             msg.sender == borrowerOperationsAddress,
222:             "ActivePool: Caller is not BorrowerOperations"
223:         );

228:         require(
229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230:             "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231:         );

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

277:         require(
278:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279:             "ActivePool: IERC3156: Callback failed"
280:         );

302:         require(
303:             collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304:             "ActivePool: Should keep same collateral share rate"
305:         );

350:         require(
351:             cachedFeeRecipientCollShares >= _shares,
352:             "ActivePool: Insufficient fee recipient coll"
353:         );

374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```
[L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137), [L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220), [L228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228), [L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236), [L277](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277), [L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302), [L350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350), [L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374), [L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393), [L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");
146:         require(
147:             ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148:             "CdpManager: Reentrancy in nonReentrant call"
149:         );

368:         require(
369:             _stEthBalanceDecrease <= _cdpStEthBalance,
370:             "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371:         );

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

541:         require(
542:             vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543:             "BorrowerOperations: deposited collateral mismatch!"
544:         );

715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

734:         require(
735:             recoveredAddress != address(0) && recoveredAddress == _borrower,
736:             "BorrowerOperations: Invalid signature"
737:         );

807:         require(
808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809:             "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810:         );

818:         require(
819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820:             "BorrowerOperations: There must be either a collateral change or a debt change"
821:         );

826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

839:         require(
840:             !_checkRecoveryModeForTCR(_tcr),
841:             "BorrowerOperations: Operation not permitted during Recovery Mode"
842:         );

846:         require(
847:             _stEthBalanceDecrease == 0,
848:             "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849:         );

911:         require(
912:             _newICR >= MCR,
913:             "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"
914:         );

918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

922:         require(
923:             _newICR >= _oldICR,
924:             "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925:         );

929:         require(
930:             _newTCR >= CCR,
931:             "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932:         );

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

940:         require(
941:             _stEthBalance >= MIN_NET_STETH_BALANCE,
942:             "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
943:         );

947:         require(
948:             _debtRepayment <= _currentDebt,
949:             "BorrowerOperations: Amount repaid must not be larger than the Cdp's debt"
950:         );

957:         require(
958:             ebtcToken.balanceOf(_account) >= _debtRepayment,
959:             "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960:         );

970:         require(
971:             _approval != PositionManagerApproval.None,
972:             "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"
973:         );

1116:         require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

1141:         require(
1142:             _feeRecipientAddress != address(0),
1143:             "BorrowerOperations: Cannot set feeRecipient to zero address"
1144:         );

1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```
[L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145), [L368](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368), [L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463), [L541](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541), [L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715), [L734](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807), [L818](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818), [L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826), [L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831), [L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839), [L846](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846), [L911](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911), [L918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918), [L922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922), [L929](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929), [L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936), [L940](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940), [L947](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947), [L957](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957), [L970](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970), [L1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116), [L1141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141), [L1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155)

```solidity
File: packages/contracts/contracts/CdpManager.sol

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");
503:         require(
504:             _toRemoveIds[_total - 1] == _end,
505:             "CdpManager: batchRemoveSortedCdpIds check end error"
506:         );

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

743:         require(
744:             callerBalance >= _amount,
745:             "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746:         );
747:         require(
748:             callerBalance <= _totalSupply,
749:             "CdpManager: redeemer's EBTC balance exceeds total supply!"
750:         );

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

762:         require(
763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764:             "Max fee percentage must be between redemption fee floor and 100%"
765:         );

774:         require(
775:             _stakingRewardSplit <= MAX_REWARD_SPLIT,
776:             "CDPManager: new staking reward split exceeds max"
777:         );

789:         require(
790:             _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791:             "CDPManager: new redemption fee floor is lower than minimum"
792:         );
793:         require(
794:             _redemptionFeeFloor <= DECIMAL_PRECISION,
795:             "CDPManager: new redemption fee floor is higher than maximum"
796:         );

808:         require(
809:             _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810:             "CDPManager: new minute decay factor out of range"
811:         );
812:         require(
813:             _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814:             "CDPManager: new minute decay factor out of range"
815:         );

```
[L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431), [L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626), [L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672), [L743](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743), [L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754), [L758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758), [L762](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762), [L774](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774), [L789](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789), [L808](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

82:             require(
83:                 _checkICRAgainstLiqThreshold(_ICR, _TCR),
84:                 "LiquidationLibrary: ICR is not below liquidation threshold in current mode"
85:             );

89:             require(
90:                 cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP,
91:                 "LiquidationLibrary: Recovery Mode grace period not started"
92:             );
93:             require(
94:                 block.timestamp >
95:                     cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96:                 "LiquidationLibrary: Recovery mode grace period still in effect"
97:             );

477:             require(
478:                 getCachedICR(_cdpId, _partialState.price) >= _partialState.ICR,
479:                 "LiquidationLibrary: !_newICR>=_ICR"
480:             );

680:         require(
681:             _cdpArray.length != 0,
682:             "LiquidationLibrary: Calldata address array must not be empty"
683:         );

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

901:         require(
902:             (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903:                 _entireDebt,
904:             "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905:         );

909:         require(
910:             _entireColl >= MIN_NET_STETH_BALANCE,
911:             "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912:         );

```
[L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56), [L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89), [L477](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477), [L680](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680), [L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710), [L901](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901), [L909](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );

242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");
243:         require(
244:             ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245:             "BorrowerOperations: Reentrancy in nonReentrant call"
246:         );

261:         require(
262:             closedStatus != Status.nonExistent && closedStatus != Status.active,
263:             "CdpManagerStorage: close non-exist or non-active CDP!"
264:         );

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

466:         require(
467:             cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468:             "CdpManagerStorage: remove non-exist or non-active CDP!"
469:         );

475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

653:         require(
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655:             "CdpManager: Only one cdp in the system"
656:         );

660:         require(
661:             msg.sender == borrowerOperationsAddress,
662:             "CdpManager: Caller is not the BorrowerOperations contract"
663:         );

```
[L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112), [L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242), [L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261), [L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475), [L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556), [L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653), [L660](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

113:         require(
114:             msg.sender == borrowerOperationsAddress,
115:             "CollSurplusPool: Caller is not Borrower Operations"
116:         );

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```
[L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92), [L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113), [L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120), [L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124), [L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

271:         require(account != address(0), "EBTCToken: burn from zero account!");

274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

296:         require(
297:             _recipient != address(0) && _recipient != address(this),
298:             "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299:         );
300:         require(
301:             _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302:             "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303:         );

307:         require(
308:             msg.sender == borrowerOperationsAddress,
309:             "EBTCToken: Caller is not BorrowerOperations"
310:         );

315:         require(
316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||
318:                 isAuthorized(msg.sender, msg.sig),
319:             "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
320:         );

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144), [L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165), [L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251), [L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274), [L296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307), [L315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );

```
[L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

367:         require(!contains(_id), "SortedCdps: List already contains the node");

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

427:         require(
428:             _firstPrev != dummyId || _lastNext != dummyId,
429:             "SortedCdps: batchRemove() leave ZERO node left!"
430:         );

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

458:         require(contains(_id), "SortedCdps: List does not contain the id");

506:         require(contains(_id), "SortedCdps: List does not contain the id");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

720:         require(
721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722:             "SortedCdps: Caller is neither BO nor CdpM"
723:         );

```
[L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427), [L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433), [L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458), [L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506), [L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508), [L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715), [L720](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

179:             require(
180:                 cdpInfo.status == checkParams.expectedStatus,
181:                 "!LeverageMacroReference: openCDP status check"
182:             );

191:             require(
192:                 cdpInfo.status == checkParams.expectedStatus,
193:                 "!LeverageMacroReference: adjustCDP status check"
194:             );

201:             require(
202:                 cdpInfo.status == checkParams.expectedStatus,
203:                 "!LeverageMacroReference: closeCDP status check"
204:             );

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

356:             require(
357:                 msg.sender == address(borrowerOperations),
358:                 "LeverageMacroReference: wrong lender for eBTC flashloan"
359:             );

362:             require(
363:                 msg.sender == address(activePool),
364:                 "LeverageMacroReference: wrong lender for stETH flashloan"
365:             );

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

```
[L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179), [L191](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191), [L201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201), [L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249), [L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251), [L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253), [L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352), [L356](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356), [L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362), [L440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

57:         require(!_authorityInitialized, "Auth: authority already initialized");

```
[L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L57)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

90:         require(
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
92:             "RolesAuthority: Capability Burned"
93:         );

134:         require(
135:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
136:             "RolesAuthority: Capability Burned"
137:         );

```
[L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134)

</details>

&nbsp;
## [G-21] Cache length outside of for loop

Currently, the solidity compiler will always read the length of the array during each iteration.

That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

57:             for (uint256 i = 0; i < _usrs.length; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {

46:         for (uint256 i = 0; i < users.length(); i++) {

```
[L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122), [L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137), [L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46)

</details>

&nbsp;
## [G-22] Using `>=` is cheaper than `>`

The compiler uses opcodes GT and ISZERO for solidity code that uses `>`, but
only requires LT for `>=`, which
[saves 3 gas](https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde).
It should be converted to the <=/>= equivalent when comparing against integer literals.

<details>
<summary>Instances: 56</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

267:         require(amount > 0, "ActivePool: 0 Amount");

```
[L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```
[L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393), [L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463), [L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835), [L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936), [L1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083)

```solidity
File: packages/contracts/contracts/CdpManager.sol

388:         while (
389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
390:         ) {

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

436:         } else if (_numCdpsFullyRedeemed > 1) {

497:         while (_cnt > 0 && _id != bytes32(0)) {

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

```
[L388](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L388), [L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431), [L436](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L436), [L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L497), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626), [L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

195:             if (_outputState.totalSurplusCollShares > 0) {

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

525:         if (totalDebtToRedistribute > 0) {

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

713:         if (totals.totalCollSurplus > 0) {

```
[L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L195), [L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L261), [L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L266), [L336](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L336), [L342](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L342), [L525](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L525), [L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710), [L713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L713)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

315:         if (_debtIndexDiff > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

653:         require(
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655:             "CdpManager: Only one cdp in the system"
656:         );

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {

```
[L315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315), [L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L362), [L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L369), [L380](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L380), [L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453), [L512](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765), [L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796), [L829](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L829), [L879](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L879)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

```
[L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)

```solidity
File: packages/contracts/contracts/Governor.sol

53:         if (count > 0) {

81:         if (count > 0) {

104:         if (count > 0) {

135:         if (_sigs.length > 0) {

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L53), [L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L81), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L104), [L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L135)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

457:         uint256 percentDeviation = maxPrice > 0
458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice
459:             : 0;

488:         return
489:             _fallbackResponse.timestamp > 0 &&
490:             _responseTimeout(_fallbackResponse.timestamp, fallbackCaller.fallbackTimeout());

```
[L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457), [L488](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L488)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

274:         if (_ownedCount > 0) {

330:             if (maxNodes > 0 && i >= maxNodes) {

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

460:         if (data.size > 1) {

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```
[L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202), [L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L274), [L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422), [L460](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L460), [L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

84:             while (
85:                 vars.currentCdpUser != address(0) &&
86:                 vars.remainingEbtcToRedeem > 0 &&
87:                 _maxIterations-- > 0
88:             ) {

```
[L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L84)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {

```
[L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L128), [L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L223), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L227), [L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L293), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L307)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {

73:         while (n > 1) {

93:         if (_debt > 0) {

109:         if (_debt > 0) {

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L73), [L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L93), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L109)

</details>

&nbsp;
## [G-23] Inline `modifier`s that are only used once, to save gas

<details>
<summary>Instances: 10</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371)

```solidity
File: packages/contracts/contracts/CdpManager.sol

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

```
[L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

```
[L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {
225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

```
[L225](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L225)

```solidity
File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```
[L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

```
[L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52)

</details>

&nbsp;
## [G-24] Inline `internal` functions that are only called once

Saves 20-40 gas per instance. See https://blog.soliditylang.org/2021/03/02/saving-gas-with-simple-inliner/ for more details.

<details>
<summary>Instances: 78</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

158:         _requireCallerIsCdpManager();

243:         _requireCallerIsBorrowerOperations();

```
[L158](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L158), [L243](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L243)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

350:             _requireNonZeroDebtChange(_debtChange);

352:         _requireSingularCollChange(_stEthBalanceIncrease, _stEthBalanceDecrease);

353:         _requireNonZeroAdjustment(_stEthBalanceIncrease, _stEthBalanceDecrease, _debtChange);

356:         (vars.collSharesChange, vars.isCollIncrease) = _getCollSharesChangeFromStEthChange(

373:         vars.newICR = _getNewICRFromCdpChange(

385:         _requireValidAdjustmentInCurrentMode(

394:             _requireValidDebtRepayment(vars.debt, vars.netDebtChange);

421:             uint256 newNICR = _getNewNominalICRFromCdpChange(vars, _isDebtIncrease);

435:             _processTokenMovesFromAdjustment(_varMvTokens);

517:         _requireCdpIsNonExistent(_cdpId);

562:         _requireNotInRecoveryMode(_getCachedTCR(price));

882:             _requireNoStEthBalanceDecrease(_stEthBalanceDecrease);

885:                 _requireNoDecreaseOfICR(_vars.newICR, _vars.oldICR);

```
[L350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L350), [L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L352), [L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L353), [L356](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L356), [L373](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L373), [L385](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L385), [L394](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L394), [L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L421), [L435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L435), [L517](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L517), [L562](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L562), [L882](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L882), [L885](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L885)

```solidity
File: packages/contracts/contracts/CdpManager.sol

171:                 _closeCdpByRedemption(

334:         _requireValidMaxFeePercentage(_maxFeePercentage);

350:         _requireTCRisNotBelowMCR(totals.price, totals.tcrAtStart);

351:         _requireAmountGreaterThanZero(_debt);

353:         _requireEbtcBalanceCoversRedemptionAndWithinSupply(

363:         if (_isValidFirstRedemptionHint(_firstRedemptionHint, totals.price)) {

403:                 SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(

437:             bytes32[] memory _toRemoveIds = _getCdpIdsToRemove(

447:         _updateBaseRateFromRedemption(

454:         totals.feeCollShares = _getRedemptionFee(totals.collSharesDrawn);

732:         return _checkPotentialRecoveryMode(_systemCollShares, _systemDebt, _price);

922:         uint256 index = _addCdpIdToArray(_cdpId);

956:         _setCdpCollShares(_cdpId, _newColl);

957:         _setCdpDebt(_cdpId, _newDebt);

```
[L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L171), [L334](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L334), [L350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L350), [L351](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L351), [L353](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L353), [L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L363), [L403](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L403), [L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L437), [L447](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L447), [L454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L454), [L732](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L732), [L922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L922), [L956](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L956), [L957](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L957)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

130:         _liquidateIndividualCdpSetupCDP(_liqState, _rs);

405:         _requirePartialLiqDebtSize(_partialDebt, _debtAndColl.debt, _partialState.price);

422:         _requirePartialLiqCollSize(collateral.getPooledEthByShares(newColl));

425:         _partiallyReduceCdpDebt(_cdpId, _partialDebt, _partialColl);

429:             _reInsertPartialLiquidation(

526:             _redistributeDebt(totalDebtToRedistribute);

699:             totals = _getTotalFromBatchLiquidate_RecoveryMode(

707:             totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray);

765:                     _getLiquidationValuesRecoveryMode(

```
[L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L130), [L405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L405), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L422), [L425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L425), [L429](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L429), [L526](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L526), [L699](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L699), [L707](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L707), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L765)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

256:         _closeCdpWithoutRemovingSortedCdps(_cdpId, closedStatus);

267:         _requireMoreThanOneCdpInSystem(cdpIdsArrayLength);

269:         _removeStake(_cdpId);

279:         _removeCdp(_cdpId, cdpIdsArrayLength);

370:                 _applyAccumulatedFeeSplit(

381:                 _updateRedistributedDebtIndex(_cdpId);

420:         (uint256 newStake, uint256 oldStake) = _updateStakeForCdp(_cdpId);

433:         uint256 newStake = _computeNewStake(_cdp.coll);

511:         _syncStEthIndex(_oldIndex, _newIndex);

518:             _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError);

519:             _updateSystemSnapshotsExcludeCollRemainder(0);

529:         _syncGracePeriod(); // Synch Grace Period

729:         return _hasRedistributedDebt(_cdpId);

891:         return _checkICRAgainstTCR(icr, tcr) && _recoveryModeGracePeriodPassed();

```
[L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L256), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L267), [L269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L269), [L279](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L279), [L370](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L370), [L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L381), [L420](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L420), [L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L433), [L511](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L511), [L518](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L518), [L519](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L519), [L529](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L529), [L729](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L729), [L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L891)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

78:         _requireCallerIsCdpManager();

90:         _requireCallerIsBorrowerOperations();

131:         _requireCallerIsActivePool();

```
[L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L78), [L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L90), [L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L131)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

87:         _mint(_account, _amount);

```
[L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L87)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

105:         FallbackResponse memory fallbackResponse = _getCurrentFallbackResponse();

404:         return _badChainlinkResponse(_currentResponse) || _badChainlinkResponse(_prevResponse);

```
[L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L105), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L404)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

588:         return _validInsertPosition(_NICR, _prevId, _nextId);

701:             return _ascendList(_NICR, nextId);

```
[L588](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L588), [L701](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L701)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

98:                     ) = _calculateCdpStateAfterPartialRedemption(vars, currentCdpDebt, _price);

```
[L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L98)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

299:             _openCdpCallback(operation.OperationData);

301:             _closeCdpCallback(operation.OperationData);

303:             _adjustCdpCallback(operation.OperationData);

386:             _doSwap(swapData[i]);

401:         _ensureNotSystem(swapData.addressForSwap);

414:         (bool success, ) = excessivelySafeCall(

430:         _doSwapChecks(swapData.swapChecks);

```
[L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L299), [L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L301), [L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L303), [L386](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L386), [L401](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L401), [L414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L414), [L430](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L430)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

115:             _executeOne(ops[i]);

165:         _fallback();

```
[L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L115), [L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L165)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

27:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

```
[L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L27)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

17:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

80:         (TCR, , ) = _getTCRWithSystemDebtAndCollShares(_price);

87:         uint256 systemDebt = _getSystemDebt();

96:         return _checkRecoveryModeForTCR(_getCachedTCR(_price));

129:             _checkICRAgainstMCR(_icr) ||

130:             (_checkICRAgainstTCR(_icr, _tcr) && _checkRecoveryModeForTCR(_tcr));

```
[L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L80), [L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L87), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L96), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L129), [L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L130)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

33:      * Used only inside the exponentiation, _decPow().

```
[L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L33)

</details>

&nbsp;
## [G-25] Expressions for constant values such as a call to `keccak256` should use `immutable` rather than `constant`

When left as `constant`, the value is re-calculated each time it is used instead of being converted to a constant at compile time. This costs an extra ~100 gas for each access.

Using `immutable` only incurs the gas costs for the computation at deploy time.

See [here](https://github.com/ethereum/solidity/issues/9232) for a detailed description of the issue.

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11)

</details>

&nbsp;
## [G-26] Avoid contract existence checks by using low level calls

Prior to 0.8.10 the compiler inserted extra code, including `EXTCODESIZE` (100 gas),
to check for contract existence for external function calls. In more recent solidity
versions, the compiler will not insert these checks if the external call has a return
value. Similar behavior can be achieved in earlier versions by using low-level calls,
since low level calls never check for contract existence.

<details>
<summary>Instances: 125</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

60:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());

272:         uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

294:         require(
295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296:             "ActivePool: Must repay Balance"
297:         );

337:         return collateral.balanceOf(address(this));

376:         uint256 balance = IERC20(token).balanceOf(address(this));

```
[L60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L60), [L272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L272), [L294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294), [L337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L337), [L376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

123:         address _authorityAddress = address(AuthNoOwner(_cdpManagerAddress).authority());

338:         address _borrower = sortedCdps.getOwnerAddress(_cdpId);

347:         vars.price = priceFeed.fetchPrice();

363:         vars.debt = cdpManager.getCdpDebt(_cdpId);
364:         vars.collShares = cdpManager.getCdpCollShares(_cdpId);

367:         uint256 _cdpStEthBalance = collateral.getPooledEthByShares(vars.collShares);

372:         vars.oldICR = EbtcMath._computeCR(_cdpStEthBalance, vars.debt, vars.price);

459:         vars.price = priceFeed.fetchPrice();

465:         uint256 _netCollAsShares = collateral.getSharesByPooledEth(vars.netStEthBalance);
466:         uint256 _liquidatorRewardShares = collateral.getSharesByPooledEth(LIQUIDATOR_REWARD);

469:         vars.ICR = EbtcMath._computeCR(vars.netStEthBalance, vars.debt, vars.price);

472:         vars.NICR = EbtcMath._computeNominalCR(_netCollAsShares, vars.debt);

513:         bytes32 _cdpId = sortedCdps.insert(_borrower, vars.NICR, _upperHint, _lowerHint);

554:         address _borrower = sortedCdps.getOwnerAddress(_cdpId);

561:         uint256 price = priceFeed.fetchPrice();

564:         uint256 collShares = cdpManager.getCdpCollShares(_cdpId);
565:         uint256 debt = cdpManager.getCdpDebt(_cdpId);
566:         uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

570:         uint256 newTCR = _getNewTCRFromCdpChange(
571:             collateral.getPooledEthByShares(collShares),
572:             false,
573:             debt,
574:             false,
575:             price
576:         );

749:             collSharesChange = collateral.getSharesByPooledEth(_collReceived);

752:             collSharesChange = collateral.getSharesByPooledEth(_requestedCollWithdrawal);

825:         uint256 status = _cdpManager.getCdpStatus(_cdpId);

830:         uint status = cdpManager.getCdpStatus(_cdpId);

873:         _vars.newTCR = _getNewTCRFromCdpChange(
874:             collateral.getPooledEthByShares(_vars.collSharesChange),
875:             _vars.isCollIncrease,
876:             _vars.netDebtChange,
877:             _isDebtIncrease,
878:             _vars.price
879:         );

999:         uint256 newNICR = EbtcMath._computeNominalCR(newCollShares, newDebt);

1022:         uint256 newICR = EbtcMath._computeCR(
1023:             collateral.getPooledEthByShares(newCollShares),
1024:             newDebt,
1025:             _price
1026:         );

1057:         uint256 systemStEthBalance = collateral.getPooledEthByShares(_systemCollShares);

1065:         uint256 newTCR = EbtcMath._computeCR(systemStEthBalance, systemDebt, _price);

```
[L123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L123), [L338](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L338), [L347](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L347), [L363](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L363), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L367), [L372](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L372), [L459](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L459), [L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L465), [L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L469), [L472](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L472), [L513](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L513), [L554](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L554), [L561](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L561), [L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L564), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L570), [L749](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L749), [L752](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L752), [L825](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L825), [L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L830), [L873](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L873), [L999](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L999), [L1022](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1022), [L1057](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1057), [L1065](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1065)

```solidity
File: packages/contracts/contracts/CdpManager.sol

140:         singleRedemption.debtToRedeem = EbtcMath._min(
141:             _redeemColFromCdp.maxEBTCamount,
142:             Cdps[_redeemColFromCdp.cdpId].debt /// @audit Redeem everything
143:         );

145:         singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth(
146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price
147:         );

163:                 address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId);

193:             uint256 newNICR = EbtcMath._computeNominalCR(newColl, newDebt);

284:         bytes32 nextCdp = sortedCdps.getNext(_firstRedemptionHint);

338:         totals.price = priceFeed.fetchPrice();

364:             currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);

366:             _cId = sortedCdps.getLast();
367:             currentBorrower = sortedCdps.getOwnerAddress(_cId);

370:                 _cId = sortedCdps.getPrev(_cId);
371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);

424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);
425:                 address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);

500:             _id = sortedCdps.getNext(_id);

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622:             _totalEBTCSupply;

625:         newBaseRate = EbtcMath._min(newBaseRate, DECIMAL_PRECISION); // cap baseRate at a maximum of 100%

648:         return
649:             EbtcMath._min(
650:                 redemptionFeeFloor + _baseRate,
651:                 DECIMAL_PRECISION // cap at a maximum of 100%
652:             );

704:         uint256 decayFactor = EbtcMath._decPow(minuteDecayFactor, minutesPassed);

742:         uint256 callerBalance = ebtcToken.balanceOf(_redeemer);

```
[L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L140), [L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L145), [L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L163), [L193](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L193), [L284](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L284), [L338](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L338), [L364](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L364), [L366](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L366), [L370](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370), [L424](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L424), [L500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621), [L625](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L625), [L648](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L648), [L704](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L704), [L742](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L742)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

71:         uint256 _price = priceFeed.fetchPrice();

235:         address _borrower = sortedCdps.getOwnerAddress(_liqState.cdpId);

279:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

309:         address _borrower = sortedCdps.getOwnerAddress(_recoveryState.cdpId);

366:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

436:             uint _cappedColl = collateral.getPooledEthByShares(_partialColl);

561:         toLiquidator = collateral.getSharesByPooledEth(_incentiveColl);

582:             toLiquidator = collateral.getSharesByPooledEth(_incentiveColl);

585:             _incentiveColl = collateral.getPooledEthByShares(_totalColToSend);

691:         vars.price = priceFeed.fetchPrice();

```
[L71](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L71), [L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L235), [L279](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L279), [L309](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L309), [L366](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L366), [L436](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L436), [L561](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L561), [L582](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L582), [L585](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L585), [L691](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L691)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

74:         uint256 price = priceFeed.fetchPrice();

93:         uint256 newTCR = EbtcMath._computeCR(
94:             collateral.getPooledEthByShares(systemCollShares),
95:             systemDebt,
96:             price
97:         );

297:         uint256 _totalCollateralSnapshot = activePool.getSystemCollShares() - _collRemainder;

494:         uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);
495:         return EbtcMath._computeCR(_totalColl, _systemDebt, _price);

564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

676:         uint256 NICR = EbtcMath._computeNominalCR(currentCollShares, currentEBTCDebt);

693:         uint256 NICR = EbtcMath._computeNominalCR(_newColl, _newDebt);

712:         uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);
713:         return EbtcMath._computeCR(_underlyingCollateral, currentDebt, _price);

878:         uint256 _systemCollShare = activePool.getSystemCollShares();

882:         uint256 _systemDebt = activePool.getSystemDebt();

```
[L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L74), [L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L93), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L297), [L494](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L494), [L564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L564), [L676](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L676), [L693](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L693), [L712](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L712), [L878](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L878), [L882](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L882)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

54:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());

145:         uint256 balance = IERC20(token).balanceOf(address(this));

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52), [L54](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L54), [L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145)

```solidity
File: packages/contracts/contracts/Governor.sol

47:             address user = users.at(i);

56:             address[] memory _usrs = users.values();

134:         bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values();

```
[L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L47), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L134)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

449:         uint256 minPrice = EbtcMath._min(_currentResponse.answer, _prevResponse.answer);
450:         uint256 maxPrice = EbtcMath._max(_currentResponse.answer, _prevResponse.answer);

531:         uint256 minPrice = EbtcMath._min(_fallbackResponse.answer, _chainlinkResponse.answer);

533:         uint256 maxPrice = EbtcMath._max(_fallbackResponse.answer, _chainlinkResponse.answer);

```
[L449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L449), [L531](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L531), [L533](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L533)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

601:             return data.head == _nextId && _NICR >= cdpManager.getCachedNominalICR(_nextId);

604:             return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);

607:             return
608:                 data.nodes[_prevId].nextId == _nextId &&
609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&
610:                 _NICR >= cdpManager.getCachedNominalICR(_nextId);

621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644:         if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {

```
[L601](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L601), [L604](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L604), [L607](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L607), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621), [L644](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

65:             vars.currentCdpId = sortedCdps.getLast();
66:             vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

72:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
73:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

90:                 uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

116:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);
117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

139:         uint256 maxRedeemableEBTC = EbtcMath._min(vars.remainingEbtcToRedeem, currentCdpDebt);

141:         uint256 newCollShare = cdpManager.getSyncedCdpCollShares(vars.currentCdpId);

144:         uint256 collShareToReceive = collateral.getSharesByPooledEth(
145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
146:         );

169:         uint256 arrayLength = cdpManager.getActiveCdpsCount();

172:             return (sortedCdps.nonExistId(), 0, _inputRandomSeed);

175:         hint = sortedCdps.getLast();
176:         diff = EbtcMath._getAbsoluteDifference(_CR, cdpManager.getSyncedNominalICR(hint));

185:             bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);
186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

189:             uint256 currentDiff = EbtcMath._getAbsoluteDifference(currentNICR, _CR);

204:         return EbtcMath._computeNominalCR(_coll, _debt);

217:         return EbtcMath._computeCR(_coll, _debt, _price);

```
[L65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L65), [L72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L72), [L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L90), [L116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116), [L139](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L139), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L141), [L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L144), [L169](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L169), [L172](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L172), [L175](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L175), [L185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L185), [L189](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L189), [L204](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L204), [L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L217)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));

173:             bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

176:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);

187:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

199:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

220:         uint256 ebtcBal = ebtcToken.balanceOf(address(this));
221:         uint256 collateralBal = stETH.sharesOf(address(this));

339:         LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

461:         OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

465:         bytes32 _cdpId = borrowerOperations.openCdp(
466:             flData.eBTCToMint,
467:             flData._upperHint,
468:             flData._lowerHint,
469:             flData.stETHToDeposit
470:         );

475:         CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483:         AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));

```
[L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L143), [L173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L173), [L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L176), [L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L187), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L220), [L339](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339), [L461](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L461), [L465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L465), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L475), [L483](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L483)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

64:         address _owner = IOwnerLike(address(this)).owner();

```
[L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

68:         return (activePool.getSystemCollShares());

76:         return (activePool.getSystemDebt());

89:         uint256 _systemStEthBalance = collateral.getPooledEthByShares(systemCollShares);
90:         TCR = EbtcMath._computeCR(_systemStEthBalance, systemDebt, _price);

```
[L68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L68), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L76), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L89)

</details>

&nbsp;
## [G-27] Using `storage` instead of `memory` for structs/arrays saves gas


When fetching data from a storage location, assigning the data to a `memory` variable causes all fields of the struct/array to be read from storage, which incurs a Gcoldsload (2100 gas) for each field of the struct/array. If the fields are read from the new memory variable, they incur an additional `MLOAD` rather than a cheap stack read.

Instead of declaring the variable with the `memory` keyword, declaring the variable with the `storage` keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incuring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a `memory` variable, is if the full struct/array is being returned by the function, is being passed to a function that requires `memory`, or if the array/struct is being read from another `memory` array/struct.

<details>
<summary>Instances: 28</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

427:             MoveTokensParams memory _varMvTokens = MoveTokensParams(
428:                 msg.sender,
429:                 vars.collSharesChange,
430:                 (vars.isCollIncrease ? _stEthBalanceIncrease : 0),
431:                 vars.isCollIncrease,
432:                 _debtChange,
433:                 _isDebtIncrease
434:             );

```
[L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L427)

```solidity
File: packages/contracts/contracts/CdpManager.sol

150:         CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
151:             Cdps[_redeemColFromCdp.cdpId].debt,
152:             Cdps[_redeemColFromCdp.cdpId].coll
153:         );

395:                 SingleRedemptionInputs memory _redeemColFromCdp = SingleRedemptionInputs(
396:                     _cId,
397:                     totals.remainingDebtToRedeem,
398:                     totals.price,
399:                     _upperPartialRedemptionHint,
400:                     _lowerPartialRedemptionHint,
401:                     _partialRedemptionHintNICR
402:                 );
403:                 SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
404:                     _redeemColFromCdp
405:                 );

437:             bytes32[] memory _toRemoveIds = _getCdpIdsToRemove(
438:                 _lastRedeemed,
439:                 _numCdpsFullyRedeemed,
440:                 _firstRedeemed
441:             );

496:         bytes32[] memory _toRemoveIds = new bytes32[](_total);

```
[L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L150), [L395](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L395), [L437](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L437), [L496](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L496)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

101:         LiquidationLocals memory _liqState = LiquidationLocals(
102:             _cdpId,
103:             _partialAmount,
104:             _price,
105:             _ICR,
106:             _upperPartialHint,
107:             _lowerPartialHint,
108:             (_recoveryModeAtStart),
109:             _TCR,
110:             0,
111:             0,
112:             0,
113:             0,
114:             0
115:         );

117:         LiquidationRecoveryModeLocals memory _rs = LiquidationRecoveryModeLocals(
118:             systemDebt,
119:             systemColl,
120:             0,
121:             0,
122:             0,
123:             _cdpId,
124:             _price,
125:             _ICR,
126:             0,
127:             0
128:         );

210:             LiquidationLocals memory _outputState = _liquidateIndividualCdpSetupCDPInNormalMode(
211:                 _liqState
212:             );

404:         CdpDebtAndCollShares memory _debtAndColl = _getSyncedDebtAndCollShares(_cdpId);

614:         LiquidationLocals memory _liqState = LiquidationLocals(
615:             vars.cdpId,
616:             0,
617:             _price,
618:             vars.ICR,
619:             vars.cdpId,
620:             vars.cdpId,
621:             (false),
622:             _TCR,
623:             0,
624:             0,
625:             0,
626:             0,
627:             0
628:         );

630:         LiquidationLocals memory _outputState = _liquidateIndividualCdpSetupCDPInNormalMode(
631:             _liqState
632:         );

649:         LiquidationRecoveryModeLocals memory _recState = LiquidationRecoveryModeLocals(
650:             _systemDebt,
651:             _systemCollShares,
652:             0,
653:             0,
654:             0,
655:             vars.cdpId,
656:             _price,
657:             vars.ICR,
658:             0,
659:             0
660:         );

662:         LiquidationRecoveryModeLocals
663:             memory _outputState = _liquidateIndividualCdpSetupCDPInRecoveryMode(_recState);

751:         bool[] memory _liqFlags = new bool[](_cnt);

```
[L101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L101), [L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L117), [L210](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L210), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L404), [L614](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L614), [L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L630), [L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L649), [L662](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L662), [L751](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L751)

```solidity
File: packages/contracts/contracts/Governor.sol

56:             address[] memory _usrs = users.values();

134:         bytes32[] memory _sigs = enabledFunctionSigsByTarget[_target].values();

```
[L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L56), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L134)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

100:         ChainlinkResponse memory chainlinkResponse = _getCurrentChainlinkResponse();
101:         ChainlinkResponse memory prevChainlinkResponse = _getPrevChainlinkResponse(
102:             chainlinkResponse.roundEthBtcId,
103:             chainlinkResponse.roundStEthEthId
104:         );
105:         FallbackResponse memory fallbackResponse = _getCurrentFallbackResponse();

```
[L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L100)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

310:         bytes32[] memory userCdps = new bytes32[](maxArraySize);

522:             Node memory _node = data.nodes[_id];

```
[L310](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L310), [L522](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

199:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

339:         LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

374:         LeverageMacroOperation memory operation = decodeFLData(data);

461:         OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

475:         CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483:         AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));

```
[L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L199), [L339](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339), [L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L374), [L461](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L461), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L475), [L483](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L483)

</details>

&nbsp;
## [G-28] Refactor modifiers to call a local function

Modifiers code is copied in all instances where it's used, increasing bytecode size. By doing a refractor to the internal function, one can reduce bytecode size significantly at the cost of one JUMP.

<details>
<summary>Instances: 5</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

144:     modifier nonReentrantSelfAndCdpM() {

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L144)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

241:     modifier nonReentrantSelfAndBOps() {

```
[L241](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L241)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

26:     modifier requiresAuth() virtual {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L26)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

16:     modifier requiresAuth() virtual {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L16)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

13:     modifier nonReentrant() virtual {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L13)

</details>

&nbsp;
## [G-29] Combine multiple mappings with the same key type where appropriate

Saves a storage slot for the mapping. Depending on the circumstances and
sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads
and subsequent writes can also be cheaper when a function requires both
values and they both fit in the same storage slot. Finally, if both fields
are accessed in the same function, can save ~42 gas per access due to
[not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0)
(Gkeccak256 - 30 gas) and that calculation's associated stack operations.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

168:     mapping(bytes32 => Cdp) public Cdps;

190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;

```
[L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L168), [L190](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L190), [L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L202)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

51:     mapping(address => uint256) private _balances;
52:     mapping(address => mapping(address => uint256)) private _allowances;

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L51)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

32:     mapping(address => bytes32) public getUserRoles;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```
[L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32), [L34](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36)

</details>

&nbsp;
## [G-30] Nesting `if`-statements is cheaper than using `&&`

Nesting `if`-statements avoids the stack operations of setting up and using
an extra `jumpdest`, and saves **6
[gas](https://gist.github.com/IllIllI000/7f3b818abecfadbef93b894481ae7d19)**.
Note that if an `else` statement is present, then nesting would use **more**
gas, not less.

<details>
<summary>Instances: 13</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {
394:             _requireValidDebtRepayment(vars.debt, vars.netDebtChange);
395:             _requireSufficientEbtcTokenBalance(msg.sender, vars.netDebtChange);
396:             _requireNonZeroDebt(vars.debt - vars.netDebtChange);
397:         }

```
[L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

157:             if (
158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&
159:                 liquidationValues.debtToBurn == 0
160:             ) {
161:                 // retry with fully liquidation
162:                 (
163:                     liquidationValues.debtToBurn,
164:                     liquidationValues.totalCollToSendToLiquidator,
165:                     liquidationValues.debtToRedistribute,
166:                     liquidationValues.liquidatorCollSharesReward,
167:                     liquidationValues.collSurplus
168:                 ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);
169:             }

756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
757:                 vars.ICR = getSyncedICR(vars.cdpId, _price);

759:                 if (
760:                     !vars.backToNormalMode &&
761:                     (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))
762:                 ) {
763:                     vars.price = _price;
764:                     _syncAccounting(vars.cdpId);
765:                     _getLiquidationValuesRecoveryMode(
766:                         _price,
767:                         vars.entireSystemDebt,
768:                         vars.entireSystemColl,
769:                         vars,
770:                         singleLiquidation
771:                     );

773:                     // Update aggregate trackers
774:                     vars.entireSystemDebt = vars.entireSystemDebt - singleLiquidation.debtToBurn;
775:                     vars.entireSystemColl =
776:                         vars.entireSystemColl -
777:                         singleLiquidation.totalCollToSendToLiquidator -
778:                         singleLiquidation.collSurplus;

780:                     // Add liquidation values to their respective running totals
781:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

783:                     _TCR = _computeTCRWithGivenSystemValues(
784:                         vars.entireSystemColl,
785:                         vars.entireSystemDebt,
786:                         _price
787:                     );
788:                     vars.backToNormalMode = _TCR < CCR ? false : true;
789:                     _liqFlags[vars.i] = true;
790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {
791:                     _syncAccounting(vars.cdpId);
792:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

794:                     // Add liquidation values to their respective running totals
795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
796:                     _liqFlags[vars.i] = true;
797:                 }

819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
820:                 vars.ICR = getSyncedICR(vars.cdpId, _price);

822:                 if (_checkICRAgainstMCR(vars.ICR)) {
823:                     _syncAccounting(vars.cdpId);
824:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);

826:                     // Add liquidation values to their respective running totals
827:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
828:                 }
829:             }

```
[L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L157), [L756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756), [L759](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L759), [L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L773), [L780](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L780), [L783](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L783), [L794](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L794), [L819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819), [L822](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L822), [L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L826)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

512:         if (_newIndex > _oldIndex && totalStakes > 0) {
513:             (
514:                 uint256 _feeTaken,
515:                 uint256 _newFeePerUnit,
516:                 uint256 _perUnitError
517:             ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
518:             _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError);
519:             _updateSystemSnapshotsExcludeCollRemainder(0);
520:         }

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
797:             (
798:                 uint256 _feeSplitDistributed,
799:                 uint256 _newCollShareAfter
800:             ) = getAccumulatedFeeSplitApplied(_cdpId, _systemStEthFeePerUnitIndex);
801:             _feeSplitApplied = _feeSplitDistributed;
802:             _newCollShare = _newCollShareAfter;
803:         }

```
[L512](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512), [L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

226:                 if (
227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)
229:                 ) {
230:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);
231:                     return _storeChainlinkPrice(chainlinkResponse.answer);
232:                 }

372:                 if (
373:                     !_fallbackIsBroken(fallbackResponse) &&
374:                     !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
375:                 ) {
376:                     address oldFallbackCaller = address(fallbackCaller);
377:                     fallbackCaller = newFallbackCaler;
378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
379:                 }

```
[L226](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226), [L372](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L372)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

202:             if (maxNodes > 0 && i >= maxNodes) {
203:                 break;
204:             }

259:             if (maxNodes > 0 && i >= maxNodes) {
260:                 break;
261:             }

330:             if (maxNodes > 0 && i >= maxNodes) {
331:                 break;
332:             }

621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {
622:             return (dummyId, _startId);
623:         }

644:         if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
645:             return (_startId, dummyId);
646:         }

```
[L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202), [L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259), [L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330), [L621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621), [L644](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644)

</details>

&nbsp;
## [G-31] Use `unchecked` for operations that cannot overflow/underflow

By bypassing Solidity's built in overflow/underflow checks using `unchecked`, we can save gas. This is especially beneficial for the index variable within for loops (saves 120 gas per iteration).

<details>
<summary>Instances: 13</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

717:         bytes32 digest = keccak256(
718:             abi.encodePacked(
719:                 "\x19\x01",
720:                 domainSeparator(),
721:                 keccak256(
722:                     abi.encode(
723:                         _PERMIT_POSITION_MANAGER_TYPEHASH,
724:                         _borrower,
725:                         _positionManager,
726:                         _approval,
727:                         _nonces[_borrower]++,
728:                         _deadline
729:                     )
730:                 )
731:             )
732:         );

```
[L717](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L717)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

209:         bytes32 digest = keccak256(
210:             abi.encodePacked(
211:                 "\x19\x01",
212:                 domainSeparator(),
213:                 keccak256(
214:                     abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
215:                 )
216:             )
217:         );

```
[L209](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L209)

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

62:                     j++;

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

87:                     j++;

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

111:                     j++;

122:         for (uint8 i = 0; i < roleIds.length; i++) {

```
[L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46), [L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57), [L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76), [L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84), [L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98), [L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

195:             i++;

```
[L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195)

</details>

&nbsp;
## [G-32] Function names can be optimized to save gas

`public`/`external` function names and `public` member variable names can be
optimized to save gas. Below are the interfaces/abstract contracts that can
be optimized so that the most frequently-called functions use the least
amount of gas possible during method lookup. Method IDs that have two leading
zero bytes can save 128 gas each during deployment, and renaming functions
to have lower method IDs will save 22 gas per call,
[per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92).

<details>
<summary>Instances: 17</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

74:     function getSystemCollShares() external view override returns (uint256) {

82:     function getSystemDebt() external view override returns (uint256) {

89:     function getFeeRecipientClaimableCollShares() external view override returns (uint256) {

100:     function transferSystemCollShares(address _account, uint256 _shares) public override {

129:     function transferSystemCollSharesAndLiquidatorReward(
130:         address _account,
131:         uint256 _shares,
132:         uint256 _liquidatorRewardShares
133:     ) external override {

157:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external override {

194:     function increaseSystemDebt(uint256 _amount) external override {

207:     function decreaseSystemDebt(uint256 _amount) external override {

242:     function increaseSystemCollShares(uint256 _value) external override {

261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {

317:     function flashFee(address token, uint256 amount) public view override returns (uint256) {

328:     function maxFlashLoan(address token) public view override returns (uint256) {

346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22), [L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L74), [L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L82), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L89), [L100](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L100), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L129), [L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L157), [L194](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L194), [L207](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L207), [L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L242), [L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L261), [L317](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L317), [L328](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L328), [L346](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371), [L390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390), [L404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404), [L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

21: contract BorrowerOperations is
22:     EbtcBase,
23:     ReentrancyGuard,
24:     IBorrowerOperations,
25:     ERC3156FlashLender,
26:     AuthNoOwner,
27:     PermitNonce
28: {

168:     function openCdp(
169:         uint256 _debt,
170:         bytes32 _upperHint,
171:         bytes32 _lowerHint,
172:         uint256 _stEthBalance
173:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

187:     function openCdpFor(
188:         uint256 _debt,
189:         bytes32 _upperHint,
190:         bytes32 _lowerHint,
191:         uint256 _stEthBalance,
192:         address _borrower
193:     ) external override nonReentrantSelfAndCdpM returns (bytes32) {

203:     function addColl(
204:         bytes32 _cdpId,
205:         bytes32 _upperHint,
206:         bytes32 _lowerHint,
207:         uint256 _stEthBalanceIncrease
208:     ) external override nonReentrantSelfAndCdpM {

219:     function withdrawColl(
220:         bytes32 _cdpId,
221:         uint256 _stEthBalanceDecrease,
222:         bytes32 _upperHint,
223:         bytes32 _lowerHint
224:     ) external override nonReentrantSelfAndCdpM {

235:     function withdrawDebt(
236:         bytes32 _cdpId,
237:         uint256 _debt,
238:         bytes32 _upperHint,
239:         bytes32 _lowerHint
240:     ) external override nonReentrantSelfAndCdpM {

250:     function repayDebt(
251:         bytes32 _cdpId,
252:         uint256 _debt,
253:         bytes32 _upperHint,
254:         bytes32 _lowerHint
255:     ) external override nonReentrantSelfAndCdpM {

270:     function adjustCdp(
271:         bytes32 _cdpId,
272:         uint256 _stEthBalanceDecrease,
273:         uint256 _debtChange,
274:         bool _isDebtIncrease,
275:         bytes32 _upperHint,
276:         bytes32 _lowerHint
277:     ) external override nonReentrantSelfAndCdpM {

300:     function adjustCdpWithColl(
301:         bytes32 _cdpId,
302:         uint256 _stEthBalanceDecrease,
303:         uint256 _debtChange,
304:         bool _isDebtIncrease,
305:         bytes32 _upperHint,
306:         bytes32 _lowerHint,
307:         uint256 _stEthBalanceIncrease
308:     ) external override nonReentrantSelfAndCdpM {

553:     function closeCdp(bytes32 _cdpId) external override {

599:     function claimSurplusCollShares() external override {

608:     function getPositionManagerApproval(
609:         address _borrower,
610:         address _positionManager
611:     ) external view override returns (PositionManagerApproval) {

628:     function setPositionManagerApproval(
629:         address _positionManager,
630:         PositionManagerApproval _approval
631:     ) external override {

647:     function revokePositionManagerApproval(address _positionManager) external override {

653:     function renouncePositionManagerApproval(address _borrower) external override {

659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

665:     function domainSeparator() public view override returns (bytes32) {

687:     function version() external pure override returns (string memory) {

693:     function permitTypeHash() external pure override returns (bytes32) {

706:     function permitPositionManagerApproval(
707:         address _borrower,
708:         address _positionManager,
709:         PositionManagerApproval _approval,
710:         uint256 _deadline,
711:         uint8 v,
712:         bytes32 r,
713:         bytes32 s
714:     ) external override {

1077:     function flashLoan(
1078:         IERC3156FlashBorrower receiver,
1079:         address token,
1080:         uint256 amount,
1081:         bytes calldata data
1082:     ) external override returns (bool) {

1114:     function flashFee(address token, uint256 amount) public view override returns (uint256) {

1124:     function maxFlashLoan(address token) public view override returns (uint256) {

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21), [L168](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L168), [L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L187), [L203](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L203), [L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L219), [L235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L235), [L250](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L250), [L270](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L270), [L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L300), [L553](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L553), [L599](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L599), [L608](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L608), [L628](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L628), [L647](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L647), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L653), [L659](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L659), [L665](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L665), [L687](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L687), [L693](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L693), [L706](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L706), [L1077](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1077), [L1114](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1114), [L1124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1124), [L1140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140), [L1154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154), [L1167](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167)

```solidity
File: packages/contracts/contracts/CdpManager.sol

16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

66:     function getActiveCdpsCount() external view override returns (uint256) {

73:     function getIdFromCdpIdsArray(uint256 _index) external view override returns (bytes32) {

99:     function liquidate(bytes32 _cdpId) external override {

109:     function partiallyLiquidate(
110:         bytes32 _cdpId,
111:         uint256 _partialAmount,
112:         bytes32 _upperPartialHint,
113:         bytes32 _lowerPartialHint
114:     ) external override {

126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

320:     function redeemCollateral(
321:         uint256 _debt,
322:         bytes32 _firstRedemptionHint,
323:         bytes32 _upperPartialRedemptionHint,
324:         bytes32 _lowerPartialRedemptionHint,
325:         uint256 _partialRedemptionHintNICR,
326:         uint256 _maxIterations,
327:         uint256 _maxFeePercentage
328:     ) external override nonReentrantSelfAndBOps {

514:     function syncAccounting(bytes32 _cdpId) external virtual override {

523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {

538:     function closeCdp(
539:         bytes32 _cdpId,
540:         address _borrower,
541:         uint256 _debt,
542:         uint256 _coll
543:     ) external override {

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

580:     function getCachedTCR(uint256 _price) external view override returns (uint256) {

589:     function checkRecoveryMode(uint256 _price) external view override returns (bool) {

638:     function getRedemptionRate() public view override returns (uint256) {

643:     function getRedemptionRateWithDecay() public view override returns (uint256) {

661:     function getRedemptionFeeWithDecay(
662:         uint256 _stETHToRedeem
663:     ) external view override returns (uint256) {

717:     function getDeploymentStartTime() public view returns (uint256) {

727:     function checkPotentialRecoveryMode(
728:         uint256 _systemCollShares,
729:         uint256 _systemDebt,
730:         uint256 _price
731:     ) external view returns (bool) {

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {

856:     function getCdpStatus(bytes32 _cdpId) external view override returns (uint256) {

863:     function getCdpStake(bytes32 _cdpId) external view override returns (uint256) {

871:     function getCdpDebt(bytes32 _cdpId) external view override returns (uint256) {

879:     function getCdpCollShares(bytes32 _cdpId) external view override returns (uint256) {

891:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view override returns (uint256) {

905:     function initializeCdp(
906:         bytes32 _cdpId,
907:         uint256 _debt,
908:         uint256 _coll,
909:         uint256 _liquidatorRewardShares,
910:         address _borrower
911:     ) external {

946:     function updateCdp(
947:         bytes32 _cdpId,
948:         address _borrower,
949:         uint256 _coll,
950:         uint256 _debt,
951:         uint256 _newColl,
952:         uint256 _newDebt
953:     ) external {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16), [L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L66), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L73), [L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L99), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L109), [L126](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126), [L320](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L320), [L514](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L514), [L523](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L523), [L538](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L538), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570), [L580](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L580), [L589](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L589), [L638](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L638), [L643](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L643), [L661](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L661), [L717](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L717), [L727](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L727), [L773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773), [L788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807), [L830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830), [L843](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843), [L856](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L856), [L863](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L863), [L871](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L871), [L879](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L879), [L891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L891), [L905](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905), [L946](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L946)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

13: contract LiquidationLibrary is CdpManagerStorage {

40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {

50:     function partiallyLiquidate(
51:         bytes32 _cdpId,
52:         uint256 _partialAmount,
53:         bytes32 _upperPartialHint,
54:         bytes32 _lowerPartialHint
55:     ) external nonReentrantSelfAndBOps {

679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13), [L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L40), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L50), [L679](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

32:     function notifyStartGracePeriod(uint256 tcr) external {

42:     function notifyEndGracePeriod(uint256 tcr) external {

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

504:     function syncGlobalAccounting() external {

527:     function syncGlobalAccountingAndGracePeriod() public {

552:     function calcFeeUponStakingReward(
553:         uint256 _newIndex,
554:         uint256 _prevIndex
555:     ) public view returns (uint256, uint256, uint256) {

616:     function getAccumulatedFeeSplitApplied(
617:         bytes32 _cdpId,
618:         uint256 _systemStEthFeePerUnitIndex
619:     ) public view returns (uint256, uint256) {

673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {

684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {

701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {

728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

745:     function getSyncedDebtAndCollShares(
746:         bytes32 _cdpId
747:     ) public view returns (uint256 debt, uint256 coll) {

839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {

848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {

864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {

890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L32), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L42), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111), [L504](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L504), [L527](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L527), [L552](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L552), [L616](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L616), [L673](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L673), [L684](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L684), [L701](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L701), [L719](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719), [L728](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L728), [L745](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L745), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L839), [L848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L848), [L864](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L864), [L874](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L874), [L890](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L890)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

61:     function getTotalSurplusCollShares() external view override returns (uint256) {

67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

77:     function increaseSurplusCollShares(address _account, uint256 _amount) external override {

89:     function claimSurplusCollShares(address _account) external override {

130:     function increaseTotalSurplusCollShares(uint256 _value) external override {

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```
[L16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L16), [L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L61), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L67), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L77), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L89), [L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L130), [L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

85:     function mint(address _account, uint256 _amount) external override {

95:     function burn(address _account, uint256 _amount) external override {

104:     function burn(uint256 _amount) external {

111:     function totalSupply() external view override returns (uint256) {

115:     function balanceOf(address account) external view override returns (uint256) {

119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

125:     function allowance(address owner, address spender) external view override returns (uint256) {

129:     function approve(address spender, uint256 amount) external override returns (bool) {

134:     function transferFrom(
135:         address sender,
136:         address recipient,
137:         uint256 amount
138:     ) external override returns (bool) {

152:     function increaseAllowance(
153:         address spender,
154:         uint256 addedValue
155:     ) external override returns (bool) {

160:     function decreaseAllowance(
161:         address spender,
162:         uint256 subtractedValue
163:     ) external override returns (bool) {

176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

182:     function domainSeparator() public view override returns (bytes32) {

199:     function permit(
200:         address owner,
201:         address spender,
202:         uint256 amount,
203:         uint256 deadline,
204:         uint8 v,
205:         bytes32 r,
206:         bytes32 s
207:     ) external override {

225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

331:     function name() external pure override returns (string memory) {

337:     function symbol() external pure override returns (string memory) {

343:     function decimals() external pure override returns (uint8) {

349:     function version() external pure override returns (string memory) {

355:     function permitTypeHash() external pure override returns (bytes32) {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L85), [L95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L95), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L104), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L111), [L115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L115), [L119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L119), [L125](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L125), [L129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L129), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L134), [L152](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L152), [L160](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L160), [L176](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L176), [L182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L182), [L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L199), [L225](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L225), [L331](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L331), [L337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L337), [L343](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L343), [L349](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L349), [L355](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L355)

```solidity
File: packages/contracts/contracts/Governor.sol

13: contract Governor is RolesAuthority {

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

131:     function getEnabledFunctionsInTarget(
132:         address _target
133:     ) public view returns (bytes4[] memory _funcs) {

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```
[L13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L43), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96), [L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120), [L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

98:     function fetchPrice() external override returns (uint256) {

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L21), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L98), [L358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

51: contract SortedCdps is ISortedCdps {

105:     function toCdpId(
106:         address owner,
107:         uint256 blockHeight,
108:         uint256 nonce
109:     ) public pure returns (bytes32) {

123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {

130:     function nonExistId() public pure override returns (bytes32) {

140:     function cdpOfOwnerByIndex(
141:         address owner,
142:         uint256 index
143:     ) external view override returns (bytes32) {

155:     function cdpOfOwnerByIdx(
156:         address owner,
157:         uint256 index,
158:         bytes32 startNodeId,
159:         uint maxNodes
160:     ) external view override returns (bytes32, bool) {

216:     function cdpCountOf(address owner) external view override returns (uint256) {

227:     function getCdpCountOf(
228:         address owner,
229:         bytes32 startNodeId,
230:         uint maxNodes
231:     ) external view override returns (uint256, bytes32) {

270:     function getCdpsOf(address owner) external view override returns (bytes32[] memory cdps) {

286:     function getAllCdpsOf(
287:         address owner,
288:         bytes32 startNodeId,
289:         uint maxNodes
290:     ) external view override returns (bytes32[] memory, uint256, bytes32) {

344:     function insert(
345:         address owner,
346:         uint256 _NICR,
347:         bytes32 _prevId,
348:         bytes32 _nextId
349:     ) external override returns (bytes32) {

410:     function remove(bytes32 _id) external override {

419:     function batchRemove(bytes32[] memory _ids) external override {

498:     function reInsert(
499:         bytes32 _id,
500:         uint256 _newNICR,
501:         bytes32 _prevId,
502:         bytes32 _nextId
503:     ) external override {

519:     function contains(bytes32 _id) public view override returns (bool) {

530:     function isFull() public view override returns (bool) {

536:     function isEmpty() public view override returns (bool) {

542:     function getSize() external view override returns (uint256) {

548:     function getMaxSize() external view override returns (uint256) {

554:     function getFirst() external view override returns (bytes32) {

560:     function getLast() external view override returns (bytes32) {

567:     function getNext(bytes32 _id) external view override returns (bytes32) {

574:     function getPrev(bytes32 _id) external view override returns (bytes32) {

583:     function validInsertPosition(
584:         uint256 _NICR,
585:         bytes32 _prevId,
586:         bytes32 _nextId
587:     ) external view override returns (bool) {

666:     function findInsertPosition(
667:         uint256 _NICR,
668:         bytes32 _prevId,
669:         bytes32 _nextId
670:     ) external view override returns (bytes32, bytes32) {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L51), [L105](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L105), [L123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L123), [L130](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L130), [L140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L140), [L155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L155), [L216](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L216), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L227), [L270](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L270), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L286), [L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L344), [L410](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L410), [L419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L419), [L498](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L498), [L519](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L519), [L530](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L530), [L536](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L536), [L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L542), [L548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L548), [L554](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L554), [L560](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L560), [L567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L567), [L574](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L574), [L583](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L583), [L666](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L666)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

11: contract HintHelpers is EbtcBase {

48:     function getRedemptionHints(
49:         uint256 _EBTCamount,
50:         uint256 _price,
51:         uint256 _maxIterations
52:     )
53:         external
54:         view
55:         returns (
56:             bytes32 firstRedemptionHint,
57:             uint256 partialRedemptionHintNICR,
58:             uint256 truncatedEBTCamount,
59:             uint256 partialRedemptionNewColl
60:         )
61:     {

164:     function getApproxHint(
165:         uint256 _CR,
166:         uint256 _numTrials,
167:         uint256 _inputRandomSeed
168:     ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

203:     function computeNominalCR(uint256 _coll, uint256 _debt) external pure returns (uint256) {

212:     function computeCR(
213:         uint256 _coll,
214:         uint256 _debt,
215:         uint256 _price
216:     ) external pure returns (uint256) {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11), [L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48), [L164](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L164), [L203](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L203), [L212](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L212)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

26: contract LeverageMacroBase {

39:     function owner() public virtual returns (address) {

118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

214:     function sweepToCaller() public {

234:     function sweepToken(address token, uint256 amount) public {

338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

344:     function onFlashLoan(
345:         address initiator,
346:         address token,
347:         uint256 amount,
348:         uint256 fee,
349:         bytes calldata data
350:     ) external returns (bytes32) {

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L39), [L118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L118), [L214](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L214), [L234](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234), [L338](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L338), [L344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L344)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

11: contract LeverageMacroFactory {

38:     function deployNewMacro() external returns (address) {

43:     function deployNewMacro(address _owner) public returns (address) {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11), [L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L38), [L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L43)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

11: contract LeverageMacroReference is LeverageMacroBase {

44:     function owner() public override returns (address) {

50:     function resetApprovals() external {

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L11), [L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L44), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L50)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

25: contract SimplifiedDiamondLike {

51:     function setFallbackHandler(bytes4 sig, address handler) external {

66:     function setAllowAnyCall(bool allowNonCallbacks) external {

76:     function enableCallbackForCall() external {

110:     function execute(Operation[] calldata ops) external payable {

```
[L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25), [L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L51), [L66](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L66), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L76), [L110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L110)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

10: contract AuthNoOwner {

22:     function authority() public view returns (Authority) {

26:     function authorityInitialized() public view returns (bool) {

38:     function setAuthority(address newAuthority) public virtual {

```
[L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L22), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L26), [L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

42:     function doesRoleHaveCapability(
43:         uint8 role,
44:         address target,
45:         bytes4 functionSig
46:     ) public view virtual returns (bool) {

50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

63:     function canCall(
64:         address user,
65:         address target,
66:         bytes4 functionSig
67:     ) public view virtual override returns (bool) {

85:     function setPublicCapability(
86:         address target,
87:         bytes4 functionSig,
88:         bool enabled
89:     ) public virtual requiresAuth {

106:     function setRoleCapability(
107:         uint8 role,
108:         address target,
109:         bytes4 functionSig,
110:         bool enabled
111:     ) public virtual requiresAuth {

133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L12), [L38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L42), [L50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L50), [L63](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L63), [L85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85), [L106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106), [L133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133), [L147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147)

</details>

&nbsp;
## [G-33] Pack state variables into fewer storage slots

If variables occupying the same slot are both written the same function or by the constructor, avoids a separate Gsset (20000 gas). Reads of the variables can also be cheaper.

For more information about variable packing, see [here](https://blog.techfund.jp/p/solidity-variable-packing-saving-deployment-costs/#:~:text=Solidity%20variable%20packing%20is%20a,bytes%20equal%20to%20256%20bits.).

<details>
<summary>Instances: 1</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19)

</details>

&nbsp;
## [G-34] Use `payable` for constructor

Payable functions cost less gas to execute, since the compiler does not have
to add extra checks to ensure that a payment wasn't provided. A constructor
can safely be marked as payable, since only the deployer would be able to
pass funds, and the project itself would not pass any funds.

<details>
<summary>Instances: 19</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

46:     constructor(
47:         address _borrowerOperationsAddress,
48:         address _cdpManagerAddress,
49:         address _collTokenAddress,
50:         address _collSurplusAddress,
51:         address _feeRecipientAddress
52:     ) {

```
[L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

107:     constructor(
108:         address _cdpManagerAddress,
109:         address _activePoolAddress,
110:         address _collSurplusPoolAddress,
111:         address _priceFeedAddress,
112:         address _sortedCdpsAddress,
113:         address _ebtcTokenAddress,
114:         address _feeRecipientAddress,
115:         address _collTokenAddress
116:     ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) {

```
[L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107)

```solidity
File: packages/contracts/contracts/CdpManager.sol

30:     constructor(
31:         address _liquidationLibraryAddress,
32:         address _authorityAddress,
33:         address _borrowerOperationsAddress,
34:         address _collSurplusPoolAddress,
35:         address _ebtcTokenAddress,
36:         address _sortedCdpsAddress,
37:         address _activePoolAddress,
38:         address _priceFeedAddress,
39:         address _collTokenAddress
40:     )
41:         CdpManagerStorage(
42:             _liquidationLibraryAddress,
43:             _authorityAddress,
44:             _borrowerOperationsAddress,
45:             _collSurplusPoolAddress,
46:             _ebtcTokenAddress,
47:             _sortedCdpsAddress,
48:             _activePoolAddress,
49:             _priceFeedAddress,
50:             _collTokenAddress
51:         )
52:     {

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

14:     constructor(
15:         address _borrowerOperationsAddress,
16:         address _collSurplusPool,
17:         address _ebtcToken,
18:         address _sortedCdps,
19:         address _activePool,
20:         address _priceFeed,
21:         address _collateral
22:     )
23:         CdpManagerStorage(
24:             address(0),
25:             address(0),
26:             _borrowerOperationsAddress,
27:             _collSurplusPool,
28:             _ebtcToken,
29:             _sortedCdps,
30:             _activePool,
31:             _priceFeed,
32:             _collateral
33:         )
34:     {}

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

217:     constructor(
218:         address _liquidationLibraryAddress,
219:         address _authorityAddress,
220:         address _borrowerOperationsAddress,
221:         address _collSurplusPool,
222:         address _ebtcToken,
223:         address _sortedCdps,
224:         address _activePool,
225:         address _priceFeed,
226:         address _collateral
227:     ) EbtcBase(_activePool, _priceFeed, _collateral) {

```
[L217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

42:     constructor(
43:         address _borrowerOperationsAddress,
44:         address _cdpManagerAddress,
45:         address _activePoolAddress,
46:         address _collTokenAddress
47:     ) {

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

61:     constructor(
62:         address _cdpManagerAddress,
63:         address _borrowerOperationsAddress,
64:         address _authorityAddress
65:     ) {

```
[L61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61)

```solidity
File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```
[L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

57:     constructor(
58:         address _fallbackCallerAddress,
59:         address _authorityAddress,
60:         address _collEthCLFeed,
61:         address _ethBtcCLFeed
62:     ) {

```
[L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {

```
[L88](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

27:     constructor(
28:         address _sortedCdpsAddress,
29:         address _cdpManagerAddress,
30:         address _collateralAddress,
31:         address _activePoolAddress,
32:         address _priceFeedAddress
33:     ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {

```
[L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

51:     constructor(
52:         address _borrowerOperationsAddress,
53:         address _activePool,
54:         address _cdpManager,
55:         address _ebtc,
56:         address _coll,
57:         address _sortedCdps,
58:         bool _sweepToCaller
59:     ) {

```
[L51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

41:     constructor(
42:         address _borrowerOperationsAddress,
43:         address _activePool,
44:         address _cdpManager,
45:         address _ebtc,
46:         address _coll,
47:         address _sortedCdps
48:     )
49:         LeverageMacroBase(
50:             _borrowerOperationsAddress,
51:             _activePool,
52:             _cdpManager,
53:             _ebtc,
54:             _coll,
55:             _sortedCdps,
56:             false // Do not sweep to caller
57:         )
58:     {

```
[L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

21:     constructor(
22:         address _borrowerOperationsAddress,
23:         address _activePool,
24:         address _cdpManager,
25:         address _ebtc,
26:         address _coll,
27:         address _sortedCdps
28:     ) {

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

17:     constructor(
18:         address _borrowerOperationsAddress,
19:         address _activePool,
20:         address _cdpManager,
21:         address _ebtc,
22:         address _coll,
23:         address _sortedCdps,
24:         address _owner
25:     )
26:         LeverageMacroBase(
27:             _borrowerOperationsAddress,
28:             _activePool,
29:             _cdpManager,
30:             _ebtc,
31:             _coll,
32:             _sortedCdps,
33:             true // Sweep to caller since this is not supposed to hold funds
34:         )
35:     {

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

44:     constructor(address _owner) {

```
[L44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {

```
[L18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L18)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

```
[L20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20)

</details>

&nbsp;
## [G-35] Pre-compute hashes

When calculating a deterministic `keccak256` hash, compute the value beforehand
and hard code it instead of computing at runtime/compile time to save gas.

Calculating a `keccak256` hash costs 30 gas + 6 gas for each 256 bits of data
being hashed.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```
[L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11)

</details>

&nbsp;
## [G-36] Use `private` rather than `public` for constants

Saves 3406-3606 gas in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table. If needed to be viewed externally, the values can be read from the verified contract source code.

<details>
<summary>Instances: 31</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";

```
[L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";

```
[L29](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

122:     string public constant NAME = "CdpManager";

139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero

150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122), [L139](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L139), [L141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141), [L149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L149), [L150](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L150)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";

32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

```
[L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22), [L32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L32), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L33), [L36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L36), [L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L42)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";

80:     bytes32 public constant dummyId =

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52), [L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L80)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";

```
[L12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

9:     uint256 public constant MAX_BPS = 10_000;

10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```
[L9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9), [L10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L10), [L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

19:     uint256 public constant LICR = 1030000000000000000; // 103%

22:     uint256 public constant MCR = 1100000000000000000; // 110%

25:     uint256 public constant CCR = 1250000000000000000; // 125%

28:     uint256 public constant LIQUIDATOR_REWARD = 2e17;

31:     uint256 public constant MIN_NET_STETH_BALANCE = 2e18;

33:     uint256 public constant PERCENT_DIVISOR = 200; // dividing by 200 yields 0.5%

35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

37:     uint256 public constant STAKING_REWARD_SPLIT = 5_000; // taking 50% cut from staking reward

39:     uint256 public constant MAX_REWARD_SPLIT = 10_000;

```
[L19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L19), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L22), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L25), [L28](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L28), [L31](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L31), [L33](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L33), [L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L35), [L37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L37), [L39](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L39)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

7:     uint256 public constant MAX_TCR = type(uint256).max;

```
[L7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L7)

</details>

&nbsp;
## [G-37] `require()` or `revert()` statements that check input arguments should be at the top of the function

Checks that involve constants should come before checks that involve state
variables, function calls, and calculations. By doing these checks first,
the function is able to revert before wasting a `Gcoldsload` (**2100 gas***)
in a function that may ultimately revert in the unhappy case.

<details>
<summary>Instances: 5</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

269:         require(amount <= maxFlashLoan(token), "ActivePool: Too much");

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```
[L269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269), [L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1085:         require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much");

```
[L1085](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

```
[L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```
[L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)

</details>

&nbsp;
## [G-38]  Split `require` statements using `&&`

Replacing with two separate require statements saves 16 gas per instance.

<details>
<summary>Instances: 33</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

734:         require(

735:             recoveredAddress != address(0) && recoveredAddress == _borrower,

736:             "BorrowerOperations: Invalid signature"

737:         );

```
[L734](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734), [L735](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L735), [L736](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L736), [L737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L737)

```solidity
File: packages/contracts/contracts/CdpManager.sol

762:         require(

763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,

764:             "Max fee percentage must be between redemption fee floor and 100%"

765:         );

```
[L762](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762), [L763](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L763), [L764](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L764), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L765)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

261:         require(

262:             closedStatus != Status.nonExistent && closedStatus != Status.active,

263:             "CdpManagerStorage: close non-exist or non-active CDP!"

264:         );

466:         require(

467:             cdpStatus != Status.nonExistent && cdpStatus != Status.active,

468:             "CdpManagerStorage: remove non-exist or non-active CDP!"

469:         );

653:         require(

654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

655:             "CdpManager: Only one cdp in the system"

656:         );

```
[L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261), [L262](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L262), [L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L263), [L264](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L264), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466), [L467](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L467), [L468](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L468), [L469](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L469), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653), [L654](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L654), [L655](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L655), [L656](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L656)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

296:         require(

297:             _recipient != address(0) && _recipient != address(this),

298:             "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"

299:         );

300:         require(

301:             _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,

302:             "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"

303:         );

```
[L296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296), [L297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297), [L298](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L298), [L299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L299), [L300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300), [L301](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L301), [L302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L302), [L303](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L303)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

79:         require(

80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&

81:                 !_chainlinkIsFrozen(chainlinkResponse),

82:             "PriceFeed: Chainlink must be working and current"

83:         );

```
[L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79), [L80](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L80), [L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L81), [L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L82), [L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L83)

</details>

&nbsp;
## [G-39] Not using the named return variable is confusing and can waste gas

Consider changing the variable to be an unnamed one, since the variable is
never assigned, nor is it returned by name. If the optimizer is not turned
on, leaving the code as it is will also waste gas for the stack variable.

<details>
<summary>Instances: 21</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

744:     function _getCollSharesChangeFromStEthChange(
745:         uint256 _collReceived,
746:         uint256 _requestedCollWithdrawal
747:     ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

```
[L744](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744)

```solidity
File: packages/contracts/contracts/CdpManager.sol

570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

```
[L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L570)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

544:     function _calculatePartialLiquidationSurplusAndCap(
545:         uint256 _ICR,
546:         uint256 _price,
547:         uint256 _totalDebtToBurn,
548:         uint256 _totalColToSend
549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

570:     function _calculateFullLiquidationSurplusAndCap(
571:         uint256 _ICR,
572:         uint256 _price,
573:         uint256 _totalDebtToBurn,
574:         uint256 _totalColToSend
575:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

```
[L544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544), [L570](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L570)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {

745:     function getSyncedDebtAndCollShares(
746:         bytes32 _cdpId
747:     ) public view returns (uint256 debt, uint256 coll) {

```
[L304](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L304), [L719](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L719), [L745](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L745)

```solidity
File: packages/contracts/contracts/Governor.sol

43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {

96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

131:     function getEnabledFunctionsInTarget(
132:         address _target
133:     ) public view returns (bytes4[] memory _funcs) {

146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

```
[L43](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L43), [L73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L73), [L96](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L96), [L131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L131), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L146)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

582:     function _getCurrentFallbackResponse()
583:         internal
584:         view
585:         returns (FallbackResponse memory fallbackResponse)
586:     {

```
[L582](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

270:     function getCdpsOf(address owner) external view override returns (bytes32[] memory cdps) {

```
[L270](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L270)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

48:     function getRedemptionHints(
49:         uint256 _EBTCamount,
50:         uint256 _price,
51:         uint256 _maxIterations
52:     )
53:         external
54:         view
55:         returns (
56:             bytes32 firstRedemptionHint,
57:             uint256 partialRedemptionHintNICR,
58:             uint256 truncatedEBTCamount,
59:             uint256 partialRedemptionNewColl
60:         )
61:     {

```
[L48](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L48)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

```
[L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L83)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

83:     function _getTCRWithSystemDebtAndCollShares(
84:         uint256 _price
85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

```
[L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L67), [L75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L75), [L83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L35)

```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

259:     function getSyncedDebtAndCollShares(
260:         bytes32 _cdpId
261:     ) external view returns (uint256 debt, uint256 collShares);

```
[L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L259)

</details>

&nbsp;
## [G-40] Use Solidity version `0.8.19` for gas savings

Upgrade to the latest solidity version 0.8.19 to get additional gas savings.
See [here](https://blog.soliditylang.org/2023/02/22/solidity-0.8.19-release-announcement/)
for reference.

<details>
<summary>Instances: 19</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3)

```solidity
File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3)

```solidity
File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2)

```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2)

```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2)

```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;

```
[L3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;

```
[L2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2)

</details>

&nbsp;
## [G-41] State variable read in a loop

The state variable should be cached in and read from a local variable, or
accumulated in a local variable then written to storage once outside of the
loop, rather than reading/updating it on every iteration of the loop, which
will replace each `Gwarmaccess` (**100 gas**) with a much cheaper stack read.

<details>
<summary>Instances: 8</summary>

```solidity
File: packages/contracts/contracts/SortedCdps.sol

199:             _currentCdpId = data.nodes[_currentCdpId].prevId;

256:             _currentCdpId = data.nodes[_currentCdpId].prevId;

327:             _currentCdpId = data.nodes[_currentCdpId].prevId;

450:             delete data.nodes[_ids[i]];

630:             prevId = data.nodes[prevId].nextId;
631:             nextId = data.nodes[prevId].nextId;

653:             nextId = data.nodes[nextId].prevId;
654:             prevId = data.nodes[nextId].prevId;

```
[L199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L199), [L256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256), [L327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L327), [L450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L450), [L630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653)

</details>

&nbsp;
## [G-42] Structs can be packed into fewer storage slots

Each slot saved can avoid an extra Gsset (20000 gas) for the first
setting of the struct. Subsequent reads as well as writes have smaller
gas savings.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

97:     struct MoveTokensParams {
98:         address user;
99:         uint256 collSharesChange;
100:         uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101:         bool isCollIncrease;
102:         uint256 netDebtChange;
103:         bool isDebtIncrease;
104:     }

```
[L97](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L97)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

99:     struct Operation {
100:         address to; // Target to call
101:         bool checkSuccess; // If false we will ignore a revert
102:         uint128 value; // How much ETH to send
103:         uint128 gas; // How much gas to send
104:         bool capGas; // true to use above "gas" setting or we send gasleft()
105:         OperationType opType; // See `OperationType`
106:         bytes data; // Calldata to send (funsig + data)
107:     }

```
[L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99)

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17)

</details>

&nbsp;
## [G-43] Pack structs into fewer storage slots by truncating `uint256` values referencing time

By using a `uint32` rather than a larger type for variables that track
timestamps, one can save gas by using fewer storage slots per struct,
at the expense of the protocol breaking after the year 2106 (when `uint32`
wraps). If this is an acceptable tradeoff, each slot saved can avoid an
extra Gsset (20000 gas) for the first setting of the struct. Subsequent
reads as well as writes have smaller gas savings.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }

26:     struct FallbackResponse {
27:         uint256 answer;
28:         uint256 timestamp;
29:         bool success;
30:     }

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17), [L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26)

</details>

&nbsp;
## [G-44] Remove superfluous event fields

`block.number` and `block.timestamp` are included in event emission automatically
and so emitting them manually wastes gas.

<details>
<summary>Instances: 3</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

```
[L698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

```
[L542](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L542)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

```
[L381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381)

</details>

&nbsp;
## [G-45] Use `!= 0` instead of `> 0` for uints

<details>
<summary>Instances: 50</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

267:         require(amount > 0, "ActivePool: 0 Amount");

```
[L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```
[L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393), [L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463), [L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835), [L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936), [L1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083)

```solidity
File: packages/contracts/contracts/CdpManager.sol

388:         while (
389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
390:         ) {

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

497:         while (_cnt > 0 && _id != bytes32(0)) {

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

```
[L388](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L388), [L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431), [L497](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L497), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626), [L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

195:             if (_outputState.totalSurplusCollShares > 0) {

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

525:         if (totalDebtToRedistribute > 0) {

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

713:         if (totals.totalCollSurplus > 0) {

```
[L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L195), [L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L261), [L266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L266), [L336](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L336), [L342](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L342), [L525](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L525), [L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710), [L713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L713)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

315:         if (_debtIndexDiff > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {

```
[L315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315), [L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L362), [L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L369), [L380](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L380), [L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453), [L512](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512), [L765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765), [L796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796), [L829](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L829), [L879](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L879)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

```
[L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92)

```solidity
File: packages/contracts/contracts/Governor.sol

53:         if (count > 0) {

81:         if (count > 0) {

104:         if (count > 0) {

135:         if (_sigs.length > 0) {

```
[L53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L53), [L81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L81), [L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L104), [L135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L135)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

457:         uint256 percentDeviation = maxPrice > 0
458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice
459:             : 0;

488:         return
489:             _fallbackResponse.timestamp > 0 &&
490:             _responseTimeout(_fallbackResponse.timestamp, fallbackCaller.fallbackTimeout());

```
[L457](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457), [L488](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L488)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

274:         if (_ownedCount > 0) {

330:             if (maxNodes > 0 && i >= maxNodes) {

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```
[L202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202), [L259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L274), [L330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371), [L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

84:             while (
85:                 vars.currentCdpUser != address(0) &&
86:                 vars.remainingEbtcToRedeem > 0 &&
87:                 _maxIterations-- > 0
88:             ) {

```
[L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L84)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {

```
[L128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L128), [L223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L223), [L227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L227), [L293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L293), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L307)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

93:         if (_debt > 0) {

109:         if (_debt > 0) {

```
[L93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L93), [L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L109)

</details>

&nbsp;
## [G-46] Usage of `uint` smaller than 32 bytes (256 bits) incurs overhead

When using elements that are smaller than 32 bytes, your contract's gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.

Consider using a larger size then downcasting where needed.

https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

```
[L21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L21), [L22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L22), [L24](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L24), [L25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L25)

```solidity
File: packages/contracts/contracts/Governor.sol

30:     mapping(uint8 => string) internal roleNames;

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L30)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14)

</details>

&nbsp;
## [G-47] Remove unused state variables

Reduces bytecode size and reduces deployment cost.

<details>
<summary>Instances: 9</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;
143:     bool public redemptionsPaused;

148:     uint256 public minuteDecayFactor = 999037758833783000;

159:     uint256 public beta = 2;

161:     uint256 public baseRate;

166:     uint256 public lastRedemptionTimestamp;

193:     uint256 public lastEBTCDebtErrorRedistribution;

```
[L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148), [L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L159), [L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161), [L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L166), [L193](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L193)

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```
[L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30)

</details>

&nbsp;
## [G-48] Avoid updating storage when the value hasn't changed

If the old value is equal to the new value, not re-storing the value will
avoid a Gsreset (2900 gas), potentially at the expense of a Gcoldsload
(2100 gas) or a Gwarmaccess (100 gas).

<details>
<summary>Instances: 6</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );

117:         syncGlobalAccountingAndGracePeriod();
118:         recoveryModeGracePeriodDuration = _gracePeriod;
119:         emit GracePeriodDurationSet(_gracePeriod);
120:     }

574:     function _takeSplitAndUpdateFeePerUnit(
575:         uint256 _feeTaken,
576:         uint256 _newPerUnit,
577:         uint256 _newErrorPerUnit
578:     ) internal {
579:         uint256 _oldPerUnit = systemStEthFeePerUnitIndex;

581:         systemStEthFeePerUnitIndex = _newPerUnit;
582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;

584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");
585:         activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken);

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);
588:     }

```
[L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111), [L117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L117), [L574](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574), [L581](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L581), [L584](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584), [L587](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L587)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

546:     function _changeStatus(Status _status) internal {
547:         status = _status;
548:         emit PriceFeedStatusChanged(_status);
549:     }

553:     function _storePrice(uint256 _currentPrice) internal {
554:         lastGoodPrice = _currentPrice;
555:         emit LastGoodPriceUpdated(_currentPrice);
556:     }

```
[L546](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L546), [L553](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L553)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

42:     function setAuthority(Authority newAuthority) public virtual {
43:         // We check if the caller is the owner first because we want to ensure they can
44:         // always swap out the authority even if it's reverting or using up a lot of gas.
45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

47:         authority = newAuthority;

49:         emit AuthorityUpdated(msg.sender, newAuthority);
50:     }

52:     function transferOwnership(address newOwner) public virtual requiresAuth {
53:         owner = newOwner;

55:         emit OwnershipTransferred(msg.sender, newOwner);
56:     }

```
[L42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L42), [L47](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L47), [L49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L49), [L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52), [L55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L55)

</details>

&nbsp;
## [G-49] Use assembly for integer zero checks

Using assembly to check for zero can save gas by allowing more direct access to the
evm and reducing some of the overhead associated with high-level operations in solidity.

<details>
<summary>Instances: 26</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

807:         require(
808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809:             "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810:         );

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

846:         require(
847:             _stEthBalanceDecrease == 0,
848:             "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849:         );

```
[L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807), [L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831), [L846](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846)

```solidity
File: packages/contracts/contracts/CdpManager.sol

159:         if (newDebt == 0) {

377:         if (_maxIterations == 0) {

```
[L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L159), [L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L377)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

144:         if (_liqState.partialAmount == 0) {

157:             if (
158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&
159:                 liquidationValues.debtToBurn == 0
160:             ) {

417:         if (newColl == 0) {

863:         if (_debt == 0) {

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L144), [L157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L157), [L417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L417), [L863](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L863)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

443:         if (totalCollateralSnapshot == 0) {

623:         if (
624:             _cdpStEthFeePerUnitIndex == 0 ||
625:             _cdpCol == 0 ||
626:             _cdpStEthFeePerUnitIndex == _systemStEthFeePerUnitIndex
627:         ) {

```
[L443](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L443), [L623](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L623)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

419:         if (
420:             _response.timestampEthBtc == 0 ||
421:             _response.timestampEthBtc > block.timestamp ||
422:             _response.timestampStEthEth == 0 ||
423:             _response.timestampStEthEth > block.timestamp
424:         ) {

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

475:         if (_response.answer == 0) {

532:         if (minPrice == 0) return false;

695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

777:         if (_roundId == 0) return false;

```
[L419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L419), [L471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L471), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L475), [L532](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L532), [L695](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L695), [L777](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L777)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

89:         if (_size == 0) {

305:         if (maxArraySize == 0) {

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

537:         return data.size == 0;

```
[L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L89), [L305](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L305), [L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352), [L537](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L537)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

78:         if (_maxIterations == 0) {

171:         if (arrayLength == 0) {

```
[L78](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L78), [L171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L171)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

64:         if (_minutes == 0) {

74:             if (n % 2 == 0) {

```
[L64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L64), [L74](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L74)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

124:             if (enabledFunctionSigsByTarget[target].length() == 0) {

```
[L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L124)

</details>

&nbsp;
## [G-50] Use custom errors

Use of custom errors reduces both deployment and runtime gas costs, and allows
passing of dynamic information.

<details>
<summary>Instances: 163</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

220:         require(
221:             msg.sender == borrowerOperationsAddress,
222:             "ActivePool: Caller is not BorrowerOperations"
223:         );

228:         require(
229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230:             "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231:         );

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

267:         require(amount > 0, "ActivePool: 0 Amount");

269:         require(amount <= maxFlashLoan(token), "ActivePool: Too much");

277:         require(
278:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279:             "ActivePool: IERC3156: Callback failed"
280:         );

294:         require(
295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),
296:             "ActivePool: Must repay Balance"
297:         );
298:         require(
299:             collateral.sharesOf(address(this)) >= systemCollShares,
300:             "ActivePool: Must repay Share"
301:         );
302:         require(
303:             collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,
304:             "ActivePool: Should keep same collateral share rate"
305:         );

318:         require(token == address(collateral), "ActivePool: collateral Only");
319:         require(!flashLoansPaused, "ActivePool: Flash Loans Paused");

350:         require(
351:             cachedFeeRecipientCollShares >= _shares,
352:             "ActivePool: Insufficient fee recipient coll"
353:         );

374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```
[L104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104), [L137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137), [L162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162), [L220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220), [L228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228), [L236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236), [L267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267), [L269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269), [L277](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277), [L294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294), [L318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L318), [L350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350), [L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374), [L377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377), [L393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393), [L407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407)

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");
146:         require(
147:             ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148:             "CdpManager: Reentrancy in nonReentrant call"
149:         );

368:         require(
369:             _stEthBalanceDecrease <= _cdpStEthBalance,
370:             "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371:         );

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

541:         require(
542:             vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543:             "BorrowerOperations: deposited collateral mismatch!"
544:         );

715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

734:         require(
735:             recoveredAddress != address(0) && recoveredAddress == _borrower,
736:             "BorrowerOperations: Invalid signature"
737:         );

807:         require(
808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
809:             "BorrowerOperations: Cannot add and withdraw collateral in same operation"
810:         );

818:         require(
819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
820:             "BorrowerOperations: There must be either a collateral change or a debt change"
821:         );

826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

839:         require(
840:             !_checkRecoveryModeForTCR(_tcr),
841:             "BorrowerOperations: Operation not permitted during Recovery Mode"
842:         );

846:         require(
847:             _stEthBalanceDecrease == 0,
848:             "BorrowerOperations: Collateral withdrawal not permitted during Recovery Mode"
849:         );

911:         require(
912:             _newICR >= MCR,
913:             "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"
914:         );

918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

922:         require(
923:             _newICR >= _oldICR,
924:             "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925:         );

929:         require(
930:             _newTCR >= CCR,
931:             "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932:         );

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

940:         require(
941:             _stEthBalance >= MIN_NET_STETH_BALANCE,
942:             "BorrowerOperations: Cdp's net stEth balance must not fall below minimum"
943:         );

947:         require(
948:             _debtRepayment <= _currentDebt,
949:             "BorrowerOperations: Amount repaid must not be larger than the Cdp's debt"
950:         );

957:         require(
958:             ebtcToken.balanceOf(_account) >= _debtRepayment,
959:             "BorrowerOperations: Caller doesnt have enough eBTC to make repayment"
960:         );

970:         require(
971:             _approval != PositionManagerApproval.None,
972:             "BorrowerOperations: Only borrower account or approved position manager can OpenCdp on borrower's behalf"
973:         );

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

1085:         require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much");

1091:         require(
1092:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
1093:             "IERC3156: Callback failed"
1094:         );

1115:         require(token == address(ebtcToken), "BorrowerOperations: EBTC Only");
1116:         require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

1141:         require(
1142:             _feeRecipientAddress != address(0),
1143:             "BorrowerOperations: Cannot set feeRecipient to zero address"
1144:         );

1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```
[L145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145), [L368](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368), [L463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463), [L541](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541), [L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715), [L734](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734), [L807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807), [L818](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818), [L826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826), [L831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831), [L835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835), [L839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839), [L846](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846), [L911](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911), [L918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918), [L922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922), [L929](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929), [L936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936), [L940](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940), [L947](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947), [L957](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957), [L970](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970), [L1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083), [L1085](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085), [L1091](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091), [L1115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1115), [L1141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141), [L1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155)

```solidity
File: packages/contracts/contracts/CdpManager.sol

332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");
503:         require(
504:             _toRemoveIds[_total - 1] == _end,
505:             "CdpManager: batchRemoveSortedCdpIds check end error"
506:         );

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

678:         require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!"); // The baseRate can decay to 0

743:         require(
744:             callerBalance >= _amount,
745:             "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746:         );
747:         require(
748:             callerBalance <= _totalSupply,
749:             "CdpManager: redeemer's EBTC balance exceeds total supply!"
750:         );

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

762:         require(
763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764:             "Max fee percentage must be between redemption fee floor and 100%"
765:         );

774:         require(
775:             _stakingRewardSplit <= MAX_REWARD_SPLIT,
776:             "CDPManager: new staking reward split exceeds max"
777:         );

789:         require(
790:             _redemptionFeeFloor >= MIN_REDEMPTION_FEE_FLOOR,
791:             "CDPManager: new redemption fee floor is lower than minimum"
792:         );
793:         require(
794:             _redemptionFeeFloor <= DECIMAL_PRECISION,
795:             "CDPManager: new redemption fee floor is higher than maximum"
796:         );

808:         require(
809:             _minuteDecayFactor >= MIN_MINUTE_DECAY_FACTOR,
810:             "CDPManager: new minute decay factor out of range"
811:         );
812:         require(
813:             _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
814:             "CDPManager: new minute decay factor out of range"
815:         );

```
[L332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332), [L431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431), [L502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502), [L626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626), [L672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672), [L678](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678), [L743](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743), [L754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754), [L758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758), [L762](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762), [L774](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774), [L789](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789), [L808](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808)

```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

82:             require(
83:                 _checkICRAgainstLiqThreshold(_ICR, _TCR),
84:                 "LiquidationLibrary: ICR is not below liquidation threshold in current mode"
85:             );

89:             require(
90:                 cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP,
91:                 "LiquidationLibrary: Recovery Mode grace period not started"
92:             );
93:             require(
94:                 block.timestamp >
95:                     cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
96:                 "LiquidationLibrary: Recovery mode grace period still in effect"
97:             );

477:             require(
478:                 getCachedICR(_cdpId, _partialState.price) >= _partialState.ICR,
479:                 "LiquidationLibrary: !_newICR>=_ICR"
480:             );

680:         require(
681:             _cdpArray.length != 0,
682:             "LiquidationLibrary: Calldata address array must not be empty"
683:         );

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

901:         require(
902:             (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903:                 _entireDebt,
904:             "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905:         );

909:         require(
910:             _entireColl >= MIN_NET_STETH_BALANCE,
911:             "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912:         );

```
[L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56), [L82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82), [L89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89), [L477](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477), [L680](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680), [L710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710), [L901](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901), [L909](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909)

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );

242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");
243:         require(
244:             ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245:             "BorrowerOperations: Reentrancy in nonReentrant call"
246:         );

261:         require(
262:             closedStatus != Status.nonExistent && closedStatus != Status.active,
263:             "CdpManagerStorage: close non-exist or non-active CDP!"
264:         );

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

466:         require(
467:             cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468:             "CdpManagerStorage: remove non-exist or non-active CDP!"
469:         );

475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

653:         require(
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655:             "CdpManager: Only one cdp in the system"
656:         );

660:         require(
661:             msg.sender == borrowerOperationsAddress,
662:             "CdpManager: Caller is not the BorrowerOperations contract"
663:         );

```
[L112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112), [L242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242), [L261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261), [L453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453), [L466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475), [L556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556), [L584](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584), [L649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649), [L653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653), [L660](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660)

```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

99:         require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

113:         require(
114:             msg.sender == borrowerOperationsAddress,
115:             "CollSurplusPool: Caller is not Borrower Operations"
116:         );

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```
[L92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92), [L99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99), [L113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113), [L120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120), [L124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124), [L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143), [L146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146)

```solidity
File: packages/contracts/contracts/EBTCToken.sol

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

208:         require(deadline >= block.timestamp, "EBTC: expired deadline");

219:         require(recoveredAddress == owner, "EBTC: invalid signature");

247:         require(sender != address(0), "EBTCToken: zero sender!");
248:         require(recipient != address(0), "EBTCToken: zero recipient!");

251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

271:         require(account != address(0), "EBTCToken: burn from zero account!");

274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

286:         require(owner != address(0), "EBTCToken: zero approve owner!");
287:         require(spender != address(0), "EBTCToken: zero approve spender!");

296:         require(
297:             _recipient != address(0) && _recipient != address(this),
298:             "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299:         );
300:         require(
301:             _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302:             "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303:         );

307:         require(
308:             msg.sender == borrowerOperationsAddress,
309:             "EBTCToken: Caller is not BorrowerOperations"
310:         );

315:         require(
316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||
318:                 isAuthorized(msg.sender, msg.sig),
319:             "EBTC: Caller is neither BorrowerOperations nor CdpManager nor authorized"
320:         );

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");

```
[L144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144), [L165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165), [L208](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L208), [L219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L219), [L247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247), [L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251), [L263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263), [L271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271), [L274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274), [L286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286), [L296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296), [L307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307), [L315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315), [L324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324)

```solidity
File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );

```
[L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

365:         require(!isFull(), "SortedCdps: List is full");

367:         require(!contains(_id), "SortedCdps: List already contains the node");

369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

427:         require(
428:             _firstPrev != dummyId || _lastNext != dummyId,
429:             "SortedCdps: batchRemove() leave ZERO node left!"
430:         );

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

458:         require(contains(_id), "SortedCdps: List does not contain the id");

506:         require(contains(_id), "SortedCdps: List does not contain the id");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

720:         require(
721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722:             "SortedCdps: Caller is neither BO nor CdpM"
723:         );

```
[L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352), [L365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L365), [L367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367), [L369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369), [L371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371), [L422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422), [L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427), [L433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433), [L458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458), [L506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506), [L508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508), [L715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715), [L720](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

40:         revert("Must be overridden");

45:         require(owner() == msg.sender, "Must be owner");

179:             require(
180:                 cdpInfo.status == checkParams.expectedStatus,
181:                 "!LeverageMacroReference: openCDP status check"
182:             );

191:             require(
192:                 cdpInfo.status == checkParams.expectedStatus,
193:                 "!LeverageMacroReference: adjustCDP status check"
194:             );

201:             require(
202:                 cdpInfo.status == checkParams.expectedStatus,
203:                 "!LeverageMacroReference: closeCDP status check"
204:             );

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

255:             revert("Operator not found");

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

356:             require(
357:                 msg.sender == address(borrowerOperations),
358:                 "LeverageMacroReference: wrong lender for eBTC flashloan"
359:             );

362:             require(
363:                 msg.sender == address(activePool),
364:                 "LeverageMacroReference: wrong lender for stETH flashloan"
365:             );

421:         require(success, "Call has failed");

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

452:         require(addy != address(borrowerOperations));
453:         require(addy != address(sortedCdps));
454:         require(addy != address(activePool));
455:         require(addy != address(cdpManager));
456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

```
[L40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40), [L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45), [L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179), [L191](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191), [L201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201), [L249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249), [L251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251), [L253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253), [L255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L255), [L352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352), [L356](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356), [L362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362), [L421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L421), [L440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440), [L452](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452)

```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

56:         require(sig != 0x94b24d09);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111:         require(msg.sender == owner, "Must be owner");

154:             require(success);

179:             require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks");

187:         require(facet != address(0), "Diamond: Function does not exist");

195:                 revert(0, returndatasize())

```
[L52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56), [L67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67), [L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111), [L154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154), [L179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179), [L187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187), [L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L195)

```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

27:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```
[L27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L27), [L45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

17:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");
57:         require(!_authorityInitialized, "Auth: authority already initialized");

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17), [L41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L41), [L56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L56)

```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

109:         require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");

```
[L109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L109)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

90:         require(
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
92:             "RolesAuthority: Capability Burned"
93:         );

134:         require(
135:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
136:             "RolesAuthority: Capability Burned"
137:         );

```
[L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90), [L134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134)

</details>

&nbsp;
## [G-51] Using `storage` instead of `memory` for state variables saves gas

When fetching data from a storage location, assigning the data to a `memory`
variable causes all fields of the struct/array to be read from storage, which
incurs a Gcoldsload (**2100 gas**) for *each* field of the struct/array. If
the fields are read from the new memory variable, they incur an additional
`MLOAD` rather than a cheap stack read. Instead of declaring the variable
with the `memory` keyword, declaring the variable with the `storage` keyword
and caching any fields that need to be re-read in stack variables, will be
much cheaper, only incurring the Gcoldsload for the fields actually read. The
only time it makes sense to read the whole struct/array into a `memory`
variable, is if the full struct/array is being returned by the function, is
being passed to a function that requires `memory`, or if the array/struct is
being read from another `memory` array/struct.

<details>
<summary>Instances: 7</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

427:             MoveTokensParams memory _varMvTokens = MoveTokensParams(
428:                 msg.sender,
429:                 vars.collSharesChange,
430:                 (vars.isCollIncrease ? _stEthBalanceIncrease : 0),
431:                 vars.isCollIncrease,
432:                 _debtChange,
433:                 _isDebtIncrease
434:             );

```
[L427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L427)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

522:             Node memory _node = data.nodes[_id];

```
[L522](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

339:         LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

374:         LeverageMacroOperation memory operation = decodeFLData(data);

461:         OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

475:         CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483:         AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));

```
[L339](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339), [L374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L374), [L461](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L461), [L475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L475), [L483](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L483)

</details>

&nbsp;
## [G-52] Use `uint(1)`/`uint(2)` instead of `true`/`false`

If you don't use boolean for storage you will avoid Gwarmaccess 100 gas. In
addition, state changes of boolean from `true` to `false` can cost up to
~20000 gas rather than `uint(2)` to `uint(1)` that would cost significantly
less. This implementation can be found in OpenZeppelin's
[ReentrancyGuard](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol#L23-L35)
implementation.

<details>
<summary>Instances: 4</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

143:     bool public redemptionsPaused;

```
[L143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143)

```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

35:     bool internal immutable willSweep;

```
[L35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L35)

```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

14:     bool private _authorityInitialized;

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

15:     bool public flashLoansPaused;

```
[L15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15)

</details>

&nbsp;
## [G-53] `++i` costs less gas than `i++`

True for `--i`/`i--` as well, and is especially important in for loops. Saves 5 gas per iteration.

<details>
<summary>Instances: 12</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

429:             _maxIterations--;

```
[L429](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L429)

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

62:                     j++;

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

87:                     j++;

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

111:                     j++;

122:         for (uint8 i = 0; i < roleIds.length; i++) {

```
[L46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46), [L57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57), [L62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L62), [L76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76), [L84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84), [L87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L87), [L98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98), [L107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107), [L111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L111), [L122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122)

```solidity
File: packages/contracts/contracts/HintHelpers.sol

195:             i++;

```
[L195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L195)

</details>

&nbsp;
## [G-54] State variables only assigned to in the constructor should be `immutable`

Avoids a Gsset (20000 gas) in the constructor, and replaces the first access
in each transaction (Gcoldsload - 2100 gas) and each access thereafter
(Gwarmacces - 100 gas) with a `PUSH32` (3 gas).

While strings are not value types, and therefore cannot be `immutable`/`constant`
if not hard-coded outside of the constructor, the same behavior can be
achieved by making the current contract `abstract` with `virtual` functions for
the `string` accessors, and having a child contract override the functions with
the hard-coded implementation-specific values.

<details>
<summary>Instances: 2</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

59:         systemStEthFeePerUnitIndex = DECIMAL_PRECISION;

```
[L59](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L59)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

90:             _size = type(uint256).max;

```
[L90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L90)

</details>

&nbsp;
## [G-55] State variables that do not change should be `constant` or `immutable`

Compared to regular state variables, the gas costs of constant and immutable
variables are much lower. For a constant variable, the expression assigned to
it is copied to all the places where it is accessed and also re-evaluated each
time. This allows for local optimizations. Immutable variables are evaluated
once at construction time and their value is copied to all the places in the
code where they are accessed. For these values, 32 bytes are reserved, even if
they would fit in fewer bytes. Due to this, constant values can sometimes be
cheaper than immutable values.

See [Solidity docs](https://docs.soliditylang.org/en/v0.8.11/contracts.html#constant-and-immutable-state-variables)
for more info.

<details>
<summary>Instances: 17</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;
143:     bool public redemptionsPaused;

148:     uint256 public minuteDecayFactor = 999037758833783000;

159:     uint256 public beta = 2;

161:     uint256 public baseRate;

163:     uint256 public stakingRewardSplit;

166:     uint256 public lastRedemptionTimestamp;

193:     uint256 public lastEBTCDebtErrorRedistribution;

```
[L142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L142), [L148](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L148), [L159](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L159), [L161](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L161), [L163](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L163), [L166](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L166), [L193](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L193)

```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);

```
[L17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L17)

```solidity
File: packages/contracts/contracts/SortedCdps.sol

77:     Data public data;

79:     uint256 public nextCdpNonce;

```
[L77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L77), [L79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L79)

```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance
15:     bool public flashLoansPaused;

```
[L14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14)

```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

11:     uint256 public locked = OPEN;

```
[L11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L11)

```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

26:     EnumerableSet.AddressSet internal users;
27:     EnumerableSet.AddressSet internal targets;

30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```
[L26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L26), [L30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30)

</details>

&nbsp;
## [G-56] Use `via-ir` for deployment

Enable on the command line using `--via-ir` or with the option `{"viaIR": true}`
for more powerful optimization passes that span across functions. See
[here](https://docs.soliditylang.org/en/v0.8.17/ir-breaking-changes.html) for
more info.

&nbsp;
