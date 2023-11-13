### <a id="summary-gas-optimizations"></a> Gas Optimizations
There are 759 instances over 27 issues.
|      ID       | Description                                                                                                                                                | Count | Gas Per Instance | Gas Savings |
| :-----------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------- | ----: | ---------------: | ----------: |
| [G-01](#g-01) | `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops |    10 |               60 |         600 |
| [G-02](#g-02) | `>=` costs less gas than `>`                                                                                                                               |    77 |                3 |         231 |
| [G-03](#g-03) | Constructors can be marked `payable`                                                                                                                       |    19 |               21 |         399 |
| [G-04](#g-04) | Don't compare boolean expressions to boolean literals                                                                                                      |     1 |                9 |           9 |
| [G-05](#g-05) | Events should be emitted outside of loops                                                                                                                  |     1 |              375 |         375 |
| [G-06](#g-06) | Functions guaranteed to revert when called by normal users can be marked `payable`                                                                         |    24 |               21 |         504 |
| [G-07](#g-07) | Gas use can be reduced by using Solidity 0.8.19 or later                                                                                                   |    39 |                - |           - |
| [G-08](#g-08) | `internal` functions not called by the contract should be removed to save deployment gas                                                                   |    15 |                - |           - |
| [G-09](#g-09) | `internal`/`private` functions only called once can be inlined to save gas                                                                                 |    77 |               20 |       1,540 |
| [G-10](#g-10) | `keccak256()` should only need to be called on a specific string literal once                                                                              |     4 |               21 |          84 |
| [G-11](#g-11) | Multiplication by powers of two should use bit shifting                                                                                                    |     1 |              112 |         112 |
| [G-12](#g-12) | Nesting `if`-statements is cheaper than using `&&`                                                                                                         |    14 |                6 |          84 |
| [G-13](#g-13) | Optimize names to save gas                                                                                                                                 |    26 |               22 |         572 |
| [G-14](#g-14) | Remove unused local variable                                                                                                                               |     4 |                - |           - |
| [G-15](#g-15) | `require()`/`revert()` strings longer than 32 bytes cost extra gas                                                                                         |   115 |                3 |         345 |
| [G-16](#g-16) | Splitting `require()` statements that use `&&` saves gas                                                                                                   |     8 |                3 |          24 |
| [G-17](#g-17) | State variable read in a loop                                                                                                                              |    31 |              100 |       3,100 |
| [G-18](#g-18) | The result of function calls should be cached rather than re-calling the function                                                                          |     1 |               20 |          20 |
| [G-19](#g-19) | `unchecked {}` can be used on the division of two `uint`s in order to save gas                                                                             |    31 |               20 |         620 |
| [G-20](#g-20) | Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead                                                                                   |     9 |               22 |         198 |
| [G-21](#g-21) | Use assembly for small keccak256 hashes, in order to save gas                                                                                              |     1 |               80 |          80 |
| [G-22](#g-22) | Use assembly to emit events, in order to save gas                                                                                                          |    55 |               38 |       2,090 |
| [G-23](#g-23) | Use custom errors rather than `revert()`/`require()` strings to save gas                                                                                   |   162 |                - |           - |
| [G-24](#g-24) | Use predefined address instead of `address(this)`                                                                                                          |    27 |               50 |       1,350 |
| [G-25](#g-25) | Use `uint256(1)`/`uint256(2)` instead of `true`/`false` to save gas for changes                                                                            |     3 |            8,550 |      25,650 |
| [G-26](#g-26) | Using `constant`s directly, rather than caching the value, saves gas                                                                                       |     1 |                - |           - |
| [G-27](#g-27) | Using `storage` instead of `memory` for structs/arrays saves gas                                                                                           |     3 |            4,200 |      12,600 |
|               | Total Gas Savings                                                                                                                                          |       |                  |      50,587 |

Gas totals use lower bounds of ranges and count two iterations of each `for` loop. Gas savings values are runtime values except for cases where only deployment values are applicable, like for constant declarations.

### <a id="details-gas-optimizations"></a> Gas Optimizations
#### <a id="g-01"></a> \[G-01\] `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops
##### Description:
`++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for` and `while` loops. This [saves 30-40 gas per loop iteration](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked).

##### Instances:
There are 10 instances of this issue.
<details><summary>View 10 Instances</summary>

```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {
```

| File Link                                                                                                        | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              8 | [46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46),[57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57),[76](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76),[84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84),[98](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L98),[107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107),[122](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L122),[137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

432:         for (uint256 i = 0; i < _len; ++i) {

449:         for (uint i = 0; i < _len; ++i) {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              2 | [432](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432),[449](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L449) |
___
</details>

#### <a id="g-02"></a> \[G-02\] `>=` costs less gas than `>`
##### Description:
The compiler uses opcodes `GT` and `ISZERO` for Solidity code that uses `>`, but only requires `LT` for `>=`, which saves 3 gas. If `<` is being used, the condition can be inverted.

##### Instances:
There are 77 instances of this issue.
<details><summary>View 77 Instances</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {

495:             if (newTCR < CCR) {

495:             if (newTCR < CCR) {

891:             if (_vars.newTCR < CCR) {

891:             if (_vars.newTCR < CCR) {
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              5 | [393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393),[495](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L495),[495](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L495),[891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L891),[891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L891) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

203:                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE

203:                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE

279:             getSyncedICR(_firstRedemptionHint, _price) < MCR

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

436:         } else if (_numCdpsFullyRedeemed > 1) {

436:         } else if (_numCdpsFullyRedeemed > 1) {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              6 | [203](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L203),[203](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L203),[279](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L279),[369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369),[436](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L436),[436](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L436) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

99:         if (newTCR < CCR) {

315:         if (_debtIndexDiff > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

369:             if (_feeSplitDistributed > 0) {

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

380:             if (_debtIndexDelta > 0) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

636:         if (_scaledCdpColl > _feeSplitDistributed) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |             17 | [99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L99),[315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315),[362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L362),[362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L362),[369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L369),[369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L369),[380](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L380),[380](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L380),[453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453),[512](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512),[512](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512),[636](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L636),[765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765),[765](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L765),[796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796),[829](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L829),[879](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L879) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {

93:         if (_debt > 0) {

109:         if (_debt > 0) {
```

| File Link                                                                                                                     | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                            |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol) |              3 | [60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60),[93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L93),[109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L109) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

53:         if (count > 0) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

81:         if (count > 0) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

104:         if (count > 0) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

135:         if (_sigs.length > 0) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {
```

| File Link                                                                                                        | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              8 | [53](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L53),[57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L57),[81](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L81),[84](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L84),[104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L104),[107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L107),[135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L135),[137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L137) |
___
```solidity
File: packages/contracts/contracts/HintHelpers.sol

93:                 if (currentCdpDebt > vars.remainingEbtcToRedeem) {

102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <
103:                         MIN_NET_STETH_BALANCE

102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <
103:                         MIN_NET_STETH_BALANCE

191:             if (currentDiff < diff) {
```

| File Link                                                                                                              | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              4 | [93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L93),[102](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102),[102](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102),[191](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L191) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              5 | [128](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L128),[223](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L223),[227](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L227),[293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L293),[307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L307) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

94:                 block.timestamp >
95:                     cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,

195:             if (_outputState.totalSurplusCollShares > 0) {

195:             if (_outputState.totalSurplusCollShares > 0) {

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

476:         if (_partialState.ICR > LICR) {

525:         if (totalDebtToRedistribute > 0) {

553:         if (_ICR > LICR) {

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

578:         if (_ICR > LICR) {

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

594:             debtToRedistribute = _debtToRepay < _totalDebtToBurn

713:         if (totals.totalCollSurplus > 0) {

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |             17 | [94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L94),[195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L195),[195](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L195),[261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L261),[266](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L266),[336](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L336),[342](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L342),[476](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L476),[525](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L525),[553](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L553),[555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555),[578](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L578),[579](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L579),[594](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L594),[713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L713),[788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788),[788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

421:             _response.timestampEthBtc > block.timestamp ||

423:             _response.timestampStEthEth > block.timestamp

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {
```

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                            |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              3 | [421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L421),[423](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L423),[471](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L471) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

274:         if (_ownedCount > 0) {

330:             if (maxNodes > 0 && i >= maxNodes) {

460:         if (data.size > 1) {

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {

690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {

690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              9 | [202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202),[259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259),[274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L274),[330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330),[460](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L460),[683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L683),[683](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L683),[690](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L690),[690](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L690) |
___
</details>

#### <a id="g-03"></a> \[G-03\] Constructors can be marked `payable`
##### Description:
`payable` functions cost less gas to execute since the compiler does not have to add extra checks to ensure that a payment wasn't provided. A `constructor` can safely be marked as `payable` since only the deployer can pass funds.

##### Instances:
There are 19 instances of this issue.
<details><summary>View 19 Instances</summary>

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

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              1 | [46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46) |
___
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

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [107](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107) |
___
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

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                         |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              1 | [217](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217) |
___
```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

42:     constructor(
43:         address _borrowerOperationsAddress,
44:         address _cdpManagerAddress,
45:         address _activePoolAddress,
46:         address _collTokenAddress
47:     ) {
```

| File Link                                                                                                                      | Instance Count | Instance Link                                                                                                     |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------- |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              1 | [42](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {
```

| File Link                                                                                                             | Instance Count | Instance Link                                                                                                       |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              1 | [18](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L18) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {
```

| File Link                                                                                                                     | Instance Count | Instance Link                                                                                                           |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol) |              1 | [52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52) |
___
```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                                 |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------- |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              1 | [20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

61:     constructor(
62:         address _cdpManagerAddress,
63:         address _borrowerOperationsAddress,
64:         address _authorityAddress
65:     ) {
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              1 | [61](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
```

| File Link                                                                                                        | Instance Count | Instance Link                                                                                              |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              1 | [36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36) |
___
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

| File Link                                                                                                              | Instance Count | Instance Link                                                                                                 |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------ |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              1 | [27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                       |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              1 | [51](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51) |
___
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

| File Link                                                                                                                                              | Instance Count | Instance Link                                                                                                                 |
| :----------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroDelegateTarget.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol) |              1 | [41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41) |
___
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

| File Link                                                                                                                                | Instance Count | Instance Link                                                                                                          |
| :--------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroFactory.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol) |              1 | [21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21) |
___
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

| File Link                                                                                                                                    | Instance Count | Instance Link                                                                                                            |
| :------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroReference.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol) |              1 | [17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17) |
___
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

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                        |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              1 | [14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

57:     constructor(
58:         address _fallbackCallerAddress,
59:         address _authorityAddress,
60:         address _collEthCLFeed,
61:         address _ethBtcCLFeed
62:     ) {
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57) |
___
```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

44:     constructor(address _owner) {
```

| File Link                                                                                                                                  | Instance Count | Instance Link                                                                                                           |
| :----------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol) |              1 | [44](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              1 | [88](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88) |
___
</details>

#### <a id="g-04"></a> \[G-04\] Don't compare boolean expressions to boolean literals
##### Description:
Do not compare `boolean` expressions to the `boolean` literals `true` and `false`.
 * No: `if (foo == true)`
 * Yes: `if (foo)`
 * No: `if (bar == false)`
 * Yes: `if (!bar)`

##### Instances:
There is 1 instance of this issue.
```solidity
File: packages/contracts/contracts/CdpManager.sol

332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332) |
___
#### <a id="g-05"></a> \[G-05\] Events should be emitted outside of loops
##### Description:
Emitting an event has an overhead of 375 gas, which will be incurred on every iteration of the loop. It is cheaper to `emit` [as a "batch"](https://github.com/ethereum/EIPs/blob/adad5968fd6de29902174e0cb51c8fc3dceb9ab5/EIPS/eip-1155.md?plain=1#L68) once after the loop has finished.

##### Instances:
There is 1 instance of this issue.
```solidity
File: packages/contracts/contracts/SortedCdps.sol

451:             emit NodeRemoved(_ids[i]);
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              1 | [451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451) |
___
#### <a id="g-06"></a> \[G-06\] Functions guaranteed to revert when called by normal users can be marked `payable`
##### Description:
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided. The extra opcodes avoided are `CALLVALUE`(2), `DUP1`(3), `ISZERO`(3), `PUSH2`(3), `JUMPI`(10), `PUSH1`(3), `DUP1`(3), `REVERT`(0), `JUMPDEST`(1), and `POP`(2). In addition to the extra deployment cost, on average, approximately 21 gas can be saved per call to the function.

##### Instances:
There are 24 instances of this issue.
<details><summary>View 24 Instances</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              5 | [346](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L346),[371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L371),[390](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L390),[404](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L404),[417](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L417) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                             |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              3 | [1140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1140),[1154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1154),[1167](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1167) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              5 | [773](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L773),[788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L788),[807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L807),[830](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L830),[843](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L843) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                         |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              1 | [111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L111) |
___
```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
```

| File Link                                                                                                                      | Instance Count | Instance Link                                                                                                       |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              1 | [142](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L142) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

52:     function transferOwnership(address newOwner) public virtual requiresAuth {
```

| File Link                                                                                                             | Instance Count | Instance Link                                                                                                       |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              1 | [52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L52) |
___
```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

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

| File Link                                                                                                                                 | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              5 | [20](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20),[85](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85),[106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106),[133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133),[147](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {
```

| File Link                                                                                                        | Instance Count | Instance Links                                                                                                                                                                                                          |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              2 | [36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36),[154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L154) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                                 |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------ |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [358](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L358) |
___
</details>

#### <a id="g-07"></a> \[G-07\] Gas use can be reduced by using Solidity 0.8.19 or later
##### Description:
See [Preventing Dead Code in Runtime Bytecode](https://blog.soliditylang.org/2023/02/22/solidity-0.8.19-release-announcement/#preventing-dead-code-in-runtime-bytecode) for the full details.

##### Instances:
There are 39 instances of this issue.
<details><summary>View 39 Instances</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                              |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L3) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                      |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L3) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                              |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L3) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                     |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L3) |
___
```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                      | Instance Count | Instance Link                                                                                                   |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------- |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                             | Instance Count | Instance Link                                                                                                     |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------- |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L2) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                            |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2) |
___
```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                   |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :------------------------------------------------------------------------------------------------------------------------------ |
| [ERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                     | Instance Count | Instance Link                                                                                                         |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                     | Instance Count | Instance Link                                                                                                         |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                   | Instance Count | Instance Link                                                                                                                |
| :------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :--------------------------------------------------------------------------------------------------------------------------- |
| [ReentrancyGuard.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2) |
___
```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                               |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------- |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                             |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                        | Instance Count | Instance Link                                                                                            |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L2) |
___
```solidity
File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                              | Instance Count | Instance Link                                                                                               |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                         | Instance Count | Instance Link                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [IActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :----------------------------------------------------------------------------------------------------------------------------- |
| [IBorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                         | Instance Count | Instance Link                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [ICdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [ICdpManagerData.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                   | Instance Count | Instance Link                                                                                                               |
| :------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------------- |
| [ICollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                       | Instance Count | Instance Link                                                                                                         |
| :------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [IEBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                             | Instance Count | Instance Link                                                                                                                    |
| :---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------- |
| [IERC3156FlashBorrower.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :----------------------------------------------------------------------------------------------------------------------------- |
| [IERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                     | Instance Count | Instance Link                                                                                                        |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------- |
| [IEbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [IFallbackCaller.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                           |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [IPermitNonce.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                             | Instance Count | Instance Link                                                                                                    |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------- |
| [IPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                                     | Instance Count | Instance Link                                                                                                                |
| :-------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------------- |
| [IPositionManagers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                       | Instance Count | Instance Link                                                                                                         |
| :------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [IPriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                                   | Instance Count | Instance Link                                                                                                                       |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------- |
| [IRecoveryModeGracePeriod.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                         | Instance Count | Instance Link                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [ISortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                     |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L2) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                              | Instance Count | Instance Link                                                                                                               |
| :----------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroDelegateTarget.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                | Instance Count | Instance Link                                                                                                        |
| :--------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroFactory.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L2) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                    | Instance Count | Instance Link                                                                                                          |
| :------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroReference.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L2) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                      |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L3) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                             |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L3) |
___
```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;
```

| File Link                                                                                                                                  | Instance Count | Instance Link                                                                                                         |
| :----------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol) |              1 | [2](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                              |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              1 | [3](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L3) |
___
</details>

#### <a id="g-08"></a> \[G-08\] `internal` functions not called by the contract should be removed to save deployment gas
##### Description:
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword.

##### Instances:
There are 15 instances of this issue.
<details><summary>View 15 Instances</summary>

```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

87:     function _syncGracePeriodForGivenValues(
88:         uint256 systemCollShares,
89:         uint256 systemDebt,
90:         uint256 price
91:     ) internal {

255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {

344:     function _syncAccounting(bytes32 _cdpId) internal {

419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

489:     function _computeTCRWithGivenSystemValues(
490:         uint256 _systemCollShares,
491:         uint256 _systemDebt,
492:         uint256 _price
493:     ) internal view returns (uint256) {

648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {

733:     function _getSyncedDebtAndCollShares(
734:         bytes32 _cdpId
735:     ) internal view returns (CdpDebtAndCollShares memory) {
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              7 | [87](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L87),[255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L255),[344](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L344),[419](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L419),[489](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L489),[648](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L648),[733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L733) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

55:     function _initializeAuthority(address newAuthority) internal {
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              1 | [55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L55) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

103:     function _requireUserAcceptsFee(
104:         uint256 _fee,
105:         uint256 _amount,
106:         uint256 _maxFeePercentage
107:     ) internal pure {

115:     function _convertDebtDenominationToBtc(
116:         uint256 _debt,
117:         uint256 _price
118:     ) internal pure returns (uint256) {

124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {
```

| File Link                                                                                                                     | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol) |              5 | [60](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L60),[95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L95),[103](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L103),[115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L115),[124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L124) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

306:     function _requireCallerIsBorrowerOperations() internal view {

323:     function _requireCallerIsCdpM() internal view {
```

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              2 | [306](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L306),[323](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L323) |
___
</details>

#### <a id="g-09"></a> \[G-09\] `internal`/`private` functions only called once can be inlined to save gas
##### Description:
The two extra `JUMP` instructions and additional stack operations needed for function calls costs 20 to 40 gas.

##### Recommendation:
For `internal` or `private` functions used just once, move the function logic to the calling function.

##### Instances:
There are 77 instances of this issue.
<details><summary>View 77 Instances</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

219:     function _requireCallerIsBorrowerOperations() internal view {

235:     function _requireCallerIsCdpManager() internal view {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              2 | [219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L219),[235](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L235) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

744:     function _getCollSharesChangeFromStEthChange(
745:         uint256 _collReceived,
746:         uint256 _requestedCollWithdrawal
747:     ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

760:     function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

803:     function _requireSingularCollChange(
804:         uint256 _stEthBalanceIncrease,
805:         uint256 _stEthBalanceDecrease
806:     ) internal pure {

813:     function _requireNonZeroAdjustment(
814:         uint256 _stEthBalanceIncrease,
815:         uint256 _debtChange,
816:         uint256 _stEthBalanceDecrease
817:     ) internal pure {

829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {

838:     function _requireNotInRecoveryMode(uint256 _tcr) internal view {

845:     function _requireNoStEthBalanceDecrease(uint256 _stEthBalanceDecrease) internal pure {

852:     function _requireValidAdjustmentInCurrentMode(
853:         bool _isRecoveryMode,
854:         uint256 _stEthBalanceDecrease,
855:         bool _isDebtIncrease,
856:         AdjustCdpLocals memory _vars
857:     ) internal {

921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

946:     function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

986:     function _getNewNominalICRFromCdpChange(
987:         AdjustCdpLocals memory vars,
988:         bool _isDebtIncrease
989:     ) internal pure returns (uint256) {

1004:     function _getNewICRFromCdpChange(
1005:         uint256 _collShares,
1006:         uint256 _debt,
1007:         uint256 _collSharesChange,
1008:         bool _isCollIncrease,
1009:         uint256 _debtChange,
1010:         bool _isDebtIncrease,
1011:         uint256 _price
1012:     ) internal view returns (uint256) {
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |             13 | [744](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744),[760](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L760),[803](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L803),[813](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L813),[829](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L829),[834](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L834),[838](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L838),[845](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L845),[852](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L852),[921](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L921),[946](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L946),[986](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L986),[1004](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1004) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

135:     function _redeemCollateralFromCdp(
136:         SingleRedemptionInputs memory _redeemColFromCdp
137:     ) internal returns (SingleRedemptionValues memory singleRedemption) {

244:     function _closeCdpByRedemption(
245:         bytes32 _cdpId,
246:         uint256 _EBTC,
247:         uint256 _collSurplus,
248:         uint256 _liquidatorRewardShares,
249:         address _borrower
250:     ) internal {

272:     function _isValidFirstRedemptionHint(
273:         bytes32 _firstRedemptionHint,
274:         uint256 _price
275:     ) internal view returns (bool) {

489:     function _getCdpIdsToRemove(
490:         bytes32 _start,
491:         uint256 _total,
492:         bytes32 _end
493:     ) internal view returns (bytes32[] memory) {

550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

595:     function _checkPotentialRecoveryMode(
596:         uint256 _systemCollShares,
597:         uint256 _systemDebt,
598:         uint256 _price
599:     ) internal view returns (bool) {

612:     function _updateBaseRateFromRedemption(
613:         uint256 _ETHDrawn,
614:         uint256 _price,
615:         uint256 _totalEBTCSupply
616:     ) internal returns (uint256) {

655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {

737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(
738:         address _redeemer,
739:         uint256 _amount,
740:         uint256 _totalSupply
741:     ) internal view {

753:     function _requireAmountGreaterThanZero(uint256 _amount) internal pure {

757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

761:     function _requireValidMaxFeePercentage(uint256 _maxFeePercentage) internal view {

977:     function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {

984:     function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |             14 | [135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135),[244](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L244),[272](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L272),[489](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L489),[550](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L550),[595](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L595),[612](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L612),[655](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L655),[737](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L737),[753](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L753),[757](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L757),[761](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L761),[977](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L977),[984](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L984) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

73:     function _syncGracePeriod() internal {

260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

410:     function _removeStake(bytes32 _cdpId) internal {

431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {

539:     function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {

574:     function _takeSplitAndUpdateFeePerUnit(
575:         uint256 _feeTaken,
576:         uint256 _newPerUnit,
577:         uint256 _newErrorPerUnit
578:     ) internal {

592:     function _applyAccumulatedFeeSplit(
593:         bytes32 _cdpId,
594:         uint256 _newColl,
595:         uint256 _feeSplitDistributed,
596:         uint256 _oldPerUnitCdp,
597:         uint256 _systemStEthFeePerUnitIndex
598:     ) internal {

652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {

895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |             14 | [73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L73),[260](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260),[293](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L293),[327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L327),[336](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L336),[410](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L410),[431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L431),[441](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L441),[463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L463),[539](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L539),[574](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L574),[592](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L592),[652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L652),[895](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L895) |
___
```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

112:     function _requireCallerIsBorrowerOperations() internal view {

119:     function _requireCallerIsCdpManager() internal view {

123:     function _requireCallerIsActivePool() internal view {
```

| File Link                                                                                                                      | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              3 | [112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112),[119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L119),[123](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L123) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {
```

| File Link                                                                                                             | Instance Count | Instance Link                                                                                                       |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              1 | [32](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L32) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              1 | [30](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

83:     function _getTCRWithSystemDebtAndCollShares(
84:         uint256 _price
85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {
```

| File Link                                                                                                                     | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol) |              5 | [75](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L75),[79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L79),[83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L83),[134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L134),[140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L140) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

262:     function _mint(address account, uint256 amount) internal {
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                                 |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------ |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              1 | [262](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L262) |
___
```solidity
File: packages/contracts/contracts/HintHelpers.sol

133:     function _calculateCdpStateAfterPartialRedemption(
134:         LocalVariables_getRedemptionHints memory vars,
135:         uint256 currentCdpDebt,
136:         uint256 _price
137:     ) internal view returns (uint256, uint256) {
```

| File Link                                                                                                              | Instance Count | Instance Link                                                                                                   |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------- |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              1 | [133](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L133) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

398:     function _doSwap(SwapOperation memory swapData) internal {

435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

450:     function _ensureNotSystem(address addy) internal {

460:     function _openCdpCallback(bytes memory data) internal {

474:     function _closeCdpCallback(bytes memory data) internal {

482:     function _adjustCdpCallback(bytes memory data) internal {

498:     function excessivelySafeCall(
499:         address _target,
500:         uint256 _gas,
501:         uint256 _value,
502:         uint16 _maxCopy,
503:         bytes memory _calldata
504:     ) internal returns (bool, bytes memory) {
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              7 | [398](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L398),[435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L435),[450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L450),[460](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L460),[474](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L474),[482](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L482),[498](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L498) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

135:     function _liquidateIndividualCdpSetupCDP(
136:         LiquidationLocals memory _liqState,
137:         LiquidationRecoveryModeLocals memory _recoveryState
138:     ) internal {

397:     function _liquidateCDPPartially(
398:         LiquidationLocals memory _partialState
399:     ) private returns (uint256, uint256) {

450:     function _partiallyReduceCdpDebt(
451:         bytes32 _cdpId,
452:         uint256 _partialDebt,
453:         uint256 _partialColl
454:     ) internal {

466:     function _reInsertPartialLiquidation(
467:         LiquidationLocals memory _partialState,
468:         uint256 _newNICR,
469:         uint256 _oldDebt,
470:         uint256 _oldColl
471:     ) internal {

544:     function _calculatePartialLiquidationSurplusAndCap(
545:         uint256 _ICR,
546:         uint256 _price,
547:         uint256 _totalDebtToBurn,
548:         uint256 _totalColToSend
549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

642:     function _getLiquidationValuesRecoveryMode(
643:         uint256 _price,
644:         uint256 _systemDebt,
645:         uint256 _systemCollShares,
646:         LocalVariables_LiquidationSequence memory vars,
647:         LiquidationValues memory singleLiquidation
648:     ) internal {

733:     function _getTotalFromBatchLiquidate_RecoveryMode(
734:         uint256 _price,
735:         uint256 _systemCollShares,
736:         uint256 _systemDebt,
737:         bytes32[] memory _cdpArray
738:     ) internal returns (LiquidationTotals memory totals) {

807:     function _getTotalsFromBatchLiquidate_NormalMode(
808:         uint256 _price,
809:         uint256 _TCR,
810:         bytes32[] memory _cdpArray
811:     ) internal returns (LiquidationTotals memory totals) {

862:     function _redistributeDebt(uint256 _debt) internal {

896:     function _requirePartialLiqDebtSize(
897:         uint256 _partialDebt,
898:         uint256 _entireDebt,
899:         uint256 _price
900:     ) internal view {

908:     function _requirePartialLiqCollSize(uint256 _entireColl) internal pure {
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |             11 | [135](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L135),[397](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L397),[450](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450),[466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L466),[544](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L544),[642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L642),[733](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L733),[807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L807),[862](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L862),[896](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L896),[908](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L908) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

582:     function _getCurrentFallbackResponse()
583:         internal
584:         view
585:         returns (FallbackResponse memory fallbackResponse)
586:     {
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                                 |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------ |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [582](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L582) |
___
```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

134:     function _executeOne(Operation calldata op) internal {

174:     function _fallback() internal {
```

| File Link                                                                                                                                  | Instance Count | Instance Links                                                                                                                                                                                                                                      |
| :----------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol) |              2 | [134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L134),[174](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L174) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              1 | [642](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L642) |
___
</details>

#### <a id="g-10"></a> \[G-10\] `keccak256()` should only need to be called on a specific string literal once
##### Description:
The result of the call to `keccak256()` should be saved to an immutable variable, and that variable used instead. If the hash is being used as a part of a function selector, the cast to `bytes4` should also only be done once.

##### Recommendation:
To reduce gas cost and redundancy, `keccak256()` should only be called on a specific string literal once.

##### Instances:
There are 4 instances of this issue.
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

/// @audit also at packages/contracts/contracts/EBTCToken.sol:72
129:         bytes32 hashedVersion = keccak256(bytes(_VERSION));
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [129](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L129) |
___
```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

/// @audit also at packages/contracts/contracts/LeverageMacroBase.sol:37
11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                     |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------------------- |
| [ERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol) |              1 | [11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

/// @audit also at packages/contracts/contracts/BorrowerOperations.sol:129
72:         bytes32 hashedVersion = keccak256(bytes(_VERSION));
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              1 | [72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L72) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

/// @audit also at packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol:11
37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                       |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              1 | [37](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37) |
___
#### <a id="g-11"></a> \[G-11\] Multiplication by powers of two should use bit shifting

Note: This issue was listed in the automated findings output; however, additional instances of the issue are listed here.

##### Description:
When multiplying a number by two and powers of two, use shift left instead of multiplication. Shifting left by `N` is the same as multiplying by `2^N`. Examples:<br/>`uint256 b = a * 2;` --> `uint256 b = a << 1;`<br/>`uint256 c = a * 4;` --> `uint256 c = a << 2;`<br/>Using shift left instead of multiplication will [save 112 gas](https://gist.github.com/ezcodeslide/64e22541a154bebd8b2cbcd4128a9c1c).

##### Instances:
There is 1 instance of this issue.
```solidity
File: packages/contracts/contracts/PriceFeed.sol

804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                                 |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------ |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [804](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L804) |
___
#### <a id="g-12"></a> \[G-12\] Nesting `if`-statements is cheaper than using `&&`
##### Description:
Nesting `if`-statements avoids the stack operations of setting up and using an extra `jumpdest`, and saves 6 gas.

##### Instances:
There are 14 instances of this issue.
<details><summary>View 14 Instances</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {
394:             _requireValidDebtRepayment(vars.debt, vars.netDebtChange);
395:             _requireSufficientEbtcTokenBalance(msg.sender, vars.netDebtChange);
396:             _requireNonZeroDebt(vars.debt - vars.netDebtChange);
397:         }
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                              |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              2 | [512](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512),[796](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L796) |
___
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
758:
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
772:
773:                     // Update aggregate trackers
774:                     vars.entireSystemDebt = vars.entireSystemDebt - singleLiquidation.debtToBurn;
775:                     vars.entireSystemColl =
776:                         vars.entireSystemColl -
777:                         singleLiquidation.totalCollToSendToLiquidator -
778:                         singleLiquidation.collSurplus;
779:
780:                     // Add liquidation values to their respective running totals
781:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
782:
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
793:
794:                     // Add liquidation values to their respective running totals
795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
796:                     _liqFlags[vars.i] = true;
797:                 }
798:                 // In Normal Mode skip cdps with ICR >= MCR
799:             }

790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {
791:                     _syncAccounting(vars.cdpId);
792:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);
793:
794:                     // Add liquidation values to their respective running totals
795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
796:                     _liqFlags[vars.i] = true;
797:                 }

819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
820:                 vars.ICR = getSyncedICR(vars.cdpId, _price);
821:
822:                 if (_checkICRAgainstMCR(vars.ICR)) {
823:                     _syncAccounting(vars.cdpId);
824:                     _getLiquidationValuesNormalMode(_price, _TCR, vars, singleLiquidation);
825:
826:                     // Add liquidation values to their respective running totals
827:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);
828:                 }
829:             }
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              4 | [157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L157),[756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756),[790](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L790),[819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819) |
___
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

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              2 | [226](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226),[372](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L372) |
___
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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              5 | [202](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202),[259](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L259),[330](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L330),[621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L621),[644](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L644) |
___
</details>

#### <a id="g-13"></a> \[G-13\] Optimize names to save gas
##### Description:
`public` and `external` function names and `public` member variable names can be optimized to save gas. The contracts listed below can be optimized so that the most frequently called functions use the least amount of gas possible during the Method ID lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment. Renaming functions to have lower Method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92).

##### Recommendation:
Use a tool like [Solidity Optimize Name](https://emn178.github.io/solidity-optimize-name/) to find names that will generate Method IDs that will prioritize the most used functions.

##### Instances:
There are 26 instances of this issue.
<details><summary>View 26 Instances</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

/// @audit sweepToken(), setFeeRecipientAddress(), setFeeBps(), setFlashLoansPaused()
22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              1 | [22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L22) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

/// @audit DOMAIN_SEPARATOR(), setFeeRecipientAddress(), setFeeBps(), setFlashLoansPaused()
21: contract BorrowerOperations is
22:     EbtcBase,
23:     ReentrancyGuard,
24:     IBorrowerOperations,
25:     ERC3156FlashLender,
26:     AuthNoOwner,
27:     PermitNonce
28: {
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                        |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [21](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L21) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

/// @audit getSystemDebt(), getDeploymentStartTime(), checkPotentialRecoveryMode(), setStakingRewardSplit(), setRedemptionFeeFloor(), setMinuteDecayFactor(), setBeta(), setRedemptionsPaused(), initializeCdp(), updateCdp()
16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [16](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L16) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

/// @audit notifyStartGracePeriod(), notifyEndGracePeriod(), setGracePeriod(), syncGlobalAccounting(), syncGlobalAccountingAndGracePeriod(), calcFeeUponStakingReward(), getAccumulatedFeeSplitApplied(), getCachedNominalICR(), getSyncedNominalICR(), getCachedICR(), getPendingRedistributedDebt(), hasPendingRedistributedDebt(), getSyncedDebtAndCollShares(), getSyncedCdpDebt(), getSyncedCdpCollShares(), getSyncedICR(), getSyncedTCR(), canLiquidateRecoveryMode()
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                       |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              1 | [19](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L19) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

/// @audit authority(), authorityInitialized(), setAuthority()
10: contract AuthNoOwner {
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              1 | [10](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10) |
___
```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

/// @audit doesUserHaveRole(), doesRoleHaveCapability(), isPublicCapability(), setPublicCapability(), setRoleCapability(), burnCapability(), setUserRole()
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                                 |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------- |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              1 | [12](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L12) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

/// @audit burn(), DOMAIN_SEPARATOR()
26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              1 | [26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L26) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

/// @audit getUsersByRole(), getRolesForUser(), getRolesFromByteMap(), getByteMapFromRoles(), getEnabledFunctionsInTarget(), getRoleName(), setRoleName()
13: contract Governor is RolesAuthority {
```

| File Link                                                                                                        | Instance Count | Instance Link                                                                                              |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              1 | [13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L13) |
___
```solidity
File: packages/contracts/contracts/HintHelpers.sol

/// @audit getRedemptionHints(), getApproxHint(), computeNominalCR(), computeCR()
11: contract HintHelpers is EbtcBase {
```

| File Link                                                                                                              | Instance Count | Instance Link                                                                                                 |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------ |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              1 | [11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L11) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

/// @audit transferSystemCollShares(), increaseSystemCollShares(), transferSystemCollSharesAndLiquidatorReward(), allocateSystemCollSharesToFeeRecipient(), claimFeeRecipientCollShares(), feeRecipientAddress(), getFeeRecipientClaimableCollShares(), setFeeRecipientAddress()
7: interface IActivePool is IPool {
```

| File Link                                                                                                                         | Instance Count | Instance Link                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [IActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol) |              1 | [7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L7) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

/// @audit openCdp(), openCdpFor(), addColl(), withdrawColl(), withdrawDebt(), repayDebt(), closeCdp(), adjustCdp(), adjustCdpWithColl(), claimSurplusCollShares(), feeRecipientAddress()
7: interface IBorrowerOperations is IPositionManagers {
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :----------------------------------------------------------------------------------------------------------------------------- |
| [IBorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol) |              1 | [7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

/// @audit getActiveCdpsCount(), getIdFromCdpIdsArray(), liquidate(), partiallyLiquidate(), batchLiquidateCdps(), redeemCollateral(), updateStakeAndTotalStakes(), syncAccounting(), closeCdp(), getRedemptionRate(), getRedemptionRateWithDecay(), getRedemptionFeeWithDecay(), getCdpStatus(), getCdpStake(), getCdpDebt(), getCdpCollShares(), getCdpLiquidatorRewardShares(), initializeCdp(), updateCdp(), getCachedTCR(), checkRecoveryMode()
9: interface ICdpManager is IEbtcBase, ICdpManagerData {
```

| File Link                                                                                                                         | Instance Count | Instance Link                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [ICdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol) |              1 | [9](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManager.sol#L9) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

/// @audit totalStakes(), ebtcToken(), systemStEthFeePerUnitIndex(), systemStEthFeePerUnitIndexError(), stEthIndex(), calcFeeUponStakingReward(), syncGlobalAccounting(), syncGlobalAccountingAndGracePeriod(), getAccumulatedFeeSplitApplied(), getCachedNominalICR(), getCachedICR(), getSyncedCdpDebt(), getSyncedCdpCollShares(), getSyncedICR(), getSyncedTCR(), getSyncedNominalICR(), getPendingRedistributedDebt(), hasPendingRedistributedDebt(), getSyncedDebtAndCollShares(), canLiquidateRecoveryMode()
13: interface ICdpManagerData is IRecoveryModeGracePeriod {
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                                |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------------- |
| [ICdpManagerData.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol) |              1 | [13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

/// @audit getTotalSurplusCollShares(), getSurplusCollShares(), increaseSurplusCollShares(), claimSurplusCollShares(), increaseTotalSurplusCollShares()
5: interface ICollSurplusPool {
```

| File Link                                                                                                                                   | Instance Count | Instance Link                                                                                                               |
| :------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------------- |
| [ICollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol) |              1 | [5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

/// @audit mint(), burn()
8: interface IEBTCToken is IERC20, IERC2612 {
```

| File Link                                                                                                                       | Instance Count | Instance Link                                                                                                         |
| :------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [IEBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol) |              1 | [8](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

/// @audit maxFlashLoan(), flashFee(), flashLoan()
7: interface IERC3156FlashLender {
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :----------------------------------------------------------------------------------------------------------------------------- |
| [IERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol) |              1 | [7](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

/// @audit getFallbackResponse(), fallbackTimeout(), setFallbackTimeout()
5: interface IFallbackCaller {
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [IFallbackCaller.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol) |              1 | [5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

/// @audit increasePermitNonce(), nonces()
5: interface IPermitNonce {
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                           |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [IPermitNonce.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol) |              1 | [5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

/// @audit getSystemCollShares(), getSystemDebt(), increaseSystemDebt(), decreaseSystemDebt()
6: interface IPool {
```

| File Link                                                                                                             | Instance Count | Instance Link                                                                                                    |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------- |
| [IPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol) |              1 | [6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPool.sol#L6) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

/// @audit getPositionManagerApproval(), setPositionManagerApproval(), revokePositionManagerApproval(), renouncePositionManagerApproval(), permitPositionManagerApproval(), version(), permitTypeHash(), domainSeparator()
5: interface IPositionManagers {
```

| File Link                                                                                                                                     | Instance Count | Instance Link                                                                                                                |
| :-------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------------- |
| [IPositionManagers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol) |              1 | [5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5) |
___
```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

/// @audit notifyStartGracePeriod(), notifyEndGracePeriod()
5: interface IRecoveryModeGracePeriod {
```

| File Link                                                                                                                                                   | Instance Count | Instance Link                                                                                                                       |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------- |
| [IRecoveryModeGracePeriod.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol) |              1 | [5](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5) |
___
```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

/// @audit remove(), batchRemove(), reInsert(), contains(), isFull(), isEmpty(), getSize(), getMaxSize(), getFirst(), getLast(), getNext(), getPrev(), validInsertPosition(), findInsertPosition(), insert(), getOwnerAddress(), nonExistId(), cdpCountOf(), getCdpCountOf(), getCdpsOf(), getAllCdpsOf(), cdpOfOwnerByIndex(), cdpOfOwnerByIdx()
6: interface ISortedCdps {
```

| File Link                                                                                                                         | Instance Count | Instance Link                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [ISortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol) |              1 | [6](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

/// @audit owner(), doOperation(), sweepToCaller(), sweepToken(), decodeFLData(), onFlashLoan()
26: contract LeverageMacroBase {
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                       |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              1 | [26](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L26) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

/// @audit deployNewMacro(), deployNewMacro()
11: contract LeverageMacroFactory {
```

| File Link                                                                                                                                | Instance Count | Instance Link                                                                                                          |
| :--------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroFactory.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol) |              1 | [11](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L11) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

/// @audit liquidate(), partiallyLiquidate(), batchLiquidateCdps()
13: contract LiquidationLibrary is CdpManagerStorage {
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                        |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              1 | [13](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L13) |
___
```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

/// @audit setFallbackHandler(), setAllowAnyCall(), enableCallbackForCall(), execute()
25: contract SimplifiedDiamondLike {
```

| File Link                                                                                                                                  | Instance Count | Instance Link                                                                                                           |
| :----------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol) |              1 | [25](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25) |
___
</details>

#### <a id="g-14"></a> \[G-14\] Remove unused local variable

##### Instances:
There are 4 instances of this issue.
```solidity
File: packages/contracts/contracts/CdpManager.sol

922:         uint256 index = _addCdpIdToArray(_cdpId);
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L922) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

357:             uint _pendingDebt,

687:         (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                              |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              2 | [357](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L357),[687](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L687) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

465:         bytes32 _cdpId = borrowerOperations.openCdp(
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                         |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |              1 | [465](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L465) |
___
#### <a id="g-15"></a> \[G-15\] `require()`/`revert()` strings longer than 32 bytes cost extra gas

Note: This issue was listed in the automated findings output; however, additional instances of the issue are listed here.

##### Description:
Shortening revert strings to fit in 32 bytes will decrease deploy-time gas and will decrease runtime gas when the revert condition has been met. Revert strings that are longer than 32 bytes require at least one additional `mstore` (3 gas), along with additional overhead for computing memory offset, etc. (When using Solidity 0.8.4 or later, it is recommended to use custom errors instead.)

##### Instances:
There are 115 instances of this issue.
<details><summary>View 115 Instances</summary>

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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |             12 | [137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137),[162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162),[220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220),[228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228),[236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236),[277](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277),[302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302),[350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350),[374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374),[377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377),[393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393),[407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407) |
___
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

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |             26 | [145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145),[146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146),[368](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368),[463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463),[541](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541),[715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715),[734](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734),[807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807),[818](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818),[826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826),[831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831),[835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835),[839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839),[846](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846),[911](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911),[918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918),[922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922),[929](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929),[936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936),[940](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940),[947](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947),[957](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957),[970](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970),[1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116),[1141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141),[1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155) |
___
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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |             15 | [431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431),[502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502),[503](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503),[626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626),[672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672),[743](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743),[747](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747),[754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754),[758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758),[762](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762),[774](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774),[789](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789),[793](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793),[808](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808),[812](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |             11 | [112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112),[242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242),[243](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243),[261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261),[453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453),[466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466),[475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475),[556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556),[649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649),[653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653),[660](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660) |
___
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

| File Link                                                                                                                      | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              6 | [92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92),[113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113),[120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120),[124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124),[143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143),[146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

57:         require(!_authorityInitialized, "Auth: authority already initialized");
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              1 | [57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L57) |
___
```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");
```

| File Link                                                                                                                                   | Instance Count | Instance Link                                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :----------------------------------------------------------------------------------------------------------------------------- |
| [ReentrancyGuard.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol) |              1 | [14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14) |
___
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

| File Link                                                                                                                                 | Instance Count | Instance Links                                                                                                                                                                                                                                                |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              2 | [90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90),[134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134) |
___
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

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |             10 | [144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144),[165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165),[251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251),[263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263),[271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271),[274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274),[296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296),[300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300),[307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307),[315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |             10 | [179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179),[191](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191),[201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201),[249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249),[251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251),[253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253),[352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352),[356](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356),[362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362),[440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440) |
___
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

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              9 | [56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56),[82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82),[89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89),[93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93),[477](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477),[680](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680),[710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710),[901](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901),[909](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79) |
___
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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |             11 | [352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352),[367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367),[371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371),[422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422),[427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427),[433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433),[458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458),[506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506),[508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508),[715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715),[720](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720) |
___
</details>

#### <a id="g-16"></a> \[G-16\] Splitting `require()` statements that use `&&` saves gas
##### Description:
Instead of using the `&&` operator in a single `require` statement to check multiple conditions, using multiple `require` statements with 1 condition per `require` statement [will save 3 GAS](https://github.com/code-423n4/2022-01-xdefi-findings/issues/128) per `&&`.

##### Instances:
There are 8 instances of this issue.
<details><summary>View 8 Instances</summary>

```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

734:         require(
735:             recoveredAddress != address(0) && recoveredAddress == _borrower,
736:             "BorrowerOperations: Invalid signature"
737:         );
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [734](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

762:         require(
763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764:             "Max fee percentage must be between redemption fee floor and 100%"
765:         );
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [762](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                    |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              3 | [261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261),[466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466),[653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653) |
___
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

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              2 | [296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296),[300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79) |
___
</details>

#### <a id="g-17"></a> \[G-17\] State variable read in a loop
##### Description:
State variables should be cached in a local variable rather than reading it them every iteration of the `for`-loop, which will replace each `Gwarmaccess` (100 gas) with a much cheaper stack read.

##### Instances:
There are 31 instances of this issue.
<details><summary>View 31 Instances</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

/// @audit MCR
369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

/// @audit sortedCdps
370:                 _cId = sortedCdps.getPrev(_cId);

/// @audit sortedCdps
371:                 currentBorrower = sortedCdps.getOwnerAddress(_cId);

/// @audit sortedCdps
500:             _id = sortedCdps.getNext(_id);
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              4 | [369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L369),[370](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L370),[371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L371),[500](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L500) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

/// @audit users
46:         for (uint256 i = 0; i < users.length(); i++) {
```

| File Link                                                                                                        | Instance Count | Instance Link                                                                                              |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              1 | [46](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46) |
___
```solidity
File: packages/contracts/contracts/HintHelpers.sol

/// @audit cdpManager, MCR
70:                 cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR

/// @audit sortedCdps
72:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

/// @audit sortedCdps
73:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

/// @audit MIN_NET_STETH_BALANCE
101:                     if (
102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <
103:                         MIN_NET_STETH_BALANCE
104:                     ) {

/// @audit MIN_NET_STETH_BALANCE, collateral
102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <
103:                         MIN_NET_STETH_BALANCE

/// @audit sortedCdps
116:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

/// @audit sortedCdps
117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);
```

| File Link                                                                                                              | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              7 | [70](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L70),[72](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L72),[73](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L73),[101](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L101),[102](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L102),[116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L116),[117](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L117) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

/// @audit Cdps
756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

/// @audit Cdps
756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

/// @audit CCR
788:                     vars.backToNormalMode = _TCR < CCR ? false : true;

/// @audit CCR
788:                     vars.backToNormalMode = _TCR < CCR ? false : true;

/// @audit CCR
788:                     vars.backToNormalMode = _TCR < CCR ? false : true;

/// @audit Cdps
819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

/// @audit Cdps
819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              7 | [756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756),[756](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L756),[788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788),[788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788),[788](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L788),[819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819),[819](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L819) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

/// @audit dummyId
185:         while (_currentCdpId != dummyId) {

/// @audit data
199:             _currentCdpId = data.nodes[_currentCdpId].prevId;

/// @audit dummyId
248:         while (_currentCdpId != dummyId) {

/// @audit data
256:             _currentCdpId = data.nodes[_currentCdpId].prevId;

/// @audit dummyId
318:         while (_currentCdpId != dummyId) {

/// @audit data
327:             _currentCdpId = data.nodes[_currentCdpId].prevId;

/// @audit dummyId
629:         while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {

/// @audit data
630:             prevId = data.nodes[prevId].nextId;

/// @audit data
631:             nextId = data.nodes[prevId].nextId;

/// @audit dummyId
652:         while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {

/// @audit data
653:             nextId = data.nodes[nextId].prevId;

/// @audit data
654:             prevId = data.nodes[nextId].prevId;
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |             12 | [185](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L185),[199](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L199),[248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L248),[256](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L256),[318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L318),[327](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L327),[629](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L629),[630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L630),[631](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L631),[652](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L652),[653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L653),[654](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L654) |
___
</details>

#### <a id="g-18"></a> \[G-18\] The result of function calls should be cached rather than re-calling the function
##### Description:
The instances below point to the second+ call of the function within a single function.

##### Instances:
There is 1 instance of this issue.
```solidity
File: packages/contracts/contracts/CdpManager.sol

/// @audit sortedCdps.nonExistId() on line 277
285:         return nextCdp == sortedCdps.nonExistId() || getSyncedICR(nextCdp, _price) < MCR;
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [285](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L285) |
___
#### <a id="g-19"></a> \[G-19\] `unchecked {}` can be used on the division of two `uint`s in order to save gas
##### Description:
The division cannot overflow, since both the numerator and the denominator are non-negative. Using `unchecked {}` will save 20 gas per instance.

##### Instances:
There are 31 instances of this issue.
<details><summary>View 31 Instances</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

321:         return (amount * feeBps) / MAX_BPS;
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              1 | [321](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L321) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1118:         return (amount * feeBps) / MAX_BPS;
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                            |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [1118](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1118) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622:             _totalEBTCSupply;

624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

671:         uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

706:         return (baseRate * decayFactor) / DECIMAL_PRECISION;

712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              6 | [146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L146),[621](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621),[624](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L624),[671](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L671),[706](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L706),[712](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L712) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;

454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

558:         uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              6 | [316](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L316),[454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L454),[558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L558),[564](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L564),[567](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L567),[639](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L639) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

108:         uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;

119:         return (_debt * _price) / DECIMAL_PRECISION;
```

| File Link                                                                                                                     | Instance Count | Instance Links                                                                                                                                                                                                                                      |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol) |              2 | [108](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L108),[119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L119) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

94:             return (_collShares * NICR_PRECISION) / _debt;

110:             uint256 newCollRatio = (_stEthBalance * _price) / _debt;
```

| File Link                                                                                                                     | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                            |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol) |              3 | [38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38),[94](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L94),[110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L110) |
___
```solidity
File: packages/contracts/contracts/HintHelpers.sol

145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
```

| File Link                                                                                                              | Instance Count | Instance Link                                                                                                   |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------- |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              1 | [145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L145) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

558:             _incentiveColl = (_totalDebtToBurn * LICR) / _price;

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

592:             uint256 _debtToRepay = (_incentiveColl * _price) / LICR;

882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              8 | [278](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L278),[365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L365),[435](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L435),[555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555),[558](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L558),[579](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L579),[592](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L592),[882](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L882) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice

534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /
535:             minPrice;

801:             (_scaledDecimal *
802:                 uint256(_ethBtcAnswer) *
803:                 uint256(_stEthEthAnswer) *
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);
```

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                            |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              3 | [458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L458),[534](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L534),[801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L801) |
___
</details>

#### <a id="g-20"></a> \[G-20\] Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead
##### Description:
According to [the Solidity docs](https://docs.soliditylang.org/en/latest/internals/layout_in_storage.html), "When using elements that are smaller than 32 bytes, your contract's gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size." Each operation involving a `uint8` costs an extra 22-28 gas (depending on whether the other operand is also a variable of type `uint8`) as compared to ones involving `uint256`, due to the compiler having to clear the higher bits of the memory word before operating on the `uint8`, as well as the associated stack operations of doing so.

##### Recommendation:
Use `uint256`/`int256` for integers, then downcast (using [OpenZeppelin's SafeCast](https://docs.openzeppelin.com/contracts/3.x/api/utils#SafeCast)) where needed.

##### Instances:
There are 9 instances of this issue.
<details><summary>View 9 Instances</summary>

```solidity
File: packages/contracts/contracts/CdpManager.sol

/// @audit uint128 index
559:         index = uint128(CdpIds.length - 1);
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              1 | [559](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L559) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

/// @audit uint8[] rolesForUser
83:             rolesForUser = new uint8[](count);

/// @audit uint8[] rolesForUser
86:                     rolesForUser[j] = i;

/// @audit uint8[] roleIds
106:             roleIds = new uint8[](count);

/// @audit uint8[] roleIds
110:                     roleIds[j] = i;
```

| File Link                                                                                                        | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              4 | [83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L83),[86](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L86),[106](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L106),[110](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L110) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

/// @audit uint8 ethBtcDecimals
617:             ethBtcDecimals = decimals;

/// @audit uint8 stEthEthDecimals
625:             stEthEthDecimals = decimals;

/// @audit uint8 ethBtcDecimals
705:             ethBtcDecimals = decimals;

/// @audit uint8 stEthEthDecimals
713:             stEthEthDecimals = decimals;
```

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              4 | [617](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L617),[625](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L625),[705](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L705),[713](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L713) |
___
</details>

#### <a id="g-21"></a> \[G-21\] Use assembly for small keccak256 hashes, in order to save gas
##### Description:
If the arguments to the encode call can fit into the scratch space (two words or fewer), then it is more efficient to use assembly to generate the hash (80 gas).

##### Recommendation:
Use assembly as shown in the following example:
```solidity
// Before:
keccak256(abi.encodePacked(x, y));

// After
assembly {
  mstore(0x00, a);
  mstore(0x20, b);
  let hash := keccak256(0x00, 0x40);
}
```

##### Instances:
There is 1 instance of this issue.
```solidity
File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));
```

| File Link                                                                                                              | Instance Count | Instance Link                                                                                                   |
| :--------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------- |
| [HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol) |              1 | [182](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182) |
___
#### <a id="g-22"></a> \[G-22\] Use assembly to emit events, in order to save gas
##### Description:
Using the [scratch space](https://github.com/Vectorized/solady/blob/30558f5402f02351b96eeb6eaf32bcea29773841/src/tokens/ERC1155.sol#L501-L504) for event arguments (two words or fewer) will save gas over needing Solidity's full abi memory expansion used for emitting normally.

##### Instances:
There are 55 instances of this issue.
<details><summary>View 55 Instances</summary>

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

360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

421:         emit FlashLoansPaused(msg.sender, _paused);
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |             13 | [65](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L65),[112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L112),[113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L113),[145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L145),[146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L146),[173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L173),[174](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L174),[200](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L200),[213](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L213),[247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L247),[360](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L360),[399](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L399),[421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L421) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1171:         emit FlashLoansPaused(msg.sender, _paused);
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                           |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              3 | [136](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L136),[1149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1149),[1171](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1171) |
___
```solidity
File: packages/contracts/contracts/CdpManager.sol

55:         emit StakingRewardSplitSet(stakingRewardSplit);

630:         emit BaseRateUpdated(newBaseRate);

681:         emit BaseRateUpdated(decayedBaseRate);

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |              9 | [55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L55),[630](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L630),[681](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L681),[698](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L698),[782](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L782),[801](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L801),[824](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L824),[836](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L836),[848](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L848) |
___
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

50:         emit TCRNotified(_tcr);

64:         emit TCRNotified(_tcr);

119:         emit GracePeriodDurationSet(_gracePeriod);

300:         emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);

340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

414:         emit TotalStakesUpdated(_newTotalStakes);

425:         emit TotalStakesUpdated(_newTotalStakes);

481:         emit CdpArrayIndexUpdated(idToMove, index);
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              8 | [50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L50),[64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L64),[119](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L119),[300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L300),[340](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L340),[414](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L414),[425](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L425),[481](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L481) |
___
```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

83:         emit SurplusCollSharesUpdated(_account, newAmount);

95:         emit SurplusCollSharesUpdated(_account, 0);

104:         emit CollSharesTransferred(_account, claimableColl);
```

| File Link                                                                                                                      | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              3 | [83](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L83),[95](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L95),[104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L104) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

22:         emit OwnershipTransferred(msg.sender, _owner);

23:         emit AuthorityUpdated(msg.sender, _authority);

49:         emit AuthorityUpdated(msg.sender, newAuthority);

55:         emit OwnershipTransferred(msg.sender, newOwner);
```

| File Link                                                                                                             | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              4 | [22](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L22),[23](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L23),[49](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L49),[55](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L55) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));
```

| File Link                                                                                                                           | Instance Count | Instance Links                                                                                                                                                                                                                                        |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              2 | [50](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50),[62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62) |
___
```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

140:         emit CapabilityBurned(target, functionSig);
```

| File Link                                                                                                                                 | Instance Count | Instance Link                                                                                                                   |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------ |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              1 | [140](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L140) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

157:         emit RoleNameSet(role, roleName);
```

| File Link                                                                                                        | Instance Count | Instance Link                                                                                                |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              1 | [157](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L157) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

56:         emit DeployNewMacro(_owner, addy);
```

| File Link                                                                                                                                | Instance Count | Instance Link                                                                                                          |
| :--------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroFactory.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol) |              1 | [56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L56) |
___
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              1 | [891](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L891) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

548:         emit PriceFeedStatusChanged(_status);

555:         emit LastGoodPriceUpdated(_currentPrice);
```

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              6 | [67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L67),[378](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L378),[381](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L381),[387](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L387),[548](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L548),[555](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L555) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

405:         emit NodeAdded(_id, _NICR);

451:             emit NodeRemoved(_ids[i]);

490:         emit NodeRemoved(_id);
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                               |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              3 | [405](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L405),[451](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L451),[490](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L490) |
___
</details>

#### <a id="g-23"></a> \[G-23\] Use custom errors rather than `revert()`/`require()` strings to save gas

Note: This issue was listed in the automated findings output; however, additional instances of the issue are listed here.

##### Description:
Custom errors are available since Solidity 0.8.4. Custom errors save ~50 gas each time they are hit by [avoiding having to allocate and store the revert string](https://blog.soliditylang.org/2021/04/21/custom-errors/#errors-in-depth). Not defining the strings will also save deployment gas.

##### Instances:
There are 162 instances of this issue.
<details><summary>View 162 Instances</summary>

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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |             19 | [104](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104),[137](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L137),[162](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L162),[220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L220),[228](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L228),[236](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L236),[267](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L267),[269](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L269),[277](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L277),[294](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L294),[298](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L298),[302](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L302),[318](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L318),[319](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L319),[350](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L350),[374](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L374),[377](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L377),[393](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L393),[407](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L407) |
___
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

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |             30 | [145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145),[146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L146),[368](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L368),[463](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L463),[541](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L541),[715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L715),[734](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734),[807](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L807),[818](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L818),[826](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L826),[831](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L831),[835](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L835),[839](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L839),[846](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L846),[911](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L911),[918](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L918),[922](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L922),[929](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L929),[936](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L936),[940](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L940),[947](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L947),[957](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L957),[970](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L970),[1083](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1083),[1085](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1085),[1091](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1091),[1115](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1115),[1116](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1116),[1141](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1141),[1155](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1155) |
___
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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol) |             17 | [332](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L332),[431](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L431),[502](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502),[503](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L503),[626](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L626),[672](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L672),[678](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L678),[743](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L743),[747](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L747),[754](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L754),[758](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L758),[762](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762),[774](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L774),[789](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L789),[793](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L793),[808](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L808),[812](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L812) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |             12 | [112](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L112),[242](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L242),[243](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L243),[261](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261),[453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L453),[466](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L466),[475](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L475),[556](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L556),[584](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L584),[649](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L649),[653](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L653),[660](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L660) |
___
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

| File Link                                                                                                                      | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              7 | [92](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L92),[99](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L99),[113](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L113),[120](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L120),[124](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L124),[143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L143),[146](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L146) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

27:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

| File Link                                                                                                             | Instance Count | Instance Links                                                                                                                                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              2 | [27](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L27),[45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

17:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

57:         require(!_authorityInitialized, "Auth: authority already initialized");
```

| File Link                                                                                                                           | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              4 | [17](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17),[41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L41),[56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L56),[57](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L57) |
___
```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

109:         require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");
```

| File Link                                                                                                                     | Instance Count | Instance Link                                                                                                             |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------ |
| [EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol) |              1 | [109](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L109) |
___
```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");
```

| File Link                                                                                                                                   | Instance Count | Instance Link                                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :----------------------------------------------------------------------------------------------------------------------------- |
| [ReentrancyGuard.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol) |              1 | [14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14) |
___
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

| File Link                                                                                                                                 | Instance Count | Instance Links                                                                                                                                                                                                                                                |
| :---------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol) |              2 | [90](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90),[134](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134) |
___
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

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |             17 | [144](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144),[165](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L165),[208](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L208),[219](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L219),[247](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L247),[248](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L248),[251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L251),[263](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L263),[271](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L271),[274](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L274),[286](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L286),[287](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L287),[296](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296),[300](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L300),[307](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L307),[315](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L315),[324](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L324) |
___
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

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |             19 | [40](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L40),[45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45),[179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L179),[191](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L191),[201](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L201),[249](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L249),[251](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L251),[253](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L253),[255](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L255),[352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352),[356](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L356),[362](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L362),[421](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L421),[440](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L440),[452](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L452),[453](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L453),[454](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L454),[455](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L455),[456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456) |
___
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

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              9 | [56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56),[82](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L82),[89](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L89),[93](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93),[477](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L477),[680](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L680),[710](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L710),[901](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L901),[909](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L909) |
___
```solidity
File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );
```

| File Link                                                                                                          | Instance Count | Instance Link                                                                                               |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------- |
| [PriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol) |              1 | [79](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79) |
___
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
```

| File Link                                                                                                                                  | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol) |              8 | [52](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52),[56](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L56),[67](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67),[77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77),[111](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111),[154](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L154),[179](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L179),[187](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L187) |
___
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

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |             13 | [352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352),[365](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L365),[367](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L367),[369](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L369),[371](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L371),[422](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L422),[427](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L427),[433](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L433),[458](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L458),[506](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L506),[508](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L508),[715](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715),[720](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L720) |
___
</details>

#### <a id="g-24"></a> \[G-24\] Use predefined address instead of `address(this)`
##### Description:
Instead of using `address(this)`, it is more gas-efficient to pre-calculate and use the predefined address. Foundry's `script.sol` and Solmate's `LibRlp.sol` contracts can help pre-determine the address (see [computeCreateAddress](https://book.getfoundry.sh/reference/forge-std/compute-create-address)). The address can be passed in via a constructor argument and assigned to an immutable variable (rather than using a hardcoded constant) so that the code can remain the same across deployments on different networks.

##### Instances:
There are 27 instances of this issue.
<details><summary>View 27 Instances</summary>

```solidity
File: packages/contracts/contracts/ActivePool.sol

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

299:             collateral.sharesOf(address(this)) >= systemCollShares,

337:         return collateral.balanceOf(address(this));

376:         uint256 balance = IERC20(token).balanceOf(address(this));
```

| File Link                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ActivePool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol) |              5 | [283](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283),[295](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L295),[299](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L299),[337](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L337),[376](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L376) |
___
```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

682:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

| File Link                                                                                                                            | Instance Count | Instance Link                                                                                                          |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------------------- |
| [BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol) |              1 | [682](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682) |
___
```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

145:         uint256 balance = IERC20(token).balanceOf(address(this));
```

| File Link                                                                                                                      | Instance Count | Instance Link                                                                                                       |
| :----------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------ |
| [CollSurplusPool.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol) |              1 | [145](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L145) |
___
```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

38:             (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

| File Link                                                                                                             | Instance Count | Instance Links                                                                                                                                                                                                                          |
| :-------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Auth.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol) |              2 | [38](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38),[45](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));
```

| File Link                                                                                                                           | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                   |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              3 | [35](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35),[41](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L41),[62](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62) |
___
```solidity
File: packages/contracts/contracts/EBTCToken.sol

240:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

297:             _recipient != address(0) && _recipient != address(this),
```

| File Link                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol) |              2 | [240](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240),[297](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L297) |
___
```solidity
File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
```

| File Link                                                                                                        | Instance Count | Instance Link                                                                                              |
| :--------------------------------------------------------------------------------------------------------------- | -------------: | :--------------------------------------------------------------------------------------------------------- |
| [Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol) |              1 | [36](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

131:                 address(this),

143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));

149:                 IERC3156FlashBorrower(address(this)),

156:                 IERC3156FlashBorrower(address(this)),

173:             bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

220:         uint256 ebtcBal = ebtcToken.balanceOf(address(this));

221:         uint256 collateralBal = stETH.sharesOf(address(this));

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller
```

| File Link                                                                                                                          | Instance Count | Instance Links                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol) |             10 | [131](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131),[143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L143),[149](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L149),[156](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L156),[173](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L173),[220](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L220),[221](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L221),[352](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L352),[441](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L441),[456](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L456) |
___
```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

64:         address _owner = IOwnerLike(address(this)).owner();
```

| File Link                                                                                                                                              | Instance Count | Instance Link                                                                                                                 |
| :----------------------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------------- |
| [LeverageMacroDelegateTarget.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol) |              1 | [64](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64) |
___
```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag
```

| File Link                                                                                                                                  | Instance Count | Instance Link                                                                                                           |
| :----------------------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol) |              1 | [77](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77) |
___
</details>

#### <a id="g-25"></a> \[G-25\] Use `uint256(1)`/`uint256(2)` instead of `true`/`false` to save gas for changes
##### Description:
Using a `uint256` instead of a `bool` avoids a `Gsset` (20,000 gas) when changing from `false` to `true`, after having been `true` in the past.

##### Instances:
There are 3 instances of this issue.
```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

143:     bool public redemptionsPaused;
```

| File Link                                                                                                                          | Instance Count | Instance Link                                                                                                         |
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------- |
| [CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol) |              1 | [143](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L143) |
___
```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

14:     bool private _authorityInitialized;
```

| File Link                                                                                                                           | Instance Count | Instance Link                                                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------------------- |
| [AuthNoOwner.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol) |              1 | [14](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14) |
___
```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

15:     bool public flashLoansPaused;
```

| File Link                                                                                                                                         | Instance Count | Instance Link                                                                                                                     |
| :------------------------------------------------------------------------------------------------------------------------------------------------ | -------------: | :-------------------------------------------------------------------------------------------------------------------------------- |
| [ERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol) |              1 | [15](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15) |
___
#### <a id="g-26"></a> \[G-26\] Using `constant`s directly, rather than caching the value, saves gas
##### Description:
Avoid assigning `constant`s to a variable. Instead, use the constant directly.

##### Instances:
There is 1 instance of this issue.
```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

/// @audit DECIMAL_PRECISION
68:         uint256 y = DECIMAL_PRECISION;
```

| File Link                                                                                                                     | Instance Count | Instance Link                                                                                                           |
| :---------------------------------------------------------------------------------------------------------------------------- | -------------: | :---------------------------------------------------------------------------------------------------------------------- |
| [EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol) |              1 | [68](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcMath.sol#L68) |
___
#### <a id="g-27"></a> \[G-27\] Using `storage` instead of `memory` for structs/arrays saves gas
##### Description:
When fetching data from a storage location, assigning the data to a `memory` variable causes all fields of the struct/array to be read from storage, which incurs a `Gcoldsload` (2,100 gas) for each field of the struct/array. If the fields are read from the new memory variable, they incur an additional `MLOAD` rather than a cheap stack read. Instead of declaring the variable with the `memory` keyword, declaring the variable with the `storage` keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incurring the `Gcoldsload` for the fields actually read. The only time it makes sense to read the whole struct/array into a `memory` variable is if the full struct/array is being returned by the function, is being passed to a function that requires `memory`, or if the array/struct is being read from another `memory` array/struct.

##### Instances:
There are 3 instances of this issue.
```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

699:             totals = _getTotalFromBatchLiquidate_RecoveryMode(
700:                 vars.price,
701:                 systemColl,
702:                 systemDebt,
703:                 _cdpArray
704:             );

707:             totals = _getTotalsFromBatchLiquidate_NormalMode(vars.price, _TCR, _cdpArray);
```

| File Link                                                                                                                            | Instance Count | Instance Links                                                                                                                                                                                                                                |
| :----------------------------------------------------------------------------------------------------------------------------------- | -------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LiquidationLibrary.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol) |              2 | [699](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L699),[707](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L707) |
___
```solidity
File: packages/contracts/contracts/SortedCdps.sol

522:             Node memory _node = data.nodes[_id];
```

| File Link                                                                                                            | Instance Count | Instance Link                                                                                                  |
| :------------------------------------------------------------------------------------------------------------------- | -------------: | :------------------------------------------------------------------------------------------------------------- |
| [SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol) |              1 | [522](https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L522) |
___
