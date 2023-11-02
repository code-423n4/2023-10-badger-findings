## Summary

### Gas Optimizations

| |Issue|Instances|Total Gas Saved|
|-|:-|:-:|:-:|
| [[GAS&#x2011;1](#gas1-multiple-accesses-of-a-mapping-array-should-use-a-local-variable-cache)] | Multiple accesses of a mapping/array should use a local variable cache | 4 | 168 | 
| [[GAS&#x2011;2](#gas2-use-assembly-to-calculate-hashes-to-save-gas)] | Use assembly to calculate hashes to save gas | 15 | 1200 | 
| [[GAS&#x2011;3](#gas3-use-assembly-to-check-for-address-0)] | Use assembly to check for `address(0)` | 29 | 174 | 
| [[GAS&#x2011;4](#gas4-optimize-address-storage-value-management-with-assembly)] | Optimize Address Storage Value Management with `assembly` | 23 | - | 
| [[GAS&#x2011;5](#gas5-use-assembly-to-emit-events)] | Use assembly to emit events | 88 | 3344 | 
| [[GAS&#x2011;6](#gas6-avoid-contract-existence-checks-by-using-low-level-calls)] | Avoid contract existence checks by using low level calls | 10 | 1000 | 
| [[GAS&#x2011;7](#gas7-using-bools-for-storage-incurs-overhead)] | Using bools for storage incurs overhead | 14 | 1400 | 
| [[GAS&#x2011;8](#gas8-cache-array-length-outside-of-loop)] | Cache array length outside of loop | 5 | 485 | 
| [[GAS&#x2011;9](#gas9-state-variables-should-be-cached-in-stack-variables-rather-than-re-reading-them-from-storage)] | State variables should be cached in stack variables rather than re-reading them from storage | 2 | 194 | 
| [[GAS&#x2011;10](#gas10-use-calldata-instead-of-memory-for-function-arguments-that-do-not-get-mutated)] | Use calldata instead of memory for function arguments that do not get mutated | 4 | - | 
| [[GAS&#x2011;11](#gas11-add-unchecked-for-subtractions-where-the-operands-cannot-underflow-because-of-a-previous-require-or-if-statement)] | Add `unchecked {}` for subtractions where the operands cannot underflow because of a previous `require()` or `if`-statement | 13 | 1105 | 
| [[GAS&#x2011;12](#gas12-don-t-compare-boolean-expressions-to-boolean-literals)] | Don't compare boolean expressions to boolean literals | 1 | 9 | 
| [[GAS&#x2011;13](#gas13-use-custom-errors-rather-than-revert-require-strings-to-save-gas)] | Use custom errors rather than `revert()`/`require()` strings to save gas | 148 | - | 
| [[GAS&#x2011;14](#gas14-divisions-which-do-not-divide-by-x-cannot-overflow-or-overflow-so-such-operations-can-be-unchecked-to-save-gas)] | Divisions which do not divide by -X cannot overflow or overflow so such operations can be unchecked to save gas | 35 | - | 
| [[GAS&#x2011;15](#gas15-do-not-calculate-constants)] | Do not calculate constants | 1 | - | 
| [[GAS&#x2011;16](#gas16-stack-variable-cost-less-while-used-in-emiting-event)] | Stack variable cost less while used in emiting event | 9 | 900 | 
| [[GAS&#x2011;17](#gas17-superfluous-event-fields)] | Superfluous event fields | 3 | - | 
| [[GAS&#x2011;18](#gas18-events-should-be-emitted-outside-of-loops)] | Events should be emitted outside of loops | 1 | 375 | 
| [[GAS&#x2011;19](#gas19-the-result-of-function-calls-should-be-cached-rather-than-re-calling-the-function)] | The result of function calls should be cached rather than re-calling the function | 1 | - | 
| [[GAS&#x2011;20](#gas20-require-or-revert-statements-that-check-input-arguments-should-be-at-the-top-of-the-function)] | `require()` or `revert()` statements that check input arguments should be at the top of the function | 3 | - | 
| [[GAS&#x2011;21](#gas21-internal-functions-only-called-once-can-be-inlined-to-save-gas)] | `internal` functions only called once can be inlined to save gas | 75 | 1500 | 
| [[GAS&#x2011;22](#gas22-internal-functions-not-called-by-the-contract-should-be-removed-to-save-deployment-gas)] | `internal` functions not called by the contract should be removed to save deployment gas | 6 | - | 
| [[GAS&#x2011;23](#gas23-require-revert-strings-longer-than-32-bytes-cost-extra-gas)] | `require()`/`revert()` strings longer than 32 bytes cost extra gas | 115 | 2070 | 
| [[GAS&#x2011;24](#gas24-consider-merging-sequential-for-loops)] | Consider merging sequential for loops | 4 | - | 
| [[GAS&#x2011;25](#gas25-reduce-gas-usage-by-moving-to-solidity-0-8-19-or-later)] | Reduce gas usage by moving to Solidity 0.8.19 or later | 39 | - | 
| [[GAS&#x2011;26](#gas26-multiple-address-id-mappings-can-be-combined-into-a-single-mapping-of-an-address-id-to-a-struct-where-appropriate)] | Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`, where appropriate | 6 | - | 
| [[GAS&#x2011;27](#gas27-optimize-names-to-save-gas)] | Optimize names to save gas | 37 | 814 | 
| [[GAS&#x2011;28](#gas28-not-using-the-named-return-variables-anywhere-in-the-function-is-confusing)] | Not using the named return variables anywhere in the function is confusing | 8 | - | 
| [[GAS&#x2011;29](#gas29-structs-can-be-packed-into-fewer-storage-slots)] | Structs can be packed into fewer storage slots | 3 | 6000 | 
| [[GAS&#x2011;30](#gas30-constructors-can-be-marked-payable)] | Constructors can be marked `payable` | 19 | 399 | 
| [[GAS&#x2011;31](#gas31-using-private-rather-than-public-for-constants-saves-gas)] | Using `private` rather than `public` for constants, saves gas | 31 | - | 
| [[GAS&#x2011;32](#gas32-private-functions-only-called-once-can-be-inlined-to-save-gas)] | `private` functions only called once can be inlined to save gas | 2 | - | 
| [[GAS&#x2011;33](#gas33-remove-or-replace-unused-state-variables)] | Remove or replace unused state variables | 2 | - | 
| [[GAS&#x2011;34](#gas34-redundant-else-statement)] | Redundant else statement | 11 | - | 
| [[GAS&#x2011;35](#gas35-avoid-updating-storage-when-the-value-hasn-t-changed-to-save-gas)] | Avoid updating storage when the value hasn't changed to save gas | 21 | 16800 | 
| [[GAS&#x2011;36](#gas36-use-shift-right-instead-of-division-if-possible-to-save-gas)] | Use shift Right instead of division if possible to save gas | 3 | 60 | 
| [[GAS&#x2011;37](#gas37-use-shift-left-instead-of-multiplication-if-possible-to-save-gas)] | Use shift Left instead of multiplication if possible to save gas | 1 | - | 
| [[GAS&#x2011;38](#gas38-usage-of-uints-ints-smaller-than-32-bytes-256-bits-incurs-overhead)] | Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead | 43 | - | 
| [[GAS&#x2011;39](#gas39-the-use-of-a-logical-and-in-place-of-double-if-is-slightly-less-gas-efficient-in-instances-where-there-isn-t-a-corresponding-else-statement-for-the-given-if-statement)] | The use of a logical AND in place of double if is slightly less gas efficient in instances where there isn't a corresponding else statement for the given if statement | 14 | 210 | 
| [[GAS&#x2011;40](#gas40-splitting-require-statements-that-use-saves-gas)] | Splitting `require()` statements that use `&&` saves gas | 8 | 24 | 
| [[GAS&#x2011;41](#gas41-stack-variable-used-as-a-cheaper-cache-for-a-state-variable-is-only-used-once)] | Stack variable used as a cheaper cache for a state variable is only used once | 1 | 3 | 
| [[GAS&#x2011;42](#gas42-cache-state-variables-outside-of-loop-to-avoid-reading-storage-on-every-iteration)] | Cache state variables outside of loop to avoid reading storage on every iteration | 8 | - | 
| [[GAS&#x2011;43](#gas43-costs-less-gas-than)] | `>=`/`<=` costs less gas than `>`/`<` | 113 | 339 | 
| [[GAS&#x2011;44](#gas44-ternary-unnecessary)] | Ternary unnecessary | 3 | - | 
| [[GAS&#x2011;45](#gas45-use-assembly-to-validate-msg-sender)] | Use assembly to validate `msg.sender` | 39 | 468 | 
| [[GAS&#x2011;46](#gas46-can-make-the-variable-outside-the-loop-to-save-gas)] | Can make the variable outside the loop to save gas | 16 | - | 
| [[GAS&#x2011;47](#gas47-i-costs-less-gas-than-i-especially-when-it-s-used-in-for-loops-i-i-too)] | `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) | 15 | - | 
| [[GAS&#x2011;48](#gas48-structs-can-be-packed-into-fewer-storage-slots-by-truncating-timestamp-bytes)] | Structs can be packed into fewer storage slots by truncating timestamp bytes | 2 | - | 
| [[GAS&#x2011;49](#gas49-stat-variables-can-be-packed-into-fewer-storage-slots-by-truncating-timestamp-bytes)] | Stat variables can be packed into fewer storage slots by truncating timestamp bytes | 1 | - | 
| [[GAS&#x2011;50](#gas50-using-mappings-instead-of-arrays-to-avoid-length-checks-save-gas)] | Using mappings instead of arrays to avoid length checks save gas | 1 | - | 
| [[GAS&#x2011;51](#gas51-state-variables-can-be-packed-into-fewer-storage-slots)] | State variables can be packed into fewer storage slots | 2 | 4000 | 
| [[GAS&#x2011;52](#gas52-use-do-while-loops-instead-of-for-loops)] | Use `do while` loops instead of `for` loops | 15 | 1815 | 
| [[GAS&#x2011;53](#gas53-use-for-mapping-s)] | Use `+=` for `mapping`s | 2 | - | 
| [[GAS&#x2011;54](#gas54-avoid-transferring-amounts-of-zero-in-order-to-save-gas)] | Avoid transferring amounts of zero in order to save gas | 4 | - | 
| [[GAS&#x2011;55](#gas55-when-no-addresses-are-used-abi-encodepacked-outperforms-abi-encode-in-efficiency)] | When no `addresses` are used `abi.encodepacked()` Outperforms `abi.encode()` in Efficiency | 2 | 122 | 
| [[GAS&#x2011;56](#gas56-simple-checks-for-zero-uint-can-be-done-using-assembly-to-save-gas)] | Simple checks for zero `uint` can be done using assembly to save gas | 31 | 186 | 
| [[GAS&#x2011;57](#gas57-i-i-should-be-unchecked-i-unchecked-i-when-it-is-not-possible-for-them-to-overflow-as-is-the-case-when-used-in-for-and-while-loops)] | `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops | 10 | - | 

Total: 1122 instances over 57 issues with **45164 gas** saved




## Gas Optimizations

### [GAS&#x2011;1] Multiple accesses of a mapping/array should use a local variable cache 
The instances below point to the second+ access of a value inside a mapping/array, within a function. Caching a mapping's value in a local `storage` or `calldata` variable when the value is accessed [multiple times](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0), saves **~42 gas per access** due to not having to recalculate the key's keccak256 hash (Gkeccak256 - **30 gas**) and that calculation's associated stack operations. Caching an array's struct avoids recalculating the array offsets into memory/calldata


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

// @audit Cdps[_cdpId]
272:         Cdps[_cdpId].coll = 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L272-L272) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

// @audit capabilityFlag[target]
98:             capabilityFlag[target][functionSig] = CapabilityFlag.None;

// @audit getRolesWithCapability[target]
113:             getRolesWithCapability[target][functionSig] |= bytes32(1 << role);

// @audit enabledFunctionSigsByTarget[target]
114:             enabledFunctionSigsByTarget[target].add(bytes32(functionSig));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L98-L98) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L113-L113), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L114-L114)


</details>


### [GAS&#x2011;2] Use assembly to calculate hashes to save gas 
Using assembly to calculate hashes can save *** 80 gas *** per instance


*There are 15 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

33:         keccak256(

128:         bytes32 hashedName = keccak256(bytes(NAME));

129:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

682:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

717:         bytes32 digest = keccak256(

721:                 keccak256(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L33-L33) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L128-L128), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L129-L129), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L682-L682), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L717-L717), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L721-L721)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

71:         bytes32 hashedName = keccak256(bytes(_NAME));

72:         bytes32 hashedVersion = keccak256(bytes(_VERSION));

209:         bytes32 digest = keccak256(

240:         return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

213:                 keccak256(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L71-L71) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L72-L72), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L209-L209), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L240-L240), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L213-L213)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L182-L182) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L37-L37) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L39-L39) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11-L11) 


</details>


### [GAS&#x2011;3] Use assembly to check for `address(0)` 
*Saves 6 gas per instance*


*There are 29 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

61:         if (_authorityAddress != address(0)) {

394:             _feeRecipientAddress != address(0),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L61-L61) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L394-L394)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

124:         if (_authorityAddress != address(0)) {

1142:             _feeRecipientAddress != address(0),

735:             recoveredAddress != address(0) && recoveredAddress == _borrower,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L124-L124) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1142-L1142), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L735-L735)


```solidity

File: packages/contracts/contracts/CdpManager.sol

497:         while (_cnt > 0 && _id != bytes32(0)) {

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L497-L497) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L389-L389), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L369-L369)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L756-L756) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L819-L819)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

55:         if (_authorityAddress != address(0)) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L55-L55) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L247-L247) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L248-L248), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L263-L263), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L271-L271), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L286-L286), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L287-L287), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L297-L297)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

363:         if (_fallbackCaller != address(0)) {

587:         if (address(fallbackCaller) != address(0)) {

224:             if (address(fallbackCaller) == address(0)) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L363-L363) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L587-L587), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L224-L224)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

69:                 vars.currentCdpUser != address(0) &&

85:                 vars.currentCdpUser != address(0) &&


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L69-L69) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L85-L85)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

187:         require(facet != address(0), "Diamond: Function does not exist");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L187-L187) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

38:             (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L38-L38) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L56-L56) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35-L35)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

158:             if (getUserRoles[user] == bytes32(0)) {

75:             return bytes32(0) != getUserRoles[user] & getRolesWithCapability[target][functionSig];


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L158-L158) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L75-L75)


</details>


### [GAS&#x2011;4] Optimize Address Storage Value Management with `assembly` 



*There are 23 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

53:         borrowerOperationsAddress = _borrowerOperationsAddress;

54:         cdpManagerAddress = _cdpManagerAddress;

56:         collSurplusPoolAddress = _collSurplusAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L53-L53) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L54-L54), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L56-L56)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

121:         feeRecipientAddress = _feeRecipientAddress;

1148:         feeRecipientAddress = _feeRecipientAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L121-L121) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1148-L1148)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

229:         liquidationLibrary = _liquidationLibraryAddress;

233:         borrowerOperationsAddress = _borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L229-L229) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L233-L233)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

48:         borrowerOperationsAddress = _borrowerOperationsAddress;

49:         cdpManagerAddress = _cdpManagerAddress;

50:         activePoolAddress = _activePoolAddress;

52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L48-L48) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L50-L50), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L52-L52)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

68:         cdpManagerAddress = _cdpManagerAddress;

69:         borrowerOperationsAddress = _borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L68-L68) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L69-L69)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

96:         borrowerOperationsAddress = _borrowerOperationsAddress;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L96-L96) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

29:         borrowerOperations = _borrowerOperationsAddress;

30:         activePool = _activePool;

31:         cdpManager = _cdpManager;

32:         ebtcToken = _ebtc;

33:         stETH = _coll;

34:         sortedCdps = _sortedCdps;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L29-L29) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L30-L30), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L34-L34)


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

36:         theOwner = _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L36-L36) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

19:         owner = _owner;

53:         owner = newOwner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L53-L53)


</details>


### [GAS&#x2011;5] Use assembly to emit events 
We can use assembly to emit events efficiently by utilizing `scratch space` and the `free memory pointer`. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.


*There are 88 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L65-L65) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L112-L112), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L113-L113), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L145-L145), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L146-L146), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L173-L173), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L174-L174), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L200-L200), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L213-L213), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L247-L247), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L307-L307), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L360-L360), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L383-L383), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L399-L399), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L412-L412), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L421-L421)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

1162:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

1171:         emit FlashLoansPaused(msg.sender, _paused);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L136-L136) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L641-L641), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1105-L1105), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1149-L1149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1162-L1162), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1171-L1171)


```solidity

File: packages/contracts/contracts/CdpManager.sol

55:         emit StakingRewardSplitSet(stakingRewardSplit);

466:         emit Redemption(

545:         emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);

630:         emit BaseRateUpdated(newBaseRate);

681:         emit BaseRateUpdated(decayedBaseRate);

782:         emit StakingRewardSplitSet(_stakingRewardSplit);

801:         emit RedemptionFeeFloorSet(_redemptionFeeFloor);

824:         emit MinuteDecayFactorSet(_minuteDecayFactor);

836:         emit BetaSet(_beta);

848:         emit RedemptionsPaused(_paused);

925:         emit CdpUpdated(

961:         emit CdpUpdated(

220:             emit CdpUpdated(

698:             emit LastRedemptionTimestampUpdated(block.timestamp);

179:                 emit CdpUpdated(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L55-L55) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L466-L466), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L545-L545), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L630-L630), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L681-L681), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L782-L782), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L801-L801), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L824-L824), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L836-L836), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L848-L848), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L925-L925), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L961-L961), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L220-L220), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L698-L698), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L179-L179)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

238:         emit CdpUpdated(

281:         emit CdpLiquidated(

312:         emit CdpUpdated(

367:         emit CdpLiquidated(

490:         emit CdpUpdated(

516:         emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);

891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);

437:             emit CdpPartiallyLiquidated(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L238-L238) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L281-L281), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L312-L312), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L367-L367), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L490-L490), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L516-L516), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L891-L891), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L437-L437)


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

587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

602:         emit CdpFeeSplitApplied(

55:             emit GracePeriodStart();

69:             emit GracePeriodEnd();

390:             emit CdpUpdated(

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L50-L50) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L64-L64), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L119-L119), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L300-L300), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L340-L340), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L414-L414), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L425-L425), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L481-L481), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L587-L587), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L602-L602), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L55-L55), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L69-L69), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L390-L390), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L542-L542)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

83:         emit SurplusCollSharesUpdated(_account, newAmount);

95:         emit SurplusCollSharesUpdated(_account, 0);

104:         emit CollSharesTransferred(_account, claimableColl);

150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L83-L83) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L95-L95), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L104-L104), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L150-L150)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

259:         emit Transfer(sender, recipient, amount);

267:         emit Transfer(address(0), account, amount);

282:         emit Transfer(account, address(0), amount);

290:         emit Approval(owner, spender, amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L259-L259) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L267-L267), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L282-L282), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L290-L290)


```solidity

File: packages/contracts/contracts/Governor.sol

157:         emit RoleNameSet(role, roleName);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L157-L157) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

67:         emit FallbackCallerChanged(address(0), _fallbackCallerAddress);

548:         emit PriceFeedStatusChanged(_status);

555:         emit LastGoodPriceUpdated(_currentPrice);

387:             emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);

378:                     emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L67-L67) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L548-L548), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L555-L555), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L387-L387), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L381-L381), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L378-L378)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

405:         emit NodeAdded(_id, _NICR);

490:         emit NodeRemoved(_id);

451:             emit NodeRemoved(_ids[i]);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L405-L405) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L490-L490), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L451-L451)


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

56:         emit DeployNewMacro(_owner, addy);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L56-L56) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

22:         emit OwnershipTransferred(msg.sender, _owner);

23:         emit AuthorityUpdated(msg.sender, _authority);

49:         emit AuthorityUpdated(msg.sender, newAuthority);

55:         emit OwnershipTransferred(msg.sender, newOwner);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L23-L23), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L49-L49), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L55-L55)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

50:         emit AuthorityUpdated(msg.sender, Authority(newAuthority));

62:         emit AuthorityUpdated(address(this), Authority(newAuthority));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L50-L50) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L62-L62)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

140:         emit CapabilityBurned(target, functionSig);

163:         emit UserRoleUpdated(user, role, enabled);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L101-L101) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L129-L129), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L140-L140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L163-L163)


</details>


### [GAS&#x2011;6] Avoid contract existence checks by using low level calls 
Prior to 0.8.10 the compiler inserted extra code, including `EXTCODESIZE` (100 gas), to check for contract existence for external function calls. In more recent solidity versions, the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low level calls never check for contract existence


*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

//@audit syncGlobalAccountingAndGracePeriod() 
347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

//@audit syncGlobalAccountingAndGracePeriod() 
372:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

//@audit syncGlobalAccountingAndGracePeriod() 
391:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

//@audit syncGlobalAccountingAndGracePeriod() 
405:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

//@audit syncGlobalAccountingAndGracePeriod() 
418:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First

//@audit authority() 
60:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L347-L347) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L372-L372), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L391-L391), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L405-L405), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L418-L418), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L60-L60)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit locked() 
244:             ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,

//@audit getOwnerAddress() 
392:                 ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L244-L244) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L392-L392)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

//@audit feeRecipientAddress() 
52:         feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

//@audit authority() 
54:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L54-L54)


</details>


### [GAS&#x2011;7] Using bools for storage incurs overhead 
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from 'false' to 'true', after having been 'true' in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).


*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit change `isCollIncrease` to `uint256`
72:     struct AdjustCdpLocals {
73:         uint256 price;
74:         uint256 collSharesChange;
75:         uint256 netDebtChange;
76:         bool isCollIncrease;
77:         uint256 debt;
78:         uint256 collShares;
79:         uint256 oldICR;
80:         uint256 newICR;
81:         uint256 newTCR;
82:         uint256 newDebt;
83:         uint256 newCollShares;
84:         uint256 stake;
85:     }

//@audit change `isCollIncrease` to `uint256`
//@audit change `isDebtIncrease` to `uint256`
097:     struct MoveTokensParams {
098:         address user;
099:         uint256 collSharesChange;
100:         uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101:         bool isCollIncrease;
102:         uint256 netDebtChange;
103:         bool isDebtIncrease;
104:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L72-L85) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L97-L104)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit avoid using `bool` type for redemptionsPaused
143:     bool public redemptionsPaused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L143-L143) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit change `_isDebtIncrease` to `uint256`
322:     struct AdjustCdpOperation {
323:         bytes32 _cdpId;
324:         uint256 _stEthBalanceDecrease;
325:         uint256 _EBTCChange;
326:         bool _isDebtIncrease;
327:         bytes32 _upperHint;
328:         bytes32 _lowerHint;
329:         uint256 _stEthBalanceIncrease;
330:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L322-L330) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

//@audit change `allowNonCallback` to `uint256`
//@audit change `callbackEnabledForCall` to `uint256`
28:     struct OurSettings {
29:         bool allowNonCallback;
30:         bool callbackEnabledForCall;
31:     }

//@audit change `checkSuccess` to `uint256`
//@audit change `capGas` to `uint256`
099:     struct Operation {
100:         address to; // Target to call
101:         bool checkSuccess; // If false we will ignore a revert
102:         uint128 value; // How much ETH to send
103:         uint128 gas; // How much gas to send
104:         bool capGas; // true to use above "gas" setting or we send gasleft()
105:         OperationType opType; // See `OperationType`
106:         bytes data; // Calldata to send (funsig + data)
107:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L28-L31) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

//@audit avoid using `bool` type for _authorityInitialized
14:     bool private _authorityInitialized;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L14-L14) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

//@audit avoid using `bool` type for flashLoansPaused
15:     bool public flashLoansPaused;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L15-L15) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

//@audit change `recoveryModeAtStart` to `uint256`
118:     struct LiquidationLocals {
119:         bytes32 cdpId;
120:         uint256 partialAmount; // used only for partial liquidation, default 0 means full liquidation
121:         uint256 price;
122:         uint256 ICR;
123:         bytes32 upperPartialHint;
124:         bytes32 lowerPartialHint;
125:         bool recoveryModeAtStart;
126:         uint256 TCR;
127:         uint256 totalSurplusCollShares;
128:         uint256 totalCollSharesToSend;
129:         uint256 totalDebtToBurn;
130:         uint256 totalDebtToRedistribute;
131:         uint256 totalLiquidatorRewardCollShares;
132:     }

//@audit change `recoveryModeAtStart` to `uint256`
147:     struct LocalVariables_OuterLiquidationFunction {
148:         uint256 price;
149:         bool recoveryModeAtStart;
150:         uint256 liquidatedDebt;
151:         uint256 liquidatedColl;
152:     }

//@audit change `backToNormalMode` to `uint256`
154:     struct LocalVariables_LiquidationSequence {
155:         uint256 i;
156:         uint256 ICR;
157:         bytes32 cdpId;
158:         bool backToNormalMode;
159:         uint256 entireSystemDebt;
160:         uint256 entireSystemColl;
161:         uint256 price;
162:         uint256 TCR;
163:     }

//@audit change `cancelledPartial` to `uint256`
//@audit change `fullRedemption` to `uint256`
208:     struct SingleRedemptionValues {
209:         uint256 debtToRedeem;
210:         uint256 collSharesDrawn;
211:         uint256 collSurplus;
212:         uint256 liquidatorRewardShares;
213:         bool cancelledPartial;
214:         bool fullRedemption;
215:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L118-L132) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L147-L152), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L154-L163), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L208-L215)


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

//@audit change `success` to `uint256`
17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }

//@audit change `success` to `uint256`
26:     struct FallbackResponse {
27:         uint256 answer;
28:         uint256 timestamp;
29:         bool success;
30:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30)


</details>


### [GAS&#x2011;8] Cache array length outside of loop 
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L46-L46) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L137-L137)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

292:         uint256 beforeSwapsLength = operation.swapsBefore.length;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L292-L292) 


</details>


### [GAS&#x2011;9] State variables should be cached in stack variables rather than re-reading them from storage 
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

*Saves 100 gas per instance*


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

1103:         ebtcToken.burn(feeRecipientAddress, amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1103-L1103) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

384:             address oldFallbackCaller = address(fallbackCaller);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L384-L384) 


</details>


### [GAS&#x2011;10] Use calldata instead of memory for function arguments that do not get mutated 
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit Make `_cdpArray` as a calldata
126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L126-L126) 


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit Make `roleIds` as a calldata
120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L120-L120) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

//@audit Make `_ids` as a calldata
419:     function batchRemove(bytes32[] memory _ids) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L419-L419) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

//@audit Make `_ids` as a calldata
16:     function batchRemove(bytes32[] memory _ids) external;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L16-L16) 


</details>


### [GAS&#x2011;11] Add `unchecked {}` for subtractions where the operands cannot underflow because of a previous `require()` or `if`-statement 
`require(a <= b); x = b - a` => `require(a <= b); unchecked { x = b - a }`


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

289:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

567:         collSurplus = _totalColToSend - toLiquidator; // Can use unchecked but w/e

603:         collSurplus = (toLiquidator == _totalColToSend) ? 0 : _totalColToSend - toLiquidator;

595:                 ? _totalDebtToBurn - _debtToRepay //  Bad Debt (to be redistributed) is (CdpDebt - Repaid)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L289-L289) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L375-L375), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L444-L444), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L567-L567), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L603-L603), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L595-L595)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

557:         uint256 deltaIndex = _newIndex - _prevIndex;

632:             (_systemStEthFeePerUnitIndex - _cdpStEthFeePerUnitIndex);

639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L557-L557) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L632-L632), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L639-L639)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

799:             : 10 ** (_ethBtcDecimals - _stEthEthDecimals);

798:             ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L799-L799) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L798-L798)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

89:         return (_a >= _b) ? (_a - _b) : (_b - _a);

89:         return (_a >= _b) ? (_a - _b) : (_b - _a);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L89-L89) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L89-L89)


</details>


### [GAS&#x2011;12] Don't compare boolean expressions to boolean literals 
`if (<x> == true)` => `if (<x>)`, `if (<x> == false)` => `if (!<x>)`


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

The left expression is already a boolean expression
332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L332-L332) 


</details>


### [GAS&#x2011;13] Use custom errors rather than `revert()`/`require()` strings to save gas 
Custom errors are available from solidity version 0.8.4. Custom errors save [**~50 gas**](https://gist.github.com/IllIllI000/ad1bd0d29a0101b25e57c293b4b0c746) each time they're hit by [avoiding having to allocate and store the revert string](https://blog.soliditylang.org/2021/04/21/custom-errors/#errors-in-depth). Not defining the strings also save deployment gas


*There are 148 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L104-L104) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L137-L137), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L162-L162), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L220-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L228-L231), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L236-L236), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L267-L267), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L269-L269), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L277-L280), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L294-L297), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L298-L301), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L302-L305), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L318-L318), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L319-L319), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L350-L353), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L374-L374), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L377-L377), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L393-L396), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L407-L407)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L145-L145) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L146-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L368-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L463-L463), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L541-L544), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L715-L715), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L734-L737), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L807-L810), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L818-L821), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L826-L826), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L831-L831), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L835-L835), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L839-L842), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L846-L849), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L911-L914), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L918-L918), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L922-L925), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L929-L932), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L936-L936), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L940-L943), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L947-L950), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L957-L960), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L970-L973), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1083-L1083), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1085-L1085), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1091-L1094), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1115-L1115), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1116-L1116), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1155-L1155)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L332-L332) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L431-L431), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L502-L502), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L503-L506), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L626-L626), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L672-L672), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L678-L678), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L743-L746), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L747-L750), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L754-L754), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L758-L758), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L762-L765), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L774-L777), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L789-L792), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L793-L796), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L808-L811), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L812-L815)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

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


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L56-L56) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L680-L683), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L710-L710), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L901-L905), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L909-L912), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L82-L85), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L89-L92), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L93-L97), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L477-L480)


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

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L112-L115) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L242-L242), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L243-L246), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L261-L264), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L466-L469), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L475-L475), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L556-L556), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L584-L584), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L649-L649), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L653-L656), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L660-L663), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L453-L453)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L92-L92) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L99-L99), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L113-L116), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L120-L120), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L124-L124), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L143-L143), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L146-L146)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

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

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L165-L165) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L208-L208), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L219-L219), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L247-L247), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L248-L248), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L251-L251), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L263-L263), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L271-L271), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L274-L274), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L286-L286), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L287-L287), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L296-L299), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L300-L303), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L307-L310), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L315-L320), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L324-L324), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L144-L144)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L79-L83) 


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

458:         require(contains(_id), "SortedCdps: List does not contain the id");

506:         require(contains(_id), "SortedCdps: List does not contain the id");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

720:         require(
721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722:             "SortedCdps: Caller is neither BO nor CdpM"
723:         );

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L352-L352) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L365-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L367-L367), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L369-L369), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L371-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L422-L422), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L427-L430), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L458-L458), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L506-L506), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L508-L508), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L715-L715), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L720-L723), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L433-L433)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

45:         require(owner() == msg.sender, "Must be owner");

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

421:         require(success, "Call has failed");

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

362:             require(
363:                 msg.sender == address(activePool),
364:                 "LeverageMacroReference: wrong lender for stETH flashloan"
365:             );

356:             require(
357:                 msg.sender == address(borrowerOperations),
358:                 "LeverageMacroReference: wrong lender for eBTC flashloan"
359:             );

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L352-L352), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L421-L421), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L179-L182), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L191-L194), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L201-L204), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L362-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L356-L359), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L249-L249), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L440-L444), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L251-L251), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L253-L253)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

111:         require(msg.sender == owner, "Must be owner");

187:         require(facet != address(0), "Diamond: Function does not exist");

179:             require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L111-L111) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L187-L187), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L179-L179)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

27:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L27-L27) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

17:         require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

56:         require(address(_authority) == address(0), "Auth: authority is non-zero");

57:         require(!_authorityInitialized, "Auth: authority already initialized");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17-L17) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L56-L56), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L57-L57)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

109:         require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L109-L109) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14-L14) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90-L93) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134-L137)


</details>


### [GAS&#x2011;14] Divisions which do not divide by -X cannot overflow or overflow so such operations can be unchecked to save gas 
Make such found divisions are unchecked when ensured it is safe to do so


*There are 35 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

321:         return (amount * feeBps) / MAX_BPS;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L321-L321) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

1118:         return (amount * feeBps) / MAX_BPS;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1118-L1118) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /

671:         uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

706:         return (baseRate * decayFactor) / DECIMAL_PRECISION;

146:             (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price

624:         uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L621-L621) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L671-L671), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L706-L706), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L146-L146), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L624-L624), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L712-L712)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

278:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

365:         uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;

435:             uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

592:             uint256 _debtToRepay = (_incentiveColl * _price) / LICR;

558:             _incentiveColl = (_totalDebtToBurn * LICR) / _price;

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L278-L278) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L365-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L882-L882), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L435-L435), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L592-L592), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L558-L558), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L555-L555), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L579-L579)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

558:         uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;

567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;

454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L558-L558), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L564-L564), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L567-L567), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L316-L316), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L454-L454), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L639-L639)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /

801:             (_scaledDecimal *

458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L534-L534) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L801-L801), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L458-L458)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

145:             (maxRedeemableEBTC * DECIMAL_PRECISION) / _price


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L145-L145) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

108:         uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;

119:         return (_debt * _price) / DECIMAL_PRECISION;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L108-L108) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L119-L119)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

94:             return (_collShares * NICR_PRECISION) / _debt;

110:             uint256 newCollRatio = (_stEthBalance * _price) / _debt;

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

81:                 n = (n - 1) / 2;

76:                 n = n / 2;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L38-L38) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L94-L94), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L110-L110), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L38-L38), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L81-L81), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L76-L76)


</details>


### [GAS&#x2011;15] Do not calculate constants 
Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141) 


</details>


### [GAS&#x2011;16] Stack variable cost less while used in emiting event 
Even if the variable is going to be used only one time, caching a state variable and use its cache in an emit would help you reduce the cost by at least ***9 gas***


*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

// @audit `stakingRewardSplit` is a state variable
55:         emit StakingRewardSplitSet(stakingRewardSplit);

// @audit `Cdps` is a state variable
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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L55-L55) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L220-L230)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

// @audit `Cdps` is a state variable
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

// @audit `Cdps` is a state variable
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

// @audit `Cdps` is a state variable
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

// @audit `systemDebtRedistributionIndex` is a state variable
891:         emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L490-L500) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L490-L500), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L490-L500), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L891-L891)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

// @audit `feeRecipientAddress` is a state variable
150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L150-L150) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

// @audit `owner` is a state variable
290:         emit Approval(owner, spender, amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L290-L290) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

// @audit `_authority` is a state variable
23:         emit AuthorityUpdated(msg.sender, _authority);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L23-L23) 


</details>


### [GAS&#x2011;17] Superfluous event fields 
`block.timestamp` and `block.number` are added to event information by default so adding them manually wastes gas


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

698:             emit LastRedemptionTimestampUpdated(block.timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L698-L698) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L542-L542) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

381:                 emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L381-L381) 


</details>


### [GAS&#x2011;18] Events should be emitted outside of loops 
Emitting an event has an overhead of **375 gas**, which will be incurred on every iteration of the loop. It is cheaper to `emit` only [once](https://github.com/ethereum/EIPs/blob/adad5968fd6de29902174e0cb51c8fc3dceb9ab5/EIPS/eip-1155.md?plain=1#L68) after the loop has finished.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SortedCdps.sol

//@audit NodeRemoved is emited inside this loop
449:         for (uint i = 0; i < _len; ++i) {
450:             delete data.nodes[_ids[i]];
451:             emit NodeRemoved(_ids[i]);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L449-L451) 


</details>


### [GAS&#x2011;19] The result of function calls should be cached rather than re-calling the function 
The instances below point to the second+ call of the function within a single function


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

// @audit sortedCdps.nonExistId() is called 2 times in the function `_isValidFirstRedemptionHint`
272:     function _isValidFirstRedemptionHint(
273:         bytes32 _firstRedemptionHint,
274:         uint256 _price
275:     ) internal view returns (bool) {
276:         if (
277:             _firstRedemptionHint == sortedCdps.nonExistId() ||
278:             !sortedCdps.contains(_firstRedemptionHint) ||
279:             getSyncedICR(_firstRedemptionHint, _price) < MCR
280:         ) {
281:             return false;
282:         }
283: 
284:         bytes32 nextCdp = sortedCdps.getNext(_firstRedemptionHint);
285:         return nextCdp == sortedCdps.nonExistId() || getSyncedICR(nextCdp, _price) < MCR;
286:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L272-L286) 


</details>


### [GAS&#x2011;20] `require()` or `revert()` statements that check input arguments should be at the top of the function 



*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SortedCdps.sol

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {
364:         // List must not be full
365:         require(!isFull(), "SortedCdps: List is full");
366:         // List must not already contain node
367:         require(!contains(_id), "SortedCdps: List already contains the node");
368:         // Node id must not be null
369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");

363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {
364:         // List must not be full
365:         require(!isFull(), "SortedCdps: List is full");
366:         // List must not already contain node
367:         require(!contains(_id), "SortedCdps: List already contains the node");
368:         // Node id must not be null
369:         require(_id != dummyId, "SortedCdps: Id cannot be zero");
370:         // NICR must be non-zero
371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

498:     function reInsert(
499:         bytes32 _id,
500:         uint256 _newNICR,
501:         bytes32 _prevId,
502:         bytes32 _nextId
503:     ) external override {
504:         _requireCallerIsBOorCdpM();
505:         // List must contain the node
506:         require(contains(_id), "SortedCdps: List does not contain the id");
507:         // NICR must be non-zero
508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L363-L369) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L363-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L498-L508)


</details>


### [GAS&#x2011;21] `internal` functions only called once can be inlined to save gas 
Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.


*There are 75 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

219:     function _requireCallerIsBorrowerOperations() internal view {

235:     function _requireCallerIsCdpManager() internal view {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L219-L219) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L235-L235)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L744-L747) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L760-L760), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L803-L806), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L813-L817), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L829-L829), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L834-L834), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L838-L838), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L845-L845), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L852-L857), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L921-L921), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L946-L946), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L986-L989), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1004-L1012)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L135-L137) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L244-L250), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L272-L275), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L489-L493), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L550-L550), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L595-L599), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L612-L616), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L655-L655), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L737-L741), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L753-L753), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L757-L757), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L761-L761), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L977-L977), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L984-L984)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

135:     function _liquidateIndividualCdpSetupCDP(
136:         LiquidationLocals memory _liqState,
137:         LiquidationRecoveryModeLocals memory _recoveryState
138:     ) internal {

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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L135-L138) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L450-L454), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L466-L471), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L642-L648), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L733-L738), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L807-L811), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L862-L862), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L896-L900), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L908-L908)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L73-L73) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L260-L260), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L327-L327), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L336-L336), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L410-L410), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L431-L431), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L441-L441), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L463-L463), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L539-L539), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L574-L578), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L592-L598), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L652-L652), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L895-L895)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

112:     function _requireCallerIsBorrowerOperations() internal view {

119:     function _requireCallerIsCdpManager() internal view {

123:     function _requireCallerIsActivePool() internal view {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L112-L112) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L119-L119), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L123-L123)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

262:     function _mint(address account, uint256 amount) internal {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L262-L262) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

582:     function _getCurrentFallbackResponse()
583:         internal
584:         view
585:         returns (FallbackResponse memory fallbackResponse)
586:     {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L582-L586) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L642-L642) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

133:     function _calculateCdpStateAfterPartialRedemption(
134:         LocalVariables_getRedemptionHints memory vars,
135:         uint256 currentCdpDebt,
136:         uint256 _price
137:     ) internal view returns (uint256, uint256) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L133-L137) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L398-L398) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L435-L435), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L450-L450), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L460-L460), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L474-L474), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L482-L482), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L498-L504)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

134:     function _executeOne(Operation calldata op) internal {

174:     function _fallback() internal {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L134-L134) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L174-L174)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L32-L32) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L30-L30) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L75-L75) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L79-L79), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L83-L85), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L134-L134), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L140-L140)


</details>


### [GAS&#x2011;22] `internal` functions not called by the contract should be removed to save deployment gas 
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

306:     function _requireCallerIsBorrowerOperations() internal view {

323:     function _requireCallerIsCdpM() internal view {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L306-L306) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L323-L323)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

103:     function _requireUserAcceptsFee(

115:     function _convertDebtDenominationToBtc(

124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L95-L95) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L103-L103), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L115-L115), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L124-L124)


</details>


### [GAS&#x2011;23] `require()`/`revert()` strings longer than 32 bytes cost extra gas 
Each extra memory word of bytes past the original 32 [incurs an MSTORE](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#consider-having-short-revert-strings) which costs **3 gas**


*There are 115 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");
138:         uint256 totalShares = _shares + _liquidatorRewardShares;

162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");
163:         unchecked {

220:         require(
221:             msg.sender == borrowerOperationsAddress,
222:             "ActivePool: Caller is not BorrowerOperations"
223:         );

228:         require(
229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230:             "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231:         );

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
237:     }

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
375: 

377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");
378: 

393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );

407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");
408: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L137-L138) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L162-L163), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L220-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L228-L231), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L236-L237), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L277-L280), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L302-L305), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L350-L353), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L374-L375), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L377-L378), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L393-L396), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L407-L408)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

145:         require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");
146:         require(

146:         require(
147:             ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148:             "CdpManager: Reentrancy in nonReentrant call"
149:         );

368:         require(
369:             _stEthBalanceDecrease <= _cdpStEthBalance,
370:             "BorrowerOperations: Cannot withdraw greater stEthBalance than the value in Cdp"
371:         );

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");
464: 

541:         require(
542:             vars.netStEthBalance + LIQUIDATOR_REWARD == _stEthBalance,
543:             "BorrowerOperations: deposited collateral mismatch!"
544:         );

715:         require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");
716: 

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
827:     }

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");
832:     }

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");
836:     }

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
919:     }

922:         require(
923:             _newICR >= _oldICR,
924:             "BorrowerOperations: Cannot decrease your Cdp's ICR in Recovery Mode"
925:         );

929:         require(
930:             _newTCR >= CCR,
931:             "BorrowerOperations: An operation that would result in TCR < CCR is not permitted"
932:         );

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");
937:     }

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
1117: 

1141:         require(
1142:             _feeRecipientAddress != address(0),
1143:             "BorrowerOperations: Cannot set feeRecipient to zero address"
1144:         );

1155:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");
1156: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L145-L146) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L146-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L368-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L463-L464), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L541-L544), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L715-L716), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L734-L737), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L807-L810), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L818-L821), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L826-L827), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L831-L832), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L835-L836), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L839-L842), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L846-L849), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L911-L914), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L918-L919), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L922-L925), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L929-L932), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L936-L937), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L940-L943), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L947-L950), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L957-L960), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L970-L973), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1116-L1117), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1141-L1144), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1155-L1156)


```solidity

File: packages/contracts/contracts/CdpManager.sol

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");
432: 

502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");
503:         require(

503:         require(
504:             _toRemoveIds[_total - 1] == _end,
505:             "CdpManager: batchRemoveSortedCdpIds check end error"
506:         );

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption
627: 

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");
673:         return redemptionFee;

743:         require(
744:             callerBalance >= _amount,
745:             "CdpManager: Requested redemption amount must be <= user's EBTC token balance"
746:         );

747:         require(
748:             callerBalance <= _totalSupply,
749:             "CdpManager: redeemer's EBTC balance exceeds total supply!"
750:         );

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");
755:     }

758:         require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");
759:     }

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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L431-L432) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L502-L503), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L503-L506), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L626-L627), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L672-L673), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L743-L746), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L747-L750), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L754-L755), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L758-L759), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L762-L765), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L774-L777), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L789-L792), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L793-L796), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L808-L811), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L812-L815)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");
57:         _liquidateIndividualCdpSetup(_cdpId, _partialAmount, _upperPartialHint, _lowerPartialHint);

680:         require(
681:             _cdpArray.length != 0,
682:             "LiquidationLibrary: Calldata address array must not be empty"
683:         );

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");
711: 

901:         require(
902:             (_partialDebt + _convertDebtDenominationToBtc(MIN_NET_STETH_BALANCE, _price)) <=
903:                 _entireDebt,
904:             "LiquidationLibrary: Partial debt liquidated must be less than total debt"
905:         );

909:         require(
910:             _entireColl >= MIN_NET_STETH_BALANCE,
911:             "LiquidationLibrary: Coll remaining in partially liquidated CDP must be >= minimum"
912:         );

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


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L56-L57) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L680-L683), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L710-L711), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L901-L905), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L909-L912), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L82-L85), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L89-L92), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L93-L97), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L477-L480)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );

242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");
243:         require(

243:         require(
244:             ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245:             "BorrowerOperations: Reentrancy in nonReentrant call"
246:         );

261:         require(
262:             closedStatus != Status.nonExistent && closedStatus != Status.active,
263:             "CdpManagerStorage: close non-exist or non-active CDP!"
264:         );

466:         require(
467:             cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468:             "CdpManagerStorage: remove non-exist or non-active CDP!"
469:         );

475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");
476: 

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");
557:         uint256 deltaIndex = _newIndex - _prevIndex;

649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");
650:     }

653:         require(
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655:             "CdpManager: Only one cdp in the system"
656:         );

660:         require(
661:             msg.sender == borrowerOperationsAddress,
662:             "CdpManager: Caller is not the BorrowerOperations contract"
663:         );

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L112-L115) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L242-L243), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L243-L246), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L261-L264), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L466-L469), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L475-L476), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L556-L557), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L649-L650), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L653-L656), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L660-L663), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L453-L454)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");
93: 

113:         require(
114:             msg.sender == borrowerOperationsAddress,
115:             "CollSurplusPool: Caller is not Borrower Operations"
116:         );

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");
121:     }

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
125:     }

143:         require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");
144: 

146:         require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");
147: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L92-L93) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L113-L116), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L120-L121), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L124-L125), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L143-L144), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L146-L147)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

165:         require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");
166:         unchecked {

251:         require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");
252: 

263:         require(account != address(0), "EBTCToken: mint to zero recipient!");
264: 

271:         require(account != address(0), "EBTCToken: burn from zero account!");
272: 

274:         require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");
275: 

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

144:             require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");
145:             unchecked {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L165-L166) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L251-L252), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L263-L264), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L271-L272), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L274-L275), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L296-L299), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L300-L303), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L307-L310), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L315-L320), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L144-L145)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L79-L83) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");
353: 

367:         require(!contains(_id), "SortedCdps: List already contains the node");
368:         // Node id must not be null

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");
372: 

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");
423: 

427:         require(
428:             _firstPrev != dummyId || _lastNext != dummyId,
429:             "SortedCdps: batchRemove() leave ZERO node left!"
430:         );

458:         require(contains(_id), "SortedCdps: List does not contain the id");
459: 

506:         require(contains(_id), "SortedCdps: List does not contain the id");
507:         // NICR must be non-zero

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");
509: 

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");
716:     }

720:         require(
721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
722:             "SortedCdps: Caller is neither BO nor CdpM"
723:         );

433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");
434:         }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L352-L353) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L367-L368), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L371-L372), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L422-L423), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L427-L430), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L458-L459), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L506-L507), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L508-L509), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L715-L716), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L720-L723), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L433-L434)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

352:         require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");
353: 

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

362:             require(
363:                 msg.sender == address(activePool),
364:                 "LeverageMacroReference: wrong lender for stETH flashloan"
365:             );

356:             require(
357:                 msg.sender == address(borrowerOperations),
358:                 "LeverageMacroReference: wrong lender for eBTC flashloan"
359:             );

249:             require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");
250:         } else if (check.operator == Operator.lte) {

440:                 require(
441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >
442:                         swapChecks[i].expectedMinOut,
443:                     "LeverageMacroReference: swap check failure!"
444:                 );

251:             require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");
252:         } else if (check.operator == Operator.equal) {

253:             require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");
254:         } else {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L352-L353) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L179-L182), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L191-L194), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L201-L204), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L362-L365), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L356-L359), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L249-L250), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L440-L444), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L251-L252), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L253-L254)


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

57:         require(!_authorityInitialized, "Auth: authority already initialized");
58: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L57-L58) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

14:         require(locked == OPEN, "ReentrancyGuard: Reentrancy in nonReentrant call");
15: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L14-L15) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L90-L93) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L134-L137)


</details>


### [GAS&#x2011;24] Consider merging sequential for loops 
Merging multiple `for` loops within a function in Solidity can enhance efficiency and reduce gas costs, especially when they share a common iterating variable or perform related operations. By minimizing redundant iterations over the same data set, execution becomes more cost-effective. However, while merging can optimize gas usage and simplify logic, it may also increase code complexity. Therefore, careful balance between optimization and maintainability is essential, along with thorough testing to ensure the refactored code behaves as expected.


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {
47:             address user = users.at(i);
48:             bool _canCall = doesUserHaveRole(user, role);
49:             if (_canCall) {
50:                 count += 1;
51:             }
52:         }
53:         if (count > 0) {
54:             uint256 j = 0;
55:             usersWithRole = new address[](count);
56:             address[] memory _usrs = users.values();
57:             for (uint256 i = 0; i < _usrs.length; i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {
77:             if (doesUserHaveRole(user, i)) {
78:                 count += 1;
79:             }
80:         }
81:         if (count > 0) {
82:             uint256 j = 0;
83:             rolesForUser = new uint8[](count);
84:             for (uint8 i = 0; i < type(uint8).max; i++) {

098:         for (uint8 i = 0; i < type(uint8).max; i++) {
099:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
100:             if (roleEnabled) {
101:                 count += 1;
102:             }
103:         }
104:         if (count > 0) {
105:             uint256 j = 0;
106:             roleIds = new uint8[](count);
107:             for (uint8 i = 0; i < type(uint8).max; i++) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L46-L57) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L76-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L98-L107)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

432:         for (uint256 i = 0; i < _len; ++i) {
433:             require(contains(_ids[i]), "SortedCdps: List does not contain the id");
434:         }
435: 
436:         // orphan nodes in between to save gas
437:         if (_firstPrev != dummyId) {
438:             data.nodes[_firstPrev].nextId = _lastNext;
439:         } else {
440:             data.head = _lastNext;
441:         }
442:         if (_lastNext != dummyId) {
443:             data.nodes[_lastNext].prevId = _firstPrev;
444:         } else {
445:             data.tail = _firstPrev;
446:         }
447: 
448:         // delete node & owner storages to get gas refund
449:         for (uint i = 0; i < _len; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L432-L449) 


</details>


### [GAS&#x2011;25] Reduce gas usage by moving to Solidity 0.8.19 or later 
See [this](https://blog.soliditylang.org/2023/02/22/solidity-0.8.19-release-announcement/#preventing-dead-code-in-runtime-bytecode) link for the full details


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Governor.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ReentrancyGuard.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L3-L3) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

2: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L2-L2) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

3: pragma solidity 0.8.17;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L3-L3) 


</details>


### [GAS&#x2011;26] Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`, where appropriate 
Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (**20000 gas**) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save **~42 gas per access** due to [not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0) (Gkeccak256 - 30 gas) and that calculation's associated stack operations.


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

51:     mapping(address => uint256) private _balances;

52:     mapping(address => mapping(address => uint256)) private _allowances;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L51-L51) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L52-L52)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

32:     mapping(address => bytes32) public getUserRoles;

34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L28-L28) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34-L34), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L36-L36)


</details>


### [GAS&#x2011;27] Optimize names to save gas 
`public`/`external` function names and `public` member variable names can be optimized to save gas. See [this](https://gist.github.com/IllIllI000/a5d8b486a8259f9f77891a919febd1a9) link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save **128 gas** each during deployment, and renaming functions to have lower method IDs will save **22 gas** per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92)


*There are 37 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

// @audit sweepToken(address,uint256) ==> sweepToken_anC(address,uint256),0000226a
// @audit setFeeBps(uint256) ==> setFeeBps_97K(uint256),00007071
// @audit setFlashLoansPaused(bool) ==> setFlashLoansPaused_14b(bool),0000a339
22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L22-L22) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

// @audit DOMAIN_SEPARATOR() ==> DOMAIN_SEPARATOR_5BT(),0000ecd0
// @audit setFeeRecipientAddress(address) ==> setFeeRecipientAddress_Vkn(address),0000bbe9
// @audit setFeeBps(uint256) ==> setFeeBps_97K(uint256),00007071
// @audit setFlashLoansPaused(bool) ==> setFlashLoansPaused_14b(bool),0000a339
21: contract BorrowerOperations is


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

// @audit getSystemDebt() ==> getSystemDebt_7b1Y(),00006f32
// @audit getDeploymentStartTime() ==> getDeploymentStartTime_Xj(),00006002
// @audit checkPotentialRecoveryMode(uint256,uint256,uint256) ==> checkPotentialRecoveryMode_CkN(uint256,uint256,uint256),0000a3a8
// @audit setStakingRewardSplit(uint256) ==> setStakingRewardSplit_vhT(uint256),00001edf
// @audit setRedemptionFeeFloor(uint256) ==> setRedemptionFeeFloor_037(uint256),00008e8d
// @audit setMinuteDecayFactor(uint256) ==> setMinuteDecayFactor_W81(uint256),0000d419
// @audit setBeta(uint256) ==> setBeta_p4U(uint256),0000e0bf
// @audit setRedemptionsPaused(bool) ==> setRedemptionsPaused_rqp(bool),00003d0e
16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

// @audit liquidate(bytes32) ==> liquidate_14S(bytes32),00008ba3
// @audit partiallyLiquidate(bytes32,uint256,bytes32,bytes32) ==> partiallyLiquidate_L6K(bytes32,uint256,bytes32,bytes32),0000af3e
// @audit batchLiquidateCdps(bytes32[]) ==> batchLiquidateCdps_I9V(bytes32[]),0000948b
13: contract LiquidationLibrary is CdpManagerStorage {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

// @audit setGracePeriod(uint128) ==> setGracePeriod_J3w(uint128),00002354
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

// @audit sweepToken(address,uint256) ==> sweepToken_anC(address,uint256),0000226a
16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

// @audit DOMAIN_SEPARATOR() ==> DOMAIN_SEPARATOR_5BT(),0000ecd0
26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L26-L26) 


```solidity

File: packages/contracts/contracts/Governor.sol

// @audit getUsersByRole(uint8) ==> getUsersByRole_L69(uint8),00002b10
// @audit getRolesForUser(address) ==> getRolesForUser_Hdb(address),00004ae8
// @audit getRolesFromByteMap(bytes32) ==> getRolesFromByteMap_f7d(bytes32),0000b52b
// @audit getByteMapFromRoles(uint8[]) ==> getByteMapFromRoles_J16(uint8[]),00004ea5
// @audit getEnabledFunctionsInTarget(address) ==> getEnabledFunctionsInTarget_O1R(address),00008766
// @audit getRoleName(uint8) ==> getRoleName_G8J(uint8),00007ee3
// @audit setRoleName(uint8,string) ==> setRoleName_ftm(uint8,string),0000e01b
13: contract Governor is RolesAuthority {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

// @audit setFallbackCaller(address) ==> setFallbackCaller_X7v(address),0000d700
21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L21-L21) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

// @audit toCdpId(address,uint256,uint256) ==> toCdpId_PJ(address,uint256,uint256),00002ee4
51: contract SortedCdps is ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L51-L51) 


```solidity

File: packages/contracts/contracts/HintHelpers.sol

// @audit getRedemptionHints(uint256,uint256,uint256) ==> getRedemptionHints_Cbn(uint256,uint256,uint256),000045e5
// @audit getApproxHint(uint256,uint256,uint256) ==> getApproxHint_Bbx(uint256,uint256,uint256),0000253d
// @audit computeNominalCR(uint256,uint256) ==> computeNominalCR_keq(uint256,uint256),0000045f
// @audit computeCR(uint256,uint256,uint256) ==> computeCR_EkK(uint256,uint256,uint256),0000e1d1
11: contract HintHelpers is EbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

// @audit Cdps(bytes32) ==> Cdps_OdL(bytes32),0000c7df
14: interface ICdpCdps {

// @audit owner() ==> owner_ZdW(),000030c3
// @audit sweepToCaller() ==> sweepToCaller_Xge(),00000633
// @audit sweepToken(address,uint256) ==> sweepToken_anC(address,uint256),0000226a
// @audit decodeFLData(bytes) ==> decodeFLData_NkO(bytes),0000fdc6
// @audit onFlashLoan(address,address,uint256,uint256,bytes) ==> onFlashLoan_gdG(address,address,uint256,uint256,bytes),0000d01a
26: contract LeverageMacroBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L14-L14) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L26-L26)


```solidity

File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

// @audit owner() ==> owner_ZdW(),000030c3
6: interface IOwnerLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/LeverageMacroFactory.sol

// @audit deployNewMacro() ==> deployNewMacro_C8a(),0000d1d7
// @audit deployNewMacro(address) ==> deployNewMacro_w1v(address),00009a31
11: contract LeverageMacroFactory {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

// @audit resetApprovals() ==> resetApprovals_Z4L(),0000fce9
11: contract LeverageMacroReference is LeverageMacroBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L11-L11) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

// @audit setFallbackHandler(bytes4,address) ==> setFallbackHandler_cqv(bytes4,address),0000f97e
// @audit setAllowAnyCall(bool) ==> setAllowAnyCall_IqS(bool),00005b72
// @audit enableCallbackForCall() ==> enableCallbackForCall_Nc1(),0000793d
25: contract SimplifiedDiamondLike {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L25-L25) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

// @audit transferOwnership(address) ==> transferOwnership_m0(address),0000e7f1
9: abstract contract Auth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

// @audit authority() ==> authority_Ede(),000090c5
// @audit authorityInitialized() ==> authorityInitialized_5dC(),0000a210
// @audit setAuthority(address) ==> setAuthority_2rv(address),00005d7e
10: contract AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L10-L10) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

// @audit getSystemCollShares() ==> getSystemCollShares_7f1F(),0000b6c4
16: contract EbtcBase is BaseMath, IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L16-L16) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

// @audit doesUserHaveRole(address,uint8) ==> doesUserHaveRole_5qv(address,uint8),0000b854
// @audit doesRoleHaveCapability(uint8,address,bytes4) ==> doesRoleHaveCapability_j2M(uint8,address,bytes4),000081cc
// @audit isPublicCapability(address,bytes4) ==> isPublicCapability_vi3(address,bytes4),000002ed
// @audit setPublicCapability(address,bytes4,bool) ==> setPublicCapability_f3k(address,bytes4,bool),0000f55c
// @audit setRoleCapability(uint8,address,bytes4,bool) ==> setRoleCapability_1dq(uint8,address,bytes4,bool),0000ea02
// @audit burnCapability(address,bytes4) ==> burnCapability_Z1N(address,bytes4),0000feb5
// @audit setUserRole(address,uint8,bool) ==> setUserRole_Eu4(address,uint8,bool),000068ed
12: contract RolesAuthority is IRolesAuthority, Auth, Authority {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/Interfaces/IActivePool.sol

// @audit transferSystemCollShares(address,uint256) ==> transferSystemCollShares_6fq(address,uint256),00002f80
// @audit increaseSystemCollShares(uint256) ==> increaseSystemCollShares_1h(uint256),000073e1
// @audit transferSystemCollSharesAndLiquidatorReward(address,uint256,uint256) ==> transferSystemCollSharesAndLiquidatorReward_HzI(address,uint256,uint256),0000c867
// @audit allocateSystemCollSharesToFeeRecipient(uint256) ==> allocateSystemCollSharesToFeeRecipient_T72(uint256),000000af
// @audit claimFeeRecipientCollShares(uint256) ==> claimFeeRecipientCollShares_zJb(uint256),000077a7
// @audit feeRecipientAddress() ==> feeRecipientAddress_eoH(),000010a7
// @audit getFeeRecipientClaimableCollShares() ==> getFeeRecipientClaimableCollShares_jma(),00006918
// @audit setFeeRecipientAddress(address) ==> setFeeRecipientAddress_Vkn(address),0000bbe9
7: interface IActivePool is IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IActivePool.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

// @audit openCdp(uint256,bytes32,bytes32,uint256) ==> openCdp_eV(uint256,bytes32,bytes32,uint256),00001735
// @audit openCdpFor(uint256,bytes32,bytes32,uint256,address) ==> openCdpFor_ci1(uint256,bytes32,bytes32,uint256,address),00009898
// @audit addColl(bytes32,bytes32,bytes32,uint256) ==> addColl_C7Z(bytes32,bytes32,bytes32,uint256),0000c15d
// @audit withdrawColl(bytes32,uint256,bytes32,bytes32) ==> withdrawColl_lL(bytes32,uint256,bytes32,bytes32),000094b1
// @audit withdrawDebt(bytes32,uint256,bytes32,bytes32) ==> withdrawDebt_Z8d(bytes32,uint256,bytes32,bytes32),00005bf4
// @audit repayDebt(bytes32,uint256,bytes32,bytes32) ==> repayDebt_AoE(bytes32,uint256,bytes32,bytes32),000079b2
// @audit closeCdp(bytes32) ==> closeCdp_7mC(bytes32),00009a5a
// @audit adjustCdp(bytes32,uint256,uint256,bool,bytes32,bytes32) ==> adjustCdp_c8z(bytes32,uint256,uint256,bool,bytes32,bytes32),0000e604
// @audit adjustCdpWithColl(bytes32,uint256,uint256,bool,bytes32,bytes32,uint256) ==> adjustCdpWithColl_ocQ(bytes32,uint256,uint256,bool,bytes32,bytes32,uint256),0000db74
// @audit claimSurplusCollShares() ==> claimSurplusCollShares_K7i(),0000f007
// @audit feeRecipientAddress() ==> feeRecipientAddress_eoH(),000010a7
7: interface IBorrowerOperations is IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IBorrowerOperations.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManager.sol

// @audit getActiveCdpsCount() ==> getActiveCdpsCount_x2G(),0000bf03
// @audit getIdFromCdpIdsArray(uint256) ==> getIdFromCdpIdsArray_FOe(uint256),00000ac6
// @audit liquidate(bytes32) ==> liquidate_14S(bytes32),00008ba3
// @audit partiallyLiquidate(bytes32,uint256,bytes32,bytes32) ==> partiallyLiquidate_L6K(bytes32,uint256,bytes32,bytes32),0000af3e
// @audit batchLiquidateCdps(bytes32[]) ==> batchLiquidateCdps_I9V(bytes32[]),0000948b
// @audit redeemCollateral(uint256,bytes32,bytes32,bytes32,uint256,uint256,uint256) ==> redeemCollateral_95z(uint256,bytes32,bytes32,bytes32,uint256,uint256,uint256),00008aa9
// @audit updateStakeAndTotalStakes(bytes32) ==> updateStakeAndTotalStakes_k2j(bytes32),00002a2e
// @audit syncAccounting(bytes32) ==> syncAccounting_A86(bytes32),0000a8af
// @audit closeCdp(bytes32,address,uint256,uint256) ==> closeCdp_qL1(bytes32,address,uint256,uint256),0000b6ab
// @audit getRedemptionRate() ==> getRedemptionRate_Pdf(),00008902
// @audit getRedemptionRateWithDecay() ==> getRedemptionRateWithDecay_sis(),00007308
// @audit getRedemptionFeeWithDecay(uint256) ==> getRedemptionFeeWithDecay_Z51U(uint256),0000ce0b
// @audit getCdpStatus(bytes32) ==> getCdpStatus_v6G(bytes32),00004f11
// @audit getCdpStake(bytes32) ==> getCdpStake_rvo(bytes32),00000786
// @audit getCdpDebt(bytes32) ==> getCdpDebt_E6s(bytes32),000050d9
// @audit getCdpCollShares(bytes32) ==> getCdpCollShares_q1K(bytes32),0000f98a
// @audit getCdpLiquidatorRewardShares(bytes32) ==> getCdpLiquidatorRewardShares_ThL(bytes32),000078b6
// @audit initializeCdp(bytes32,uint256,uint256,uint256,address) ==> initializeCdp_zi1(bytes32,uint256,uint256,uint256,address),00001541
// @audit updateCdp(bytes32,address,uint256,uint256,uint256,uint256) ==> updateCdp_gGC(bytes32,address,uint256,uint256,uint256,uint256),000086a1
// @audit getCachedTCR(uint256) ==> getCachedTCR_A7f(uint256),0000afe4
9: interface ICdpManager is IEbtcBase, ICdpManagerData {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManager.sol#L9-L9) 


```solidity

File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

// @audit totalStakes() ==> totalStakes_tb2(),00004f48
// @audit ebtcToken() ==> ebtcToken_dY(),0000e4fc
// @audit systemStEthFeePerUnitIndex() ==> systemStEthFeePerUnitIndex_F8e(),0000d864
// @audit systemStEthFeePerUnitIndexError() ==> systemStEthFeePerUnitIndexError_i1d(),0000fafb
// @audit stEthIndex() ==> stEthIndex_pEA(),0000a408
// @audit calcFeeUponStakingReward(uint256,uint256) ==> calcFeeUponStakingReward_11U(uint256,uint256),0000c99a
// @audit syncGlobalAccounting() ==> syncGlobalAccounting_BHK(),0000331f
// @audit syncGlobalAccountingAndGracePeriod() ==> syncGlobalAccountingAndGracePeriod_F9g(),0000e88a
// @audit getAccumulatedFeeSplitApplied(bytes32,uint256) ==> getAccumulatedFeeSplitApplied_x2m(bytes32,uint256),0000c7e5
// @audit getCachedNominalICR(bytes32) ==> getCachedNominalICR_Ec(bytes32),00007380
// @audit getCachedICR(bytes32,uint256) ==> getCachedICR_t6C(bytes32,uint256),00007f0d
// @audit getSyncedCdpDebt(bytes32) ==> getSyncedCdpDebt_N52(bytes32),00009c5f
// @audit getSyncedCdpCollShares(bytes32) ==> getSyncedCdpCollShares_4bb(bytes32),0000577c
// @audit getSyncedICR(bytes32,uint256) ==> getSyncedICR_Op2(bytes32,uint256),0000e9a4
// @audit getSyncedTCR(uint256) ==> getSyncedTCR_G3E(uint256),0000a070
// @audit getSyncedNominalICR(bytes32) ==> getSyncedNominalICR_R6p(bytes32),0000fdc1
// @audit getPendingRedistributedDebt(bytes32) ==> getPendingRedistributedDebt_m45(bytes32),00002a3b
// @audit hasPendingRedistributedDebt(bytes32) ==> hasPendingRedistributedDebt_6df(bytes32),0000756d
// @audit getSyncedDebtAndCollShares(bytes32) ==> getSyncedDebtAndCollShares_DtZ(bytes32),00009460
// @audit canLiquidateRecoveryMode(uint256,uint256) ==> canLiquidateRecoveryMode_n4l(uint256,uint256),00005e36
13: interface ICdpManagerData is IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L13-L13) 


```solidity

File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

// @audit getTotalSurplusCollShares() ==> getTotalSurplusCollShares_wdY(),0000e482
// @audit getSurplusCollShares(address) ==> getSurplusCollShares_011C(address),0000a558
// @audit increaseSurplusCollShares(address,uint256) ==> increaseSurplusCollShares_F7C(address,uint256),00006464
// @audit increaseTotalSurplusCollShares(uint256) ==> increaseTotalSurplusCollShares_pix(uint256),00001fc2
5: interface ICollSurplusPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ICollSurplusPool.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

// @audit priceFeed() ==> priceFeed_pcG(),000086ac
7: interface IEbtcBase {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEbtcBase.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

// @audit mint(address,uint256) ==> mint_Qgo(address,uint256),00001784
// @audit burn(address,uint256) ==> burn_J8M(address,uint256),0000b783
8: interface IEBTCToken is IERC20, IERC2612 {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IEBTCToken.sol#L8-L8) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

// @audit onFlashLoan(address,address,uint256,uint256,bytes) ==> onFlashLoan_gdG(address,address,uint256,uint256,bytes),0000d01a
5: interface IERC3156FlashBorrower {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

// @audit maxFlashLoan(address) ==> maxFlashLoan_qcx(address),00001837
// @audit flashFee(address,uint256) ==> flashFee_crX(address,uint256),000010c1
7: interface IERC3156FlashLender {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L7-L7) 


```solidity

File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

// @audit getFallbackResponse() ==> getFallbackResponse_f2z(),0000fbbf
// @audit fallbackTimeout() ==> fallbackTimeout_8dW(),000089fa
// @audit setFallbackTimeout(uint256) ==> setFallbackTimeout_Wb8(uint256),0000d728
5: interface IFallbackCaller {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IFallbackCaller.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

// @audit increasePermitNonce() ==> increasePermitNonce_Ej3(),0000a926
// @audit nonces(address) ==> nonces_bpo(address),000097e9
5: interface IPermitNonce {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPermitNonce.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPool.sol

// @audit getSystemCollShares() ==> getSystemCollShares_7f1F(),0000b6c4
// @audit getSystemDebt() ==> getSystemDebt_7b1Y(),00006f32
// @audit increaseSystemDebt(uint256) ==> increaseSystemDebt_t3k(uint256),000076d1
// @audit decreaseSystemDebt(uint256) ==> decreaseSystemDebt_K9(uint256),0000df1b
6: interface IPool {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPool.sol#L6-L6) 


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

// @audit getPositionManagerApproval(address,address) ==> getPositionManagerApproval_Xci(address,address),00009a8d
// @audit revokePositionManagerApproval(address) ==> revokePositionManagerApproval_4ka(address),00008f7d
// @audit renouncePositionManagerApproval(address) ==> renouncePositionManagerApproval_b2O(address),000032ab
// @audit version() ==> version_Z5x(),00005021
// @audit permitTypeHash() ==> permitTypeHash_SeU(),0000999f
// @audit domainSeparator() ==> domainSeparator_d1Z(),00006ab3
5: interface IPositionManagers {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

// @audit fetchPrice() ==> fetchPrice_RqI(),0000a472
5: interface IPriceFeed {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

// @audit notifyStartGracePeriod(uint256) ==> notifyStartGracePeriod_mkt(uint256),00000d4a
// @audit notifyEndGracePeriod(uint256) ==> notifyEndGracePeriod_3eC(uint256),0000158e
5: interface IRecoveryModeGracePeriod {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol#L5-L5) 


```solidity

File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

// @audit remove(bytes32) ==> remove_W2k(bytes32),000062f0
// @audit batchRemove(bytes32[]) ==> batchRemove_viR(bytes32[]),00008505
// @audit reInsert(bytes32,uint256,bytes32,bytes32) ==> reInsert_E7i(bytes32,uint256,bytes32,bytes32),00008dd4
// @audit contains(bytes32) ==> contains_m1H(bytes32),0000b2f8
// @audit isFull() ==> isFull_dIX(),00002d8f
// @audit isEmpty() ==> isEmpty_K2k(),0000cbd5
// @audit getSize() ==> getSize_XbR(),00003496
// @audit getMaxSize() ==> getMaxSize_Xv(),0000ed98
// @audit getFirst() ==> getFirst_osV(),00001f40
// @audit getLast() ==> getLast_IbC(),00004f7b
// @audit getNext(bytes32) ==> getNext_ffX(bytes32),0000e4af
// @audit getPrev(bytes32) ==> getPrev_91L(bytes32),00006a06
// @audit validInsertPosition(uint256,bytes32,bytes32) ==> validInsertPosition_hpR(uint256,bytes32,bytes32),00006049
// @audit findInsertPosition(uint256,bytes32,bytes32) ==> findInsertPosition_m8P(uint256,bytes32,bytes32),0000c8a2
// @audit insert(address,uint256,bytes32,bytes32) ==> insert_u1R(address,uint256,bytes32,bytes32),00005937
// @audit getOwnerAddress(bytes32) ==> getOwnerAddress_22D(bytes32),0000dd8d
// @audit nonExistId() ==> nonExistId_F8I(),00007bac
// @audit cdpCountOf(address) ==> cdpCountOf_6il(address),00008f53
// @audit getCdpCountOf(address,bytes32,uint256) ==> getCdpCountOf_8eQ(address,bytes32,uint256),00005321
// @audit getCdpsOf(address) ==> getCdpsOf_qmF(address),0000a7c6
// @audit getAllCdpsOf(address,bytes32,uint256) ==> getAllCdpsOf_Svx(address,bytes32,uint256),0000190a
// @audit cdpOfOwnerByIndex(address,uint256) ==> cdpOfOwnerByIndex_d3O(address,uint256),00007636
// @audit cdpOfOwnerByIdx(address,uint256,bytes32,uint256) ==> cdpOfOwnerByIdx_KyL(address,uint256,bytes32,uint256),00008db7
6: interface ISortedCdps {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/ISortedCdps.sol#L6-L6) 


</details>


### [GAS&#x2011;28] Not using the named return variables anywhere in the function is confusing 
Consider changing the variable to be an unnamed one, since the variable is never assigned, nor is it returned by name. If the optimizer is not turned on, leaving the code as it is will also waste gas for the stack variable.


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

// @audit entireSystemDebt
570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L570-L570) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

// @audit debtToRedistribute
544:     function _calculatePartialLiquidationSurplusAndCap(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L544-L544) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

// @audit pendingEBTCDebtReward
719:     function getPendingRedistributedDebt(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L719-L719) 


```solidity

File: packages/contracts/contracts/Governor.sol

// @audit roleName
146:     function getRoleName(uint8 role) external view returns (string memory roleName) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L146-L146) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

// @audit ds
83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L83-L83) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

// @audit entireSystemColl
67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

// @audit entireSystemDebt
75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

// @audit _coll
// @audit _debt
83:     function _getTCRWithSystemDebtAndCollShares(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L67-L67) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L75-L75), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L83-L83)


</details>


### [GAS&#x2011;29] Structs can be packed into fewer storage slots 
Each slot saved can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

// @audit from 6 to 4 you need to change the structure elements order to: , uint256, uint256, uint256, address, bool, bool
097:     struct MoveTokensParams {
098:         address user;
099:         uint256 collSharesChange;
100:         uint256 collAddUnderlying; // ONLY for isCollIncrease=true
101:         bool isCollIncrease;
102:         uint256 netDebtChange;
103:         bool isDebtIncrease;
104:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L97-L104) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

// @audit from 6 to 5 you need to change the structure elements order to: , uint256, bytes, address, address, address, array
268:     struct SwapOperation {
269:         // Swap Data
270:         address tokenForSwap;
271:         address addressForApprove;
272:         uint256 exactApproveAmount;
273:         address addressForSwap;
274:         bytes calldataForSwap;
275:         SwapCheck[] swapChecks; // Empty to skip
276:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L268-L276) 


```solidity

File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

// @audit from 5 to 4 you need to change the structure elements order to: , uint256, uint256, uint256, uint80, uint80, bool
17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24) 


</details>


### [GAS&#x2011;30] Constructors can be marked `payable` 
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided.A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.


*There are 19 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L46-L52) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L107-L116) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L30-L52) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L14-L34) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L217-L227) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

42:     constructor(
43:         address _borrowerOperationsAddress,
44:         address _cdpManagerAddress,
45:         address _activePoolAddress,
46:         address _collTokenAddress
47:     ) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L42-L47) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

61:     constructor(
62:         address _cdpManagerAddress,
63:         address _borrowerOperationsAddress,
64:         address _authorityAddress
65:     ) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L61-L65) 


```solidity

File: packages/contracts/contracts/Governor.sol

36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
37: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L36-L37) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

57:     constructor(
58:         address _fallbackCallerAddress,
59:         address _authorityAddress,
60:         address _collEthCLFeed,
61:         address _ethBtcCLFeed
62:     ) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L57-L62) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {
89:         if (_size == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L88-L89) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L27-L33) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L51-L59) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41-L58) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroFactory.sol#L21-L28) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L17-L35) 


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

44:     constructor(address _owner) {
45:         owner = _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L44-L45) 


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

18:     constructor(address _owner, Authority _authority) {
19:         owner = _owner;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L18-L19) 


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {
53:         activePool = IActivePool(_activePoolAddress);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L52-L53) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}
21: 


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20-L21) 


</details>


### [GAS&#x2011;31] Using `private` rather than `public` for constants, saves gas 
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table


*There are 31 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

24:     string public constant NAME = "ActivePool";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L24-L24) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

29:     string public constant NAME = "BorrowerOperations";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L29-L29) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L21-L21) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L139-L139), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L141-L141), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L149-L149), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L150-L150)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

19:     string public constant NAME = "CollSurplusPool";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L19-L19) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

22:     string public constant NAME = "PriceFeed";

32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L22-L22) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L32-L32), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L36-L36), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L42-L42)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

52:     string public constant NAME = "SortedCdps";

80:     bytes32 public constant dummyId =


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L80-L80)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

12:     string public constant NAME = "HintHelpers";


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L12-L12) 


```solidity

File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

9:     uint256 public constant MAX_BPS = 10_000;

10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L9-L9) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L10-L10), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11-L11)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L19-L19) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L22-L22), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L25-L25), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L28-L28), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L31-L31), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L33-L33), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L35-L35), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L37-L37), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L39-L39)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

7:     uint256 public constant MAX_TCR = type(uint256).max;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L7-L7) 


</details>


### [GAS&#x2011;32] `private` functions only called once can be inlined to save gas 
Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

397:     function _liquidateCDPPartially(
398:         LiquidationLocals memory _partialState
399:     ) private returns (uint256, uint256) {

544:     function _calculatePartialLiquidationSurplusAndCap(
545:         uint256 _ICR,
546:         uint256 _price,
547:         uint256 _totalDebtToBurn,
548:         uint256 _totalColToSend
549:     ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L397-L399) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L544-L549)


</details>


### [GAS&#x2011;33] Remove or replace unused state variables 
Saves a storage slot. If the variable is assigned a non-zero value, saves Gsset (**20000 gas**). If it's assigned a zero value, saves Gsreset (**2900 gas**). If the variable remains unassigned, there is no gas savings unless the variable is `public`, in which case the compiler-generated non-payable getter deployment cost is saved. If the state variable is overriding an interface's public function, mark the variable as `constant` or `immutable` so that it does not use a storage slot


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Governor.sol

17:     bytes32 NO_ROLES = bytes32(0);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L17-L17) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L30-L30) 


</details>


### [GAS&#x2011;34] Redundant else statement 



*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

666:         if (_chainID() == _CACHED_CHAIN_ID) {
667:             return _CACHED_DOMAIN_SEPARATOR;
668:         } else {
669:             return _buildDomainSeparator(_TYPE_HASH, _HASHED_NAME, _HASHED_VERSION);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L666-L669) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

190:         if (_liqState.recoveryModeAtStart) {
191:             LiquidationRecoveryModeLocals
192:                 memory _outputState = _liquidateIndividualCdpSetupCDPInRecoveryMode(_recoveryState);
193: 
194:             // housekeeping leftover collateral for liquidated CDP
195:             if (_outputState.totalSurplusCollShares > 0) {
196:                 activePool.transferSystemCollShares(
197:                     address(collSurplusPool),
198:                     _outputState.totalSurplusCollShares
199:                 );
200:             }
201: 
202:             return (
203:                 _outputState.totalDebtToBurn,
204:                 _outputState.totalCollSharesToSend,
205:                 _outputState.totalDebtToRedistribute,
206:                 _outputState.totalLiquidatorRewardCollShares,
207:                 _outputState.totalSurplusCollShares
208:             );
209:         } else {
210:             LiquidationLocals memory _outputState = _liquidateIndividualCdpSetupCDPInNormalMode(
211:                 _liqState
212:             );
213:             return (


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L190-L213) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

636:         if (_scaledCdpColl > _feeSplitDistributed) {
637:             return (
638:                 _feeSplitDistributed,
639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
640:             );
641:         } else {
642:             // extreme unlikely case to skip fee split on this CDP to avoid revert
643:             return (0, _cdpCol);

765:         if (_newIndex > _oldIndex && totalStakes > 0) {
766:             /// @audit-ok We don't take the fee if we had a negative rebase
767:             (
768:                 uint256 _feeTaken,
769:                 uint256 _deltaFeePerUnit,
770:                 uint256 _perUnitError
771:             ) = calcFeeUponStakingReward(_newIndex, _oldIndex);
772: 
773:             // calculate new split per stake unit
774:             uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
775:             return (_feeTaken, _newPerUnit, _perUnitError);
776:         } else {
777:             return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L636-L643) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L765-L777)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

183:         if (_chainID() == _CACHED_CHAIN_ID) {
184:             return _CACHED_DOMAIN_SEPARATOR;
185:         } else {
186:             return _buildDomainSeparator(_TYPE_HASH, _HASHED_NAME, _HASHED_VERSION);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L183-L186) 


```solidity

File: packages/contracts/contracts/SortedCdps.sol

189:                 if (_currentIndex == index) {
190:                     return (_currentCdpId, true);
191:                 } else {
192:                     // if not, increment the owner index as we've seen a CDP owned by them
193:                     _currentIndex = _currentIndex + 1;
194:                 }
195:             }
196:             ++i;
197: 
198:             // move to the next CDP in the list
199:             _currentCdpId = data.nodes[_currentCdpId].prevId;
200: 
201:             // cut the run if we exceed expected iterations through the loop
202:             if (maxNodes > 0 && i >= maxNodes) {
203:                 break;
204:             }
205:         }
206:         // if we reach maximum iteration or end of list
207:         // without seeing the specified index for the owner
208:         // then maybe a new pagination is needed
209:         return (_currentCdpId, false);

602:         } else if (_nextId == dummyId) {
603:             // `(_prevId, null)` is a valid insert position if `_prevId` is the tail of the list
604:             return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);
605:         } else {
606:             // `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs
607:             return

702:         } else if (nextId == dummyId) {
703:             // No `nextId` for hint - descend list starting from `prevId`
704:             return _descendList(_NICR, prevId);
705:         } else {
706:             // Descend list starting from `prevId`
707:             return _descendList(_NICR, prevId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L189-L209) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L602-L607), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L702-L707)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

93:         if (_debt > 0) {
94:             return (_collShares * NICR_PRECISION) / _debt;
95:         }
96:         // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
97:         else {
98:             // if (_debt == 0)
99:             return MAX_TCR;

109:         if (_debt > 0) {
110:             uint256 newCollRatio = (_stEthBalance * _price) / _debt;
111: 
112:             return newCollRatio;
113:         }
114:         // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
115:         else {
116:             // if (_debt == 0)
117:             return MAX_TCR;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L93-L99) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L109-L117)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

72:         } else if (flag == CapabilityFlag.Public) {
73:             return true;
74:         } else {
75:             return bytes32(0) != getUserRoles[user] & getRolesWithCapability[target][functionSig];


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L72-L75) 


</details>


### [GAS&#x2011;35] Avoid updating storage when the value hasn't changed to save gas 
If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (**2900 gas**), potentially at the expense of a Gcoldsload (**2100 gas**) or a Gwarmaccess (**100 gas**)


*There are 21 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

404:     function setFeeBps(uint256 _newFee) external requiresAuth {

417:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L390-L390) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L404-L404), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L417-L417)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

628:     function setPositionManagerApproval(

1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L628-L628) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1140-L1140), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1154-L1154), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1167-L1167)


```solidity

File: packages/contracts/contracts/CdpManager.sol

523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {

773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {

788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {

807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {

830:     function setBeta(uint256 _beta) external requiresAuth {

843:     function setRedemptionsPaused(bool _paused) external requiresAuth {

946:     function updateCdp(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L523-L523) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L773-L773), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L788-L788), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L807-L807), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L830-L830), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L843-L843), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L946-L946)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

130:     function increaseTotalSurplusCollShares(uint256 _value) external override {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L130-L130) 


```solidity

File: packages/contracts/contracts/Governor.sol

154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L154) 


```solidity

File: packages/contracts/contracts/PriceFeed.sol

358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L358-L358) 


```solidity

File: packages/contracts/contracts/LeverageMacroReference.sol

50:     function resetApprovals() external {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroReference.sol#L50-L50) 


```solidity

File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

38:     function setAuthority(address newAuthority) public virtual {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L38-L38) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

85:     function setPublicCapability(


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L85-L85) 


</details>


### [GAS&#x2011;36] Use shift Right instead of division if possible to save gas 



*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

38:         decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;

81:                 n = (n - 1) / 2;

76:                 n = n / 2;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L38-L38) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L81-L81), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L76-L76)


</details>


### [GAS&#x2011;37] Use shift Left instead of multiplication if possible to save gas 



*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/PriceFeed.sol

804:                 EbtcMath.DECIMAL_PRECISION) / 10 ** (_decimalDenominator * 2);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L804-L804) 


</details>


### [GAS&#x2011;38] Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead 
> When using elements that are smaller than 32 bytes, your contract's gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.
https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html
Each operation involving a `uint8` costs an extra [** 22 - 28 gas **](https://gist.github.com/IllIllI000/9388d20c70f9a4632eb3ca7836f54977) (depending on whether the other operand is also a variable of type `uint8`) as compared to ones involving `uint256`, due to the compiler having to clear the higher bits of the memory word before operating on the `uint8`, as well as the associated stack operations of doing so. Use a larger size then downcast where needed


*There are 43 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

//@audit `v` is `uint8`
711:         uint8 v,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L711-L711) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

//@audit `index` is `uint128`
550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L550-L550) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

//@audit `cachedLastGracePeriodStartTimestamp` is `uint128`
88:             uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L88-L88) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit `` is `uint128`
111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

//@audit `index` is `uint128`
471:         uint128 index = Cdps[_cdpId].arrayIndex;

//@audit `cachedLastGracePeriodStartTimestamp` is `uint128`
897:         uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L111-L111) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L471-L471), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L897-L897)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

//@audit `v` is `uint8`
204:         uint8 v,

//@audit `` is `uint8`
343:     function decimals() external pure override returns (uint8) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L204-L204) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L343-L343)


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit `role` is `uint8`
43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

//@audit `i` is `uint8`
76:         for (uint8 i = 0; i < type(uint8).max; i++) {

//@audit `i` is `uint8`
84:             for (uint8 i = 0; i < type(uint8).max; i++) {

//@audit `i` is `uint8`
98:         for (uint8 i = 0; i < type(uint8).max; i++) {

//@audit `i` is `uint8`
107:             for (uint8 i = 0; i < type(uint8).max; i++) {

//@audit `i` is `uint8`
122:         for (uint8 i = 0; i < roleIds.length; i++) {

//@audit `role` is `uint8`
146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

//@audit `role` is `uint8`
154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L43-L43) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L76-L76), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L84-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L98-L98), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L107-L107), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L146-L146), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L154-L154)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

//@audit `ethBtcDecimals` is `uint8`
612:         uint8 ethBtcDecimals;

//@audit `stEthEthDecimals` is `uint8`
613:         uint8 stEthEthDecimals;

//@audit `decimals` is `uint8`
615:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

//@audit `decimals` is `uint8`
623:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

//@audit `roundId` is `uint80`
635:             uint80 roundId,

//@audit `` is `uint80`
640:             uint80 /* answeredInRound */

//@audit `roundId` is `uint80`
651:             uint80 roundId,

//@audit `` is `uint80`
656:             uint80 /* answeredInRound */

//@audit `_currentRoundEthBtcId` is `uint80`
688:         uint80 _currentRoundEthBtcId,

//@audit `_currentRoundStEthEthId` is `uint80`
689:         uint80 _currentRoundStEthEthId

//@audit `ethBtcDecimals` is `uint8`
700:         uint8 ethBtcDecimals;

//@audit `stEthEthDecimals` is `uint8`
701:         uint8 stEthEthDecimals;

//@audit `decimals` is `uint8`
703:         try ETH_BTC_CL_FEED.decimals() returns (uint8 decimals) {

//@audit `decimals` is `uint8`
711:         try STETH_ETH_CL_FEED.decimals() returns (uint8 decimals) {

//@audit `roundId` is `uint80`
723:             uint80 roundId,

//@audit `` is `uint80`
728:             uint80 /* answeredInRound */

//@audit `roundId` is `uint80`
739:             uint80 roundId,

//@audit `` is `uint80`
744:             uint80 /* answeredInRound */

//@audit `_roundId` is `uint80`
775:     function _checkHealthyCLResponse(uint80 _roundId, int256 _answer) internal view returns (bool) {

//@audit `_ethBtcDecimals` is `uint8`
791:         uint8 _ethBtcDecimals,

//@audit `_stEthEthDecimals` is `uint8`
792:         uint8 _stEthEthDecimals


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L612-L612) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L613-L613), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L615-L615), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L623-L623), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L635-L635), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L640-L640), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L651-L651), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L656-L656), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L688-L688), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L689-L689), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L700-L700), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L701-L701), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L703-L703), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L711-L711), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L723-L723), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L728-L728), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L739-L739), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L744-L744), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L775-L775), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L791-L791), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L792-L792)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

//@audit `_maxCopy` is `uint16`
502:         uint16 _maxCopy,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L502-L502) 


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

//@audit `role` is `uint8`
38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

//@audit `role` is `uint8`
43:         uint8 role,

//@audit `role` is `uint8`
107:         uint8 role,

//@audit `role` is `uint8`
147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L38-L38) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L43-L43), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L107-L107), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L147-L147)


```solidity

File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

//@audit `v` is `uint8`
37:         uint8 v,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPositionManagers.sol#L37-L37) 


</details>


### [GAS&#x2011;39] The use of a logical AND in place of double if is slightly less gas efficient in instances where there isn't a corresponding else statement for the given if statement 
Using a double if statement instead of logical AND (&&) can provide similar short-circuiting behavior whereas double if is slightly more efficient.


*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {
394:             _requireValidDebtRepayment(vars.debt, vars.netDebtChange);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L393-L394) 


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

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

756:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
757:                 vars.ICR = getSyncedICR(vars.cdpId, _price);

819:             if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
820:                 vars.ICR = getSyncedICR(vars.cdpId, _price);

790:                 } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {
791:                     _syncAccounting(vars.cdpId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L158-L168) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L756-L757), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L819-L820), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L790-L791)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

512:         if (_newIndex > _oldIndex && totalStakes > 0) {
513:             (
514:                 uint256 _feeTaken,
515:                 uint256 _newFeePerUnit,
516:                 uint256 _perUnitError
517:             ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
797:             (
798:                 uint256 _feeSplitDistributed,
799:                 uint256 _newCollShareAfter
800:             ) = getAccumulatedFeeSplitApplied(_cdpId, _systemStEthFeePerUnitIndex);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L512-L517) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L796-L800)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

227:                     !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228:                     !_chainlinkIsFrozen(chainlinkResponse)
229:                 ) {
230:                     _changeStatus(Status.usingChainlinkFallbackUntrusted);

373:                     !_fallbackIsBroken(fallbackResponse) &&
374:                     !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
375:                 ) {
376:                     address oldFallbackCaller = address(fallbackCaller);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L227-L230) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L373-L376)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

621:         if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {
622:             return (dummyId, _startId);

644:         if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
645:             return (_startId, dummyId);

202:             if (maxNodes > 0 && i >= maxNodes) {
203:                 break;

259:             if (maxNodes > 0 && i >= maxNodes) {
260:                 break;

330:             if (maxNodes > 0 && i >= maxNodes) {
331:                 break;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L621-L622) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L644-L645), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L202-L203), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L259-L260), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L330-L331)


</details>


### [GAS&#x2011;40] Splitting `require()` statements that use `&&` saves gas 
See [this issue](https://github.com/code-423n4/2022-01-xdefi-findings/issues/128) which describes the fact that there is a larger deployment gas cost, but with enough runtime calls, the change ends up being cheaper by **3 gas**


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

734:         require(
735:             recoveredAddress != address(0) && recoveredAddress == _borrower,
736:             "BorrowerOperations: Invalid signature"
737:         );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L734-L737) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

762:         require(
763:             _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764:             "Max fee percentage must be between redemption fee floor and 100%"
765:         );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L762-L765) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L261-L264) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L466-L469), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L653-L656)


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L296-L299) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L300-L303)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

79:         require(
80:             !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81:                 !_chainlinkIsFrozen(chainlinkResponse),
82:             "PriceFeed: Chainlink must be working and current"
83:         );


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L79-L83) 


</details>


### [GAS&#x2011;41] Stack variable used as a cheaper cache for a state variable is only used once 
If the variable is only accessed once, it's cheaper to use the state variable directly that one time, and save the **3 gas** the extra stack assignment would spend. However, if it used as a parameter in an event emit, then caching it will help reduce gas by at least ***10 gas***


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

84:         bytes32 position = DIAMOND_STORAGE_POSITION;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L84-L84) 


</details>


### [GAS&#x2011;42] Cache state variables outside of loop to avoid reading storage on every iteration 
Reading from storage should always try to be avoided within loops.In the following instances, we are able to cache state variables outside of the loop to save a Gwarmaccess(100 gas) per loop iteration.

Note: Due to stack too deep errors, we will not be able to cache all the state variables read within the loops.


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/SortedCdps.sol

//@audit `data` is a state variable, try to cache it outside the loop
199:             _currentCdpId = data.nodes[_currentCdpId].prevId;

//@audit `data` is a state variable, try to cache it outside the loop
256:             _currentCdpId = data.nodes[_currentCdpId].prevId;

//@audit `data` is a state variable, try to cache it outside the loop
327:             _currentCdpId = data.nodes[_currentCdpId].prevId;

//@audit `data` is a state variable, try to cache it outside the loop
450:             delete data.nodes[_ids[i]];

//@audit `data` is a state variable, try to cache it outside the loop
630:             prevId = data.nodes[prevId].nextId;

//@audit `data` is a state variable, try to cache it outside the loop
631:             nextId = data.nodes[prevId].nextId;

//@audit `data` is a state variable, try to cache it outside the loop
653:             nextId = data.nodes[nextId].prevId;

//@audit `data` is a state variable, try to cache it outside the loop
654:             prevId = data.nodes[nextId].prevId;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L199-L199) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L256-L256), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L327-L327), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L450-L450), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L630-L630), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L631-L631), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L653-L653), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L654-L654)


</details>


### [GAS&#x2011;43] `>=`/`<=` costs less gas than `>`/`<` 
The compiler uses opcodes `GT` and `ISZERO` for solidity code that uses `>`, but only requires `LT` for `>=`, [which saves **3 gas**](https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde)


*There are 113 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

267:         require(amount > 0, "ActivePool: 0 Amount");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L267-L267) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

393:         if (!_isDebtIncrease && _debtChange > 0) {

463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

495:             if (newTCR < CCR) {

891:             if (_vars.newTCR < CCR) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L393-L393) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L463-L463), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L835-L835), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L936-L936), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1083-L1083), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L495-L495), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L891-L891)


```solidity

File: packages/contracts/contracts/CdpManager.sol

601:         return TCR < CCR;

279:             getSyncedICR(_firstRedemptionHint, _price) < MCR

285:         return nextCdp == sortedCdps.nonExistId() || getSyncedICR(nextCdp, _price) < MCR;

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

436:         } else if (_numCdpsFullyRedeemed > 1) {

497:         while (_cnt > 0 && _id != bytes32(0)) {

626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672:         require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

690:         uint256 timePassed = block.timestamp > lastRedemptionTimestamp

711:             block.timestamp > lastRedemptionTimestamp

754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

203:                 collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE

369:             while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L601-L601) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L279-L279), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L285-L285), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L389-L389), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L431-L431), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L436-L436), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L497-L497), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L626-L626), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L672-L672), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L690-L690), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L711-L711), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L754-L754), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L389-L389), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L203-L203), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L369-L369)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

476:         if (_partialState.ICR > LICR) {

525:         if (totalDebtToRedistribute > 0) {

553:         if (_ICR > LICR) {

578:         if (_ICR > LICR) {

713:         if (totals.totalCollSurplus > 0) {

100:         bool _recoveryModeAtStart = _TCR < CCR ? true : false;

261:             if (_collSurplus > 0) {

266:             if (_debtToRedistribute > 0) {

336:             if (_collSurplus > 0) {

342:             if (_debtToRedistribute > 0) {

564:         assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

195:             if (_outputState.totalSurplusCollShares > 0) {

289:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

358:         _recoveryState.entireSystemDebt = _recoveryState.entireSystemDebt > _totalDebtToBurn

361:         _recoveryState.entireSystemColl = _recoveryState.entireSystemColl > _totalColToSend

375:             _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

602:         toLiquidator = toLiquidator < _totalColToSend ? toLiquidator : _totalColToSend;

695:         vars.recoveryModeAtStart = _TCR < CCR ? true : false;

94:                 block.timestamp >

444:                 _cappedColl > _debtToColl ? (_cappedColl - _debtToColl) : 0

594:             debtToRedistribute = _debtToRepay < _totalDebtToBurn

555:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L476-L476) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L525-L525), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L553-L553), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L578-L578), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L713-L713), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L100-L100), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L261-L261), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L266-L266), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L336-L336), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L342-L342), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L564-L564), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L710-L710), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L195-L195), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L289-L289), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L358-L358), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L361-L361), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L375-L375), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L602-L602), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L695-L695), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L94-L94), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L444-L444), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L594-L594), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L555-L555), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L579-L579), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L788-L788)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

99:         if (newTCR < CCR) {

315:         if (_debtIndexDiff > 0) {

636:         if (_scaledCdpColl > _feeSplitDistributed) {

829:         if (pendingDebtRedistributed > 0) {

879:         if (_feeTaken > 0) {

332:         return (cdpDebtRedistributionIndex[_cdpId] < systemDebtRedistributionIndex);

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

512:         if (_newIndex > _oldIndex && totalStakes > 0) {

556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

765:         if (_newIndex > _oldIndex && totalStakes > 0) {

796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {

900:             block.timestamp > cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration;

369:             if (_feeSplitDistributed > 0) {

380:             if (_debtIndexDelta > 0) {

654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L99-L99) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L315-L315), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L636-L636), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L829-L829), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L879-L879), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L332-L332), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L362-L362), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L362-L362), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L512-L512), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L512-L512), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L556-L556), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L584-L584), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L765-L765), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L765-L765), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L796-L796), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L900-L900), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L369-L369), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L380-L380), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L654-L654), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L654-L654), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L453-L453)


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

92:         require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L92-L92) 


```solidity

File: packages/contracts/contracts/Governor.sol

53:         if (count > 0) {

81:         if (count > 0) {

104:         if (count > 0) {

135:         if (_sigs.length > 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L53-L53) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L81-L81), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L104-L104), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L135-L135)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

462:         return percentDeviation > MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND;

494:         return block.timestamp - _timestamp > _timeout;

423:             _response.timestampStEthEth > block.timestamp

457:         uint256 percentDeviation = maxPrice > 0

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

489:             _fallbackResponse.timestamp > 0 &&

794:         uint256 _decimalDenominator = _stEthEthDecimals > _ethBtcDecimals

797:         uint256 _scaledDecimal = _stEthEthDecimals > _ethBtcDecimals

421:             _response.timestampEthBtc > block.timestamp ||


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L462-L462) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L494-L494), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L423-L423), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L457-L457), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L471-L471), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L489-L489), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L794-L794), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L797-L797), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L421-L421)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

274:         if (_ownedCount > 0) {

460:         if (data.size > 1) {

371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

202:             if (maxNodes > 0 && i >= maxNodes) {

259:             if (maxNodes > 0 && i >= maxNodes) {

330:             if (maxNodes > 0 && i >= maxNodes) {

683:             if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {

690:             if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L274-L274) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L460-L460), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L371-L371), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L422-L422), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L508-L508), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L202-L202), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L259-L259), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L330-L330), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L683-L683), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L690-L690)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

181:         while (i < _numTrials) {

70:                 cdpManager.getSyncedICR(vars.currentCdpId, _price) < MCR

87:                 _maxIterations-- > 0

191:             if (currentDiff < diff) {

93:                 if (currentCdpDebt > vars.remainingEbtcToRedeem) {

86:                 vars.remainingEbtcToRedeem > 0 &&

102:                         collateral.getPooledEthByShares(partialRedemptionNewColl) <


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L181-L181) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L70-L70), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L87-L87), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L191-L191), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L93-L93), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L86-L86), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L102-L102)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

128:         if (operation.amountToTransferIn > 0) {

223:         if (ebtcBal > 0) {

227:         if (collateralBal > 0) {

293:         if (beforeSwapsLength > 0) {

307:         if (afterSwapsLength > 0) {

441:                     IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L128-L128) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L223-L223), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L227-L227), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L293-L293), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L307-L307), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L441-L441)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcBase.sol

100:         return _tcr < CCR;

135:         return _icr < MCR;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L100-L100) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcBase.sol#L135-L135)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

60:         if (_minutes > 525600000) {

73:         while (n > 1) {

93:         if (_debt > 0) {

109:         if (_debt > 0) {

21:         return (_a < _b) ? _a : _b;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L60-L60) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L73-L73), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L93-L93), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L109-L109), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L21-L21)


</details>


### [GAS&#x2011;44] Ternary unnecessary 
`z = (x == y) ? true : false` => `z = (x == y)`


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

100:         bool _recoveryModeAtStart = _TCR < CCR ? true : false;

695:         vars.recoveryModeAtStart = _TCR < CCR ? true : false;

788:                     vars.backToNormalMode = _TCR < CCR ? false : true;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L100-L100) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L695-L695), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L788-L788)


</details>


### [GAS&#x2011;45] Use assembly to validate `msg.sender` 
We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. For more details check the following report [Here](https://code4rena.com/reports/2023-05-juicebox#g-06-use-assembly-to-validate-msgsender)


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

221:             msg.sender == borrowerOperationsAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

278:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L221-L221) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L229-L229), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L229-L229), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L229-L229), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L229-L229), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L236-L236), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L278-L278)


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

964:         if (_borrower == msg.sender) {

1092:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L964-L964) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1092-L1092)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

661:             msg.sender == borrowerOperationsAddress,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L661-L661) 


```solidity

File: packages/contracts/contracts/CollSurplusPool.sol

114:             msg.sender == borrowerOperationsAddress,

120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L114-L114) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L120-L120), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CollSurplusPool.sol#L124-L124)


```solidity

File: packages/contracts/contracts/EBTCToken.sol

308:             msg.sender == borrowerOperationsAddress,

316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||
318:                 isAuthorized(msg.sender, msg.sig),

316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||
318:                 isAuthorized(msg.sender, msg.sig),

316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||
318:                 isAuthorized(msg.sender, msg.sig),

316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||

316:             msg.sender == borrowerOperationsAddress ||
317:                 msg.sender == cdpManagerAddress ||

316:             msg.sender == borrowerOperationsAddress ||

317:                 msg.sender == cdpManagerAddress ||

324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L308-L308) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L318), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L318), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L318), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L317), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L317), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L316-L316), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L317-L317), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L324-L324)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),

721:             msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L715-L715) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L721-L721), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L721-L721), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L721-L721), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L721-L721)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

363:                 msg.sender == address(activePool),

357:                 msg.sender == address(borrowerOperations),

45:         require(owner() == msg.sender, "Must be owner");

363:                 msg.sender == address(activePool),

357:                 msg.sender == address(borrowerOperations),


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L363-L363) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L357-L357), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L363-L363), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L357-L357)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

52:         require(msg.sender == owner);

67:         require(msg.sender == owner);

77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111:         require(msg.sender == owner, "Must be owner");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L52-L52) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L67-L67), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L77-L77), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L111-L111)


```solidity

File: packages/contracts/contracts/Dependencies/Auth.sol

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L45-L45) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L45-L45), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/Auth.sol#L45-L45)


</details>


### [GAS&#x2011;46] Can make the variable outside the loop to save gas 
Creating variables inside the loop consum more gas compared to declaring them outside and just reaffecting values to them inside the loop.


*There are 16 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManager.sol

//@audit variable `_redeemColFromCdp` is created inside a loop.
395:                 SingleRedemptionInputs memory _redeemColFromCdp = SingleRedemptionInputs(

//@audit variable `singleRedemption` is created inside a loop.
403:                 SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(

//@audit variable `_nextId` is created inside a loop.
424:                 bytes32 _nextId = sortedCdps.getPrev(_cId);

//@audit variable `nextUserToCheck` is created inside a loop.
425:                 address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L395-L395) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L403-L403), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L424-L424), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L425-L425)


```solidity

File: packages/contracts/contracts/Governor.sol

//@audit variable `user` is created inside a loop.
47:             address user = users.at(i);

//@audit variable `_canCall` is created inside a loop.
48:             bool _canCall = doesUserHaveRole(user, role);

//@audit variable `roleEnabled` is created inside a loop.
99:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

//@audit variable `user` is created inside a loop.
58:                 address user = _usrs[i];

//@audit variable `_canCall` is created inside a loop.
59:                 bool _canCall = doesUserHaveRole(user, role);

//@audit variable `roleEnabled` is created inside a loop.
108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L47-L47) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L48-L48), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L99-L99), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L58-L58), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L59-L59), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L108-L108)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

//@audit variable `arrayIndex` is created inside a loop.
184:             uint256 arrayIndex = latestRandomSeed % arrayLength;

//@audit variable `_cId` is created inside a loop.
185:             bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);

//@audit variable `currentNICR` is created inside a loop.
186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

//@audit variable `currentDiff` is created inside a loop.
189:             uint256 currentDiff = EbtcMath._getAbsoluteDifference(currentNICR, _CR);

//@audit variable `currentCdpDebt` is created inside a loop.
90:                 uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

//@audit variable `_cachedEbtcToRedeem` is created inside a loop.
94:                     uint256 _cachedEbtcToRedeem = vars.remainingEbtcToRedeem;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L184-L184) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L185-L185), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L186-L186), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L189-L189), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L90-L90), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L94-L94)


</details>


### [GAS&#x2011;47] `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) 
*Saves 5 gas per loop*


*There are 15 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

727:                         _nonces[_borrower]++,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L727-L727) 


```solidity

File: packages/contracts/contracts/CdpManager.sol

429:             _maxIterations--;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L429-L429) 


```solidity

File: packages/contracts/contracts/EBTCToken.sol

214:                     abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L214-L214) 


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L46-L46) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L62-L62), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L76-L76), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L84-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L87-L87), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L98-L98), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L107-L107), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L111-L111), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L122-L122)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

87:                 _maxIterations-- > 0

195:             i++;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L87-L87) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L195-L195)


</details>


### [GAS&#x2011;48] Structs can be packed into fewer storage slots by truncating timestamp bytes 
By using a `uint32` rather than a larger type for variables that track timestamps, one can save gas by using fewer storage slots per struct, at the expense of the protocol breaking after the year 2106 (when `uint32` wraps). If this is an acceptable tradeoff, each slot saved can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

//@audit the following variables: timestampEthBtc, timestampStEthEth,  could be packed
17:     struct ChainlinkResponse {
18:         uint80 roundEthBtcId;
19:         uint80 roundStEthEthId;
20:         uint256 answer;
21:         uint256 timestampEthBtc;
22:         uint256 timestampStEthEth;
23:         bool success;
24:     }

//@audit the following variables: timestamp,  could be packed
26:     struct FallbackResponse {
27:         uint256 answer;
28:         uint256 timestamp;
29:         bool success;
30:     }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26-L30)


</details>


### [GAS&#x2011;49] Stat variables can be packed into fewer storage slots by truncating timestamp bytes 
By using a `uint32` rather than a larger type for variables that track timestamps, one can save gas by using fewer storage slots per struct, at the expense of the protocol breaking after the year 2106 (when `uint32` wraps). If this is an acceptable tradeoff, each slot saved can avoid an extra Gsset (**20000 gas**) for the first setting of the stat variable. Subsequent reads as well as writes have smaller gas savings


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

//@audit the following variables could be packed: 
    uint256 public lastRedemptionTimestamp;
 
19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L19-L19) 


</details>


### [GAS&#x2011;50] Using mappings instead of arrays to avoid length checks save gas 
Just by using a mapping, we get a gas saving of 2102 gas. When you read the value of an index of an array, solidity adds bytecode that checks that you are reading from a valid index (i.e an index strictly less than the length of the array) else it reverts with a panic error (Panic(0x32) to be precise). This prevents from reading unallocated or worse, allocated storage/memory locations.
Due to the way mappings are(simply a key => value pair), no check like that exists and we are able to read from the a storage slot directly.It’s important to note that when using mappings in this manner, your code should ensure that you are not reading an out of bound index of your canonical array.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

205:     bytes32[] public CdpIds;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L205-L205) 


</details>


### [GAS&#x2011;51] State variables can be packed into fewer storage slots 
If variables occupying the same slot are both written the same function or by the constructor, avoids a separate Gsset (**20000 gas**). Reads of the variables can also be cheaper


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

// @audit from 8 to 7 you need to change the structure elements order to: , uint256, uint256, uint256, address, address, address, address, ICollateralToken
022: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {
023:     using SafeERC20 for IERC20;
024:     string public constant NAME = "ActivePool";
025: 
026:     address public immutable borrowerOperationsAddress;
027:     address public immutable cdpManagerAddress;
028:     address public immutable collSurplusPoolAddress;
029:     address public feeRecipientAddress;
030: 
031:     uint256 internal systemCollShares; // deposited collateral tracker
032:     uint256 internal systemDebt;
033:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient
034:     ICollateralToken public immutable collateral;
035: 
036:     // --- Contract setters ---
037: 
038:     /// @notice Constructor for the ActivePool contract
039:     /// @dev Initializes the contract with the borrowerOperationsAddress, cdpManagerAddress, collateral token address, collSurplusAddress, and feeRecipientAddress
040:     /// @param _borrowerOperationsAddress The address of the Borrower Operations contract
041:     /// @param _cdpManagerAddress The address of the Cdp Manager contract
042:     /// @param _collTokenAddress The address of the collateral token
043:     /// @param _collSurplusAddress The address of the collateral surplus pool
044:     /// @param _feeRecipientAddress The address of the fee recipient
045: 
046:     constructor(
047:         address _borrowerOperationsAddress,
048:         address _cdpManagerAddress,
049:         address _collTokenAddress,
050:         address _collSurplusAddress,
051:         address _feeRecipientAddress
052:     ) {
053:         borrowerOperationsAddress = _borrowerOperationsAddress;
054:         cdpManagerAddress = _cdpManagerAddress;
055:         collateral = ICollateralToken(_collTokenAddress);
056:         collSurplusPoolAddress = _collSurplusAddress;
057:         feeRecipientAddress = _feeRecipientAddress;
058: 
059:         // TEMP: read authority to avoid signature change
060:         address _authorityAddress = address(AuthNoOwner(cdpManagerAddress).authority());
061:         if (_authorityAddress != address(0)) {
062:             _initializeAuthority(_authorityAddress);
063:         }
064: 
065:         emit FeeRecipientAddressChanged(_feeRecipientAddress);
066:     }
067: 
068:     // --- Getters for public variables. Required by IPool interface ---
069: 
070:     /// @notice Amount of stETH collateral shares in the contract
071:     /// @dev Not necessarily equal to the the contract's raw systemCollShares balance - tokens can be forcibly sent to contracts
072:     /// @return uint256 The amount of systemCollShares allocated to the pool
073: 
074:     function getSystemCollShares() external view override returns (uint256) {
075:         return systemCollShares;
076:     }
077: 
078:     /// @notice Returns the systemDebt state variable
079:     /// @dev The amount of EBTC debt in the pool. Like systemCollShares, this is not necessarily equal to the contract's EBTC token balance - tokens can be forcibly sent to contracts
080:     /// @return uint256 The amount of EBTC debt in the pool
081: 
082:     function getSystemDebt() external view override returns (uint256) {
083:         return systemDebt;
084:     }
085: 
086:     /// @notice The amount of stETH collateral shares claimable by the fee recipient
087:     /// @return uint256 The amount of collateral shares claimable by the fee recipient
088: 
089:     function getFeeRecipientClaimableCollShares() external view override returns (uint256) {
090:         return feeRecipientCollShares;
091:     }
092: 
093:     // --- Pool functionality ---
094: 
095:     /// @notice Sends stETH collateral shares to a specified account
096:     /// @dev Only for use by system contracts, the caller must be either BorrowerOperations or CdpManager
097:     /// @param _account The address of the account to send stETH to
098:     /// @param _shares The amount of stETH shares to send
099: 
100:     function transferSystemCollShares(address _account, uint256 _shares) public override {
101:         _requireCallerIsBOorCdpM();
102: 
103:         uint256 cachedSystemCollShares = systemCollShares;
104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");
105:         unchecked {
106:             // Can use unchecked due to above
107:             cachedSystemCollShares -= _shares; // Updating here avoids an SLOAD
108:         }
109: 
110:         systemCollShares = cachedSystemCollShares;
111: 
112:         emit SystemCollSharesUpdated(cachedSystemCollShares);
113:         emit CollSharesTransferred(_account, _shares);
114: 
115:         _transferCollSharesWithContractHooks(_account, _shares);
116:     }
117: 
118:     /// @notice Sends stETH to a specified account, drawing from both core shares and liquidator rewards shares
119:     /// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager
120:     /// @dev Liquidator reward shares are added when a cdp is opened, and removed when it is closed
121:     /// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares
122:     /// @dev Redemptions result in the shares being sent to the coll surplus pool for claiming by the CDP owner
123:     /// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.
124:     /// @dev Requires that the caller is either BorrowerOperations or CdpManager
125:     /// @param _account The address of the account to send systemCollShares and the liquidator reward to
126:     /// @param _shares The amount of systemCollShares to send
127:     /// @param _liquidatorRewardShares The amount of the liquidator reward shares to send
128: 
129:     function transferSystemCollSharesAndLiquidatorReward(
130:         address _account,
131:         uint256 _shares,
132:         uint256 _liquidatorRewardShares
133:     ) external override {
134:         _requireCallerIsBOorCdpM();
135: 
136:         uint256 cachedSystemCollShares = systemCollShares;
137:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");
138:         uint256 totalShares = _shares + _liquidatorRewardShares;
139:         unchecked {
140:             // Safe per the check above
141:             cachedSystemCollShares -= _shares;
142:         }
143:         systemCollShares = cachedSystemCollShares;
144: 
145:         emit SystemCollSharesUpdated(cachedSystemCollShares);
146:         emit CollSharesTransferred(_account, totalShares);
147: 
148:         _transferCollSharesWithContractHooks(_account, totalShares);
149:     }
150: 
151:     /// @notice Allocate stETH shares from the system to the fee recipient to claim at-will (pull model)
152:     /// @dev Requires that the caller is CdpManager
153:     /// @dev Only the current fee recipient address is able to claim the shares
154:     /// @dev If the fee recipient address is changed while outstanding claimable coll is available, only the new fee recipient will be able to claim the outstanding coll
155:     /// @param _shares The amount of systemCollShares to allocate to the fee recipient
156: 
157:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external override {
158:         _requireCallerIsCdpManager();
159: 
160:         uint256 cachedSystemCollShares = systemCollShares;
161: 
162:         require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");
163:         unchecked {
164:             // Safe per the check above
165:             cachedSystemCollShares -= _shares;
166:         }
167: 
168:         systemCollShares = cachedSystemCollShares;
169: 
170:         uint256 cachedFeeRecipientCollShares = feeRecipientCollShares + _shares;
171:         feeRecipientCollShares = cachedFeeRecipientCollShares;
172: 
173:         emit SystemCollSharesUpdated(cachedSystemCollShares);
174:         emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);
175:     }
176: 
177:     /// @notice Helper function to transfer stETH shares to another address, ensuring to call hooks into other system pools if they are the recipient
178:     /// @param _account The address to transfer shares to
179:     /// @param _shares The amount of shares to transfer
180: 
181:     function _transferCollSharesWithContractHooks(address _account, uint256 _shares) internal {
182:         // NOTE: No need for safe transfer if the collateral asset is standard. Make sure this is the case!
183:         collateral.transferShares(_account, _shares);
184: 
185:         if (_account == collSurplusPoolAddress) {
186:             ICollSurplusPool(_account).increaseTotalSurplusCollShares(_shares);
187:         }
188:     }
189: 
190:     /// @notice Increases the tracked EBTC debt of the system by a specified amount
191:     /// @dev Managed by system contracts - requires that the caller is either BorrowerOperations or CdpManager
192:     /// @param _amount: The amount to increase the system EBTC debt by
193: 
194:     function increaseSystemDebt(uint256 _amount) external override {
195:         _requireCallerIsBOorCdpM();
196: 
197:         uint256 cachedSystemDebt = systemDebt + _amount;
198: 
199:         systemDebt = cachedSystemDebt;
200:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
201:     }
202: 
203:     /// @notice Decreases the tracked EBTC debt of the system by a specified amount
204:     /// @dev Managed by system contracts - requires that the caller is either BorrowerOperations or CdpManager
205:     /// @param _amount: The amount to decrease the system EBTC debt by
206: 
207:     function decreaseSystemDebt(uint256 _amount) external override {
208:         _requireCallerIsBOorCdpM();
209: 
210:         uint256 cachedSystemDebt = systemDebt - _amount;
211: 
212:         systemDebt = cachedSystemDebt;
213:         emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
214:     }
215: 
216:     // --- 'require' functions ---
217: 
218:     /// @notice Checks if the caller is BorrowerOperations
219:     function _requireCallerIsBorrowerOperations() internal view {
220:         require(
221:             msg.sender == borrowerOperationsAddress,
222:             "ActivePool: Caller is not BorrowerOperations"
223:         );
224:     }
225: 
226:     /// @notice Checks if the caller is either BorrowerOperations or CdpManager
227:     function _requireCallerIsBOorCdpM() internal view {
228:         require(
229:             msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
230:             "ActivePool: Caller is neither BorrowerOperations nor CdpManager"
231:         );
232:     }
233: 
234:     /// @notice Checks if the caller is CdpManager
235:     function _requireCallerIsCdpManager() internal view {
236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
237:     }
238: 
239:     /// @notice Notify that stETH collateral shares have been recieved, updating internal accounting accordingly
240:     /// @param _value The amount of collateral to receive
241: 
242:     function increaseSystemCollShares(uint256 _value) external override {
243:         _requireCallerIsBorrowerOperations();
244: 
245:         uint256 cachedSystemCollShares = systemCollShares + _value;
246:         systemCollShares = cachedSystemCollShares;
247:         emit SystemCollSharesUpdated(cachedSystemCollShares);
248:     }
249: 
250:     // === Flashloans === //
251: 
252:     /// @notice Borrow assets with a flash loan
253:     /// @dev The Collateral checks may cause reverts if you trigger a fee change big enough
254:     ///         consider calling `cdpManagerAddress.syncGlobalAccountingAndGracePeriod()`
255:     /// @param receiver The address to receive the flash loan
256:     /// @param token The address of the token to loan
257:     /// @param amount The amount of tokens to loan
258:     /// @param data Additional data
259:     /// @return A boolean value indicating whether the operation was successful
260: 
261:     function flashLoan(
262:         IERC3156FlashBorrower receiver,
263:         address token,
264:         uint256 amount,
265:         bytes calldata data
266:     ) external override returns (bool) {
267:         require(amount > 0, "ActivePool: 0 Amount");
268:         uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused
269:         require(amount <= maxFlashLoan(token), "ActivePool: Too much");
270: 
271:         uint256 amountWithFee = amount + fee;
272:         uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);
273: 
274:         collateral.transfer(address(receiver), amount);
275: 
276:         // Callback
277:         require(
278:             receiver.onFlashLoan(msg.sender, token, amount, fee, data) == FLASH_SUCCESS_VALUE,
279:             "ActivePool: IERC3156: Callback failed"
280:         );
281: 
282:         // Transfer of (principal + Fee) from flashloan receiver
283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);
284: 
285:         // Send earned fee to designated recipient
286:         collateral.transfer(feeRecipientAddress, fee);
287: 
288:         // Check new balance
289:         // NOTE: Invariant Check, technically breaks CEI but I think we must use it
290:         // NOTE: This means any balance > systemCollShares is stuck, this is also present in LUSD as is
291: 
292:         // NOTE: This check effectively prevents running 2 FL at the same time
293:         //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert
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
306: 
307:         emit FlashLoanSuccess(address(receiver), token, amount, fee);
308: 
309:         return true;
310:     }
311: 
312:     /// @notice Calculate the flash loan fee for a given token and amount loaned
313:     /// @param token The address of the token to calculate the fee for
314:     /// @param amount The amount of tokens to calculate the fee for
315:     /// @return The flashloan fee calcualted for given token and loan amount
316: 
317:     function flashFee(address token, uint256 amount) public view override returns (uint256) {
318:         require(token == address(collateral), "ActivePool: collateral Only");
319:         require(!flashLoansPaused, "ActivePool: Flash Loans Paused");
320: 
321:         return (amount * feeBps) / MAX_BPS;
322:     }
323: 
324:     /// @notice Get the maximum flash loan amount for a specific token
325:     /// @dev Exclusively used here for stETH collateral, equal to the current balance of the pool
326:     /// @param token The address of the token to get the maximum flash loan amount for
327:     /// @return The maximum available flashloan amount for the token
328:     function maxFlashLoan(address token) public view override returns (uint256) {
329:         if (token != address(collateral)) {
330:             return 0;
331:         }
332: 
333:         if (flashLoansPaused) {
334:             return 0;
335:         }
336: 
337:         return collateral.balanceOf(address(this));
338:     }
339: 
340:     // === Governed Functions === //
341: 
342:     /// @notice Claim outstanding shares for fee recipient, updating internal accounting and transferring the shares.
343:     /// @dev Call permissinos are managed via authority for flexibility, rather than gating call to just feeRecipient.
344:     /// @dev Is likely safe as an open permission though caution should be taken.
345:     /// @param _shares The amount of shares to claim to feeRecipient
346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {
347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first
348: 
349:         uint256 cachedFeeRecipientCollShares = feeRecipientCollShares;
350:         require(
351:             cachedFeeRecipientCollShares >= _shares,
352:             "ActivePool: Insufficient fee recipient coll"
353:         );
354: 
355:         unchecked {
356:             cachedFeeRecipientCollShares -= _shares;
357:         }
358: 
359:         feeRecipientCollShares = cachedFeeRecipientCollShares;
360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);
361: 
362:         collateral.transferShares(feeRecipientAddress, _shares);
363:     }
364: 
365:     /// @dev Function to move unintended dust that are not protected
366:     /// @notice moves given amount of given token (collateral is NOT allowed)
367:     /// @notice because recipient are fixed, this function is safe to be called by anyone
368:     /// @param token The token address to be swept
369:     /// @param amount The token amount to be swept
370: 
371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
372:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
373: 
374:         require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");
375: 
376:         uint256 balance = IERC20(token).balanceOf(address(this));
377:         require(amount <= balance, "ActivePool: Attempt to sweep more than balance");
378: 
379:         address cachedFeeRecipientAddress = feeRecipientAddress; // Saves an SLOAD
380: 
381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);
382: 
383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);
384:     }
385: 
386:     /// @notice Set new FeeRecipient
387:     /// @dev Previous fees are forfeited, if you wish to claim to previous address
388:     ///       call `claimFeeRecipientCollShares` first
389:     /// @param _feeRecipientAddress The new fee recipient address to be set
390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
391:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
392: 
393:         require(
394:             _feeRecipientAddress != address(0),
395:             "ActivePool: Cannot set fee recipient to zero address"
396:         );
397: 
398:         feeRecipientAddress = _feeRecipientAddress;
399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);
400:     }
401: 
402:     /// @notice Sets new Fee for FlashLoans
403:     /// @param _newFee The new flashloan fee to be set
404:     function setFeeBps(uint256 _newFee) external requiresAuth {
405:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
406: 
407:         require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");
408: 
409:         // set new flash fee
410:         uint256 _oldFee = feeBps;
411:         feeBps = uint16(_newFee);
412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);
413:     }
414: 
415:     /// @notice Should Flashloans be paused?
416:     /// @param _paused The flag (true or false) whether flashloan will be paused
417:     function setFlashLoansPaused(bool _paused) external requiresAuth {
418:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Accrue State First
419: 
420:         flashLoansPaused = _paused;
421:         emit FlashLoansPaused(msg.sender, _paused);
422:     }
423: }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L22-L423) 


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

// @audit from 23 to 22 you need to change the structure elements order to: , uint256, uint256, uint256, uint256, uint256, uint256, uint256, mapping, uint256, uint256, uint256, uint256, mapping, uint256, uint256, uint256, uint256, mapping, address, address, uint128, uint128, bool, ICollSurplusPool, ISortedCdps, IEBTCToken, array
019: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {
020:     // NOTE: No packing cause it's the last var, no need for u64
021:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
022:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;
023: 
024:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify
025:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;
026: 
027:     /// @notice Start the recovery mode grace period, if the system is in RM and the grace period timestamp has not already been set
028:     /// @dev Trusted function to allow BorrowerOperations actions to set RM Grace Period
029:     /// @dev Assumes BorrowerOperations has correctly calculated and passed in the new system TCR
030:     /// @dev To maintain CEI compliance we use this trusted function
031:     /// @param tcr The TCR to be checked whether Grace Period should be started
032:     function notifyStartGracePeriod(uint256 tcr) external {
033:         _requireCallerIsBorrowerOperations();
034:         _startGracePeriod(tcr);
035:     }
036: 
037:     /// @notice End the recovery mode grace period, if the system is no longer in RM
038:     /// @dev Trusted function to allow BorrowerOperations actions to set RM Grace Period
039:     /// @dev Assumes BorrowerOperations has correctly calculated and passed in the new system TCR
040:     /// @dev To maintain CEI compliance we use this trusted function
041:     /// @param tcr The TCR to be checked whether Grace Period should be ended
042:     function notifyEndGracePeriod(uint256 tcr) external {
043:         _requireCallerIsBorrowerOperations();
044:         _endGracePeriod(tcr);
045:     }
046: 
047:     /// @dev Internal notify called by Redemptions and Liquidations
048:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
049:     function _startGracePeriod(uint256 _tcr) internal {
050:         emit TCRNotified(_tcr);
051: 
052:         if (lastGracePeriodStartTimestamp == UNSET_TIMESTAMP) {
053:             lastGracePeriodStartTimestamp = uint128(block.timestamp);
054: 
055:             emit GracePeriodStart();
056:         }
057:     }
058: 
059:     /// @notice Clear RM Grace Period timestamp if it has been set
060:     /// @notice No input validation, calling function must confirm that the system is not in recovery mode to be valid
061:     /// @dev Specified TCR is emitted for notification pruposes regardless of whether the Grace Period timestamp is set
062:     /// @dev Internal notify called by Redemptions and Liquidations
063:     function _endGracePeriod(uint256 _tcr) internal {
064:         emit TCRNotified(_tcr);
065: 
066:         if (lastGracePeriodStartTimestamp != UNSET_TIMESTAMP) {
067:             lastGracePeriodStartTimestamp = UNSET_TIMESTAMP;
068: 
069:             emit GracePeriodEnd();
070:         }
071:     }
072: 
073:     function _syncGracePeriod() internal {
074:         uint256 price = priceFeed.fetchPrice();
075:         uint256 tcr = _getCachedTCR(price);
076:         bool isRecoveryMode = _checkRecoveryModeForTCR(tcr);
077: 
078:         if (isRecoveryMode) {
079:             _startGracePeriod(tcr);
080:         } else {
081:             _endGracePeriod(tcr);
082:         }
083:     }
084: 
085:     /// @dev Set RM grace period based on specified system collShares, system debt, and price
086:     /// @dev Variant for internal use in redemptions and liquidations
087:     function _syncGracePeriodForGivenValues(
088:         uint256 systemCollShares,
089:         uint256 systemDebt,
090:         uint256 price
091:     ) internal {
092:         // Compute TCR with specified values
093:         uint256 newTCR = EbtcMath._computeCR(
094:             collateral.getPooledEthByShares(systemCollShares),
095:             systemDebt,
096:             price
097:         );
098: 
099:         if (newTCR < CCR) {
100:             // Notify system is in RM
101:             _startGracePeriod(newTCR);
102:         } else {
103:             // Notify system is outside RM
104:             _endGracePeriod(newTCR);
105:         }
106:     }
107: 
108:     /// @notice Set grace period duratin
109:     /// @notice Permissioned governance function, must set grace period duration above hardcoded minimum
110:     /// @param _gracePeriod new grace period duration, in seconds
111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
112:         require(
113:             _gracePeriod >= MINIMUM_GRACE_PERIOD,
114:             "CdpManager: Grace period below minimum duration"
115:         );
116: 
117:         syncGlobalAccountingAndGracePeriod();
118:         recoveryModeGracePeriodDuration = _gracePeriod;
119:         emit GracePeriodDurationSet(_gracePeriod);
120:     }
121: 
122:     string public constant NAME = "CdpManager";
123: 
124:     // --- Connected contract declarations ---
125: 
126:     address public immutable borrowerOperationsAddress;
127: 
128:     ICollSurplusPool immutable collSurplusPool;
129: 
130:     IEBTCToken public immutable override ebtcToken;
131: 
132:     address public immutable liquidationLibrary;
133: 
134:     // A doubly linked list of Cdps, sorted by their sorted by their collateral ratios
135:     ISortedCdps public immutable sortedCdps;
136: 
137:     // --- Data structures ---
138: 
139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;
140: 
141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;
143:     bool public redemptionsPaused;
144:     /*
145:      * Half-life of 12h. 12h = 720 min
146:      * (1/2) = d^720 => d = (1/2)^(1/720)
147:      */
148:     uint256 public minuteDecayFactor = 999037758833783000;
149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero
150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme
151: 
152:     uint256 internal immutable deploymentStartTime;
153: 
154:     /*
155:      * BETA: 18 digit decimal. Parameter by which to divide the redeemed fraction,
156:      * in order to calc the new base rate from a redemption.
157:      * Corresponds to (1 / ALPHA) in the Liquity white paper.
158:      */
159:     uint256 public beta = 2;
160: 
161:     uint256 public baseRate;
162: 
163:     uint256 public stakingRewardSplit;
164: 
165:     // The timestamp of the latest fee operation (redemption or new EBTC issuance)
166:     uint256 public lastRedemptionTimestamp;
167: 
168:     mapping(bytes32 => Cdp) public Cdps;
169: 
170:     uint256 public override totalStakes;
171: 
172:     // Snapshot of the value of totalStakes, taken immediately after the latest liquidation and split fee claim
173:     uint256 public totalStakesSnapshot;
174: 
175:     // Snapshot of the total collateral across the ActivePool, immediately after the latest liquidation and split fee claim
176:     uint256 public totalCollateralSnapshot;
177: 
178:     /*
179:      * systemDebtRedistributionIndex track the sums of accumulated socialized liquidations per unit staked.
180:      * During its lifetime, each stake earns:
181:      *
182:      * A systemDebt increase  of ( stake * [systemDebtRedistributionIndex - systemDebtRedistributionIndex(0)] )
183:      *
184:      * Where systemDebtRedistributionIndex(0) are snapshots of systemDebtRedistributionIndex
185:      * for the active Cdp taken at the instant the stake was made
186:      */
187:     uint256 public systemDebtRedistributionIndex;
188: 
189:     // Map active cdps to their RewardSnapshot (eBTC debt redistributed)
190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;
191: 
192:     // Error trackers for the cdp redistribution calculation
193:     uint256 public lastEBTCDebtErrorRedistribution;
194: 
195:     /* Global Index for (Full Price Per Share) of underlying collateral token */
196:     uint256 public override stEthIndex;
197:     /* Global Fee accumulator (never decreasing) per stake unit in CDPManager, similar to systemDebtRedistributionIndex */
198:     uint256 public override systemStEthFeePerUnitIndex;
199:     /* Global Fee accumulator calculation error due to integer division, similar to redistribution calculation */
200:     uint256 public override systemStEthFeePerUnitIndexError;
201:     /* Individual CDP Fee accumulator tracker, used to calculate fee split distribution */
202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;
203: 
204:     // Array of all active cdp Ids - used to to compute an approximate hint off-chain, for the sorted list insertion
205:     bytes32[] public CdpIds;
206: 
207:     /// @notice Initializes the contract with the provided addresses and sets up the required initial state
208:     /// @param _liquidationLibraryAddress The address of the Liquidation Library
209:     /// @param _authorityAddress The address of the Authority
210:     /// @param _borrowerOperationsAddress The address of Borrower Operations
211:     /// @param _collSurplusPool The address of the Collateral Surplus Pool
212:     /// @param _ebtcToken The address of the eBTC Token contract
213:     /// @param _sortedCdps The address of the Sorted CDPs contract
214:     /// @param _activePool The address of the Active Pool
215:     /// @param _priceFeed The address of the Price Feed
216:     /// @param _collateral The address of the Collateral token
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
228:         deploymentStartTime = block.timestamp;
229:         liquidationLibrary = _liquidationLibraryAddress;
230: 
231:         _initializeAuthority(_authorityAddress);
232: 
233:         borrowerOperationsAddress = _borrowerOperationsAddress;
234:         collSurplusPool = ICollSurplusPool(_collSurplusPool);
235:         ebtcToken = IEBTCToken(_ebtcToken);
236:         sortedCdps = ISortedCdps(_sortedCdps);
237:     }
238: 
239:     /// @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation
240:     /// @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.
241:     modifier nonReentrantSelfAndBOps() {
242:         require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");
243:         require(
244:             ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245:             "BorrowerOperations: Reentrancy in nonReentrant call"
246:         );
247: 
248:         locked = LOCKED;
249: 
250:         _;
251: 
252:         locked = OPEN;
253:     }
254: 
255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {
256:         _closeCdpWithoutRemovingSortedCdps(_cdpId, closedStatus);
257:         sortedCdps.remove(_cdpId);
258:     }
259: 
260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {
261:         require(
262:             closedStatus != Status.nonExistent && closedStatus != Status.active,
263:             "CdpManagerStorage: close non-exist or non-active CDP!"
264:         );
265: 
266:         uint256 cdpIdsArrayLength = CdpIds.length;
267:         _requireMoreThanOneCdpInSystem(cdpIdsArrayLength);
268: 
269:         _removeStake(_cdpId);
270: 
271:         Cdps[_cdpId].status = closedStatus;
272:         Cdps[_cdpId].coll = 0;
273:         Cdps[_cdpId].debt = 0;
274:         Cdps[_cdpId].liquidatorRewardShares = 0;
275: 
276:         cdpDebtRedistributionIndex[_cdpId] = 0;
277:         cdpStEthFeePerUnitIndex[_cdpId] = 0;
278: 
279:         _removeCdp(_cdpId, cdpIdsArrayLength);
280:     }
281: 
282:     /*
283:      * Updates snapshots of system total stakes and total collateral,
284:      * excluding a given collateral remainder from the calculation.
285:      * Used in a liquidation sequence.
286:      *
287:      * The calculation excludes a portion of collateral that is in the ActivePool:
288:      *
289:      * the total stETH liquidator reward compensation from the liquidation sequence
290:      *
291:      * The stETH as compensation must be excluded as it is always sent out at the very end of the liquidation sequence.
292:      */
293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {
294:         uint256 _totalStakesSnapshot = totalStakes;
295:         totalStakesSnapshot = _totalStakesSnapshot;
296: 
297:         uint256 _totalCollateralSnapshot = activePool.getSystemCollShares() - _collRemainder;
298:         totalCollateralSnapshot = _totalCollateralSnapshot;
299: 
300:         emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);
301:     }
302: 
303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake
304:     function _getPendingRedistributedDebt(
305:         bytes32 _cdpId
306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {
307:         Cdp storage cdp = Cdps[_cdpId];
308: 
309:         if (cdp.status != Status.active) {
310:             return (0, 0);
311:         }
312: 
313:         _debtIndexDiff = systemDebtRedistributionIndex - cdpDebtRedistributionIndex[_cdpId];
314: 
315:         if (_debtIndexDiff > 0) {
316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;
317:         } else {
318:             return (0, 0);
319:         }
320:     }
321: 
322:     /*
323:      * A Cdp has pending redistributed debt if its snapshot is less than the current rewards per-unit-staked sum:
324:      * this indicates that redistributions have occured since the snapshot was made, and the user therefore has
325:      * pending debt
326:      */
327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {
328:         if (Cdps[_cdpId].status != Status.active) {
329:             return false;
330:         }
331: 
332:         return (cdpDebtRedistributionIndex[_cdpId] < systemDebtRedistributionIndex);
333:     }
334: 
335:     /// @dev Sync Cdp debt redistribution index to global value
336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {
337:         uint256 _systemDebtRedistributionIndex = systemDebtRedistributionIndex;
338: 
339:         cdpDebtRedistributionIndex[_cdpId] = _systemDebtRedistributionIndex;
340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);
341:     }
342: 
343:     /// @dev Calculate the new collateral and debt values for a given CDP, based on pending state changes
344:     function _syncAccounting(bytes32 _cdpId) internal {
345:         // Ensure global states like systemStEthFeePerUnitIndex get updated in a timely fashion
346:         // whenever there is a CDP modification operation,
347:         // such as opening, closing, adding collateral, repaying debt, or liquidating
348:         _syncGlobalAccounting();
349: 
350:         uint256 _oldPerUnitCdp = cdpStEthFeePerUnitIndex[_cdpId];
351:         uint256 _systemStEthFeePerUnitIndex = systemStEthFeePerUnitIndex;
352: 
353:         (
354:             uint256 _newColl,
355:             uint256 _newDebt,
356:             uint256 _feeSplitDistributed,
357:             uint _pendingDebt,
358:             uint256 _debtIndexDelta
359:         ) = _calcSyncedAccounting(_cdpId, _oldPerUnitCdp, _systemStEthFeePerUnitIndex);
360: 
361:         // If any collShares or debt changes occured
362:         if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {
363:             Cdp storage _cdp = Cdps[_cdpId];
364: 
365:             uint prevCollShares = _cdp.coll;
366:             uint256 prevDebt = _cdp.debt;
367: 
368:             // Apply Fee Split
369:             if (_feeSplitDistributed > 0) {
370:                 _applyAccumulatedFeeSplit(
371:                     _cdpId,
372:                     _newColl,
373:                     _feeSplitDistributed,
374:                     _oldPerUnitCdp,
375:                     _systemStEthFeePerUnitIndex
376:                 );
377:             }
378: 
379:             // Apply Debt Redistribution
380:             if (_debtIndexDelta > 0) {
381:                 _updateRedistributedDebtIndex(_cdpId);
382: 
383:                 if (prevDebt != _newDebt) {
384:                     {
385:                         // Apply pending debt redistribution to this CDP
386:                         _cdp.debt = _newDebt;
387:                     }
388:                 }
389:             }
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
401:         }
402: 
403:         // sync per stake index for given CDP
404:         if (_oldPerUnitCdp != _systemStEthFeePerUnitIndex) {
405:             cdpStEthFeePerUnitIndex[_cdpId] = _systemStEthFeePerUnitIndex;
406:         }
407:     }
408: 
409:     // Remove borrower's stake from the totalStakes sum, and set their stake to 0
410:     function _removeStake(bytes32 _cdpId) internal {
411:         uint256 _newTotalStakes = totalStakes - Cdps[_cdpId].stake;
412:         totalStakes = _newTotalStakes;
413:         Cdps[_cdpId].stake = 0;
414:         emit TotalStakesUpdated(_newTotalStakes);
415:     }
416: 
417:     // Update borrower's stake based on their latest collateral value
418:     // and update totalStakes accordingly as well
419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {
420:         (uint256 newStake, uint256 oldStake) = _updateStakeForCdp(_cdpId);
421: 
422:         uint256 _newTotalStakes = totalStakes + newStake - oldStake;
423:         totalStakes = _newTotalStakes;
424: 
425:         emit TotalStakesUpdated(_newTotalStakes);
426: 
427:         return newStake;
428:     }
429: 
430:     // Update borrower's stake based on their latest collateral value
431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {
432:         Cdp storage _cdp = Cdps[_cdpId];
433:         uint256 newStake = _computeNewStake(_cdp.coll);
434:         uint256 oldStake = _cdp.stake;
435:         _cdp.stake = newStake;
436: 
437:         return (newStake, oldStake);
438:     }
439: 
440:     // Calculate a new stake based on the snapshots of the totalStakes and totalCollateral taken at the last liquidation
441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {
442:         uint256 stake;
443:         if (totalCollateralSnapshot == 0) {
444:             stake = _coll;
445:         } else {
446:             /*
447:              * The following check holds true because:
448:              * - The system always contains >= 1 cdp
449:              * - When we close or liquidate a cdp, we redistribute the pending rewards,
450:              * so if all cdps were closed/liquidated,
451:              * rewards wouldb�ve been emptied and totalCollateralSnapshot would be zero too.
452:              */
453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
454:             stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;
455:         }
456:         return stake;
457:     }
458: 
459:     /*
460:      * Remove a Cdp owner from the CdpOwners array, not preserving array order. Removing owner 'B' does the following:
461:      * [A B C D E] => [A E C D], and updates E's Cdp struct to point to its new array index.
462:      */
463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
464:         Status cdpStatus = Cdps[_cdpId].status;
465:         // Itb�s set in caller function `_closeCdp`
466:         require(
467:             cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468:             "CdpManagerStorage: remove non-exist or non-active CDP!"
469:         );
470: 
471:         uint128 index = Cdps[_cdpId].arrayIndex;
472:         uint256 length = cdpIdsArrayLength;
473:         uint256 idxLast = length - 1;
474: 
475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");
476: 
477:         bytes32 idToMove = CdpIds[idxLast];
478: 
479:         CdpIds[index] = idToMove;
480:         Cdps[idToMove].arrayIndex = index;
481:         emit CdpArrayIndexUpdated(idToMove, index);
482: 
483:         CdpIds.pop();
484:     }
485: 
486:     // --- Recovery Mode and TCR functions ---
487: 
488:     // Calculate TCR given an price, and the entire system coll and debt.
489:     function _computeTCRWithGivenSystemValues(
490:         uint256 _systemCollShares,
491:         uint256 _systemDebt,
492:         uint256 _price
493:     ) internal view returns (uint256) {
494:         uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);
495:         return EbtcMath._computeCR(_totalColl, _systemDebt, _price);
496:     }
497: 
498:     // --- Staking-Reward Fee split functions ---
499: 
500:     /// @notice Claim split fee if there is staking-reward coming
501:     /// @notice and update global index & fee-per-unit variables
502:     /// @dev only BorrowerOperations is allowed to call this
503:     /// @dev otherwise use syncGlobalAccountingAndGracePeriod()
504:     function syncGlobalAccounting() external {
505:         _requireCallerIsBorrowerOperations();
506:         _syncGlobalAccounting();
507:     }
508: 
509:     function _syncGlobalAccounting() internal {
510:         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();
511:         _syncStEthIndex(_oldIndex, _newIndex);
512:         if (_newIndex > _oldIndex && totalStakes > 0) {
513:             (
514:                 uint256 _feeTaken,
515:                 uint256 _newFeePerUnit,
516:                 uint256 _perUnitError
517:             ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
518:             _takeSplitAndUpdateFeePerUnit(_feeTaken, _newFeePerUnit, _perUnitError);
519:             _updateSystemSnapshotsExcludeCollRemainder(0);
520:         }
521:     }
522: 
523:     /// @notice Claim fee split, if there is staking-reward coming
524:     /// @notice and update global index & fee-per-unit variables
525:     /// @notice and toggles Grace Period accordingly.
526:     /// @dev Call this if you want to help eBTC system to accrue split fee
527:     function syncGlobalAccountingAndGracePeriod() public {
528:         _syncGlobalAccounting(); // Apply // Could trigger RM
529:         _syncGracePeriod(); // Synch Grace Period
530:     }
531: 
532:     /// @return existing(old) local stETH index AND
533:     /// @return current(new) stETH index from collateral token
534:     function _readStEthIndex() internal view returns (uint256, uint256) {
535:         return (stEthIndex, collateral.getPooledEthByShares(DECIMAL_PRECISION));
536:     }
537: 
538:     // Update the global index via collateral token
539:     function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {
540:         if (_newIndex != _oldIndex) {
541:             stEthIndex = _newIndex;
542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);
543:         }
544:     }
545: 
546:     /// @notice Calculate fee for given pair of collateral indexes
547:     /// @param _newIndex The value synced with stETH.getPooledEthByShares(1e18)
548:     /// @param _prevIndex The cached global value of `stEthIndex`
549:     /// @return _feeTaken The fee split in collateral token which will be deduced from current total system collateral
550:     /// @return _deltaFeePerUnit The fee split increase per unit, used to added to `systemStEthFeePerUnitIndex`
551:     /// @return _perUnitError The fee split calculation error, used to update `systemStEthFeePerUnitIndexError`
552:     function calcFeeUponStakingReward(
553:         uint256 _newIndex,
554:         uint256 _prevIndex
555:     ) public view returns (uint256, uint256, uint256) {
556:         require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");
557:         uint256 deltaIndex = _newIndex - _prevIndex;
558:         uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;
559: 
560:         // we take the fee for all CDPs immediately which is scaled by index precision
561:         uint256 _deltaFeeSplit = deltaIndexFees * getSystemCollShares();
562:         uint256 _cachedAllStakes = totalStakes;
563:         // return the values to update the global fee accumulator
564:         uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;
565:         uint256 _deltaFeeSplitShare = (_feeTaken * DECIMAL_PRECISION) +
566:             systemStEthFeePerUnitIndexError;
567:         uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;
568:         uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes);
569:         return (_feeTaken, _deltaFeePerUnit, _perUnitError);
570:     }
571: 
572:     // Take the cut from staking reward
573:     // and update global fee-per-unit accumulator
574:     function _takeSplitAndUpdateFeePerUnit(
575:         uint256 _feeTaken,
576:         uint256 _newPerUnit,
577:         uint256 _newErrorPerUnit
578:     ) internal {
579:         uint256 _oldPerUnit = systemStEthFeePerUnitIndex;
580: 
581:         systemStEthFeePerUnitIndex = _newPerUnit;
582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;
583: 
584:         require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");
585:         activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken);
586: 
587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);
588:     }
589: 
590:     // Apply accumulated fee split distributed to the CDP
591:     // and update its accumulator tracker accordingly
592:     function _applyAccumulatedFeeSplit(
593:         bytes32 _cdpId,
594:         uint256 _newColl,
595:         uint256 _feeSplitDistributed,
596:         uint256 _oldPerUnitCdp,
597:         uint256 _systemStEthFeePerUnitIndex
598:     ) internal {
599:         // apply split fee to given CDP
600:         Cdps[_cdpId].coll = _newColl;
601: 
602:         emit CdpFeeSplitApplied(
603:             _cdpId,
604:             _oldPerUnitCdp,
605:             _systemStEthFeePerUnitIndex,
606:             _feeSplitDistributed,
607:             _newColl
608:         );
609:     }
610: 
611:     /// @notice Calculate the applied split fee(scaled by 1e18) and the resulting CDP collateral share after applied
612:     /// @param _cdpId The Cdp to which the calculated split fee is going to be applied
613:     /// @param _systemStEthFeePerUnitIndex The fee-per-stake-unit value to be used in fee split calculation, could be result of calcFeeUponStakingReward()
614:     /// @return _feeSplitDistributed The applied fee split to the specified Cdp (scaled up by 1e18)
615:     /// @return _cdpCol The new collateral share of the specified Cdp after fe split applied
616:     function getAccumulatedFeeSplitApplied(
617:         bytes32 _cdpId,
618:         uint256 _systemStEthFeePerUnitIndex
619:     ) public view returns (uint256, uint256) {
620:         uint256 _cdpStEthFeePerUnitIndex = cdpStEthFeePerUnitIndex[_cdpId];
621:         uint256 _cdpCol = Cdps[_cdpId].coll;
622: 
623:         if (
624:             _cdpStEthFeePerUnitIndex == 0 ||
625:             _cdpCol == 0 ||
626:             _cdpStEthFeePerUnitIndex == _systemStEthFeePerUnitIndex
627:         ) {
628:             return (0, _cdpCol);
629:         }
630: 
631:         uint256 _feeSplitDistributed = Cdps[_cdpId].stake *
632:             (_systemStEthFeePerUnitIndex - _cdpStEthFeePerUnitIndex);
633: 
634:         uint256 _scaledCdpColl = _cdpCol * DECIMAL_PRECISION;
635: 
636:         if (_scaledCdpColl > _feeSplitDistributed) {
637:             return (
638:                 _feeSplitDistributed,
639:                 (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
640:             );
641:         } else {
642:             // extreme unlikely case to skip fee split on this CDP to avoid revert
643:             return (0, _cdpCol);
644:         }
645:     }
646: 
647:     // -- Modifier functions --
648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {
649:         require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");
650:     }
651: 
652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {
653:         require(
654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655:             "CdpManager: Only one cdp in the system"
656:         );
657:     }
658: 
659:     function _requireCallerIsBorrowerOperations() internal view {
660:         require(
661:             msg.sender == borrowerOperationsAddress,
662:             "CdpManager: Caller is not the BorrowerOperations contract"
663:         );
664:     }
665: 
666:     // --- Helper functions ---
667: 
668:     /// @notice Return the Nominal Collateral Ratio (NICR) of the specified Cdp as "cached view" (maybe outdated).
669:     /// @dev Takes a cdp's pending coll and debt rewards from redistributions into account.
670:     /// @param _cdpId The CdpId whose NICR to be queried
671:     /// @return The Nominal Collateral Ratio (NICR) of the specified Cdp.
672:     /// @dev Use getSyncedNominalICR() instead if pending fee split and debt redistribution should be considered
673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {
674:         (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);
675: 
676:         uint256 NICR = EbtcMath._computeNominalCR(currentCollShares, currentEBTCDebt);
677:         return NICR;
678:     }
679: 
680:     /// @notice Return the Nominal Collateral Ratio (NICR) of the specified Cdp.
681:     /// @dev Takes a cdp's pending coll and debt rewards as well as stETH Index into account.
682:     /// @param _cdpId The CdpId whose NICR to be queried
683:     /// @return The Nominal Collateral Ratio (NICR) of the specified Cdp with fee split and debt redistribution considered.
684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {
685:         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();
686:         (, uint256 _newGlobalSplitIdx, ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
687:         (uint256 _newColl, uint256 _newDebt, , uint256 _pendingDebt, ) = _calcSyncedAccounting(
688:             _cdpId,
689:             cdpStEthFeePerUnitIndex[_cdpId],
690:             _newGlobalSplitIdx /// NOTE: This is latest index
691:         );
692: 
693:         uint256 NICR = EbtcMath._computeNominalCR(_newColl, _newDebt);
694:         return NICR;
695:     }
696: 
697:     /// @notice Return the Individual Collateral Ratio (ICR) of the specified Cdp as "cached view" (maybe outdated).
698:     /// @param _cdpId The CdpId whose ICR to be queried
699:     /// @return The Individual Collateral Ratio (ICR) of the specified Cdp.
700:     /// @dev Use getSyncedICR() instead if pending fee split and debt redistribution should be considered
701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
702:         (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);
703:         uint256 ICR = _calculateCR(currentCollShares, currentEBTCDebt, _price);
704:         return ICR;
705:     }
706: 
707:     function _calculateCR(
708:         uint256 currentCollShare,
709:         uint256 currentDebt,
710:         uint256 _price
711:     ) internal view returns (uint256) {
712:         uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);
713:         return EbtcMath._computeCR(_underlyingCollateral, currentDebt, _price);
714:     }
715: 
716:     /// @notice Return the pending extra debt assigned to the Cdp from liquidation redistribution, calcualted by Cdp's stake
717:     /// @param _cdpId The CdpId whose pending debt redistribution to be queried
718:     /// @return pendingEBTCDebtReward The pending debt redistribution of the specified Cdp.
719:     function getPendingRedistributedDebt(
720:         bytes32 _cdpId
721:     ) public view returns (uint256 pendingEBTCDebtReward) {
722:         (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);
723:         return _pendingDebt;
724:     }
725: 
726:     /// @return Whether the debt redistribution tracking index of the specified Cdp is less than the global tracking one (meaning it might get pending debt redistribution)
727:     /// @param _cdpId The CdpId whose debt redistribution tracking index to be queried against the gloabl one
728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {
729:         return _hasRedistributedDebt(_cdpId);
730:     }
731: 
732:     // Return the Cdps entire debt and coll struct
733:     function _getSyncedDebtAndCollShares(
734:         bytes32 _cdpId
735:     ) internal view returns (CdpDebtAndCollShares memory) {
736:         (uint256 entireDebt, uint256 entireColl) = getSyncedDebtAndCollShares(_cdpId);
737:         return CdpDebtAndCollShares(entireDebt, entireColl);
738:     }
739: 
740:     /// @notice Calculate the Cdps entire debt and coll, including pending debt redistributions and collateral reduction from split fee.
741:     /// @param _cdpId The CdpId to be queried
742:     /// @return debt The total debt value of the Cdp including debt redistribution considered
743:     /// @return coll The total collateral value of the Cdp including possible fee split considered
744:     /// @dev Should always use this as the first(default) choice for Cdp position size query
745:     function getSyncedDebtAndCollShares(
746:         bytes32 _cdpId
747:     ) public view returns (uint256 debt, uint256 coll) {
748:         (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(
749:             _cdpId,
750:             cdpStEthFeePerUnitIndex[_cdpId],
751:             systemStEthFeePerUnitIndex
752:         );
753:         coll = _newColl;
754:         debt = _newDebt;
755:     }
756: 
757:     /// @dev calculate pending global state change to be applied:
758:     /// @return split fee taken (if any) AND
759:     /// @return new split index per stake unit AND
760:     /// @return new split index error
761:     function _calcSyncedGlobalAccounting(
762:         uint256 _newIndex,
763:         uint256 _oldIndex
764:     ) internal view returns (uint256, uint256, uint256) {
765:         if (_newIndex > _oldIndex && totalStakes > 0) {
766:             /// @audit-ok We don't take the fee if we had a negative rebase
767:             (
768:                 uint256 _feeTaken,
769:                 uint256 _deltaFeePerUnit,
770:                 uint256 _perUnitError
771:             ) = calcFeeUponStakingReward(_newIndex, _oldIndex);
772: 
773:             // calculate new split per stake unit
774:             uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
775:             return (_feeTaken, _newPerUnit, _perUnitError);
776:         } else {
777:             return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);
778:         }
779:     }
780: 
781:     /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):
782:     /// @return new CDP collateral share after pending change applied
783:     /// @return new CDP debt after pending change applied
784:     /// @return split fee applied to given CDP
785:     /// @return redistributed debt applied to given CDP
786:     /// @return delta between debt redistribution index of given CDP and global tracking index
787:     function _calcSyncedAccounting(
788:         bytes32 _cdpId,
789:         uint256 _cdpPerUnitIdx,
790:         uint256 _systemStEthFeePerUnitIndex
791:     ) internal view returns (uint256, uint256, uint256, uint256, uint256) {
792:         uint256 _feeSplitApplied;
793:         uint256 _newCollShare = Cdps[_cdpId].coll;
794: 
795:         // processing split fee to be applied
796:         if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
797:             (
798:                 uint256 _feeSplitDistributed,
799:                 uint256 _newCollShareAfter
800:             ) = getAccumulatedFeeSplitApplied(_cdpId, _systemStEthFeePerUnitIndex);
801:             _feeSplitApplied = _feeSplitDistributed;
802:             _newCollShare = _newCollShareAfter;
803:         }
804: 
805:         // processing redistributed debt to be applied
806:         (
807:             uint256 _newDebt,
808:             uint256 pendingDebtRedistributed,
809:             uint256 _debtIndexDelta
810:         ) = _getSyncedCdpDebtAndRedistribution(_cdpId);
811: 
812:         return (
813:             _newCollShare,
814:             _newDebt,
815:             _feeSplitApplied,
816:             pendingDebtRedistributed,
817:             _debtIndexDelta
818:         );
819:     }
820: 
821:     /// @return CDP debt and pending redistribution from liquidation applied
822:     function _getSyncedCdpDebtAndRedistribution(
823:         bytes32 _cdpId
824:     ) internal view returns (uint256, uint256, uint256) {
825:         (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(
826:             _cdpId
827:         );
828:         uint256 _newDebt = Cdps[_cdpId].debt;
829:         if (pendingDebtRedistributed > 0) {
830:             _newDebt = _newDebt + pendingDebtRedistributed;
831:         }
832:         return (_newDebt, pendingDebtRedistributed, _debtIndexDelta);
833:     }
834: 
835:     /// @notice Calculate the Cdps entire debt, including pending debt redistributions.
836:     /// @param _cdpId The CdpId to be queried
837:     /// @return _newDebt The total debt value of the Cdp including debt redistribution considered
838:     /// @dev Should always use this as the first(default) choice for Cdp debt query
839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {
840:         (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);
841:         return _newDebt;
842:     }
843: 
844:     /// @notice Calculate the Cdps entire collateral, including pending fee split to be applied
845:     /// @param _cdpId The CdpId to be queried
846:     /// @return _newColl The total collateral value of the Cdp including fee split considered
847:     /// @dev Should always use this as the first(default) choice for Cdp collateral query
848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {
849:         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();
850:         (, uint256 _newGlobalSplitIdx, ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
851:         (uint256 _newColl, , , , ) = _calcSyncedAccounting(
852:             _cdpId,
853:             cdpStEthFeePerUnitIndex[_cdpId],
854:             _newGlobalSplitIdx
855:         );
856:         return _newColl;
857:     }
858: 
859:     /// @notice Calculate the Cdps ICR, including pending debt distribution and fee split to be applied
860:     /// @param _cdpId The CdpId to be queried
861:     /// @param _price The ETH:eBTC price to be used in ICR calculation
862:     /// @return The ICR of the Cdp including debt distribution and fee split considered
863:     /// @dev Should always use this as the first(default) choice for Cdp ICR query
864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
865:         uint256 _debt = getSyncedCdpDebt(_cdpId);
866:         uint256 _collShare = getSyncedCdpCollShares(_cdpId);
867:         return _calculateCR(_collShare, _debt, _price);
868:     }
869: 
870:     /// @notice Calculate the TCR, including pending debt distribution and fee split to be taken
871:     /// @param _price The ETH:eBTC price to be used in TCR calculation
872:     /// @return The TCR of the eBTC system including debt distribution and fee split considered
873:     /// @dev Should always use this as the first(default) choice for TCR query
874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {
875:         (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();
876:         (uint256 _feeTaken, , ) = _calcSyncedGlobalAccounting(_newIndex, _oldIndex);
877: 
878:         uint256 _systemCollShare = activePool.getSystemCollShares();
879:         if (_feeTaken > 0) {
880:             _systemCollShare = _systemCollShare - _feeTaken;
881:         }
882:         uint256 _systemDebt = activePool.getSystemDebt();
883:         return _calculateCR(_systemCollShare, _systemDebt, _price);
884:     }
885: 
886:     /// @param icr The ICR of a Cdp to check if liquidatable
887:     /// @param tcr The TCR of the eBTC system used to determine if Recovery Mode is triggered
888:     /// @return whether the Cdp of specified icr is liquidatable with specified tcr
889:     /// @dev The flag will only be set to true if enough time has passed since Grace Period starts
890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {
891:         return _checkICRAgainstTCR(icr, tcr) && _recoveryModeGracePeriodPassed();
892:     }
893: 
894:     /// @dev Check if enough time has passed for grace period after enabled
895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {
896:         // we have waited enough
897:         uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;
898:         return
899:             cachedLastGracePeriodStartTimestamp != UNSET_TIMESTAMP &&
900:             block.timestamp > cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration;
901:     }
902: }


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L19-L902) 


</details>


### [GAS&#x2011;52] Use `do while` loops instead of `for` loops 
A `do while` loop will cost less gas since the condition is not being checked for the first iteration, Check my example on [github](https://github.com/he110-1/gasOptimization/blob/main/forToDoWhileOptimizationProof.sol). Actually, `do while` alwayse cast less gas compared to `For` check my second example [github](https://github.com/he110-1/gasOptimization/blob/main/forToDoWhileOptimizationProof2.sol)


*There are 15 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

753:         for (vars.i = _start; ; ) {

816:         for (vars.i = _start; ; ) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L753-L753) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L816-L816)


```solidity

File: packages/contracts/contracts/Governor.sol

46:         for (uint256 i = 0; i < users.length(); i++) {

76:         for (uint8 i = 0; i < type(uint8).max; i++) {

98:         for (uint8 i = 0; i < type(uint8).max; i++) {

122:         for (uint8 i = 0; i < roleIds.length; i++) {

57:             for (uint256 i = 0; i < _usrs.length; i++) {

84:             for (uint8 i = 0; i < type(uint8).max; i++) {

107:             for (uint8 i = 0; i < type(uint8).max; i++) {

137:             for (uint256 i = 0; i < _sigs.length; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L46-L46) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L76-L76), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L98-L98), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L84-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L107-L107), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L137-L137)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

432:         for (uint256 i = 0; i < _len; ++i) {

449:         for (uint i = 0; i < _len; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L432-L432) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L449-L449)


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

385:         for (uint256 i; i < swapLength; ) {

438:             for (uint256 i; i < length; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L385-L385) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L438-L438)


```solidity

File: packages/contracts/contracts/SimplifiedDiamondLike.sol

114:         for (uint256 i; i < length; ) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SimplifiedDiamondLike.sol#L114-L114) 


</details>


### [GAS&#x2011;53] Use `+=` for `mapping`s 
Using `+=` for mappings saves **[40 gas](https://gist.github.com/IllIllI000/4fc5f83a9edc6ed16677258bf58f32a5)** due to not having to recalculate the mapping's value's hash


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/EBTCToken.sol

258:         _balances[recipient] = _balances[recipient] + amount;

266:         _balances[account] = _balances[account] + amount;


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L258-L258) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/EBTCToken.sol#L266-L266)


</details>


### [GAS&#x2011;54] Avoid transferring amounts of zero in order to save gas 
Skipping the external call when nothing will be transferred, will save at least **100 gas**


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/ActivePool.sol

283:         collateral.transferFrom(address(receiver), address(this), amountWithFee);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/ActivePool.sol#L283-L283) 


```solidity

File: packages/contracts/contracts/BorrowerOperations.sol

1100:         ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L1100-L1100) 


```solidity

File: packages/contracts/contracts/LeverageMacroBase.sol

129:             IERC20(operation.tokenToTransferIn).safeTransferFrom(

237:         IERC20(token).safeTransfer(msg.sender, amount);


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L129-L129) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L237-L237)


</details>


### [GAS&#x2011;55] When no `addresses` are used `abi.encodepacked()` Outperforms `abi.encode()` in Efficiency 
when dealing with non address type parameters `encodepacked()` function less gas than `encode()`. For more details check the following [comparison](https://github.com/ConnorBlockchain/Solidity-Encode-Gas-Comparison)


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

152:                 abi.encode(operation)

159:                 abi.encode(operation)


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L152-L152) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LeverageMacroBase.sol#L159-L159)


</details>


### [GAS&#x2011;56] Simple checks for zero `uint` can be done using assembly to save gas 



*There are 31 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

847:             _stEthBalanceDecrease == 0,

808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L831-L831) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L847-L847), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L808-L808), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/BorrowerOperations.sol#L808-L808)


```solidity

File: packages/contracts/contracts/CdpManager.sol

159:         if (newDebt == 0) {

377:         if (_maxIterations == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L159-L159) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManager.sol#L377-L377)


```solidity

File: packages/contracts/contracts/LiquidationLibrary.sol

144:         if (_liqState.partialAmount == 0) {

417:         if (newColl == 0) {

863:         if (_debt == 0) {

158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&

159:                 liquidationValues.debtToBurn == 0


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L144-L144) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L417-L417), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L863-L863), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L158-L158), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/LiquidationLibrary.sol#L159-L159)


```solidity

File: packages/contracts/contracts/CdpManagerStorage.sol

443:         if (totalCollateralSnapshot == 0) {

624:             _cdpStEthFeePerUnitIndex == 0 ||

625:             _cdpCol == 0 ||


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L443-L443) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L624-L624), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/CdpManagerStorage.sol#L625-L625)


```solidity

File: packages/contracts/contracts/PriceFeed.sol

475:         if (_response.answer == 0) {

532:         if (minPrice == 0) return false;

777:         if (_roundId == 0) return false;

471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

422:             _response.timestampStEthEth == 0 ||

420:             _response.timestampEthBtc == 0 ||


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L475-L475) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L532-L532), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L777-L777), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L471-L471), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L695-L695), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L695-L695), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L422-L422), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/PriceFeed.sol#L420-L420)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

89:         if (_size == 0) {

305:         if (maxArraySize == 0) {

537:         return data.size == 0;

352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L89-L89) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L305-L305), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L537-L537), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L352-L352)


```solidity

File: packages/contracts/contracts/HintHelpers.sol

78:         if (_maxIterations == 0) {

171:         if (arrayLength == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L78-L78) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/HintHelpers.sol#L171-L171)


```solidity

File: packages/contracts/contracts/Dependencies/EbtcMath.sol

64:         if (_minutes == 0) {

74:             if (n % 2 == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L64-L64) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/EbtcMath.sol#L74-L74)


```solidity

File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

124:             if (enabledFunctionSigsByTarget[target].length() == 0) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Dependencies/RolesAuthority.sol#L124-L124) 


</details>


### [GAS&#x2011;57] `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops 
The `unchecked` keyword is new in solidity version 0.8.0, so this only applies to that version or higher, which these instances are. This saves **30-40 gas [per loop](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked)**


*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L46-L46) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L57-L57), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L76-L76), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L84-L84), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L98-L98), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L107-L107), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L122-L122), [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/Governor.sol#L137-L137)


```solidity

File: packages/contracts/contracts/SortedCdps.sol

432:         for (uint256 i = 0; i < _len; ++i) {

449:         for (uint i = 0; i < _len; ++i) {


```

[link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L432-L432) , [link](https://github.com/code-423n4/2023-10-badger/blob/main//packages/contracts/contracts/SortedCdps.sol#L449-L449)


</details>
