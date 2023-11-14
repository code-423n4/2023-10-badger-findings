## Gas Optimizations


| |Issue|Instances|Estimated Gas Saved|
|-|:-|:-:|-:|
| [GAS-1](#GAS-1) | 'Don't compare boolean expressions to boolean literals' | 1 | 9 |
| [GAS-2](#GAS-2) | Increments can be unchecked to save gas | 11 | 660 |
| [GAS-3](#GAS-3) | `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants) | 2 | 76 |
| [GAS-4](#GAS-4) | Avoid emitting storage values | 2 | - |
| [GAS-5](#GAS-5) |  Avoid updating storage when the value hasn’t changed | 63 | 50400 |
| [GAS-6](#GAS-6) | Using this to access functions results in an external call, wasting gas | 6 | 600 |
| [GAS-7](#GAS-7) | Using bools for storage incurs overhead | 4 | 400 |
| [GAS-8](#GAS-8) | bytes constants are more efficient than string constants | 11 | - |
| [GAS-9](#GAS-9) | Cache array length outside of loop | 5 | 15 |
| [GAS-10](#GAS-10) | Multiple accesses of the same mapping/array key/index should be cached | 12 | 504 |
| [GAS-11](#GAS-11) | The result of a function call should be cached rather than re-calling the function | 35 | 3500 |
| [GAS-12](#GAS-12) | State variables that are used multiple times in a function should be cached in stack variables | 69 | 6900 |
| [GAS-13](#GAS-13) | Use calldata instead of memory for function arguments that do not get mutated | 6 | 1800 |
| [GAS-14](#GAS-14) | Gas savings can be achieved by changing the model for assigning value to the structure | 8 | 2080 |
| [GAS-15](#GAS-15) | Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate | 6 | - |
| [GAS-16](#GAS-16) | Consider activating via-ir for deploying | 1 | - |
| [GAS-17](#GAS-17) | Expressions for constant values such as a call to keccak256(), should use immutable rather than constant | 7 | - |
| [GAS-18](#GAS-18) | Constructors can be marked as payable to save deployment gas | 19 | 399 |
| [GAS-19](#GAS-19) | Use custom errors rather than revert()/require() strings to save gas | 150 | 7500 |
| [GAS-20](#GAS-20) | ++i costs less gas than i++, especially when its used in for loops | 7 | 35 |
| [GAS-21](#GAS-21) | Division by powers of two should use bit shifting | 3 | 60 |
| [GAS-22](#GAS-22) | Do not shrink Variables | 30 | - |
| [GAS-23](#GAS-23) | Empty blocks should be removed or emit something | 1 | - |
| [GAS-24](#GAS-24) | Events should be emitted outside of loops | 1 | - |
| [GAS-25](#GAS-25) |  >=/<= costs less gas than >/< | 63 | 189 |
| [GAS-26](#GAS-26) | keccak256() hash of literals should only be computed once | 4 | 168 |
| [GAS-27](#GAS-27) | Don't initialize variables with default value | 19 | - |
| [GAS-28](#GAS-28) | internal functions only called once can be inlined to save gas | 75 | 1500 |
| [GAS-29](#GAS-29) | A modifier used only once and not being inherited should be inlined to save gas | 1 | - |
| [GAS-30](#GAS-30) | Private functions only used once can be inlined to save gas | 2 | 60 |
| [GAS-31](#GAS-31) | Usage of ints/uints smaller than 32 bytes incurs overhead | 70 | 3850 |
| [GAS-32](#GAS-32) | Long require/revert strings | 55 | 715 |
| [GAS-33](#GAS-33) | Reduce gas usage by moving to Solidity 0.8.19 or later | 39 | 39000 |
| [GAS-34](#GAS-34) | Using a nesting if statement instead of a logical AND(&&) | 14 | 84 |
| [GAS-35](#GAS-35) | Optimize names to save gas | 40 | 880 |
| [GAS-36](#GAS-36) | Operator += costs more gas than <x> = <x> + <y> for variables | 8 | 904 |
| [GAS-37](#GAS-37) | Using `private` rather than `public` for constants, saves gas | 31 | 105586 |
| [GAS-38](#GAS-38) | Change public state variable visibility to private | 42 | - |
| [GAS-39](#GAS-39) | Redundant state variable getters | 4 | - |
| [GAS-40](#GAS-40) | Duplicated require()/revert() checks should be refactored to a modifier Or function to save gas | 4 | - |
| [GAS-41](#GAS-41) | require() or revert() statements that check input arguments should be at the top of the function | 38 | - |
| [GAS-42](#GAS-42) | Same cast is done multiple times | 4 | - |
| [GAS-43](#GAS-43) | Use shift Right/Left instead of division/multiplication if possible | 3 | 60 |
| [GAS-44](#GAS-44) | State variable read in a loop | 21 | 2037 |
| [GAS-45](#GAS-45) | State variables only set in the constructor should be declared immutable  | 54 | 113238 |
| [GAS-46](#GAS-46) | State variables only set in their definitions should be declared constant | 6 | 12582 |
| [GAS-47](#GAS-47) | Use uint256(1)/uint256(2) instead of true/false to save gas for changes | 4 | 34200 |
| [GAS-48](#GAS-48) | Ternary unnecessary | 3 | - |
| [GAS-49](#GAS-49) | Use != 0 instead of > 0 for unsigned integer comparison | 53 | 212 |
| [GAS-50](#GAS-50) | Unused named return variables without optimizer waste gas | 9 | 81 |
| [GAS-51](#GAS-51) | Remove or replace unused state variables | 10 | - |
| [GAS-52](#GAS-52) | Using bitmap to store bool states can save gas | 1 | - |
| [GAS-53](#GAS-53) | Use constants instead of type(uintx).max | 20 | - |
| [GAS-54](#GAS-54) | Using delete instead of setting `info` struct to 0 saves gas | 5 | - |
| [GAS-55](#GAS-55) | Use do while loops instead of for loops | 15 | - |
| [GAS-56](#GAS-56) | unchecked {} can be used on the division of two uints in order to save gas | 35 | 700 |
| [GAS-57](#GAS-57) | Use unchecked block for safe subtractions | 22 | 1870 |
| [GAS-58](#GAS-58) | `internal` functions not called by the contract should be removed | 1 | - |
| [GAS-59](#GAS-59) | Use assembly to write address/contract type storage values | 26 | 1300 |
| [GAS-60](#GAS-60) | Use assembly to emit events | 57 | 2166 |
| [GAS-61](#GAS-61) | Use assembly to compute hashes to save gas | 9 | 720 |
| [GAS-62](#GAS-62) | Using assembly to check for zero can save gas | 55 | 330 |
| [GAS-63](#GAS-63) | Amounts should be checked for 0 before calling a transfer | 7 | - |

 Total: 1429 instances over 63 issues with *397370 gas* saved.

  ### <a name="GAS-1"></a>[GAS-1] 'Don't compare boolean expressions to boolean literals'
if (<x> == true) => if (<x>), if (<x> == false) => if (!<x>)

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

```

### <a name="GAS-2"></a>[GAS-2] Increments can be unchecked to save gas
Using unchecked increments can save gas by bypassing the built-in overflow checks. This can save 30-40 gas per iteration. So it is recommended to use unchecked increments when overflow is not possible.

 There are 11 instances:

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


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 438:             for (uint256 i; i < length; ++i) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 432:         for (uint256 i = 0; i < _len; ++i) {

 449:         for (uint i = 0; i < _len; ++i) {

```

### <a name="GAS-3"></a>[GAS-3] `array[index] += amount` is cheaper than `array[index] = array[index] + amount` (or related variants)
When updating a value in an array with arithmetic, using `array[index] += amount` is cheaper than `array[index] = array[index] + amount`.
This is because you avoid an additonal `mload` when the array is stored in memory, and an `sload` when the array is stored in storage.
This can be applied for any arithmetic operation including `+=`, `-=`,`/=`,`*=`,`^=`,`&=`, `%=`, `<<=`,`>>=`, and `>>>=`.
This optimization can be particularly significant if the pattern occurs during a loop.

*Saves 28 gas for a storage array, 38 for a memory array*

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/EBTCToken.sol

 258:         _balances[recipient] = _balances[recipient] + amount;

 266:         _balances[account] = _balances[account] + amount;

```

### <a name="GAS-4"></a>[GAS-4] Avoid emitting storage values
Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. We can avoid unecessary SLOADs by caching storage values that were previously accessed and emitting those cached values.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  cache sortedCdps
 390:             emit CdpUpdated(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  cache feeRecipientAddress
 150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```

### <a name="GAS-5"></a>[GAS-5]  Avoid updating storage when the value hasn’t changed
If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (2900 gas), potentially at the expense of a Gcoldsload (2100 gas) or a Gwarmaccess (100 gas)

 There are 63 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

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


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 1148:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 118:         recoveryModeGracePeriodDuration = _gracePeriod;

 271:         Cdps[_cdpId].status = closedStatus;

 272:         Cdps[_cdpId].coll = 0;

 273:         Cdps[_cdpId].debt = 0;

 274:         Cdps[_cdpId].liquidatorRewardShares = 0;

 276:         cdpDebtRedistributionIndex[_cdpId] = 0;

 277:         cdpStEthFeePerUnitIndex[_cdpId] = 0;

 295:         totalStakesSnapshot = _totalStakesSnapshot;

 298:         totalCollateralSnapshot = _totalCollateralSnapshot;

 339:         cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex;

 405:             cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex;

 412:         totalStakes = _newTotalStakes;

 413:         Cdps[_cdpId].stake = 0;

 423:         totalStakes = _newTotalStakes;

 479:         CdpIds[index] = idToMove;

 480:         Cdps[idToMove].arrayIndex = index;

 541:             stEthIndex = _newIndex;

 581:         systemStEthFeePerUnitIndex = _newPerUnit;

 582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;

 600:         Cdps[_cdpId].coll = _newColl;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 81:         balances[_account] = newAmount;

 94:         balances[_account] = 0;

 102:             totalSurplusCollShares = cachedTotalSurplusCollShares - claimableColl;

 132:         totalSurplusCollShares = totalSurplusCollShares + _value;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 47:         authority = newAuthority;

 53:         owner = newOwner;

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 43:         _authority = Authority(newAuthority);

 47:             _authorityInitialized = true;

 59:         _authority = Authority(newAuthority);

 60:         _authorityInitialized = true;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 255:             _balances[sender] = cachedSenderBalances - amount;

 258:         _balances[recipient] = _balances[recipient] + amount;

 265:         _totalSupply = _totalSupply + amount;

 266:         _balances[account] = _balances[account] + amount;

 278:             _balances[account] = cachedBalance - amount;

 281:         _totalSupply = _totalSupply - amount;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 155:         roleNames[role] = roleName;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 377:                     fallbackCaller = newFallbackCaler;

 386:             fallbackCaller = newFallbackCaler;

 547:         status = _status;

 554:         lastGoodPrice = _currentPrice;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 384:             data.head = _id;

 385:             data.tail = _id;

 390:             data.head = _id;

 395:             data.tail = _id;

 404:         data.size = data.size + 1;

 440:             data.head = _lastNext;

 445:             data.tail = _firstPrev;

 453:         data.size = data.size - _len;

 465:                 data.head = data.nodes[_id].nextId;

 471:                 data.tail = data.nodes[_id].prevId;

 484:             data.head = dummyId;

 485:             data.tail = dummyId;

```

### <a name="GAS-6"></a>[GAS-6] Using this to access functions results in an external call, wasting gas
External calls have an overhead of 100 gas, which can be avoided by not referencing the function using this. Contracts are allowed to override their parents functions and change the visibility from external to public, so make this change if its required in order to call the function internally.

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 73:         noFlashloan // Use this to not perform a FL and just `doOperation`

 456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 33:             true // Sweep to caller since this is not supposed to hold funds

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

```

### <a name="GAS-7"></a>[GAS-7] Using bools for storage incurs overhead
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 143:     bool public redemptionsPaused;

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 14:     bool private _authorityInitialized;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 15:     bool public flashLoansPaused;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 35:     bool internal immutable willSweep;

```

### <a name="GAS-8"></a>[GAS-8] bytes constants are more efficient than string constants
If the data can fit in 32 bytes, the bytes32 data type can be used instead of bytes or strings, as it is more gas efficient and less robust in terms of robustness.

 There are 11 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 24:     string public constant NAME = "ActivePool";

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 29:     string public constant NAME = "BorrowerOperations";

 41:     string internal constant _VERSION = "1";

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 122:     string public constant NAME = "CdpManager";

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 19:     string public constant NAME = "CollSurplusPool";

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 28:     string internal constant _NAME = "EBTC Stablecoin";

 29:     string internal constant _SYMBOL = "EBTC";

 30:     string internal constant _VERSION = "1";

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 12:     string public constant NAME = "HintHelpers";

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 22:     string public constant NAME = "PriceFeed";

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 52:     string public constant NAME = "SortedCdps";

```

### <a name="GAS-9"></a>[GAS-9] Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

 There are 5 instances:

 ```solidity
File: packages/contracts/contracts/Governor.sol

 46:         for (uint256 i = 0; i < users.length(); i++) {

 57:             for (uint256 i = 0; i < _usrs.length; i++) {

 122:         for (uint8 i = 0; i < roleIds.length; i++) {

 137:             for (uint256 i = 0; i < _sigs.length; ++i) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 292:         uint256 beforeSwapsLength = operation.swapsBefore.length;

```

### <a name="GAS-10"></a>[GAS-10] Multiple accesses of the same mapping/array key/index should be cached
The instances below point to the second+ access of a value inside a mapping/array, within a function. Caching a mapping’s value in a local storage or calldata variable when the value is accessed multiple times, saves ~42 gas per access due to not having to recalculate the key’s keccak256 hash (Gkeccak256 - 30 gas) and that calculation’s associated stack operations. Caching an array’s struct avoids recalculating the array offsets into memory/calldata

 There are 12 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 152:             Cdps[_redeemColFromCdp.cdpId].coll

 915:         Cdps[_cdpId].coll = _coll;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 471:         uint128 index = Cdps[_cdpId].arrayIndex;

 631:         uint256 _feeSplitDistributed = Cdps[_cdpId].stake *

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 98:             capabilityFlag[target][functionSig] = CapabilityFlag.None;

 113:             getRolesWithCapability[target][functionSig] |= bytes32(1 << role);

 114:             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

 135:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 497:             Cdps[_cdpId].coll,

 796:                     _liqFlags[vars.i] = true;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

```

### <a name="GAS-11"></a>[GAS-11] The result of a function call should be cached rather than re-calling the function
The function calls in solidity are expensive. If the same result of the same function calls are to be used several times, the result should be cached to reduce the gas consumption of repeated calls.

 There are 35 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

 62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 75:                 x = decMul(x, x);

 79:                 y = decMul(x, y);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 59:                 bool _canCall = doesUserHaveRole(user, role);

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 85:                 if (doesUserHaveRole(user, i)) {

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 156:                 IERC3156FlashBorrower(address(this)),

 189:             _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);

 190:             _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);

 427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 40:         stETH.approve(_borrowerOperationsAddress, type(uint256).max);

 54:         stETH.approve(address(borrowerOperations), type(uint256).max);

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 168:                 ) = _liquidateCdpInGivenMode(_liqState, _recoveryState);

 761:                     (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))

 783:                     _TCR = _computeTCRWithGivenSystemValues(

 791:                     _syncAccounting(vars.cdpId);

 795:                     totals = _addLiquidationValuesToTotals(totals, singleLiquidation);

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 126:                 _changeStatus(Status.usingFallbackChainlinkUntrusted);

 169:                 if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {

 202:             if (_fallbackIsBroken(fallbackResponse)) {

 240:                 _bothOraclesLiveAndUnbrokenAndSimilarPrice(

 246:                 _changeStatus(Status.chainlinkWorking);

 256:             if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {

 274:             if (_chainlinkIsFrozen(chainlinkResponse)) {

 292:                 _changeStatus(Status.usingChainlinkFallbackUntrusted);

 297:             if (_fallbackIsFrozen(fallbackResponse)) {

 310:             return _storeFallbackPrice(fallbackResponse);

 317:                 _changeStatus(Status.bothOraclesUntrusted);

 340:             if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {

 347:             return _storeChainlinkPrice(chainlinkResponse.answer);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 704:             return _descendList(_NICR, prevId);

```

### <a name="GAS-12"></a>[GAS-12] State variables that are used multiple times in a function should be cached in stack variables
When performing multiple operations on a state variable in a function, it is recommended to cache it first. Either multiple reads or multiple writes to a state variable can save gas by caching it on the stack. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses. Saves 100 gas per instance.

 There are 69 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 60:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());

 295:             collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

 303:             collateral.getPooledEthByShares(DECIMAL_PRECISION) == oldRate,

 337:         return collateral.balanceOf(address(this));

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 364:         vars.collShares = cdpManager.getCdpCollShares(_cdpId);

 422:             sortedCdps.reInsert(_cdpId, newNICR, _upperHint, _lowerHint);

 497:                 cdpManager.notifyStartGracePeriod(newTCR);

 583:         cdpManager.closeCdp(_cdpId, _borrower, debt, collShares);

 893:                 cdpManager.notifyStartGracePeriod(_vars.newTCR);

 1103:         ebtcToken.burn(feeRecipientAddress, amount);

 1103:         ebtcToken.burn(feeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 67:             lastGracePeriodStartTimestamp = UNSET_TIMESTAMP;

 454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

 454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

 483:         CdpIds.pop();

 631:         uint256 _feeSplitDistributed = Cdps[_cdpId].stake *

 774:             uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

 54:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

 57:         require(!_authorityInitialized, "Auth: authority already initialized");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

 65:             return DECIMAL_PRECISION;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 96:             capabilityFlag[target][functionSig] = CapabilityFlag.Public;

 113:             getRolesWithCapability[target][functionSig] |= bytes32(1 << role);

 117:                 targets.add(target);

 124:             if (enabledFunctionSigsByTarget[target].length() == 0) {

 135:             capabilityFlag[target][functionSig] != CapabilityFlag.Burned,

 152:                 users.add(user);

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 90:                 uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

 117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

 172:             return (sortedCdps.nonExistId(), 0, _inputRandomSeed);

 186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 143:             initialCdpIndex = sortedCdps.cdpCountOf(address(this));

 199:             ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);

 224:             ebtcToken.transfer(msg.sender, ebtcBal);

 228:             stETH.transferShares(msg.sender, collateralBal);

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 283:                     return lastGoodPrice;

 314:         if (status == Status.usingChainlinkFallbackUntrusted) {

 588:             try fallbackCaller.getFallbackResponse() returns (

 634:         try ETH_BTC_CL_FEED.latestRoundData() returns (

 650:         try STETH_ETH_CL_FEED.latestRoundData() returns (

 722:         try ETH_BTC_CL_FEED.getRoundData(_currentRoundEthBtcId - 1) returns (

 738:         try STETH_ETH_CL_FEED.getRoundData(_currentRoundStEthEthId - 1) returns (

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 181:         bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);

 199:             _currentCdpId = data.nodes[_currentCdpId].prevId;

 244:         bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);

 256:             _currentCdpId = data.nodes[_currentCdpId].prevId;

 275:             (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);

 316:         bytes32 _currentCdpId = (startNodeId == dummyId ? data.tail : startNodeId);

 327:             _currentCdpId = data.nodes[_currentCdpId].prevId;

 357:             ++nextCdpNonce;

 394:             data.nodes[data.tail].nextId = _id;

 428:             _firstPrev != dummyId || _lastNext != dummyId,

 443:             data.nodes[_lastNext].prevId = _firstPrev;

 473:                 data.nodes[data.tail].nextId = dummyId;

 479:                 data.nodes[data.nodes[_id].nextId].prevId = data.nodes[_id].prevId;

 520:         bool _exist = _id != dummyId && (data.head == _id || data.tail == _id);

 523:             _exist = _id != dummyId && (_node.nextId != dummyId && _node.prevId != dummyId);

 602:         } else if (_nextId == dummyId) {

 608:                 data.nodes[_prevId].nextId == _nextId &&

 609:                 cdpManager.getCachedNominalICR(_prevId) >= _NICR &&

 622:             return (dummyId, _startId);

 631:             nextId = data.nodes[prevId].nextId;

 645:             return (_startId, dummyId);

 654:             prevId = data.nodes[nextId].prevId;

 690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {

 692:                 nextId = dummyId;

```

### <a name="GAS-13"></a>[GAS-13] Use calldata instead of memory for function arguments that do not get mutated
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  _cdpArray
 126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  roleIds
 120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

 /// @audit  roleName
 154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 /// @audit  _ids
 16:     function batchRemove(bytes32[] memory _ids) external;

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  _cdpArray
 679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  _ids
 419:     function batchRemove(bytes32[] memory _ids) external override {

```

### <a name="GAS-14"></a>[GAS-14] Gas savings can be achieved by changing the model for assigning value to the structure
By changing the pattern of assigning value to the structure, gas savings of ~130 per instance are achieved. In addition, this use will provide significant savings in distribution costs. 
 `structure = Structure({parameter1: value1})` 
 can be changed to 
 `structure.parameter1 = value1`

 There are 8 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 427:             MoveTokensParams memory _varMvTokens = MoveTokensParams(
                     msg.sender,
                     vars.collSharesChange,
                     (vars.isCollIncrease ? _stEthBalanceIncrease : 0),
                     vars.isCollIncrease,
                     _debtChange,
                     _isDebtIncrease

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 150:         CdpDebtAndCollShares memory _oldDebtAndColl = CdpDebtAndCollShares(
                 Cdps[_redeemColFromCdp.cdpId].debt,
                 Cdps[_redeemColFromCdp.cdpId].coll

 395:                 SingleRedemptionInputs memory _redeemColFromCdp = SingleRedemptionInputs(
                         _cId,
                         totals.remainingDebtToRedeem,
                         totals.price,
                         _upperPartialRedemptionHint,
                         _lowerPartialRedemptionHint,
                         _partialRedemptionHintNICR

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 737:         return CdpDebtAndCollShares(entireDebt, entireColl);

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 101:         LiquidationLocals memory _liqState = LiquidationLocals(
                 _cdpId,
                 _partialAmount,
                 _price,
                 _ICR,
                 _upperPartialHint,
                 _lowerPartialHint,
                 (_recoveryModeAtStart),
                 _TCR,
                 0,
                 0,
                 0,
                 0,
                 0

 117:         LiquidationRecoveryModeLocals memory _rs = LiquidationRecoveryModeLocals(
                 systemDebt,
                 systemColl,
                 0,
                 0,
                 0,
                 _cdpId,
                 _price,
                 _ICR,
                 0,
                 0

 614:         LiquidationLocals memory _liqState = LiquidationLocals(
                 vars.cdpId,
                 0,
                 _price,
                 vars.ICR,
                 vars.cdpId,
                 vars.cdpId,
                 (false),
                 _TCR,
                 0,
                 0,
                 0,
                 0,
                 0

 649:         LiquidationRecoveryModeLocals memory _recState = LiquidationRecoveryModeLocals(
                 _systemDebt,
                 _systemCollShares,
                 0,
                 0,
                 0,
                 vars.cdpId,
                 _price,
                 vars.ICR,
                 0,
                 0

```

### <a name="GAS-15"></a>[GAS-15] Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate
Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key keccak256 hash (Gkeccak256 - 30 gas) and that calculations associated stack operations.

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

 32:     mapping(address => bytes32) public getUserRoles;

 34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

 36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 51:     mapping(address => uint256) private _balances;

 52:     mapping(address => mapping(address => uint256)) private _allowances;

```

### <a name="GAS-16"></a>[GAS-16] Consider activating via-ir for deploying
By using --via-ir or {"viaIR": true}, the compiler is able to use more advanced multi-function optimizations, for extra gas savings.

 There is 1 instance:

 ```solidity
File: All Files

```

### <a name="GAS-17"></a>[GAS-17] Expressions for constant values such as a call to keccak256(), should use immutable rather than constant
The reason for this is that constant variables are evaluated at runtime and their value is included in the bytecode of the contract. This means that any expensive operations performed as part of the constant expression, such as a call to keccak256(), will be executed every time the contract is deployed, even if the result is always the same. This can result in higher gas costs. In contrast, immutable variables are evaluated at compilation time, and their values are included in the bytecode of the contract as constants. This means that any expensive operations performed as part of the immutable expression are only executed once, when the contract is compiled, and the result is reused every time the contract is deployed. This can result in lower gas costs compared to using constant variables.

 There are 7 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 32:     bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

 141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 7:     uint256 public constant MAX_TCR = type(uint256).max;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```

### <a name="GAS-18"></a>[GAS-18] Constructors can be marked as payable to save deployment gas
Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. A constructor can be safely marked as payable, because only the deployer would be able to pass funds, and the project itself would not pass any funds.

 There are 19 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 46:     constructor(

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 107:     constructor(

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 30:     constructor(

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 217:     constructor(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 42:     constructor(

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 18:     constructor(address _owner, Authority _authority) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 61:     constructor(

```


```solidity
File: packages/contracts/contracts/Governor.sol

 36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 27:     constructor(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 51:     constructor(

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 41:     constructor(

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 21:     constructor(

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 17:     constructor(

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 14:     constructor(

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 57:     constructor(

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 44:     constructor(address _owner) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {

```

### <a name="GAS-19"></a>[GAS-19] Use custom errors rather than revert()/require() strings to save gas
Custom errors are available from solidity version 0.8.4. Custom errors save ~50 gas each time they’re hit by avoiding having to allocate and store the revert string. Not defining the strings also save deployment gas.

 There are 150 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

 137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

 162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

 220:         require(

 228:         require(

 236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

 267:         require(amount > 0, "ActivePool: 0 Amount");

 269:         require(amount <= maxFlashLoan(token), "ActivePool: Too much");

 277:         require(

 294:         require(

 298:         require(

 302:         require(

 318:         require(token == address(collateral), "ActivePool: collateral Only");

 319:         require(!flashLoansPaused, "ActivePool: Flash Loans Paused");

 350:         require(

 374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

 377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

 393:         require(

 407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");

 146:         require(

 368:         require(

 463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

 541:         require(

 715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

 734:         require(

 807:         require(

 818:         require(

 826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

 831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

 835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

 839:         require(

 846:         require(

 911:         require(

 918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

 922:         require(

 929:         require(

 936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

 940:         require(

 947:         require(

 957:         require(

 970:         require(

 1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

 1085:         require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much");

 1091:         require(

 1115:         require(token == address(ebtcToken), "BorrowerOperations: EBTC Only");

 1116:         require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

 1141:         require(

 1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

 431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

 502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

 503:         require(

 626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

 672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

 678:         require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!"); // The baseRate can decay to 0

 743:         require(

 747:         require(

 754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

 758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

 762:         require(

 774:         require(

 789:         require(

 793:         require(

 808:         require(

 812:         require(

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 112:         require(

 242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");

 243:         require(

 261:         require(

 453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

 466:         require(

 475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

 556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

 584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

 649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

 653:         require(

 660:         require(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

 99:         require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

 113:         require(

 120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

 124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

 143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

 146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 27:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 17:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

 56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

 57:         require(!_authorityInitialized, "Auth: authority already initialized");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 109:         require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 90:         require(

 134:         require(

```


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

 300:         require(

 307:         require(

 315:         require(

 324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 40:         revert("Must be overridden");

 45:         require(owner() == msg.sender, "Must be owner");

 179:             require(

 191:             require(

 201:             require(

 249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

 251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

 253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

 255:             revert("Operator not found");

 352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

 356:             require(

 362:             require(

 421:         require(success, "Call has failed");

 440:                 require(

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

 82:             require(

 89:             require(

 93:             require(

 477:             require(

 680:         require(

 710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

 901:         require(

 909:         require(

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 79:         require(

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 111:         require(msg.sender == owner, "Must be owner");

 179:             require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks");

 187:         require(facet != address(0), "Diamond: Function does not exist");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

 365:         require(!isFull(), "SortedCdps: List is full");

 367:         require(!contains(_id), "SortedCdps: List already contains the node");

 369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

 371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

 422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

 427:         require(

 433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

 458:         require(contains(_id), "SortedCdps: List does not contain the id");

 506:         require(contains(_id), "SortedCdps: List does not contain the id");

 508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

 715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

 720:         require(

```

### <a name="GAS-20"></a>[GAS-20] ++i costs less gas than i++, especially when its used in for loops
nothing for description

 There are 7 instances:

 ```solidity
File: packages/contracts/contracts/Governor.sol

 46:         for (uint256 i = 0; i < users.length(); i++) {

 57:             for (uint256 i = 0; i < _usrs.length; i++) {

 76:         for (uint8 i = 0; i < type(uint8).max; i++) {

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 98:         for (uint8 i = 0; i < type(uint8).max; i++) {

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

 122:         for (uint8 i = 0; i < roleIds.length; i++) {

```

### <a name="GAS-21"></a>[GAS-21] Division by powers of two should use bit shifting
<x> / 2 is the same as <x> >> 1. While the compiler uses the SHR opcode to accomplish both, the version that uses division incurs an overhead of 20 gas due to JUMPs to and from a compiler utility function that introduces checks which can be avoided by using unchecked {} around the division by two.

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

 77:             } else {

 81:                 n = (n - 1) / 2;

```

### <a name="GAS-22"></a>[GAS-22] Do not shrink Variables
This means that if you use uint8 or any variable smaller than 256 bits, EVM has to first convert it uint256 to work on it and the conversion costs extra gas! You may wonder, What were the devs thinking? Why did they create smaller variables then? The answer lies in packing. In solidity, you can pack multiple small variables into one slot, but if you are defining a lone variable and can’t pack it, it’s optimal to use a uint256.

 There are 30 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 830:         uint status = cdpManager.getCdpStatus(_cdpId);

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

 22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

 24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

 25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

 357:             uint _pendingDebt,

 365:             uint prevCollShares = _cdp.coll;

 471:         uint128 index = Cdps[_cdpId].arrayIndex;

 897:         uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 31:     uint8 internal constant _DECIMALS = 18;

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 88:             uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;

 278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

 279:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

 365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

 366:         uint _cappedColl = collateral.getPooledEthByShares(_cappedColPortion + _liquidatorReward);

 435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

 436:             uint _cappedColl = collateral.getPooledEthByShares(_partialColl);

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 612:         uint8 ethBtcDecimals;

 613:         uint8 stEthEthDecimals;

 700:         uint8 ethBtcDecimals;

 701:         uint8 stEthEthDecimals;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 182:         uint _currentIndex = 0;

 183:         uint i;

 245:         uint _ownedCount = 0;

 246:         uint i = 0;

 273:         (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);

 293:         (uint _ownedCount, ) = _cdpCountOf(owner, startNodeId, maxNodes);

 311:         uint i = 0;

 312:         uint _cdpRetrieved;

```

### <a name="GAS-23"></a>[GAS-23] Empty blocks should be removed or emit something
 Removing empty blocks help conserve computational resources on the blockchain network, reducing transaction costs and improving overall efficiency.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 160:     receive() external payable {

```

### <a name="GAS-24"></a>[GAS-24] Events should be emitted outside of loops
Emitting an event has an overhead of 375 gas, which will be incurred on every iteration of the loop. It is cheaper to emit only once after the loop has finished.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/SortedCdps.sol

 451:             emit NodeRemoved(_ids[i]);

```

### <a name="GAS-25"></a>[GAS-25]  >=/<= costs less gas than >/<
The compiler uses opcodes GT and ISZERO for code that uses >, but only requires LT for >=. A similar behaviour applies for >, which uses opcodes LT and ISZERO, but only requires GT for <=, and it can save 3 gas for each.

 There are 63 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 267:         require(amount > 0, "ActivePool: 0 Amount");

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

 476:             CCR > MCR (125% vs 110%)

 479:             Additionally, the new system TCR after the Cdps addition must be >CCR

 495:             if (newTCR < CCR) {

 891:             if (_vars.newTCR < CCR) {

 913:             "BorrowerOperations: An operation that would result in ICR < MCR is not permitted"

 931:             "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"

 1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

 431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

 553:         3e30 EBTC dwarfs the value of all wealth in the world ( which is < 1e15 USD). */

 601:         return TCR < CCR;

 626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

 690:         uint256 timePassed = block.timestamp > lastRedemptionTimestamp

 711:             block.timestamp > lastRedemptionTimestamp

 758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 99:         if (newTCR < CCR) {

 453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

 512:         if (_newIndex > _oldIndex && totalStakes > 0) {

 654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

 765:         if (_newIndex > _oldIndex && totalStakes > 0) {

 829:         if (pendingDebtRedistributed > 0) {

 900:             block.timestamp > cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 73:         while (n > 1) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 46:         for (uint256 i = 0; i < users.length(); i++) {

 53:         if (count > 0) {

 76:         for (uint8 i = 0; i < type(uint8).max; i++) {

 81:         if (count > 0) {

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 98:         for (uint8 i = 0; i < type(uint8).max; i++) {

 104:         if (count > 0) {

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

 122:         for (uint8 i = 0; i < roleIds.length; i++) {

 135:         if (_sigs.length > 0) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 86:                 vars.remainingEbtcToRedeem > 0 &&

 93:                 if (currentCdpDebt > vars.remainingEbtcToRedeem) {

 191:             if (currentDiff < diff) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 128:         if (operation.amountToTransferIn > 0) {

 223:         if (ebtcBal > 0) {

 227:         if (collateralBal > 0) {

 293:         if (beforeSwapsLength > 0) {

 307:         if (afterSwapsLength > 0) {

 385:         for (uint256 i; i < swapLength; ) {

 438:             for (uint256 i; i < length; ++i) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 94:                 block.timestamp >

 98:         } // Implicit Else Case, Implies ICR < MRC, meaning the CDP is liquidatable

 195:             if (_outputState.totalSurplusCollShares > 0) {

 476:         if (_partialState.ICR > LICR) {

 525:         if (totalDebtToRedistribute > 0) {

 710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

 713:         if (totals.totalCollSurplus > 0) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 421:             _response.timestampEthBtc > block.timestamp ||

 423:             _response.timestampStEthEth > block.timestamp

 457:         uint256 percentDeviation = maxPrice > 0

 471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

 489:             _fallbackResponse.timestamp > 0 &&

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 114:         for (uint256 i; i < length; ) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 202:             if (maxNodes > 0 && i >= maxNodes) {

 259:             if (maxNodes > 0 && i >= maxNodes) {

 330:             if (maxNodes > 0 && i >= maxNodes) {

 460:         if (data.size > 1) {

```

### <a name="GAS-26"></a>[GAS-26] keccak256() hash of literals should only be computed once
The result of the hash should be stored in an immutable variable, and the variable should be used instead. If the hash is being used as a part of a function selector, the cast to bytes4 should also only be done once. 

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 33:         keccak256(

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```

### <a name="GAS-27"></a>[GAS-27] Don't initialize variables with default value

 There are 19 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

```


```solidity
File: packages/contracts/contracts/Governor.sol

 46:         for (uint256 i = 0; i < users.length(); i++) {

 54:             uint256 j = 0;

 57:             for (uint256 i = 0; i < _usrs.length; i++) {

 76:         for (uint8 i = 0; i < type(uint8).max; i++) {

 82:             uint256 j = 0;

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 98:         for (uint8 i = 0; i < type(uint8).max; i++) {

 105:             uint256 j = 0;

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

 122:         for (uint8 i = 0; i < roleIds.length; i++) {

 137:             for (uint256 i = 0; i < _sigs.length; ++i) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 105:                         partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 182:         uint _currentIndex = 0;

 245:         uint _ownedCount = 0;

 246:         uint i = 0;

 311:         uint i = 0;

 432:         for (uint256 i = 0; i < _len; ++i) {

 449:         for (uint i = 0; i < _len; ++i) {

```

### <a name="GAS-28"></a>[GAS-28] internal functions only called once can be inlined to save gas
If an internal function is only used once, there is no need to modularize it, unless the function calling it would otherwise be too long and complex. Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

 There are 75 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 219:     function _requireCallerIsBorrowerOperations() internal view {

 235:     function _requireCallerIsCdpManager() internal view {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 744:     function _getCollSharesChangeFromStEthChange(
             uint256 _collReceived,
             uint256 _requestedCollWithdrawal
         ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

 760:     function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

 803:     function _requireSingularCollChange(
             uint256 _stEthBalanceIncrease,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 813:     function _requireNonZeroAdjustment(
             uint256 _stEthBalanceIncrease,
             uint256 _debtChange,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

 834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {

 838:     function _requireNotInRecoveryMode(uint256 _tcr) internal view {

 845:     function _requireNoStEthBalanceDecrease(uint256 _stEthBalanceDecrease) internal pure {

 852:     function _requireValidAdjustmentInCurrentMode(
             bool _isRecoveryMode,
             uint256 _stEthBalanceDecrease,
             bool _isDebtIncrease,
             AdjustCdpLocals memory _vars
         ) internal {

 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 946:     function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

 986:     function _getNewNominalICRFromCdpChange(
             AdjustCdpLocals memory vars,
             bool _isDebtIncrease
         ) internal pure returns (uint256) {

 1004:     function _getNewICRFromCdpChange(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 135:     function _redeemCollateralFromCdp(
             SingleRedemptionInputs memory _redeemColFromCdp
         ) internal returns (SingleRedemptionValues memory singleRedemption) {

 244:     function _closeCdpByRedemption(
             bytes32 _cdpId,
             uint256 _EBTC,
             uint256 _collSurplus,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) internal {

 272:     function _isValidFirstRedemptionHint(
             bytes32 _firstRedemptionHint,
             uint256 _price
         ) internal view returns (bool) {

 489:     function _getCdpIdsToRemove(
             bytes32 _start,
             uint256 _total,
             bytes32 _end
         ) internal view returns (bytes32[] memory) {
             uint256 _cnt = _total;

 550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
             /* Max array size is 2**128 - 1, i.e. ~3e30 cdps. No risk of overflow, since cdps have minimum EBTC

 595:     function _checkPotentialRecoveryMode(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (bool) {
             uint256 TCR = _computeTCRWithGivenSystemValues(_systemCollShares, _systemDebt, _price);

 612:     function _updateBaseRateFromRedemption(
             uint256 _ETHDrawn,
             uint256 _price,
             uint256 _totalEBTCSupply
         ) internal returns (uint256) {
             uint256 decayedBaseRate = _calcDecayedBaseRate();

 655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {
             return _calcRedemptionFee(getRedemptionRate(), _ETHDrawn);

 737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(
             address _redeemer,
             uint256 _amount,
             uint256 _totalSupply
         ) internal view {
             uint256 callerBalance = ebtcToken.balanceOf(_redeemer);

 753:     function _requireAmountGreaterThanZero(uint256 _amount) internal pure {
             require(_amount > 0, "CdpManager: Amount must be greater than zero");

 757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {
             require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

 761:     function _requireValidMaxFeePercentage(uint256 _maxFeePercentage) internal view {
             require(

 977:     function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {
             Cdps[_cdpId].coll = _newColl;

 984:     function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {
             Cdps[_cdpId].debt = _newDebt;

```


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
             Status cdpStatus = Cdps[_cdpId].status;

 539:     function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {
             if (_newIndex != _oldIndex) {

 574:     function _takeSplitAndUpdateFeePerUnit(
             uint256 _feeTaken,
             uint256 _newPerUnit,
             uint256 _newErrorPerUnit
         ) internal {
             uint256 _oldPerUnit = systemStEthFeePerUnitIndex;

 592:     function _applyAccumulatedFeeSplit(
             bytes32 _cdpId,
             uint256 _newColl,
             uint256 _feeSplitDistributed,
             uint256 _oldPerUnitCdp,
             uint256 _systemStEthFeePerUnitIndex
         ) internal {
             // apply split fee to given CDP

 652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {
             require(

 895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {
             // we have waited enough

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 112:     function _requireCallerIsBorrowerOperations() internal view {

 119:     function _requireCallerIsCdpManager() internal view {

 123:     function _requireCallerIsActivePool() internal view {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 83:     function _getTCRWithSystemDebtAndCollShares(
            uint256 _price
        ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

 134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

 140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 262:     function _mint(address account, uint256 amount) internal {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 133:     function _calculateCdpStateAfterPartialRedemption(
             LocalVariables_getRedemptionHints memory vars,
             uint256 currentCdpDebt,
             uint256 _price
         ) internal view returns (uint256, uint256) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 398:     function _doSwap(SwapOperation memory swapData) internal {

 435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

 450:     function _ensureNotSystem(address addy) internal {

 460:     function _openCdpCallback(bytes memory data) internal {

 474:     function _closeCdpCallback(bytes memory data) internal {

 482:     function _adjustCdpCallback(bytes memory data) internal {

 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 135:     function _liquidateIndividualCdpSetupCDP(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) internal {

 450:     function _partiallyReduceCdpDebt(
             bytes32 _cdpId,
             uint256 _partialDebt,
             uint256 _partialColl
         ) internal {

 466:     function _reInsertPartialLiquidation(
             LiquidationLocals memory _partialState,
             uint256 _newNICR,
             uint256 _oldDebt,
             uint256 _oldColl
         ) internal {

 642:     function _getLiquidationValuesRecoveryMode(
             uint256 _price,
             uint256 _systemDebt,
             uint256 _systemCollShares,
             LocalVariables_LiquidationSequence memory vars,
             LiquidationValues memory singleLiquidation
         ) internal {

 733:     function _getTotalFromBatchLiquidate_RecoveryMode(
             uint256 _price,
             uint256 _systemCollShares,
             uint256 _systemDebt,
             bytes32[] memory _cdpArray
         ) internal returns (LiquidationTotals memory totals) {

 807:     function _getTotalsFromBatchLiquidate_NormalMode(
             uint256 _price,
             uint256 _TCR,
             bytes32[] memory _cdpArray
         ) internal returns (LiquidationTotals memory totals) {

 862:     function _redistributeDebt(uint256 _debt) internal {

 896:     function _requirePartialLiqDebtSize(
             uint256 _partialDebt,
             uint256 _entireDebt,
             uint256 _price
         ) internal view {

 908:     function _requirePartialLiqCollSize(uint256 _entireColl) internal pure {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 582:     function _getCurrentFallbackResponse()
             internal
             view
             returns (FallbackResponse memory fallbackResponse)
         {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 134:     function _executeOne(Operation calldata op) internal {

 174:     function _fallback() internal {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

```

### <a name="GAS-29"></a>[GAS-29] A modifier used only once and not being inherited should be inlined to save gas
When you use a modifier in Solidity, Solidity generates code to check the conditions of the modifier and execute the modified function if the conditions are met. This generated code can consume gas, especially if the modifier is used frequently or if the modified function is called multiple times. By inlining a modifier that is used only once and not being inherited, you can eliminate the overhead of the generated code and reduce the gas cost of your contract.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 26:     modifier requiresAuth() virtual {

```

### <a name="GAS-30"></a>[GAS-30] Private functions only used once can be inlined to save gas
If a private function is only used once, there is no need to modularize it, unless the function calling it would otherwise be too long and complex.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 397:     function _liquidateCDPPartially(
             LiquidationLocals memory _partialState
         ) private returns (uint256, uint256) {

 544:     function _calculatePartialLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

```

### <a name="GAS-31"></a>[GAS-31] Usage of ints/uints smaller than 32 bytes incurs overhead
Using ints/uints smaller than 32 bytes may cost more gas. This is because the EVM operates on 32 bytes at a time, so if an element is smaller than 32 bytes, the EVM must perform more operations to reduce the size of the element from 32 bytes to the desired size.

 There are 70 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"

 711:         uint8 v,

 1133:         return type(uint112).max;

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

 21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

 22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

 24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

 25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

 111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

 471:         uint128 index = Cdps[_cdpId].arrayIndex;

 897:         uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

 43:         uint8 role,

 107:         uint8 role,

 147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 31:     uint8 internal constant _DECIMALS = 18;

 204:         uint8 v,

 343:     function decimals() external pure override returns (uint8) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 20:         uint8 roleId;

 27:         uint8[] roles;

 30:     mapping(uint8 => string) internal roleNames;

 32:     event RoleNameSet(uint8 indexed role, string indexed name);

 43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

 73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {

 76:         for (uint8 i = 0; i < type(uint8).max; i++) {

 76:         for (uint8 i = 0; i < type(uint8).max; i++) {

 83:             rolesForUser = new uint8[](count);

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

 98:         for (uint8 i = 0; i < type(uint8).max; i++) {

 98:         for (uint8 i = 0; i < type(uint8).max; i++) {

 106:             roleIds = new uint8[](count);

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

 120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

 122:         for (uint8 i = 0; i < roleIds.length; i++) {

 146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

 154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 103:         uint128 arrayIndex;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 37:         uint8 v,

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 18:         uint80 roundEthBtcId;

 19:         uint80 roundStEthEthId;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 502:         uint16 _maxCopy,

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 88:             uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 612:         uint8 ethBtcDecimals;

 613:         uint8 stEthEthDecimals;

 615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

 623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

 635:             uint80 roundId,

 640:             uint80 /* answeredInRound */

 651:             uint80 roundId,

 656:             uint80 /* answeredInRound */

 688:         uint80 _currentRoundEthBtcId,

 689:         uint80 _currentRoundStEthEthId

 700:         uint8 ethBtcDecimals;

 701:         uint8 stEthEthDecimals;

 703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

 711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

 723:             uint80 roundId,

 728:             uint80 /* answeredInRound */

 739:             uint80 roundId,

 744:             uint80 /* answeredInRound */

 775:     function _checkHealthyCLResponse(uint80 _roundId, int256 _answer) internal view returns (bool) {

 791:         uint8 _ethBtcDecimals,

 792:         uint8 _stEthEthDecimals

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 102:         uint128 value; // How much ETH to send

 103:         uint128 gas; // How much gas to send

```

### <a name="GAS-32"></a>[GAS-32] Long require/revert strings
require()/revert() strings longer than 32 bytes cost extra gas

 There are 55 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

 162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

 236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

 374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

 377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

 407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");

 463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

 715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

 826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

 831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

 835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

 918:         require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

 936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

 1116:         require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

 1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

 502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

 626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

 672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

 754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

 758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");

 453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

 475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

 556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

 649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

 120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

 124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

 143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

 146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 57:         require(!_authorityInitialized, "Auth: authority already initialized");

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

 165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

 251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

 263:         require(account != address(0), "EBTCToken: mint to zero recipient!");

 271:         require(account != address(0), "EBTCToken: burn from zero account!");

 274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

 251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

 253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

 352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

 710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

 367:         require(!contains(_id), "SortedCdps: List already contains the node");

 371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

 422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

 433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");

 458:         require(contains(_id), "SortedCdps: List does not contain the id");

 506:         require(contains(_id), "SortedCdps: List does not contain the id");

 508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

 715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

```

### <a name="GAS-33"></a>[GAS-33] Reduce gas usage by moving to Solidity 0.8.19 or later
Solidity version 0.8.19 introduced a number of gas optimizations, refer to the Solidity 0.8.19 Release Announcement for details.

 There are 39 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 3: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 2: pragma solidity 0.8.17;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 3: pragma solidity 0.8.17;

```

### <a name="GAS-34"></a>[GAS-34] Using a nesting if statement instead of a logical AND(&&)
Using a nesting if statement instead of a logical AND (&&) can provide similar short-circuiting behavior whereas double if is slightly more gas efficient.

 There are 14 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 393:         if (!_isDebtIncrease && _debtChange > 0) {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 512:         if (_newIndex > _oldIndex && totalStakes > 0) {

 796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 157:             if (

 756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

 790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {

 819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 226:                 if (

 372:                 if (

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 202:             if (maxNodes > 0 && i >= maxNodes) {

 259:             if (maxNodes > 0 && i >= maxNodes) {

 330:             if (maxNodes > 0 && i >= maxNodes) {

 621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

 644:         if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {

```

### <a name="GAS-35"></a>[GAS-35] Optimize names to save gas
public/external function names and public member variable names can be optimized to save gas. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, per sorted position shifted.

 There are 40 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  (), getSystemCollShares(), getSystemDebt(), getFeeRecipientClaimableCollShares(), transferSystemCollShares(), transferSystemCollSharesAndLiquidatorReward(), allocateSystemCollSharesToFeeRecipient(), increaseSystemDebt(), decreaseSystemDebt(), increaseSystemCollShares(), flashLoan(), flashFee(), maxFlashLoan(), claimFeeRecipientCollShares(), sweepToken(), setFeeRecipientAddress(), setFeeBps(), setFlashLoansPaused(), NAME, borrowerOperationsAddress, cdpManagerAddress, collSurplusPoolAddress, feeRecipientAddress, collateral, 
 22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  (), openCdp(), openCdpFor(), addColl(), withdrawColl(), withdrawDebt(), repayDebt(), adjustCdp(), adjustCdpWithColl(), closeCdp(), claimSurplusCollShares(), getPositionManagerApproval(), setPositionManagerApproval(), revokePositionManagerApproval(), renouncePositionManagerApproval(), DOMAIN_SEPARATOR(), domainSeparator(), version(), permitTypeHash(), permitPositionManagerApproval(), flashLoan(), flashFee(), maxFlashLoan(), setFeeRecipientAddress(), setFeeBps(), setFlashLoansPaused(), NAME, cdpManager, collSurplusPool, feeRecipientAddress, ebtcToken, sortedCdps, positionManagers, 
 21: contract BorrowerOperations is

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  (), getActiveCdpsCount(), getIdFromCdpIdsArray(), liquidate(), partiallyLiquidate(), batchLiquidateCdps(), redeemCollateral(), syncAccounting(), updateStakeAndTotalStakes(), closeCdp(), getSystemDebt(), getCachedTCR(), checkRecoveryMode(), getRedemptionRate(), getRedemptionRateWithDecay(), getRedemptionFeeWithDecay(), getDeploymentStartTime(), checkPotentialRecoveryMode(), setStakingRewardSplit(), setRedemptionFeeFloor(), setMinuteDecayFactor(), setBeta(), setRedemptionsPaused(), getCdpStatus(), getCdpStake(), getCdpDebt(), getCdpCollShares(), getCdpLiquidatorRewardShares(), initializeCdp(), updateCdp(), 
 16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  notifyStartGracePeriod(), notifyEndGracePeriod(), setGracePeriod(), (), syncGlobalAccounting(), syncGlobalAccountingAndGracePeriod(), calcFeeUponStakingReward(), getAccumulatedFeeSplitApplied(), getCachedNominalICR(), getSyncedNominalICR(), getCachedICR(), getPendingRedistributedDebt(), hasPendingRedistributedDebt(), getSyncedDebtAndCollShares(), getSyncedCdpDebt(), getSyncedCdpCollShares(), getSyncedICR(), getSyncedTCR(), canLiquidateRecoveryMode(), UNSET_TIMESTAMP, MINIMUM_GRACE_PERIOD, lastGracePeriodStartTimestamp, recoveryModeGracePeriodDuration, NAME, borrowerOperationsAddress, ebtcToken, liquidationLibrary, sortedCdps, SECONDS_IN_ONE_MINUTE, MIN_REDEMPTION_FEE_FLOOR, redemptionFeeFloor, redemptionsPaused, minuteDecayFactor, MIN_MINUTE_DECAY_FACTOR, MAX_MINUTE_DECAY_FACTOR, beta, baseRate, stakingRewardSplit, lastRedemptionTimestamp, Cdps, totalStakes, totalStakesSnapshot, totalCollateralSnapshot, systemDebtRedistributionIndex, cdpDebtRedistributionIndex, lastEBTCDebtErrorRedistribution, stEthIndex, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError, cdpStEthFeePerUnitIndex, CdpIds, 
 19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  (), getTotalSurplusCollShares(), getSurplusCollShares(), increaseSurplusCollShares(), claimSurplusCollShares(), increaseTotalSurplusCollShares(), sweepToken(), NAME, borrowerOperationsAddress, cdpManagerAddress, activePoolAddress, feeRecipientAddress, collateral, 
 16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  setAuthority(), transferOwnership(), owner, authority, 
 9: abstract contract Auth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 /// @audit  authority(), authorityInitialized(), setAuthority(), 
 10: contract AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 /// @audit  MAX_BPS, MAX_FEE_BPS, FLASH_SUCCESS_VALUE, feeBps, flashLoansPaused, 
 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  (), getSystemCollShares(), LICR, MCR, CCR, LIQUIDATOR_REWARD, MIN_NET_STETH_BALANCE, PERCENT_DIVISOR, BORROWING_FEE_FLOOR, STAKING_REWARD_SPLIT, MAX_REWARD_SPLIT, activePool, priceFeed, collateral, 
 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 /// @audit  locked, 
 7: abstract contract ReentrancyGuard {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  (), doesUserHaveRole(), doesRoleHaveCapability(), isPublicCapability(), canCall(), setPublicCapability(), setRoleCapability(), burnCapability(), setUserRole(), getUserRoles, capabilityFlag, getRolesWithCapability, 
 12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  (), mint(), burn(), burn(), totalSupply(), balanceOf(), transfer(), allowance(), approve(), transferFrom(), increaseAllowance(), decreaseAllowance(), DOMAIN_SEPARATOR(), domainSeparator(), permit(), nonces(), name(), symbol(), decimals(), version(), permitTypeHash(), cdpManagerAddress, borrowerOperationsAddress, 
 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  (), getUsersByRole(), getRolesForUser(), getRolesFromByteMap(), getByteMapFromRoles(), getEnabledFunctionsInTarget(), getRoleName(), setRoleName(), 
 13: contract Governor is RolesAuthority {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  (), getRedemptionHints(), getApproxHint(), computeNominalCR(), computeCR(), NAME, sortedCdps, cdpManager, 
 11: contract HintHelpers is EbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 /// @audit  transferSystemCollShares(), increaseSystemCollShares(), transferSystemCollSharesAndLiquidatorReward(), allocateSystemCollSharesToFeeRecipient(), claimFeeRecipientCollShares(), feeRecipientAddress(), getFeeRecipientClaimableCollShares(), setFeeRecipientAddress(), 
 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 /// @audit  openCdp(), openCdpFor(), addColl(), withdrawColl(), withdrawDebt(), repayDebt(), closeCdp(), adjustCdp(), adjustCdpWithColl(), claimSurplusCollShares(), feeRecipientAddress(), 
 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 /// @audit  getActiveCdpsCount(), getIdFromCdpIdsArray(), liquidate(), partiallyLiquidate(), batchLiquidateCdps(), redeemCollateral(), updateStakeAndTotalStakes(), syncAccounting(), closeCdp(), getRedemptionRate(), getRedemptionRateWithDecay(), getRedemptionFeeWithDecay(), getCdpStatus(), getCdpStake(), getCdpDebt(), getCdpCollShares(), getCdpLiquidatorRewardShares(), initializeCdp(), updateCdp(), getCachedTCR(), checkRecoveryMode(), 
 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  totalStakes(), ebtcToken(), systemStEthFeePerUnitIndex(), systemStEthFeePerUnitIndexError(), stEthIndex(), calcFeeUponStakingReward(), syncGlobalAccounting(), syncGlobalAccountingAndGracePeriod(), getAccumulatedFeeSplitApplied(), getCachedNominalICR(), getCachedICR(), getSyncedCdpDebt(), getSyncedCdpCollShares(), getSyncedICR(), getSyncedTCR(), getSyncedNominalICR(), getPendingRedistributedDebt(), hasPendingRedistributedDebt(), getSyncedDebtAndCollShares(), canLiquidateRecoveryMode(), 
 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 /// @audit  getTotalSurplusCollShares(), getSurplusCollShares(), increaseSurplusCollShares(), claimSurplusCollShares(), increaseTotalSurplusCollShares(), 
 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 /// @audit  mint(), burn(), 
 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 /// @audit  onFlashLoan(), 
 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 /// @audit  maxFlashLoan(), flashFee(), flashLoan(), 
 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 /// @audit  priceFeed(), 
 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 /// @audit  getFallbackResponse(), fallbackTimeout(), setFallbackTimeout(), 
 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 /// @audit  increasePermitNonce(), nonces(), 
 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 /// @audit  getSystemCollShares(), getSystemDebt(), increaseSystemDebt(), decreaseSystemDebt(), 
 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 /// @audit  getPositionManagerApproval(), setPositionManagerApproval(), revokePositionManagerApproval(), renouncePositionManagerApproval(), permitPositionManagerApproval(), version(), permitTypeHash(), domainSeparator(), 
 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 /// @audit  fetchPrice(), 
 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 /// @audit  notifyStartGracePeriod(), notifyEndGracePeriod(), 
 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 /// @audit  remove(), batchRemove(), reInsert(), contains(), isFull(), isEmpty(), getSize(), getMaxSize(), getFirst(), getLast(), getNext(), getPrev(), validInsertPosition(), findInsertPosition(), insert(), getOwnerAddress(), nonExistId(), cdpCountOf(), getCdpCountOf(), getCdpsOf(), getAllCdpsOf(), cdpOfOwnerByIndex(), cdpOfOwnerByIdx(), 
 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  Cdps(), 
 14: interface ICdpCdps {

 /// @audit  owner(), (), doOperation(), sweepToCaller(), sweepToken(), decodeFLData(), onFlashLoan(), borrowerOperations, activePool, cdpManager, ebtcToken, sortedCdps, stETH, 
 26: contract LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 /// @audit  owner(), 
 6: interface IOwnerLike {

 /// @audit  (), owner(), 
 40: contract LeverageMacroDelegateTarget is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 /// @audit  (), deployNewMacro(), deployNewMacro(), borrowerOperations, activePool, cdpManager, ebtcToken, stETH, sortedCdps, 
 11: contract LeverageMacroFactory {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 /// @audit  (), owner(), resetApprovals(), 
 11: contract LeverageMacroReference is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  (), liquidate(), partiallyLiquidate(), batchLiquidateCdps(), 
 13: contract LiquidationLibrary is CdpManagerStorage {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  (), fetchPrice(), setFallbackCaller(), NAME, ETH_BTC_CL_FEED, STETH_ETH_CL_FEED, fallbackCaller, TIMEOUT_ETH_BTC_FEED, TIMEOUT_STETH_ETH_FEED, MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND, MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES, lastGoodPrice, status, 
 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  (), setFallbackHandler(), setAllowAnyCall(), enableCallbackForCall(), execute(), (), (), owner, 
 25: contract SimplifiedDiamondLike {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  (), toCdpId(), getOwnerAddress(), nonExistId(), cdpOfOwnerByIndex(), cdpOfOwnerByIdx(), cdpCountOf(), getCdpCountOf(), getCdpsOf(), getAllCdpsOf(), insert(), remove(), batchRemove(), reInsert(), contains(), isFull(), isEmpty(), getSize(), getMaxSize(), getFirst(), getLast(), getNext(), getPrev(), validInsertPosition(), findInsertPosition(), NAME, borrowerOperationsAddress, cdpManager, maxSize, data, nextCdpNonce, dummyId, 
 51: contract SortedCdps is ISortedCdps {

```

### <a name="GAS-36"></a>[GAS-36] Operator += costs more gas than <x> = <x> + <y> for variables
Using the += like operator instead of plus-equals saves 113 gas.

 There are 8 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 107:             cachedSystemCollShares -= _shares; // Updating here avoids an SLOAD

 141:             cachedSystemCollShares -= _shares;

 165:             cachedSystemCollShares -= _shares;

 356:             cachedFeeRecipientCollShares -= _shares;

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 697:             lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 50:                 count += 1;

 78:                 count += 1;

 101:                 count += 1;

```

### <a name="GAS-37"></a>[GAS-37] Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

 There are 31 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 24:     string public constant NAME = "ActivePool";

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 29:     string public constant NAME = "BorrowerOperations";

```


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


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 19:     string public constant NAME = "CollSurplusPool";

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 9:     uint256 public constant MAX_BPS = 10_000;

 10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

 11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


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


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 7:     uint256 public constant MAX_TCR = type(uint256).max;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 12:     string public constant NAME = "HintHelpers";

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 22:     string public constant NAME = "PriceFeed";

 32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

 33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

 36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

 42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 52:     string public constant NAME = "SortedCdps";

 80:     bytes32 public constant dummyId =

```

### <a name="GAS-38"></a>[GAS-38] Change public state variable visibility to private
its generally a good practice to limit the visibility of state variables to the minimum necessary level. This means that you should use the private visibility modifier for state variables whenever possible, and avoid using the public modifier unless it is absolutely necessary. Public state variables can be more expensive to read and write than private state variables, since Solidity generates additional getter and setter functions for public variables. By using private state variables, you can reduce the gas cost of your contract and improve its efficiency. Public state variables can be more expensive to read and write than private state variables, since Solidity generates additional getter and setter functions for public variables. By using private state variables, you can reduce the gas cost of your contract and improve its efficiency.

 There are 42 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 26:     address public immutable borrowerOperationsAddress;

 27:     address public immutable cdpManagerAddress;

 28:     address public immutable collSurplusPoolAddress;

 29:     address public feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 29:     string public constant NAME = "BorrowerOperations";

 53:     ICdpManager public immutable cdpManager;

 57:     address public feeRecipientAddress;

 65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

 126:     address public immutable borrowerOperationsAddress;

 173:     uint256 public totalStakesSnapshot;

 176:     uint256 public totalCollateralSnapshot;

 190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

 196:     uint256 public override stEthIndex;

 200:     uint256 public override systemStEthFeePerUnitIndexError;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 21:     address public immutable borrowerOperationsAddress;

 22:     address public immutable cdpManagerAddress;

 23:     address public immutable activePoolAddress;

 24:     address public immutable feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 16:     Authority public authority;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 7:     uint256 public constant MAX_TCR = type(uint256).max;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 32:     mapping(address => bytes32) public getUserRoles;

 34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

 36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 55:     address public immutable cdpManagerAddress;

 56:     address public immutable borrowerOperationsAddress;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 15:     ICdpManager public immutable cdpManager;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 31:     ICdpCdps public immutable cdpManager;

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 14:     address public immutable cdpManager;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 25:     AggregatorV3Interface public immutable ETH_BTC_CL_FEED;

 26:     AggregatorV3Interface public immutable STETH_ETH_CL_FEED;

 29:     IFallbackCaller public fallbackCaller; // Wrapper contract that calls the fallback system

 32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

 33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

 36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

 42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

 45:     uint256 public lastGoodPrice;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 54:     address public immutable borrowerOperationsAddress;

 56:     ICdpManager public immutable cdpManager;

 58:     uint256 public immutable maxSize;

 79:     uint256 public nextCdpNonce;

 80:     bytes32 public constant dummyId =

```

### <a name="GAS-39"></a>[GAS-39] Redundant state variable getters
Getters for public state variables are automatically generated so there is no need to code them manually and waste gas.

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 22:     function authority() public view returns (Authority) {

 26:     function authorityInitialized() public view returns (bool) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 44:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 130:     function nonExistId() public pure override returns (bytes32) {

```

### <a name="GAS-40"></a>[GAS-40] Duplicated require()/revert() checks should be refactored to a modifier Or function to save gas
Saves deployment costs.

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 134:         require(

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 67:         require(msg.sender == owner);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 506:         require(contains(_id), "SortedCdps: List does not contain the id");

```

### <a name="GAS-41"></a>[GAS-41] require() or revert() statements that check input arguments should be at the top of the function
Checks that involve constants should come before checks that involve state variables, function calls, and calculations. By doing these checks first, the function is able to revert before wasting a Gcoldsload (2100 gas*) in a function that may ultimately revert in the unhappy case.

 There are 38 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  could be moved to line 101
 104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

 /// @audit  could be moved to line 134
 137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

 /// @audit  could be moved to line 158
 162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

 /// @audit  could be moved to line 267
 269:         require(amount <= maxFlashLoan(token), "ActivePool: Too much");

 /// @audit  could be moved to line 347
 350:         require(
                 cachedFeeRecipientCollShares >= _shares,
                 "ActivePool: Insufficient fee recipient coll"

 /// @audit  could be moved to line 372
 374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

 /// @audit  could be moved to line 372
 377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

 /// @audit  could be moved to line 391
 393:         require(
                 _feeRecipientAddress != address(0),
                 "ActivePool: Cannot set fee recipient to zero address"

 /// @audit  could be moved to line 405
 407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  could be moved to line 338
 368:         require(
                 _stEthBalanceDecrease <= _cdpStEthBalance,
                 "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"

 /// @audit  could be moved to line 446
 541:         require(
                 vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
                 "BorrowerOperations: deposited collateral mismatch!"

 /// @audit  could be moved to line 715
 734:         require(
                 recoveredAddress != address(0) && recoveredAddress == _borrower,
                 "BorrowerOperations: Invalid signature"

 /// @audit  could be moved to line 1083
 1085:         require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  could be moved to line 494
 502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

 /// @audit  could be moved to line 494
 503:         require(
                 _toRemoveIds[_total - 1] == _end,
                 "CdpManager: batchRemoveSortedCdpIds check end error"

 /// @audit  could be moved to line 671
 672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

 /// @audit  could be moved to line 742
 743:         require(
                 callerBalance >= _amount,
                 "CdpManager: Requested redemption amount must be <= user's EBTC token balance"

 /// @audit  could be moved to line 742
 747:         require(
                 callerBalance <= _totalSupply,
                 "CdpManager: redeemer's EBTC balance exceeds total supply!"

 /// @audit  could be moved to line 789
 793:         require(
                 _redemptionFeeFloor <= DECIMAL_PRECISION,
                 "CDPManager: new redemption fee floor is higher than maximum"

 /// @audit  could be moved to line 808
 812:         require(
                 _minuteDecayFactor <= MAX_MINUTE_DECAY_FACTOR,
                 "CDPManager: new minute decay factor out of range"

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  could be moved to line 579
 584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  could be moved to line 143
 146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  could be moved to line 108
 109:         require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  could be moved to line 164
 165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

 /// @audit  could be moved to line 208
 219:         require(recoveredAddress == owner, "EBTC: invalid signature");

 /// @audit  could be moved to line 247
 248:         require(recipient != address(0), "EBTCToken: zero recipient!");

 /// @audit  could be moved to line 247
 251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

 /// @audit  could be moved to line 271
 274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

 /// @audit  could be moved to line 286
 287:         require(spender != address(0), "EBTCToken: zero approve spender!");

 /// @audit  could be moved to line 296
 300:         require(
                 _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
                 "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  could be moved to line 452
 453:         require(addy != address(sortedCdps));

 /// @audit  could be moved to line 452
 454:         require(addy != address(activePool));

 /// @audit  could be moved to line 452
 455:         require(addy != address(cdpManager));

 /// @audit  could be moved to line 452
 456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  could be moved to line 52
 56:         require(sig != 0x94b24d09);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  could be moved to line 365
 369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

 /// @audit  could be moved to line 365
 371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

 /// @audit  could be moved to line 504
 508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```

### <a name="GAS-42"></a>[GAS-42] Same cast is done multiple times
It’s cheaper to do it once, and store the result to a variable. The examples below are the second+ instance of a given cast of the variable

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 114:             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));

 120:             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);

 155:             getUserRoles[user] &= ~bytes32(1 << role);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

```

### <a name="GAS-43"></a>[GAS-43] Use shift Right/Left instead of division/multiplication if possible

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

 76:                 n = n / 2;

 81:                 n = (n - 1) / 2;

```

### <a name="GAS-44"></a>[GAS-44] State variable read in a loop
The state variable should be cached in a local variable rather than reading it on every iteration of the for-loop, which will replace each Gwarmaccess (100 gas) with a much cheaper stack read.

 There are 21 instances:

 ```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  cdpManager
 70:                 cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR

 /// @audit  sortedCdps
 72:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

 /// @audit  sortedCdps
 73:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

 /// @audit  cdpManager
 90:                 uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

 /// @audit  sortedCdps
 116:                 vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

 /// @audit  sortedCdps
 117:                 vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

 /// @audit  cdpManager
 185:             bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);

 /// @audit  cdpManager
 186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  dummyId
 185:         while (_currentCdpId != dummyId) {

 /// @audit  data
 199:             _currentCdpId = data.nodes[_currentCdpId].prevId;

 /// @audit  dummyId
 248:         while (_currentCdpId != dummyId) {

 /// @audit  data
 256:             _currentCdpId = data.nodes[_currentCdpId].prevId;

 /// @audit  dummyId
 318:         while (_currentCdpId != dummyId) {

 /// @audit  data
 327:             _currentCdpId = data.nodes[_currentCdpId].prevId;

 /// @audit  data
 450:             delete data.nodes[_ids[i]];

 /// @audit  dummyId
 629:         while (prevId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {

 /// @audit  data
 630:             prevId = data.nodes[prevId].nextId;

 /// @audit  data
 631:             nextId = data.nodes[prevId].nextId;

 /// @audit  dummyId
 652:         while (nextId != dummyId && !_validInsertPosition(_NICR, prevId, nextId)) {

 /// @audit  data
 653:             nextId = data.nodes[nextId].prevId;

 /// @audit  data
 654:             prevId = data.nodes[nextId].prevId;

```

### <a name="GAS-45"></a>[GAS-45] State variables only set in the constructor should be declared immutable 
Avoids a Gsset (20000 gas) in the constructor, and replaces the first access in each transaction (Gcoldsload - 2100 gas) and each access thereafter (Gwarmacces - 100 gas) with a PUSH32 (3 gas). While strings are not value types, and therefore cannot be immutable/constant if not hard-coded outside of the constructor, the same behavior can be achieved by making the current contract abstract with virtual functions for the string accessors, and having a child contract override the functions with the hard-coded implementation-specific values.

 There are 54 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 53:         borrowerOperationsAddress = _borrowerOperationsAddress;

 54:         cdpManagerAddress = _cdpManagerAddress;

 55:         collateral = ICollateralToken(_collTokenAddress);

 56:         collSurplusPoolAddress = _collSurplusAddress;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 117:         cdpManager = ICdpManager(_cdpManagerAddress);

 118:         collSurplusPool = ICollSurplusPool(_collSurplusPoolAddress);

 119:         sortedCdps = ISortedCdps(_sortedCdpsAddress);

 120:         ebtcToken = IEBTCToken(_ebtcTokenAddress);

 131:         _HASHED_NAME = hashedName;

 132:         _HASHED_VERSION = hashedVersion;

 133:         _CACHED_CHAIN_ID = _chainID();

 134:         _CACHED_DOMAIN_SEPARATOR = _buildDomainSeparator(_TYPE_HASH, hashedName, hashedVersion);

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 228:         deploymentStartTime = block.timestamp;

 229:         liquidationLibrary = _liquidationLibraryAddress;

 233:         borrowerOperationsAddress = _borrowerOperationsAddress;

 234:         collSurplusPool = ICollSurplusPool(_collSurplusPool);

 235:         ebtcToken = IEBTCToken(_ebtcToken);

 236:         sortedCdps = ISortedCdps(_sortedCdps);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 48:         borrowerOperationsAddress = _borrowerOperationsAddress;

 49:         cdpManagerAddress = _cdpManagerAddress;

 50:         activePoolAddress = _activePoolAddress;

 51:         collateral = ICollateralToken(_collTokenAddress);

 52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 53:         activePool = IActivePool(_activePoolAddress);

 54:         priceFeed = IPriceFeed(_priceFeedAddress);

 55:         collateral = ICollateralToken(_collateralAddress);

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 68:         cdpManagerAddress = _cdpManagerAddress;

 69:         borrowerOperationsAddress = _borrowerOperationsAddress;

 74:         _HASHED_NAME = hashedName;

 75:         _HASHED_VERSION = hashedVersion;

 76:         _CACHED_CHAIN_ID = _chainID();

 77:         _CACHED_DOMAIN_SEPARATOR = _buildDomainSeparator(_TYPE_HASH, hashedName, hashedVersion);

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 34:         sortedCdps = ISortedCdps(_sortedCdpsAddress);

 35:         cdpManager = ICdpManager(_cdpManagerAddress);

```


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


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 29:         borrowerOperations = _borrowerOperationsAddress;

 30:         activePool = _activePool;

 31:         cdpManager = _cdpManager;

 32:         ebtcToken = _ebtc;

 33:         stETH = _coll;

 34:         sortedCdps = _sortedCdps;

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 36:         theOwner = _owner;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 69:         ETH_BTC_CL_FEED = AggregatorV3Interface(_ethBtcCLFeed);

 70:         STETH_ETH_CL_FEED = AggregatorV3Interface(_collEthCLFeed);

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 45:         owner = _owner;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 93:         maxSize = _size;

 95:         cdpManager = ICdpManager(_cdpManagerAddress);

 96:         borrowerOperationsAddress = _borrowerOperationsAddress;

```

### <a name="GAS-46"></a>[GAS-46] State variables only set in their definitions should be declared constant
Avoids a Gsset (20000 gas) at deployment, and replaces the first access in each transaction (Gcoldsload - 2100 gas) and each access thereafter (Gwarmacces - 100 gas) with a PUSH32 (3 gas).

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;

 148:     uint256 public minuteDecayFactor = 999037758833783000;

 159:     uint256 public beta = 2;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 11:     uint256 public locked = OPEN;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 17:     bytes32 NO_ROLES = bytes32(0);

```

### <a name="GAS-47"></a>[GAS-47] Use uint256(1)/uint256(2) instead of true/false to save gas for changes
Avoids a Gsset (20000 gas) when changing from false to true, after having been true in the past

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 143:     bool public redemptionsPaused;

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 14:     bool private _authorityInitialized;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 15:     bool public flashLoansPaused;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 35:     bool internal immutable willSweep;

```

### <a name="GAS-48"></a>[GAS-48] Ternary unnecessary
`z = (x == y) ? true : false` `=>` `z = (x == y)`

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 100:         bool _recoveryModeAtStart = _TCR < CCR ? true : false;

 695:         vars.recoveryModeAtStart = _TCR < CCR ? true : false;

 788:                     vars.backToNormalMode = _TCR < CCR ? false : true;

```

### <a name="GAS-49"></a>[GAS-49] Use != 0 instead of > 0 for unsigned integer comparison

 There are 53 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 267:         require(amount > 0, "ActivePool: 0 Amount");

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 393:         if (!_isDebtIncrease && _debtChange > 0) {

 463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

 835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

 936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

 1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

 389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

 431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

 497:         while (_cnt > 0 && _id != bytes32(0)) {

 626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

 754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 315:         if (_debtIndexDiff > 0) {

 362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

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


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 93:         if (_debt > 0) {

 109:         if (_debt > 0) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 53:         if (count > 0) {

 81:         if (count > 0) {

 104:         if (count > 0) {

 135:         if (_sigs.length > 0) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 86:                 vars.remainingEbtcToRedeem > 0 &&

 87:                 _maxIterations-- > 0

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 128:         if (operation.amountToTransferIn > 0) {

 223:         if (ebtcBal > 0) {

 227:         if (collateralBal > 0) {

 293:         if (beforeSwapsLength > 0) {

 307:         if (afterSwapsLength > 0) {

```


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


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 457:         uint256 percentDeviation = maxPrice > 0

 489:             _fallbackResponse.timestamp > 0 &&

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 202:             if (maxNodes > 0 && i >= maxNodes) {

 259:             if (maxNodes > 0 && i >= maxNodes) {

 274:         if (_ownedCount > 0) {

 330:             if (maxNodes > 0 && i >= maxNodes) {

 371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

 508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

```

### <a name="GAS-50"></a>[GAS-50] Unused named return variables without optimizer waste gas
Consider changing the variable to be an unnamed one, since the variable is never assigned, nor is it returned by name. If the optimizer is not turned on, leaving the code as it is will also waste gas for the stack variable.

 There are 9 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  entireSystemDebt
 570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  pendingEBTCDebtReward
 721:     ) public view returns (uint256 pendingEBTCDebtReward) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  entireSystemColl
 67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

 /// @audit  entireSystemDebt
 75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

 /// @audit  _coll, _debt
 85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  roleName
 146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  debt, collShares
 261:     ) external view returns (uint256 debt, uint256 collShares);

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  debtToRedistribute
 549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  ds
 83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

```

### <a name="GAS-51"></a>[GAS-51] Remove or replace unused state variables
Saves a storage slot. If the variable is assigned a non-zero value, saves Gsset (20000 gas). If it’s assigned a zero value, saves Gsreset (2900 gas). If the variable remains unassigned, there is no gas savings unless the variable is public, in which case the compiler-generated non-payable getter deployment cost is saved. If the state variable is overriding an interface’s public function, mark the variable as constant or immutable so that it does not use a storage slot. 
 Note that there may be cases where a variable superficially appears to be used, but this is only because there are multiple definitions of the variable in different files. In such cases, the variable definition should be moved into a separate file. The instances below are the unused variables.

 There are 10 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 24:     string public constant NAME = "ActivePool";

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 122:     string public constant NAME = "CdpManager";

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 19:     string public constant NAME = "CollSurplusPool";

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 33:     uint256 public constant PERCENT_DIVISOR = 200; // dividing by 200 yields 0.5%

 35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 17:     bytes32 NO_ROLES = bytes32(0);

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 12:     string public constant NAME = "HintHelpers";

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 22:     string public constant NAME = "PriceFeed";

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 52:     string public constant NAME = "SortedCdps";

```

### <a name="GAS-52"></a>[GAS-52] Using bitmap to store bool states can save gas
Using a bitmap instead of a bool array or a bool mapping to store boolean states can save gas fees. This is because the bitmap can store 256 boolean values in a single slot instead of 256 slots, which can save gas when writing bool values or when reading multiple bool values from the same slot.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 751:         bool[] memory _liqFlags = new bool[](_cnt);

```

### <a name="GAS-53"></a>[GAS-53] Use constants instead of type(uintx).max
'it's generally more gas-efficient to use constants instead of type(uintX).max when you need to set the maximum value of an unsigned integer type.'

 There are 20 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 1133:         return type(uint112).max;

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 378:             _maxIterations = type(uint256).max;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 7:     uint256 public constant MAX_TCR = type(uint256).max;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 143:         if (cachedAllowance != type(uint256).max) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 76:         for (uint8 i = 0; i < type(uint8).max; i++) {

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {

 98:         for (uint8 i = 0; i < type(uint8).max; i++) {

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 79:             _maxIterations = type(uint256).max;

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 21:     ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);

 22:     stETH.approve(_borrowerOperationsAddress, type(uint256).max);

 23:     stETH.approve(_activePool, type(uint256).max);

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 39:         ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);

 40:         stETH.approve(_borrowerOperationsAddress, type(uint256).max);

 41:         stETH.approve(_activePool, type(uint256).max);

 53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);

 54:         stETH.approve(address(borrowerOperations), type(uint256).max);

 55:         stETH.approve(address(activePool), type(uint256).max);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 90:             _size = type(uint256).max;

```

### <a name="GAS-54"></a>[GAS-54] Using delete instead of setting `info` struct to 0 saves gas
using the delete keyword to clear a struct or state variable, instead of manually setting its fields to 0 or default values, can save gas. This is because delete efficiently frees up the storage slot, reducing gas costs, particularly in cases involving large or complex data structures.

 There are 5 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 272:         Cdps[_cdpId].coll = 0;

 273:         Cdps[_cdpId].debt = 0;

 274:         Cdps[_cdpId].liquidatorRewardShares = 0;

 413:         Cdps[_cdpId].stake = 0;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 109:                         vars.remainingEbtcToRedeem = 0;

```

### <a name="GAS-55"></a>[GAS-55] Use do while loops instead of for loops
A do while loop will cost less gas since the condition is not being checked for the first iteration.

 There are 15 instances:

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


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 385:         for (uint256 i; i < swapLength; ) {

 438:             for (uint256 i; i < length; ++i) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 753:         for (vars.i = _start; ; ) {

 816:         for (vars.i = _start; ; ) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 114:         for (uint256 i; i < length; ) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 432:         for (uint256 i = 0; i < _len; ++i) {

 449:         for (uint i = 0; i < _len; ++i) {

```

### <a name="GAS-56"></a>[GAS-56] unchecked {} can be used on the division of two uints in order to save gas
The division cannot overflow, since both the numerator and the denominator are non-negative

 There are 35 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 321:         return (amount * feeBps) / MAX_BPS;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 1118:         return (amount * feeBps) / MAX_BPS;

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price

 621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /

 624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

 671:         uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

 706:         return (baseRate * decayFactor) / DECIMAL_PRECISION;

 712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

 316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;

 454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

 558:         uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

 564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

 567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

 639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 108:         uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;

 119:         return (_debt * _price) / DECIMAL_PRECISION;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

 38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

 77:             } else {

 81:                 n = (n - 1) / 2;

 94:             return (_collShares * NICR_PRECISION) / _debt;

 110:             uint256 newCollRatio = (_stEthBalance * _price) / _debt;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price

```


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


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice

 534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /

 801:             (_scaledDecimal *

```

### <a name="GAS-57"></a>[GAS-57] Use unchecked block for safe subtractions
If it can be confirmed that the subtraction operation will not overflow, using an unchecked block can save gas. For example, require(x <= y); z = y - x; can be optimized to require(x <= y); unchecked { z = y - x; }.

 There are 22 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  checked on line 690
 691:             ? block.timestamp - lastRedemptionTimestamp

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  checked on line 556
 557:         uint256 deltaIndex = _newIndex - _prevIndex;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  checked on line 99
 102:             totalSurplusCollShares = cachedTotalSurplusCollShares - claimableColl;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 /// @audit  checked on line 21
 89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  checked on line 25
 89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  checked on line 89
 89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  checked on line 21
 89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  checked on line 25
 89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  checked on line 89
 89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  checked on line 144
 146:                 _approve(sender, msg.sender, cachedAllowance - amount);

 /// @audit  checked on line 165
 167:             _approve(msg.sender, spender, cachedAllowances - subtractedValue);

 /// @audit  checked on line 251
 255:             _balances[sender] = cachedSenderBalances - amount;

 /// @audit  checked on line 274
 278:             _balances[account] = cachedBalance - amount;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  checked on line 93
 113:                     vars.remainingEbtcToRedeem = vars.remainingEbtcToRedeem - currentCdpDebt;

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  checked on line 358
 359:             ? _recoveryState.entireSystemDebt - _totalDebtToBurn

 /// @audit  checked on line 361
 362:             ? _recoveryState.entireSystemColl - _totalColToSend

 /// @audit  checked on line 564
 567:         collSurplus = _totalColToSend - toLiquidator; // Can use unchecked but w/e

 /// @audit  checked on line 594
 595:                 ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)

 /// @audit  checked on line 564
 603:         collSurplus = (toLiquidator == _totalColToSend) ? 0 : _totalColToSend - toLiquidator;

 /// @audit  checked on line 602
 603:         collSurplus = (toLiquidator == _totalColToSend) ? 0 : _totalColToSend - toLiquidator;

 /// @audit  checked on line 603
 603:         collSurplus = (toLiquidator == _totalColToSend) ? 0 : _totalColToSend - toLiquidator;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  checked on line 422
 425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;

```

### <a name="GAS-58"></a>[GAS-58] `internal` functions not called by the contract should be removed
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/EBTCToken.sol

 323:     function _requireCallerIsCdpM() internal view {

```

### <a name="GAS-59"></a>[GAS-59] Use assembly to write address/contract type storage values
Using `assembly { sstore(state.slot, addr) instead of state = addr` can save gas.

 There are 26 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 53:         borrowerOperationsAddress = _borrowerOperationsAddress;

 54:         cdpManagerAddress = _cdpManagerAddress;

 56:         collSurplusPoolAddress = _collSurplusAddress;

 57:         feeRecipientAddress = _feeRecipientAddress;

 398:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 121:         feeRecipientAddress = _feeRecipientAddress;

 1148:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 229:         liquidationLibrary = _liquidationLibraryAddress;

 233:         borrowerOperationsAddress = _borrowerOperationsAddress;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 48:         borrowerOperationsAddress = _borrowerOperationsAddress;

 49:         cdpManagerAddress = _cdpManagerAddress;

 50:         activePoolAddress = _activePoolAddress;

 52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 19:         owner = _owner;

 53:         owner = newOwner;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 68:         cdpManagerAddress = _cdpManagerAddress;

 69:         borrowerOperationsAddress = _borrowerOperationsAddress;

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 29:         borrowerOperations = _borrowerOperationsAddress;

 30:         activePool = _activePool;

 31:         cdpManager = _cdpManager;

 32:         ebtcToken = _ebtc;

 33:         stETH = _coll;

 34:         sortedCdps = _sortedCdps;

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 36:         theOwner = _owner;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 45:         owner = _owner;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 96:         borrowerOperationsAddress = _borrowerOperationsAddress;

```

### <a name="GAS-60"></a>[GAS-60] Use assembly to emit events
To efficiently emit events, it’s possible to utilize assembly by making use of [scratch space](https://github.com/Vectorized/solady/blob/30558f5402f02351b96eeb6eaf32bcea29773841/src/tokens/ERC1155.sol#L501-L504) in order to save gas. This approach has the advantage of potentially avoiding the costs associated with memory expansion. However, it’s important to note that in order to safely optimize this process, it is preferable to cache and restore the free memory pointer.

 There are 57 instances:

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


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

 1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

 1171:         emit FlashLoansPaused(msg.sender, _paused);

```


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


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

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


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 83:         emit SurplusCollSharesUpdated(_account, newAmount);

 95:         emit SurplusCollSharesUpdated(_account, 0);

 104:         emit CollSharesTransferred(_account, claimableColl);

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 22:         emit OwnershipTransferred(msg.sender, _owner);

 23:         emit AuthorityUpdated(msg.sender, _authority);

 49:         emit AuthorityUpdated(msg.sender, newAuthority);

 55:         emit OwnershipTransferred(msg.sender, newOwner);

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

 62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 140:         emit CapabilityBurned(target, functionSig);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 157:         emit RoleNameSet(role, roleName);

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 56:         emit DeployNewMacro(_owner, addy);

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

 378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

 381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

 387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

 548:         emit PriceFeedStatusChanged(_status);

 555:         emit LastGoodPriceUpdated(_currentPrice);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 405:         emit NodeAdded(_id, _NICR);

 451:             emit NodeRemoved(_ids[i]);

 490:         emit NodeRemoved(_id);

```

### <a name="GAS-61"></a>[GAS-61] Use assembly to compute hashes to save gas
If the arguments to the encode call can fit into the scratch space (two words or fewer), then it’s more efficient to use assembly to generate the hash (80 gas): keccak256(abi.encodePacked(x, y)) -> assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }

 There are 9 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 33:         keccak256(
                "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"

 128:         bytes32 hashedName = keccak256(bytes(NAME));

 129:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 71:         bytes32 hashedName = keccak256(bytes(_NAME));

 72:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```

### <a name="GAS-62"></a>[GAS-62] Using assembly to check for zero can save gas
Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.

 There are 55 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 61:         if (_authorityAddress != address(0)) {

 394:             _feeRecipientAddress != address(0),

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 124:         if (_authorityAddress != address(0)) {

 735:             recoveredAddress != address(0) && recoveredAddress == _borrower,

 748:         if (_collReceived != 0) {

 808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

 808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

 819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,

 831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

 847:             _stEthBalanceDecrease == 0,

 1142:             _feeRecipientAddress != address(0),

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 159:         if (newDebt == 0) {

 369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {

 377:         if (_maxIterations == 0) {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 443:         if (totalCollateralSnapshot == 0) {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 55:         if (_authorityAddress != address(0)) {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

 56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 64:         if (_minutes == 0) {

 74:             if (n % 2 == 0) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 39:         return (uint256(getUserRoles[user]) >> role) & 1 != 0;

 47:         return (uint256(getRolesWithCapability[target][functionSig]) >> role) & 1 != 0;

 124:             if (enabledFunctionSigsByTarget[target].length() == 0) {

```


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


```solidity
File: packages/contracts/contracts/Governor.sol

 99:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

 108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 69:                 vars.currentCdpUser != address(0) &&

 78:         if (_maxIterations == 0) {

 171:         if (arrayLength == 0) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

 144:         if (_liqState.partialAmount == 0) {

 158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&

 159:                 liquidationValues.debtToBurn == 0

 417:         if (newColl == 0) {

 681:             _cdpArray.length != 0,

 863:         if (_debt == 0) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 224:             if (address(fallbackCaller) == address(0)) {

 471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

 475:         if (_response.answer == 0) {

 532:         if (minPrice == 0) return false;

 587:         if (address(fallbackCaller) != address(0)) {

 695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

 695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

 777:         if (_roundId == 0) return false;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 187:         require(facet != address(0), "Diamond: Function does not exist");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 89:         if (_size == 0) {

 305:         if (maxArraySize == 0) {

 352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

 537:         return data.size == 0;

```

### <a name="GAS-63"></a>[GAS-63] Amounts should be checked for 0 before calling a transfer
It is generally a good practice to check for zero values before making any transfers in smart contract functions. This can help to avoid unnecessary external calls and can save gas costs. Checking for zero values is especially important when transferring tokens or ether, as sending these assets to an address with a zero value will result in the loss of those assets.

 There are 7 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);

 286:         collateral.transfer(feeRecipientAddress, fee);

 381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 785:         collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

 1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 237:         IERC20(token).safeTransfer(msg.sender, amount);

```