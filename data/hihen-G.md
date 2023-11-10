# Gas Report

## Summary

Total **722 instances** over **46 issues**with **358776** gas saved:

|ID|Issue|Instances|Gas|
|:--:|:---|:--:|:--:|
| [[G&#x2011;01]](#g01-use-storage-instead-of-memory-for-structsarrays) | Use `storage` instead of `memory` for structs/arrays | 1 | 4200 |
| [[G&#x2011;02]](#g02-constructors-can-be-marked-as-payable-to-save-deployment-gas) | Constructors can be marked as payable to save deployment gas | 19 | 399 |
| [[G&#x2011;03]](#g03-state-variables-only-set-in-their-definitions-should-be-declared-constant) | State variables only set in their definitions should be declared `constant` | 12 | 25164 |
| [[G&#x2011;04]](#g04-splitting-require-statements-that-use-) | Splitting `require()` statements that use `&&` | 8 | 24 |
| [[G&#x2011;05]](#g05-unnecessary-event-parameters-should-be-removed) | Unnecessary event parameters should be removed | 3 | 1074 |
| [[G&#x2011;06]](#g06-unnecessary-ternary-operator) | Unnecessary ternary operator | 3 | 54 |
| [[G&#x2011;07]](#g07-use-unchecked-block-for-safe-subtractions) | Use `unchecked` block for safe subtractions | 19 | 1615 |
| [[G&#x2011;08]](#g08-comparing-booleans-to-true-or-false) | Comparing booleans to `true` or `false` | 1 | 9 |
| [[G&#x2011;09]](#g09-using-constants-directly-is-more-gas-efficient) | Using `constant`s directly is more gas efficient | 1 | - |
| [[G&#x2011;10]](#g10-do-not-cache-state-variables-that-are-used-only-once) | Do not cache state variables that are used only once | 4 | 12 |
| [[G&#x2011;11]](#g11-do-not-calculate-constants) | Do not calculate constants | 1 | - |
| [[G&#x2011;12]](#g12-use-of-emit-inside-a-loop) | Use of `emit` inside a loop | 1 | 375 |
| [[G&#x2011;13]](#g13-initializing-mutable-state-variables-with-default-value-wastes-gas) | Initializing mutable state variables with default value wastes gas | 1 | 2900 |
| [[G&#x2011;14]](#g14-use-local-variables-for-emitting) | Use local variables for emitting | 6 | 600 |
| [[G&#x2011;15]](#g15-contract-storage-can-use-fewer-slots-by-changing-the-order-of-state-variables) | Contract storage can use fewer slots by changing the order of state variables | 1 | 20000 |
| [[G&#x2011;16]](#g16-structs-can-use-fewer-slots-by-changing-the-order-of-fields) | Structs can use fewer slots by changing the order of fields | 4 | 100000 |
| [[G&#x2011;17]](#g17-internal-functions-only-called-once-can-be-inlined-to-save-gas) | `internal` functions only called once can be inlined to save gas | 13 | 390 |
| [[G&#x2011;18]](#g18-using-this-to-access-functions-results-in-an-external-call-wasting-gas) | Using `this` to access functions results in an external call, wasting gas | 1 | 100 |
| [[G&#x2011;19]](#g19-functions-that-revert-when-called-by-normal-users-can-be-marked-payable) | Functions that revert when called by normal users can be marked `payable` | 38 | 798 |
| [[G&#x2011;20]](#g20-use-x--x--y-instead-of-x--y-for-state-variables) | Use `x = x + y` instead of `x += y` for state variables | 1 | 10 |
| [[G&#x2011;21]](#g21-operator--costs-less-gas-than-operator-) | Operator `>=`/`<=` costs less gas than operator `>`/`<` | 126 | 378 |
| [[G&#x2011;22]](#g22-usage-of-intsuints-smaller-than-32-bytes-incurs-overhead) | Usage of `int`s/`uint`s smaller than 32 bytes incurs overhead | 64 | 3520 |
| [[G&#x2011;23]](#g23-using-a-double-if-statement-instead-of-a-logical-and) | Using a double `if` statement instead of a logical AND(`&&`) | 14 | 420 |
| [[G&#x2011;24]](#g24-divisions-can-be-unchecked-to-save-gas) | Divisions can be unchecked to save gas | 34 | 680 |
| [[G&#x2011;25]](#g25-increments-can-be-unchecked-to-save-gas) | Increments can be `unchecked` to save gas | 11 | 660 |
| [[G&#x2011;26]](#g26-remove-unused-local-variables) | Remove unused local variables | 6 | - |
| [[G&#x2011;27]](#g27-use-assembly-to-validate-msgsender) | Use assembly to validate `msg.sender` | 24 | 288 |
| [[G&#x2011;28]](#g28-use-x--y-instead-of-x--x--y-for-mapping-state-variables) | Use `x += y` instead of `x = x + y` for mapping state variables | 2 | 80 |
| [[G&#x2011;29]](#g29-avoid-zero-transfer-to-save-gas) | Avoid zero transfer to save gas | 2 | 200 |
| [[G&#x2011;30]](#g30-optimize-names-to-save-gas) | Optimize names to save gas | 33 | 726 |
| [[G&#x2011;31]](#g31-reduce-gas-usage-by-moving-to-solidity-0819-or-later) | Reduce gas usage by moving to Solidity 0.8.19 or later | 39 | - |
| [[G&#x2011;32]](#g32-newer-versions-of-solidity-are-more-gas-efficient) | Newer versions of solidity are more gas efficient | 39 | - |
| [[G&#x2011;33]](#g33-avoid-updating-storage-when-the-value-hasnt-changed) | Avoid updating storage when the value hasn't changed | 37 | 29600 |
| [[G&#x2011;34]](#g34-same-cast-is-done-multiple-times) | Same cast is done multiple times | 4 | - |
| [[G&#x2011;35]](#g35-require-or-revert-statements-that-check-input-arguments-should-be-at-the-top-of-the-function) | `require()` or `revert()` statements that check input arguments should be at the top of the function | 6 | - |
| [[G&#x2011;36]](#g36-contracts-can-use-fewer-storage-slots-by-truncating-state-variables) | Contracts can use fewer storage slots by truncating state variables | 1 | 80000 |
| [[G&#x2011;37]](#g37-structs-can-be-packed-into-fewer-storage-slots-by-truncating-fields) | Structs can be packed into fewer storage slots by truncating fields | 2 | 80000 |
| [[G&#x2011;38]](#g38-redundant-state-variable-getters) | Redundant state variable getters | 2 | - |
| [[G&#x2011;39]](#g39-refactor-duplicated-requirerevert-checks-to-save-gas) | Refactor duplicated `require()`/`revert()` checks to save gas | 4 | - |
| [[G&#x2011;40]](#g40-using-constants-instead-of-enum-can-save-gas) | Using `constant`s instead of `enum` can save gas | 9 | - |
| [[G&#x2011;41]](#g41-use-assembly-to-emit-events) | Use assembly to emit events | 71 | 2698 |
| [[G&#x2011;42]](#g42-use-assembly-to-compute-hashes-to-save-gas) | Use assembly to compute hashes to save gas | 1 | 80 |
| [[G&#x2011;43]](#g43-consider-activating-via-ir-for-deploying) | Consider activating via-ir for deploying | 1 | - |
| [[G&#x2011;44]](#g44-multiple-accesses-of-the-same-mappingarray-keyindex-should-be-cached) | Multiple accesses of the same mapping/array key/index should be cached | 36 | 1512 |
| [[G&#x2011;45]](#g45-multiple-mappings-can-be-replaced-with-a-single-struct-mapping) | Multiple mappings can be replaced with a single struct mapping | 5 | 210 |
| [[G&#x2011;46]](#g46-consider-using-bytes32-rather-than-a-string) | Consider using `bytes32` rather than a `string` | 11 | - |

## Gas Optimizations

### [G&#x2011;01] Use `storage` instead of `memory` for structs/arrays

When fetching data from a storage location, assigning the data to a `memory` variable causes all fields of the struct/array to be read from storage, which incurs a Gcoldsload (**2100 gas**) for *each* field of the struct/array. If the fields are read from the new memory variable, they incur an additional `MLOAD` rather than a cheap stack read. Instead of declaring the variable with the `memory` keyword, declaring the variable with the `storage` keyword and caching any fields that need to be re-read in stack variables, will be much cheaper, only incurring the Gcoldsload for the fields actually read. The only time it makes sense to read the whole struct/array into a `memory` variable, is if the full struct/array is being returned by the function, is being passed to a function that requires `memory`, or if the array/struct is being read from another `memory` array/struct.

There is 1 instance:

- *SortedCdps.sol* ( [522](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L522) ):

```solidity
522:             Node memory _node = data.nodes[_id];
```

### [G&#x2011;02] Constructors can be marked as payable to save deployment gas

Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. A constructor can be safely marked as payable, because only the deployer would be able to pass funds, and the project itself would not pass any funds.

<details>
<summary>There are 19 instances (click to show):</summary>

- *ActivePool.sol* ( [46-52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L46-L52) ):

```solidity
46:     constructor(
47:         address _borrowerOperationsAddress,
48:         address _cdpManagerAddress,
49:         address _collTokenAddress,
50:         address _collSurplusAddress,
51:         address _feeRecipientAddress
52:     ) {
```

- *BorrowerOperations.sol* ( [107-116](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L107-L116) ):

```solidity
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

- *CdpManager.sol* ( [30-52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L30-L52) ):

```solidity
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

- *CdpManagerStorage.sol* ( [217-227](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L217-L227) ):

```solidity
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

- *CollSurplusPool.sol* ( [42-47](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L42-L47) ):

```solidity
42:     constructor(
43:         address _borrowerOperationsAddress,
44:         address _cdpManagerAddress,
45:         address _activePoolAddress,
46:         address _collTokenAddress
47:     ) {
```

- *Auth.sol* ( [18](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L18) ):

```solidity
18:     constructor(address _owner, Authority _authority) {
```

- *EbtcBase.sol* ( [52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52) ):

```solidity
52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {
```

- *RolesAuthority.sol* ( [20](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20) ):

```solidity
20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}
```

- *EBTCToken.sol* ( [61-65](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L61-L65) ):

```solidity
61:     constructor(
62:         address _cdpManagerAddress,
63:         address _borrowerOperationsAddress,
64:         address _authorityAddress
65:     ) {
```

- *Governor.sol* ( [36](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L36) ):

```solidity
36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
```

- *HintHelpers.sol* ( [27-33](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L27-L33) ):

```solidity
27:     constructor(
28:         address _sortedCdpsAddress,
29:         address _cdpManagerAddress,
30:         address _collateralAddress,
31:         address _activePoolAddress,
32:         address _priceFeedAddress
33:     ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {
```

- *LeverageMacroBase.sol* ( [51-59](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L51-L59) ):

```solidity
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

- *LeverageMacroDelegateTarget.sol* ( [41-58](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L58) ):

```solidity
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

- *LeverageMacroFactory.sol* ( [21-28](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L21-L28) ):

```solidity
21:     constructor(
22:         address _borrowerOperationsAddress,
23:         address _activePool,
24:         address _cdpManager,
25:         address _ebtc,
26:         address _coll,
27:         address _sortedCdps
28:     ) {
```

- *LeverageMacroReference.sol* ( [17-35](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L17-L35) ):

```solidity
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

- *LiquidationLibrary.sol* ( [14-34](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L14-L34) ):

```solidity
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

- *PriceFeed.sol* ( [57-62](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L57-L62) ):

```solidity
57:     constructor(
58:         address _fallbackCallerAddress,
59:         address _authorityAddress,
60:         address _collEthCLFeed,
61:         address _ethBtcCLFeed
62:     ) {
```

- *SimplifiedDiamondLike.sol* ( [44](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44) ):

```solidity
44:     constructor(address _owner) {
```

- *SortedCdps.sol* ( [88](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L88) ):

```solidity
88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {
```

</details>

### [G&#x2011;03] State variables only set in their definitions should be declared `constant`

This can avoid a Gsset (**20000 gas**) on deployment (in constructor), and replaces the first access in each transaction (Gcoldsload - **2100 gas**) and each access thereafter (Gwarmacces - **100 gas**) with a `PUSH32` (**3 gas**).

<details>
<summary>There are 12 instances (click to show):</summary>

- *CdpManagerStorage.sol* ( [142](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L142), [143](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L143), [148](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L148), [159](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L159), [161](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L161), [163](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L163), [166](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L166), [187](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L187), [193](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L193) ):

```solidity
142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;

143:     bool public redemptionsPaused;

148:     uint256 public minuteDecayFactor = 999037758833783000;

159:     uint256 public beta = 2;

161:     uint256 public baseRate;

163:     uint256 public stakingRewardSplit;

166:     uint256 public lastRedemptionTimestamp;

187:     uint256 public systemDebtRedistributionIndex;

193:     uint256 public lastEBTCDebtErrorRedistribution;
```

- *ERC3156FlashLender.sol* ( [14](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14), [15](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15) ):

```solidity
14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

15:     bool public flashLoansPaused;
```

- *Governor.sol* ( [17](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L17) ):

```solidity
17:     bytes32 NO_ROLES = bytes32(0);
```

</details>

### [G&#x2011;04] Splitting `require()` statements that use `&&`

Splitting a `require()` statement containing `&&` into multiple `require()` statements can save gas.

<details>
<summary>There are 8 instances (click to show):</summary>

- *BorrowerOperations.sol* ( [734-737](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L734-L737) ):

```solidity
734:         require(
735:             recoveredAddress != address(0) && recoveredAddress == _borrower,
736:             "BorrowerOperations: Invalid signature"
737:         );
```

- *CdpManager.sol* ( [762-765](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L762-L765) ):

```solidity
762:         require(
763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764:             "Max fee percentage must be between redemption fee floor and 100%"
765:         );
```

- *CdpManagerStorage.sol* ( [261-264](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L261-L264), [466-469](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L466-L469), [653-656](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L653-L656) ):

```solidity
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

- *EBTCToken.sol* ( [296-299](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L296-L299), [300-303](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L300-L303) ):

```solidity
296:         require(
297:             _recipient != address(0) && _recipient != address(this),
298:             "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299:         );

300:         require(
301:             _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302:             "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303:         );
```

- *PriceFeed.sol* ( [79-83](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L79-L83) ):

```solidity
79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );
```

</details>

### [G&#x2011;05] Unnecessary event parameters should be removed

Data that can be obtained from off-chain data and event log details should not be added as event parameters to save gas.

There are 3 instances:

- *CdpManager.sol* ( [698](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L698) ):

```solidity
/// @audit `block.timestamp`
698:             emit LastRedemptionTimestampUpdated(block.timestamp);
```

- *CdpManagerStorage.sol* ( [542](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L542) ):

```solidity
/// @audit `block.timestamp`
542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);
```

- *PriceFeed.sol* ( [381](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L381) ):

```solidity
/// @audit `block.timestamp`
381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);
```

### [G&#x2011;06] Unnecessary ternary operator

Consider assigning the value of the comparison directly instead of performing an additional operation.

(e.g.) `z = (x == y) ? true : false` -> `z = (x == y)`

There are 3 instances:

- *LiquidationLibrary.sol* ( [100](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L100), [695](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L695), [788](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L788) ):

```solidity
100:         bool _recoveryModeAtStart = _TCR < CCR ? true : false;

695:         vars.recoveryModeAtStart = _TCR < CCR ? true : false;

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;
```

### [G&#x2011;07] Use `unchecked` block for safe subtractions

If it can be confirmed that the subtraction operation will not overflow, using an unchecked block can save gas.
For example, `require(x <= y); z = y - x;` can be optimized to `require(x <= y); unchecked { z = y - x; }`.

<details>
<summary>There are 19 instances (click to show):</summary>

- *CdpManager.sol* ( [691](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L691), [712](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L712) ):

```solidity
/// @audit checked on line 690
691:             ? block.timestamp - lastRedemptionTimestamp

/// @audit checked on line 711
712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
```

- *CdpManagerStorage.sol* ( [557](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L557), [639](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L639) ):

```solidity
/// @audit checked on line 556
557:         uint256 deltaIndex = _newIndex - _prevIndex;

/// @audit checked on line 636
639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
```

- *EbtcMath.sol* ( [81](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L81), [89](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L89), [89](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L89) ):

```solidity
/// @audit checked on line 73
81:                 n = (n - 1) / 2;

/// @audit checked on line 89
89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

/// @audit checked on line 89
89:         return (_a >= _b) ? (_a - _b) : (_b - _a);
```

- *LiquidationLibrary.sol* ( [289](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L289), [359](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L359), [362](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L362), [375](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L375), [444](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L444), [567](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L567), [595](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L595), [603](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L603) ):

```solidity
/// @audit checked on line 289
289:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

/// @audit checked on line 358
359:             ? _recoveryState.entireSystemDebt - _totalDebtToBurn

/// @audit checked on line 361
362:             ? _recoveryState.entireSystemColl - _totalColToSend

/// @audit checked on line 375
375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

/// @audit checked on line 444
444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

/// @audit checked on line 564
567:         collSurplus = _totalColToSend - toLiquidator; // Can use unchecked but w/e

/// @audit checked on line 594
595:                 ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)

/// @audit checked on line 602
603:         collSurplus = (toLiquidator == _totalColToSend) ? 0 : _totalColToSend - toLiquidator;
```

- *PriceFeed.sol* ( [798](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L798), [799](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L799) ):

```solidity
/// @audit checked on line 794
798:             ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)

/// @audit checked on line 794
799:             : 10 ** (_ethBtcDecimals - _stEthEthDecimals);
```

- *SortedCdps.sol* ( [425](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L425), [489](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L489) ):

```solidity
/// @audit checked on line 422
425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;

/// @audit checked on line 460
489:         data.size = data.size - 1;
```

</details>

### [G&#x2011;08] Comparing booleans to `true` or `false`

The `true` and `false` are constants and it is more expensive comparing a boolean against them than checking the boolean value directly: `if (<x> == true)` => `if (<x>)`, `if (<x> == false)` => `if (!<x>)`.

There is 1 instance:

- *CdpManager.sol* ( [332](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L332) ):

```solidity
332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");
```

### [G&#x2011;09] Using `constant`s directly is more gas efficient

Using `constant`s directly is more gas efficient than using variables caching the constant values.

There is 1 instance:

- *SimplifiedDiamondLike.sol* ( [84](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L84) ):

```solidity
/// @audit DIAMOND_STORAGE_POSITION
84:         bytes32 position = DIAMOND_STORAGE_POSITION;
```

### [G&#x2011;10] Do not cache state variables that are used only once

It's cheaper to access the state variable directly if it is accessed only once. This can save the 3 gas cost of the extra stack allocation.

There are 4 instances:

- *ActivePool.sol* ( [410](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L410) ):

```solidity
410:         uint256 _oldFee = feeBps;
```

- *BorrowerOperations.sol* ( [1160](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1160) ):

```solidity
1160:         uint256 _oldFee = feeBps;
```

- *CdpManagerStorage.sol* ( [579](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L579) ):

```solidity
579:         uint256 _oldPerUnit = systemStEthFeePerUnitIndex;
```

- *LiquidationLibrary.sol* ( [389](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L389) ):

```solidity
389:         uint256 _liquidatorReward = Cdps[_cdpId].liquidatorRewardShares;
```

### [G&#x2011;11] Do not calculate constants

Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.

There is 1 instance:

- *CdpManagerStorage.sol* ( [141](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L141) ):

```solidity
141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
```

### [G&#x2011;12] Use of `emit` inside a loop

Emitting an event inside a loop performs a `LOG` op N times, where N is the loop length. Consider refactoring the code to emit the event only once at the end of loop. Gas savings should be multiplied by the average loop length.

There is 1 instance:

- *SortedCdps.sol* ( [451](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L451) ):

```solidity
451:             emit NodeRemoved(_ids[i]);
```

### [G&#x2011;13] Initializing mutable state variables with default value wastes gas

It costs more gas to initialize non-`constant`/non-`immutable` state variables to zero than to let the default of zero be applied. Not overwriting the default for storage variables avoids a Gsreset ([**2900 gas**](https://gist.github.com/IllIllI000/85b09af2291f626095eb11403ddc74f1)) during deployment.

There is 1 instance:

- *Governor.sol* ( [17](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L17) ):

```solidity
17:     bytes32 NO_ROLES = bytes32(0);
```

### [G&#x2011;14] Use local variables for emitting

Use the function/modifier's local copy of the state variable, rather than incurring an extra Gwarmaccess (**100 gas**). In the unlikely event that the state variable hasn't already been used by the function/modifier, consider whether it is really necessary to include it in the event, given the fact that it incurs a Gcoldsload (**2100 gas**), or whether it can be passed in to or back out of the functions that _do_ use it.

<details>
<summary>There are 6 instances (click to show):</summary>

- *CdpManager.sol* ( [55](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L55), [220-230](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L220-L230) ):

```solidity
/// @audit stakingRewardSplit
55:         emit StakingRewardSplitSet(stakingRewardSplit);

/// @audit Cdps
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
```

- *LiquidationLibrary.sol* ( [490-500](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L490-L500), [891](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L891) ):

```solidity
/// @audit Cdps
/// @audit Cdps
/// @audit Cdps
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

/// @audit systemDebtRedistributionIndex
891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);
```

</details>

### [G&#x2011;15] Contract storage can use fewer slots by changing the order of state variables

The reduction of slots can reduce the gas consumption of each storage read/write operation. If variables occupying the same slot are written within the same transaction, avoids a separate Gsset (**20000 gas**). Reads of the variables can also be cheaper.

There is 1 instance:

- *PriceFeed.sol* ( [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L21) ):

```solidity
/// @audit 3 slots -> 2 slots by new order:
///        32 B: uint256 lastGoodPrice
///        20 B: IFallbackCaller fallbackCaller
///        1 B: Status status
21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
```

### [G&#x2011;16] Structs can use fewer slots by changing the order of fields

The reduction of slots can reduce the gas consumption of each storage read/write operation. Each slot saved can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

<details>
<summary>There are 4 instances (click to show):</summary>

- *BorrowerOperations.sol* ( [97-104](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L97-L104) ):

```solidity
/// @audit 6 slots -> 4 slots by new order:
///        32 B: uint256 collSharesChange
///        32 B: uint256 collAddUnderlying
///        32 B: uint256 netDebtChange
///        20 B: address user
///        1 B: bool isCollIncrease
///        1 B: bool isDebtIncrease
97:     struct MoveTokensParams {
98:         address user;
99:         uint256 collSharesChange;
100:         uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101:         bool isCollIncrease;
102:         uint256 netDebtChange;
103:         bool isDebtIncrease;
104:     }
```

- *IPriceFeed.sol* ( [17-24](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24) ):

```solidity
/// @audit 5 slots -> 4 slots by new order:
///        32 B: uint256 answer
///        32 B: uint256 timestampEthBtc
///        32 B: uint256 timestampStEthEth
///        10 B: uint80 roundEthBtcId
///        10 B: uint80 roundStEthEthId
///        1 B: bool success
17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }
```

- *LeverageMacroBase.sol* ( [259-266](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L259-L266) ):

```solidity
/// @audit 6 slots -> 5 slots by new order:
///        32 B: uint256 amountToTransferIn
///        32 B: SwapOperation[] swapsBefore
///        32 B: SwapOperation[] swapsAfter
///        32 B: bytes OperationData
///        20 B: address tokenToTransferIn
///        1 B: OperationType operationType
259:     struct LeverageMacroOperation {
260:         address tokenToTransferIn;
261:         uint256 amountToTransferIn;
262:         SwapOperation[] swapsBefore; // Empty to skip
263:         SwapOperation[] swapsAfter; // Empty to skip
264:         OperationType operationType; // Open, Close, etc..
265:         bytes OperationData; // Generic Operation Data, which we'll decode to use
266:     }
```

- *SimplifiedDiamondLike.sol* ( [99-107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107) ):

```solidity
/// @audit 4 slots -> 3 slots by new order:
///        32 B: bytes data
///        20 B: address to
///        1 B: bool checkSuccess
///        1 B: bool capGas
///        1 B: OperationType opType
///        16 B: uint128 value
///        16 B: uint128 gas
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

</details>

### [G&#x2011;17] `internal` functions only called once can be inlined to save gas

If an `internal` function is only used once, there is no need to modularize it, unless the function calling it would otherwise be too long and complex. Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

<details>
<summary>There are 13 instances (click to show):</summary>

- *ActivePool.sol* ( [235](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L235) ):

```solidity
235:     function _requireCallerIsCdpManager() internal view {
```

- *BorrowerOperations.sol* ( [829](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L829), [834](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L834) ):

```solidity
829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {
```

- *CdpManager.sol* ( [655](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L655), [753](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L753), [757](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L757), [977](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L977), [984](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L984) ):

```solidity
655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {

753:     function _requireAmountGreaterThanZero(uint256 _amount) internal pure {

757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

977:     function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {

984:     function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {
```

- *CdpManagerStorage.sol* ( [648](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L648) ):

```solidity
648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {
```

- *CollSurplusPool.sol* ( [119](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L119), [123](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L123) ):

```solidity
119:     function _requireCallerIsCdpManager() internal view {

123:     function _requireCallerIsActivePool() internal view {
```

- *EbtcBase.sol* ( [60](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L60), [95](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L95) ):

```solidity
60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {
```

</details>

### [G&#x2011;18] Using `this` to access functions results in an external call, wasting gas

External calls have an overhead of **100 gas**, which can be avoided by not referencing the function using `this`. Contracts [are allowed](https://docs.soliditylang.org/en/latest/contracts.html#function-overriding) to override their parents' functions and change the visibility from `external` to `public`, so make this change if it's required in order to call the function internally.

There is 1 instance:

- *LeverageMacroDelegateTarget.sol* ( [64](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64) ):

```solidity
64:         address _owner = IOwnerLike(address(this)).owner();
```

### [G&#x2011;19] Functions that revert when called by normal users can be marked `payable`

If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.
The extra opcodes avoided are: 
`CALLVALUE(2), DUP1(3), ISZERO(3), PUSH2(3), JUMPI(10), PUSH1(3), DUP1(3), REVERT(0), JUMPDEST(1), POP(2)` 
which cost an average of about 21 gas per call to the function, in addition to the extra deployment cost.

<details>
<summary>There are 38 instances (click to show):</summary>

- *ActivePool.sol* ( [157](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L157), [346](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L346), [371](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L371), [390](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L390), [404](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L404), [417](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L417) ):

```solidity
157:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external override {

346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {

371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
```

- *BorrowerOperations.sol* ( [553](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L553), [628-631](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L628-L631), [647](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L647), [653](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L653), [706-714](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L706-L714), [1140](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1140), [1154](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1154), [1167](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1167) ):

```solidity
553:     function closeCdp(bytes32 _cdpId) external override {

628:     function setPositionManagerApproval(
629:         address _positionManager,
630:         PositionManagerApproval _approval
631:     ) external override {

647:     function revokePositionManagerApproval(address _positionManager) external override {

653:     function renouncePositionManagerApproval(address _borrower) external override {

706:     function permitPositionManagerApproval(
707:         address _borrower,
708:         address _positionManager,
709:         PositionManagerApproval _approval,
710:         uint256 _deadline,
711:         uint8 v,
712:         bytes32 r,
713:         bytes32 s
714:     ) external override {

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {
```

- *CdpManager.sol* ( [773](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L773), [788](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L788), [807](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L807), [830](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L830), [843](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L843) ):

```solidity
773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {
```

- *CdpManagerStorage.sol* ( [111](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L111) ):

```solidity
111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
```

- *CollSurplusPool.sol* ( [77](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L77), [142](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L142) ):

```solidity
77:     function increaseSurplusCollShares(address _account, uint256 _amount) external override {

142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
```

- *Auth.sol* ( [52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L52) ):

```solidity
52:     function transferOwnership(address newOwner) public virtual requiresAuth {
```

- *RolesAuthority.sol* ( [85-89](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L89), [106-111](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L106-L111), [133](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L133), [147](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147) ):

```solidity
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

- *EBTCToken.sol* ( [85](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L85), [95](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L95), [104](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L104) ):

```solidity
85:     function mint(address _account, uint256 _amount) external override {

95:     function burn(address _account, uint256 _amount) external override {

104:     function burn(uint256 _amount) external {
```

- *Governor.sol* ( [154](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L154) ):

```solidity
154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {
```

- *LeverageMacroBase.sol* ( [118-124](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L118-L124), [214](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L214), [234](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L234) ):

```solidity
118:     function doOperation(
119:         FlashLoanType flType,
120:         uint256 borrowAmount,
121:         LeverageMacroOperation calldata operation,
122:         PostOperationCheck postCheckType,
123:         PostCheckParams calldata checkParams
124:     ) external {

214:     function sweepToCaller() public {

234:     function sweepToken(address token, uint256 amount) public {
```

- *LeverageMacroReference.sol* ( [50](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L50) ):

```solidity
50:     function resetApprovals() external {
```

- *PriceFeed.sol* ( [358](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L358) ):

```solidity
358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
```

- *SortedCdps.sol* ( [410](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L410), [419](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L419) ):

```solidity
410:     function remove(bytes32 _id) external override {

419:     function batchRemove(bytes32[] memory _ids) external override {
```

</details>

### [G&#x2011;20] Use `x = x + y` instead of `x += y` for state variables

Using the `x = x + y` instead of `x += y` for state simple state variables can save **10 gas**. The same applies to `-=`, `*=`, etc.

There is 1 instance:

- *CdpManager.sol* ( [697](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L697) ):

```solidity
697:             lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;
```

### [G&#x2011;21] Operator `>=`/`<=` costs less gas than operator `>`/`<`

The compiler uses opcodes `GT` and `ISZERO` for code that uses `>`, but only requires `LT` for `>=`. A similar behavior applies for `>`, which uses opcodes `LT` and `ISZERO`, but only requires `GT` for `<=`. It can [save **3 gas**](https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde) for each.
It should be converted to the `<=`/`>=` equivalent when comparing against integer literals.

<details>
<summary>There are 126 instances (click to show):</summary>

- *ActivePool.sol* ( [267](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L267) ):

```solidity
267:         require(amount > 0, "ActivePool: 0 Amount");
```

- *BorrowerOperations.sol* ( [393](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L393), [463](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L463), [495](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L495), [835](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L835), [891](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L891), [936](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L936), [1083](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1083) ):

```solidity
393:         if (!_isDebtIncrease && _debtChange > 0) {

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

495:             if (newTCR < CCR) {

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

891:             if (_vars.newTCR < CCR) {

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");
```

- *CdpManager.sol* ( [203](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L203), [279](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L279), [285](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L285), [369](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L369), [389](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L389), [389](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L389), [431](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L431), [436](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L436), [497](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L497), [601](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L601), [626](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L626), [672](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L672), [690](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L690), [711](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L711), [754](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L754) ):

```solidity
203:                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE

279:             getSyncedICR(_firstRedemptionHint, _price) < MCR

285:         return nextCdp == sortedCdps.nonExistId() || getSyncedICR(nextCdp, _price) < MCR;

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

436:         } else if (_numCdpsFullyRedeemed > 1) {

497:         while (_cnt > 0 && _id != bytes32(0)) {

601:         return TCR < CCR;

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

690:         uint256 timePassed = block.timestamp > lastRedemptionTimestamp

711:             block.timestamp > lastRedemptionTimestamp

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");
```

- *CdpManagerStorage.sol* ( [99](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L99), [315](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L315), [332](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L332), [362](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L362), [362](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L362), [369](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L369), [380](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L380), [453](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L453), [512](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L512), [512](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L512), [556](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L556), [584](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L584), [636](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L636), [654](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L654), [654](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L654), [765](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L765), [765](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L765), [796](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L796), [829](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L829), [879](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L879), [900](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L900) ):

```solidity
99:         if (newTCR < CCR) {

315:         if (_debtIndexDiff > 0) {

332:         return (cdpDebtRedistributionIndex[_cdpId] < systemDebtRedistributionIndex);

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

636:         if (_scaledCdpColl > _feeSplitDistributed) {

654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {

900:             block.timestamp > cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration;
```

- *CollSurplusPool.sol* ( [92](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L92) ):

```solidity
92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");
```

- *EbtcBase.sol* ( [100](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L100), [135](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L135) ):

```solidity
100:         return _tcr < CCR;

135:         return _icr < MCR;
```

- *EbtcMath.sol* ( [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L21), [60](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L60), [73](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L73), [93](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L93), [109](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L109) ):

```solidity
21:         return (_a < _b) ? _a : _b;

60:         if (_minutes > 525600000) {

73:         while (n > 1) {

93:         if (_debt > 0) {

109:         if (_debt > 0) {
```

- *Governor.sol* ( [46](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L46), [53](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L53), [57](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L57), [76](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L76), [81](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L81), [84](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L84), [98](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L98), [104](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L104), [107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L107), [122](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L122), [135](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L135), [137](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L137) ):

```solidity
46:         for (uint256 i = 0; i < users.length(); i++) {

53:         if (count > 0) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

81:         if (count > 0) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

104:         if (count > 0) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

135:         if (_sigs.length > 0) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {
```

- *HintHelpers.sol* ( [70](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L70), [86](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L86), [87](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L87), [93](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L93), [102-103](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L102-L103), [181](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L181), [191](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L191) ):

```solidity
70:                 cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR

86:                 vars.remainingEbtcToRedeem > 0 &&

87:                 _maxIterations-- > 0

93:                 if (currentCdpDebt > vars.remainingEbtcToRedeem) {

102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <
103:                         MIN_NET_STETH_BALANCE

181:         while (i < _numTrials) {

191:             if (currentDiff < diff) {
```

- *LeverageMacroBase.sol* ( [128](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L128), [223](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L223), [227](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L227), [293](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L293), [307](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L307), [385](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L385), [438](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L438), [441-442](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L441-L442) ):

```solidity
128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {

385:         for (uint256 i; i < swapLength; ) {

438:             for (uint256 i; i < length; ++i) {

441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
```

- *LiquidationLibrary.sol* ( [94-95](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L94-L95), [100](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L100), [195](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L195), [261](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L261), [266](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L266), [289](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L289), [336](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L336), [342](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L342), [358](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L358), [361](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L361), [375](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L375), [444](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L444), [476](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L476), [525](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L525), [553](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L553), [555](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L555), [564](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L564), [578](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L578), [579](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L579), [594](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L594), [602](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L602), [695](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L695), [710](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L710), [713](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L713), [788](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L788) ):

```solidity
94:                 block.timestamp >
95:                     cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,

100:         bool _recoveryModeAtStart = _TCR < CCR ? true : false;

195:             if (_outputState.totalSurplusCollShares > 0) {

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

289:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

358:         _recoveryState.entireSystemDebt = _recoveryState.entireSystemDebt > _totalDebtToBurn

361:         _recoveryState.entireSystemColl = _recoveryState.entireSystemColl > _totalColToSend

375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

476:         if (_partialState.ICR > LICR) {

525:         if (totalDebtToRedistribute > 0) {

553:         if (_ICR > LICR) {

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

564:         assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

578:         if (_ICR > LICR) {

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

594:             debtToRedistribute = _debtToRepay < _totalDebtToBurn

602:         toLiquidator = toLiquidator < _totalColToSend ? toLiquidator : _totalColToSend;

695:         vars.recoveryModeAtStart = _TCR < CCR ? true : false;

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

713:         if (totals.totalCollSurplus > 0) {

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;
```

- *PriceFeed.sol* ( [421](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L421), [423](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L423), [457](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L457), [462](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L462), [471](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L471), [489](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L489), [494](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L494), [794](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L794), [797](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L797) ):

```solidity
421:             _response.timestampEthBtc > block.timestamp ||

423:             _response.timestampStEthEth > block.timestamp

457:         uint256 percentDeviation = maxPrice > 0

462:         return percentDeviation > MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND;

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

489:             _fallbackResponse.timestamp > 0 &&

494:         return block.timestamp - _timestamp > _timeout;

794:         uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals

797:         uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals
```

- *SimplifiedDiamondLike.sol* ( [114](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L114) ):

```solidity
114:         for (uint256 i; i < length; ) {
```

- *SortedCdps.sol* ( [202](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L202), [259](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L259), [274](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L274), [330](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L330), [371](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L371), [422](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L422), [432](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L432), [449](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L449), [460](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L460), [508](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L508), [683](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L683), [690](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L690) ):

```solidity
202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

274:         if (_ownedCount > 0) {

330:             if (maxNodes > 0 && i >= maxNodes) {

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

432:         for (uint256 i = 0; i < _len; ++i) {

449:         for (uint i = 0; i < _len; ++i) {

460:         if (data.size > 1) {

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {

690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {
```

</details>

### [G&#x2011;22] Usage of `int`s/`uint`s smaller than 32 bytes incurs overhead

Using `ints`/`uints` smaller than 32 bytes may cost more gas. This is because the EVM operates on 32 bytes at a time, so if an element is smaller than 32 bytes, the EVM must perform more operations to reduce the size of the element from 32 bytes to the desired size.

<details>
<summary>There are 64 instances (click to show):</summary>

- *BorrowerOperations.sol* ( [711](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L711) ):

```solidity
/// @audit uint8
711:         uint8 v,
```

- *CdpManager.sol* ( [550](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L550) ):

```solidity
/// @audit uint128
550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
```

- *CdpManagerStorage.sol* ( [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L21), [22](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L22), [24](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L24), [25](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L25), [111](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L111), [148](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L148), [161](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L161), [166](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L166), [471](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L471), [897](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L897) ):

```solidity
/// @audit uint128
21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

/// @audit uint128
22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

/// @audit uint128
24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

/// @audit uint128
25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

/// @audit uint128
111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

/// @audit uint256
148:     uint256 public minuteDecayFactor = 999037758833783000;

/// @audit uint256
161:     uint256 public baseRate;

/// @audit uint256
166:     uint256 public lastRedemptionTimestamp;

/// @audit uint128
471:         uint128 index = Cdps[_cdpId].arrayIndex;

/// @audit uint128
897:         uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;
```

- *ERC3156FlashLender.sol* ( [14](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L14) ):

```solidity
/// @audit uint16
14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance
```

- *RolesAuthority.sol* ( [38](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38), [43](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L43), [107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L107), [147](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147) ):

```solidity
/// @audit uint8
38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

/// @audit uint8
43:         uint8 role,

/// @audit uint8
107:         uint8 role,

/// @audit uint8
147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
```

- *EBTCToken.sol* ( [31](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L31), [204](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L204), [343](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L343) ):

```solidity
/// @audit uint8
31:     uint8 internal constant _DECIMALS = 18;

/// @audit uint8
204:         uint8 v,

/// @audit uint8
343:     function decimals() external pure override returns (uint8) {
```

- *Governor.sol* ( [20](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L20), [32](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L32), [43](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L43), [76](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L76), [84](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L84), [98](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L98), [107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L107), [122](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L122), [146](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L146), [154](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L154) ):

```solidity
/// @audit uint8
20:         uint8 roleId;

/// @audit uint8
32:     event RoleNameSet(uint8 indexed role, string indexed name);

/// @audit uint8
43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

/// @audit uint8
76:         for (uint8 i = 0; i < type(uint8).max; i++) {

/// @audit uint8
84:             for (uint8 i = 0; i < type(uint8).max; i++) {

/// @audit uint8
98:         for (uint8 i = 0; i < type(uint8).max; i++) {

/// @audit uint8
107:             for (uint8 i = 0; i < type(uint8).max; i++) {

/// @audit uint8
122:         for (uint8 i = 0; i < roleIds.length; i++) {

/// @audit uint8
146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

/// @audit uint8
154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {
```

- *ICdpManagerData.sol* ( [103](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L103), [201](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L201) ):

```solidity
/// @audit uint128
103:         uint128 arrayIndex;

/// @audit uint256
201:         uint256 decayedBaseRate;
```

- *IPositionManagers.sol* ( [37](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L37) ):

```solidity
/// @audit uint8
37:         uint8 v,
```

- *IPriceFeed.sol* ( [18](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L18), [19](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L19), [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L21), [22](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L22), [28](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L28) ):

```solidity
/// @audit uint80
18:         uint80 roundEthBtcId;

/// @audit uint80
19:         uint80 roundStEthEthId;

/// @audit uint256
21:         uint256 timestampEthBtc;

/// @audit uint256
22:         uint256 timestampStEthEth;

/// @audit uint256
28:         uint256 timestamp;
```

- *LeverageMacroBase.sol* ( [502](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L502) ):

```solidity
/// @audit uint16
502:         uint16 _maxCopy,
```

- *LiquidationLibrary.sol* ( [88](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L88) ):

```solidity
/// @audit uint128
88:             uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;
```

- *PriceFeed.sol* ( [612](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L612), [613](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L613), [615](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L615), [623](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L623), [635](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L635), [640](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L640), [651](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L651), [656](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L656), [688](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L688), [689](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L689), [700](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L700), [701](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L701), [703](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L703), [711](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L711), [723](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L723), [728](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L728), [739](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L739), [744](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L744), [775](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L775), [791](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L791), [792](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L792) ):

```solidity
/// @audit uint8
612:         uint8 ethBtcDecimals;

/// @audit uint8
613:         uint8 stEthEthDecimals;

/// @audit uint8
615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

/// @audit uint8
623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

/// @audit uint80
635:             uint80 roundId,

/// @audit uint80
640:             uint80 /* answeredInRound */

/// @audit uint80
651:             uint80 roundId,

/// @audit uint80
656:             uint80 /* answeredInRound */

/// @audit uint80
688:         uint80 _currentRoundEthBtcId,

/// @audit uint80
689:         uint80 _currentRoundStEthEthId

/// @audit uint8
700:         uint8 ethBtcDecimals;

/// @audit uint8
701:         uint8 stEthEthDecimals;

/// @audit uint8
703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

/// @audit uint8
711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

/// @audit uint80
723:             uint80 roundId,

/// @audit uint80
728:             uint80 /* answeredInRound */

/// @audit uint80
739:             uint80 roundId,

/// @audit uint80
744:             uint80 /* answeredInRound */

/// @audit uint80
775:     function _checkHealthyCLResponse(uint80 _roundId, int256 _answer) internal view returns (bool) {

/// @audit uint8
791:         uint8 _ethBtcDecimals,

/// @audit uint8
792:         uint8 _stEthEthDecimals
```

- *SimplifiedDiamondLike.sol* ( [102](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L102), [103](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L103) ):

```solidity
/// @audit uint128
102:         uint128 value; // How much ETH to send

/// @audit uint128
103:         uint128 gas; // How much gas to send
```

- *SortedCdps.sol* ( [79](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L79) ):

```solidity
/// @audit uint256
79:     uint256 public nextCdpNonce;
```

</details>

### [G&#x2011;23] Using a double `if` statement instead of a logical AND(`&&`)

Using a double `if` statement instead of a logical AND (`&&`) can provide similar short-circuiting behavior whereas double if is slightly [more gas efficient](https://gist.github.com/DadeKuma/931ce6794a050201ec6544dbcc31316c).

<details>
<summary>There are 14 instances (click to show):</summary>

- *BorrowerOperations.sol* ( [393](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L393) ):

```solidity
393:         if (!_isDebtIncrease && _debtChange > 0) {
```

- *CdpManagerStorage.sol* ( [512](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L512), [796](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L796) ):

```solidity
512:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
```

- *LiquidationLibrary.sol* ( [157-159](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L157-L159), [756](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L756), [790](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L790), [819](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L819) ):

```solidity
157:             if (
158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&
159:                 liquidationValues.debtToBurn == 0

756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {

819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
```

- *PriceFeed.sol* ( [226-228](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L226-L228), [372-374](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L372-L374) ):

```solidity
226:                 if (
227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)

372:                 if (
373:                     !_fallbackIsBroken(fallbackResponse) &&
374:                     !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
```

- *SortedCdps.sol* ( [202](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L202), [259](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L259), [330](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L330), [621](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L621), [644](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L644) ):

```solidity
202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

330:             if (maxNodes > 0 && i >= maxNodes) {

621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644:         if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
```

</details>

### [G&#x2011;24] Divisions can be unchecked to save gas

The expression `type(int).min/(-1)` is the only case where division causes an overflow. Therefore, uncheck can be used to [save gas](https://gist.github.com/DadeKuma/3bc597338ae774b8b3bd43280d55271f) in scenarios where it is certain that such an overflow will not occur.

<details>
<summary>There are 34 instances (click to show):</summary>

- *ActivePool.sol* ( [321](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L321) ):

```solidity
321:         return (amount * feeBps) / MAX_BPS;
```

- *BorrowerOperations.sol* ( [1118](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1118) ):

```solidity
1118:         return (amount * feeBps) / MAX_BPS;
```

- *CdpManager.sol* ( [146](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L146), [621-622](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L621-L622), [624](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L624), [671](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L671), [706](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L706), [712](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L712) ):

```solidity
146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622:             _totalEBTCSupply;

624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

671:         uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

706:         return (baseRate * decayFactor) / DECIMAL_PRECISION;

712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)
```

- *CdpManagerStorage.sol* ( [316](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L316), [454](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L454), [558](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L558), [564](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L564), [567](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L567), [639](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L639) ):

```solidity
316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;

454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

558:         uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
```

- *EbtcBase.sol* ( [108](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L108), [119](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L119) ):

```solidity
108:         uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;

119:         return (_debt * _price) / DECIMAL_PRECISION;
```

- *EbtcMath.sol* ( [38](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38), [38](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38), [76](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L76), [81](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L81), [94](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L94), [110](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L110) ):

```solidity
38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

76:                 n = n / 2;

81:                 n = (n - 1) / 2;

94:             return (_collShares * NICR_PRECISION) / _debt;

110:             uint256 newCollRatio = (_stEthBalance * _price) / _debt;
```

- *HintHelpers.sol* ( [145](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L145) ):

```solidity
145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
```

- *LiquidationLibrary.sol* ( [278](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L278), [365](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L365), [435](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L435), [555](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L555), [558](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L558), [579](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L579), [592](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L592), [882](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L882) ):

```solidity
278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

558:             _incentiveColl = (_totalDebtToBurn * LICR) / _price;

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

592:             uint256 _debtToRepay = (_incentiveColl * _price) / LICR;

882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;
```

- *PriceFeed.sol* ( [458](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L458), [534-535](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L534-L535), [801-804](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L801-L804) ):

```solidity
458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice

534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /
535:             minPrice;

801:             (_scaledDecimal *
802:                 uint256(_ethBtcAnswer) *
803:                 uint256(_stEthEthAnswer) *
804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);
```

</details>

### [G&#x2011;25] Increments can be `unchecked` to save gas

Using `unchecked` increments can save gas by bypassing the built-in overflow checks. This can save [30-40 gas](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked) **per iteration**. So it is recommended to use `unchecked` increments when overflow is not possible.

<details>
<summary>There are 11 instances (click to show):</summary>

- *Governor.sol* ( [46](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L46), [57](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L57), [76](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L76), [84](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L84), [98](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L98), [107](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L107), [122](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L122), [137](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L137) ):

```solidity
46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {
```

- *LeverageMacroBase.sol* ( [438](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L438) ):

```solidity
438:             for (uint256 i; i < length; ++i) {
```

- *SortedCdps.sol* ( [432](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L432), [449](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L449) ):

```solidity
432:         for (uint256 i = 0; i < _len; ++i) {

449:         for (uint i = 0; i < _len; ++i) {
```

</details>

### [G&#x2011;26] Remove unused local variables

Unused local variables to save gas.

There are 6 instances:

- *CdpManager.sol* ( [922](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L922) ):

```solidity
922:         uint256 index = _addCdpIdToArray(_cdpId);
```

- *CdpManagerStorage.sol* ( [357](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L357), [687](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L687) ):

```solidity
357:             uint _pendingDebt,

687:         (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(
```

- *LeverageMacroBase.sol* ( [465](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L465) ):

```solidity
465:         bytes32 _cdpId = borrowerOperations.openCdp(
```

- *PriceFeed.sol* ( [656](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L656), [744](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L744) ):

```solidity
656:             uint80 /* answeredInRound */

744:             uint80 /* answeredInRound */
```

### [G&#x2011;27] Use assembly to validate `msg.sender`

We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. For more details check the following report [Here](https://code4rena.com/reports/2023-05-juicebox#g-06-use-assembly-to-validate-msgsender)

<details>
<summary>There are 24 instances (click to show):</summary>

- *ActivePool.sol* ( [221](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L221), [229](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L229), [229](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L229), [236](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L236) ):

```solidity
221:             msg.sender == borrowerOperationsAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
```

- *BorrowerOperations.sol* ( [964](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L964) ):

```solidity
964:         if (_borrower == msg.sender) {
```

- *CdpManagerStorage.sol* ( [661](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L661) ):

```solidity
661:             msg.sender == borrowerOperationsAddress,
```

- *CollSurplusPool.sol* ( [114](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L114), [120](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L120), [124](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L124) ):

```solidity
114:             msg.sender == borrowerOperationsAddress,

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
```

- *Auth.sol* ( [45](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L45) ):

```solidity
45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

- *EBTCToken.sol* ( [308](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L308), [316](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L316), [317](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L317), [324](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L324) ):

```solidity
308:             msg.sender == borrowerOperationsAddress,

316:             msg.sender == borrowerOperationsAddress ||

317:                 msg.sender == cdpManagerAddress ||

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
```

- *LeverageMacroBase.sol* ( [45](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L45), [357](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L357), [363](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L363) ):

```solidity
45:         require(owner() == msg.sender, "Must be owner");

357:                 msg.sender == address(borrowerOperations),

363:                 msg.sender == address(activePool),
```

- *SimplifiedDiamondLike.sol* ( [52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52), [67](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L67), [77](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L77), [111](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L111) ):

```solidity
52:         require(msg.sender == owner);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111:         require(msg.sender == owner, "Must be owner");
```

- *SortedCdps.sol* ( [715](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L715), [721](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L721), [721](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L721) ):

```solidity
715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
```

</details>

### [G&#x2011;28] Use `x += y` instead of `x = x + y` for mapping state variables

Using `+=` for mappings saves **40 gas** due to not having to recalculate the mapping's value's hash. The same applies to `-=`, `*=`, etc.

There are 2 instances:

- *EBTCToken.sol* ( [258](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L258), [266](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L266) ):

```solidity
258:         _balances[recipient] = _balances[recipient] + amount;

266:         _balances[account] = _balances[account] + amount;
```

### [G&#x2011;29] Avoid zero transfer to save gas

In Solidity, unnecessary operations can waste gas. For example, a transfer function without a zero amount check uses gas even if called with a zero amount, since the contract state remains unchanged. Implementing a zero amount check avoids these unnecessary function calls, saving gas and improving efficiency.

There are 2 instances:

- *BorrowerOperations.sol* ( [785](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L785) ):

```solidity
785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);
```

- *LeverageMacroBase.sol* ( [237](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L237) ):

```solidity
237:         IERC20(token).safeTransfer(msg.sender, amount);
```

### [G&#x2011;30] Optimize names to save gas

`public`/`external` function names and `public` member variable names can be optimized to save gas. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92).

<details>
<summary>There are 33 instances (click to show):</summary>

- *ActivePool.sol* ( [22](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L22) ):

```solidity
/// @audit getSystemCollShares(), getSystemDebt(), getFeeRecipientClaimableCollShares(), transferSystemCollShares(), transferSystemCollSharesAndLiquidatorReward(), allocateSystemCollSharesToFeeRecipient(), increaseSystemDebt(), decreaseSystemDebt(), increaseSystemCollShares(), flashLoan(), flashFee(), maxFlashLoan(), claimFeeRecipientCollShares(), sweepToken(), setFeeRecipientAddress(), setFeeBps(), setFlashLoansPaused(), NAME, borrowerOperationsAddress, cdpManagerAddress, collSurplusPoolAddress, feeRecipientAddress, collateral
22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {
```

- *BorrowerOperations.sol* ( [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L21) ):

```solidity
/// @audit openCdp(), openCdpFor(), addColl(), withdrawColl(), withdrawDebt(), repayDebt(), adjustCdp(), adjustCdpWithColl(), closeCdp(), claimSurplusCollShares(), getPositionManagerApproval(), setPositionManagerApproval(), revokePositionManagerApproval(), renouncePositionManagerApproval(), DOMAIN_SEPARATOR(), domainSeparator(), version(), permitTypeHash(), permitPositionManagerApproval(), flashLoan(), flashFee(), maxFlashLoan(), setFeeRecipientAddress(), setFeeBps(), setFlashLoansPaused(), NAME, cdpManager, collSurplusPool, feeRecipientAddress, ebtcToken, sortedCdps, positionManagers
21: contract BorrowerOperations is
```

- *CdpManager.sol* ( [16](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L16) ):

```solidity
/// @audit getActiveCdpsCount(), getIdFromCdpIdsArray(), liquidate(), partiallyLiquidate(), batchLiquidateCdps(), redeemCollateral(), syncAccounting(), updateStakeAndTotalStakes(), closeCdp(), getSystemDebt(), getCachedTCR(), checkRecoveryMode(), getRedemptionRate(), getRedemptionRateWithDecay(), getRedemptionFeeWithDecay(), getDeploymentStartTime(), checkPotentialRecoveryMode(), setStakingRewardSplit(), setRedemptionFeeFloor(), setMinuteDecayFactor(), setBeta(), setRedemptionsPaused(), getCdpStatus(), getCdpStake(), getCdpDebt(), getCdpCollShares(), getCdpLiquidatorRewardShares(), initializeCdp(), updateCdp()
16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {
```

- *CdpManagerStorage.sol* ( [19](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L19) ):

```solidity
/// @audit notifyStartGracePeriod(), notifyEndGracePeriod(), setGracePeriod(), syncGlobalAccounting(), syncGlobalAccountingAndGracePeriod(), calcFeeUponStakingReward(), getAccumulatedFeeSplitApplied(), getCachedNominalICR(), getSyncedNominalICR(), getCachedICR(), getPendingRedistributedDebt(), hasPendingRedistributedDebt(), getSyncedDebtAndCollShares(), getSyncedCdpDebt(), getSyncedCdpCollShares(), getSyncedICR(), getSyncedTCR(), canLiquidateRecoveryMode(), UNSET_TIMESTAMP, MINIMUM_GRACE_PERIOD, lastGracePeriodStartTimestamp, recoveryModeGracePeriodDuration, NAME, borrowerOperationsAddress, ebtcToken, liquidationLibrary, sortedCdps, SECONDS_IN_ONE_MINUTE, MIN_REDEMPTION_FEE_FLOOR, redemptionFeeFloor, redemptionsPaused, minuteDecayFactor, MIN_MINUTE_DECAY_FACTOR, MAX_MINUTE_DECAY_FACTOR, beta, baseRate, stakingRewardSplit, lastRedemptionTimestamp, Cdps, totalStakes, totalStakesSnapshot, totalCollateralSnapshot, systemDebtRedistributionIndex, cdpDebtRedistributionIndex, lastEBTCDebtErrorRedistribution, stEthIndex, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError, cdpStEthFeePerUnitIndex, CdpIds
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {
```

- *CollSurplusPool.sol* ( [16](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L16) ):

```solidity
/// @audit getTotalSurplusCollShares(), getSurplusCollShares(), increaseSurplusCollShares(), claimSurplusCollShares(), increaseTotalSurplusCollShares(), sweepToken(), NAME, borrowerOperationsAddress, cdpManagerAddress, activePoolAddress, feeRecipientAddress, collateral
16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {
```

- *Auth.sol* ( [9](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L9) ):

```solidity
/// @audit setAuthority(), transferOwnership(), owner, authority
9: abstract contract Auth {
```

- *AuthNoOwner.sol* ( [10](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10) ):

```solidity
/// @audit authority(), authorityInitialized(), setAuthority()
10: contract AuthNoOwner {
```

- *ERC3156FlashLender.sol* ( [8](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L8) ):

```solidity
/// @audit MAX_BPS, MAX_FEE_BPS, FLASH_SUCCESS_VALUE, feeBps, flashLoansPaused
8: abstract contract ERC3156FlashLender is IERC3156FlashLender {
```

- *EbtcBase.sol* ( [16](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L16) ):

```solidity
/// @audit getSystemCollShares(), LICR, MCR, CCR, LIQUIDATOR_REWARD, MIN_NET_STETH_BALANCE, PERCENT_DIVISOR, BORROWING_FEE_FLOOR, STAKING_REWARD_SPLIT, MAX_REWARD_SPLIT, activePool, priceFeed, collateral
16: contract EbtcBase is BaseMath, IEbtcBase {
```

- *RolesAuthority.sol* ( [12](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L12) ):

```solidity
/// @audit doesUserHaveRole(), doesRoleHaveCapability(), isPublicCapability(), canCall(), setPublicCapability(), setRoleCapability(), burnCapability(), setUserRole(), getUserRoles, capabilityFlag, getRolesWithCapability
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {
```

- *EBTCToken.sol* ( [26](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L26) ):

```solidity
/// @audit mint(), burn(), burn(), increaseAllowance(), decreaseAllowance(), DOMAIN_SEPARATOR(), domainSeparator(), permit(), nonces(), version(), permitTypeHash(), cdpManagerAddress, borrowerOperationsAddress
26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {
```

- *Governor.sol* ( [13](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L13) ):

```solidity
/// @audit getUsersByRole(), getRolesForUser(), getRolesFromByteMap(), getByteMapFromRoles(), getEnabledFunctionsInTarget(), getRoleName(), setRoleName()
13: contract Governor is RolesAuthority {
```

- *HintHelpers.sol* ( [11](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L11) ):

```solidity
/// @audit getRedemptionHints(), getApproxHint(), computeNominalCR(), computeCR(), NAME, sortedCdps, cdpManager
11: contract HintHelpers is EbtcBase {
```

- *IActivePool.sol* ( [7](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IActivePool.sol#L7) ):

```solidity
/// @audit transferSystemCollShares(), increaseSystemCollShares(), transferSystemCollSharesAndLiquidatorReward(), allocateSystemCollSharesToFeeRecipient(), claimFeeRecipientCollShares(), feeRecipientAddress(), getFeeRecipientClaimableCollShares(), setFeeRecipientAddress()
7: interface IActivePool is IPool {
```

- *IBorrowerOperations.sol* ( [7](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7) ):

```solidity
/// @audit openCdp(), openCdpFor(), addColl(), withdrawColl(), withdrawDebt(), repayDebt(), closeCdp(), adjustCdp(), adjustCdpWithColl(), claimSurplusCollShares(), feeRecipientAddress()
7: interface IBorrowerOperations is IPositionManagers {
```

- *ICdpManager.sol* ( [9](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManager.sol#L9) ):

```solidity
/// @audit getActiveCdpsCount(), getIdFromCdpIdsArray(), liquidate(), partiallyLiquidate(), batchLiquidateCdps(), redeemCollateral(), updateStakeAndTotalStakes(), syncAccounting(), closeCdp(), getRedemptionRate(), getRedemptionRateWithDecay(), getRedemptionFeeWithDecay(), getCdpStatus(), getCdpStake(), getCdpDebt(), getCdpCollShares(), getCdpLiquidatorRewardShares(), initializeCdp(), updateCdp(), getCachedTCR(), checkRecoveryMode()
9: interface ICdpManager is IEbtcBase, ICdpManagerData {
```

- *ICdpManagerData.sol* ( [13](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13) ):

```solidity
/// @audit totalStakes(), ebtcToken(), systemStEthFeePerUnitIndex(), systemStEthFeePerUnitIndexError(), stEthIndex(), calcFeeUponStakingReward(), syncGlobalAccounting(), syncGlobalAccountingAndGracePeriod(), getAccumulatedFeeSplitApplied(), getCachedNominalICR(), getCachedICR(), getSyncedCdpDebt(), getSyncedCdpCollShares(), getSyncedICR(), getSyncedTCR(), getSyncedNominalICR(), getPendingRedistributedDebt(), hasPendingRedistributedDebt(), getSyncedDebtAndCollShares(), canLiquidateRecoveryMode()
13: interface ICdpManagerData is IRecoveryModeGracePeriod {
```

- *ICollSurplusPool.sol* ( [5](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5) ):

```solidity
/// @audit getTotalSurplusCollShares(), getSurplusCollShares(), increaseSurplusCollShares(), claimSurplusCollShares(), increaseTotalSurplusCollShares()
5: interface ICollSurplusPool {
```

- *IEBTCToken.sol* ( [8](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8) ):

```solidity
/// @audit mint(), burn()
8: interface IEBTCToken is IERC20, IERC2612 {
```

- *IERC3156FlashLender.sol* ( [7](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7) ):

```solidity
/// @audit maxFlashLoan(), flashFee(), flashLoan()
7: interface IERC3156FlashLender {
```

- *IFallbackCaller.sol* ( [5](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5) ):

```solidity
/// @audit getFallbackResponse(), fallbackTimeout(), setFallbackTimeout()
5: interface IFallbackCaller {
```

- *IPermitNonce.sol* ( [5](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5) ):

```solidity
/// @audit increasePermitNonce(), nonces()
5: interface IPermitNonce {
```

- *IPool.sol* ( [6](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPool.sol#L6) ):

```solidity
/// @audit getSystemCollShares(), getSystemDebt(), increaseSystemDebt(), decreaseSystemDebt()
6: interface IPool {
```

- *IPositionManagers.sol* ( [5](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5) ):

```solidity
/// @audit getPositionManagerApproval(), setPositionManagerApproval(), revokePositionManagerApproval(), renouncePositionManagerApproval(), permitPositionManagerApproval(), version(), permitTypeHash(), domainSeparator()
5: interface IPositionManagers {
```

- *IRecoveryModeGracePeriod.sol* ( [5](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5) ):

```solidity
/// @audit notifyStartGracePeriod(), notifyEndGracePeriod()
5: interface IRecoveryModeGracePeriod {
```

- *ISortedCdps.sol* ( [6](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6) ):

```solidity
/// @audit remove(), batchRemove(), reInsert(), contains(), isFull(), isEmpty(), getSize(), getMaxSize(), getFirst(), getLast(), getNext(), getPrev(), validInsertPosition(), findInsertPosition(), insert(), getOwnerAddress(), nonExistId(), cdpCountOf(), getCdpCountOf(), getCdpsOf(), getAllCdpsOf(), cdpOfOwnerByIndex(), cdpOfOwnerByIdx()
6: interface ISortedCdps {
```

- *LeverageMacroBase.sol* ( [26](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L26) ):

```solidity
/// @audit owner(), doOperation(), sweepToCaller(), sweepToken(), decodeFLData(), onFlashLoan(), borrowerOperations, activePool, cdpManager, ebtcToken, sortedCdps, stETH
26: contract LeverageMacroBase {
```

- *LeverageMacroFactory.sol* ( [11](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L11) ):

```solidity
/// @audit deployNewMacro(), deployNewMacro(), borrowerOperations, activePool, cdpManager, ebtcToken, stETH, sortedCdps
11: contract LeverageMacroFactory {
```

- *LeverageMacroReference.sol* ( [11](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L11) ):

```solidity
/// @audit owner(), resetApprovals()
11: contract LeverageMacroReference is LeverageMacroBase {
```

- *LiquidationLibrary.sol* ( [13](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L13) ):

```solidity
/// @audit liquidate(), partiallyLiquidate(), batchLiquidateCdps()
13: contract LiquidationLibrary is CdpManagerStorage {
```

- *PriceFeed.sol* ( [21](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L21) ):

```solidity
/// @audit fetchPrice(), setFallbackCaller(), NAME, ETH_BTC_CL_FEED, STETH_ETH_CL_FEED, fallbackCaller, TIMEOUT_ETH_BTC_FEED, TIMEOUT_STETH_ETH_FEED, MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND, MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES, lastGoodPrice, status
21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {
```

- *SimplifiedDiamondLike.sol* ( [25](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L25) ):

```solidity
/// @audit setFallbackHandler(), setAllowAnyCall(), enableCallbackForCall(), execute(), owner
25: contract SimplifiedDiamondLike {
```

- *SortedCdps.sol* ( [51](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L51) ):

```solidity
/// @audit toCdpId(), getOwnerAddress(), nonExistId(), cdpOfOwnerByIndex(), cdpOfOwnerByIdx(), cdpCountOf(), getCdpCountOf(), getCdpsOf(), getAllCdpsOf(), insert(), remove(), batchRemove(), reInsert(), contains(), isFull(), isEmpty(), getSize(), getMaxSize(), getFirst(), getLast(), getNext(), getPrev(), validInsertPosition(), findInsertPosition(), NAME, borrowerOperationsAddress, cdpManager, maxSize, data, nextCdpNonce, dummyId
51: contract SortedCdps is ISortedCdps {
```

</details>

### [G&#x2011;31] Reduce gas usage by moving to Solidity 0.8.19 or later

Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

<details>
<summary>There are 39 instances (click to show):</summary>

- *ActivePool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *BorrowerOperations.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *CdpManager.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *CdpManagerStorage.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *CollSurplusPool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *Auth.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *AuthNoOwner.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *ERC3156FlashLender.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *EbtcBase.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *EbtcMath.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ReentrancyGuard.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *RolesAuthority.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *EBTCToken.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *Governor.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *HintHelpers.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IActivePool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IActivePool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IBorrowerOperations.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ICdpManager.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ICdpManagerData.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ICollSurplusPool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IEBTCToken.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IERC3156FlashBorrower.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IERC3156FlashLender.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IEbtcBase.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IFallbackCaller.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPermitNonce.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPositionManagers.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPriceFeed.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IRecoveryModeGracePeriod.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *ISortedCdps.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *LeverageMacroBase.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LeverageMacroDelegateTarget.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LeverageMacroFactory.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LeverageMacroReference.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LiquidationLibrary.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *PriceFeed.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *SimplifiedDiamondLike.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *SortedCdps.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

</details>

### [G&#x2011;32] Newer versions of solidity are more gas efficient

The solidity language continues to pursue more efficient gas optimization schemes. Adopting a [newer version of solidity](https://github.com/ethereum/solc-js/tags) can be more gas efficient.

<details>
<summary>There are 39 instances (click to show):</summary>

- *ActivePool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *BorrowerOperations.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *CdpManager.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *CdpManagerStorage.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *CollSurplusPool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *Auth.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *AuthNoOwner.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *ERC3156FlashLender.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *EbtcBase.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *EbtcMath.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ReentrancyGuard.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *RolesAuthority.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *EBTCToken.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *Governor.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *HintHelpers.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IActivePool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IActivePool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IBorrowerOperations.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ICdpManager.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManager.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ICdpManagerData.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *ICollSurplusPool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IEBTCToken.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IERC3156FlashBorrower.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IERC3156FlashLender.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IEbtcBase.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IFallbackCaller.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPermitNonce.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPool.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPool.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPositionManagers.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IPriceFeed.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *IRecoveryModeGracePeriod.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *ISortedCdps.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *LeverageMacroBase.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LeverageMacroDelegateTarget.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LeverageMacroFactory.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LeverageMacroReference.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroReference.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *LiquidationLibrary.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *PriceFeed.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

- *SimplifiedDiamondLike.sol* ( [2](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L2) ):

```solidity
2: pragma solidity 0.8.17;
```

- *SortedCdps.sol* ( [3](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L3) ):

```solidity
3: pragma solidity 0.8.17;
```

</details>

### [G&#x2011;33] Avoid updating storage when the value hasn't changed

Manipulating storage in solidity is gas-intensive. It can be optimized by avoiding unnecessary storage updates when the new value equals the existing value.
If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (**2900 gas**), potentially at the expense of a Gcoldsload (**2100 gas**) or a Gwarmaccess (**100 gas**).

<details>
<summary>There are 37 instances (click to show):</summary>

- *ActivePool.sol* ( [171](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L171), [199](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L199), [212](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L212), [246](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L246), [398](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L398), [420](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L420) ):

```solidity
171:         feeRecipientCollShares = cachedFeeRecipientCollShares;

199:         systemDebt = cachedSystemDebt;

212:         systemDebt = cachedSystemDebt;

246:         systemCollShares = cachedSystemCollShares;

398:         feeRecipientAddress = _feeRecipientAddress;

420:         flashLoansPaused = _paused;
```

- *BorrowerOperations.sol* ( [640](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L640), [1148](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1148), [1170](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1170) ):

```solidity
640:         positionManagers[_borrower][_positionManager] = _approval;

1148:         feeRecipientAddress = _feeRecipientAddress;

1170:         flashLoansPaused = _paused;
```

- *CdpManager.sol* ( [629](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L629), [680](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L680), [781](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L781), [800](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L800), [823](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L823), [835](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L835), [847](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L847), [919](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L919) ):

```solidity
629:         baseRate = newBaseRate;

680:         baseRate = decayedBaseRate;

781:         stakingRewardSplit = _stakingRewardSplit;

800:         redemptionFeeFloor = _redemptionFeeFloor;

823:         minuteDecayFactor = _minuteDecayFactor;

835:         beta = _beta;

847:         redemptionsPaused = _paused;

919:         cdpStEthFeePerUnitIndex[_cdpId] = systemStEthFeePerUnitIndex; /// @audit We critically assume global accounting is synced here
```

- *CdpManagerStorage.sol* ( [53](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L53), [118](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L118), [295](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L295), [298](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L298), [339](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L339), [412](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L412), [423](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L423), [479](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L479), [541](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L541), [582](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L582) ):

```solidity
53:             lastGracePeriodStartTimestamp = uint128(block.timestamp);

118:         recoveryModeGracePeriodDuration = _gracePeriod;

295:         totalStakesSnapshot = _totalStakesSnapshot;

298:         totalCollateralSnapshot = _totalCollateralSnapshot;

339:         cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex;

412:         totalStakes = _newTotalStakes;

423:         totalStakes = _newTotalStakes;

479:         CdpIds[index] = idToMove;

541:             stEthIndex = _newIndex;

582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;
```

- *Auth.sol* ( [47](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L47), [53](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L53) ):

```solidity
47:         authority = newAuthority;

53:         owner = newOwner;
```

- *AuthNoOwner.sol* ( [43](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L43), [59](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L59) ):

```solidity
43:         _authority = Authority(newAuthority);

59:         _authority = Authority(newAuthority);
```

- *EBTCToken.sol* ( [289](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L289) ):

```solidity
289:         _allowances[owner][spender] = amount;
```

- *Governor.sol* ( [155](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L155) ):

```solidity
155:         roleNames[role] = roleName;
```

- *PriceFeed.sol* ( [377](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L377), [386](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L386), [547](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L547), [554](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L554) ):

```solidity
377:                     fallbackCaller = newFallbackCaler;

386:             fallbackCaller = newFallbackCaler;

547:         status = _status;

554:         lastGoodPrice = _currentPrice;
```

</details>

### [G&#x2011;34] Same cast is done multiple times

It's cheaper to do it once, and store the result to a variable. The examples below are the second+ instance of a given cast of the variable.

There are 4 instances:

- *RolesAuthority.sol* ( [114](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L114), [120](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L120), [155](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L155) ):

```solidity
114:             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

120:             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);

155:             getUserRoles[user] &= ~bytes32(1 << role);
```

- *Governor.sol* ( [108](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L108) ):

```solidity
108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
```

### [G&#x2011;35] `require()` or `revert()` statements that check input arguments should be at the top of the function

Checks that involve constants should come before checks that involve state variables, function calls, and calculations. By doing these checks first, the function is able to revert before wasting a Gcoldsload (**2100 gas***) in a function that may ultimately revert in the unhappy case.

There are 6 instances:

- *ActivePool.sol* ( [374](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L374), [393-396](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L393-L396), [407](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L407) ):

```solidity
/// @audit should check before line 372
374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

/// @audit should check before line 391
393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );

/// @audit should check before line 405
407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");
```

- *SortedCdps.sol* ( [369](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L369), [371](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L371), [508](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L508) ):

```solidity
/// @audit should check before line 365
369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

/// @audit should check before line 365
371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

/// @audit should check before line 504
508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");
```

### [G&#x2011;36] Contracts can use fewer storage slots by truncating state variables

Some state variables can be safely modified so that the contract uses fewer storage slots. Each saved slot can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

<details>
<summary>There is 1 instance (click to show):</summary>

- *CdpManagerStorage.sol* ( [19](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L19) ):

```solidity
/// @audit Truncate `lastGracePeriodStartTimestamp` to `uint32`
/// @audit Truncate `recoveryModeGracePeriodDuration` to `uint32`
/// @audit Truncate `minuteDecayFactor` to `uint32`
/// @audit Truncate `baseRate` to `uint32`
/// @audit Truncate `lastRedemptionTimestamp` to `uint32`
/// @audit Fewer storage usage (20 slots -> 16 slots):
///        32 B: uint256 redemptionFeeFloor
///        32 B: uint256 beta
///        32 B: uint256 stakingRewardSplit
///        32 B: mapping(bytes32 => Cdp) Cdps
///        32 B: uint256 totalStakes
///        32 B: uint256 totalStakesSnapshot
///        32 B: uint256 totalCollateralSnapshot
///        32 B: uint256 systemDebtRedistributionIndex
///        32 B: mapping(bytes32 => uint256) cdpDebtRedistributionIndex
///        32 B: uint256 lastEBTCDebtErrorRedistribution
///        32 B: uint256 stEthIndex
///        32 B: uint256 systemStEthFeePerUnitIndex
///        32 B: uint256 systemStEthFeePerUnitIndexError
///        32 B: mapping(bytes32 => uint256) cdpStEthFeePerUnitIndex
///        32 B: bytes32[] CdpIds
///        4 B: uint32 lastGracePeriodStartTimestamp
///        4 B: uint32 recoveryModeGracePeriodDuration
///        4 B: uint32 minuteDecayFactor
///        4 B: uint32 baseRate
///        4 B: uint32 lastRedemptionTimestamp
///        1 B: bool redemptionsPaused
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {
```

</details>

### [G&#x2011;37] Structs can be packed into fewer storage slots by truncating fields

Some struct fields  can be safely modified so that the struct variable uses fewer storage slots. Each saved slot can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

<details>
<summary>There are 2 instances (click to show):</summary>

- *IPriceFeed.sol* ( [17-24](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24), [26-30](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30) ):

```solidity
/// @audit Truncate `timestampEthBtc` to `uint32`
/// @audit Truncate `timestampStEthEth` to `uint32`
/// @audit Fewer storage usage (5 slots -> 2 slots):
///        32 B: uint256 answer
///        10 B: uint80 roundEthBtcId
///        10 B: uint80 roundStEthEthId
///        4 B: uint32 timestampEthBtc
///        4 B: uint32 timestampStEthEth
///        1 B: bool success
17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }

/// @audit Truncate `timestamp` to `uint32`
/// @audit Fewer storage usage (3 slots -> 2 slots):
///        32 B: uint256 answer
///        4 B: uint32 timestamp
///        1 B: bool success
26:     struct FallbackResponse {
27:         uint256 answer;
28:         uint256 timestamp;
29:         bool success;
30:     }
```

</details>

### [G&#x2011;38] Redundant state variable getters

Getters for public state variables are automatically generated so there is no need to code them manually and waste gas.

There are 2 instances:

- *SortedCdps.sol* ( [130-132](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L130-L132), [548-550](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L548-L550) ):

```solidity
130:     function nonExistId() public pure override returns (bytes32) {
131:         return dummyId;
132:     }

548:     function getMaxSize() external view override returns (uint256) {
549:         return maxSize;
550:     }
```

### [G&#x2011;39] Refactor duplicated `require()`/`revert()` checks to save gas

Duplicate `require()`/`revert()` checks can be refactored into a modifier or function, saving deployment costs.

There are 4 instances:

- *ActivePool.sol* ( [137](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L137) ):

```solidity
/// @audit Duplicated on line 162
137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");
```

- *RolesAuthority.sol* ( [90-93](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90-L93) ):

```solidity
/// @audit Duplicated on line 134
90:         require(
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
92:             "RolesAuthority: Capability Burned"
93:         );
```

- *SimplifiedDiamondLike.sol* ( [52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52) ):

```solidity
/// @audit Duplicated on line 67
52:         require(msg.sender == owner);
```

- *SortedCdps.sol* ( [458](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L458) ):

```solidity
/// @audit Duplicated on line 506
458:         require(contains(_id), "SortedCdps: List does not contain the id");
```

### [G&#x2011;40] Using `constant`s instead of `enum` can save gas

`Enum` is expensive and it is [more efficient to use constants](https://www.codehawks.com/finding/clm84992q02j9w9ruebun36d9) instead. An illustrative example of this approach can be found in the [ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/181d518609a9f006fcb97af63e6952e603cf100e/contracts/utils/ReentrancyGuard.sol#L34-L35).

<details>
<summary>There are 9 instances (click to show):</summary>

- *ICdpManagerData.sol* ( [77-86](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L77-L86), [88-94](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L88-L94) ):

```solidity
77:     enum CdpOperation {
78:         openCdp,
79:         closeCdp,
80:         adjustCdp,
81:         syncAccounting,
82:         liquidateInNormalMode,
83:         liquidateInRecoveryMode,
84:         redeemCollateral,
85:         partiallyLiquidate
86:     }

88:     enum Status {
89:         nonExistent,
90:         active,
91:         closedByOwner,
92:         closedByLiquidation,
93:         closedByRedemption
94:     }
```

- *IPositionManagers.sol* ( [6-10](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPositionManagers.sol#L6-L10) ):

```solidity
6:     enum PositionManagerApproval {
7:         None,
8:         OneTime,
9:         Persistent
10:     }
```

- *IPriceFeed.sol* ( [34-40](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L34-L40) ):

```solidity
34:     enum Status {
35:         chainlinkWorking,
36:         usingFallbackChainlinkUntrusted,
37:         bothOraclesUntrusted,
38:         usingFallbackChainlinkFrozen,
39:         usingChainlinkFallbackUntrusted
40:     }
```

- *LeverageMacroBase.sol* ( [70-74](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L70-L74), [76-80](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L76-L80), [82-87](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L82-L87), [284-288](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L284-L288) ):

```solidity
70:     enum FlashLoanType {
71:         stETH,
72:         eBTC,
73:         noFlashloan // Use this to not perform a FL and just `doOperation`
74:     }

76:     enum PostOperationCheck {
77:         openCdp,
78:         cdpStats,
79:         isClosed
80:     }

82:     enum Operator {
83:         skip,
84:         equal,
85:         gte,
86:         lte
87:     }

284:     enum OperationType {
285:         OpenCdpOperation,
286:         AdjustCdpOperation,
287:         CloseCdpOperation
288:     }
```

- *SimplifiedDiamondLike.sol* ( [94-97](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L94-L97) ):

```solidity
94:     enum OperationType {
95:         call,
96:         delegatecall
97:     }
```

</details>

### [G&#x2011;41] Use assembly to emit events

To efficiently emit events, it's possible to utilize assembly by making use of scratch space and the free memory pointer. This approach has the advantage of potentially avoiding the costs associated with memory expansion.

However, it's important to note that in order to safely optimize this process, it is preferable to cache and restore the free memory pointer.

A good example of such practice can be seen in [Solady's](https://github.com/Vectorized/solady/blob/main/src/tokens/ERC1155.sol#L167) codebase.

<details>
<summary>There are 71 instances (click to show):</summary>

- *ActivePool.sol* ( [65](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L65), [112](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L112), [113](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L113), [145](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L145), [146](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L146), [173](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L173), [174](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L174), [200](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L200), [213](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L213), [247](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L247), [307](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L307), [360](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L360), [383](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L383), [399](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L399), [412](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L412), [421](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L421) ):

```solidity
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

- *BorrowerOperations.sol* ( [136](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L136), [641](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L641), [1105](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1105), [1149](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1149), [1162](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1162), [1171](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1171) ):

```solidity
136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1171:         emit FlashLoansPaused(msg.sender, _paused);
```

- *CdpManager.sol* ( [55](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L55), [630](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L630), [681](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L681), [698](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L698), [782](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L782), [801](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L801), [824](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L824), [836](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L836), [848](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L848) ):

```solidity
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

- *CdpManagerStorage.sol* ( [50](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L50), [55](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L55), [64](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L64), [69](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L69), [119](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L119), [300](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L300), [340](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L340), [414](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L414), [425](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L425), [481](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L481) ):

```solidity
50:         emit TCRNotified(_tcr);

55:             emit GracePeriodStart();

64:         emit TCRNotified(_tcr);

69:             emit GracePeriodEnd();

119:         emit GracePeriodDurationSet(_gracePeriod);

300:         emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);

340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

414:         emit TotalStakesUpdated(_newTotalStakes);

425:         emit TotalStakesUpdated(_newTotalStakes);

481:         emit CdpArrayIndexUpdated(idToMove, index);
```

- *CollSurplusPool.sol* ( [83](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L83), [95](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L95), [104](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L104), [150](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L150) ):

```solidity
83:         emit SurplusCollSharesUpdated(_account, newAmount);

95:         emit SurplusCollSharesUpdated(_account, 0);

104:         emit CollSharesTransferred(_account, claimableColl);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);
```

- *Auth.sol* ( [22](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L22), [23](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L23), [49](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L49), [55](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/Auth.sol#L55) ):

```solidity
22:         emit OwnershipTransferred(msg.sender, _owner);

23:         emit AuthorityUpdated(msg.sender, _authority);

49:         emit AuthorityUpdated(msg.sender, newAuthority);

55:         emit OwnershipTransferred(msg.sender, newOwner);
```

- *AuthNoOwner.sol* ( [50](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50), [62](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62) ):

```solidity
50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));
```

- *RolesAuthority.sol* ( [101](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101), [129](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L129), [140](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L140), [163](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L163) ):

```solidity
101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140:         emit CapabilityBurned(target, functionSig);

163:         emit UserRoleUpdated(user, role, enabled);
```

- *EBTCToken.sol* ( [259](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L259), [267](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L267), [282](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L282), [290](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L290) ):

```solidity
259:         emit Transfer(sender, recipient, amount);

267:         emit Transfer(address(0), account, amount);

282:         emit Transfer(account, address(0), amount);

290:         emit Approval(owner, spender, amount);
```

- *Governor.sol* ( [157](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L157) ):

```solidity
157:         emit RoleNameSet(role, roleName);
```

- *LeverageMacroFactory.sol* ( [56](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroFactory.sol#L56) ):

```solidity
56:         emit DeployNewMacro(_owner, addy);
```

- *LiquidationLibrary.sol* ( [891](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L891) ):

```solidity
891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);
```

- *PriceFeed.sol* ( [67](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L67), [378](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L378), [381](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L381), [387](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L387), [548](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L548), [555](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L555) ):

```solidity
67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

548:         emit PriceFeedStatusChanged(_status);

555:         emit LastGoodPriceUpdated(_currentPrice);
```

- *SortedCdps.sol* ( [405](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L405), [451](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L451), [490](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L490) ):

```solidity
405:         emit NodeAdded(_id, _NICR);

451:             emit NodeRemoved(_ids[i]);

490:         emit NodeRemoved(_id);
```

</details>

### [G&#x2011;42] Use assembly to compute hashes to save gas

If the arguments to the encode call can fit into the scratch space (two words or fewer), then it's more efficient to use assembly to generate the hash (**80 gas**):

`keccak256(abi.encodePacked(x, y))` -> `assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }`

There is 1 instance:

- *HintHelpers.sol* ( [182](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L182) ):

```solidity
182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));
```

### [G&#x2011;43] Consider activating via-ir for deploying

By using `--via-ir` or `{"viaIR": true}`, the compiler is able to use more advanced [multi-function optimizations](https://docs.soliditylang.org/en/v0.8.17/ir-breaking-changes.html#solidity-ir-based-codegen-changes), for extra gas savings.

There is 1 instance:

- Global finding

### [G&#x2011;44] Multiple accesses of the same mapping/array key/index should be cached

The instances below point to the second+ access of a value inside a mapping/array, within a function. Caching a mapping's value in a local `storage` or `calldata` variable when the value is accessed [multiple times](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0), saves **~42 gas per access** due to not having to recalculate the key's keccak256 hash (Gkeccak256 - **30 gas**) and that calculation's associated stack operations. Caching an array's struct avoids recalculating the array offsets into memory/calldata

<details>
<summary>There are 36 instances (click to show):</summary>

- *CdpManager.sol* ( [151](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L151), [914](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L914) ):

```solidity
/// @audit `Cdps[_redeemColFromCdp.cdpId]` is also accessed on line 152, 142, 216, 217, 228, 164
151:             Cdps[_redeemColFromCdp.cdpId].debt,

/// @audit `Cdps[_cdpId]` is also accessed on line 915, 916, 917
914:         Cdps[_cdpId].debt = _debt;
```

- *CdpManagerStorage.sol* ( [271](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L271), [350](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L350), [411](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L411), [464](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L464), [621](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L621) ):

```solidity
/// @audit `Cdps[_cdpId]` is also accessed on line 272, 273, 274
271:         Cdps[_cdpId].status = closedStatus;

/// @audit `cdpStEthFeePerUnitIndex[_cdpId]` is also accessed on line 405
350:         uint256 _oldPerUnitCdp = cdpStEthFeePerUnitIndex[_cdpId];

/// @audit `Cdps[_cdpId]` is also accessed on line 413
411:         uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake;

/// @audit `Cdps[_cdpId]` is also accessed on line 471
464:         Status cdpStatus = Cdps[_cdpId].status;

/// @audit `Cdps[_cdpId]` is also accessed on line 631
621:         uint256 _cdpCol = Cdps[_cdpId].coll;
```

- *CollSurplusPool.sol* ( [80](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L80), [91](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L91) ):

```solidity
/// @audit `balances[_account]` is also accessed on line 81
80:         uint256 newAmount = balances[_account] + _amount;

/// @audit `balances[_account]` is also accessed on line 94
91:         uint256 claimableColl = balances[_account];
```

- *RolesAuthority.sol* ( [91](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L91), [91](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L91), [120](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L120), [120](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L120), [121](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L121), [138](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L138), [138](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L138), [155](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L155) ):

```solidity
/// @audit `capabilityFlag[target][functionSig]` is also accessed on line 98, 96
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,

/// @audit `capabilityFlag[target]` is also accessed on line 98, 96
91:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,

/// @audit `getRolesWithCapability[target][functionSig]` is also accessed on line 113
120:             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);

/// @audit `getRolesWithCapability[target]` is also accessed on line 113
120:             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);

/// @audit `enabledFunctionSigsByTarget[target]` is also accessed on line 114, 124
121:             enabledFunctionSigsByTarget[target].remove(bytes32(functionSig));

/// @audit `capabilityFlag[target][functionSig]` is also accessed on line 135
138:         capabilityFlag[target][functionSig] = CapabilityFlag.Burned;

/// @audit `capabilityFlag[target]` is also accessed on line 135
138:         capabilityFlag[target][functionSig] = CapabilityFlag.Burned;

/// @audit `getUserRoles[user]` is also accessed on line 158, 149
155:             getUserRoles[user] &= ~bytes32(1 << role);
```

- *EBTCToken.sol* ( [250](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L250), [258](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L258), [266](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L266), [273](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L273) ):

```solidity
/// @audit `_balances[sender]` is also accessed on line 255
250:         uint256 cachedSenderBalances = _balances[sender];

/// @audit `_balances[recipient]` is also accessed on line 258
258:         _balances[recipient] = _balances[recipient] + amount;

/// @audit `_balances[account]` is also accessed on line 266
266:         _balances[account] = _balances[account] + amount;

/// @audit `_balances[account]` is also accessed on line 278
273:         uint256 cachedBalance = _balances[account];
```

- *LiquidationLibrary.sol* ( [496](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LiquidationLibrary.sol#L496) ):

```solidity
/// @audit `Cdps[_cdpId]` is also accessed on line 497, 498
496:             Cdps[_cdpId].debt,
```

</details>

### [G&#x2011;45] Multiple mappings can be replaced with a single struct mapping

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (**20000 gas**) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save **~42 gas per access** due to [not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0) (Gkeccak256 - 30 gas) and that calculation's associated stack operations.

There are 5 instances:

- *CdpManagerStorage.sol* ( [168](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L168), [190](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L190), [202](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L202) ):

```solidity
168:     mapping(bytes32 => Cdp) public Cdps;

190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;
```

- *EBTCToken.sol* ( [51](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L51), [52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L52) ):

```solidity
51:     mapping(address => uint256) private _balances;

52:     mapping(address => mapping(address => uint256)) private _allowances;
```

### [G&#x2011;46] Consider using `bytes32` rather than a `string`

Using the `bytes` types for fixed-length strings is more efficient than having the EVM have to incur the overhead of string processing. Consider whether the value _needs_ to be a `string`. A good reason to keep it as a `string` would be if the variable is defined in an interface that this project does not own.

<details>
<summary>There are 11 instances (click to show):</summary>

- *ActivePool.sol* ( [24](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L24) ):

```solidity
24:     string public constant NAME = "ActivePool";
```

- *BorrowerOperations.sol* ( [29](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L29), [41](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L41) ):

```solidity
29:     string public constant NAME = "BorrowerOperations";

41:     string internal constant _VERSION = "1";
```

- *CdpManagerStorage.sol* ( [122](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L122) ):

```solidity
122:     string public constant NAME = "CdpManager";
```

- *CollSurplusPool.sol* ( [19](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CollSurplusPool.sol#L19) ):

```solidity
19:     string public constant NAME = "CollSurplusPool";
```

- *EBTCToken.sol* ( [28](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L28), [29](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L29), [30](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L30) ):

```solidity
28:     string internal constant _NAME = "EBTC Stablecoin";

29:     string internal constant _SYMBOL = "EBTC";

30:     string internal constant _VERSION = "1";
```

- *HintHelpers.sol* ( [12](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L12) ):

```solidity
12:     string public constant NAME = "HintHelpers";
```

- *PriceFeed.sol* ( [22](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L22) ):

```solidity
22:     string public constant NAME = "PriceFeed";
```

- *SortedCdps.sol* ( [52](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L52) ):

```solidity
52:     string public constant NAME = "SortedCdps";
```

</details>

