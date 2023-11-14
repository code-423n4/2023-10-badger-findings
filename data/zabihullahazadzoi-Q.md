## Low Issues


| |Issue|Instances|
|-|:-|:-:|
| [L-1](#L-1) | Code does not follow the best practice of check-effects-interaction | 1 |
| [L-2](#L-2) | Consider implementing two-step procedure for updating protocol addresses | 13 |
| [L-3](#L-3) | Division by zero not prevented | 19 |
| [L-4](#L-4) | Empty `receive()`/`fallback()` function | 1 |
| [L-5](#L-5) | Loss of precision | 33 |
| [L-6](#L-6) | Missing checks for `address(0x0)` in the constructor | 19 |
| [L-7](#L-7) | Missing checks for address(0x0) when updating address state variables | 51 |
| [L-8](#L-8) | Missing contract-existence checks before yul `call()` | 2 |
| [L-9](#L-9) | Numbers downcast to `address`es may result in collisions | 1 |
| [L-10](#L-10) | `receive()`/`payable fallback()` function does not authorize requests | 2 |
| [L-11](#L-11) | `require()` should be used instead of `assert()` | 1 |
| [L-12](#L-12) | `safeApprove()` is deprecated | 2 |
| [L-13](#L-13) | Some tokens may revert when large transfers are made | 6 |
| [L-14](#L-14) | State variables not capped at reasonable values | 11 |
| [L-15](#L-15) | Subtraction may underflow if multiplication is too large | 6 |

 Total: 168 instances over 15 issues.
 
## Non Critical Issues


| |Issue|Instances|
|-|:-|:-:|
| [NC-1](#NC-1) | Large or complicated code bases should implement invariant tests | 1 |
| [NC-2](#NC-2) | Adding a return statement when the function defines a named return variable, is redundant | 9 |
| [NC-3](#NC-3) | Missing checks for `address(0)` when assigning values to address state variables | 4 |
| [NC-4](#NC-4) | Array indices should be referenced via enums rather than via numeric literals | 2 |
| [NC-5](#NC-5) | Array is `push()ed` but not `pop()ed` | 1 |
| [NC-6](#NC-6) | Assembly blocks should have extensive comments | 4 |
| [NC-7](#NC-7) | Avoid the use of sensitive terms | 7 |
| [NC-8](#NC-8) | Cast to bytes or bytes32 for clearer semantic meaning | 1 |
| [NC-9](#NC-9) | Complex casting | 2 |
| [NC-10](#NC-10) | Common functions should be refactored to a common base contract | 1 |
| [NC-11](#NC-11) | Consider adding formal verification proofs | 41 |
| [NC-12](#NC-12) | Consider bounding input array length | 10 |
| [NC-13](#NC-13) | Consider moving msg.sender checks to a common authorization `modifier` | 23 |
| [NC-14](#NC-14) | Consider using delete rather than assigning zero/false to clear values | 6 |
| [NC-15](#NC-15) | Consider using descriptive constants when passing zero as a function argument | 15 |
| [NC-16](#NC-16) | Constant redefined elsewhere | 75 |
| [NC-17](#NC-17) | Constants in comparisons should appear on the left side | 93 |
| [NC-18](#NC-18) | constants should be defined rather than using magic numbers | 31 |
| [NC-19](#NC-19) | Contracts should expose an interface | 83 |
| [NC-20](#NC-20) | Contract timekeeping will break earlier than the Ethereum network itself will stop working | 1 |
| [NC-21](#NC-21) | Contracts should have full test coverage | 1 |
| [NC-22](#NC-22) | Control structures do not follow the Solidity Style Guide | 251 |
| [NC-23](#NC-23) | Custom errors should be used rather than revert()/require() | 150 |
| [NC-24](#NC-24) | else-block not required | 15 |
| [NC-25](#NC-25) | Empty bytes check is missing | 144 |
| [NC-26](#NC-26) | Empty function body | 3 |
| [NC-27](#NC-27) | Error messages should be descriptive, rather than cryptic | 2 |
| [NC-28](#NC-28) | Event is not properly indexed | 8 |
| [NC-29](#NC-29) | Events are missing sender information | 65 |
| [NC-30](#NC-30) | Events may be emitted out of order due to reentrancy | 5 |
| [NC-31](#NC-31) | Events should use parameters to convey information | 2 |
| [NC-32](#NC-32) | Events that mark critical parameter changes should contain both the old and the new value | 18 |
| [NC-33](#NC-33) | Expressions for constant values should use immutable rather than constant | 7 |
| [NC-34](#NC-34) | High cyclomatic complexity | 4 |
| [NC-35](#NC-35) | if-statement can be converted to a ternary | 26 |
| [NC-36](#NC-36) | Import declarations should import specific identifiers, rather than the whole file | 96 |
| [NC-37](#NC-37) | Interfaces should be defined in separate files from their usage | 2 |
| [NC-38](#NC-38) | `internal` functions not called by the contract should be removed | 1 |
| [NC-39](#NC-39) | Large numeric literals should use underscores for readability | 10 |
| [NC-40](#NC-40) | Long functions should be refactored into multiple, smaller, functions | 15 |
| [NC-41](#NC-41) | Missing checks constructor/initializer assignments | 30 |
| [NC-42](#NC-42) | Missing checks for state variable assignments | 17 |
| [NC-43](#NC-43) | Missing checks for state variable assignments | 17 |
| [NC-44](#NC-44) | Multiple `address`/`ID` mappings can be combined into a single `mapping` of an `address`/`ID` to a struct, for readability | 6 |
| [NC-45](#NC-45) | Named imports of parent contracts are missing | 17 |
| [NC-46](#NC-46) | NatSpec: Contract declarations should have `@author` tags | 36 |
| [NC-47](#NC-47) | NatSpec: Contract declarations should have descriptions | 25 |
| [NC-48](#NC-48) | NatSpec: Contract declarations should have `@dev` tags | 30 |
| [NC-49](#NC-49) | NatSpec: Contract declarations should have `@notice` tags | 28 |
| [NC-50](#NC-50) | NatSpec: Contract declarations should have `@title` tags | 30 |
| [NC-51](#NC-51) | NatSpec: Event declarations should have descriptions | 54 |
| [NC-52](#NC-52) | NatSpec: file is missing NatSpec | 14 |
| [NC-53](#NC-53) | NatSpec: Function `@param` tag is missing | 255 |
| [NC-54](#NC-54) | NatSpec: Function `@return` tag is missing | 167 |
| [NC-55](#NC-55) | NatSpec: Function declarations should have` @notice` tags | 327 |
| [NC-56](#NC-56) | NatSpec: Function declarations should have descriptions | 275 |
| [NC-57](#NC-57) | NatSpec: Modifier declarations should have descriptions | 3 |
| [NC-58](#NC-58) | NatSpec: state variable declarations should have descriptions | 155 |
| [NC-59](#NC-59) | Not using the named return variables anywhere in the function is confusing | 8 |
| [NC-60](#NC-60) | Overflows in unchecked blocks | 4 |
| [NC-61](#NC-61) | Polymorphic functions make security audits more time-consuming and error-prone | 4 |
| [NC-62](#NC-62) | Functions not used internally could be marked external | 21 |
| [NC-63](#NC-63) | `pure` function accesses storage | 18 |
| [NC-64](#NC-64) | Duplicated require()/revert() checks should be refactored to a modifier or function. | 4 |
| [NC-65](#NC-65) | require()/revert() statements should have descriptive reason strings | 12 |
| [NC-66](#NC-66) | Return values of `approve()` not checked | 12 |
| [NC-67](#NC-67) | Setters should prevent re-setting of the same value | 6 |
| [NC-68](#NC-68) | Style guide: Contract does not follow the Solidity style guide’s suggested layout ordering | 18 |
| [NC-69](#NC-69) | Style guide: Function names should use lowerCamelCase | 48 |
| [NC-70](#NC-70) | Style guide: Function ordering does not follow the Solidity style guide | 58 |
| [NC-71](#NC-71) | Style guide: Lines are too long | 150 |
| [NC-72](#NC-72) | Style guide: Non-external/public function names should begin with an underscore | 4 |
| [NC-73](#NC-73) | Style guide: Non-external/public variable names should begin with an underscore | 23 |
| [NC-74](#NC-74) | Style guide: State and local variables should be named using lowerCamelCase | 95 |
| [NC-75](#NC-75) | Style guide: Strings should use double quotes rather than single quotes | 9 |
| [NC-76](#NC-76) | Style guide: Top level pragma declarations should be separated by two blank lines | 39 |
| [NC-77](#NC-77) | Style guide: Variable names for constants are improperly named | 1 |
| [NC-78](#NC-78) | Style guide: Variable names for immutables should use CONSTANT_CASE | 44 |
| [NC-79](#NC-79) | TODO Left in the code | 1 |
| [NC-80](#NC-80) | Unused event definition | 4 |
| [NC-81](#NC-81) | Unused public contract variable | 8 |
| [NC-82](#NC-82) | Unused file | 2 |
| [NC-83](#NC-83) | Unused function parameter | 192 |
| [NC-84](#NC-84) | Unused import | 3 |
| [NC-85](#NC-85) | Use bit shifts in an immutable variable rather than long bit masks of a single bit, for readability | 1 |
| [NC-86](#NC-86) | Use bytes.concat() on bytes instead of abi.encodePacked() for clearer semantic meaning | 3 |
| [NC-87](#NC-87) | Use of override is unnecessary. | 103 |
| [NC-88](#NC-88) | Utility contracts can be made into libraries | 3 |
| [NC-89](#NC-89) | Variables need not be initialized to zero | 18 |
| [NC-90](#NC-90) | Visibility should be set explicitly rather than defaulting to internal | 6 |

 Total: 3723 instances over 90 issues.

  ### <a name="L-1"></a>[L-1] Code does not follow the best practice of check-effects-interaction
Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  syncGlobalAccountingAndGracePeriod() prior to this assignment
 398:         feeRecipientAddress = _feeRecipientAddress;

```

### <a name="L-2"></a>[L-2] Consider implementing two-step procedure for updating protocol addresses
A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must "accept" the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement [EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the "set" functions ensure that the recipient is of the right interface type.

 There are 13 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 628:     function setPositionManagerApproval(
             address _positionManager,
             PositionManagerApproval _approval
         ) external override {

 1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 946:     function updateCdp(
             bytes32 _cdpId,
             address _borrower,
             uint256 _coll,
             uint256 _debt,
             uint256 _newColl,
             uint256 _newDebt
         ) external {
             _requireCallerIsBorrowerOperations();

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 38:     function setAuthority(address newAuthority) public virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 85:     function setPublicCapability(
            address target,
            bytes4 functionSig,
            bool enabled
        ) public virtual requiresAuth {

 106:     function setRoleCapability(
             uint8 role,
             address target,
             bytes4 functionSig,
             bool enabled
         ) public virtual requiresAuth {

 147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 66:     function updateCdp(

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 23:     function setPositionManagerApproval(

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 51:     function setFallbackHandler(bytes4 sig, address handler) external {

```

### <a name="L-3"></a>[L-3] Division by zero not prevented
The divisions below take an input parameter or state variable which does not have any zero-value checks, which may lead to the functions reverting when zero is passed.

 There are 19 instances:

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

 671:         uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

 706:         return (baseRate * decayFactor) / DECIMAL_PRECISION;

 712:                 ? ((block.timestamp - lastRedemptionTimestamp) / SECONDS_IN_ONE_MINUTE)

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 316:             pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;

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

 579:             _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

 882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;

```

### <a name="L-4"></a>[L-4] Empty `receive()`/`fallback()` function
If the intention is for Ether sent by a caller to be used for an actual purpose (i.e. the function is not just a WETH `withdraw()` handler), the function should call another function (e.g. call `weth.deposit()` and use the token on the caller’s behalf) or at least emit an event to track that funds were sent directly to it.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 160:     receive() external payable {

```

### <a name="L-5"></a>[L-5] Loss of precision
Division by large numbers may result in the result being zero, due to solidity not supporting fractions. Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator.

 There are 33 instances:

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

### <a name="L-6"></a>[L-6] Missing checks for `address(0x0)` in the constructor
'Constructors often take address parameters to initialize important components of a contract, such as owner or linked contracts. However, without a checking, there's a risk that an address parameter could be mistakenly set to the zero address (0x0). This could be due to an error or oversight during contract deployment. A zero address in a crucial role can cause serious issues, as it cannot perform actions like a normal address, and any funds sent to it will be irretrievable. It's therefore crucial to include a zero address check in constructors to prevent such potential problems. If a zero address is detected, the constructor should revert the transaction.'

 There are 19 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  _borrowerOperationsAddress, _cdpManagerAddress, _collTokenAddress, _collSurplusAddress, _feeRecipientAddress not checked!
 46:     constructor(
            address _borrowerOperationsAddress,
            address _cdpManagerAddress,
            address _collTokenAddress,
            address _collSurplusAddress,
            address _feeRecipientAddress
        ) {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  _cdpManagerAddress, _activePoolAddress, _collSurplusPoolAddress, _priceFeedAddress, _sortedCdpsAddress, _ebtcTokenAddress, _feeRecipientAddress, _collTokenAddress not checked!
 107:     constructor(
             address _cdpManagerAddress,
             address _activePoolAddress,
             address _collSurplusPoolAddress,
             address _priceFeedAddress,
             address _sortedCdpsAddress,
             address _ebtcTokenAddress,
             address _feeRecipientAddress,
             address _collTokenAddress
         ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  _liquidationLibraryAddress, _authorityAddress, _borrowerOperationsAddress, _collSurplusPoolAddress, _ebtcTokenAddress, _sortedCdpsAddress, _activePoolAddress, _priceFeedAddress, _collTokenAddress not checked!
 30:     constructor(
            address _liquidationLibraryAddress,
            address _authorityAddress,
            address _borrowerOperationsAddress,
            address _collSurplusPoolAddress,
            address _ebtcTokenAddress,
            address _sortedCdpsAddress,
            address _activePoolAddress,
            address _priceFeedAddress,
            address _collTokenAddress
        )
            CdpManagerStorage(
                _liquidationLibraryAddress,
                _authorityAddress,
                _borrowerOperationsAddress,
                _collSurplusPoolAddress,
                _ebtcTokenAddress,
                _sortedCdpsAddress,
                _activePoolAddress,
                _priceFeedAddress,
                _collTokenAddress
            )
        {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  _liquidationLibraryAddress, _authorityAddress, _borrowerOperationsAddress, _collSurplusPool, _ebtcToken, _sortedCdps, _activePool, _priceFeed, _collateral not checked!
 217:     constructor(
             address _liquidationLibraryAddress,
             address _authorityAddress,
             address _borrowerOperationsAddress,
             address _collSurplusPool,
             address _ebtcToken,
             address _sortedCdps,
             address _activePool,
             address _priceFeed,
             address _collateral
         ) EbtcBase(_activePool, _priceFeed, _collateral) {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  _borrowerOperationsAddress, _cdpManagerAddress, _activePoolAddress, _collTokenAddress not checked!
 42:     constructor(
            address _borrowerOperationsAddress,
            address _cdpManagerAddress,
            address _activePoolAddress,
            address _collTokenAddress
        ) {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  _owner not checked!
 18:     constructor(address _owner, Authority _authority) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  _activePoolAddress, _priceFeedAddress, _collateralAddress not checked!
 52:     constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  _owner not checked!
 20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  _cdpManagerAddress, _borrowerOperationsAddress, _authorityAddress not checked!
 61:     constructor(
            address _cdpManagerAddress,
            address _borrowerOperationsAddress,
            address _authorityAddress
        ) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  _owner not checked!
 36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  _sortedCdpsAddress, _cdpManagerAddress, _collateralAddress, _activePoolAddress, _priceFeedAddress not checked!
 27:     constructor(
            address _sortedCdpsAddress,
            address _cdpManagerAddress,
            address _collateralAddress,
            address _activePoolAddress,
            address _priceFeedAddress
        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  _borrowerOperationsAddress, _activePool, _cdpManager, _ebtc, _coll, _sortedCdps not checked!
 51:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            bool _sweepToCaller
        ) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 /// @audit  _borrowerOperationsAddress, _activePool, _cdpManager, _ebtc, _coll, _sortedCdps not checked!
 41:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                false // Do not sweep to caller
            )
        {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 /// @audit  _borrowerOperationsAddress, _activePool, _cdpManager, _ebtc, _coll, _sortedCdps not checked!
 21:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        ) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 /// @audit  _borrowerOperationsAddress, _activePool, _cdpManager, _ebtc, _coll, _sortedCdps, _owner not checked!
 17:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            address _owner
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                true // Sweep to caller since this is not supposed to hold funds
            )
        {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  _borrowerOperationsAddress, _collSurplusPool, _ebtcToken, _sortedCdps, _activePool, _priceFeed, _collateral not checked!
 14:     constructor(
            address _borrowerOperationsAddress,
            address _collSurplusPool,
            address _ebtcToken,
            address _sortedCdps,
            address _activePool,
            address _priceFeed,
            address _collateral
        )
            CdpManagerStorage(
                address(0),
                address(0),
                _borrowerOperationsAddress,
                _collSurplusPool,
                _ebtcToken,
                _sortedCdps,
                _activePool,
                _priceFeed,
                _collateral
            )
        {}

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  _fallbackCallerAddress, _authorityAddress, _collEthCLFeed, _ethBtcCLFeed not checked!
 57:     constructor(
            address _fallbackCallerAddress,
            address _authorityAddress,
            address _collEthCLFeed,
            address _ethBtcCLFeed
        ) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  _owner not checked!
 44:     constructor(address _owner) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  _cdpManagerAddress, _borrowerOperationsAddress not checked!
 88:     constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {

```

### <a name="L-7"></a>[L-7] Missing checks for address(0x0) when updating address state variables

 There are 51 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 53:         borrowerOperationsAddress = _borrowerOperationsAddress;

 54:         cdpManagerAddress = _cdpManagerAddress;

 55:         collateral = ICollateralToken(_collTokenAddress);

 56:         collSurplusPoolAddress = _collSurplusAddress;

 57:         feeRecipientAddress = _feeRecipientAddress;

 398:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 117:         cdpManager = ICdpManager(_cdpManagerAddress);

 118:         collSurplusPool = ICollSurplusPool(_collSurplusPoolAddress);

 119:         sortedCdps = ISortedCdps(_sortedCdpsAddress);

 120:         ebtcToken = IEBTCToken(_ebtcTokenAddress);

 121:         feeRecipientAddress = _feeRecipientAddress;

 1148:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

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

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 19:         owner = _owner;

 53:         owner = newOwner;

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 43:         _authority = Authority(newAuthority);

 59:         _authority = Authority(newAuthority);

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

 63:         fallbackCaller = IFallbackCaller(_fallbackCallerAddress);

 69:         ETH_BTC_CL_FEED = AggregatorV3Interface(_ethBtcCLFeed);

 70:         STETH_ETH_CL_FEED = AggregatorV3Interface(_collEthCLFeed);

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 45:         owner = _owner;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 95:         cdpManager = ICdpManager(_cdpManagerAddress);

 96:         borrowerOperationsAddress = _borrowerOperationsAddress;

```

### <a name="L-8"></a>[L-8] Missing contract-existence checks before yul `call()`
Low-level calls return success if there is no code present at the specified address. In addition to the zero-address checks, add a check to verify that `extcodesize()` is non-zero.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 514:             _success := call(

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 149:                 success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

```

### <a name="L-9"></a>[L-9] Numbers downcast to `address`es may result in collisions
If a number is downcast to an `address` the upper bytes are truncated, which may mean that more than one value will map to the `address`.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/SortedCdps.sol

 125:         return address(uint160(_tmp));

```

### <a name="L-10"></a>[L-10] `receive()`/`payable fallback()` function does not authorize requests
Having no access control on the function (e.g. `require(msg.sender == address(weth))`) means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue mistakenly-sent Ether.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 160:     receive() external payable {

 164:     fallback() external payable {

```

### <a name="L-11"></a>[L-11] `require()` should be used instead of `assert()`
Prior to solidity version 0.8.0, hitting an assert consumes the remainder of the transaction’s available gas rather than returning it, as `require()`/`revert()` do. `assert()` should be avoided even past solidity version 0.8.0 as its [documentation](https://docs.soliditylang.org/en/v0.8.14/control-structures.html#panic-via-assert-and-error-via-require) states that “The assert function creates an error of type Panic(uint256). … Properly functioning code should never create a Panic, not even on invalid external input. If this happens, then there is a bug in your contract which you should fix”.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 564:         assert(toLiquidator < _totalColToSend); // Assert is correct here for Echidna

```

### <a name="L-12"></a>[L-12] `safeApprove()` is deprecated
[Deprecated](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/bfff03c0d2a59bcd8e2ead1da9aed9edf0080d05/contracts/token/ERC20/utils/SafeERC20.sol#L38-L45) in favor of `safeIncreaseAllowance()` and `safeDecreaseAllowance()`. If only setting the initial allowance to the value that means infinite, `safeIncreaseAllowance()` can be used instead. The function may currently work, but if a bug is found in this version of OpenZeppelin, and the version that you’re forced to upgrade to no longer has this function, you’ll encounter unnecessary delays in porting and testing replacement contracts.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 405:         IERC20(swapData.tokenForSwap).safeApprove(

 427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```

### <a name="L-13"></a>[L-13] Some tokens may revert when large transfers are made
Tokens such as COMP or UNI will revert when an address’ balance reaches `type(uint96).max`. Ensure that the calls below can be broken up into smaller batches if necessary.

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  flashLoan()
 274:         collateral.transfer(address(receiver), amount);

 /// @audit  flashLoan()
 286:         collateral.transfer(feeRecipientAddress, fee);

 /// @audit  sweepToken()
 381:         IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  sweepToken()
 148:         IERC20(token).safeTransfer(feeRecipientAddress, amount);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  sweepToCaller()
 224:             ebtcToken.transfer(msg.sender, ebtcBal);

 /// @audit  sweepToken()
 237:         IERC20(token).safeTransfer(msg.sender, amount);

```

### <a name="L-14"></a>[L-14] State variables not capped at reasonable values
Consider adding minimum/maximum value checks to ensure that the state variables below can never be used to excessively harm users, including via griefing.

 There are 11 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 835:         beta = _beta;

 914:         Cdps[_cdpId].debt = _debt;

 915:         Cdps[_cdpId].coll = _coll;

 917:         Cdps[_cdpId].liquidatorRewardShares = _liquidatorRewardShares;

 978:         Cdps[_cdpId].coll = _newColl;

 985:         Cdps[_cdpId].debt = _newDebt;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 581:         systemStEthFeePerUnitIndex = _newPerUnit;

 582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;

 600:         Cdps[_cdpId].coll = _newColl;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 289:         _allowances[owner][spender] = amount;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 554:         lastGoodPrice = _currentPrice;

```

### <a name="L-15"></a>[L-15] Subtraction may underflow if multiplication is too large

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 142:         @dev Prevents multi-contract reentrancy between these two contracts

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 568:         uint256 _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes);

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 61:             - That capability is public, or the user has a role that has been granted the capability to call the function

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 885:             EBTCDebtNumerator -

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 458:             ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice

 534:         uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /


```


## Non Critical Issues


### <a name="NC-1"></a>[NC-1] Large or complicated code bases should implement invariant tests
Large code bases, or code with lots of inline-assembly, complicated math, or complicated interactions between multiple contracts, should implement [invariant fuzzing tests](https://medium.com/coinmonks/smart-contract-fuzzing-d9b88e0b0a05). Invariant fuzzers such as Echidna require the test writer to come up with invariants which should not be violated under any circumstances, and the fuzzer tests various inputs and function calls to ensure that the invariants always hold. Even code with 100% code coverage can still have bugs due to the order of the operations a user performs, and invariant fuzzers, with properly and extensively-written invariants, can close this testing gap significantly.

 There is 1 instance:

 ```solidity
File: All Files

```

### <a name="NC-2"></a>[NC-2] Adding a return statement when the function defines a named return variable, is redundant
Once the return variable has been assigned (or has its default value), there is no need to explicitly return it at the end of the function, since it’s returned automatically.

 There are 9 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 233:         return singleRedemption;

 562:         return index;

 571:         return _getSystemDebt();

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 723:         return _pendingDebt;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 68:         return (activePool.getSystemCollShares());

 76:         return (activePool.getSystemDebt());

 92:         return (TCR, systemCollShares, systemDebt);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 147:         return roleNames[role];

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 859:         return newTotals;

```

### <a name="NC-3"></a>[NC-3] Missing checks for `address(0)` when assigning values to address state variables

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 57:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 121:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 19:         owner = _owner;

 53:         owner = newOwner;

```

### <a name="NC-4"></a>[NC-4] Array indices should be referenced via enums rather than via numeric literals

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 502:         require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 424:         bytes32 _firstPrev = data.nodes[_ids[0]].prevId;

```

### <a name="NC-5"></a>[NC-5] Array is `push()ed` but not `pop()ed`
Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed. Cases where there are specific potential problems will be flagged separately under a different issue.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 556:         CdpIds.push(_cdpId);

```

### <a name="NC-6"></a>[NC-6] Assembly blocks should have extensive comments
Assembly blocks take a lot more time to audit than normal Solidity code, and often have gotchas and side-effects that the Solidity versions of the same code do not. Consider adding more comments explaining what is being done in every step of the assembly code, and describe why assembly is being used instead of Solidity.

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 85:         assembly {
                ds.slot := position

 143:             assembly {
                     success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)

 148:             assembly {
                     success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

 189:         assembly {
                 calldatacopy(0, 0, calldatasize())
                 let result := delegatecall(gas(), facet, 0, calldatasize(), 0, 0)
                 returndatacopy(0, 0, returndatasize())
                 switch result

```

### <a name="NC-7"></a>[NC-7] Avoid the use of sensitive terms
Use [alternative variants](https://www.zdnet.com/article/mysql-drops-master-slave-and-blacklist-whitelist-terminology/), e.g. allowlist/denylist instead of whitelist/blacklist.

 There are 7 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 8: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 9: /// @author Modified from Dappsys (https://github.com/dapphub/ds-auth/blob/master/src/auth.sol)

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 11: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 13:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol

```


```solidity
File: packages/contracts/contracts/Governor.sol

 12: /// @author Modified from Dappsys (https://github.com/dapphub/ds-roles/blob/master/src/roles.sol)

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 30:  * https://github.com/livepeer/protocol/blob/master/contracts/libraries/SortedDoublyLL.sol

```

### <a name="NC-8"></a>[NC-8] Cast to bytes or bytes32 for clearer semantic meaning
Using a cast on a single argument, rather than abi.encodePacked() makes the intended operation more clear, leading to less reviewer confusion.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/HintHelpers.sol

 182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```

### <a name="NC-9"></a>[NC-9] Complex casting
Consider whether the number of casts is really necessary, or whether using a different type would be more appropriate. Alternatively, add comments to explain in detail why the casts are necessary, and any implicit reasons why the cast does not introduce an overflow.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/SortedCdps.sol

 114:         serialized |= bytes32(uint256(uint160(owner))) << ADDRESS_SHIFT;

 125:         return address(uint160(_tmp));

```

### <a name="NC-10"></a>[NC-10] Common functions should be refactored to a common base contract
The functions below have the same implementation as is seen in other files. The functions should be refactored into functions of a common base contract

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 /// @audit   seen in  ,packages/contracts/contracts/Interfaces/IActivePool.sol ,packages/contracts/contracts/Interfaces/IBorrowerOperations.sol
 37:     function feeRecipientAddress() external view returns (address);

```

### <a name="NC-11"></a>[NC-11] Consider adding formal verification proofs
Consider using formal verification to mathematically prove that your code does what is intended, and does not have any edge cases with unexpected behavior. The solidity compiler itself has this functionality [built in](https://docs.soliditylang.org/en/latest/smtchecker.html#smtchecker-and-formal-verification)

 There are 41 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 21: contract BorrowerOperations is

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 9: abstract contract Auth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 10: contract AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 5: library EbtcMath {

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 7: abstract contract ReentrancyGuard {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 13: contract Governor is RolesAuthority {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 11: contract HintHelpers is EbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

 26: contract LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

 40: contract LeverageMacroDelegateTarget is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 11: contract LeverageMacroFactory {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 11: contract LeverageMacroReference is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 13: contract LiquidationLibrary is CdpManagerStorage {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 25: contract SimplifiedDiamondLike {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-12"></a>[NC-12] Consider bounding input array length
The functions below take in an unbounded array, and make function calls for entries in the array. While the function will revert if it eventually runs out of gas, it may be a nicer user experience to require() that the length of the array is below some reasonable maximum, so that the user doesn’t have to use up a full transaction’s gas only to see that the transaction reverts.

 There are 10 instances:

 ```solidity
File: packages/contracts/contracts/Governor.sol

 57:             for (uint256 i = 0; i < _usrs.length; i++) {
                    address user = _usrs[i];
                    bool _canCall = doesUserHaveRole(user, role);
                    if (_canCall) {
                        usersWithRole[j] = user;

 84:             for (uint8 i = 0; i < type(uint8).max; i++) {
                    if (doesUserHaveRole(user, i)) {
                        rolesForUser[j] = i;

 107:             for (uint8 i = 0; i < type(uint8).max; i++) {
                     bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;
                     if (roleEnabled) {
                         roleIds[j] = i;

 122:         for (uint8 i = 0; i < roleIds.length; i++) {

 137:             for (uint256 i = 0; i < _sigs.length; ++i) {
                     _funcs[i] = bytes4(_sigs[i]);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 385:         for (uint256 i; i < swapLength; ) {
                 _doSwap(swapData[i]);

 438:             for (uint256 i; i < length; ++i) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 114:         for (uint256 i; i < length; ) {
                 _executeOne(ops[i]);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 432:         for (uint256 i = 0; i < _len; ++i) {
                 require(contains(_ids[i]), "SortedCdps: List does not contain the id");

 449:         for (uint i = 0; i < _len; ++i) {
                 delete data.nodes[_ids[i]];

```

### <a name="NC-13"></a>[NC-13] Consider moving msg.sender checks to a common authorization `modifier`

 There are 23 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 220:         require(

 228:         require(

 228:         require(

 236:         require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 660:         require(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 113:         require(

 120:         require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

 124:         require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 307:         require(

 315:         require(

 315:         require(

 324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 45:         require(owner() == msg.sender, "Must be owner");

 356:             require(

 362:             require(

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 52:         require(msg.sender == owner);

 67:         require(msg.sender == owner);

 77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

 111:         require(msg.sender == owner, "Must be owner");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 715:         require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

 720:         require(

 720:         require(

```

### <a name="NC-14"></a>[NC-14] Consider using delete rather than assigning zero/false to clear values
The delete keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic

 There are 6 instances:

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


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 742:         vars.backToNormalMode = false;

```

### <a name="NC-15"></a>[NC-15] Consider using descriptive constants when passing zero as a function argument
Passing zero as a function argument can sometimes result in a security issue (e.g. passing zero as the slippage parameter). Consider using a constant variable with a descriptive name, so it’s clear that the argument is intentionally being used, and for the right reasons.

 There are 15 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 209:         _adjustCdpInternal(_cdpId, 0, 0, false, _upperHint, _lowerHint, _stEthBalanceIncrease);

 225:         _adjustCdpInternal(_cdpId, _stEthBalanceDecrease, 0, false, _upperHint, _lowerHint, 0);

 241:         _adjustCdpInternal(_cdpId, 0, _debt, true, _upperHint, _lowerHint, 0);

 256:         _adjustCdpInternal(_cdpId, 0, _debt, false, _upperHint, _lowerHint, 0);

 278:         _adjustCdpInternal(
                 _cdpId,
                 _stEthBalanceDecrease,
                 _debtChange,
                 _isDebtIncrease,
                 _upperHint,
                 _lowerHint,
                 0

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 171:                 _closeCdpByRedemption(
                         _redeemColFromCdp.cdpId,
                         0,
                         newColl,
                         _liquidatorRewardShares,
                         _borrower

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 519:             _updateSystemSnapshotsExcludeCollRemainder(0);
             }

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 414:         (bool success, ) = excessivelySafeCall(
                 swapData.addressForSwap,
                 gasleft(),
                 0,
                 0,
                 swapData.calldataForSwap

 427:         IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 41:         _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 144:         (bytes32 _cdpId, ) = _cdpOfOwnerByIndex(owner, index, dummyId, 0);

 217:         (uint256 _cnt, ) = _cdpCountOf(owner, dummyId, 0);

 273:         (uint _ownedCount, ) = _cdpCountOf(owner, dummyId, 0);

 275:             (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);

 306:             return (new bytes32[](0), 0, dummyId);

```

### <a name="NC-16"></a>[NC-16] Constant redefined elsewhere
Consider defining in only one contract so that values cannot become out of sync when only one location is updated. A [cheap way](https://medium.com/coinmonks/gas-cost-of-solidity-library-functions-dbe0cedd4678) to store constants in a single location is to create an internal constant in a library. If the variable is a local cache of another contract’s value, consider making the cache variable internal or private, which will require external users to query the contract with the source of truth, so that callers don’t get out of sync.

 There are 75 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  also seen in packages/contracts/contracts/BorrowerOperations.sol,
 24:     string public constant NAME = "ActivePool";

 /// @audit  also seen in packages/contracts/contracts/CdpManagerStorage.sol,
 24:     string public constant NAME = "ActivePool";

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 24:     string public constant NAME = "ActivePool";

 /// @audit  also seen in packages/contracts/contracts/PriceFeed.sol,
 24:     string public constant NAME = "ActivePool";

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 24:     string public constant NAME = "ActivePool";

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 24:     string public constant NAME = "ActivePool";

 /// @audit  also seen in packages/contracts/contracts/CdpManagerStorage.sol,
 26:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 26:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 26:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 26:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 27:     address public immutable cdpManagerAddress;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 27:     address public immutable cdpManagerAddress;

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 34:     ICollateralToken public immutable collateral;

 /// @audit  also seen in packages/contracts/contracts/Dependencies/EbtcBase.sol,
 34:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  also seen in packages/contracts/contracts/CdpManagerStorage.sol,
 29:     string public constant NAME = "BorrowerOperations";

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 29:     string public constant NAME = "BorrowerOperations";

 /// @audit  also seen in packages/contracts/contracts/PriceFeed.sol,
 29:     string public constant NAME = "BorrowerOperations";

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 29:     string public constant NAME = "BorrowerOperations";

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 29:     string public constant NAME = "BorrowerOperations";

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 38:     bytes32 private constant _TYPE_HASH =

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 41:     string internal constant _VERSION = "1";

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 45:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 46:     uint256 private immutable _CACHED_CHAIN_ID;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 48:     bytes32 private immutable _HASHED_NAME;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 49:     bytes32 private immutable _HASHED_VERSION;

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 53:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 53:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 53:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 53:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/CdpManagerStorage.sol,
 55:     ICollSurplusPool public immutable collSurplusPool;

 /// @audit  also seen in packages/contracts/contracts/CdpManagerStorage.sol,
 59:     IEBTCToken public immutable ebtcToken;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 59:     IEBTCToken public immutable ebtcToken;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 59:     IEBTCToken public immutable ebtcToken;

 /// @audit  also seen in packages/contracts/contracts/CdpManagerStorage.sol,
 62:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 62:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 62:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 62:     ISortedCdps public immutable sortedCdps;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 122:     string public constant NAME = "CdpManager";

 /// @audit  also seen in packages/contracts/contracts/PriceFeed.sol,
 122:     string public constant NAME = "CdpManager";

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 122:     string public constant NAME = "CdpManager";

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 122:     string public constant NAME = "CdpManager";

 /// @audit  also seen in packages/contracts/contracts/CollSurplusPool.sol,
 126:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 126:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 126:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 130:     IEBTCToken public immutable override ebtcToken;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 130:     IEBTCToken public immutable override ebtcToken;

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 135:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 135:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 135:     ISortedCdps public immutable sortedCdps;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  also seen in packages/contracts/contracts/PriceFeed.sol,
 19:     string public constant NAME = "CollSurplusPool";

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 19:     string public constant NAME = "CollSurplusPool";

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 19:     string public constant NAME = "CollSurplusPool";

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 21:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 21:     address public immutable borrowerOperationsAddress;

 /// @audit  also seen in packages/contracts/contracts/EBTCToken.sol,
 22:     address public immutable cdpManagerAddress;

 /// @audit  also seen in packages/contracts/contracts/Dependencies/EbtcBase.sol,
 25:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 56:     address public immutable borrowerOperationsAddress;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 14:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 14:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 15:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 15:     ICdpManager public immutable cdpManager;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 29:     IBorrowerOperations public immutable borrowerOperations;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 30:     IActivePool public immutable activePool;

 /// @audit  also seen in packages/contracts/contracts/Dependencies/EbtcBase.sol,
 30:     IActivePool public immutable activePool;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 31:     ICdpCdps public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 32:     IEBTCToken public immutable ebtcToken;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 33:     ISortedCdps public immutable sortedCdps;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 34:     ICollateralToken public immutable stETH;

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 /// @audit  also seen in packages/contracts/contracts/Dependencies/EbtcBase.sol,
 13:     address public immutable activePool;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  also seen in packages/contracts/contracts/SortedCdps.sol,
 22:     string public constant NAME = "PriceFeed";

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 22:     string public constant NAME = "PriceFeed";

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 52:     string public constant NAME = "SortedCdps";

 /// @audit  also seen in packages/contracts/contracts/HintHelpers.sol,
 56:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroBase.sol,
 56:     ICdpManager public immutable cdpManager;

 /// @audit  also seen in packages/contracts/contracts/LeverageMacroFactory.sol,
 56:     ICdpManager public immutable cdpManager;

```

### <a name="NC-17"></a>[NC-17] Constants in comparisons should appear on the left side
Doing so will prevent [typo bugs](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html)

 There are 93 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 267:         require(amount > 0, "ActivePool: 0 Amount");

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 393:         if (!_isDebtIncrease && _debtChange > 0) {

 463:         require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

 748:         if (_collReceived != 0) {

 808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

 808:             _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,

 819:             _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,

 826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

 831:         require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

 835:         require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

 847:             _stEthBalanceDecrease == 0,

 936:         require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

 1083:         require(amount > 0, "BorrowerOperations: 0 Amount");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 159:         if (newDebt == 0) {

 332:         require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

 377:         if (_maxIterations == 0) {

 389:             currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0

 431:         require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

 434:         if (_numCdpsFullyRedeemed == 1) {

 436:         } else if (_numCdpsFullyRedeemed > 1) {

 497:         while (_cnt > 0 && _id != bytes32(0)) {

 626:         require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

 754:         require(_amount > 0, "CdpManager: Amount must be greater than zero");

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 315:         if (_debtIndexDiff > 0) {

 443:         if (totalCollateralSnapshot == 0) {

 453:             require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

 512:         if (_newIndex > _oldIndex && totalStakes > 0) {

 654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

 654:             CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,

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

 60:         if (_minutes > 525600000) {

 64:         if (_minutes == 0) {

 73:         while (n > 1) {

 74:             if (n % 2 == 0) {

 93:         if (_debt > 0) {

 109:         if (_debt > 0) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 39:         return (uint256(getUserRoles[user]) >> role) & 1 != 0;

 47:         return (uint256(getRolesWithCapability[target][functionSig]) >> role) & 1 != 0;

 124:             if (enabledFunctionSigsByTarget[target].length() == 0) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 53:         if (count > 0) {

 81:         if (count > 0) {

 99:             bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

 104:         if (count > 0) {

 108:                 bool roleEnabled = (uint256(byteMap >> i) & 1) != 0;

 135:         if (_sigs.length > 0) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 78:         if (_maxIterations == 0) {

 87:                 _maxIterations-- > 0

 171:         if (arrayLength == 0) {

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

 56:         require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

 144:         if (_liqState.partialAmount == 0) {

 158:                 liquidationValues.totalCollToSendToLiquidator == 0 &&

 159:                 liquidationValues.debtToBurn == 0

 195:             if (_outputState.totalSurplusCollShares > 0) {

 261:             if (_collSurplus > 0) {

 266:             if (_debtToRedistribute > 0) {

 336:             if (_collSurplus > 0) {

 342:             if (_debtToRedistribute > 0) {

 417:         if (newColl == 0) {

 525:         if (totalDebtToRedistribute > 0) {

 681:             _cdpArray.length != 0,

 710:         require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

 713:         if (totals.totalCollSurplus > 0) {

 863:         if (_debt == 0) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 457:         uint256 percentDeviation = maxPrice > 0

 471:         if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

 475:         if (_response.answer == 0) {

 489:             _fallbackResponse.timestamp > 0 &&

 532:         if (minPrice == 0) return false;

 695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

 695:         if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {

 776:         if (_answer <= 0) return false;

 777:         if (_roundId == 0) return false;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 56:         require(sig != 0x94b24d09);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 89:         if (_size == 0) {

 202:             if (maxNodes > 0 && i >= maxNodes) {

 259:             if (maxNodes > 0 && i >= maxNodes) {

 274:         if (_ownedCount > 0) {

 305:         if (maxArraySize == 0) {

 330:             if (maxNodes > 0 && i >= maxNodes) {

 352:         require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

 371:         require(_NICR > 0, "SortedCdps: NICR must be positive");

 422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

 508:         require(_newNICR > 0, "SortedCdps: NICR must be positive");

 537:         return data.size == 0;

```

### <a name="NC-18"></a>[NC-18] constants should be defined rather than using magic numbers
Even assembly can benefit from using readable constants instead of hex/numeric literals

 There are 31 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 826:         require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 421:                     _numCdpsFullyRedeemed = _numCdpsFullyRedeemed + 1;

 434:         if (_numCdpsFullyRedeemed == 1) {

 436:         } else if (_numCdpsFullyRedeemed > 1) {

 499:             _cnt = _cnt - 1;

 559:         index = uint128(CdpIds.length - 1);

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

 141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

 475:         require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 60:         if (_minutes > 525600000) {

 61:             _minutes = 525600000;

 74:             if (n % 2 == 0) {

 77:             } else {

 82:             }

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 113:             getRolesWithCapability[target][functionSig] |= bytes32(1 << role);

 120:             getRolesWithCapability[target][functionSig] &= ~bytes32(1 << role);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 50:                 count += 1;

 78:                 count += 1;

 101:                 count += 1;

 123:             _data |= bytes32(1 << uint256(roleIds[i]));

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 722:         try ETH_BTC_CL_FEED.getRoundData(_currentRoundEthBtcId - 1) returns (

 738:         try STETH_ETH_CL_FEED.getRoundData(_currentRoundStEthEthId - 1) returns (

 798:             ? 10 ** (_stEthEthDecimals - _ethBtcDecimals)

 799:             : 10 ** (_ethBtcDecimals - _stEthEthDecimals);

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 56:         require(sig != 0x94b24d09);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 193:                     _currentIndex = _currentIndex + 1;

 251:                 _ownedCount = _ownedCount + 1;

 404:         data.size = data.size + 1;

 422:         require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

 425:         bytes32 _lastNext = data.nodes[_ids[_len - 1]].nextId;

 489:         data.size = data.size - 1;

```

### <a name="NC-19"></a>[NC-19] Contracts should expose an interface
The `contracts` should expose an `interface` so that other projects can more easily integrate with it, without having to develop their own non-standard variants.

 There are 83 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

 390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

 404:     function setFeeBps(uint256 _newFee) external requiresAuth {

 417:     function setFlashLoansPaused(bool _paused) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

 1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

 1154:     function setFeeBps(uint256 _newFee) external requiresAuth {

 1167:     function setFlashLoansPaused(bool _paused) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {
             return _getSystemDebt();

 717:     function getDeploymentStartTime() public view returns (uint256) {
             return deploymentStartTime;

 727:     function checkPotentialRecoveryMode(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) external view returns (bool) {
             return _checkPotentialRecoveryMode(_systemCollShares, _systemDebt, _price);

 773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {
             require(

 788:     function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {
             require(

 807:     function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {
             require(

 830:     function setBeta(uint256 _beta) external requiresAuth {
             syncGlobalAccountingAndGracePeriod();

 843:     function setRedemptionsPaused(bool _paused) external requiresAuth {
             syncGlobalAccountingAndGracePeriod();

 905:     function initializeCdp(
             bytes32 _cdpId,
             uint256 _debt,
             uint256 _coll,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) external {
             _requireCallerIsBorrowerOperations();

 946:     function updateCdp(
             bytes32 _cdpId,
             address _borrower,
             uint256 _coll,
             uint256 _debt,
             uint256 _newColl,
             uint256 _newDebt
         ) external {
             _requireCallerIsBorrowerOperations();

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 32:     function notifyStartGracePeriod(uint256 tcr) external {

 42:     function notifyEndGracePeriod(uint256 tcr) external {

 111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

 504:     function syncGlobalAccounting() external {
             _requireCallerIsBorrowerOperations();

 527:     function syncGlobalAccountingAndGracePeriod() public {
             _syncGlobalAccounting(); // Apply // Could trigger RM

 552:     function calcFeeUponStakingReward(
             uint256 _newIndex,
             uint256 _prevIndex
         ) public view returns (uint256, uint256, uint256) {
             require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

 616:     function getAccumulatedFeeSplitApplied(
             bytes32 _cdpId,
             uint256 _systemStEthFeePerUnitIndex
         ) public view returns (uint256, uint256) {
             uint256 _cdpStEthFeePerUnitIndex = cdpStEthFeePerUnitIndex[_cdpId];

 673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {
             (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
             (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 719:     function getPendingRedistributedDebt(
             bytes32 _cdpId
         ) public view returns (uint256 pendingEBTCDebtReward) {
             (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);

 728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {
             return _hasRedistributedDebt(_cdpId);

 745:     function getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) public view returns (uint256 debt, uint256 coll) {
             (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(

 839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {
             (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);

 848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
             uint256 _debt = getSyncedCdpDebt(_cdpId);

 874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {
             return _checkICRAgainstTCR(icr, tcr) && _recoveryModeGracePeriodPassed();

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 42:     function setAuthority(Authority newAuthority) public virtual {

 52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 22:     function authority() public view returns (Authority) {

 26:     function authorityInitialized() public view returns (bool) {

 38:     function setAuthority(address newAuthority) public virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

 42:     function doesRoleHaveCapability(
            uint8 role,
            address target,
            bytes4 functionSig
        ) public view virtual returns (bool) {

 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

 85:     function setPublicCapability(
            address target,
            bytes4 functionSig,
            bool enabled
        ) public virtual requiresAuth {

 106:     function setRoleCapability(
             uint8 role,
             address target,
             bytes4 functionSig,
             bool enabled
         ) public virtual requiresAuth {

 133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

 147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 104:     function burn(uint256 _amount) external {

 176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 43:     function getUsersByRole(uint8 role) external view returns (address[] memory usersWithRole) {

 73:     function getRolesForUser(address user) external view returns (uint8[] memory rolesForUser) {

 96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

 120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

 131:     function getEnabledFunctionsInTarget(
             address _target
         ) public view returns (bytes4[] memory _funcs) {

 146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

 154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 48:     function getRedemptionHints(
            uint256 _EBTCamount,
            uint256 _price,
            uint256 _maxIterations
        )
            external
            view
            returns (
                bytes32 firstRedemptionHint,
                uint256 partialRedemptionHintNICR,
                uint256 truncatedEBTCamount,
                uint256 partialRedemptionNewColl
            )
        {

 164:     function getApproxHint(
             uint256 _CR,
             uint256 _numTrials,
             uint256 _inputRandomSeed
         ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

 203:     function computeNominalCR(uint256 _coll, uint256 _debt) external pure returns (uint256) {

 212:     function computeCR(
             uint256 _coll,
             uint256 _debt,
             uint256 _price
         ) external pure returns (uint256) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 39:     function owner() public virtual returns (address) {

 118:     function doOperation(
             FlashLoanType flType,
             uint256 borrowAmount,
             LeverageMacroOperation calldata operation,
             PostOperationCheck postCheckType,
             PostCheckParams calldata checkParams
         ) external {

 214:     function sweepToCaller() public {

 234:     function sweepToken(address token, uint256 amount) public {

 338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 38:     function deployNewMacro() external returns (address) {

 43:     function deployNewMacro(address _owner) public returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 50:     function resetApprovals() external {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {

 50:     function partiallyLiquidate(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) external nonReentrantSelfAndBOps {

 679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 51:     function setFallbackHandler(bytes4 sig, address handler) external {

 66:     function setAllowAnyCall(bool allowNonCallbacks) external {

 76:     function enableCallbackForCall() external {

 110:     function execute(Operation[] calldata ops) external payable {

 160:     receive() external payable {

 164:     fallback() external payable {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 105:     function toCdpId(
             address owner,
             uint256 blockHeight,
             uint256 nonce
         ) public pure returns (bytes32) {

```

### <a name="NC-20"></a>[NC-20] Contract timekeeping will break earlier than the Ethereum network itself will stop working
When a timestamp is downcast from `uint256` to `uint32`, the value will wrap in the year 2106, and the contracts will break. Other downcasts will have different endpoints. Consider whether your contract is intended to live past the size of the type being used.

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 53:             lastGracePeriodStartTimestamp = uint128(block.timestamp);

```

### <a name="NC-21"></a>[NC-21] Contracts should have full test coverage
While 100% code coverage does not guarantee that there are no bugs, it often will catch easy-to-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. Furthermore, in order to get full coverage, code authors will often have to re-organize their code so that it is more modular, so that each component can be tested separately, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.

 There is 1 instance:

 ```solidity
File: All Files

```

### <a name="NC-22"></a>[NC-22] Control structures do not follow the Solidity Style Guide
See the [control structures](https://docs.soliditylang.org/en/latest/style-guide.html#control-structures) section of the Solidity Style Guide.

 There are 251 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 46:     constructor(

 129:     function transferSystemCollSharesAndLiquidatorReward(

 261:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 21: contract BorrowerOperations is

 107:     constructor(

 168:     function openCdp(

 187:     function openCdpFor(

 203:     function addColl(

 219:     function withdrawColl(

 235:     function withdrawDebt(

 250:     function repayDebt(

 270:     function adjustCdp(

 300:     function adjustCdpWithColl(

 328:     function _adjustCdpInternal(

 439:     function _openCdp(

 608:     function getPositionManagerApproval(

 615:     function _getPositionManagerApproval(

 628:     function setPositionManagerApproval(

 635:     function _setPositionManagerApproval(

 677:     function _buildDomainSeparator(

 706:     function permitPositionManagerApproval(

 744:     function _getCollSharesChangeFromStEthChange(

 803:     function _requireSingularCollChange(

 813:     function _requireNonZeroAdjustment(

 852:     function _requireValidAdjustmentInCurrentMode(

 953:     function _requireSufficientEbtcTokenBalance(

 986:     function _getNewNominalICRFromCdpChange(

 1004:     function _getNewICRFromCdpChange(

 1030:     function _getNewCdpAmounts(

 1049:     function _getNewTCRFromCdpChange(

 1077:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 30:     constructor(

 109:     function partiallyLiquidate(

 135:     function _redeemCollateralFromCdp(

 244:     function _closeCdpByRedemption(

 272:     function _isValidFirstRedemptionHint(

 320:     function redeemCollateral(

 489:     function _getCdpIdsToRemove(

 538:     function closeCdp(

 595:     function _checkPotentialRecoveryMode(

 612:     function _updateBaseRateFromRedemption(

 661:     function getRedemptionFeeWithDecay(

 667:     function _calcRedemptionFee(

 727:     function checkPotentialRecoveryMode(

 737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(

 905:     function initializeCdp(

 946:     function updateCdp(

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 87:     function _syncGracePeriodForGivenValues(

 217:     constructor(

 304:     function _getPendingRedistributedDebt(

 489:     function _computeTCRWithGivenSystemValues(

 552:     function calcFeeUponStakingReward(

 574:     function _takeSplitAndUpdateFeePerUnit(

 592:     function _applyAccumulatedFeeSplit(

 616:     function getAccumulatedFeeSplitApplied(

 707:     function _calculateCR(

 719:     function getPendingRedistributedDebt(

 733:     function _getSyncedDebtAndCollShares(

 745:     function getSyncedDebtAndCollShares(

 761:     function _calcSyncedGlobalAccounting(

 787:     function _calcSyncedAccounting(

 822:     function _getSyncedCdpDebtAndRedistribution(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 42:     constructor(

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 83:     function _getTCRWithSystemDebtAndCollShares(

 103:     function _requireUserAcceptsFee(

 115:     function _convertDebtDenominationToBtc(

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 104:     function _computeCR(

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 42:     function doesRoleHaveCapability(

 63:     function canCall(

 85:     function setPublicCapability(

 106:     function setRoleCapability(

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 61:     constructor(

 134:     function transferFrom(

 152:     function increaseAllowance(

 160:     function decreaseAllowance(

 199:     function permit(

 235:     function _buildDomainSeparator(

```


```solidity
File: packages/contracts/contracts/Governor.sol

 131:     function getEnabledFunctionsInTarget(

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 27:     constructor(

 48:     function getRedemptionHints(

 133:     function _calculateCdpStateAfterPartialRedemption(

 164:     function getApproxHint(

 212:     function computeCR(

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 23:     function transferSystemCollShares(address _account, uint256 _amount) external;

 25:     function increaseSystemCollShares(uint256 _value) external;

 27:     function transferSystemCollSharesAndLiquidatorReward(

 33:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;

 35:     function claimFeeRecipientCollShares(uint256 _shares) external;

 37:     function feeRecipientAddress() external view returns (address);

 39:     function getFeeRecipientClaimableCollShares() external view returns (uint256);

 41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 20:     function openCdp(

 27:     function openCdpFor(

 35:     function addColl(

 42:     function withdrawColl(

 49:     function withdrawDebt(

 56:     function repayDebt(

 63:     function closeCdp(bytes32 _cdpId) external;

 65:     function adjustCdp(

 74:     function adjustCdpWithColl(

 84:     function claimSurplusCollShares() external;

 86:     function feeRecipientAddress() external view returns (address);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 11:     function getActiveCdpsCount() external view returns (uint256);

 13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

 15:     function liquidate(bytes32 _cdpId) external;

 17:     function partiallyLiquidate(

 24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;

 26:     function redeemCollateral(

 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 38:     function syncAccounting(bytes32 _cdpId) external;

 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 42:     function getRedemptionRate() external view returns (uint256);

 44:     function getRedemptionRateWithDecay() external view returns (uint256);

 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 58:     function initializeCdp(

 66:     function updateCdp(

 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

 77:     function checkRecoveryMode(uint256 _price) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 217:     function totalStakes() external view returns (uint256);

 219:     function ebtcToken() external view returns (IEBTCToken);

 221:     function systemStEthFeePerUnitIndex() external view returns (uint256);

 223:     function systemStEthFeePerUnitIndexError() external view returns (uint256);

 225:     function stEthIndex() external view returns (uint256);

 227:     function calcFeeUponStakingReward(

 232:     function syncGlobalAccounting() external; // Accrues StEthFeeSplit without influencing Grace Period

 234:     function syncGlobalAccountingAndGracePeriod() external; // Accrues StEthFeeSplit and influences Grace Period

 236:     function getAccumulatedFeeSplitApplied(

 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 259:     function getSyncedDebtAndCollShares(

 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 15:     function getTotalSurplusCollShares() external view returns (uint256);

 17:     function getSurplusCollShares(address _account) external view returns (uint256);

 19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

 21:     function claimSurplusCollShares(address _account) external;

 23:     function increaseTotalSurplusCollShares(uint256 _value) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 11:     function mint(address _account, uint256 _amount) external;

 13:     function burn(address _account, uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 15:     function onFlashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 15:     function maxFlashLoan(address token) external view returns (uint256);

 21:     function flashFee(address token, uint256 amount) external view returns (uint256);

 28:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 8:     function priceFeed() external view returns (IPriceFeed);

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

 17:     function fallbackTimeout() external view returns (uint256);

 21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 7:     function increasePermitNonce() external returns (uint256);

 9:     function nonces(address owner) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 15:     function getSystemCollShares() external view returns (uint256);

 17:     function getSystemDebt() external view returns (uint256);

 19:     function increaseSystemDebt(uint256 _amount) external;

 21:     function decreaseSystemDebt(uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 18:     function getPositionManagerApproval(

 23:     function setPositionManagerApproval(

 28:     function revokePositionManagerApproval(address _positionManager) external;

 30:     function renouncePositionManagerApproval(address _borrower) external;

 32:     function permitPositionManagerApproval(

 42:     function version() external view returns (string memory);

 44:     function permitTypeHash() external view returns (bytes32);

 46:     function domainSeparator() external view returns (bytes32);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 43:     function fetchPrice() external returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 13:     function notifyStartGracePeriod(uint256 tcr) external;

 15:     function notifyEndGracePeriod(uint256 tcr) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 14:     function remove(bytes32 _id) external;

 16:     function batchRemove(bytes32[] memory _ids) external;

 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 20:     function contains(bytes32 _id) external view returns (bool);

 22:     function isFull() external view returns (bool);

 24:     function isEmpty() external view returns (bool);

 26:     function getSize() external view returns (uint256);

 28:     function getMaxSize() external view returns (uint256);

 30:     function getFirst() external view returns (bytes32);

 32:     function getLast() external view returns (bytes32);

 34:     function getNext(bytes32 _id) external view returns (bytes32);

 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 38:     function validInsertPosition(

 44:     function findInsertPosition(

 50:     function insert(

 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 59:     function nonExistId() external view returns (bytes32);

 61:     function cdpCountOf(address owner) external view returns (uint256);

 63:     function getCdpCountOf(

 69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

 71:     function getAllCdpsOf(

 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

 51:     constructor(

 118:     function doOperation(

 344:     function onFlashLoan(

 498:     function excessivelySafeCall(

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 7:     function owner() external view returns (address);

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

 50:     function partiallyLiquidate(

 61:     function _liquidateIndividualCdpSetup(

 135:     function _liquidateIndividualCdpSetupCDP(

 186:     function _liquidateCdpInGivenMode(

 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(

 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(

 397:     function _liquidateCDPPartially(

 450:     function _partiallyReduceCdpDebt(

 466:     function _reInsertPartialLiquidation(

 503:     function _finalizeLiquidation(

 544:     function _calculatePartialLiquidationSurplusAndCap(

 570:     function _calculateFullLiquidationSurplusAndCap(

 608:     function _getLiquidationValuesNormalMode(

 642:     function _getLiquidationValuesRecoveryMode(

 733:     function _getTotalFromBatchLiquidate_RecoveryMode(

 807:     function _getTotalsFromBatchLiquidate_NormalMode(

 839:     function _addLiquidationValuesToTotals(

 896:     function _requirePartialLiqDebtSize(

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 57:     constructor(

 400:     function _chainlinkIsBroken(

 445:     function _chainlinkPriceChangeAboveMax(

 485:     function _fallbackIsFrozen(

 503:     function _bothOraclesLiveAndUnbrokenAndSimilarPrice(

 526:     function _bothOraclesSimilarPrice(

 561:     function _storeFallbackPrice(

 582:     function _getCurrentFallbackResponse()

 606:     function _getCurrentChainlinkResponse()

 687:     function _getPrevChainlinkResponse(

 788:     function _formatClAggregateAnswer(

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 105:     function toCdpId(

 140:     function cdpOfOwnerByIndex(

 155:     function cdpOfOwnerByIdx(

 173:     function _cdpOfOwnerByIndex(

 227:     function getCdpCountOf(

 237:     function _cdpCountOf(

 286:     function getAllCdpsOf(

 299:     function _getCdpsOf(

 344:     function insert(

 498:     function reInsert(

 583:     function validInsertPosition(

 591:     function _validInsertPosition(

 666:     function findInsertPosition(

 674:     function _findInsertPosition(

```

### <a name="NC-23"></a>[NC-23] Custom errors should be used rather than revert()/require()
Custom errors are available from solidity version 0.8.4. Custom errors are more easily processed in try-catch blocks, and are easier to re-use and maintain.

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

### <a name="NC-24"></a>[NC-24] else-block not required
One level of nesting can be removed by not having an else block when the if-block returns, and `if (foo) { return 1; } else { return 2; }` becomes `if (foo) { return 1; } return 2;`. A following `else if` can become `if`

 There are 15 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 666:         if (_chainID() == _CACHED_CHAIN_ID) {
                 return _CACHED_DOMAIN_SEPARATOR;
             } else {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 159:         if (newDebt == 0) {
                 // No debt remains, close Cdp
                 // No debt left in the Cdp, therefore the cdp gets closed
                 {
                     address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId);
                     uint256 _liquidatorRewardShares = Cdps[_redeemColFromCdp.cdpId]
                         .liquidatorRewardShares;
     
                     singleRedemption.collSurplus = newColl; // Collateral surplus processed on full redemption
                     singleRedemption.liquidatorRewardShares = _liquidatorRewardShares;
                     singleRedemption.fullRedemption = true;
     
                     _closeCdpByRedemption(
                         _redeemColFromCdp.cdpId,
                         0,
                         newColl,
                         _liquidatorRewardShares,
                         _borrower
                     );
     
                     emit CdpUpdated(
                         _redeemColFromCdp.cdpId,
                         _borrower,
                         msg.sender,
                         _oldDebtAndColl.debt,
                         _oldDebtAndColl.collShares,
                         0,
                         0,
                         0,
                         CdpOperation.redeemCollateral
                     );
                 }
             } else {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 315:         if (_debtIndexDiff > 0) {
                 pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;
             } else {

 636:         if (_scaledCdpColl > _feeSplitDistributed) {
                 return (
                     _feeSplitDistributed,
                     (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
                 );
             } else {
                 // extreme unlikely case to skip fee split on this CDP to avoid revert

 765:         if (_newIndex > _oldIndex && totalStakes > 0) {
                 /// @audit-ok We don't take the fee if we had a negative rebase
                 (
                     uint256 _feeTaken,
                     uint256 _deltaFeePerUnit,
                     uint256 _perUnitError
                 ) = calcFeeUponStakingReward(_newIndex, _oldIndex);
     
                 // calculate new split per stake unit
                 uint256 _newPerUnit = systemStEthFeePerUnitIndex + _deltaFeePerUnit;
                 return (_feeTaken, _newPerUnit, _perUnitError);
             } else {
                 return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 93:         if (_debt > 0) {
                return (_collShares * NICR_PRECISION) / _debt;
            }
            // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
            else {
                // if (_debt == 0)

 109:         if (_debt > 0) {
                 uint256 newCollRatio = (_stEthBalance * _price) / _debt;
     
                 return newCollRatio;
             }
             // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
             else {
                 // if (_debt == 0)

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 72:         } else if (flag == CapabilityFlag.Public) {
                return true;
            } else {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 183:         if (_chainID() == _CACHED_CHAIN_ID) {
                 return _CACHED_DOMAIN_SEPARATOR;
             } else {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 190:         if (_liqState.recoveryModeAtStart) {
                 LiquidationRecoveryModeLocals
                     memory _outputState = _liquidateIndividualCdpSetupCDPInRecoveryMode(_recoveryState);
     
                 // housekeeping leftover collateral for liquidated CDP
                 if (_outputState.totalSurplusCollShares > 0) {
                     activePool.transferSystemCollShares(
                         address(collSurplusPool),
                         _outputState.totalSurplusCollShares
                     );
                 }
     
                 return (
                     _outputState.totalDebtToBurn,
                     _outputState.totalCollSharesToSend,
                     _outputState.totalDebtToRedistribute,
                     _outputState.totalLiquidatorRewardCollShares,
                     _outputState.totalSurplusCollShares
                 );
             } else {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 666:         if (
                 _checkHealthyCLResponse(chainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
                 _checkHealthyCLResponse(chainlinkResponse.roundStEthEthId, stEthEthAnswer)
             ) {
                 chainlinkResponse.answer = _formatClAggregateAnswer(
                     ethBtcAnswer,
                     stEthEthAnswer,
                     ethBtcDecimals,
                     stEthEthDecimals
                 );
             } else {

 754:         if (
                 _checkHealthyCLResponse(prevChainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
                 _checkHealthyCLResponse(prevChainlinkResponse.roundStEthEthId, stEthEthAnswer)
             ) {
                 prevChainlinkResponse.answer = _formatClAggregateAnswer(
                     ethBtcAnswer,
                     stEthEthAnswer,
                     ethBtcDecimals,
                     stEthEthDecimals
                 );
             } else {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 189:                 if (_currentIndex == index) {
                         return (_currentCdpId, true);
                     } else {

 602:         } else if (_nextId == dummyId) {
                 // `(_prevId, null)` is a valid insert position if `_prevId` is the tail of the list
                 return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);
             } else {

 702:         } else if (nextId == dummyId) {
                 // No `nextId` for hint - descend list starting from `prevId`
                 return _descendList(_NICR, prevId);
             } else {

```

### <a name="NC-25"></a>[NC-25] Empty bytes check is missing
'When developing smart contracts in Solidity, it's crucial to validate the inputs of your functions. This includes ensuring that the bytes parameters are not empty, especially when they represent crucial data such as addresses, identifiers, or raw data that the contract needs to process. Missing empty bytes checks can lead to unexpected behaviour in your contract.For instance, certain operations might fail, produce incorrect results, or consume unnecessary gas when performed with empty bytes.Moreover, missing input validation can potentially expose your contract to malicious activity, including exploitation of unhandled edge cases. To mitigate these issues, always validate that bytes parameters are not empty when the logic of your contract requires it.'

 There are 144 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  data is not checked
 261:     function flashLoan(
             IERC3156FlashBorrower receiver,
             address token,
             uint256 amount,
             bytes calldata data
         ) external override returns (bool) {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  _upperHint, _lowerHint are not checked
 168:     function openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance
         ) external override nonReentrantSelfAndCdpM returns (bytes32) {

 /// @audit  _upperHint, _lowerHint are not checked
 187:     function openCdpFor(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) external override nonReentrantSelfAndCdpM returns (bytes32) {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 203:     function addColl(
             bytes32 _cdpId,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) external override nonReentrantSelfAndCdpM {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 219:     function withdrawColl(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 235:     function withdrawDebt(
             bytes32 _cdpId,
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 250:     function repayDebt(
             bytes32 _cdpId,
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 270:     function adjustCdp(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 300:     function adjustCdpWithColl(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) external override nonReentrantSelfAndCdpM {

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 328:     function _adjustCdpInternal(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) internal {

 /// @audit  _upperHint, _lowerHint are not checked
 439:     function _openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) internal returns (bytes32) {

 /// @audit  _cdpId is not checked
 553:     function closeCdp(bytes32 _cdpId) external override {

 /// @audit  typeHash, name, version are not checked
 677:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 /// @audit  r, s are not checked
 706:     function permitPositionManagerApproval(
             address _borrower,
             address _positionManager,
             PositionManagerApproval _approval,
             uint256 _deadline,
             uint8 v,
             bytes32 r,
             bytes32 s
         ) external override {

 /// @audit  _cdpId is not checked
 824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {

 /// @audit  _cdpId is not checked
 829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

 /// @audit  data is not checked
 1077:     function flashLoan(
              IERC3156FlashBorrower receiver,
              address token,
              uint256 amount,
              bytes calldata data
          ) external override returns (bool) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  _cdpId is not checked
 99:     function liquidate(bytes32 _cdpId) external override {

 /// @audit  _cdpId, _upperPartialHint, _lowerPartialHint are not checked
 109:     function partiallyLiquidate(
             bytes32 _cdpId,
             uint256 _partialAmount,
             bytes32 _upperPartialHint,
             bytes32 _lowerPartialHint
         ) external override {

 /// @audit  _cdpId is not checked
 244:     function _closeCdpByRedemption(
             bytes32 _cdpId,
             uint256 _EBTC,
             uint256 _collSurplus,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) internal {

 /// @audit  _firstRedemptionHint, _upperPartialRedemptionHint, _lowerPartialRedemptionHint are not checked
 320:     function redeemCollateral(
             uint256 _debt,
             bytes32 _firstRedemptionHint,
             bytes32 _upperPartialRedemptionHint,
             bytes32 _lowerPartialRedemptionHint,
             uint256 _partialRedemptionHintNICR,
             uint256 _maxIterations,
             uint256 _maxFeePercentage
         ) external override nonReentrantSelfAndBOps {
             RedemptionTotals memory totals;

 /// @audit  _start, _end are not checked
 489:     function _getCdpIdsToRemove(
             bytes32 _start,
             uint256 _total,
             bytes32 _end
         ) internal view returns (bytes32[] memory) {
             uint256 _cnt = _total;

 /// @audit  _cdpId is not checked
 514:     function syncAccounting(bytes32 _cdpId) external virtual override {
             /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

 /// @audit  _cdpId is not checked
 523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {
             _requireCallerIsBorrowerOperations();

 /// @audit  _cdpId is not checked
 538:     function closeCdp(
             bytes32 _cdpId,
             address _borrower,
             uint256 _debt,
             uint256 _coll
         ) external override {
             _requireCallerIsBorrowerOperations();

 /// @audit  _cdpId is not checked
 550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
             /* Max array size is 2**128 - 1, i.e. ~3e30 cdps. No risk of overflow, since cdps have minimum EBTC

 /// @audit  _cdpId is not checked
 856:     function getCdpStatus(bytes32 _cdpId) external view override returns (uint256) {
             return uint256(Cdps[_cdpId].status);

 /// @audit  _cdpId is not checked
 863:     function getCdpStake(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].stake;

 /// @audit  _cdpId is not checked
 871:     function getCdpDebt(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].debt;

 /// @audit  _cdpId is not checked
 879:     function getCdpCollShares(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].coll;

 /// @audit  _cdpId is not checked
 891:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].liquidatorRewardShares;

 /// @audit  _cdpId is not checked
 905:     function initializeCdp(
             bytes32 _cdpId,
             uint256 _debt,
             uint256 _coll,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) external {
             _requireCallerIsBorrowerOperations();

 /// @audit  _cdpId is not checked
 946:     function updateCdp(
             bytes32 _cdpId,
             address _borrower,
             uint256 _coll,
             uint256 _debt,
             uint256 _newColl,
             uint256 _newDebt
         ) external {
             _requireCallerIsBorrowerOperations();

 /// @audit  _cdpId is not checked
 977:     function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {
             Cdps[_cdpId].coll = _newColl;

 /// @audit  _cdpId is not checked
 984:     function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {
             Cdps[_cdpId].debt = _newDebt;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  _cdpId is not checked
 255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {

 /// @audit  _cdpId is not checked
 260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

 /// @audit  _cdpId is not checked
 304:     function _getPendingRedistributedDebt(
             bytes32 _cdpId
         ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

 /// @audit  _cdpId is not checked
 327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

 /// @audit  _cdpId is not checked
 336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

 /// @audit  _cdpId is not checked
 344:     function _syncAccounting(bytes32 _cdpId) internal {

 /// @audit  _cdpId is not checked
 410:     function _removeStake(bytes32 _cdpId) internal {

 /// @audit  _cdpId is not checked
 419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

 /// @audit  _cdpId is not checked
 431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

 /// @audit  _cdpId is not checked
 463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
             Status cdpStatus = Cdps[_cdpId].status;

 /// @audit  _cdpId is not checked
 592:     function _applyAccumulatedFeeSplit(
             bytes32 _cdpId,
             uint256 _newColl,
             uint256 _feeSplitDistributed,
             uint256 _oldPerUnitCdp,
             uint256 _systemStEthFeePerUnitIndex
         ) internal {
             // apply split fee to given CDP

 /// @audit  _cdpId is not checked
 616:     function getAccumulatedFeeSplitApplied(
             bytes32 _cdpId,
             uint256 _systemStEthFeePerUnitIndex
         ) public view returns (uint256, uint256) {
             uint256 _cdpStEthFeePerUnitIndex = cdpStEthFeePerUnitIndex[_cdpId];

 /// @audit  _cdpId is not checked
 648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {
             require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

 /// @audit  _cdpId is not checked
 673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {
             (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  _cdpId is not checked
 684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 /// @audit  _cdpId is not checked
 701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
             (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  _cdpId is not checked
 719:     function getPendingRedistributedDebt(
             bytes32 _cdpId
         ) public view returns (uint256 pendingEBTCDebtReward) {
             (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);

 /// @audit  _cdpId is not checked
 728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {
             return _hasRedistributedDebt(_cdpId);

 /// @audit  _cdpId is not checked
 733:     function _getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) internal view returns (CdpDebtAndCollShares memory) {
             (uint256 entireDebt, uint256 entireColl) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  _cdpId is not checked
 745:     function getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) public view returns (uint256 debt, uint256 coll) {
             (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(

 /// @audit  _cdpId is not checked
 787:     function _calcSyncedAccounting(
             bytes32 _cdpId,
             uint256 _cdpPerUnitIdx,
             uint256 _systemStEthFeePerUnitIndex
         ) internal view returns (uint256, uint256, uint256, uint256, uint256) {
             uint256 _feeSplitApplied;

 /// @audit  _cdpId is not checked
 822:     function _getSyncedCdpDebtAndRedistribution(
             bytes32 _cdpId
         ) internal view returns (uint256, uint256, uint256) {
             (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(

 /// @audit  _cdpId is not checked
 839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {
             (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);

 /// @audit  _cdpId is not checked
 848:     function getSyncedCdpCollShares(bytes32 _cdpId) public view returns (uint256) {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 /// @audit  _cdpId is not checked
 864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
             uint256 _debt = getSyncedCdpDebt(_cdpId);

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  functionSig is not checked
 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 /// @audit  functionSig is not checked
 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  functionSig is not checked
 42:     function doesRoleHaveCapability(
            uint8 role,
            address target,
            bytes4 functionSig
        ) public view virtual returns (bool) {

 /// @audit  functionSig is not checked
 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

 /// @audit  functionSig is not checked
 63:     function canCall(
            address user,
            address target,
            bytes4 functionSig
        ) public view virtual override returns (bool) {

 /// @audit  functionSig is not checked
 85:     function setPublicCapability(
            address target,
            bytes4 functionSig,
            bool enabled
        ) public virtual requiresAuth {

 /// @audit  functionSig is not checked
 106:     function setRoleCapability(
             uint8 role,
             address target,
             bytes4 functionSig,
             bool enabled
         ) public virtual requiresAuth {

 /// @audit  functionSig is not checked
 133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  r, s are not checked
 199:     function permit(
             address owner,
             address spender,
             uint256 amount,
             uint256 deadline,
             uint8 v,
             bytes32 r,
             bytes32 s
         ) external override {

 /// @audit  typeHash, name, version are not checked
 235:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 /// @audit  _upperHint, _lowerHint are not checked
 20:     function openCdp(

 /// @audit  _upperHint, _lowerHint are not checked
 27:     function openCdpFor(

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 35:     function addColl(

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 42:     function withdrawColl(

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 49:     function withdrawDebt(

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 56:     function repayDebt(

 /// @audit  _cdpId is not checked
 63:     function closeCdp(bytes32 _cdpId) external;

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 65:     function adjustCdp(

 /// @audit  _cdpId, _upperHint, _lowerHint are not checked
 74:     function adjustCdpWithColl(

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 /// @audit  _cdpId is not checked
 15:     function liquidate(bytes32 _cdpId) external;

 /// @audit  _cdpId, _upperPartialHint, _lowerPartialHint are not checked
 17:     function partiallyLiquidate(

 /// @audit  _firstRedemptionHint, _upperPartialRedemptionHint, _lowerPartialRedemptionHint are not checked
 26:     function redeemCollateral(

 /// @audit  _cdpId is not checked
 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 /// @audit  _cdpId is not checked
 38:     function syncAccounting(bytes32 _cdpId) external;

 /// @audit  _cdpId is not checked
 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 /// @audit  _cdpId is not checked
 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 /// @audit  _cdpId is not checked
 58:     function initializeCdp(

 /// @audit  _cdpId is not checked
 66:     function updateCdp(

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  _cdpId is not checked
 236:     function getAccumulatedFeeSplitApplied(

 /// @audit  _cdpId is not checked
 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  _cdpId is not checked
 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  _cdpId is not checked
 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId is not checked
 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 /// @audit  _cdpId is not checked
 259:     function getSyncedDebtAndCollShares(

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 /// @audit  data is not checked
 15:     function onFlashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 /// @audit  data is not checked
 28:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 /// @audit  r, s are not checked
 32:     function permitPositionManagerApproval(

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 /// @audit  _id is not checked
 14:     function remove(bytes32 _id) external;

 /// @audit  _id, _prevId, _nextId are not checked
 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 /// @audit  _id is not checked
 20:     function contains(bytes32 _id) external view returns (bool);

 /// @audit  _id is not checked
 34:     function getNext(bytes32 _id) external view returns (bytes32);

 /// @audit  _id is not checked
 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 /// @audit  _prevId, _nextId are not checked
 38:     function validInsertPosition(

 /// @audit  _prevId, _nextId are not checked
 44:     function findInsertPosition(

 /// @audit  _prevId, _nextId are not checked
 50:     function insert(

 /// @audit  _id is not checked
 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 /// @audit  startNodeId is not checked
 63:     function getCdpCountOf(

 /// @audit  startNodeId is not checked
 71:     function getAllCdpsOf(

 /// @audit  startNodeId is not checked
 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit   is not checked
 15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

 /// @audit  data is not checked
 338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

 /// @audit  data is not checked
 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

 /// @audit  data is not checked
 460:     function _openCdpCallback(bytes memory data) internal {

 /// @audit  data is not checked
 474:     function _closeCdpCallback(bytes memory data) internal {

 /// @audit  data is not checked
 482:     function _adjustCdpCallback(bytes memory data) internal {

 /// @audit  _calldata is not checked
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

 /// @audit  _cdpId is not checked
 40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {

 /// @audit  _cdpId, _upperPartialHint, _lowerPartialHint are not checked
 50:     function partiallyLiquidate(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) external nonReentrantSelfAndBOps {

 /// @audit  _cdpId, _upperPartialHint, _lowerPartialHint are not checked
 61:     function _liquidateIndividualCdpSetup(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) internal {

 /// @audit  _cdpId is not checked
 384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

 /// @audit  _cdpId is not checked
 450:     function _partiallyReduceCdpDebt(
             bytes32 _cdpId,
             uint256 _partialDebt,
             uint256 _partialColl
         ) internal {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  cdpId is not checked
 123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {

 /// @audit  startNodeId is not checked
 155:     function cdpOfOwnerByIdx(
             address owner,
             uint256 index,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32, bool) {

 /// @audit  startNodeId is not checked
 227:     function getCdpCountOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (uint256, bytes32) {

 /// @audit  startNodeId is not checked
 286:     function getAllCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32[] memory, uint256, bytes32) {

 /// @audit  _prevId, _nextId are not checked
 344:     function insert(
             address owner,
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external override returns (bytes32) {

 /// @audit  _prevId, _nextId are not checked
 363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

 /// @audit  _id is not checked
 410:     function remove(bytes32 _id) external override {

 /// @audit  _id, _prevId, _nextId are not checked
 498:     function reInsert(
             bytes32 _id,
             uint256 _newNICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external override {

 /// @audit  _id is not checked
 567:     function getNext(bytes32 _id) external view override returns (bytes32) {

 /// @audit  _id is not checked
 574:     function getPrev(bytes32 _id) external view override returns (bytes32) {

 /// @audit  _prevId, _nextId are not checked
 583:     function validInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bool) {

 /// @audit  _startId is not checked
 619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

 /// @audit  _startId is not checked
 642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

 /// @audit  _prevId, _nextId are not checked
 666:     function findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bytes32, bytes32) {

 /// @audit  _prevId, _nextId are not checked
 674:     function _findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bytes32, bytes32) {

```

### <a name="NC-26"></a>[NC-26] Empty function body
Consider adding a comment about why the function body is empty.

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

```


```solidity
File: packages/contracts/contracts/Governor.sol

 36:     constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 14:     constructor(
            address _borrowerOperationsAddress,
            address _collSurplusPool,
            address _ebtcToken,
            address _sortedCdps,
            address _activePool,
            address _priceFeed,
            address _collateral
        )
            CdpManagerStorage(
                address(0),
                address(0),
                _borrowerOperationsAddress,
                _collSurplusPool,
                _ebtcToken,
                _sortedCdps,
                _activePool,
                _priceFeed,
                _collateral
            )
        {}

```

### <a name="NC-27"></a>[NC-27] Error messages should be descriptive, rather than cryptic
The error message should clearly state how/why something is an error, not just that a specific error state was reached; someone shouldn’t have to read the code in order to see how to resolve the problem

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 104:         require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 99:         require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

```

### <a name="NC-28"></a>[NC-28] Event is not properly indexed
Index event fields make the field more quickly accessible to off-chain tools that parse events. This is especially useful when it comes to filtering based on an address. However, note that each index field costs extra gas during emission, so it’s not necessarily best to index the maximum allowed per event (three fields). Where applicable, each `event` should use three `indexed` fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three applicable fields, all of the applicable fields should be indexed.

 There are 8 instances:

 ```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 23:     event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);

 42:     event CdpLiquidated(
            bytes32 indexed _cdpId,
            address indexed _borrower,
            uint _debt,
            uint _collShares,
            CdpOperation _operation,
            address indexed _liquidator,
            uint _premiumToLiquidator

 51:     event CdpPartiallyLiquidated(
            bytes32 indexed _cdpId,
            address indexed _borrower,
            uint256 _debt,
            uint256 _collShares,
            CdpOperation operation,
            address indexed _liquidator,
            uint _premiumToLiquidator

 65:     event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);

 66:     event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);

 69:     event CdpFeeSplitApplied(
            bytes32 _cdpId,
            uint256 _oldPerUnitCdp,
            uint256 _newPerUnitCdp,
            uint256 _collReduced,
            uint256 _collLeft

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 9:     event NodeAdded(bytes32 _id, uint _NICR);

 10:     event NodeRemoved(bytes32 _id);

```

### <a name="NC-29"></a>[NC-29] Events are missing sender information
When an action is triggered based on a user’s action, not being able to filter based on who triggered the action makes event processing a lot more cumbersome. Including the `msg.sender` the events of these types of action will make events much more useful to end users, especially when `msg.sender` is not `tx.origin`.

 There are 65 instances:

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

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

 641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

 1105:         emit FlashLoanSuccess(address(receiver), token, amount, fee);

 1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

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

 542:             emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);

 587:         emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);

 602:         emit CdpFeeSplitApplied(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 83:         emit SurplusCollSharesUpdated(_account, newAmount);

 95:         emit SurplusCollSharesUpdated(_account, 0);

 104:         emit CollSharesTransferred(_account, claimableColl);

 150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 62:         emit AuthorityUpdated(address(this), Authority(newAuthority));

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 101:         emit PublicCapabilityUpdated(target, functionSig, enabled);

 129:         emit RoleCapabilityUpdated(role, target, functionSig, enabled);

 140:         emit CapabilityBurned(target, functionSig);

 163:         emit UserRoleUpdated(user, role, enabled);

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 267:         emit Transfer(address(0), account, amount);

 282:         emit Transfer(account, address(0), amount);

 290:         emit Approval(owner, spender, amount);

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

 516:         emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);

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

### <a name="NC-30"></a>[NC-30] Events may be emitted out of order due to reentrancy
Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls

 There are 5 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  syncGlobalAccountingAndGracePeriod() prior to emission
 383:         emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);

 /// @audit  syncGlobalAccountingAndGracePeriod() prior to emission
 399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

 /// @audit  syncGlobalAccountingAndGracePeriod() prior to emission
 412:         emit FlashFeeSet(msg.sender, _oldFee, _newFee);

 /// @audit  syncGlobalAccountingAndGracePeriod() prior to emission
 421:         emit FlashLoansPaused(msg.sender, _paused);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  balanceOf() prior to emission
 150:         emit SweepTokenSuccess(token, amount, feeRecipientAddress);

```

### <a name="NC-31"></a>[NC-31] Events should use parameters to convey information
For example, rather than using `event Paused()` and `event Unpaused()`, use `event PauseState(address indexed whoChangedIt, bool wasPaused, bool isNowPaused)`

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 9:     event GracePeriodStart();

 10:     event GracePeriodEnd();

```

### <a name="NC-32"></a>[NC-32] Events that mark critical parameter changes should contain both the old and the new value
This should especially be done if the new value is not required to be different from the old value.

 There are 18 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  ()
 65:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

 /// @audit  allocateSystemCollSharesToFeeRecipient()
 174:         emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);

 /// @audit  claimFeeRecipientCollShares()
 360:         emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);

 /// @audit  setFeeRecipientAddress()
 399:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  ()
 136:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

 /// @audit  _setPositionManagerApproval()
 641:         emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);

 /// @audit  setFeeRecipientAddress()
 1149:         emit FeeRecipientAddressChanged(_feeRecipientAddress);

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  setGracePeriod()
 119:         emit GracePeriodDurationSet(_gracePeriod);

 /// @audit  _updateRedistributedDebtIndex()
 340:         emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  increaseSurplusCollShares()
 83:         emit SurplusCollSharesUpdated(_account, newAmount);

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  ()
 22:         emit OwnershipTransferred(msg.sender, _owner);

 /// @audit  ()
 23:         emit AuthorityUpdated(msg.sender, _authority);

 /// @audit  setAuthority()
 49:         emit AuthorityUpdated(msg.sender, newAuthority);

 /// @audit  transferOwnership()
 55:         emit OwnershipTransferred(msg.sender, newOwner);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  setRoleName()
 157:         emit RoleNameSet(role, roleName);

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  _changeStatus()
 548:         emit PriceFeedStatusChanged(_status);

 /// @audit  _storePrice()
 555:         emit LastGoodPriceUpdated(_currentPrice);

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  _insert()
 405:         emit NodeAdded(_id, _NICR);

```

### <a name="NC-33"></a>[NC-33] Expressions for constant values should use immutable rather than constant
While it does not save gas for some simple binary expressions because the compiler knows that developers often make this mistake, it’s still best to use the right tool for the task at hand. There is a difference between `constant` variables and `immutable` variables, and they should each be used in their appropriate contexts. `constants` should be used for literal values written into the code, and `immutable` variables should be used for expressions, or values calculated in, or passed into the constructor.

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

### <a name="NC-34"></a>[NC-34] High cyclomatic complexity
Consider breaking down these blocks into more manageable units, by splitting things into utility functions, by reducing nesting, and by using early returns.

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 320:     function redeemCollateral(
             uint256 _debt,
             bytes32 _firstRedemptionHint,
             bytes32 _upperPartialRedemptionHint,
             bytes32 _lowerPartialRedemptionHint,
             uint256 _partialRedemptionHintNICR,
             uint256 _maxIterations,
             uint256 _maxFeePercentage
         ) external override nonReentrantSelfAndBOps {
             RedemptionTotals memory totals;
     
             // early check to ensure redemption is not paused
             require(redemptionsPaused == false, "CdpManager: Redemptions Paused");
     
             _requireValidMaxFeePercentage(_maxFeePercentage);
     
             _syncGlobalAccounting(); // Apply state, we will syncGracePeriod at end of function
     
             totals.price = priceFeed.fetchPrice();
             {
                 (
                     uint256 tcrAtStart,
                     uint256 systemCollSharesAtStart,
                     uint256 systemDebtAtStart
                 ) = _getTCRWithSystemDebtAndCollShares(totals.price);
                 totals.tcrAtStart = tcrAtStart;
                 totals.systemCollSharesAtStart = systemCollSharesAtStart;
                 totals.systemDebtAtStart = systemDebtAtStart;
             }
     
             _requireTCRisNotBelowMCR(totals.price, totals.tcrAtStart);
             _requireAmountGreaterThanZero(_debt);
     
             _requireEbtcBalanceCoversRedemptionAndWithinSupply(
                 msg.sender,
                 _debt,
                 totals.systemDebtAtStart
             );
     
             totals.remainingDebtToRedeem = _debt;
             address currentBorrower;
             bytes32 _cId = _firstRedemptionHint;
     
             if (_isValidFirstRedemptionHint(_firstRedemptionHint, totals.price)) {
                 currentBorrower = sortedCdps.getOwnerAddress(_firstRedemptionHint);
             } else {
                 _cId = sortedCdps.getLast();
                 currentBorrower = sortedCdps.getOwnerAddress(_cId);
                 // Find the first cdp with ICR >= MCR
                 while (currentBorrower != address(0) && getSyncedICR(_cId, totals.price) < MCR) {
                     _cId = sortedCdps.getPrev(_cId);
                     currentBorrower = sortedCdps.getOwnerAddress(_cId);
                 }
             }
     
             // Loop through the Cdps starting from the one with lowest collateral
             // ratio until _amount of EBTC is exchanged for collateral
             if (_maxIterations == 0) {
                 _maxIterations = type(uint256).max;
             }
     
             bytes32 _firstRedeemed = _cId;
             bytes32 _lastRedeemed = _cId;
             uint256 _numCdpsFullyRedeemed;
     
             /**
                 Core Redemption Loop
             */
             while (
                 currentBorrower != address(0) && totals.remainingDebtToRedeem > 0 && _maxIterations > 0
             ) {
                 // Save the address of the Cdp preceding the current one, before potentially modifying the list
                 {
                     _syncAccounting(_cId); /// @audit This happens even if the re-insertion doesn't
     
                     SingleRedemptionInputs memory _redeemColFromCdp = SingleRedemptionInputs(
                         _cId,
                         totals.remainingDebtToRedeem,
                         totals.price,
                         _upperPartialRedemptionHint,
                         _lowerPartialRedemptionHint,
                         _partialRedemptionHintNICR
                     );
                     SingleRedemptionValues memory singleRedemption = _redeemCollateralFromCdp(
                         _redeemColFromCdp
                     );
                     // Partial redemption was cancelled (out-of-date hint, or new net debt < minimum),
                     // therefore we could not redeem from the last Cdp
                     if (singleRedemption.cancelledPartial) break;
     
                     totals.debtToRedeem = totals.debtToRedeem + singleRedemption.debtToRedeem;
                     totals.collSharesDrawn = totals.collSharesDrawn + singleRedemption.collSharesDrawn;
                     totals.remainingDebtToRedeem =
                         totals.remainingDebtToRedeem -
                         singleRedemption.debtToRedeem;
                     totals.totalCollSharesSurplus =
                         totals.totalCollSharesSurplus +
                         singleRedemption.collSurplus;
     
                     if (singleRedemption.fullRedemption) {
                         _lastRedeemed = _cId;
                         _numCdpsFullyRedeemed = _numCdpsFullyRedeemed + 1;
                     }
     
                     bytes32 _nextId = sortedCdps.getPrev(_cId);
                     address nextUserToCheck = sortedCdps.getOwnerAddress(_nextId);
                     currentBorrower = nextUserToCheck;
                     _cId = _nextId;
                 }
                 _maxIterations--;
             }
             require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");
     
             // remove from sortedCdps
             if (_numCdpsFullyRedeemed == 1) {
                 sortedCdps.remove(_firstRedeemed);
             } else if (_numCdpsFullyRedeemed > 1) {
                 bytes32[] memory _toRemoveIds = _getCdpIdsToRemove(
                     _lastRedeemed,
                     _numCdpsFullyRedeemed,
                     _firstRedeemed
                 );
                 sortedCdps.batchRemove(_toRemoveIds);
             }
     
             // Decay the baseRate due to time passed, and then increase it according to the size of this redemption.
             // Use the saved total EBTC supply value, from before it was reduced by the redemption.
             _updateBaseRateFromRedemption(
                 totals.collSharesDrawn,
                 totals.price,
                 totals.systemDebtAtStart
             );
     
             // Calculate the ETH fee
             totals.feeCollShares = _getRedemptionFee(totals.collSharesDrawn);
     
             _requireUserAcceptsFee(totals.feeCollShares, totals.collSharesDrawn, _maxFeePercentage);
     
             totals.collSharesToRedeemer = totals.collSharesDrawn - totals.feeCollShares;
     
             _syncGracePeriodForGivenValues(
                 totals.systemCollSharesAtStart - totals.collSharesDrawn - totals.totalCollSharesSurplus,
                 totals.systemDebtAtStart - totals.debtToRedeem,
                 totals.price
             );
     
             emit Redemption(
                 _debt,
                 totals.debtToRedeem,
                 totals.collSharesDrawn,
                 totals.feeCollShares,
                 msg.sender
             );
     
             // Burn the total eBTC that is redeemed
             ebtcToken.burn(msg.sender, totals.debtToRedeem);
     
             // Update Active Pool eBTC debt internal accounting
             activePool.decreaseSystemDebt(totals.debtToRedeem);
     
             // Allocate the stETH fee to the FeeRecipient
             activePool.allocateSystemCollSharesToFeeRecipient(totals.feeCollShares);
     
             // CEI: Send the stETH drawn to the redeemer
             activePool.transferSystemCollShares(msg.sender, totals.collSharesToRedeemer);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 118:     function doOperation(
             FlashLoanType flType,
             uint256 borrowAmount,
             LeverageMacroOperation calldata operation,
             PostOperationCheck postCheckType,
             PostCheckParams calldata checkParams
         ) external {
             _assertOwner();
     
             // Call FL Here, then the stuff below needs to happen inside the FL
             if (operation.amountToTransferIn > 0) {
                 IERC20(operation.tokenToTransferIn).safeTransferFrom(
                     msg.sender,
                     address(this),
                     operation.amountToTransferIn
                 );
             }
     
             /**
              * SETUP FOR POST CALL CHECK
              */
             uint256 initialCdpIndex;
             if (postCheckType == PostOperationCheck.openCdp) {
                 // How to get owner
                 // sortedCdps.existCdpOwners(_cdpId);
                 initialCdpIndex = sortedCdps.cdpCountOf(address(this));
             }
     
             // Take eBTC or stETH FlashLoan
             if (flType == FlashLoanType.eBTC) {
                 IERC3156FlashLender(address(borrowerOperations)).flashLoan(
                     IERC3156FlashBorrower(address(this)),
                     address(ebtcToken),
                     borrowAmount,
                     abi.encode(operation)
                 );
             } else if (flType == FlashLoanType.stETH) {
                 IERC3156FlashLender(address(activePool)).flashLoan(
                     IERC3156FlashBorrower(address(this)),
                     address(stETH),
                     borrowAmount,
                     abi.encode(operation)
                 );
             } else {
                 // No leverage, just do the operation
                 _handleOperation(operation);
             }
     
             /**
              * POST CALL CHECK FOR CREATION
              */
             if (postCheckType == PostOperationCheck.openCdp) {
                 // How to get owner
                 // sortedCdps.existCdpOwners(_cdpId);
                 // initialCdpIndex is initialCdpIndex + 1
                 bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);
     
                 // Check for param details
                 ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(cdpId);
                 _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);
                 _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);
                 require(
                     cdpInfo.status == checkParams.expectedStatus,
                     "!LeverageMacroReference: openCDP status check"
                 );
             }
     
             // Update CDP, Ensure the stats are as intended
             if (postCheckType == PostOperationCheck.cdpStats) {
                 ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);
     
                 _doCheckValueType(checkParams.expectedDebt, cdpInfo.debt);
                 _doCheckValueType(checkParams.expectedCollateral, cdpInfo.coll);
                 require(
                     cdpInfo.status == checkParams.expectedStatus,
                     "!LeverageMacroReference: adjustCDP status check"
                 );
             }
     
             // Post check type: Close, ensure it has the status we want
             if (postCheckType == PostOperationCheck.isClosed) {
                 ICdpManagerData.Cdp memory cdpInfo = cdpManager.Cdps(checkParams.cdpId);
     
                 require(
                     cdpInfo.status == checkParams.expectedStatus,
                     "!LeverageMacroReference: closeCDP status check"
                 );
             }
     
             // Sweep here if it's Reference, do not if it's delegate
             if (willSweep) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 98:     function fetchPrice() external override returns (uint256) {
            // Get current and previous price data from Chainlink, and current price data from Fallback
            ChainlinkResponse memory chainlinkResponse = _getCurrentChainlinkResponse();
            ChainlinkResponse memory prevChainlinkResponse = _getPrevChainlinkResponse(
                chainlinkResponse.roundEthBtcId,
                chainlinkResponse.roundStEthEthId
            );
            FallbackResponse memory fallbackResponse = _getCurrentFallbackResponse();
    
            // --- CASE 1: System fetched last price from Chainlink  ---
            if (status == Status.chainlinkWorking) {
                // If Chainlink is broken, try Fallback
                if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
                    // If Fallback is broken then both oracles are untrusted, so return the last good price
                    if (_fallbackIsBroken(fallbackResponse)) {
                        _changeStatus(Status.bothOraclesUntrusted);
                        return lastGoodPrice;
                    }
                    /*
                     * If Fallback is only frozen but otherwise returning valid data, return the last good price.
                     * Fallback may need to be tipped to return current data.
                     */
                    if (_fallbackIsFrozen(fallbackResponse)) {
                        _changeStatus(Status.usingFallbackChainlinkUntrusted);
                        return lastGoodPrice;
                    }
    
                    // If Chainlink is broken and Fallback is working, switch to Fallback and return current Fallback price
                    _changeStatus(Status.usingFallbackChainlinkUntrusted);
                    return _storeFallbackPrice(fallbackResponse);
                }
    
                // If Chainlink is frozen, try Fallback
                if (_chainlinkIsFrozen(chainlinkResponse)) {
                    // If Fallback is broken too, remember Fallback broke, and return last good price
                    if (_fallbackIsBroken(fallbackResponse)) {
                        _changeStatus(Status.usingChainlinkFallbackUntrusted);
                        return lastGoodPrice;
                    }
    
                    // If Fallback is frozen or working, remember Chainlink froze, and switch to Fallback
                    _changeStatus(Status.usingFallbackChainlinkFrozen);
    
                    if (_fallbackIsFrozen(fallbackResponse)) {
                        return lastGoodPrice;
                    }
    
                    // If Fallback is working, use it
                    return _storeFallbackPrice(fallbackResponse);
                }
    
                // If Chainlink price has changed by > 50% between two consecutive rounds, compare it to Fallback's price
                if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
                    // If Fallback is broken, both oracles are untrusted, and return last good price
                    // We don't trust CL for now given this large price differential
                    if (_fallbackIsBroken(fallbackResponse)) {
                        _changeStatus(Status.bothOraclesUntrusted);
                        return lastGoodPrice;
                    }
    
                    // If Fallback is frozen, switch to Fallback and return last good price
                    // We don't trust CL for now given this large price differential
                    if (_fallbackIsFrozen(fallbackResponse)) {
                        _changeStatus(Status.usingFallbackChainlinkUntrusted);
                        return lastGoodPrice;
                    }
    
                    /*
                     * If Fallback is live and both oracles have a similar price, conclude that Chainlink's large price deviation between
                     * two consecutive rounds was likely a legitmate market price movement, and so continue using Chainlink
                     */
                    if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {
                        return _storeChainlinkPrice(chainlinkResponse.answer);
                    }
    
                    // If Fallback is live but the oracles differ too much in price, conclude that Chainlink's initial price deviation was
                    // an oracle failure. Switch to Fallback, and use Fallback price
                    _changeStatus(Status.usingFallbackChainlinkUntrusted);
                    return _storeFallbackPrice(fallbackResponse);
                }
    
                // If Chainlink is working and Fallback is broken, remember Fallback is broken
                if (_fallbackIsBroken(fallbackResponse)) {
                    _changeStatus(Status.usingChainlinkFallbackUntrusted);
                }
    
                // If Chainlink is working, return Chainlink current price (no status change)
                return _storeChainlinkPrice(chainlinkResponse.answer);
            }
    
            // --- CASE 2: The system fetched last price from Fallback ---
            if (status == Status.usingFallbackChainlinkUntrusted) {
                // If both Fallback and Chainlink are live, unbroken, and reporting similar prices, switch back to Chainlink
                if (
                    _bothOraclesLiveAndUnbrokenAndSimilarPrice(
                        chainlinkResponse,
                        prevChainlinkResponse,
                        fallbackResponse
                    )
                ) {
                    _changeStatus(Status.chainlinkWorking);
                    return _storeChainlinkPrice(chainlinkResponse.answer);
                }
    
                if (_fallbackIsBroken(fallbackResponse)) {
                    _changeStatus(Status.bothOraclesUntrusted);
                    return lastGoodPrice;
                }
    
                /*
                 * If Fallback is only frozen but otherwise returning valid data, just return the last good price.
                 * Fallback may need to be tipped to return current data.
                 */
                if (_fallbackIsFrozen(fallbackResponse)) {
                    return lastGoodPrice;
                }
    
                // Otherwise, use Fallback price
                return _storeFallbackPrice(fallbackResponse);
            }
    
            // --- CASE 3: Both oracles were untrusted at the last price fetch ---
            if (status == Status.bothOraclesUntrusted) {
                /*
                 * If there's no fallback, only use Chainlink
                 */
                if (address(fallbackCaller) == address(0)) {
                    // If CL has resumed working
                    if (
                        !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
                        !_chainlinkIsFrozen(chainlinkResponse)
                    ) {
                        _changeStatus(Status.usingChainlinkFallbackUntrusted);
                        return _storeChainlinkPrice(chainlinkResponse.answer);
                    }
                }
    
                /*
                 * If both oracles are now live, unbroken and similar price, we assume that they are reporting
                 * accurately, and so we switch back to Chainlink.
                 */
                if (
                    _bothOraclesLiveAndUnbrokenAndSimilarPrice(
                        chainlinkResponse,
                        prevChainlinkResponse,
                        fallbackResponse
                    )
                ) {
                    _changeStatus(Status.chainlinkWorking);
                    return _storeChainlinkPrice(chainlinkResponse.answer);
                }
    
                // Otherwise, return the last good price - both oracles are still untrusted (no status change)
                return lastGoodPrice;
            }
    
            // --- CASE 4: Using Fallback, and Chainlink is frozen ---
            if (status == Status.usingFallbackChainlinkFrozen) {
                if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
                    // If both Oracles are broken, return last good price
                    if (_fallbackIsBroken(fallbackResponse)) {
                        _changeStatus(Status.bothOraclesUntrusted);
                        return lastGoodPrice;
                    }
    
                    // If Chainlink is broken, remember it and switch to using Fallback
                    _changeStatus(Status.usingFallbackChainlinkUntrusted);
    
                    if (_fallbackIsFrozen(fallbackResponse)) {
                        return lastGoodPrice;
                    }
    
                    // If Fallback is working, return Fallback current price
                    return _storeFallbackPrice(fallbackResponse);
                }
    
                if (_chainlinkIsFrozen(chainlinkResponse)) {
                    // if Chainlink is frozen and Fallback is broken, remember Fallback broke, and return last good price
                    if (_fallbackIsBroken(fallbackResponse)) {
                        _changeStatus(Status.usingChainlinkFallbackUntrusted);
                        return lastGoodPrice;
                    }
    
                    // If both are frozen, just use lastGoodPrice
                    if (_fallbackIsFrozen(fallbackResponse)) {
                        return lastGoodPrice;
                    }
    
                    // if Chainlink is frozen and Fallback is working, keep using Fallback (no status change)
                    return _storeFallbackPrice(fallbackResponse);
                }
    
                // if Chainlink is live and Fallback is broken, remember Fallback broke, and return Chainlink price
                if (_fallbackIsBroken(fallbackResponse)) {
                    _changeStatus(Status.usingChainlinkFallbackUntrusted);
                    return _storeChainlinkPrice(chainlinkResponse.answer);
                }
    
                // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison
                if (_fallbackIsFrozen(fallbackResponse)) {
                    return lastGoodPrice;
                }
    
                // If Chainlink is live and Fallback is working, compare prices. Switch to Chainlink
                // if prices are within 5%, and return Chainlink price.
                if (_bothOraclesSimilarPrice(chainlinkResponse, fallbackResponse)) {
                    _changeStatus(Status.chainlinkWorking);
                    return _storeChainlinkPrice(chainlinkResponse.answer);
                }
    
                // Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price
                _changeStatus(Status.usingFallbackChainlinkUntrusted);
                return _storeFallbackPrice(fallbackResponse);
            }
    
            // --- CASE 5: Using Chainlink, Fallback is untrusted ---
            if (status == Status.usingChainlinkFallbackUntrusted) {
                // If Chainlink breaks, now both oracles are untrusted
                if (_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse)) {
                    _changeStatus(Status.bothOraclesUntrusted);
                    return lastGoodPrice;
                }
    
                // If Chainlink is frozen, return last good price (no status change)
                if (_chainlinkIsFrozen(chainlinkResponse)) {
                    return lastGoodPrice;
                }
    
                // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price
                if (
                    _bothOraclesLiveAndUnbrokenAndSimilarPrice(
                        chainlinkResponse,
                        prevChainlinkResponse,
                        fallbackResponse
                    )
                ) {
                    _changeStatus(Status.chainlinkWorking);
                    return _storeChainlinkPrice(chainlinkResponse.answer);
                }
    
                // If Chainlink is live but deviated >50% from it's previous price and Fallback is still untrusted, switch
                // to bothOraclesUntrusted and return last good price
                if (_chainlinkPriceChangeAboveMax(chainlinkResponse, prevChainlinkResponse)) {
                    _changeStatus(Status.bothOraclesUntrusted);
                    return lastGoodPrice;
                }
    
                // Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,
                // return Chainlink price (no status change)
                return _storeChainlinkPrice(chainlinkResponse.answer);
            }
    
            /// @audit This should never be used, but we added it for the Certora Prover
            return lastGoodPrice;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 674:     function _findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bytes32, bytes32) {
             bytes32 prevId = _prevId;
             bytes32 nextId = _nextId;
     
             if (prevId != dummyId) {
                 if (!contains(prevId) || _NICR > cdpManager.getCachedNominalICR(prevId)) {
                     // `prevId` does not exist anymore or now has a smaller NICR than the given NICR
                     prevId = dummyId;
                 }
             }
     
             if (nextId != dummyId) {
                 if (!contains(nextId) || _NICR < cdpManager.getCachedNominalICR(nextId)) {
                     // `nextId` does not exist anymore or now has a larger NICR than the given NICR
                     nextId = dummyId;
                 }
             }
     
             if (prevId == dummyId && nextId == dummyId) {

```

### <a name="NC-35"></a>[NC-35] if-statement can be converted to a ternary
The code can be made more compact while also increasing readability by converting the following if-statements to ternaries (e.g. ``foo += (x > y) ? a : b`)

 There are 26 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 495:             if (newTCR < CCR) {
                     // Notify RM
                     cdpManager.notifyStartGracePeriod(newTCR);
                 } else {

 666:         if (_chainID() == _CACHED_CHAIN_ID) {
                 return _CACHED_DOMAIN_SEPARATOR;
             } else {

 762:         if (_varMvTokens.isDebtIncrease) {
                 _withdrawDebt(_varMvTokens.user, _varMvTokens.netDebtChange);
             } else {

 769:         if (_varMvTokens.isCollIncrease) {
                 // Coll increase: send change value of stETH to Active Pool, increment ActivePool stETH internal accounting
                 _activePoolAddColl(_varMvTokens.collAddUnderlying, _varMvTokens.collSharesChange);
             } else {

 891:             if (_vars.newTCR < CCR) {
                     // Notify RM
                     cdpManager.notifyStartGracePeriod(_vars.newTCR);
                 } else {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 78:         if (isRecoveryMode) {
                _startGracePeriod(tcr);
            } else {

 99:         if (newTCR < CCR) {
                // Notify system is in RM
                _startGracePeriod(newTCR);
            } else {

 315:         if (_debtIndexDiff > 0) {
                 pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;
             } else {

 636:         if (_scaledCdpColl > _feeSplitDistributed) {
                 return (
                     _feeSplitDistributed,
                     (_scaledCdpColl - _feeSplitDistributed) / DECIMAL_PRECISION
                 );
             } else {
                 // extreme unlikely case to skip fee split on this CDP to avoid revert

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 93:         if (_debt > 0) {
                return (_collShares * NICR_PRECISION) / _debt;
            }
            // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
            else {
                // if (_debt == 0)

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 72:         } else if (flag == CapabilityFlag.Public) {
                return true;
            } else {

 95:         if (enabled) {
                capabilityFlag[target][functionSig] = CapabilityFlag.Public;
            } else {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 183:         if (_chainID() == _CACHED_CHAIN_ID) {
                 return _CACHED_DOMAIN_SEPARATOR;
             } else {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 154:         } else if (flType == FlashLoanType.stETH) {
                 IERC3156FlashLender(address(activePool)).flashLoan(
                     IERC3156FlashBorrower(address(this)),
                     address(stETH),
                     borrowAmount,
                     abi.encode(operation)
                 );
             } else {

 252:         } else if (check.operator == Operator.equal) {
                 require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");
             } else {

 355:         if (token == address(ebtcToken)) {
                 require(
                     msg.sender == address(borrowerOperations),
                     "LeverageMacroReference: wrong lender for eBTC flashloan"
                 );
             } else {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 553:         if (_ICR > LICR) {
                 // Cap at 10%
                 _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;
             } else {

 698:         if (vars.recoveryModeAtStart) {
                 totals = _getTotalFromBatchLiquidate_RecoveryMode(
                     vars.price,
                     systemColl,
                     systemDebt,
                     _cdpArray
                 );
             } else {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 666:         if (
                 _checkHealthyCLResponse(chainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
                 _checkHealthyCLResponse(chainlinkResponse.roundStEthEthId, stEthEthAnswer)
             ) {
                 chainlinkResponse.answer = _formatClAggregateAnswer(
                     ethBtcAnswer,
                     stEthEthAnswer,
                     ethBtcDecimals,
                     stEthEthDecimals
                 );
             } else {

 754:         if (
                 _checkHealthyCLResponse(prevChainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
                 _checkHealthyCLResponse(prevChainlinkResponse.roundStEthEthId, stEthEthAnswer)
             ) {
                 prevChainlinkResponse.answer = _formatClAggregateAnswer(
                     ethBtcAnswer,
                     stEthEthAnswer,
                     ethBtcDecimals,
                     stEthEthDecimals
                 );
             } else {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 141:         if (op.opType == OperationType.delegatecall) {
                 // solhint-disable-next-line no-inline-assembly
                 assembly {
                     success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0)
                 }
             } else {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 189:                 if (_currentIndex == index) {
                         return (_currentCdpId, true);
                     } else {

 437:         if (_firstPrev != dummyId) {
                 data.nodes[_firstPrev].nextId = _lastNext;
             } else {

 442:         if (_lastNext != dummyId) {
                 data.nodes[_lastNext].prevId = _firstPrev;
             } else {

 602:         } else if (_nextId == dummyId) {
                 // `(_prevId, null)` is a valid insert position if `_prevId` is the tail of the list
                 return data.tail == _prevId && _NICR <= cdpManager.getCachedNominalICR(_prevId);
             } else {

 702:         } else if (nextId == dummyId) {
                 // No `nextId` for hint - descend list starting from `prevId`
                 return _descendList(_NICR, prevId);
             } else {

```

### <a name="NC-36"></a>[NC-36] Import declarations should import specific identifiers, rather than the whole file
Using import declarations of the form `import {<identifier_name>} from "some/file.sol"` avoids polluting the symbol namespace making flattened files smaller, and speeds up compilation (but does not save any gas)

 There are 96 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 5: import "./Interfaces/IActivePool.sol";

 6: import "./Interfaces/ICollSurplusPool.sol";

 7: import "./Dependencies/ICollateralToken.sol";

 8: import "./Interfaces/ICdpManagerData.sol";

 9: import "./Dependencies/ERC3156FlashLender.sol";

 10: import "./Dependencies/SafeERC20.sol";

 11: import "./Dependencies/ReentrancyGuard.sol";

 12: import "./Dependencies/AuthNoOwner.sol";

 13: import "./Dependencies/BaseMath.sol";

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 5: import "./Interfaces/IBorrowerOperations.sol";

 6: import "./Interfaces/ICdpManager.sol";

 7: import "./Interfaces/ICdpManagerData.sol";

 8: import "./Interfaces/IEBTCToken.sol";

 9: import "./Interfaces/ICollSurplusPool.sol";

 10: import "./Interfaces/ISortedCdps.sol";

 11: import "./Dependencies/EbtcBase.sol";

 12: import "./Dependencies/ReentrancyGuard.sol";

 13: import "./Dependencies/Ownable.sol";

 14: import "./Dependencies/AuthNoOwner.sol";

 15: import "./Dependencies/ERC3156FlashLender.sol";

 16: import "./Dependencies/PermitNonce.sol";

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 5: import "./Interfaces/ICdpManager.sol";

 6: import "./Interfaces/ICollSurplusPool.sol";

 7: import "./Interfaces/IEBTCToken.sol";

 8: import "./Interfaces/ISortedCdps.sol";

 9: import "./Dependencies/ICollateralTokenOracle.sol";

 10: import "./CdpManagerStorage.sol";

 11: import "./Dependencies/Proxy.sol";

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 5: import "./Interfaces/ICdpManager.sol";

 6: import "./Interfaces/ICollSurplusPool.sol";

 7: import "./Interfaces/IEBTCToken.sol";

 8: import "./Interfaces/ISortedCdps.sol";

 9: import "./Dependencies/EbtcBase.sol";

 10: import "./Dependencies/ReentrancyGuard.sol";

 11: import "./Dependencies/ICollateralTokenOracle.sol";

 12: import "./Dependencies/AuthNoOwner.sol";

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 5: import "./Interfaces/ICollSurplusPool.sol";

 6: import "./Dependencies/ICollateralToken.sol";

 7: import "./Dependencies/SafeERC20.sol";

 8: import "./Dependencies/ReentrancyGuard.sol";

 9: import "./Dependencies/AuthNoOwner.sol";

 10: import "./Interfaces/IActivePool.sol";

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 5: import "../Interfaces/IERC3156FlashLender.sol";

 6: import "../Interfaces/IWETH.sol";

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 5: import "./BaseMath.sol";

 6: import "./EbtcMath.sol";

 7: import "../Interfaces/IActivePool.sol";

 8: import "../Interfaces/IPriceFeed.sol";

 9: import "../Interfaces/IEbtcBase.sol";

 10: import "../Dependencies/ICollateralToken.sol";

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 6: import "./EnumerableSet.sol";

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 5: import "./Interfaces/IEBTCToken.sol";

 7: import "./Dependencies/AuthNoOwner.sol";

 8: import "./Dependencies/PermitNonce.sol";

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 5: import "./Interfaces/ICdpManager.sol";

 6: import "./Interfaces/ISortedCdps.sol";

 7: import "./Dependencies/EbtcBase.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 5: import "./IPool.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 4: import "./IPositionManagers.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 5: import "./IEbtcBase.sol";

 6: import "./ICdpManagerData.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 5: import "./ICollSurplusPool.sol";

 6: import "./IEBTCToken.sol";

 7: import "./ISortedCdps.sol";

 8: import "./IActivePool.sol";

 9: import "./IRecoveryModeGracePeriod.sol";

 10: import "../Dependencies/ICollateralTokenOracle.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 5: import "../Dependencies/IERC20.sol";

 6: import "../Dependencies/IERC2612.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 5: import "./IERC3156FlashBorrower.sol";

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 5: import "./IPriceFeed.sol";

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 4: import "./Interfaces/IBorrowerOperations.sol";

 5: import "./Interfaces/IERC3156FlashLender.sol";

 6: import "./Interfaces/IEBTCToken.sol";

 7: import "./Interfaces/ICdpManager.sol";

 8: import "./Interfaces/ISortedCdps.sol";

 9: import "./Interfaces/IPriceFeed.sol";

 10: import "./Dependencies/ICollateralToken.sol";

 12: import "./Dependencies/SafeERC20.sol";

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 5: import "./Dependencies/ICollateralToken.sol";

 6: import "./Interfaces/IEBTCToken.sol";

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 4: import "./Interfaces/ICdpManagerData.sol";

 5: import "./Interfaces/ICollSurplusPool.sol";

 6: import "./Interfaces/IEBTCToken.sol";

 7: import "./Interfaces/ISortedCdps.sol";

 8: import "./Dependencies/ICollateralTokenOracle.sol";

 9: import "./CdpManagerStorage.sol";

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 5: import "./Interfaces/IPriceFeed.sol";

 6: import "./Interfaces/IFallbackCaller.sol";

 7: import "./Dependencies/AggregatorV3Interface.sol";

 8: import "./Dependencies/BaseMath.sol";

 9: import "./Dependencies/EbtcMath.sol";

 10: import "./Dependencies/AuthNoOwner.sol";

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 5: import "./Interfaces/ISortedCdps.sol";

 6: import "./Interfaces/ICdpManager.sol";

 7: import "./Interfaces/IBorrowerOperations.sol";

```

### <a name="NC-37"></a>[NC-37] Interfaces should be defined in separate files from their usage
The interfaces below should be defined in separate files, so that it’s easier for future projects to import them, and to avoid duplication later on if they need to be used elsewhere in the project

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

```

### <a name="NC-38"></a>[NC-38] `internal` functions not called by the contract should be removed
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/EBTCToken.sol

 323:     function _requireCallerIsCdpM() internal view {

```

### <a name="NC-39"></a>[NC-39] Large numeric literals should use underscores for readability

 There are 10 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

 148:     uint256 public minuteDecayFactor = 999037758833783000;

 150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 19:     uint256 public constant LICR = 1030000000000000000; // 103%

 22:     uint256 public constant MCR = 1100000000000000000; // 110%

 25:     uint256 public constant CCR = 1250000000000000000; // 125%

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 60:         if (_minutes > 525600000) {

 61:             _minutes = 525600000;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

 33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

```

### <a name="NC-40"></a>[NC-40] Long functions should be refactored into multiple, smaller, functions

 There are 15 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  40+ lines
 261:     function flashLoan(
             IERC3156FlashBorrower receiver,
             address token,
             uint256 amount,
             bytes calldata data
         ) external override returns (bool) {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  90+ lines
 328:     function _adjustCdpInternal(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) internal {

 /// @audit  100+ lines
 439:     function _openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) internal returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  90+ lines
 135:     function _redeemCollateralFromCdp(
             SingleRedemptionInputs memory _redeemColFromCdp
         ) internal returns (SingleRedemptionValues memory singleRedemption) {

 /// @audit  160+ lines
 320:     function redeemCollateral(
             uint256 _debt,
             bytes32 _firstRedemptionHint,
             bytes32 _upperPartialRedemptionHint,
             bytes32 _lowerPartialRedemptionHint,
             uint256 _partialRedemptionHintNICR,
             uint256 _maxIterations,
             uint256 _maxFeePercentage
         ) external override nonReentrantSelfAndBOps {
             RedemptionTotals memory totals;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  60+ lines
 344:     function _syncAccounting(bytes32 _cdpId) internal {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  70+ lines
 48:     function getRedemptionHints(
            uint256 _EBTCamount,
            uint256 _price,
            uint256 _maxIterations
        )
            external
            view
            returns (
                bytes32 firstRedemptionHint,
                uint256 partialRedemptionHintNICR,
                uint256 truncatedEBTCamount,
                uint256 partialRedemptionNewColl
            )
        {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  90+ lines
 118:     function doOperation(
             FlashLoanType flType,
             uint256 borrowAmount,
             LeverageMacroOperation calldata operation,
             PostOperationCheck postCheckType,
             PostCheckParams calldata checkParams
         ) external {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  60+ lines
 61:     function _liquidateIndividualCdpSetup(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) internal {

 /// @audit  60+ lines
 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(
             LiquidationLocals memory _liqState
         ) private returns (LiquidationLocals memory) {

 /// @audit  80+ lines
 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (LiquidationRecoveryModeLocals memory) {

 /// @audit  50+ lines
 397:     function _liquidateCDPPartially(
             LiquidationLocals memory _partialState
         ) private returns (uint256, uint256) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  250+ lines
 98:     function fetchPrice() external override returns (uint256) {

 /// @audit  70+ lines
 606:     function _getCurrentChainlinkResponse()
             internal
             view
             returns (ChainlinkResponse memory chainlinkResponse)
         {

 /// @audit  80+ lines
 687:     function _getPrevChainlinkResponse(
             uint80 _currentRoundEthBtcId,
             uint80 _currentRoundStEthEthId
         ) internal view returns (ChainlinkResponse memory prevChainlinkResponse) {

```

### <a name="NC-41"></a>[NC-41] Missing checks constructor/initializer assignments
Consider whether reasonable bounds checks for variables would be useful.

 There are 30 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 53:         borrowerOperationsAddress = _borrowerOperationsAddress;

 54:         cdpManagerAddress = _cdpManagerAddress;

 56:         collSurplusPoolAddress = _collSurplusAddress;

 57:         feeRecipientAddress = _feeRecipientAddress;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 121:         feeRecipientAddress = _feeRecipientAddress;

 131:         _HASHED_NAME = hashedName;

 132:         _HASHED_VERSION = hashedVersion;

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 53:         stakingRewardSplit = STAKING_REWARD_SPLIT;

 59:         systemStEthFeePerUnitIndex = DECIMAL_PRECISION;

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

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 19:         owner = _owner;

 20:         authority = _authority;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 68:         cdpManagerAddress = _cdpManagerAddress;

 69:         borrowerOperationsAddress = _borrowerOperationsAddress;

 74:         _HASHED_NAME = hashedName;

 75:         _HASHED_VERSION = hashedVersion;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

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
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 45:         owner = _owner;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 96:         borrowerOperationsAddress = _borrowerOperationsAddress;

```

### <a name="NC-42"></a>[NC-42] Missing checks for state variable assignments
Consider whether reasonable bounds checks for variables would be useful.

 There are 17 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 171:         feeRecipientCollShares = cachedFeeRecipientCollShares;

 199:         systemDebt = cachedSystemDebt;

 212:         systemDebt = cachedSystemDebt;

 246:         systemCollShares = cachedSystemCollShares;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 67:             lastGracePeriodStartTimestamp = UNSET_TIMESTAMP;

 295:         totalStakesSnapshot = _totalStakesSnapshot;

 298:         totalCollateralSnapshot = _totalCollateralSnapshot;

 412:         totalStakes = _newTotalStakes;

 423:         totalStakes = _newTotalStakes;

 581:         systemStEthFeePerUnitIndex = _newPerUnit;

 582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 47:         authority = newAuthority;

 53:         owner = newOwner;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 377:                     fallbackCaller = newFallbackCaler;

 386:             fallbackCaller = newFallbackCaler;

 547:         status = _status;

 554:         lastGoodPrice = _currentPrice;

```

### <a name="NC-43"></a>[NC-43] Missing checks for state variable assignments
Consider whether reasonable bounds checks for variables would be useful.

 There are 17 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 171:         feeRecipientCollShares = cachedFeeRecipientCollShares;

 199:         systemDebt = cachedSystemDebt;

 212:         systemDebt = cachedSystemDebt;

 246:         systemCollShares = cachedSystemCollShares;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 67:             lastGracePeriodStartTimestamp = UNSET_TIMESTAMP;

 295:         totalStakesSnapshot = _totalStakesSnapshot;

 298:         totalCollateralSnapshot = _totalCollateralSnapshot;

 412:         totalStakes = _newTotalStakes;

 423:         totalStakes = _newTotalStakes;

 581:         systemStEthFeePerUnitIndex = _newPerUnit;

 582:         systemStEthFeePerUnitIndexError = _newErrorPerUnit;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 47:         authority = newAuthority;

 53:         owner = newOwner;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 377:                     fallbackCaller = newFallbackCaler;

 386:             fallbackCaller = newFallbackCaler;

 547:         status = _status;

 554:         lastGoodPrice = _currentPrice;

```

### <a name="NC-44"></a>[NC-44] Multiple `address`/`ID` mappings can be combined into a single `mapping` of an `address`/`ID` to a struct, for readability
Well-organized data structures make code reviews easier, which may lead to fewer bugs. Consider combining related mappings into mappings to structs, so it’s clear what data is related.

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

### <a name="NC-45"></a>[NC-45] Named imports of parent contracts are missing

 There are 17 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner
 22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  EbtcBase, ReentrancyGuard, IBorrowerOperations, ERC3156FlashLender, AuthNoOwner, PermitNonce
 21: contract BorrowerOperations is

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  CdpManagerStorage, ICdpManager, Proxy
 16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner
 19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  ICollSurplusPool, ReentrancyGuard, AuthNoOwner
 16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 /// @audit  IERC3156FlashLender
 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  BaseMath, IEbtcBase
 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  IEBTCToken, AuthNoOwner, PermitNonce
 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  EbtcBase
 11: contract HintHelpers is EbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 /// @audit  IPool
 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 /// @audit  IPositionManagers
 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 /// @audit  IEbtcBase, ICdpManagerData
 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  IRecoveryModeGracePeriod
 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 /// @audit  IERC20, IERC2612
 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  CdpManagerStorage
 13: contract LiquidationLibrary is CdpManagerStorage {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  BaseMath, IPriceFeed, AuthNoOwner
 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  ISortedCdps
 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-46"></a>[NC-46] NatSpec: Contract declarations should have `@author` tags

 There are 36 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 22: contract ActivePool is IActivePool, ERC3156FlashLender, ReentrancyGuard, BaseMath, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 21: contract BorrowerOperations is

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 5: library EbtcMath {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 11: contract HintHelpers is EbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

 26: contract LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

 40: contract LeverageMacroDelegateTarget is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 11: contract LeverageMacroFactory {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 11: contract LeverageMacroReference is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 13: contract LiquidationLibrary is CdpManagerStorage {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 25: contract SimplifiedDiamondLike {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-47"></a>[NC-47] NatSpec: Contract declarations should have descriptions
e.g. `@dev` or `@notice`, and it must appear above the contract definition braces in order to be identified by the compiler as NatSpec

 There are 25 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 5: library EbtcMath {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 11: contract LeverageMacroFactory {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-48"></a>[NC-48] NatSpec: Contract declarations should have `@dev` tags
`@dev` is used to explain extra details to developers

 There are 30 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 9: abstract contract Auth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 10: contract AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 5: library EbtcMath {

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 7: abstract contract ReentrancyGuard {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 13: contract Governor is RolesAuthority {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 11: contract LeverageMacroFactory {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-49"></a>[NC-49] NatSpec: Contract declarations should have `@notice` tags
`@notice` is used to explain to end users what the contract does, and the compiler interprets `///` or `/**` comments as this tag if one wasn’t explicitly provided

 There are 28 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 19: contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 5: library EbtcMath {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 11: contract HintHelpers is EbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 11: contract LeverageMacroFactory {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 13: contract LiquidationLibrary is CdpManagerStorage {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-50"></a>[NC-50] NatSpec: Contract declarations should have `@title` tags

 There are 30 instances:

 ```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 16: contract CollSurplusPool is ICollSurplusPool, ReentrancyGuard, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 9: abstract contract Auth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 10: contract AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 8: abstract contract ERC3156FlashLender is IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 16: contract EbtcBase is BaseMath, IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 5: library EbtcMath {

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 7: abstract contract ReentrancyGuard {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 12: contract RolesAuthority is IRolesAuthority, Auth, Authority {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 26: contract EBTCToken is IEBTCToken, AuthNoOwner, PermitNonce {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 13: contract Governor is RolesAuthority {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 7: interface IActivePool is IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 7: interface IBorrowerOperations is IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 9: interface ICdpManager is IEbtcBase, ICdpManagerData {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 13: interface ICdpManagerData is IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 5: interface ICollSurplusPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 8: interface IEBTCToken is IERC20, IERC2612 {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 5: interface IERC3156FlashBorrower {

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 7: interface IERC3156FlashLender {

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 7: interface IEbtcBase {

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 5: interface IFallbackCaller {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 6: interface IPool {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 5: interface IPositionManagers {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 5: interface IPriceFeed {

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 5: interface IRecoveryModeGracePeriod {

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 6: interface ISortedCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 14: interface ICdpCdps {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 21: contract PriceFeed is BaseMath, IPriceFeed, AuthNoOwner {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 51: contract SortedCdps is ISortedCdps {

```

### <a name="NC-51"></a>[NC-51] NatSpec: Event declarations should have descriptions

 There are 54 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 10:     event OwnershipTransferred(address indexed user, address indexed newOwner);

 12:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 11:     event AuthorityUpdated(address indexed user, Authority indexed newAuthority);

```


```solidity
File: packages/contracts/contracts/Governor.sol

 32:     event RoleNameSet(uint8 indexed role, string indexed name);

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);

 10:     event SystemCollSharesUpdated(uint256 _coll);

 11:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

 12:     event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);

 13:     event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);

 14:     event FlashLoanSuccess(
            address indexed _receiver,
            address indexed _token,
            uint256 _amount,
            uint256 _fee

 20:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 10:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

 11:     event FlashLoanSuccess(
            address indexed _receiver,
            address indexed _token,
            uint256 _amount,
            uint256 _fee

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 16:     event FeeRecipientAddressChanged(address indexed _feeRecipientAddress);

 17:     event StakingRewardSplitSet(uint256 _stakingRewardSplit);

 18:     event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);

 19:     event MinuteDecayFactorSet(uint256 _minuteDecayFactor);

 20:     event BetaSet(uint256 _beta);

 21:     event RedemptionsPaused(bool _paused);

 23:     event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);

 24:     event Redemption(
            uint256 _debtToRedeemExpected,
            uint256 _debtToRedeemActual,
            uint256 _collSharesSent,
            uint256 _feeCollShares,
            address indexed _redeemer

 31:     event CdpUpdated(
            bytes32 indexed _cdpId,
            address indexed _borrower,
            address indexed _executor,
            uint256 _oldDebt,
            uint256 _oldCollShares,
            uint256 _debt,
            uint256 _collShares,
            uint256 _stake,
            CdpOperation _operation

 42:     event CdpLiquidated(
            bytes32 indexed _cdpId,
            address indexed _borrower,
            uint _debt,
            uint _collShares,
            CdpOperation _operation,
            address indexed _liquidator,
            uint _premiumToLiquidator

 51:     event CdpPartiallyLiquidated(
            bytes32 indexed _cdpId,
            address indexed _borrower,
            uint256 _debt,
            uint256 _collShares,
            CdpOperation operation,
            address indexed _liquidator,
            uint _premiumToLiquidator

 60:     event BaseRateUpdated(uint256 _baseRate);

 61:     event LastRedemptionTimestampUpdated(uint256 _lastFeeOpTime);

 62:     event TotalStakesUpdated(uint256 _newTotalStakes);

 63:     event SystemSnapshotsUpdated(uint256 _totalStakesSnapshot, uint256 _totalCollateralSnapshot);

 64:     event SystemDebtRedistributionIndexUpdated(uint256 _systemDebtRedistributionIndex);

 65:     event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);

 66:     event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);

 67:     event StEthIndexUpdated(uint256 _oldIndex, uint256 _newIndex, uint256 _updTimestamp);

 68:     event CollateralFeePerUnitUpdated(uint256 _oldPerUnit, uint256 _newPerUnit, uint256 _feeTaken);

 69:     event CdpFeeSplitApplied(
            bytes32 _cdpId,
            uint256 _oldPerUnitCdp,
            uint256 _newPerUnitCdp,
            uint256 _collReduced,
            uint256 _collLeft

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 8:     event SurplusCollSharesUpdated(address indexed _account, uint256 _newBalance);

 9:     event CollSharesTransferred(address indexed _to, uint256 _amount);

 11:     event SweepTokenSuccess(address indexed _token, uint256 _amount, address indexed _recipient);

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 8:     event FlashFeeSet(address indexed _setter, uint256 _oldFee, uint256 _newFee);

 9:     event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);

 10:     event FlashLoansPaused(address indexed _setter, bool _paused);

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 7:     event FallbackTimeOutChanged(uint256 _oldTimeOut, uint256 _newTimeOut);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 9:     event ETHBalanceUpdated(uint256 _newBalance);

 10:     event EBTCBalanceUpdated(uint256 _newBalance);

 11:     event CollSharesTransferred(address indexed _to, uint256 _amount);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 12:     event PositionManagerApprovalSet(
            address indexed _borrower,
            address indexed _positionManager,
            PositionManagerApproval _approval

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 7:     event LastGoodPriceUpdated(uint256 _lastGoodPrice);

 8:     event PriceFeedStatusChanged(Status newStatus);

 9:     event FallbackCallerChanged(
           address indexed _oldFallbackCaller,
           address indexed _newFallbackCaller

 13:     event UnhealthyFallbackCaller(address indexed _fallbackCaller, uint256 timestamp);

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

 11:     event GracePeriodDurationSet(uint256 _recoveryModeGracePeriodDuration);

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 9:     event NodeAdded(bytes32 _id, uint _NICR);

 10:     event NodeRemoved(bytes32 _id);

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 19:     event DeployNewMacro(address indexed sender, address indexed newContractAddress);

```

### <a name="NC-52"></a>[NC-52] NatSpec: file is missing NatSpec

 There are 14 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

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
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 3: pragma solidity 0.8.17;

```

### <a name="NC-53"></a>[NC-53] NatSpec: Function `@param` tag is missing

 There are 255 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  missing '@param _cdpManagerAddress', '@param _activePoolAddress', '@param _collSurplusPoolAddress', '@param _priceFeedAddress', '@param _sortedCdpsAddress', '@param _ebtcTokenAddress', '@param _feeRecipientAddress', '@param _collTokenAddress'
 107:     constructor(
             address _cdpManagerAddress,
             address _activePoolAddress,
             address _collSurplusPoolAddress,
             address _priceFeedAddress,
             address _sortedCdpsAddress,
             address _ebtcTokenAddress,
             address _feeRecipientAddress,
             address _collTokenAddress
         ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) {

 /// @audit  missing '@param _cdpId', '@param _stEthBalanceDecrease', '@param _debtChange', '@param _isDebtIncrease', '@param _upperHint', '@param _lowerHint', '@param _stEthBalanceIncrease'
 328:     function _adjustCdpInternal(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) internal {

 /// @audit  missing '@param _debt', '@param _upperHint', '@param _lowerHint', '@param _stEthBalance', '@param _borrower'
 439:     function _openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) internal returns (bytes32) {

 /// @audit  missing '@param _borrower', '@param _positionManager'
 615:     function _getPositionManagerApproval(
             address _borrower,
             address _positionManager
         ) internal view returns (PositionManagerApproval) {

 /// @audit  missing '@param _borrower', '@param _positionManager', '@param _approval'
 635:     function _setPositionManagerApproval(
             address _borrower,
             address _positionManager,
             PositionManagerApproval _approval
         ) internal {

 /// @audit  missing '@param typeHash', '@param name', '@param version'
 677:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 /// @audit  missing '@param _collReceived', '@param _requestedCollWithdrawal'
 744:     function _getCollSharesChangeFromStEthChange(
             uint256 _collReceived,
             uint256 _requestedCollWithdrawal
         ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

 /// @audit  missing '@param _varMvTokens'
 760:     function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

 /// @audit  missing '@param _account', '@param _debt'
 790:     function _withdrawDebt(address _account, uint256 _debt) internal {

 /// @audit  missing '@param _account', '@param _debt'
 796:     function _repayDebt(address _account, uint256 _debt) internal {

 /// @audit  missing '@param _stEthBalanceIncrease', '@param _stEthBalanceDecrease'
 803:     function _requireSingularCollChange(
             uint256 _stEthBalanceIncrease,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 /// @audit  missing '@param _stEthBalanceIncrease', '@param _debtChange', '@param _stEthBalanceDecrease'
 813:     function _requireNonZeroAdjustment(
             uint256 _stEthBalanceIncrease,
             uint256 _debtChange,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 /// @audit  missing '@param _cdpManager', '@param _cdpId'
 824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {

 /// @audit  missing '@param _cdpId'
 829:     function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

 /// @audit  missing '@param _debtChange'
 834:     function _requireNonZeroDebtChange(uint _debtChange) internal pure {

 /// @audit  missing '@param _tcr'
 838:     function _requireNotInRecoveryMode(uint256 _tcr) internal view {

 /// @audit  missing '@param _stEthBalanceDecrease'
 845:     function _requireNoStEthBalanceDecrease(uint256 _stEthBalanceDecrease) internal pure {

 /// @audit  missing '@param _isRecoveryMode', '@param _stEthBalanceDecrease', '@param _isDebtIncrease', '@param _vars'
 852:     function _requireValidAdjustmentInCurrentMode(
             bool _isRecoveryMode,
             uint256 _stEthBalanceDecrease,
             bool _isDebtIncrease,
             AdjustCdpLocals memory _vars
         ) internal {

 /// @audit  missing '@param _newICR'
 910:     function _requireICRisNotBelowMCR(uint256 _newICR) internal pure {

 /// @audit  missing '@param _newICR'
 917:     function _requireICRisNotBelowCCR(uint256 _newICR) internal pure {

 /// @audit  missing '@param _newICR', '@param _oldICR'
 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 /// @audit  missing '@param _newTCR'
 928:     function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure {

 /// @audit  missing '@param _debt'
 935:     function _requireNonZeroDebt(uint256 _debt) internal pure {

 /// @audit  missing '@param _stEthBalance'
 939:     function _requireAtLeastMinNetStEthBalance(uint256 _stEthBalance) internal pure {

 /// @audit  missing '@param _currentDebt', '@param _debtRepayment'
 946:     function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

 /// @audit  missing '@param _account', '@param _debtRepayment'
 953:     function _requireSufficientEbtcTokenBalance(
             address _account,
             uint256 _debtRepayment
         ) internal view {

 /// @audit  missing '@param _borrower'
 963:     function _requireBorrowerOrPositionManagerAndUpdateManagerApproval(address _borrower) internal {

 /// @audit  missing '@param vars', '@param _isDebtIncrease'
 986:     function _getNewNominalICRFromCdpChange(
             AdjustCdpLocals memory vars,
             bool _isDebtIncrease
         ) internal pure returns (uint256) {

 /// @audit  missing '@param _collShares', '@param _debt', '@param _collSharesChange', '@param _isCollIncrease', '@param _debtChange', '@param _isDebtIncrease', '@param _price'
 1004:     function _getNewICRFromCdpChange(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

 /// @audit  missing '@param _collShares', '@param _debt', '@param _collSharesChange', '@param _isCollIncrease', '@param _debtChange', '@param _isDebtIncrease'
 1030:     function _getNewCdpAmounts(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease
          ) internal pure returns (uint256, uint256) {

 /// @audit  missing '@param _stEthBalanceChange', '@param _isCollIncrease', '@param _debtChange', '@param _isDebtIncrease', '@param _price'
 1049:     function _getNewTCRFromCdpChange(
              uint256 _stEthBalanceChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  missing '@param _cdpId', '@param _EBTC', '@param _collSurplus', '@param _liquidatorRewardShares', '@param _borrower'
 244:     function _closeCdpByRedemption(
             bytes32 _cdpId,
             uint256 _EBTC,
             uint256 _collSurplus,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) internal {

 /// @audit  missing '@param _firstRedemptionHint', '@param _price'
 272:     function _isValidFirstRedemptionHint(
             bytes32 _firstRedemptionHint,
             uint256 _price
         ) internal view returns (bool) {

 /// @audit  missing '@param _start', '@param _total', '@param _end'
 489:     function _getCdpIdsToRemove(
             bytes32 _start,
             uint256 _total,
             bytes32 _end
         ) internal view returns (bytes32[] memory) {
             uint256 _cnt = _total;

 /// @audit  missing '@param _cdpId'
 550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
             /* Max array size is 2**128 - 1, i.e. ~3e30 cdps. No risk of overflow, since cdps have minimum EBTC

 /// @audit  missing '@param _systemCollShares', '@param _systemDebt', '@param _price'
 595:     function _checkPotentialRecoveryMode(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (bool) {
             uint256 TCR = _computeTCRWithGivenSystemValues(_systemCollShares, _systemDebt, _price);

 /// @audit  missing '@param _ETHDrawn', '@param _price', '@param _totalEBTCSupply'
 612:     function _updateBaseRateFromRedemption(
             uint256 _ETHDrawn,
             uint256 _price,
             uint256 _totalEBTCSupply
         ) internal returns (uint256) {
             uint256 decayedBaseRate = _calcDecayedBaseRate();

 /// @audit  missing '@param _baseRate'
 647:     function _calcRedemptionRate(uint256 _baseRate) internal view returns (uint256) {
             return

 /// @audit  missing '@param _ETHDrawn'
 655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {
             return _calcRedemptionFee(getRedemptionRate(), _ETHDrawn);

 /// @audit  missing '@param _redemptionRate', '@param _ETHDrawn'
 667:     function _calcRedemptionFee(
             uint256 _redemptionRate,
             uint256 _ETHDrawn
         ) internal pure returns (uint256) {
             uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

 /// @audit  missing '@param _redeemer', '@param _amount', '@param _totalSupply'
 737:     function _requireEbtcBalanceCoversRedemptionAndWithinSupply(
             address _redeemer,
             uint256 _amount,
             uint256 _totalSupply
         ) internal view {
             uint256 callerBalance = ebtcToken.balanceOf(_redeemer);

 /// @audit  missing '@param _amount'
 753:     function _requireAmountGreaterThanZero(uint256 _amount) internal pure {
             require(_amount > 0, "CdpManager: Amount must be greater than zero");

 /// @audit  missing '@param _price', '@param _TCR'
 757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {
             require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

 /// @audit  missing '@param _maxFeePercentage'
 761:     function _requireValidMaxFeePercentage(uint256 _maxFeePercentage) internal view {
             require(

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  missing '@param _tcr'
 49:     function _startGracePeriod(uint256 _tcr) internal {

 /// @audit  missing '@param _tcr'
 63:     function _endGracePeriod(uint256 _tcr) internal {

 /// @audit  missing '@param systemCollShares', '@param systemDebt', '@param price'
 87:     function _syncGracePeriodForGivenValues(
            uint256 systemCollShares,
            uint256 systemDebt,
            uint256 price
        ) internal {

 /// @audit  missing '@param _cdpId', '@param closedStatus'
 255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {

 /// @audit  missing '@param _cdpId', '@param closedStatus'
 260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

 /// @audit  missing '@param _collRemainder'
 293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

 /// @audit  missing '@param _cdpId'
 304:     function _getPendingRedistributedDebt(
             bytes32 _cdpId
         ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

 /// @audit  missing '@param _cdpId'
 327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

 /// @audit  missing '@param _cdpId'
 336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

 /// @audit  missing '@param _cdpId'
 344:     function _syncAccounting(bytes32 _cdpId) internal {

 /// @audit  missing '@param _cdpId'
 410:     function _removeStake(bytes32 _cdpId) internal {

 /// @audit  missing '@param _cdpId'
 419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

 /// @audit  missing '@param _cdpId'
 431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

 /// @audit  missing '@param _coll'
 441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

 /// @audit  missing '@param _cdpId', '@param cdpIdsArrayLength'
 463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
             Status cdpStatus = Cdps[_cdpId].status;

 /// @audit  missing '@param _systemCollShares', '@param _systemDebt', '@param _price'
 489:     function _computeTCRWithGivenSystemValues(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);

 /// @audit  missing '@param _oldIndex', '@param _newIndex'
 539:     function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {
             if (_newIndex != _oldIndex) {

 /// @audit  missing '@param _feeTaken', '@param _newPerUnit', '@param _newErrorPerUnit'
 574:     function _takeSplitAndUpdateFeePerUnit(
             uint256 _feeTaken,
             uint256 _newPerUnit,
             uint256 _newErrorPerUnit
         ) internal {
             uint256 _oldPerUnit = systemStEthFeePerUnitIndex;

 /// @audit  missing '@param _cdpId', '@param _newColl', '@param _feeSplitDistributed', '@param _oldPerUnitCdp', '@param _systemStEthFeePerUnitIndex'
 592:     function _applyAccumulatedFeeSplit(
             bytes32 _cdpId,
             uint256 _newColl,
             uint256 _feeSplitDistributed,
             uint256 _oldPerUnitCdp,
             uint256 _systemStEthFeePerUnitIndex
         ) internal {
             // apply split fee to given CDP

 /// @audit  missing '@param _cdpId'
 648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {
             require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

 /// @audit  missing '@param CdpOwnersArrayLength'
 652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {
             require(

 /// @audit  missing '@param _price'
 701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {
             (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  missing '@param currentCollShare', '@param currentDebt', '@param _price'
 707:     function _calculateCR(
             uint256 currentCollShare,
             uint256 currentDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);

 /// @audit  missing '@param _cdpId'
 733:     function _getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) internal view returns (CdpDebtAndCollShares memory) {
             (uint256 entireDebt, uint256 entireColl) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  missing '@param _newIndex', '@param _oldIndex'
 761:     function _calcSyncedGlobalAccounting(
             uint256 _newIndex,
             uint256 _oldIndex
         ) internal view returns (uint256, uint256, uint256) {
             if (_newIndex > _oldIndex && totalStakes > 0) {

 /// @audit  missing '@param _cdpId', '@param _cdpPerUnitIdx', '@param _systemStEthFeePerUnitIndex'
 787:     function _calcSyncedAccounting(
             bytes32 _cdpId,
             uint256 _cdpPerUnitIdx,
             uint256 _systemStEthFeePerUnitIndex
         ) internal view returns (uint256, uint256, uint256, uint256, uint256) {
             uint256 _feeSplitApplied;

 /// @audit  missing '@param _cdpId'
 822:     function _getSyncedCdpDebtAndRedistribution(
             bytes32 _cdpId
         ) internal view returns (uint256, uint256, uint256) {
             (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  missing '@param _owner', '@param _authority'
 18:     constructor(address _owner, Authority _authority) {

 /// @audit  missing '@param user', '@param functionSig'
 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

 /// @audit  missing '@param newAuthority'
 42:     function setAuthority(Authority newAuthority) public virtual {

 /// @audit  missing '@param newOwner'
 52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 /// @audit  missing '@param user', '@param functionSig'
 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

 /// @audit  missing '@param newAuthority'
 38:     function setAuthority(address newAuthority) public virtual {

 /// @audit  missing '@param newAuthority'
 55:     function _initializeAuthority(address newAuthority) internal {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  missing '@param _stEthBalance'
 60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

 /// @audit  missing '@param _price'
 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 /// @audit  missing '@param _price'
 83:     function _getTCRWithSystemDebtAndCollShares(
            uint256 _price
        ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

 /// @audit  missing '@param _price'
 95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

 /// @audit  missing '@param _tcr'
 99:     function _checkRecoveryModeForTCR(uint256 _tcr) internal view returns (bool) {

 /// @audit  missing '@param _fee', '@param _amount', '@param _maxFeePercentage'
 103:     function _requireUserAcceptsFee(
             uint256 _fee,
             uint256 _amount,
             uint256 _maxFeePercentage
         ) internal pure {

 /// @audit  missing '@param _debt', '@param _price'
 115:     function _convertDebtDenominationToBtc(
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {

 /// @audit  missing '@param _icr', '@param _tcr'
 124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

 /// @audit  missing '@param _icr'
 134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

 /// @audit  missing '@param _icr', '@param _tcr'
 140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 /// @audit  missing '@param _a', '@param _b'
 20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a < _b) ? _a : _b;

 /// @audit  missing '@param _a', '@param _b'
 24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? _a : _b;

 /// @audit  missing '@param x', '@param y'
 35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {
            uint256 prod_xy = x * y;

 /// @audit  missing '@param _base', '@param _minutes'
 59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {
            if (_minutes > 525600000) {

 /// @audit  missing '@param _a', '@param _b'
 88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  missing '@param _collShares', '@param _debt'
 92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {
            if (_debt > 0) {

 /// @audit  missing '@param _stEthBalance', '@param _debt', '@param _price'
 104:     function _computeCR(
             uint256 _stEthBalance,
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {
             if (_debt > 0) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  missing '@param _owner', '@param _authority'
 20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

 /// @audit  missing '@param user', '@param role'
 38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

 /// @audit  missing '@param role', '@param target', '@param functionSig'
 42:     function doesRoleHaveCapability(
            uint8 role,
            address target,
            bytes4 functionSig
        ) public view virtual returns (bool) {

 /// @audit  missing '@param target', '@param functionSig'
 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

 /// @audit  missing '@param user', '@param target', '@param functionSig'
 63:     function canCall(
            address user,
            address target,
            bytes4 functionSig
        ) public view virtual override returns (bool) {

 /// @audit  missing '@param target', '@param functionSig', '@param enabled'
 85:     function setPublicCapability(
            address target,
            bytes4 functionSig,
            bool enabled
        ) public virtual requiresAuth {

 /// @audit  missing '@param role', '@param target', '@param functionSig', '@param enabled'
 106:     function setRoleCapability(
             uint8 role,
             address target,
             bytes4 functionSig,
             bool enabled
         ) public virtual requiresAuth {

 /// @audit  missing '@param target', '@param functionSig'
 133:     function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {

 /// @audit  missing '@param user', '@param role', '@param enabled'
 147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  missing '@param account'
 115:     function balanceOf(address account) external view override returns (uint256) {

 /// @audit  missing '@param recipient', '@param amount'
 119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

 /// @audit  missing '@param owner', '@param spender'
 125:     function allowance(address owner, address spender) external view override returns (uint256) {

 /// @audit  missing '@param spender', '@param amount'
 129:     function approve(address spender, uint256 amount) external override returns (bool) {

 /// @audit  missing '@param sender', '@param recipient', '@param amount'
 134:     function transferFrom(
             address sender,
             address recipient,
             uint256 amount
         ) external override returns (bool) {

 /// @audit  missing '@param spender', '@param addedValue'
 152:     function increaseAllowance(
             address spender,
             uint256 addedValue
         ) external override returns (bool) {

 /// @audit  missing '@param spender', '@param subtractedValue'
 160:     function decreaseAllowance(
             address spender,
             uint256 subtractedValue
         ) external override returns (bool) {

 /// @audit  missing '@param typeHash', '@param name', '@param version'
 235:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 /// @audit  missing '@param sender', '@param recipient', '@param amount'
 246:     function _transfer(address sender, address recipient, uint256 amount) internal {

 /// @audit  missing '@param account', '@param amount'
 262:     function _mint(address account, uint256 amount) internal {

 /// @audit  missing '@param account', '@param amount'
 270:     function _burn(address account, uint256 amount) internal {

 /// @audit  missing '@param owner', '@param spender', '@param amount'
 285:     function _approve(address owner, address spender, uint256 amount) internal {

 /// @audit  missing '@param _recipient'
 295:     function _requireValidRecipient(address _recipient) internal view {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  missing '@param _sortedCdpsAddress', '@param _cdpManagerAddress', '@param _collateralAddress', '@param _activePoolAddress', '@param _priceFeedAddress'
 27:     constructor(
            address _sortedCdpsAddress,
            address _cdpManagerAddress,
            address _collateralAddress,
            address _activePoolAddress,
            address _priceFeedAddress
        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {

 /// @audit  missing '@param _CR', '@param _numTrials', '@param _inputRandomSeed'
 164:     function getApproxHint(
             uint256 _CR,
             uint256 _numTrials,
             uint256 _inputRandomSeed
         ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 /// @audit  missing '@param _account', '@param _amount'
 23:     function transferSystemCollShares(address _account, uint256 _amount) external;

 /// @audit  missing '@param _value'
 25:     function increaseSystemCollShares(uint256 _value) external;

 /// @audit  missing '@param _account', '@param _shares', '@param _liquidatorRewardShares'
 27:     function transferSystemCollSharesAndLiquidatorReward(

 /// @audit  missing '@param _shares'
 33:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;

 /// @audit  missing '@param _shares'
 35:     function claimFeeRecipientCollShares(uint256 _shares) external;

 /// @audit  missing '@param _feeRecipientAddress'
 41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 /// @audit  missing '@param _EBTCAmount', '@param _upperHint', '@param _lowerHint', '@param _stEthBalance'
 20:     function openCdp(

 /// @audit  missing '@param _EBTCAmount', '@param _upperHint', '@param _lowerHint', '@param _collAmount', '@param _borrower'
 27:     function openCdpFor(

 /// @audit  missing '@param _cdpId', '@param _upperHint', '@param _lowerHint', '@param _stEthBalanceIncrease'
 35:     function addColl(

 /// @audit  missing '@param _cdpId', '@param _stEthBalanceDecrease', '@param _upperHint', '@param _lowerHint'
 42:     function withdrawColl(

 /// @audit  missing '@param _cdpId', '@param _amount', '@param _upperHint', '@param _lowerHint'
 49:     function withdrawDebt(

 /// @audit  missing '@param _cdpId', '@param _amount', '@param _upperHint', '@param _lowerHint'
 56:     function repayDebt(

 /// @audit  missing '@param _cdpId'
 63:     function closeCdp(bytes32 _cdpId) external;

 /// @audit  missing '@param _cdpId', '@param _stEthBalanceDecrease', '@param _debtChange', '@param isDebtIncrease', '@param _upperHint', '@param _lowerHint'
 65:     function adjustCdp(

 /// @audit  missing '@param _cdpId', '@param _stEthBalanceDecrease', '@param _debtChange', '@param isDebtIncrease', '@param _upperHint', '@param _lowerHint', '@param _stEthBalanceIncrease'
 74:     function adjustCdpWithColl(

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 /// @audit  missing '@param _index'
 13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

 /// @audit  missing '@param _cdpId'
 15:     function liquidate(bytes32 _cdpId) external;

 /// @audit  missing '@param _cdpId', '@param _partialAmount', '@param _upperPartialHint', '@param _lowerPartialHint'
 17:     function partiallyLiquidate(

 /// @audit  missing '@param _cdpArray'
 24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;

 /// @audit  missing '@param _EBTCAmount', '@param _firstRedemptionHint', '@param _upperPartialRedemptionHint', '@param _lowerPartialRedemptionHint', '@param _partialRedemptionHintNICR', '@param _maxIterations', '@param _maxFee'
 26:     function redeemCollateral(

 /// @audit  missing '@param _cdpId'
 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 /// @audit  missing '@param _cdpId'
 38:     function syncAccounting(bytes32 _cdpId) external;

 /// @audit  missing '@param _cdpId', '@param _borrower', '@param _debt', '@param _coll'
 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 /// @audit  missing '@param _stETHToRedeem'
 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 /// @audit  missing '@param _cdpId', '@param _debt', '@param _coll', '@param _liquidatorRewardShares', '@param _borrower'
 58:     function initializeCdp(

 /// @audit  missing '@param _cdpId', '@param _borrower', '@param _coll', '@param _debt', '@param _newColl', '@param _newDebt'
 66:     function updateCdp(

 /// @audit  missing '@param _price'
 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

 /// @audit  missing '@param _price'
 77:     function checkRecoveryMode(uint256 _price) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  missing '@param _newIndex', '@param _prevIndex'
 227:     function calcFeeUponStakingReward(

 /// @audit  missing '@param _cdpId', '@param _systemStEthFeePerUnitIndex'
 236:     function getAccumulatedFeeSplitApplied(

 /// @audit  missing '@param _cdpId'
 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId', '@param _price'
 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId', '@param _price'
 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  missing '@param _price'
 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@param _cdpId'
 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 /// @audit  missing '@param _cdpId'
 259:     function getSyncedDebtAndCollShares(

 /// @audit  missing '@param icr', '@param tcr'
 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 /// @audit  missing '@param _account'
 17:     function getSurplusCollShares(address _account) external view returns (uint256);

 /// @audit  missing '@param _account', '@param _amount'
 19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

 /// @audit  missing '@param _account'
 21:     function claimSurplusCollShares(address _account) external;

 /// @audit  missing '@param _value'
 23:     function increaseTotalSurplusCollShares(uint256 _value) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 /// @audit  missing '@param _account', '@param _amount'
 11:     function mint(address _account, uint256 _amount) external;

 /// @audit  missing '@param _account', '@param _amount'
 13:     function burn(address _account, uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 /// @audit  missing '@param newFallbackTimeout'
 21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 /// @audit  missing '@param owner'
 9:     function nonces(address owner) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 /// @audit  missing '@param _amount'
 19:     function increaseSystemDebt(uint256 _amount) external;

 /// @audit  missing '@param _amount'
 21:     function decreaseSystemDebt(uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 /// @audit  missing '@param _borrower', '@param _positionManager'
 18:     function getPositionManagerApproval(

 /// @audit  missing '@param _positionManager', '@param _approval'
 23:     function setPositionManagerApproval(

 /// @audit  missing '@param _positionManager'
 28:     function revokePositionManagerApproval(address _positionManager) external;

 /// @audit  missing '@param _borrower'
 30:     function renouncePositionManagerApproval(address _borrower) external;

 /// @audit  missing '@param _borrower', '@param _positionManager', '@param _approval', '@param _deadline', '@param v', '@param r', '@param s'
 32:     function permitPositionManagerApproval(

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 /// @audit  missing '@param tcr'
 13:     function notifyStartGracePeriod(uint256 tcr) external;

 /// @audit  missing '@param tcr'
 15:     function notifyEndGracePeriod(uint256 tcr) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 /// @audit  missing '@param _id'
 14:     function remove(bytes32 _id) external;

 /// @audit  missing '@param _ids'
 16:     function batchRemove(bytes32[] memory _ids) external;

 /// @audit  missing '@param _id', '@param _newICR', '@param _prevId', '@param _nextId'
 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 /// @audit  missing '@param _id'
 20:     function contains(bytes32 _id) external view returns (bool);

 /// @audit  missing '@param _id'
 34:     function getNext(bytes32 _id) external view returns (bytes32);

 /// @audit  missing '@param _id'
 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 /// @audit  missing '@param _ICR', '@param _prevId', '@param _nextId'
 38:     function validInsertPosition(

 /// @audit  missing '@param _ICR', '@param _prevId', '@param _nextId'
 44:     function findInsertPosition(

 /// @audit  missing '@param owner', '@param _ICR', '@param _prevId', '@param _nextId'
 50:     function insert(

 /// @audit  missing '@param _id'
 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 /// @audit  missing '@param owner'
 61:     function cdpCountOf(address owner) external view returns (uint256);

 /// @audit  missing '@param owner', '@param startNodeId', '@param maxNodes'
 63:     function getCdpCountOf(

 /// @audit  missing '@param owner'
 69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

 /// @audit  missing '@param owner', '@param startNodeId', '@param maxNodes'
 71:     function getAllCdpsOf(

 /// @audit  missing '@param owner', '@param index'
 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 /// @audit  missing '@param owner', '@param index', '@param startNodeId', '@param maxNodes'
 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  missing '@param _borrowerOperationsAddress', '@param _activePool', '@param _cdpManager', '@param _ebtc', '@param _coll', '@param _sortedCdps', '@param _sweepToCaller'
 51:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            bool _sweepToCaller
        ) {

 /// @audit  missing '@param flType', '@param borrowAmount', '@param operation', '@param postCheckType', '@param checkParams'
 118:     function doOperation(
             FlashLoanType flType,
             uint256 borrowAmount,
             LeverageMacroOperation calldata operation,
             PostOperationCheck postCheckType,
             PostCheckParams calldata checkParams
         ) external {

 /// @audit  missing '@param token', '@param amount'
 234:     function sweepToken(address token, uint256 amount) public {

 /// @audit  missing '@param check', '@param valueToCheck'
 244:     function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

 /// @audit  missing '@param operation'
 291:     function _handleOperation(LeverageMacroOperation memory operation) internal {

 /// @audit  missing '@param data'
 338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

 /// @audit  missing '@param initiator', '@param token', '@param amount', '@param fee', '@param data'
 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

 /// @audit  missing '@param swapData'
 382:     function _doSwaps(SwapOperation[] memory swapData) internal {

 /// @audit  missing '@param swapData'
 398:     function _doSwap(SwapOperation memory swapData) internal {

 /// @audit  missing '@param swapChecks'
 435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

 /// @audit  missing '@param addy'
 450:     function _ensureNotSystem(address addy) internal {

 /// @audit  missing '@param data'
 460:     function _openCdpCallback(bytes memory data) internal {

 /// @audit  missing '@param data'
 474:     function _closeCdpCallback(bytes memory data) internal {

 /// @audit  missing '@param data'
 482:     function _adjustCdpCallback(bytes memory data) internal {

 /// @audit  missing '@param _target', '@param _gas', '@param _value', '@param _maxCopy', '@param _calldata'
 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 /// @audit  missing '@param _borrowerOperationsAddress', '@param _activePool', '@param _cdpManager', '@param _ebtc', '@param _coll', '@param _sortedCdps'
 41:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                false // Do not sweep to caller
            )
        {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 /// @audit  missing '@param _borrowerOperationsAddress', '@param _activePool', '@param _cdpManager', '@param _ebtc', '@param _coll', '@param _sortedCdps'
 21:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        ) {

 /// @audit  missing '@param _owner'
 43:     function deployNewMacro(address _owner) public returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 /// @audit  missing '@param _borrowerOperationsAddress', '@param _activePool', '@param _cdpManager', '@param _ebtc', '@param _coll', '@param _sortedCdps', '@param _owner'
 17:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            address _owner
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                true // Sweep to caller since this is not supposed to hold funds
            )
        {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  missing '@param _borrowerOperationsAddress', '@param _collSurplusPool', '@param _ebtcToken', '@param _sortedCdps', '@param _activePool', '@param _priceFeed', '@param _collateral'
 14:     constructor(
            address _borrowerOperationsAddress,
            address _collSurplusPool,
            address _ebtcToken,
            address _sortedCdps,
            address _activePool,
            address _priceFeed,
            address _collateral
        )
            CdpManagerStorage(
                address(0),
                address(0),
                _borrowerOperationsAddress,
                _collSurplusPool,
                _ebtcToken,
                _sortedCdps,
                _activePool,
                _priceFeed,
                _collateral
            )
        {}

 /// @audit  missing '@param _cdpId', '@param _partialAmount', '@param _upperPartialHint', '@param _lowerPartialHint'
 61:     function _liquidateIndividualCdpSetup(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) internal {

 /// @audit  missing '@param _liqState', '@param _recoveryState'
 135:     function _liquidateIndividualCdpSetupCDP(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) internal {

 /// @audit  missing '@param _liqState', '@param _recoveryState'
 186:     function _liquidateCdpInGivenMode(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (uint256, uint256, uint256, uint256, uint256) {

 /// @audit  missing '@param _liqState'
 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(
             LiquidationLocals memory _liqState
         ) private returns (LiquidationLocals memory) {

 /// @audit  missing '@param _recoveryState'
 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (LiquidationRecoveryModeLocals memory) {

 /// @audit  missing '@param _cdpId'
 384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

 /// @audit  missing '@param _partialState'
 397:     function _liquidateCDPPartially(
             LiquidationLocals memory _partialState
         ) private returns (uint256, uint256) {

 /// @audit  missing '@param _cdpId', '@param _partialDebt', '@param _partialColl'
 450:     function _partiallyReduceCdpDebt(
             bytes32 _cdpId,
             uint256 _partialDebt,
             uint256 _partialColl
         ) internal {

 /// @audit  missing '@param _partialState', '@param _newNICR', '@param _oldDebt', '@param _oldColl'
 466:     function _reInsertPartialLiquidation(
             LiquidationLocals memory _partialState,
             uint256 _newNICR,
             uint256 _oldDebt,
             uint256 _oldColl
         ) internal {

 /// @audit  missing '@param totalDebtToBurn', '@param totalCollSharesToSend', '@param totalDebtToRedistribute', '@param totalLiquidatorRewardCollShares', '@param totalSurplusCollShares', '@param systemInitialCollShares', '@param systemInitialDebt', '@param price'
 503:     function _finalizeLiquidation(
             uint256 totalDebtToBurn,
             uint256 totalCollSharesToSend,
             uint256 totalDebtToRedistribute,
             uint256 totalLiquidatorRewardCollShares,
             uint256 totalSurplusCollShares,
             uint256 systemInitialCollShares,
             uint256 systemInitialDebt,
             uint256 price
         ) internal {

 /// @audit  missing '@param _ICR', '@param _price', '@param _totalDebtToBurn', '@param _totalColToSend'
 544:     function _calculatePartialLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 /// @audit  missing '@param _ICR', '@param _price', '@param _totalDebtToBurn', '@param _totalColToSend'
 570:     function _calculateFullLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 /// @audit  missing '@param _price', '@param _TCR', '@param vars', '@param singleLiquidation'
 608:     function _getLiquidationValuesNormalMode(
             uint256 _price,
             uint256 _TCR,
             LocalVariables_LiquidationSequence memory vars,
             LiquidationValues memory singleLiquidation
         ) internal {

 /// @audit  missing '@param _price', '@param _systemDebt', '@param _systemCollShares', '@param vars', '@param singleLiquidation'
 642:     function _getLiquidationValuesRecoveryMode(
             uint256 _price,
             uint256 _systemDebt,
             uint256 _systemCollShares,
             LocalVariables_LiquidationSequence memory vars,
             LiquidationValues memory singleLiquidation
         ) internal {

 /// @audit  missing '@param _price', '@param _systemCollShares', '@param _systemDebt', '@param _cdpArray'
 733:     function _getTotalFromBatchLiquidate_RecoveryMode(
             uint256 _price,
             uint256 _systemCollShares,
             uint256 _systemDebt,
             bytes32[] memory _cdpArray
         ) internal returns (LiquidationTotals memory totals) {

 /// @audit  missing '@param _price', '@param _TCR', '@param _cdpArray'
 807:     function _getTotalsFromBatchLiquidate_NormalMode(
             uint256 _price,
             uint256 _TCR,
             bytes32[] memory _cdpArray
         ) internal returns (LiquidationTotals memory totals) {

 /// @audit  missing '@param oldTotals', '@param singleLiquidation'
 839:     function _addLiquidationValuesToTotals(
             LiquidationTotals memory oldTotals,
             LiquidationValues memory singleLiquidation
         ) internal pure returns (LiquidationTotals memory newTotals) {

 /// @audit  missing '@param _debt'
 862:     function _redistributeDebt(uint256 _debt) internal {

 /// @audit  missing '@param _partialDebt', '@param _entireDebt', '@param _price'
 896:     function _requirePartialLiqDebtSize(
             uint256 _partialDebt,
             uint256 _entireDebt,
             uint256 _price
         ) internal view {

 /// @audit  missing '@param _entireColl'
 908:     function _requirePartialLiqCollSize(uint256 _entireColl) internal pure {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  missing '@param _response'
 465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

 /// @audit  missing '@param _timestamp', '@param _timeout'
 493:     function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {

 /// @audit  missing '@param _ethBtcAnswer', '@param _stEthEthAnswer', '@param _ethBtcDecimals', '@param _stEthEthDecimals'
 788:     function _formatClAggregateAnswer(
             int256 _ethBtcAnswer,
             int256 _stEthEthAnswer,
             uint8 _ethBtcDecimals,
             uint8 _stEthEthDecimals
         ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  missing '@param _owner'
 44:     constructor(address _owner) {

 /// @audit  missing '@param sig', '@param handler'
 51:     function setFallbackHandler(bytes4 sig, address handler) external {

 /// @audit  missing '@param allowNonCallbacks'
 66:     function setAllowAnyCall(bool allowNonCallbacks) external {

 /// @audit  missing '@param ops'
 110:     function execute(Operation[] calldata ops) external payable {

 /// @audit  missing '@param ds', '@param _enabled'
 129:     function _setCallbackEnabledForCall(DiamondLikeStorage storage ds, bool _enabled) internal {

 /// @audit  missing '@param op'
 134:     function _executeOne(Operation calldata op) internal {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  missing '@param owner'
 227:     function getCdpCountOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (uint256, bytes32) {

 /// @audit  missing '@param owner', '@param startNodeId', '@param maxNodes'
 237:     function _cdpCountOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) internal view returns (uint256, bytes32) {

 /// @audit  missing '@param owner'
 286:     function getAllCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32[] memory, uint256, bytes32) {

 /// @audit  missing '@param owner', '@param startNodeId', '@param maxNodes', '@param maxArraySize'
 299:     function _getCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes,
             uint maxArraySize
         ) internal view returns (bytes32[] memory, uint256, bytes32) {

 /// @audit  missing '@param _id', '@param _NICR', '@param _prevId', '@param _nextId'
 363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

 /// @audit  missing '@param _id'
 456:     function _remove(bytes32 _id) internal {

 /// @audit  missing '@param _NICR', '@param _prevId', '@param _nextId'
 591:     function _validInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bool) {

 /// @audit  missing '@param _NICR', '@param _prevId', '@param _nextId'
 674:     function _findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bytes32, bytes32) {

```

### <a name="NC-54"></a>[NC-54] NatSpec: Function `@return` tag is missing

 There are 167 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  missing '@return '
 439:     function _openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) internal returns (bytes32) {

 /// @audit  missing '@return '
 615:     function _getPositionManagerApproval(
             address _borrower,
             address _positionManager
         ) internal view returns (PositionManagerApproval) {

 /// @audit  missing '@return '
 673:     function _chainID() private view returns (uint256) {

 /// @audit  missing '@return '
 677:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 /// @audit  missing '@return collSharesChange', '@return isCollIncrease'
 744:     function _getCollSharesChangeFromStEthChange(
             uint256 _collReceived,
             uint256 _requestedCollWithdrawal
         ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

 /// @audit  missing '@return '
 986:     function _getNewNominalICRFromCdpChange(
             AdjustCdpLocals memory vars,
             bool _isDebtIncrease
         ) internal pure returns (uint256) {

 /// @audit  missing '@return '
 1004:     function _getNewICRFromCdpChange(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

 /// @audit  missing '@return ', '@return '
 1030:     function _getNewCdpAmounts(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease
          ) internal pure returns (uint256, uint256) {

 /// @audit  missing '@return '
 1049:     function _getNewTCRFromCdpChange(
              uint256 _stEthBalanceChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  missing '@return '
 272:     function _isValidFirstRedemptionHint(
             bytes32 _firstRedemptionHint,
             uint256 _price
         ) internal view returns (bool) {

 /// @audit  missing '@return '
 489:     function _getCdpIdsToRemove(
             bytes32 _start,
             uint256 _total,
             bytes32 _end
         ) internal view returns (bytes32[] memory) {
             uint256 _cnt = _total;

 /// @audit  missing '@return '
 523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {
             _requireCallerIsBorrowerOperations();

 /// @audit  missing '@return index'
 550:     function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
             /* Max array size is 2**128 - 1, i.e. ~3e30 cdps. No risk of overflow, since cdps have minimum EBTC

 /// @audit  missing '@return '
 595:     function _checkPotentialRecoveryMode(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (bool) {
             uint256 TCR = _computeTCRWithGivenSystemValues(_systemCollShares, _systemDebt, _price);

 /// @audit  missing '@return '
 612:     function _updateBaseRateFromRedemption(
             uint256 _ETHDrawn,
             uint256 _price,
             uint256 _totalEBTCSupply
         ) internal returns (uint256) {
             uint256 decayedBaseRate = _calcDecayedBaseRate();

 /// @audit  missing '@return '
 647:     function _calcRedemptionRate(uint256 _baseRate) internal view returns (uint256) {
             return

 /// @audit  missing '@return '
 655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {
             return _calcRedemptionFee(getRedemptionRate(), _ETHDrawn);

 /// @audit  missing '@return '
 667:     function _calcRedemptionFee(
             uint256 _redemptionRate,
             uint256 _ETHDrawn
         ) internal pure returns (uint256) {
             uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

 /// @audit  missing '@return '
 702:     function _calcDecayedBaseRate() internal view returns (uint256) {
             uint256 minutesPassed = _minutesPassedSinceLastRedemption();

 /// @audit  missing '@return '
 709:     function _minutesPassedSinceLastRedemption() internal view returns (uint256) {
             return

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  missing '@return pendingEBTCDebtReward', '@return _debtIndexDiff'
 304:     function _getPendingRedistributedDebt(
             bytes32 _cdpId
         ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

 /// @audit  missing '@return '
 327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

 /// @audit  missing '@return '
 419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

 /// @audit  missing '@return ', '@return '
 431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

 /// @audit  missing '@return '
 441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

 /// @audit  missing '@return '
 489:     function _computeTCRWithGivenSystemValues(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);

 /// @audit  missing '@return '
 707:     function _calculateCR(
             uint256 currentCollShare,
             uint256 currentDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);

 /// @audit  missing '@return '
 733:     function _getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) internal view returns (CdpDebtAndCollShares memory) {
             (uint256 entireDebt, uint256 entireColl) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  missing '@return '
 895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {
             // we have waited enough

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  missing '@return '
 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 /// @audit  missing '@return '
 22:     function authority() public view returns (Authority) {

 /// @audit  missing '@return '
 26:     function authorityInitialized() public view returns (bool) {

 /// @audit  missing '@return '
 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  missing '@return '
 60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

 /// @audit  missing '@return entireSystemColl'
 67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

 /// @audit  missing '@return entireSystemDebt'
 75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

 /// @audit  missing '@return TCR'
 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 /// @audit  missing '@return TCR', '@return _coll', '@return _debt'
 83:     function _getTCRWithSystemDebtAndCollShares(
            uint256 _price
        ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

 /// @audit  missing '@return '
 95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

 /// @audit  missing '@return '
 99:     function _checkRecoveryModeForTCR(uint256 _tcr) internal view returns (bool) {

 /// @audit  missing '@return '
 115:     function _convertDebtDenominationToBtc(
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {

 /// @audit  missing '@return '
 124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

 /// @audit  missing '@return '
 134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

 /// @audit  missing '@return '
 140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 /// @audit  missing '@return '
 20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a < _b) ? _a : _b;

 /// @audit  missing '@return '
 24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? _a : _b;

 /// @audit  missing '@return decProd'
 35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {
            uint256 prod_xy = x * y;

 /// @audit  missing '@return '
 59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {
            if (_minutes > 525600000) {

 /// @audit  missing '@return '
 88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? (_a - _b) : (_b - _a);

 /// @audit  missing '@return '
 92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {
            if (_debt > 0) {

 /// @audit  missing '@return '
 104:     function _computeCR(
             uint256 _stEthBalance,
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {
             if (_debt > 0) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  missing '@return '
 38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

 /// @audit  missing '@return '
 42:     function doesRoleHaveCapability(
            uint8 role,
            address target,
            bytes4 functionSig
        ) public view virtual returns (bool) {

 /// @audit  missing '@return '
 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

 /// @audit  missing '@return '
 63:     function canCall(
            address user,
            address target,
            bytes4 functionSig
        ) public view virtual override returns (bool) {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  missing '@return '
 111:     function totalSupply() external view override returns (uint256) {

 /// @audit  missing '@return '
 115:     function balanceOf(address account) external view override returns (uint256) {

 /// @audit  missing '@return '
 119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

 /// @audit  missing '@return '
 125:     function allowance(address owner, address spender) external view override returns (uint256) {

 /// @audit  missing '@return '
 129:     function approve(address spender, uint256 amount) external override returns (bool) {

 /// @audit  missing '@return '
 134:     function transferFrom(
             address sender,
             address recipient,
             uint256 amount
         ) external override returns (bool) {

 /// @audit  missing '@return '
 152:     function increaseAllowance(
             address spender,
             uint256 addedValue
         ) external override returns (bool) {

 /// @audit  missing '@return '
 160:     function decreaseAllowance(
             address spender,
             uint256 subtractedValue
         ) external override returns (bool) {

 /// @audit  missing '@return '
 225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

 /// @audit  missing '@return '
 231:     function _chainID() private view returns (uint256) {

 /// @audit  missing '@return '
 235:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  missing '@return hint', '@return diff', '@return latestRandomSeed'
 164:     function getApproxHint(
             uint256 _CR,
             uint256 _numTrials,
             uint256 _inputRandomSeed
         ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 /// @audit  missing '@return '
 37:     function feeRecipientAddress() external view returns (address);

 /// @audit  missing '@return '
 39:     function getFeeRecipientClaimableCollShares() external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 /// @audit  missing '@return '
 20:     function openCdp(

 /// @audit  missing '@return '
 27:     function openCdpFor(

 /// @audit  missing '@return '
 86:     function feeRecipientAddress() external view returns (address);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 /// @audit  missing '@return '
 11:     function getActiveCdpsCount() external view returns (uint256);

 /// @audit  missing '@return '
 13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

 /// @audit  missing '@return '
 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 /// @audit  missing '@return '
 42:     function getRedemptionRate() external view returns (uint256);

 /// @audit  missing '@return '
 44:     function getRedemptionRateWithDecay() external view returns (uint256);

 /// @audit  missing '@return '
 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

 /// @audit  missing '@return '
 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 /// @audit  missing '@return '
 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

 /// @audit  missing '@return '
 77:     function checkRecoveryMode(uint256 _price) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  missing '@return '
 217:     function totalStakes() external view returns (uint256);

 /// @audit  missing '@return '
 219:     function ebtcToken() external view returns (IEBTCToken);

 /// @audit  missing '@return '
 221:     function systemStEthFeePerUnitIndex() external view returns (uint256);

 /// @audit  missing '@return '
 223:     function systemStEthFeePerUnitIndexError() external view returns (uint256);

 /// @audit  missing '@return '
 225:     function stEthIndex() external view returns (uint256);

 /// @audit  missing '@return ', '@return ', '@return '
 227:     function calcFeeUponStakingReward(

 /// @audit  missing '@return ', '@return '
 236:     function getAccumulatedFeeSplitApplied(

 /// @audit  missing '@return '
 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  missing '@return '
 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  missing '@return '
 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 /// @audit  missing '@return '
 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  missing '@return '
 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 /// @audit  missing '@return debt', '@return collShares'
 259:     function getSyncedDebtAndCollShares(

 /// @audit  missing '@return '
 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 /// @audit  missing '@return '
 15:     function getTotalSurplusCollShares() external view returns (uint256);

 /// @audit  missing '@return '
 17:     function getSurplusCollShares(address _account) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 /// @audit  missing '@return '
 28:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 /// @audit  missing '@return '
 8:     function priceFeed() external view returns (IPriceFeed);

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 /// @audit  missing '@return ', '@return ', '@return '
 13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

 /// @audit  missing '@return '
 17:     function fallbackTimeout() external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 /// @audit  missing '@return '
 7:     function increasePermitNonce() external returns (uint256);

 /// @audit  missing '@return '
 9:     function nonces(address owner) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 /// @audit  missing '@return '
 15:     function getSystemCollShares() external view returns (uint256);

 /// @audit  missing '@return '
 17:     function getSystemDebt() external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 /// @audit  missing '@return '
 18:     function getPositionManagerApproval(

 /// @audit  missing '@return '
 42:     function version() external view returns (string memory);

 /// @audit  missing '@return '
 44:     function permitTypeHash() external view returns (bytes32);

 /// @audit  missing '@return '
 46:     function domainSeparator() external view returns (bytes32);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 /// @audit  missing '@return '
 43:     function fetchPrice() external returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 /// @audit  missing '@return '
 20:     function contains(bytes32 _id) external view returns (bool);

 /// @audit  missing '@return '
 22:     function isFull() external view returns (bool);

 /// @audit  missing '@return '
 24:     function isEmpty() external view returns (bool);

 /// @audit  missing '@return '
 26:     function getSize() external view returns (uint256);

 /// @audit  missing '@return '
 28:     function getMaxSize() external view returns (uint256);

 /// @audit  missing '@return '
 30:     function getFirst() external view returns (bytes32);

 /// @audit  missing '@return '
 32:     function getLast() external view returns (bytes32);

 /// @audit  missing '@return '
 34:     function getNext(bytes32 _id) external view returns (bytes32);

 /// @audit  missing '@return '
 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 /// @audit  missing '@return '
 38:     function validInsertPosition(

 /// @audit  missing '@return ', '@return '
 44:     function findInsertPosition(

 /// @audit  missing '@return '
 50:     function insert(

 /// @audit  missing '@return '
 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 /// @audit  missing '@return '
 59:     function nonExistId() external view returns (bytes32);

 /// @audit  missing '@return '
 61:     function cdpCountOf(address owner) external view returns (uint256);

 /// @audit  missing '@return ', '@return '
 63:     function getCdpCountOf(

 /// @audit  missing '@return '
 69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

 /// @audit  missing '@return ', '@return ', '@return '
 71:     function getAllCdpsOf(

 /// @audit  missing '@return '
 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 /// @audit  missing '@return ', '@return '
 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  missing '@return '
 15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

 /// @audit  missing '@return '
 39:     function owner() public virtual returns (address) {

 /// @audit  missing '@return '
 338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

 /// @audit  missing '@return '
 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

 /// @audit  missing '@return ', '@return '
 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 /// @audit  missing '@return '
 7:     function owner() external view returns (address);

 /// @audit  missing '@return '
 63:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 /// @audit  missing '@return '
 38:     function deployNewMacro() external returns (address) {

 /// @audit  missing '@return '
 43:     function deployNewMacro(address _owner) public returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 /// @audit  missing '@return '
 44:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  missing '@return ', '@return ', '@return ', '@return ', '@return '
 186:     function _liquidateCdpInGivenMode(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (uint256, uint256, uint256, uint256, uint256) {

 /// @audit  missing '@return '
 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(
             LiquidationLocals memory _liqState
         ) private returns (LiquidationLocals memory) {

 /// @audit  missing '@return '
 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (LiquidationRecoveryModeLocals memory) {

 /// @audit  missing '@return ', '@return ', '@return '
 384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

 /// @audit  missing '@return ', '@return '
 397:     function _liquidateCDPPartially(
             LiquidationLocals memory _partialState
         ) private returns (uint256, uint256) {

 /// @audit  missing '@return toLiquidator', '@return collSurplus', '@return debtToRedistribute'
 544:     function _calculatePartialLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 /// @audit  missing '@return toLiquidator', '@return collSurplus', '@return debtToRedistribute'
 570:     function _calculateFullLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 /// @audit  missing '@return totals'
 733:     function _getTotalFromBatchLiquidate_RecoveryMode(
             uint256 _price,
             uint256 _systemCollShares,
             uint256 _systemDebt,
             bytes32[] memory _cdpArray
         ) internal returns (LiquidationTotals memory totals) {

 /// @audit  missing '@return totals'
 807:     function _getTotalsFromBatchLiquidate_NormalMode(
             uint256 _price,
             uint256 _TCR,
             bytes32[] memory _cdpArray
         ) internal returns (LiquidationTotals memory totals) {

 /// @audit  missing '@return newTotals'
 839:     function _addLiquidationValuesToTotals(
             LiquidationTotals memory oldTotals,
             LiquidationValues memory singleLiquidation
         ) internal pure returns (LiquidationTotals memory newTotals) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  missing '@return '
 98:     function fetchPrice() external override returns (uint256) {

 /// @audit  missing '@return '
 465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

 /// @audit  missing '@return '
 493:     function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {

 /// @audit  missing '@return '
 788:     function _formatClAggregateAnswer(
             int256 _ethBtcAnswer,
             int256 _stEthEthAnswer,
             uint8 _ethBtcDecimals,
             uint8 _stEthEthDecimals
         ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  missing '@return ds'
 83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  missing '@return ', '@return '
 237:     function _cdpCountOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) internal view returns (uint256, bytes32) {

 /// @audit  missing '@return ', '@return ', '@return '
 299:     function _getCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes,
             uint maxArraySize
         ) internal view returns (bytes32[] memory, uint256, bytes32) {

 /// @audit  missing '@return '
 591:     function _validInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bool) {

 /// @audit  missing '@return ', '@return '
 674:     function _findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bytes32, bytes32) {

```

### <a name="NC-55"></a>[NC-55] NatSpec: Function declarations should have` @notice` tags
`@notice` is used to explain to end users what the function does, and the compiler interprets `///` or `/**` comments as this tag if one wasn’t explicitly provided

 There are 327 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 107:     constructor(
             address _cdpManagerAddress,
             address _activePoolAddress,
             address _collSurplusPoolAddress,
             address _priceFeedAddress,
             address _sortedCdpsAddress,
             address _ebtcTokenAddress,
             address _feeRecipientAddress,
             address _collTokenAddress
         ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) {

 328:     function _adjustCdpInternal(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) internal {

 439:     function _openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) internal returns (bytes32) {

 615:     function _getPositionManagerApproval(
             address _borrower,
             address _positionManager
         ) internal view returns (PositionManagerApproval) {

 635:     function _setPositionManagerApproval(
             address _borrower,
             address _positionManager,
             PositionManagerApproval _approval
         ) internal {

 673:     function _chainID() private view returns (uint256) {

 677:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 744:     function _getCollSharesChangeFromStEthChange(
             uint256 _collReceived,
             uint256 _requestedCollWithdrawal
         ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

 790:     function _withdrawDebt(address _account, uint256 _debt) internal {

 796:     function _repayDebt(address _account, uint256 _debt) internal {

 803:     function _requireSingularCollChange(
             uint256 _stEthBalanceIncrease,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 813:     function _requireNonZeroAdjustment(
             uint256 _stEthBalanceIncrease,
             uint256 _debtChange,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {

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

 910:     function _requireICRisNotBelowMCR(uint256 _newICR) internal pure {

 917:     function _requireICRisNotBelowCCR(uint256 _newICR) internal pure {

 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 928:     function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure {

 935:     function _requireNonZeroDebt(uint256 _debt) internal pure {

 939:     function _requireAtLeastMinNetStEthBalance(uint256 _stEthBalance) internal pure {

 946:     function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

 953:     function _requireSufficientEbtcTokenBalance(
             address _account,
             uint256 _debtRepayment
         ) internal view {

 963:     function _requireBorrowerOrPositionManagerAndUpdateManagerApproval(address _borrower) internal {

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

 1030:     function _getNewCdpAmounts(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease
          ) internal pure returns (uint256, uint256) {

 1049:     function _getNewTCRFromCdpChange(
              uint256 _stEthBalanceChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 244:     function _closeCdpByRedemption(
             bytes32 _cdpId,
             uint256 _EBTC,
             uint256 _collSurplus,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) internal {

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

 638:     function getRedemptionRate() public view override returns (uint256) {
             return _calcRedemptionRate(baseRate);

 643:     function getRedemptionRateWithDecay() public view override returns (uint256) {
             return _calcRedemptionRate(_calcDecayedBaseRate());

 647:     function _calcRedemptionRate(uint256 _baseRate) internal view returns (uint256) {
             return

 655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {
             return _calcRedemptionFee(getRedemptionRate(), _ETHDrawn);

 661:     function getRedemptionFeeWithDecay(
             uint256 _stETHToRedeem
         ) external view override returns (uint256) {
             return _calcRedemptionFee(getRedemptionRateWithDecay(), _stETHToRedeem);

 667:     function _calcRedemptionFee(
             uint256 _redemptionRate,
             uint256 _ETHDrawn
         ) internal pure returns (uint256) {
             uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

 676:     function _decayBaseRate() internal {
             uint256 decayedBaseRate = _calcDecayedBaseRate();

 689:     function _updateLastRedemptionTimestamp() internal {
             uint256 timePassed = block.timestamp > lastRedemptionTimestamp

 702:     function _calcDecayedBaseRate() internal view returns (uint256) {
             uint256 minutesPassed = _minutesPassedSinceLastRedemption();

 709:     function _minutesPassedSinceLastRedemption() internal view returns (uint256) {
             return

 717:     function getDeploymentStartTime() public view returns (uint256) {
             return deploymentStartTime;

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

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 49:     function _startGracePeriod(uint256 _tcr) internal {

 73:     function _syncGracePeriod() internal {

 87:     function _syncGracePeriodForGivenValues(
            uint256 systemCollShares,
            uint256 systemDebt,
            uint256 price
        ) internal {

 255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {

 260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

 293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

 304:     function _getPendingRedistributedDebt(
             bytes32 _cdpId
         ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

 327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

 336:     function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

 344:     function _syncAccounting(bytes32 _cdpId) internal {

 410:     function _removeStake(bytes32 _cdpId) internal {

 419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

 431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

 441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

 463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
             Status cdpStatus = Cdps[_cdpId].status;

 489:     function _computeTCRWithGivenSystemValues(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);

 509:     function _syncGlobalAccounting() internal {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 534:     function _readStEthIndex() internal view returns (uint256, uint256) {
             return (stEthIndex, collateral.getPooledEthByShares(DECIMAL_PRECISION));

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

 648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {
             require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

 652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {
             require(

 659:     function _requireCallerIsBorrowerOperations() internal view {
             require(

 707:     function _calculateCR(
             uint256 currentCollShare,
             uint256 currentDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);

 728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {
             return _hasRedistributedDebt(_cdpId);

 733:     function _getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) internal view returns (CdpDebtAndCollShares memory) {
             (uint256 entireDebt, uint256 entireColl) = getSyncedDebtAndCollShares(_cdpId);

 761:     function _calcSyncedGlobalAccounting(
             uint256 _newIndex,
             uint256 _oldIndex
         ) internal view returns (uint256, uint256, uint256) {
             if (_newIndex > _oldIndex && totalStakes > 0) {

 787:     function _calcSyncedAccounting(
             bytes32 _cdpId,
             uint256 _cdpPerUnitIdx,
             uint256 _systemStEthFeePerUnitIndex
         ) internal view returns (uint256, uint256, uint256, uint256, uint256) {
             uint256 _feeSplitApplied;

 822:     function _getSyncedCdpDebtAndRedistribution(
             bytes32 _cdpId
         ) internal view returns (uint256, uint256, uint256) {
             (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(

 890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {
             return _checkICRAgainstTCR(icr, tcr) && _recoveryModeGracePeriodPassed();

 895:     function _recoveryModeGracePeriodPassed() internal view returns (bool) {
             // we have waited enough

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 61:     function getTotalSurplusCollShares() external view override returns (uint256) {

 67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

 112:     function _requireCallerIsBorrowerOperations() internal view {

 119:     function _requireCallerIsCdpManager() internal view {

 123:     function _requireCallerIsActivePool() internal view {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 18:     constructor(address _owner, Authority _authority) {

 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

 42:     function setAuthority(Authority newAuthority) public virtual {

 52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 22:     function authority() public view returns (Authority) {

 26:     function authorityInitialized() public view returns (bool) {

 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

 38:     function setAuthority(address newAuthority) public virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 83:     function _getTCRWithSystemDebtAndCollShares(
            uint256 _price
        ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

 95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

 99:     function _checkRecoveryModeForTCR(uint256 _tcr) internal view returns (bool) {

 103:     function _requireUserAcceptsFee(
             uint256 _fee,
             uint256 _amount,
             uint256 _maxFeePercentage
         ) internal pure {

 115:     function _convertDebtDenominationToBtc(
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {

 124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

 134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

 140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a < _b) ? _a : _b;

 24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? _a : _b;

 35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {
            uint256 prod_xy = x * y;

 59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {
            if (_minutes > 525600000) {

 88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? (_a - _b) : (_b - _a);

 92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {
            if (_debt > 0) {

 104:     function _computeCR(
             uint256 _stEthBalance,
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {
             if (_debt > 0) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

 38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

 42:     function doesRoleHaveCapability(
            uint8 role,
            address target,
            bytes4 functionSig
        ) public view virtual returns (bool) {

 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

 147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 61:     constructor(
            address _cdpManagerAddress,
            address _borrowerOperationsAddress,
            address _authorityAddress
        ) {

 111:     function totalSupply() external view override returns (uint256) {

 115:     function balanceOf(address account) external view override returns (uint256) {

 119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

 125:     function allowance(address owner, address spender) external view override returns (uint256) {

 129:     function approve(address spender, uint256 amount) external override returns (bool) {

 134:     function transferFrom(
             address sender,
             address recipient,
             uint256 amount
         ) external override returns (bool) {

 152:     function increaseAllowance(
             address spender,
             uint256 addedValue
         ) external override returns (bool) {

 160:     function decreaseAllowance(
             address spender,
             uint256 subtractedValue
         ) external override returns (bool) {

 225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

 231:     function _chainID() private view returns (uint256) {

 235:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 246:     function _transfer(address sender, address recipient, uint256 amount) internal {

 262:     function _mint(address account, uint256 amount) internal {

 270:     function _burn(address account, uint256 amount) internal {

 285:     function _approve(address owner, address spender, uint256 amount) internal {

 295:     function _requireValidRecipient(address _recipient) internal view {

 306:     function _requireCallerIsBorrowerOperations() internal view {

 314:     function _requireCallerIsBOorCdpMOrAuth() internal view {

 323:     function _requireCallerIsCdpM() internal view {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 27:     constructor(
            address _sortedCdpsAddress,
            address _cdpManagerAddress,
            address _collateralAddress,
            address _activePoolAddress,
            address _priceFeedAddress
        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {

 164:     function getApproxHint(
             uint256 _CR,
             uint256 _numTrials,
             uint256 _inputRandomSeed
         ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 23:     function transferSystemCollShares(address _account, uint256 _amount) external;

 25:     function increaseSystemCollShares(uint256 _value) external;

 27:     function transferSystemCollSharesAndLiquidatorReward(

 33:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;

 35:     function claimFeeRecipientCollShares(uint256 _shares) external;

 37:     function feeRecipientAddress() external view returns (address);

 39:     function getFeeRecipientClaimableCollShares() external view returns (uint256);

 41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 20:     function openCdp(

 27:     function openCdpFor(

 35:     function addColl(

 42:     function withdrawColl(

 49:     function withdrawDebt(

 56:     function repayDebt(

 63:     function closeCdp(bytes32 _cdpId) external;

 65:     function adjustCdp(

 74:     function adjustCdpWithColl(

 84:     function claimSurplusCollShares() external;

 86:     function feeRecipientAddress() external view returns (address);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 11:     function getActiveCdpsCount() external view returns (uint256);

 13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

 15:     function liquidate(bytes32 _cdpId) external;

 17:     function partiallyLiquidate(

 24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;

 26:     function redeemCollateral(

 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 38:     function syncAccounting(bytes32 _cdpId) external;

 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 42:     function getRedemptionRate() external view returns (uint256);

 44:     function getRedemptionRateWithDecay() external view returns (uint256);

 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 58:     function initializeCdp(

 66:     function updateCdp(

 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

 77:     function checkRecoveryMode(uint256 _price) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 217:     function totalStakes() external view returns (uint256);

 219:     function ebtcToken() external view returns (IEBTCToken);

 221:     function systemStEthFeePerUnitIndex() external view returns (uint256);

 223:     function systemStEthFeePerUnitIndexError() external view returns (uint256);

 225:     function stEthIndex() external view returns (uint256);

 227:     function calcFeeUponStakingReward(

 232:     function syncGlobalAccounting() external; // Accrues StEthFeeSplit without influencing Grace Period

 234:     function syncGlobalAccountingAndGracePeriod() external; // Accrues StEthFeeSplit and influences Grace Period

 236:     function getAccumulatedFeeSplitApplied(

 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 259:     function getSyncedDebtAndCollShares(

 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 15:     function getTotalSurplusCollShares() external view returns (uint256);

 17:     function getSurplusCollShares(address _account) external view returns (uint256);

 19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

 21:     function claimSurplusCollShares(address _account) external;

 23:     function increaseTotalSurplusCollShares(uint256 _value) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 11:     function mint(address _account, uint256 _amount) external;

 13:     function burn(address _account, uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 15:     function onFlashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 15:     function maxFlashLoan(address token) external view returns (uint256);

 21:     function flashFee(address token, uint256 amount) external view returns (uint256);

 28:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 8:     function priceFeed() external view returns (IPriceFeed);

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

 17:     function fallbackTimeout() external view returns (uint256);

 21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 7:     function increasePermitNonce() external returns (uint256);

 9:     function nonces(address owner) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 15:     function getSystemCollShares() external view returns (uint256);

 17:     function getSystemDebt() external view returns (uint256);

 19:     function increaseSystemDebt(uint256 _amount) external;

 21:     function decreaseSystemDebt(uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 18:     function getPositionManagerApproval(

 23:     function setPositionManagerApproval(

 28:     function revokePositionManagerApproval(address _positionManager) external;

 30:     function renouncePositionManagerApproval(address _borrower) external;

 32:     function permitPositionManagerApproval(

 42:     function version() external view returns (string memory);

 44:     function permitTypeHash() external view returns (bytes32);

 46:     function domainSeparator() external view returns (bytes32);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 43:     function fetchPrice() external returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 13:     function notifyStartGracePeriod(uint256 tcr) external;

 15:     function notifyEndGracePeriod(uint256 tcr) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 14:     function remove(bytes32 _id) external;

 16:     function batchRemove(bytes32[] memory _ids) external;

 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 20:     function contains(bytes32 _id) external view returns (bool);

 22:     function isFull() external view returns (bool);

 24:     function isEmpty() external view returns (bool);

 26:     function getSize() external view returns (uint256);

 28:     function getMaxSize() external view returns (uint256);

 30:     function getFirst() external view returns (bytes32);

 32:     function getLast() external view returns (bytes32);

 34:     function getNext(bytes32 _id) external view returns (bytes32);

 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 38:     function validInsertPosition(

 44:     function findInsertPosition(

 50:     function insert(

 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 59:     function nonExistId() external view returns (bytes32);

 61:     function cdpCountOf(address owner) external view returns (uint256);

 63:     function getCdpCountOf(

 69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

 71:     function getAllCdpsOf(

 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

 39:     function owner() public virtual returns (address) {

 43:     function _assertOwner() internal {

 51:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            bool _sweepToCaller
        ) {

 244:     function _doCheckValueType(CheckValueAndType memory check, uint256 valueToCheck) internal {

 291:     function _handleOperation(LeverageMacroOperation memory operation) internal {

 382:     function _doSwaps(SwapOperation[] memory swapData) internal {

 398:     function _doSwap(SwapOperation memory swapData) internal {

 435:     function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

 450:     function _ensureNotSystem(address addy) internal {

 460:     function _openCdpCallback(bytes memory data) internal {

 474:     function _closeCdpCallback(bytes memory data) internal {

 482:     function _adjustCdpCallback(bytes memory data) internal {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 7:     function owner() external view returns (address);

 41:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                false // Do not sweep to caller
            )
        {

 63:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 21:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        ) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 17:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            address _owner
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                true // Sweep to caller since this is not supposed to hold funds
            )
        {

 44:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 14:     constructor(
            address _borrowerOperationsAddress,
            address _collSurplusPool,
            address _ebtcToken,
            address _sortedCdps,
            address _activePool,
            address _priceFeed,
            address _collateral
        )
            CdpManagerStorage(
                address(0),
                address(0),
                _borrowerOperationsAddress,
                _collSurplusPool,
                _ebtcToken,
                _sortedCdps,
                _activePool,
                _priceFeed,
                _collateral
            )
        {}

 61:     function _liquidateIndividualCdpSetup(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) internal {

 135:     function _liquidateIndividualCdpSetupCDP(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) internal {

 186:     function _liquidateCdpInGivenMode(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (uint256, uint256, uint256, uint256, uint256) {

 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(
             LiquidationLocals memory _liqState
         ) private returns (LiquidationLocals memory) {

 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (LiquidationRecoveryModeLocals memory) {

 384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

 397:     function _liquidateCDPPartially(
             LiquidationLocals memory _partialState
         ) private returns (uint256, uint256) {

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

 503:     function _finalizeLiquidation(
             uint256 totalDebtToBurn,
             uint256 totalCollSharesToSend,
             uint256 totalDebtToRedistribute,
             uint256 totalLiquidatorRewardCollShares,
             uint256 totalSurplusCollShares,
             uint256 systemInitialCollShares,
             uint256 systemInitialDebt,
             uint256 price
         ) internal {

 544:     function _calculatePartialLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 570:     function _calculateFullLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 608:     function _getLiquidationValuesNormalMode(
             uint256 _price,
             uint256 _TCR,
             LocalVariables_LiquidationSequence memory vars,
             LiquidationValues memory singleLiquidation
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

 839:     function _addLiquidationValuesToTotals(
             LiquidationTotals memory oldTotals,
             LiquidationValues memory singleLiquidation
         ) internal pure returns (LiquidationTotals memory newTotals) {

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

 465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

 493:     function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {

 788:     function _formatClAggregateAnswer(
             int256 _ethBtcAnswer,
             int256 _stEthEthAnswer,
             uint8 _ethBtcDecimals,
             uint8 _stEthEthDecimals
         ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 44:     constructor(address _owner) {

 83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

 129:     function _setCallbackEnabledForCall(DiamondLikeStorage storage ds, bool _enabled) internal {

 134:     function _executeOne(Operation calldata op) internal {

 160:     receive() external payable {

 164:     fallback() external payable {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 155:     function cdpOfOwnerByIdx(
             address owner,
             uint256 index,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32, bool) {

 237:     function _cdpCountOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) internal view returns (uint256, bytes32) {

 286:     function getAllCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32[] memory, uint256, bytes32) {

 299:     function _getCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes,
             uint maxArraySize
         ) internal view returns (bytes32[] memory, uint256, bytes32) {

 363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

 456:     function _remove(bytes32 _id) internal {

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
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bool) {

 591:     function _validInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bool) {

 619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

 642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

 666:     function findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bytes32, bytes32) {

 674:     function _findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bytes32, bytes32) {

 714:     function _requireCallerIsCdpManager() internal view {

 719:     function _requireCallerIsBOorCdpM() internal view {

```

### <a name="NC-56"></a>[NC-56] NatSpec: Function declarations should have descriptions

 There are 275 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 107:     constructor(
             address _cdpManagerAddress,
             address _activePoolAddress,
             address _collSurplusPoolAddress,
             address _priceFeedAddress,
             address _sortedCdpsAddress,
             address _ebtcTokenAddress,
             address _feeRecipientAddress,
             address _collTokenAddress
         ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collTokenAddress) {

 328:     function _adjustCdpInternal(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) internal {

 439:     function _openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) internal returns (bytes32) {

 615:     function _getPositionManagerApproval(
             address _borrower,
             address _positionManager
         ) internal view returns (PositionManagerApproval) {

 635:     function _setPositionManagerApproval(
             address _borrower,
             address _positionManager,
             PositionManagerApproval _approval
         ) internal {

 673:     function _chainID() private view returns (uint256) {

 677:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 744:     function _getCollSharesChangeFromStEthChange(
             uint256 _collReceived,
             uint256 _requestedCollWithdrawal
         ) internal view returns (uint256 collSharesChange, bool isCollIncrease) {

 796:     function _repayDebt(address _account, uint256 _debt) internal {

 803:     function _requireSingularCollChange(
             uint256 _stEthBalanceIncrease,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 813:     function _requireNonZeroAdjustment(
             uint256 _stEthBalanceIncrease,
             uint256 _debtChange,
             uint256 _stEthBalanceDecrease
         ) internal pure {

 824:     function _requireCdpisActive(ICdpManager _cdpManager, bytes32 _cdpId) internal view {

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

 910:     function _requireICRisNotBelowMCR(uint256 _newICR) internal pure {

 917:     function _requireICRisNotBelowCCR(uint256 _newICR) internal pure {

 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 928:     function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure {

 935:     function _requireNonZeroDebt(uint256 _debt) internal pure {

 939:     function _requireAtLeastMinNetStEthBalance(uint256 _stEthBalance) internal pure {

 946:     function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

 953:     function _requireSufficientEbtcTokenBalance(
             address _account,
             uint256 _debtRepayment
         ) internal view {

 963:     function _requireBorrowerOrPositionManagerAndUpdateManagerApproval(address _borrower) internal {

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

 1030:     function _getNewCdpAmounts(
              uint256 _collShares,
              uint256 _debt,
              uint256 _collSharesChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease
          ) internal pure returns (uint256, uint256) {

 1049:     function _getNewTCRFromCdpChange(
              uint256 _stEthBalanceChange,
              bool _isCollIncrease,
              uint256 _debtChange,
              bool _isDebtIncrease,
              uint256 _price
          ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 244:     function _closeCdpByRedemption(
             bytes32 _cdpId,
             uint256 _EBTC,
             uint256 _collSurplus,
             uint256 _liquidatorRewardShares,
             address _borrower
         ) internal {

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

 638:     function getRedemptionRate() public view override returns (uint256) {
             return _calcRedemptionRate(baseRate);

 643:     function getRedemptionRateWithDecay() public view override returns (uint256) {
             return _calcRedemptionRate(_calcDecayedBaseRate());

 647:     function _calcRedemptionRate(uint256 _baseRate) internal view returns (uint256) {
             return

 655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {
             return _calcRedemptionFee(getRedemptionRate(), _ETHDrawn);

 661:     function getRedemptionFeeWithDecay(
             uint256 _stETHToRedeem
         ) external view override returns (uint256) {
             return _calcRedemptionFee(getRedemptionRateWithDecay(), _stETHToRedeem);

 667:     function _calcRedemptionFee(
             uint256 _redemptionRate,
             uint256 _ETHDrawn
         ) internal pure returns (uint256) {
             uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;

 676:     function _decayBaseRate() internal {
             uint256 decayedBaseRate = _calcDecayedBaseRate();

 689:     function _updateLastRedemptionTimestamp() internal {
             uint256 timePassed = block.timestamp > lastRedemptionTimestamp

 702:     function _calcDecayedBaseRate() internal view returns (uint256) {
             uint256 minutesPassed = _minutesPassedSinceLastRedemption();

 709:     function _minutesPassedSinceLastRedemption() internal view returns (uint256) {
             return

 717:     function getDeploymentStartTime() public view returns (uint256) {
             return deploymentStartTime;

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

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 73:     function _syncGracePeriod() internal {

 255:     function _closeCdp(bytes32 _cdpId, Status closedStatus) internal {

 260:     function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

 293:     function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

 327:     function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

 410:     function _removeStake(bytes32 _cdpId) internal {

 419:     function _updateStakeAndTotalStakes(bytes32 _cdpId) internal returns (uint256) {

 431:     function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

 441:     function _computeNewStake(uint256 _coll) internal view returns (uint256) {

 463:     function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {
             Status cdpStatus = Cdps[_cdpId].status;

 489:     function _computeTCRWithGivenSystemValues(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);

 509:     function _syncGlobalAccounting() internal {
             (uint256 _oldIndex, uint256 _newIndex) = _readStEthIndex();

 534:     function _readStEthIndex() internal view returns (uint256, uint256) {
             return (stEthIndex, collateral.getPooledEthByShares(DECIMAL_PRECISION));

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

 648:     function _requireCdpIsActive(bytes32 _cdpId) internal view {
             require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

 652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {
             require(

 659:     function _requireCallerIsBorrowerOperations() internal view {
             require(

 707:     function _calculateCR(
             uint256 currentCollShare,
             uint256 currentDebt,
             uint256 _price
         ) internal view returns (uint256) {
             uint256 _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare);

 728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {
             return _hasRedistributedDebt(_cdpId);

 733:     function _getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) internal view returns (CdpDebtAndCollShares memory) {
             (uint256 entireDebt, uint256 entireColl) = getSyncedDebtAndCollShares(_cdpId);

 822:     function _getSyncedCdpDebtAndRedistribution(
             bytes32 _cdpId
         ) internal view returns (uint256, uint256, uint256) {
             (uint256 pendingDebtRedistributed, uint256 _debtIndexDelta) = _getPendingRedistributedDebt(

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 61:     function getTotalSurplusCollShares() external view override returns (uint256) {

 67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

 112:     function _requireCallerIsBorrowerOperations() internal view {

 119:     function _requireCallerIsCdpManager() internal view {

 123:     function _requireCallerIsActivePool() internal view {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 18:     constructor(address _owner, Authority _authority) {

 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

 42:     function setAuthority(Authority newAuthority) public virtual {

 52:     function transferOwnership(address newOwner) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 22:     function authority() public view returns (Authority) {

 26:     function authorityInitialized() public view returns (bool) {

 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

 38:     function setAuthority(address newAuthority) public virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 83:     function _getTCRWithSystemDebtAndCollShares(
            uint256 _price
        ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

 95:     function _checkRecoveryMode(uint256 _price) internal view returns (bool) {

 99:     function _checkRecoveryModeForTCR(uint256 _tcr) internal view returns (bool) {

 103:     function _requireUserAcceptsFee(
             uint256 _fee,
             uint256 _amount,
             uint256 _maxFeePercentage
         ) internal pure {

 115:     function _convertDebtDenominationToBtc(
             uint256 _debt,
             uint256 _price
         ) internal pure returns (uint256) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 20:     function _min(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a < _b) ? _a : _b;

 24:     function _max(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? _a : _b;

 35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {
            uint256 prod_xy = x * y;

 59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {
            if (_minutes > 525600000) {

 88:     function _getAbsoluteDifference(uint256 _a, uint256 _b) internal pure returns (uint256) {
            return (_a >= _b) ? (_a - _b) : (_b - _a);

 92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {
            if (_debt > 0) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 20:     constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}

 38:     function doesUserHaveRole(address user, uint8 role) public view virtual returns (bool) {

 42:     function doesRoleHaveCapability(
            uint8 role,
            address target,
            bytes4 functionSig
        ) public view virtual returns (bool) {

 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

 147:     function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 61:     constructor(
            address _cdpManagerAddress,
            address _borrowerOperationsAddress,
            address _authorityAddress
        ) {

 111:     function totalSupply() external view override returns (uint256) {

 115:     function balanceOf(address account) external view override returns (uint256) {

 119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

 125:     function allowance(address owner, address spender) external view override returns (uint256) {

 129:     function approve(address spender, uint256 amount) external override returns (bool) {

 134:     function transferFrom(
             address sender,
             address recipient,
             uint256 amount
         ) external override returns (bool) {

 152:     function increaseAllowance(
             address spender,
             uint256 addedValue
         ) external override returns (bool) {

 160:     function decreaseAllowance(
             address spender,
             uint256 subtractedValue
         ) external override returns (bool) {

 231:     function _chainID() private view returns (uint256) {

 235:     function _buildDomainSeparator(
             bytes32 typeHash,
             bytes32 name,
             bytes32 version
         ) private view returns (bytes32) {

 246:     function _transfer(address sender, address recipient, uint256 amount) internal {

 262:     function _mint(address account, uint256 amount) internal {

 270:     function _burn(address account, uint256 amount) internal {

 285:     function _approve(address owner, address spender, uint256 amount) internal {

 295:     function _requireValidRecipient(address _recipient) internal view {

 306:     function _requireCallerIsBorrowerOperations() internal view {

 323:     function _requireCallerIsCdpM() internal view {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 27:     constructor(
            address _sortedCdpsAddress,
            address _cdpManagerAddress,
            address _collateralAddress,
            address _activePoolAddress,
            address _priceFeedAddress
        ) EbtcBase(_activePoolAddress, _priceFeedAddress, _collateralAddress) {

 164:     function getApproxHint(
             uint256 _CR,
             uint256 _numTrials,
             uint256 _inputRandomSeed
         ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 23:     function transferSystemCollShares(address _account, uint256 _amount) external;

 25:     function increaseSystemCollShares(uint256 _value) external;

 27:     function transferSystemCollSharesAndLiquidatorReward(

 33:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;

 35:     function claimFeeRecipientCollShares(uint256 _shares) external;

 37:     function feeRecipientAddress() external view returns (address);

 39:     function getFeeRecipientClaimableCollShares() external view returns (uint256);

 41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 20:     function openCdp(

 27:     function openCdpFor(

 35:     function addColl(

 42:     function withdrawColl(

 49:     function withdrawDebt(

 56:     function repayDebt(

 63:     function closeCdp(bytes32 _cdpId) external;

 65:     function adjustCdp(

 74:     function adjustCdpWithColl(

 84:     function claimSurplusCollShares() external;

 86:     function feeRecipientAddress() external view returns (address);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 11:     function getActiveCdpsCount() external view returns (uint256);

 13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

 15:     function liquidate(bytes32 _cdpId) external;

 17:     function partiallyLiquidate(

 24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;

 26:     function redeemCollateral(

 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 38:     function syncAccounting(bytes32 _cdpId) external;

 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 42:     function getRedemptionRate() external view returns (uint256);

 44:     function getRedemptionRateWithDecay() external view returns (uint256);

 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 58:     function initializeCdp(

 66:     function updateCdp(

 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

 77:     function checkRecoveryMode(uint256 _price) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 217:     function totalStakes() external view returns (uint256);

 219:     function ebtcToken() external view returns (IEBTCToken);

 221:     function systemStEthFeePerUnitIndex() external view returns (uint256);

 223:     function systemStEthFeePerUnitIndexError() external view returns (uint256);

 225:     function stEthIndex() external view returns (uint256);

 227:     function calcFeeUponStakingReward(

 232:     function syncGlobalAccounting() external; // Accrues StEthFeeSplit without influencing Grace Period

 234:     function syncGlobalAccountingAndGracePeriod() external; // Accrues StEthFeeSplit and influences Grace Period

 236:     function getAccumulatedFeeSplitApplied(

 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 259:     function getSyncedDebtAndCollShares(

 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 15:     function getTotalSurplusCollShares() external view returns (uint256);

 17:     function getSurplusCollShares(address _account) external view returns (uint256);

 19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

 21:     function claimSurplusCollShares(address _account) external;

 23:     function increaseTotalSurplusCollShares(uint256 _value) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 11:     function mint(address _account, uint256 _amount) external;

 13:     function burn(address _account, uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEbtcBase.sol

 8:     function priceFeed() external view returns (IPriceFeed);

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 13:     function getFallbackResponse() external view returns (uint256, uint256, bool);

 17:     function fallbackTimeout() external view returns (uint256);

 21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 7:     function increasePermitNonce() external returns (uint256);

 9:     function nonces(address owner) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 15:     function getSystemCollShares() external view returns (uint256);

 17:     function getSystemDebt() external view returns (uint256);

 19:     function increaseSystemDebt(uint256 _amount) external;

 21:     function decreaseSystemDebt(uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 18:     function getPositionManagerApproval(

 23:     function setPositionManagerApproval(

 28:     function revokePositionManagerApproval(address _positionManager) external;

 30:     function renouncePositionManagerApproval(address _borrower) external;

 32:     function permitPositionManagerApproval(

 42:     function version() external view returns (string memory);

 44:     function permitTypeHash() external view returns (bytes32);

 46:     function domainSeparator() external view returns (bytes32);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 43:     function fetchPrice() external returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 13:     function notifyStartGracePeriod(uint256 tcr) external;

 15:     function notifyEndGracePeriod(uint256 tcr) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 14:     function remove(bytes32 _id) external;

 16:     function batchRemove(bytes32[] memory _ids) external;

 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 20:     function contains(bytes32 _id) external view returns (bool);

 22:     function isFull() external view returns (bool);

 24:     function isEmpty() external view returns (bool);

 26:     function getSize() external view returns (uint256);

 28:     function getMaxSize() external view returns (uint256);

 30:     function getFirst() external view returns (bytes32);

 32:     function getLast() external view returns (bytes32);

 34:     function getNext(bytes32 _id) external view returns (bytes32);

 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 38:     function validInsertPosition(

 44:     function findInsertPosition(

 50:     function insert(

 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 59:     function nonExistId() external view returns (bytes32);

 61:     function cdpCountOf(address owner) external view returns (uint256);

 63:     function getCdpCountOf(

 69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

 71:     function getAllCdpsOf(

 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

 39:     function owner() public virtual returns (address) {

 43:     function _assertOwner() internal {

 51:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            bool _sweepToCaller
        ) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 7:     function owner() external view returns (address);

 41:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                false // Do not sweep to caller
            )
        {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 21:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        ) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 17:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            address _owner
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                true // Sweep to caller since this is not supposed to hold funds
            )
        {

 44:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 14:     constructor(
            address _borrowerOperationsAddress,
            address _collSurplusPool,
            address _ebtcToken,
            address _sortedCdps,
            address _activePool,
            address _priceFeed,
            address _collateral
        )
            CdpManagerStorage(
                address(0),
                address(0),
                _borrowerOperationsAddress,
                _collSurplusPool,
                _ebtcToken,
                _sortedCdps,
                _activePool,
                _priceFeed,
                _collateral
            )
        {}

 61:     function _liquidateIndividualCdpSetup(
            bytes32 _cdpId,
            uint256 _partialAmount,
            bytes32 _upperPartialHint,
            bytes32 _lowerPartialHint
        ) internal {

 135:     function _liquidateIndividualCdpSetupCDP(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) internal {

 186:     function _liquidateCdpInGivenMode(
             LiquidationLocals memory _liqState,
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (uint256, uint256, uint256, uint256, uint256) {

 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(
             LiquidationLocals memory _liqState
         ) private returns (LiquidationLocals memory) {

 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(
             LiquidationRecoveryModeLocals memory _recoveryState
         ) private returns (LiquidationRecoveryModeLocals memory) {

 384:     function _closeCdpByLiquidation(bytes32 _cdpId) private returns (uint256, uint256, uint256) {

 397:     function _liquidateCDPPartially(
             LiquidationLocals memory _partialState
         ) private returns (uint256, uint256) {

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

 503:     function _finalizeLiquidation(
             uint256 totalDebtToBurn,
             uint256 totalCollSharesToSend,
             uint256 totalDebtToRedistribute,
             uint256 totalLiquidatorRewardCollShares,
             uint256 totalSurplusCollShares,
             uint256 systemInitialCollShares,
             uint256 systemInitialDebt,
             uint256 price
         ) internal {

 544:     function _calculatePartialLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 570:     function _calculateFullLiquidationSurplusAndCap(
             uint256 _ICR,
             uint256 _price,
             uint256 _totalDebtToBurn,
             uint256 _totalColToSend
         ) private view returns (uint256 toLiquidator, uint256 collSurplus, uint256 debtToRedistribute) {

 608:     function _getLiquidationValuesNormalMode(
             uint256 _price,
             uint256 _TCR,
             LocalVariables_LiquidationSequence memory vars,
             LiquidationValues memory singleLiquidation
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

 839:     function _addLiquidationValuesToTotals(
             LiquidationTotals memory oldTotals,
             LiquidationValues memory singleLiquidation
         ) internal pure returns (LiquidationTotals memory newTotals) {

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

 465:     function _fallbackIsBroken(FallbackResponse memory _response) internal view returns (bool) {

 493:     function _responseTimeout(uint256 _timestamp, uint256 _timeout) internal view returns (bool) {

 788:     function _formatClAggregateAnswer(
             int256 _ethBtcAnswer,
             int256 _stEthEthAnswer,
             uint8 _ethBtcDecimals,
             uint8 _stEthEthDecimals
         ) internal view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 44:     constructor(address _owner) {

 160:     receive() external payable {

 164:     fallback() external payable {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

 456:     function _remove(bytes32 _id) internal {

 591:     function _validInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bool) {

 674:     function _findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) internal view returns (bytes32, bytes32) {

```

### <a name="NC-57"></a>[NC-57] NatSpec: Modifier declarations should have descriptions

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 26:     modifier requiresAuth() virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 16:     modifier requiresAuth() virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 13:     modifier nonReentrant() virtual {

```

### <a name="NC-58"></a>[NC-58] NatSpec: state variable declarations should have descriptions
e.g. `@notice` for public state variables, and `@dev` for [non-public](https://docs.soliditylang.org/en/latest/natspec-format.html#tags) ones

 There are 155 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 24:     string public constant NAME = "ActivePool";

 26:     address public immutable borrowerOperationsAddress;

 27:     address public immutable cdpManagerAddress;

 28:     address public immutable collSurplusPoolAddress;

 29:     address public feeRecipientAddress;

 31:     uint256 internal systemCollShares; // deposited collateral tracker

 32:     uint256 internal systemDebt;

 33:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient

 34:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 29:     string public constant NAME = "BorrowerOperations";

 32:     bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =

 38:     bytes32 private constant _TYPE_HASH =

 41:     string internal constant _VERSION = "1";

 45:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

 46:     uint256 private immutable _CACHED_CHAIN_ID;

 48:     bytes32 private immutable _HASHED_NAME;

 49:     bytes32 private immutable _HASHED_VERSION;

 53:     ICdpManager public immutable cdpManager;

 55:     ICollSurplusPool public immutable collSurplusPool;

 57:     address public feeRecipientAddress;

 59:     IEBTCToken public immutable ebtcToken;

 62:     ISortedCdps public immutable sortedCdps;

 65:     mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 21:     uint128 public constant UNSET_TIMESTAMP = type(uint128).max;

 22:     uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;

 24:     uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify

 25:     uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;

 122:     string public constant NAME = "CdpManager";

 126:     address public immutable borrowerOperationsAddress;

 128:     ICollSurplusPool immutable collSurplusPool;

 130:     IEBTCToken public immutable override ebtcToken;

 132:     address public immutable liquidationLibrary;

 135:     ISortedCdps public immutable sortedCdps;

 139:     uint256 public constant SECONDS_IN_ONE_MINUTE = 60;

 141:     uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%

 142:     uint256 public redemptionFeeFloor = MIN_REDEMPTION_FEE_FLOOR;

 143:     bool public redemptionsPaused;

 148:     uint256 public minuteDecayFactor = 999037758833783000;

 149:     uint256 public constant MIN_MINUTE_DECAY_FACTOR = 1; // Non-zero

 150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

 152:     uint256 internal immutable deploymentStartTime;

 159:     uint256 public beta = 2;

 161:     uint256 public baseRate;

 163:     uint256 public stakingRewardSplit;

 166:     uint256 public lastRedemptionTimestamp;

 168:     mapping(bytes32 => Cdp) public Cdps;

 170:     uint256 public override totalStakes;

 173:     uint256 public totalStakesSnapshot;

 176:     uint256 public totalCollateralSnapshot;

 187:     uint256 public systemDebtRedistributionIndex;

 190:     mapping(bytes32 => uint256) public cdpDebtRedistributionIndex;

 193:     uint256 public lastEBTCDebtErrorRedistribution;

 196:     uint256 public override stEthIndex;

 198:     uint256 public override systemStEthFeePerUnitIndex;

 200:     uint256 public override systemStEthFeePerUnitIndexError;

 202:     mapping(bytes32 => uint256) public cdpStEthFeePerUnitIndex;

 205:     bytes32[] public CdpIds;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 19:     string public constant NAME = "CollSurplusPool";

 21:     address public immutable borrowerOperationsAddress;

 22:     address public immutable cdpManagerAddress;

 23:     address public immutable activePoolAddress;

 24:     address public immutable feeRecipientAddress;

 25:     ICollateralToken public immutable collateral;

 28:     uint256 internal totalSurplusCollShares;

 30:     mapping(address => uint256) internal balances;

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 14:     address public owner;

 16:     Authority public authority;

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 13:     Authority private _authority;

 14:     bool private _authorityInitialized;

```


```solidity
File: packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol

 9:     uint256 public constant MAX_BPS = 10_000;

 10:     uint256 public constant MAX_FEE_BPS = 1_000; // 10%

 11:     bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");

 14:     uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance

 15:     bool public flashLoansPaused;

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

 41:     IActivePool public immutable activePool;

 43:     IPriceFeed public immutable override priceFeed;

 46:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 6:     uint256 internal constant DECIMAL_PRECISION = 1e18;

 7:     uint256 public constant MAX_TCR = type(uint256).max;

 18:     uint256 internal constant NICR_PRECISION = 1e20;

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 8:     uint256 internal constant OPEN = 1;

 9:     uint256 internal constant LOCKED = 2;

 11:     uint256 public locked = OPEN;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 26:     EnumerableSet.AddressSet internal users;

 27:     EnumerableSet.AddressSet internal targets;

 28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

 30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

 32:     mapping(address => bytes32) public getUserRoles;

 34:     mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

 36:     mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 27:     uint256 private _totalSupply;

 28:     string internal constant _NAME = "EBTC Stablecoin";

 29:     string internal constant _SYMBOL = "EBTC";

 30:     string internal constant _VERSION = "1";

 31:     uint8 internal constant _DECIMALS = 18;

 36:     bytes32 private constant _PERMIT_TYPEHASH =

 39:     bytes32 private constant _TYPE_HASH =

 44:     bytes32 private immutable _CACHED_DOMAIN_SEPARATOR;

 45:     uint256 private immutable _CACHED_CHAIN_ID;

 47:     bytes32 private immutable _HASHED_NAME;

 48:     bytes32 private immutable _HASHED_VERSION;

 51:     mapping(address => uint256) private _balances;

 52:     mapping(address => mapping(address => uint256)) private _allowances;

 55:     address public immutable cdpManagerAddress;

 56:     address public immutable borrowerOperationsAddress;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 17:     bytes32 NO_ROLES = bytes32(0);

 30:     mapping(uint8 => string) internal roleNames;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 12:     string public constant NAME = "HintHelpers";

 14:     ISortedCdps public immutable sortedCdps;

 15:     ICdpManager public immutable cdpManager;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 29:     IBorrowerOperations public immutable borrowerOperations;

 30:     IActivePool public immutable activePool;

 31:     ICdpCdps public immutable cdpManager;

 32:     IEBTCToken public immutable ebtcToken;

 33:     ISortedCdps public immutable sortedCdps;

 34:     ICollateralToken public immutable stETH;

 35:     bool internal immutable willSweep;

 37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 12:     address public immutable borrowerOperations;

 13:     address public immutable activePool;

 14:     address public immutable cdpManager;

 15:     address public immutable ebtcToken;

 16:     address public immutable stETH;

 17:     address public immutable sortedCdps;

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 12:     address internal immutable theOwner;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 22:     string public constant NAME = "PriceFeed";

 25:     AggregatorV3Interface public immutable ETH_BTC_CL_FEED;

 26:     AggregatorV3Interface public immutable STETH_ETH_CL_FEED;

 29:     IFallbackCaller public fallbackCaller; // Wrapper contract that calls the fallback system

 32:     uint256 public constant TIMEOUT_ETH_BTC_FEED = 4800; // 1 hours & 20min: 60 * 80

 33:     uint256 public constant TIMEOUT_STETH_ETH_FEED = 90000; // 25 hours: 60 * 60 * 25

 36:     uint256 public constant MAX_PRICE_DEVIATION_FROM_PREVIOUS_ROUND = 5e17; // 50%

 42:     uint256 public constant MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES = 5e16; // 5%

 45:     uint256 public lastGoodPrice;

 48:     Status public status;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

 42:     address public immutable owner;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 52:     string public constant NAME = "SortedCdps";

 54:     address public immutable borrowerOperationsAddress;

 56:     ICdpManager public immutable cdpManager;

 58:     uint256 public immutable maxSize;

 60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

 61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

 77:     Data public data;

 79:     uint256 public nextCdpNonce;

 80:     bytes32 public constant dummyId =

```

### <a name="NC-59"></a>[NC-59] Not using the named return variables anywhere in the function is confusing
Consider changing the variable to be an unnamed one, since the variable is never assigned, nor is it returned by name. If the optimizer is not turned on, leaving the code as it is will also waste gas for the stack variable.

 There are 8 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 721:     ) public view returns (uint256 pendingEBTCDebtReward) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

 75:     function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 261:     ) external view returns (uint256 debt, uint256 collShares);

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

```

### <a name="NC-60"></a>[NC-60] Overflows in unchecked blocks
While integers with a large number of bits are unlikely to overflow on human time scales, it is not strictly correct to use an `unchecked` block around them, because eventually they will overflow, and `unchecked` blocks are meant for cases where it’s mathematically impossible for an operation to trigger an overflow (e.g. a prior `require()` statement prevents the overflow case)

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 388:                 ++i;

 438:             for (uint256 i; i < length; ++i) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 118:                 ++i;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 357:             ++nextCdpNonce;

```

### <a name="NC-61"></a>[NC-61] Polymorphic functions make security audits more time-consuming and error-prone
The instances below point to one of two functions with the same name. Consider naming each function differently, in order to make code navigation and analysis easier.

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/EBTCToken.sol

 104:     function burn(uint256 _amount) external {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 63:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 43:     function deployNewMacro(address _owner) public returns (address) {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 160:     receive() external payable {

```

### <a name="NC-62"></a>[NC-62] Functions not used internally could be marked external
When the function is not used internally marking function as 'external' designates it for external access, enhancing clarity and security for interactions with other contracts and external accounts.

 There are 21 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 100:     function transferSystemCollShares(address _account, uint256 _shares) public override {

 371:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {

 717:     function getDeploymentStartTime() public view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

 719:     function getPendingRedistributedDebt(

 728:     function hasPendingRedistributedDebt(bytes32 _cdpId) public view returns (bool) {

 864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

 874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {

 890:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) public view returns (bool) {

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 142:     function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 22:     function authority() public view returns (Authority) {

 26:     function authorityInitialized() public view returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 50:     function isPublicCapability(address target, bytes4 functionSig) public view returns (bool) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 96:     function getRolesFromByteMap(bytes32 byteMap) public pure returns (uint8[] memory roleIds) {

 120:     function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

 131:     function getEnabledFunctionsInTarget(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 234:     function sweepToken(address token, uint256 amount) public {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 63:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 44:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 130:     function nonExistId() public pure override returns (bytes32) {

```

### <a name="NC-63"></a>[NC-63] `pure` function accesses storage
While the compiler currently flags functions like these as being pure, this is a [bug](https://github.com/ethereum/solidity/issues/11573) which will be fixed in a future version, so it’s best to not use pure visibility, in order to not break when this bug is fixed.

 There are 18 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 687:     function version() external pure override returns (string memory) {

 693:     function permitTypeHash() external pure override returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 60:     function _calcNetStEthBalance(uint256 _stEthBalance) internal pure returns (uint256) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {

 59:     function _decPow(uint256 _base, uint256 _minutes) internal pure returns (uint256) {

 92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {

 104:     function _computeCR(

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 331:     function name() external pure override returns (string memory) {

 337:     function symbol() external pure override returns (string memory) {

 343:     function decimals() external pure override returns (uint8) {

 349:     function version() external pure override returns (string memory) {

 355:     function permitTypeHash() external pure override returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 445:     function _chainlinkPriceChangeAboveMax(

 526:     function _bothOraclesSimilarPrice(

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 83:     function _getStorage() internal pure returns (DiamondLikeStorage storage ds) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 105:     function toCdpId(

 123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {

 130:     function nonExistId() public pure override returns (bytes32) {

```

### <a name="NC-64"></a>[NC-64] Duplicated require()/revert() checks should be refactored to a modifier or function.
In Solidity, duplicated require() or revert() checks should be consolidated into modifiers or separate functions to enhance code clarity, reduce redundancy, and simplify maintenance.

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

### <a name="NC-65"></a>[NC-65] require()/revert() statements should have descriptive reason strings

 There are 12 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 45:         require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 41:         require(_authority.canCall(msg.sender, address(this), msg.sig));

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 452:         require(addy != address(borrowerOperations));

 453:         require(addy != address(sortedCdps));

 454:         require(addy != address(activePool));

 455:         require(addy != address(cdpManager));

 456:         require(addy != address(this)); // If it could call this it could fake the forwarded caller

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 52:         require(msg.sender == owner);

 56:         require(sig != 0x94b24d09);

 67:         require(msg.sender == owner);

 77:         require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

 154:             require(success);

```

### <a name="NC-66"></a>[NC-66] Return values of `approve()` not checked
Not all IERC20 implementations `revert()` when there's a failure in `approve()`. The function signature has a boolean return value and they indicate errors that way instead. By not checking the return value, operations that should have marked as failed, may potentially go through without actually approving anything

 There are 12 instances:

 ```solidity
File: packages/contracts/contracts/EBTCToken.sol

 130:         _approve(msg.sender, spender, amount);

 146:                 _approve(sender, msg.sender, cachedAllowance - amount);

 156:         _approve(msg.sender, spender, _allowances[msg.sender][spender] + addedValue);

 167:             _approve(msg.sender, spender, cachedAllowances - subtractedValue);

 220:         _approve(owner, spender, amount);

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 22:     stETH.approve(_borrowerOperationsAddress, type(uint256).max);

 23:     stETH.approve(_activePool, type(uint256).max);

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 40:         stETH.approve(_borrowerOperationsAddress, type(uint256).max);

 41:         stETH.approve(_activePool, type(uint256).max);

 53:         ebtcToken.approve(address(borrowerOperations), type(uint256).max);

 54:         stETH.approve(address(borrowerOperations), type(uint256).max);

 55:         stETH.approve(address(activePool), type(uint256).max);

```

### <a name="NC-67"></a>[NC-67] Setters should prevent re-setting of the same value
This is especially problematic when the setter also emits the same value, which may be confusing to offline parsers.

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  authority
 42:     function setAuthority(Authority newAuthority) public virtual {
            // We check if the caller is the owner first because we want to ensure they can
            // always swap out the authority even if it's reverting or using up a lot of gas.
            require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
    
            authority = newAuthority;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  capabilityFlag
 85:     function setPublicCapability(
            address target,
            bytes4 functionSig,
            bool enabled
        ) public virtual requiresAuth {
            require(
                capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
                "RolesAuthority: Capability Burned"
            );
    
            if (enabled) {
                capabilityFlag[target][functionSig] = CapabilityFlag.Public;
            } else {
                capabilityFlag[target][functionSig] = CapabilityFlag.None;

 /// @audit  capabilityFlag
 85:     function setPublicCapability(
            address target,
            bytes4 functionSig,
            bool enabled
        ) public virtual requiresAuth {
            require(
                capabilityFlag[target][functionSig] != CapabilityFlag.Burned,
                "RolesAuthority: Capability Burned"
            );
    
            if (enabled) {
                capabilityFlag[target][functionSig] = CapabilityFlag.Public;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  roleNames
 154:     function setRoleName(uint8 role, string memory roleName) external requiresAuth {
             roleNames[role] = roleName;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 /// @audit  fallbackCaller
 358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
             // health check-up before officially set it up
             IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);
             FallbackResponse memory fallbackResponse;
     
             if (_fallbackCaller != address(0)) {
                 try newFallbackCaler.getFallbackResponse() returns (
                     uint256 answer,
                     uint256 timestampRetrieved,
                     bool success
                 ) {
                     fallbackResponse.answer = answer;
                     fallbackResponse.timestamp = timestampRetrieved;
                     fallbackResponse.success = success;
                     if (
                         !_fallbackIsBroken(fallbackResponse) &&
                         !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
                     ) {
                         address oldFallbackCaller = address(fallbackCaller);
                         fallbackCaller = newFallbackCaler;
                         emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
                     }
                 } catch {
                     emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);
                 }
             } else {
                 address oldFallbackCaller = address(fallbackCaller);
                 // NOTE: assume intentionally bricking fallback!!!
                 fallbackCaller = newFallbackCaler;

 /// @audit  fallbackCaller
 358:     function setFallbackCaller(address _fallbackCaller) external requiresAuth {
             // health check-up before officially set it up
             IFallbackCaller newFallbackCaler = IFallbackCaller(_fallbackCaller);
             FallbackResponse memory fallbackResponse;
     
             if (_fallbackCaller != address(0)) {
                 try newFallbackCaler.getFallbackResponse() returns (
                     uint256 answer,
                     uint256 timestampRetrieved,
                     bool success
                 ) {
                     fallbackResponse.answer = answer;
                     fallbackResponse.timestamp = timestampRetrieved;
                     fallbackResponse.success = success;
                     if (
                         !_fallbackIsBroken(fallbackResponse) &&
                         !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
                     ) {
                         address oldFallbackCaller = address(fallbackCaller);
                         fallbackCaller = newFallbackCaler;

```

### <a name="NC-68"></a>[NC-68] Style guide: Contract does not follow the Solidity style guide’s suggested layout ordering
The [style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#order-of-layout) says that, within a contract, the ordering should be 1) Type declarations, 2) State variables, 3) Events, 4) Modifiers, and 5) Functions, but the contract(s) below do not follow this ordering

 There are 18 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  variable positionManagers came earlier
 72:     struct AdjustCdpLocals {

 /// @audit  function constructor came earlier
 144:     modifier nonReentrantSelfAndCdpM() {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  function setGracePeriod came earlier
 122:     string public constant NAME = "CdpManager";

 /// @audit  function constructor came earlier
 241:     modifier nonReentrantSelfAndBOps() {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  event AuthorityUpdated came earlier
 14:     address public owner;

 /// @audit  function constructor came earlier
 26:     modifier requiresAuth() virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 /// @audit  event AuthorityUpdated came earlier
 13:     Authority private _authority;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 /// @audit  function constructor came earlier
 26:     EnumerableSet.AddressSet internal users;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  variable NO_ROLES came earlier
 19:     struct Role {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  variable cdpManager came earlier
 19:     struct LocalVariables_getRedemptionHints {

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  event CdpFeeSplitApplied came earlier
 77:     enum CdpOperation {

```


```solidity
File: packages/contracts/contracts/Interfaces/IPriceFeed.sol

 /// @audit  event UnhealthyFallbackCaller came earlier
 17:     struct ChainlinkResponse {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  function Cdps came earlier
 29:     IBorrowerOperations public immutable borrowerOperations;

 /// @audit  function constructor came earlier
 70:     enum FlashLoanType {

 /// @audit  function _doCheckValueType came earlier
 259:     struct LeverageMacroOperation {

 /// @audit  function _handleOperation came earlier
 313:     struct OpenCdpOperation {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  function _getStorage came earlier
 94:     enum OperationType {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  variable BLOCK_SHIFT came earlier
 64:     struct Node {

```

### <a name="NC-69"></a>[NC-69] Style guide: Function names should use lowerCamelCase
According to the Solidity [style guide](https://docs.soliditylang.org/en/latest/style-guide.html#function-names) function names should be in `mixedCase` (lowerCamelCase)

 There are 48 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 227:     function _requireCallerIsBOorCdpM() internal view {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 659:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

 673:     function _chainID() private view returns (uint256) {

 910:     function _requireICRisNotBelowMCR(uint256 _newICR) internal pure {

 917:     function _requireICRisNotBelowCCR(uint256 _newICR) internal pure {

 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 928:     function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure {

 986:     function _getNewNominalICRFromCdpChange(

 1004:     function _getNewICRFromCdpChange(

 1049:     function _getNewTCRFromCdpChange(

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 580:     function getCachedTCR(uint256 _price) external view override returns (uint256) {

 757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 489:     function _computeTCRWithGivenSystemValues(

 673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {

 684:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256) {

 701:     function getCachedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

 707:     function _calculateCR(

 864:     function getSyncedICR(bytes32 _cdpId, uint256 _price) public view returns (uint256) {

 874:     function getSyncedTCR(uint256 _price) public view returns (uint256) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 83:     function _getTCRWithSystemDebtAndCollShares(

 99:     function _checkRecoveryModeForTCR(uint256 _tcr) internal view returns (bool) {

 124:     function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {

 134:     function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

 140:     function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 92:     function _computeNominalCR(uint256 _collShares, uint256 _debt) internal pure returns (uint256) {

 104:     function _computeCR(

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 176:     function DOMAIN_SEPARATOR() external view returns (bytes32) {

 231:     function _chainID() private view returns (uint256) {

 314:     function _requireCallerIsBOorCdpMOrAuth() internal view {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 203:     function computeNominalCR(uint256 _coll, uint256 _debt) external pure returns (uint256) {

 212:     function computeCR(

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 15:     function Cdps(bytes32) external view returns (ICdpManagerData.Cdp memory);

 338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 135:     function _liquidateIndividualCdpSetupCDP(

 223:     function _liquidateIndividualCdpSetupCDPInNormalMode(

 295:     function _liquidateIndividualCdpSetupCDPInRecoveryMode(

 397:     function _liquidateCDPPartially(

 733:     function _getTotalFromBatchLiquidate_RecoveryMode(

 807:     function _getTotalsFromBatchLiquidate_NormalMode(

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 775:     function _checkHealthyCLResponse(uint80 _roundId, int256 _answer) internal view returns (bool) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 719:     function _requireCallerIsBOorCdpM() internal view {

```

### <a name="NC-70"></a>[NC-70] Style guide: Function ordering does not follow the Solidity style guide
According to the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#order-of-functions), functions should be laid out in the following order :`constructor()`, `receive()`, `fallback()`, `external`, `public`, `internal`, `private`, but the cases below do not follow this pattern

 There are 58 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 /// @audit  transferSystemCollShares() came earlier
 129:     function transferSystemCollSharesAndLiquidatorReward(
             address _account,
             uint256 _shares,
             uint256 _liquidatorRewardShares
         ) external override {

 /// @audit  _transferCollSharesWithContractHooks() came earlier
 194:     function increaseSystemDebt(uint256 _amount) external override {

 /// @audit  _requireCallerIsCdpManager() came earlier
 242:     function increaseSystemCollShares(uint256 _value) external override {

 /// @audit  maxFlashLoan() came earlier
 346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {

 /// @audit  sweepToken() came earlier
 390:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 /// @audit  _openCdp() came earlier
 553:     function closeCdp(bytes32 _cdpId) external override {

 /// @audit  _getPositionManagerApproval() came earlier
 628:     function setPositionManagerApproval(
             address _positionManager,
             PositionManagerApproval _approval
         ) external override {

 /// @audit  _setPositionManagerApproval() came earlier
 647:     function revokePositionManagerApproval(address _positionManager) external override {

 /// @audit  _buildDomainSeparator() came earlier
 687:     function version() external pure override returns (string memory) {

 /// @audit  _getNewTCRFromCdpChange() came earlier
 1077:     function flashLoan(
              IERC3156FlashBorrower receiver,
              address token,
              uint256 amount,
              bytes calldata data
          ) external override returns (bool) {

 /// @audit  maxFlashLoan() came earlier
 1140:     function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  _isValidFirstRedemptionHint() came earlier
 320:     function redeemCollateral(
             uint256 _debt,
             bytes32 _firstRedemptionHint,
             bytes32 _upperPartialRedemptionHint,
             bytes32 _lowerPartialRedemptionHint,
             uint256 _partialRedemptionHintNICR,
             uint256 _maxIterations,
             uint256 _maxFeePercentage
         ) external override nonReentrantSelfAndBOps {
             RedemptionTotals memory totals;

 /// @audit  _getCdpIdsToRemove() came earlier
 514:     function syncAccounting(bytes32 _cdpId) external virtual override {
             /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

 /// @audit  _addCdpIdToArray() came earlier
 570:     function getSystemDebt() public view returns (uint256 entireSystemDebt) {
             return _getSystemDebt();

 /// @audit  getSystemDebt() came earlier
 580:     function getCachedTCR(uint256 _price) external view override returns (uint256) {
             return _getCachedTCR(_price);

 /// @audit  _updateBaseRateFromRedemption() came earlier
 638:     function getRedemptionRate() public view override returns (uint256) {
             return _calcRedemptionRate(baseRate);

 /// @audit  _getRedemptionFee() came earlier
 661:     function getRedemptionFeeWithDecay(
             uint256 _stETHToRedeem
         ) external view override returns (uint256) {
             return _calcRedemptionFee(getRedemptionRateWithDecay(), _stETHToRedeem);

 /// @audit  _minutesPassedSinceLastRedemption() came earlier
 717:     function getDeploymentStartTime() public view returns (uint256) {
             return deploymentStartTime;

 /// @audit  getDeploymentStartTime() came earlier
 727:     function checkPotentialRecoveryMode(
             uint256 _systemCollShares,
             uint256 _systemDebt,
             uint256 _price
         ) external view returns (bool) {
             return _checkPotentialRecoveryMode(_systemCollShares, _systemDebt, _price);

 /// @audit  _requireValidMaxFeePercentage() came earlier
 773:     function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {
             require(

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 /// @audit  _syncGracePeriodForGivenValues() came earlier
 111:     function setGracePeriod(uint128 _gracePeriod) external requiresAuth {

 /// @audit  setGracePeriod() came earlier
 217:     constructor(
             address _liquidationLibraryAddress,
             address _authorityAddress,
             address _borrowerOperationsAddress,
             address _collSurplusPool,
             address _ebtcToken,
             address _sortedCdps,
             address _activePool,
             address _priceFeed,
             address _collateral
         ) EbtcBase(_activePool, _priceFeed, _collateral) {

 /// @audit  _computeTCRWithGivenSystemValues() came earlier
 504:     function syncGlobalAccounting() external {
             _requireCallerIsBorrowerOperations();

 /// @audit  _syncGlobalAccounting() came earlier
 527:     function syncGlobalAccountingAndGracePeriod() public {
             _syncGlobalAccounting(); // Apply // Could trigger RM

 /// @audit  _syncStEthIndex() came earlier
 552:     function calcFeeUponStakingReward(
             uint256 _newIndex,
             uint256 _prevIndex
         ) public view returns (uint256, uint256, uint256) {
             require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

 /// @audit  _applyAccumulatedFeeSplit() came earlier
 616:     function getAccumulatedFeeSplitApplied(
             bytes32 _cdpId,
             uint256 _systemStEthFeePerUnitIndex
         ) public view returns (uint256, uint256) {
             uint256 _cdpStEthFeePerUnitIndex = cdpStEthFeePerUnitIndex[_cdpId];

 /// @audit  _requireCallerIsBorrowerOperations() came earlier
 673:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256) {
             (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 /// @audit  _calculateCR() came earlier
 719:     function getPendingRedistributedDebt(
             bytes32 _cdpId
         ) public view returns (uint256 pendingEBTCDebtReward) {
             (uint256 _pendingDebt, ) = _getPendingRedistributedDebt(_cdpId);

 /// @audit  _getSyncedDebtAndCollShares() came earlier
 745:     function getSyncedDebtAndCollShares(
             bytes32 _cdpId
         ) public view returns (uint256 debt, uint256 coll) {
             (uint256 _newColl, uint256 _newDebt, , , ) = _calcSyncedAccounting(

 /// @audit  _getSyncedCdpDebtAndRedistribution() came earlier
 839:     function getSyncedCdpDebt(bytes32 _cdpId) public view returns (uint256) {
             (uint256 _newDebt, , ) = _getSyncedCdpDebtAndRedistribution(_cdpId);

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 /// @audit  _requireCallerIsActivePool() came earlier
 130:     function increaseTotalSurplusCollShares(uint256 _value) external override {

```


```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 /// @audit  isAuthorized() came earlier
 42:     function setAuthority(Authority newAuthority) public virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 /// @audit  isAuthorized() came earlier
 38:     function setAuthority(address newAuthority) public virtual {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 /// @audit  _calcNetStEthBalance() came earlier
 67:     function getSystemCollShares() public view returns (uint256 entireSystemColl) {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 /// @audit  domainSeparator() came earlier
 199:     function permit(
             address owner,
             address spender,
             uint256 amount,
             uint256 deadline,
             uint8 v,
             bytes32 r,
             bytes32 s
         ) external override {

 /// @audit  _buildDomainSeparator() came earlier
 246:     function _transfer(address sender, address recipient, uint256 amount) internal {

 /// @audit  _requireCallerIsCdpM() came earlier
 331:     function name() external pure override returns (string memory) {

```


```solidity
File: packages/contracts/contracts/Governor.sol

 /// @audit  getEnabledFunctionsInTarget() came earlier
 146:     function getRoleName(uint8 role) external view returns (string memory roleName) {

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 /// @audit  _calculateCdpStateAfterPartialRedemption() came earlier
 164:     function getApproxHint(
             uint256 _CR,
             uint256 _numTrials,
             uint256 _inputRandomSeed
         ) external view returns (bytes32 hint, uint256 diff, uint256 latestRandomSeed) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  _assertOwner() came earlier
 51:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps,
            bool _sweepToCaller
        ) {

 /// @audit  _handleOperation() came earlier
 338:     function decodeFLData(bytes calldata data) public view returns (LeverageMacroOperation memory) {

 /// @audit  decodeFLData() came earlier
 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 /// @audit  owner() came earlier
 41:     constructor(
            address _borrowerOperationsAddress,
            address _activePool,
            address _cdpManager,
            address _ebtc,
            address _coll,
            address _sortedCdps
        )
            LeverageMacroBase(
                _borrowerOperationsAddress,
                _activePool,
                _cdpManager,
                _ebtc,
                _coll,
                _sortedCdps,
                false // Do not sweep to caller
            )
        {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 /// @audit  owner() came earlier
 50:     function resetApprovals() external {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 /// @audit  _liquidateCDPPartially() came earlier
 450:     function _partiallyReduceCdpDebt(
             bytes32 _cdpId,
             uint256 _partialDebt,
             uint256 _partialColl
         ) internal {

 /// @audit  _calculateFullLiquidationSurplusAndCap() came earlier
 608:     function _getLiquidationValuesNormalMode(
             uint256 _price,
             uint256 _TCR,
             LocalVariables_LiquidationSequence memory vars,
             LiquidationValues memory singleLiquidation
         ) internal {

 /// @audit  _getLiquidationValuesRecoveryMode() came earlier
 679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 /// @audit  _getStorage() came earlier
 110:     function execute(Operation[] calldata ops) external payable {

 /// @audit  _executeOne() came earlier
 160:     receive() external payable {

 /// @audit  receive() came earlier
 164:     fallback() external payable {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 /// @audit  nonExistId() came earlier
 140:     function cdpOfOwnerByIndex(
             address owner,
             uint256 index
         ) external view override returns (bytes32) {

 /// @audit  _cdpOfOwnerByIndex() came earlier
 216:     function cdpCountOf(address owner) external view override returns (uint256) {

 /// @audit  _cdpCountOf() came earlier
 270:     function getCdpsOf(address owner) external view override returns (bytes32[] memory cdps) {

 /// @audit  _getCdpsOf() came earlier
 344:     function insert(
             address owner,
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external override returns (bytes32) {

 /// @audit  _insert() came earlier
 410:     function remove(bytes32 _id) external override {

 /// @audit  _remove() came earlier
 498:     function reInsert(
             bytes32 _id,
             uint256 _newNICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external override {

 /// @audit  isEmpty() came earlier
 542:     function getSize() external view override returns (uint256) {

 /// @audit  _ascendList() came earlier
 666:     function findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bytes32, bytes32) {

```

### <a name="NC-71"></a>[NC-71] Style guide: Lines are too long
Usually lines in source code are limited to [80](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width) characters. Today’s screens are much larger so it’s reasonable to stretch this in some cases. The solidity style guide recommends a maximum line length of [120](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#maximum-line-length) characters, so the lines below should be split when they reach that length.

 There are 150 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 39:     /// @dev Initializes the contract with the borrowerOperationsAddress, cdpManagerAddress, collateral token address, collSurplusAddress, and feeRecipientAddress

 71:     /// @dev Not necessarily equal to the the contract's raw systemCollShares balance - tokens can be forcibly sent to contracts

 79:     /// @dev The amount of EBTC debt in the pool. Like systemCollShares, this is not necessarily equal to the contract's EBTC token balance - tokens can be forcibly sent to contracts

 119:     /// @notice Liquidator reward shares are not tracked via internal accounting in the active pool and are assumed to be present in expected amount as part of the intended behavior of BorowerOperations and CdpManager

 121:     /// @dev closeCdp() or liqudations result in the actor (borrower or liquidator respectively) receiving the liquidator reward shares

 123:     /// @dev Note that funds in the coll surplus pool, just like liquidator reward shares, are not tracked as part of the system CR or coll of a CDP.

 154:     /// @dev If the fee recipient address is changed while outstanding claimable coll is available, only the new fee recipient will be able to claim the outstanding coll

 177:     /// @notice Helper function to transfer stETH shares to another address, ensuring to call hooks into other system pools if they are the recipient

 268:         uint256 fee = flashFee(token, amount); // NOTE: Check for `token` is implicit in the requires above // also checks for paused

 293:         //  You technically could, but you'd be having to repay any amount below systemCollShares to get Fl2 to not revert

 347:         ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod(); // Calling this increases shares so do it first

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 31:     // keccak256("permitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)");

 34:             "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"

 43:     // Cache the domain separator as an immutable value, but also store the chain id that it corresponds to, in order to

 64:     // Mapping of borrowers to approved position managers, by approval status: cdpOwner(borrower) -> positionManager -> PositionManagerApproval (None, OneTime, Persistent)

 140:         @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation

 141:         @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.

 160:     /// @notice Function that creates a Cdp for the caller with the requested debt, and the stETH received as collateral.

 161:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

 161:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

 162:     /// @notice Upon Cdp open, a separate gas stipend (denominated in stETH) will be allocated for possible liquidation.

 162:     /// @notice Upon Cdp open, a separate gas stipend (denominated in stETH) will be allocated for possible liquidation.

 177:     /// @notice Function that creates a Cdp for the specified _borrower by caller with the requested debt, and the stETH received as collateral.

 179:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

 179:     /// @notice Successful execution is conditional mainly on the resulting collateralization ratio which must exceed minimum requirement, e.g., MCR.

 180:     /// @notice Upon Cdp open, a separate gas stipend (denominated in stETH) will be allocated for possible liquidation.

 180:     /// @notice Upon Cdp open, a separate gas stipend (denominated in stETH) will be allocated for possible liquidation.

 214:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

 214:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

 228:     /// @notice Function that withdraws `_debt` amount of eBTC token from the specified Cdp, thus increasing its debt accounting

 230:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

 230:     /// @notice Successful execution is conditional on whether the withdrawal would bring down the ICR or TCR to the minimum requirement, e.g., MCR or CCR

 267:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

 267:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

 296:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

 296:     /// @param _isDebtIncrease The flag (true or false) to indicate whether this is a eBTC token withdrawal (debt increase) or a repayment (debt reduce)

 392:         // When the adjustment is a debt repayment, check it's a valid amount, that the caller has enough EBTC, and that the resulting debt is >0

 451:         // ICR is based on the net stEth balance, i.e. the specified stEth balance amount - fixed liquidator incentive gas comp.

 533:             The static liqudiation incentive is stored in the gas pool and can be considered a deposit / voucher to be returned upon Cdp close, to the closer.

 537:         // CEI: Move the collateral and liquidator gas compensation to the Active Pool. Track only net collateral for TCR purposes.

 597:     /// @notice when a Cdp has been fully redeemed from and closed, or liquidated in Recovery Mode with a collateralization ratio higher enough (like over MCR)

 624:     /// @notice Position managers with 'OneTIme' status will be able to take a single action on one Cdp. Approval will be automatically revoked after one Cdp-related action.

 625:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

 625:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

 627:     /// @param _approval PositionManagerApproval (None/OneTime/Persistent) status set to the specified _positionManager for caller's Cdp

 645:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

 645:     /// @notice Similar to approving tokens, approving a position manager allows _stealing of all positions_ if given to a malicious account.

 646:     /// @param _positionManager The position manager address which will get all approval revoked by caller (a Cdp owner)

 782:     /// @dev These number of liquidator shares associated with each Cdp are stored in the Cdp, while the actual tokens float in the active pool

 977:         /// @dev If the PositionManagerApproval was none, we should have failed with the check in _requireBorrowerOrPositionManagerAndUpdateManagerApproval

 1084:         uint256 fee = flashFee(token, amount); // NOTE: Check for `eBTCToken` is implicit here // NOTE: Pause check is here

 1122:     /// @param token The address of the token to get the maximum flash loan amount for, exclusively used here for eBTC token

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 13: /// @title CdpManager is mainly in charge of all Cdp related core processing like collateral & debt accounting, split fee calculation, redemption, etc

 95:     /// @notice Fully liquidate a single Cdp by ID. Cdp must meet the criteria for liquidation at the time of execution.

 96:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).

 122:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.

 271:     /// @dev Returns true if the specified CdpId is not blank, exists in the list, has an ICR > MCR, and the next lower Cdp in the list is either blank or has an ICR < MCR.

 291:     /// @notice Note that if _debt is very large, this function can run out of gas, specially if traversed cdps are small (meaning many small Cdps are redeemed against).

 292:     /// @notice This can be easily avoided by splitting the total _debt in appropriate chunks and calling the function multiple times.

 294:     /// @notice There is a optional parameter `_maxIterations` which can also be provided, so the loop through Cdps is capped (if it’s zero, it will be ignored).

 295:     /// @notice This makes it easier to avoid OOG for the frontend, as only knowing approximately the average cost of an iteration is enough,

 296:     /// @notice without needing to know the "topology" of the cdp list. It also avoids the need to set the cap in stone in the contract,

 299:     /// @notice All Cdps that are redeemed from -- with the likely exception of the last one -- will end up with no debt left,

 301:     /// @notice If the last Cdp does have some remaining debt & collateral (it has a valid meaningful ICR) then reinsertion of the CDP

 304:     /// @notice A frontend should use HintHelper.getRedemptionHints() to calculate what the ICR of this Cdp will be after redemption,

 305:     /// @notice and pass a hint for its position in the SortedCdps list along with the ICR value that the hint was found for.

 311:     /// @notice In this case, the redemption will stop after the last completely redeemed Cdp and the sender will keep the

 314:     /// @param _firstRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getRedemptionHints()

 315:     /// @param _upperPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)

 316:     /// @param _lowerPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)

 317:     /// @param _partialRedemptionHintNICR The new Nominal Collateral Ratio (NICR) of the last redeemed CDP after partial redemption, could get from HintHelper.getRedemptionHints()

 515:         /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

 579:     /// @return TCR The cached total collateralization ratio (TCR) of the system (does not take into account pending global state)

 678:         require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!"); // The baseRate can decay to 0

 919:         cdpStEthFeePerUnitIndex[_cdpId] = systemStEthFeePerUnitIndex; /// @audit We critically assume global accounting is synced here

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 27:     /// @notice Start the recovery mode grace period, if the system is in RM and the grace period timestamp has not already been set

 150:     uint256 public constant MAX_MINUTE_DECAY_FACTOR = 999999999999999999; // Corresponds to a very fast decay rate, but not too extreme

 175:     // Snapshot of the total collateral across the ActivePool, immediately after the latest liquidation and split fee claim

 197:     /* Global Fee accumulator (never decreasing) per stake unit in CDPManager, similar to systemDebtRedistributionIndex */

 239:     /// @notice BorrowerOperations and CdpManager share reentrancy status by confirming the other's locked flag before beginning operation

 240:     /// @dev This is an alternative to the more heavyweight solution of both being able to set the reentrancy flag on a 3rd contract.

 303:     /// @dev get the pending Cdp debt "reward" (i.e. the amount of extra debt assigned to the Cdp) from liquidation redistribution events, earned by their stake

 440:     // Calculate a new stake based on the snapshots of the totalStakes and totalCollateral taken at the last liquidation

 613:     /// @param _systemStEthFeePerUnitIndex The fee-per-stake-unit value to be used in fee split calculation, could be result of calcFeeUponStakingReward()

 683:     /// @return The Nominal Collateral Ratio (NICR) of the specified Cdp with fee split and debt redistribution considered.

 716:     /// @notice Return the pending extra debt assigned to the Cdp from liquidation redistribution, calcualted by Cdp's stake

 726:     /// @return Whether the debt redistribution tracking index of the specified Cdp is less than the global tracking one (meaning it might get pending debt redistribution)

 740:     /// @notice Calculate the Cdps entire debt and coll, including pending debt redistributions and collateral reduction from split fee.

 781:     /// @dev calculate pending state change to be applied for given CDP and global split index(typically already synced):

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 14: /// @dev While an owner could have multiple different sized Cdps, the remaining surplus colateral from all of its closed Cdp

 36:      * @dev One-time initialization function. Can only be called by the owner as a security measure. Ownership is renounced after the function is called.

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 24:     // Critical system collateral ratio. If the system's total collateral ratio (TCR) falls below the CCR, Recovery Mode is triggered.

 66:     /// @dev Collateral tokens stored in ActivePool for liquidator rewards, fees, or coll in CollSurplusPool, are not included

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 6: /// @author Modified from OpenZeppelin (https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol)

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 10: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)

 61:             - That capability is public, or the user has a role that has been granted the capability to call the function

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 16:  * https://github.com/OpenZeppelin/openzeppelin-contracts/blob/53516bc555a454862470e7860a9b5254db4d00f5/contracts/token/ERC20/ERC20Permit.sol

 21:  * 1) Transfer protection: blocklist of addresses that are invalid recipients (i.e. core Ebtc contracts) in external transfer() and transferFrom() calls.

 42:     // Cache the domain separator as an immutable value, but also store the chain id that it corresponds to, in order to

```


```solidity
File: packages/contracts/contracts/Governor.sol

 9: /// @notice We have taken the tradeoff of additional storage usage for easier readabiliy without using off-chain / indexing services.

 11: /// @author Modified from Solmate (https://github.com/transmissions11/solmate/blob/main/src/auth/authorities/RolesAuthority.sol)

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 9: /// @title HintHelpers mainly serves to provide handy information to facilitate offchain integration like redemption bots.

 100:                     // If the partial redemption would leave the CDP with less than the minimum allowed coll, bail out of partial redemption and return only the fully redeemable

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 24: /// @custom:known-issue Due to slippage some dust amounts for all intermediary tokens can be left, since there's no way to ask to sell all available

 233:     /// @dev If you delegatecall into this, this will transfer the tokens to the caller of the DiamondLike (and not the contract)

 413:         // But technically you could approve w/e you want here, this is fine because the contract is a router and will not hold user funds

 426:         // val -> 0 -> 0 -> val means this is safe to repeat since even if full approve is unused, we always go back to 0 after

 496:     /// @dev excessivelySafeCall to perform generic calls without getting gas bombed | useful if you don't care about return value

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 12: /// @dev This contract shares same base and storage layout with CdpManager and is the delegatecall destination from CdpManager

 36:     /// @notice Fully liquidate a single Cdp by ID. Cdp must meet the criteria for liquidation at the time of execution.

 37:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).

 134:     // For partial liquidation, caller should use HintHelper smart contract to get correct hints for reinsertion into sorted CDP list

 311:         // I don't see an issue emitting the CdpUpdated() event up here and avoiding an extra cache of the values, any objections?

 675:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.

 876:          * 5) Note: static analysis tools complain about this "division before multiplication", however, it is intended.

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 31:     // Maximum time period allowed since Chainlink's latest round data timestamp, beyond which Chainlink is considered frozen.

 96:     /// @dev Uses a main oracle (Chainlink) and a fallback oracle in case Chainlink fails. If both fail, it uses the last good price seen by eBTC.

 97:     /// @dev The fallback oracle address can be swapped by the Authority. The fallback oracle must conform to the IFallbackCaller interface.

 166:                  * If Fallback is live and both oracles have a similar price, conclude that Chainlink's large price deviation between

 173:                 // If Fallback is live but the oracles differ too much in price, conclude that Chainlink's initial price deviation was

 190:             // If both Fallback and Chainlink are live, unbroken, and reporting similar prices, switch back to Chainlink

 296:             // If Chainlink is live and Fallback is frozen, just use last good price (no status change) since we have no basis for comparison

 308:             // Otherwise if Chainlink is live but price not within 5% of Fallback, distrust Chainlink, and return Fallback price

 326:             // If Chainlink and Fallback are both live, unbroken and similar price, switch back to chainlinkWorking and return Chainlink price

 345:             // Otherwise if Chainlink is live and deviated <50% from it's previous price and Fallback is still untrusted,

 394:     /// @dev Chainlink is considered broken if its current or previous round data is in any way bad. We check the previous round for two reasons.

 396:     /// @dev 2. Chainlink is the PriceFeed's preferred primary oracle - having two consecutive valid round responses adds peace of mind when using or returning to Chainlink.

 408:     /// @dev A response is considered bad if the success value reports failure, or if the timestamp is invalid (0 or in the future)

 432:     /// @dev The oracle is considered frozen if either of the feed timestamps are older than the threshold specified by the static timeout thresholds

 444:     /// @return A boolean indicating whether the price change from Chainlink oracle is above the maximum threshold allowed

 521:     /// @notice Checks if the prices reported by the Chainlink and fallback oracles are similar, within the maximum deviation specified by MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES.

 530:         // Get the relative price difference between the oracles. Use the lower price as the denominator, i.e. the reference for the calculation.

 538:          * Return true if the relative price difference is <= MAX_PRICE_DIFFERENCE_BETWEEN_ORACLES: if so, we assume both oracles are probably reporting

 579:     /// @notice Retrieves the latest response from the fallback oracle. If the fallback oracle address is set to the zero address, it returns a failing struct.

 605:     /// @return chainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.

 686:     /// @return prevChainlinkResponse A struct containing data retrieved from the price feeds, including the round IDs, timestamps, aggregated price, and a success flag.

 771:     /// @notice Returns if the CL feed is healthy or not, based on: negative value and null round id. For price aggregation

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 16:  *  Per solidity, hardcoded functions are switched into, meaning they cannot be overriden (although you could set a callbackHandler that cannot be reached)

 22:  *  This ensures that nobody can call this contract unless the owner sets this to `true` via the scary `setAllowAnyCall`

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,

 37:  * - Ordering checks for insertion are performed by comparing an NICR argument to the current NICR, calculated at runtime.

 40:  * - Public functions with parameters have been made internal to save gas, and given an external wrapper function for external access

 100:     /// @dev Inspired https://github.com/balancer-labs/balancer-v2-monorepo/blob/18bd5fb5d87b451cc27fbd30b276d1fb2987b529/pkg/vault/contracts/PoolRegistry.sol

 134:     /// @notice Find a specific CDP for a given owner, indexed by it's place in the linked list relative to other Cdps owned by the same address

 148:     /// @dev a pagination-flavor search (from least ICR to biggest ICR) for CDP owned by given owner and specified index (starting at given CDP)

 171:     /// @return cdpId The CDP Id if found, otherwise return current lastly-visited CDP as the startNode for next pagination

 280:     /// @dev a pagination-flavor search retrieval of (from least ICR to biggest ICR) Cdps owned by given owner (starting at given CDP)

 283:     /// @return all CdpIds of the specified owner found by search starting at the specified startNodeId for the specified maximum iteration count

 309:         // Two-pass strategy, halving the amount of Cdps we can process before relying on pagination or off-chain methods

 606:             // `(_prevId, _nextId)` is a valid insert position if they are adjacent nodes and `_NICR` falls between the two nodes' NICRs

```

### <a name="NC-72"></a>[NC-72] Style guide: Non-external/public function names should begin with an underscore
According to the Solidity Style Guide, non-`external`/`public` function names should begin with an [underscore](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables)

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/Dependencies/Auth.sol

 32:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/AuthNoOwner.sol

 30:     function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 35:     function decMul(uint256 x, uint256 y) internal pure returns (uint256 decProd) {
            uint256 prod_xy = x * y;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

```

### <a name="NC-73"></a>[NC-73] Style guide: Non-external/public variable names should begin with an underscore
According to the Solidity Style Guide, non-`external`/`public` variable names should begin with an [underscore](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables)

 There are 23 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 31:     uint256 internal systemCollShares; // deposited collateral tracker

 32:     uint256 internal systemDebt;

 33:     uint256 internal feeRecipientCollShares; // coll shares claimable by fee recipient

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 128:     ICollSurplusPool immutable collSurplusPool;

 152:     uint256 internal immutable deploymentStartTime;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 28:     uint256 internal totalSurplusCollShares;

 30:     mapping(address => uint256) internal balances;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 6:     uint256 internal constant DECIMAL_PRECISION = 1e18;

 18:     uint256 internal constant NICR_PRECISION = 1e20;

```


```solidity
File: packages/contracts/contracts/Dependencies/ReentrancyGuard.sol

 8:     uint256 internal constant OPEN = 1;

 9:     uint256 internal constant LOCKED = 2;

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 26:     EnumerableSet.AddressSet internal users;

 27:     EnumerableSet.AddressSet internal targets;

 28:     mapping(address => EnumerableSet.Bytes32Set) internal enabledFunctionSigsByTarget;

 30:     EnumerableSet.Bytes32Set internal enabledFunctionSigsPublic;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 17:     bytes32 NO_ROLES = bytes32(0);

 30:     mapping(uint8 => string) internal roleNames;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 35:     bool internal immutable willSweep;

 37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 12:     address internal immutable theOwner;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

 61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

```

### <a name="NC-74"></a>[NC-74] Style guide: State and local variables should be named using lowerCamelCase
The Solidity style guide [says](https://docs.soliditylang.org/en/latest/style-guide.html#local-and-state-variable-names) to use mixedCase for local and state variable names. Note that while OpenZeppelin may not follow this advice, it still is the recommended way of naming variables.

 There are 95 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 79:         uint256 oldICR;

 80:         uint256 newICR;

 81:         uint256 newTCR;

 91:         uint256 ICR;

 92:         uint256 NICR;

 421:             uint256 newNICR = _getNewNominalICRFromCdpChange(vars, _isDebtIncrease);

 482:         uint256 newTCR = _getNewTCRFromCdpChange(

 570:         uint256 newTCR = _getNewTCRFromCdpChange(

 910:     function _requireICRisNotBelowMCR(uint256 _newICR) internal pure {

 917:     function _requireICRisNotBelowCCR(uint256 _newICR) internal pure {

 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 921:     function _requireNoDecreaseOfICR(uint256 _newICR, uint256 _oldICR) internal pure {

 928:     function _requireNewTCRisNotBelowCCR(uint256 _newTCR) internal pure {

 999:         uint256 newNICR = EbtcMath._computeNominalCR(newCollShares, newDebt);

 1022:         uint256 newICR = EbtcMath._computeCR(

 1065:         uint256 newTCR = EbtcMath._computeCR(systemStEthBalance, systemDebt, _price);

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 193:             uint256 newNICR = EbtcMath._computeNominalCR(newColl, newDebt);

 246:         uint256 _EBTC,

 325:         uint256 _partialRedemptionHintNICR,

 600:         uint256 TCR = _computeTCRWithGivenSystemValues(_systemCollShares, _systemDebt, _price);

 613:         uint256 _ETHDrawn,

 615:         uint256 _totalEBTCSupply

 621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /

 655:     function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {

 662:         uint256 _stETHToRedeem

 669:         uint256 _ETHDrawn

 757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 93:         uint256 newTCR = EbtcMath._computeCR(

 168:     mapping(bytes32 => Cdp) public Cdps;

 193:     uint256 public lastEBTCDebtErrorRedistribution;

 205:     bytes32[] public CdpIds;

 306:     ) internal view returns (uint256 pendingEBTCDebtReward, uint256 _debtIndexDiff) {

 652:     function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {

 674:         (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 676:         uint256 NICR = EbtcMath._computeNominalCR(currentCollShares, currentEBTCDebt);

 693:         uint256 NICR = EbtcMath._computeNominalCR(_newColl, _newDebt);

 702:         (uint256 currentEBTCDebt, uint256 currentCollShares) = getSyncedDebtAndCollShares(_cdpId);

 703:         uint256 ICR = _calculateCR(currentCollShares, currentEBTCDebt, _price);

 721:     ) public view returns (uint256 pendingEBTCDebtReward) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 79:     function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

 85:     ) internal view returns (uint256 TCR, uint256 _coll, uint256 _debt) {

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcMath.sol

 36:         uint256 prod_xy = x * y;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 17:     bytes32 NO_ROLES = bytes32(0);

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 21:         uint256 minNetDebtInBTC;

 49:         uint256 _EBTCamount,

 57:             uint256 partialRedemptionHintNICR,

 58:             uint256 truncatedEBTCamount,

 139:         uint256 maxRedeemableEBTC = EbtcMath._min(vars.remainingEbtcToRedeem, currentCdpDebt);

 165:         uint256 _CR,

 186:             uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 9:     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 21:         uint256 _EBTCAmount,

 28:         uint _EBTCAmount,

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 27:         uint256 _EBTCAmount,

 31:         uint256 _partialRedemptionHintNICR,

 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 122:         uint256 ICR;

 126:         uint256 TCR;

 142:         uint256 ICR;

 156:         uint256 ICR;

 162:         uint256 TCR;

 167:         uint256 maxEBTCamount;

 171:         uint256 partialRedemptionHintNICR;

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 6:     event TCRNotified(uint256 TCR); /// NOTE: Mostly for debugging to ensure synch

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 9:     event NodeAdded(bytes32 _id, uint _NICR);

 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 39:         uint256 _ICR,

 45:         uint256 _ICR,

 52:         uint256 _ICR,

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 265:         bytes OperationData; // Generic Operation Data, which we'll decode to use

 315:         uint256 eBTCToMint;

 318:         uint256 stETHToDeposit;

 325:         uint256 _EBTCChange;

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 74:         uint256 _ICR = getCachedICR(_cdpId, _price); // @audit syncAccounting already called, guarenteed to be synced

 75:         (uint256 _TCR, uint256 systemColl, uint256 systemDebt) = _getTCRWithSystemDebtAndCollShares(

 468:         uint256 _newNICR,

 545:         uint256 _ICR,

 571:         uint256 _ICR,

 610:         uint256 _TCR,

 692:         (uint256 _TCR, uint256 systemColl, uint256 systemDebt) = _getTCRWithSystemDebtAndCollShares(

 745:         uint256 _TCR = _computeTCRWithGivenSystemValues(

 809:         uint256 _TCR,

 878:         uint256 EBTCDebtNumerator = (_debt * DECIMAL_PRECISION) + lastEBTCDebtErrorRedistribution;

 882:         uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 60:         address _collEthCLFeed,

 61:         address _ethBtcCLFeed

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 346:         uint256 _NICR,

 363:     function _insert(bytes32 _id, uint256 _NICR, bytes32 _prevId, bytes32 _nextId) internal {

 500:         uint256 _newNICR,

 584:         uint256 _NICR,

 592:         uint256 _NICR,

 619:     function _descendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

 642:     function _ascendList(uint256 _NICR, bytes32 _startId) internal view returns (bytes32, bytes32) {

 667:         uint256 _NICR,

 675:         uint256 _NICR,

```

### <a name="NC-75"></a>[NC-75] Style guide: Strings should use double quotes rather than single quotes
See the Solidity Style [Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#other-recommendations)

 There are 9 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 216:     // --- 'require' functions ---

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 623:     /// @notice Position managers with 'Persistent' status will be able to take actions indefinitely

 624:     /// @notice Position managers with 'OneTIme' status will be able to take a single action on one Cdp. Approval will be automatically revoked after one Cdp-related action.

 801:     // --- 'Require' wrapper functions ---

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 735:     // --- 'require' wrapper functions ---

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 460:      * Remove a Cdp owner from the CdpOwners array, not preserving array order. Removing owner 'B' does the following:

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 110:     // --- 'require' functions ---

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 293:     // --- 'require' functions ---

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 894:     // --- 'require' wrapper functions ---

```

### <a name="NC-76"></a>[NC-76] Style guide: Top level pragma declarations should be separated by two blank lines

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

### <a name="NC-77"></a>[NC-77] Style guide: Variable names for constants are improperly named
According to the [Style guide](https://docs.soliditylang.org/en/latest/style-guide.html#constants), for `constant` variable names, each word should use all capital letters, with underscores separating each word (CONSTANT_CASE)

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/SortedCdps.sol

 80:     bytes32 public constant dummyId =

```

### <a name="NC-78"></a>[NC-78] Style guide: Variable names for immutables should use CONSTANT_CASE
For `immutable` variable names, each word should use all capital letters, with underscores separating each word (CONSTANT_CASE)

 There are 44 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 26:     address public immutable borrowerOperationsAddress;

 27:     address public immutable cdpManagerAddress;

 28:     address public immutable collSurplusPoolAddress;

 34:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 53:     ICdpManager public immutable cdpManager;

 55:     ICollSurplusPool public immutable collSurplusPool;

 59:     IEBTCToken public immutable ebtcToken;

 62:     ISortedCdps public immutable sortedCdps;

```


```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 126:     address public immutable borrowerOperationsAddress;

 128:     ICollSurplusPool immutable collSurplusPool;

 130:     IEBTCToken public immutable override ebtcToken;

 132:     address public immutable liquidationLibrary;

 135:     ISortedCdps public immutable sortedCdps;

 152:     uint256 internal immutable deploymentStartTime;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 21:     address public immutable borrowerOperationsAddress;

 22:     address public immutable cdpManagerAddress;

 23:     address public immutable activePoolAddress;

 24:     address public immutable feeRecipientAddress;

 25:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/Dependencies/EbtcBase.sol

 41:     IActivePool public immutable activePool;

 43:     IPriceFeed public immutable override priceFeed;

 46:     ICollateralToken public immutable collateral;

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 55:     address public immutable cdpManagerAddress;

 56:     address public immutable borrowerOperationsAddress;

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 14:     ISortedCdps public immutable sortedCdps;

 15:     ICdpManager public immutable cdpManager;

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 29:     IBorrowerOperations public immutable borrowerOperations;

 30:     IActivePool public immutable activePool;

 31:     ICdpCdps public immutable cdpManager;

 32:     IEBTCToken public immutable ebtcToken;

 33:     ISortedCdps public immutable sortedCdps;

 34:     ICollateralToken public immutable stETH;

 35:     bool internal immutable willSweep;

```


```solidity
File: packages/contracts/contracts/LeverageMacroFactory.sol

 12:     address public immutable borrowerOperations;

 13:     address public immutable activePool;

 14:     address public immutable cdpManager;

 15:     address public immutable ebtcToken;

 16:     address public immutable stETH;

 17:     address public immutable sortedCdps;

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 12:     address internal immutable theOwner;

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 42:     address public immutable owner;

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 54:     address public immutable borrowerOperationsAddress;

 56:     ICdpManager public immutable cdpManager;

 58:     uint256 public immutable maxSize;

```

### <a name="NC-79"></a>[NC-79] TODO Left in the code
TODOs may signal that a feature is missing or not ready for audit, consider resolving the issue and removing the TODO comment

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 79:     //    Cdp ICR     |       Liquidation Behavior (TODO gas compensation?)

```

### <a name="NC-80"></a>[NC-80] Unused event definition
Note that there may be cases where an event superficially appears to be used, but this is only because there are multiple definitions of the event in different files. In such cases, the event definition should be moved into a separate file. The instances below are the unused definitions.

 There are 4 instances:

 ```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 9:     event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 7:     event FallbackTimeOutChanged(uint256 _oldTimeOut, uint256 _newTimeOut);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 9:     event ETHBalanceUpdated(uint256 _newBalance);

 10:     event EBTCBalanceUpdated(uint256 _newBalance);

```

### <a name="NC-81"></a>[NC-81] Unused public contract variable
Note that there may be cases where a variable superficially appears to be used, but this is only because there are multiple definitions of the variable in different files. In such cases, the variable definition should be moved into a separate file. The instances below are the unused variables.

 There are 8 instances:

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

### <a name="NC-82"></a>[NC-82] Unused file
The file is never imported by any other source file. If the file is needed for tests, it should be moved to a test directory.

 There are 2 instances:

 ```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 5: interface IPermitNonce {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 6: interface IOwnerLike {

```

### <a name="NC-83"></a>[NC-83] Unused function parameter
Comment out the variable name to suppress compiler warnings.

 There are 192 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 /// @audit  _cdpId
 99:     function liquidate(bytes32 _cdpId) external override {

 /// @audit  _cdpId
 109:     function partiallyLiquidate(
             bytes32 _cdpId,
             uint256 _partialAmount,
             bytes32 _upperPartialHint,
             bytes32 _lowerPartialHint
         ) external override {

 /// @audit  _partialAmount
 109:     function partiallyLiquidate(
             bytes32 _cdpId,
             uint256 _partialAmount,
             bytes32 _upperPartialHint,
             bytes32 _lowerPartialHint
         ) external override {

 /// @audit  _upperPartialHint
 109:     function partiallyLiquidate(
             bytes32 _cdpId,
             uint256 _partialAmount,
             bytes32 _upperPartialHint,
             bytes32 _lowerPartialHint
         ) external override {

 /// @audit  _lowerPartialHint
 109:     function partiallyLiquidate(
             bytes32 _cdpId,
             uint256 _partialAmount,
             bytes32 _upperPartialHint,
             bytes32 _lowerPartialHint
         ) external override {

 /// @audit  _cdpArray
 126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

 /// @audit  _price
 757:     function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {
             require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

```


```solidity
File: packages/contracts/contracts/Interfaces/IActivePool.sol

 /// @audit  _account
 23:     function transferSystemCollShares(address _account, uint256 _amount) external;

 /// @audit  _amount
 23:     function transferSystemCollShares(address _account, uint256 _amount) external;

 /// @audit  _value
 25:     function increaseSystemCollShares(uint256 _value) external;

 /// @audit  _account
 27:     function transferSystemCollSharesAndLiquidatorReward(

 /// @audit  _shares
 27:     function transferSystemCollSharesAndLiquidatorReward(

 /// @audit  _liquidatorRewardShares
 27:     function transferSystemCollSharesAndLiquidatorReward(

 /// @audit  _shares
 33:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external;

 /// @audit  _shares
 35:     function claimFeeRecipientCollShares(uint256 _shares) external;

 /// @audit  _feeRecipientAddress
 41:     function setFeeRecipientAddress(address _feeRecipientAddress) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IBorrowerOperations.sol

 /// @audit  _EBTCAmount
 20:     function openCdp(

 /// @audit  _upperHint
 20:     function openCdp(

 /// @audit  _lowerHint
 20:     function openCdp(

 /// @audit  _stEthBalance
 20:     function openCdp(

 /// @audit  _EBTCAmount
 27:     function openCdpFor(

 /// @audit  _upperHint
 27:     function openCdpFor(

 /// @audit  _lowerHint
 27:     function openCdpFor(

 /// @audit  _collAmount
 27:     function openCdpFor(

 /// @audit  _borrower
 27:     function openCdpFor(

 /// @audit  _cdpId
 35:     function addColl(

 /// @audit  _upperHint
 35:     function addColl(

 /// @audit  _lowerHint
 35:     function addColl(

 /// @audit  _stEthBalanceIncrease
 35:     function addColl(

 /// @audit  _cdpId
 42:     function withdrawColl(

 /// @audit  _stEthBalanceDecrease
 42:     function withdrawColl(

 /// @audit  _upperHint
 42:     function withdrawColl(

 /// @audit  _lowerHint
 42:     function withdrawColl(

 /// @audit  _cdpId
 49:     function withdrawDebt(

 /// @audit  _amount
 49:     function withdrawDebt(

 /// @audit  _upperHint
 49:     function withdrawDebt(

 /// @audit  _lowerHint
 49:     function withdrawDebt(

 /// @audit  _cdpId
 56:     function repayDebt(

 /// @audit  _amount
 56:     function repayDebt(

 /// @audit  _upperHint
 56:     function repayDebt(

 /// @audit  _lowerHint
 56:     function repayDebt(

 /// @audit  _cdpId
 63:     function closeCdp(bytes32 _cdpId) external;

 /// @audit  _cdpId
 65:     function adjustCdp(

 /// @audit  _stEthBalanceDecrease
 65:     function adjustCdp(

 /// @audit  _debtChange
 65:     function adjustCdp(

 /// @audit  isDebtIncrease
 65:     function adjustCdp(

 /// @audit  _upperHint
 65:     function adjustCdp(

 /// @audit  _lowerHint
 65:     function adjustCdp(

 /// @audit  _cdpId
 74:     function adjustCdpWithColl(

 /// @audit  _stEthBalanceDecrease
 74:     function adjustCdpWithColl(

 /// @audit  _debtChange
 74:     function adjustCdpWithColl(

 /// @audit  isDebtIncrease
 74:     function adjustCdpWithColl(

 /// @audit  _upperHint
 74:     function adjustCdpWithColl(

 /// @audit  _lowerHint
 74:     function adjustCdpWithColl(

 /// @audit  _stEthBalanceIncrease
 74:     function adjustCdpWithColl(

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManager.sol

 /// @audit  _index
 13:     function getIdFromCdpIdsArray(uint256 _index) external view returns (bytes32);

 /// @audit  _cdpId
 15:     function liquidate(bytes32 _cdpId) external;

 /// @audit  _cdpId
 17:     function partiallyLiquidate(

 /// @audit  _partialAmount
 17:     function partiallyLiquidate(

 /// @audit  _upperPartialHint
 17:     function partiallyLiquidate(

 /// @audit  _lowerPartialHint
 17:     function partiallyLiquidate(

 /// @audit  _cdpArray
 24:     function batchLiquidateCdps(bytes32[] calldata _cdpArray) external;

 /// @audit  _EBTCAmount
 26:     function redeemCollateral(

 /// @audit  _firstRedemptionHint
 26:     function redeemCollateral(

 /// @audit  _upperPartialRedemptionHint
 26:     function redeemCollateral(

 /// @audit  _lowerPartialRedemptionHint
 26:     function redeemCollateral(

 /// @audit  _partialRedemptionHintNICR
 26:     function redeemCollateral(

 /// @audit  _maxIterations
 26:     function redeemCollateral(

 /// @audit  _maxFee
 26:     function redeemCollateral(

 /// @audit  _cdpId
 36:     function updateStakeAndTotalStakes(bytes32 _cdpId) external returns (uint256);

 /// @audit  _cdpId
 38:     function syncAccounting(bytes32 _cdpId) external;

 /// @audit  _cdpId
 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 /// @audit  _borrower
 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 /// @audit  _debt
 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 /// @audit  _coll
 40:     function closeCdp(bytes32 _cdpId, address _borrower, uint256 _debt, uint256 _coll) external;

 /// @audit  _stETHToRedeem
 46:     function getRedemptionFeeWithDecay(uint256 _stETHToRedeem) external view returns (uint256);

 /// @audit  _cdpId
 48:     function getCdpStatus(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 50:     function getCdpStake(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 52:     function getCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 54:     function getCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 56:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);

 /// @audit  _cdpId
 58:     function initializeCdp(

 /// @audit  _debt
 58:     function initializeCdp(

 /// @audit  _coll
 58:     function initializeCdp(

 /// @audit  _liquidatorRewardShares
 58:     function initializeCdp(

 /// @audit  _borrower
 58:     function initializeCdp(

 /// @audit  _cdpId
 66:     function updateCdp(

 /// @audit  _borrower
 66:     function updateCdp(

 /// @audit  _coll
 66:     function updateCdp(

 /// @audit  _debt
 66:     function updateCdp(

 /// @audit  _newColl
 66:     function updateCdp(

 /// @audit  _newDebt
 66:     function updateCdp(

 /// @audit  _price
 75:     function getCachedTCR(uint256 _price) external view returns (uint256);

 /// @audit  _price
 77:     function checkRecoveryMode(uint256 _price) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICdpManagerData.sol

 /// @audit  _newIndex
 227:     function calcFeeUponStakingReward(

 /// @audit  _prevIndex
 227:     function calcFeeUponStakingReward(

 /// @audit  _cdpId
 236:     function getAccumulatedFeeSplitApplied(

 /// @audit  _systemStEthFeePerUnitIndex
 236:     function getAccumulatedFeeSplitApplied(

 /// @audit  _cdpId
 241:     function getCachedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  _price
 243:     function getCachedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  _cdpId
 245:     function getSyncedCdpDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 247:     function getSyncedCdpCollShares(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  _price
 249:     function getSyncedICR(bytes32 _cdpId, uint256 _price) external view returns (uint256);

 /// @audit  _price
 251:     function getSyncedTCR(uint256 _price) external view returns (uint256);

 /// @audit  _cdpId
 253:     function getSyncedNominalICR(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 255:     function getPendingRedistributedDebt(bytes32 _cdpId) external view returns (uint256);

 /// @audit  _cdpId
 257:     function hasPendingRedistributedDebt(bytes32 _cdpId) external view returns (bool);

 /// @audit  _cdpId
 259:     function getSyncedDebtAndCollShares(

 /// @audit  icr
 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

 /// @audit  tcr
 263:     function canLiquidateRecoveryMode(uint256 icr, uint256 tcr) external view returns (bool);

```


```solidity
File: packages/contracts/contracts/Interfaces/ICollSurplusPool.sol

 /// @audit  _account
 17:     function getSurplusCollShares(address _account) external view returns (uint256);

 /// @audit  _account
 19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

 /// @audit  _amount
 19:     function increaseSurplusCollShares(address _account, uint256 _amount) external;

 /// @audit  _account
 21:     function claimSurplusCollShares(address _account) external;

 /// @audit  _value
 23:     function increaseTotalSurplusCollShares(uint256 _value) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IEBTCToken.sol

 /// @audit  _account
 11:     function mint(address _account, uint256 _amount) external;

 /// @audit  _amount
 11:     function mint(address _account, uint256 _amount) external;

 /// @audit  _account
 13:     function burn(address _account, uint256 _amount) external;

 /// @audit  _amount
 13:     function burn(address _account, uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashBorrower.sol

 /// @audit  initiator
 15:     function onFlashLoan(

 /// @audit  token
 15:     function onFlashLoan(

 /// @audit  amount
 15:     function onFlashLoan(

 /// @audit  fee
 15:     function onFlashLoan(

 /// @audit  data
 15:     function onFlashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol

 /// @audit  token
 15:     function maxFlashLoan(address token) external view returns (uint256);

 /// @audit  token
 21:     function flashFee(address token, uint256 amount) external view returns (uint256);

 /// @audit  amount
 21:     function flashFee(address token, uint256 amount) external view returns (uint256);

 /// @audit  receiver
 28:     function flashLoan(

 /// @audit  token
 28:     function flashLoan(

 /// @audit  amount
 28:     function flashLoan(

 /// @audit  data
 28:     function flashLoan(

```


```solidity
File: packages/contracts/contracts/Interfaces/IFallbackCaller.sol

 /// @audit  newFallbackTimeout
 21:     function setFallbackTimeout(uint256 newFallbackTimeout) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPermitNonce.sol

 /// @audit  owner
 9:     function nonces(address owner) external view returns (uint256);

```


```solidity
File: packages/contracts/contracts/Interfaces/IPool.sol

 /// @audit  _amount
 19:     function increaseSystemDebt(uint256 _amount) external;

 /// @audit  _amount
 21:     function decreaseSystemDebt(uint256 _amount) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/IPositionManagers.sol

 /// @audit  _borrower
 18:     function getPositionManagerApproval(

 /// @audit  _positionManager
 18:     function getPositionManagerApproval(

 /// @audit  _positionManager
 23:     function setPositionManagerApproval(

 /// @audit  _approval
 23:     function setPositionManagerApproval(

 /// @audit  _positionManager
 28:     function revokePositionManagerApproval(address _positionManager) external;

 /// @audit  _borrower
 30:     function renouncePositionManagerApproval(address _borrower) external;

 /// @audit  _borrower
 32:     function permitPositionManagerApproval(

 /// @audit  _positionManager
 32:     function permitPositionManagerApproval(

 /// @audit  _approval
 32:     function permitPositionManagerApproval(

 /// @audit  _deadline
 32:     function permitPositionManagerApproval(

 /// @audit  v
 32:     function permitPositionManagerApproval(

 /// @audit  r
 32:     function permitPositionManagerApproval(

 /// @audit  s
 32:     function permitPositionManagerApproval(

```


```solidity
File: packages/contracts/contracts/Interfaces/IRecoveryModeGracePeriod.sol

 /// @audit  tcr
 13:     function notifyStartGracePeriod(uint256 tcr) external;

 /// @audit  tcr
 15:     function notifyEndGracePeriod(uint256 tcr) external;

```


```solidity
File: packages/contracts/contracts/Interfaces/ISortedCdps.sol

 /// @audit  _id
 14:     function remove(bytes32 _id) external;

 /// @audit  _ids
 16:     function batchRemove(bytes32[] memory _ids) external;

 /// @audit  _id
 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 /// @audit  _newICR
 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 /// @audit  _prevId
 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 /// @audit  _nextId
 18:     function reInsert(bytes32 _id, uint256 _newICR, bytes32 _prevId, bytes32 _nextId) external;

 /// @audit  _id
 20:     function contains(bytes32 _id) external view returns (bool);

 /// @audit  _id
 34:     function getNext(bytes32 _id) external view returns (bytes32);

 /// @audit  _id
 36:     function getPrev(bytes32 _id) external view returns (bytes32);

 /// @audit  _ICR
 38:     function validInsertPosition(

 /// @audit  _prevId
 38:     function validInsertPosition(

 /// @audit  _nextId
 38:     function validInsertPosition(

 /// @audit  _ICR
 44:     function findInsertPosition(

 /// @audit  _prevId
 44:     function findInsertPosition(

 /// @audit  _nextId
 44:     function findInsertPosition(

 /// @audit  owner
 50:     function insert(

 /// @audit  _ICR
 50:     function insert(

 /// @audit  _prevId
 50:     function insert(

 /// @audit  _nextId
 50:     function insert(

 /// @audit  _id
 57:     function getOwnerAddress(bytes32 _id) external pure returns (address);

 /// @audit  owner
 61:     function cdpCountOf(address owner) external view returns (uint256);

 /// @audit  owner
 63:     function getCdpCountOf(

 /// @audit  startNodeId
 63:     function getCdpCountOf(

 /// @audit  maxNodes
 63:     function getCdpCountOf(

 /// @audit  owner
 69:     function getCdpsOf(address owner) external view returns (bytes32[] memory);

 /// @audit  owner
 71:     function getAllCdpsOf(

 /// @audit  startNodeId
 71:     function getAllCdpsOf(

 /// @audit  maxNodes
 71:     function getAllCdpsOf(

 /// @audit  owner
 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 /// @audit  index
 77:     function cdpOfOwnerByIndex(address owner, uint256 index) external view returns (bytes32);

 /// @audit  owner
 79:     function cdpOfOwnerByIdx(

 /// @audit  index
 79:     function cdpOfOwnerByIdx(

 /// @audit  startNodeId
 79:     function cdpOfOwnerByIdx(

 /// @audit  maxNodes
 79:     function cdpOfOwnerByIdx(

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  amount
 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

 /// @audit  fee
 344:     function onFlashLoan(
             address initiator,
             address token,
             uint256 amount,
             uint256 fee,
             bytes calldata data
         ) external returns (bytes32) {

 /// @audit  _target
 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

 /// @audit  _gas
 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

 /// @audit  _value
 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

 /// @audit  _calldata
 498:     function excessivelySafeCall(
             address _target,
             uint256 _gas,
             uint256 _value,
             uint16 _maxCopy,
             bytes memory _calldata
         ) internal returns (bool, bytes memory) {

```

### <a name="NC-84"></a>[NC-84] Unused import
The identifier is imported but never used within the file.

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 /// @audit  ICdpManagerData
 11: import {ICdpManagerData} from "./Interfaces/ICdpManagerData.sol";

 /// @audit  ICdpManagerData
 11: import {ICdpManagerData} from "./Interfaces/ICdpManagerData.sol";

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 /// @audit  LeverageMacroBase
 4: import {LeverageMacroBase} from "./LeverageMacroBase.sol";

```

### <a name="NC-85"></a>[NC-85] Use bit shifts in an immutable variable rather than long bit masks of a single bit, for readability

 There are 1 instances:

 ```solidity
File: packages/contracts/contracts/SortedCdps.sol

 81:         0x0000000000000000000000000000000000000000000000000000000000000000;

```

### <a name="NC-86"></a>[NC-86] Use bytes.concat() on bytes instead of abi.encodePacked() for clearer semantic meaning
Starting with version 0.8.4, Solidity has the `bytes.concat()` function, which allows one to concatenate a list of bytes/strings, without extra padding. Using this function rather than `abi.encodePacked()` makes the intended operation more clear, leading to less reviewer confusion.

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 718:             abi.encodePacked(

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 210:             abi.encodePacked(

```


```solidity
File: packages/contracts/contracts/HintHelpers.sol

 182:             latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```

### <a name="NC-87"></a>[NC-87] Use of override is unnecessary.
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the `override` keyword when the function solely overrides an interface function, and the function doesn’t exist in multiple base contracts, is unnecessary.

 There are 103 instances:

 ```solidity
File: packages/contracts/contracts/ActivePool.sol

 74:     function getSystemCollShares() external view override returns (uint256) {

 82:     function getSystemDebt() external view override returns (uint256) {

 89:     function getFeeRecipientClaimableCollShares() external view override returns (uint256) {

 100:     function transferSystemCollShares(address _account, uint256 _shares) public override {

 129:     function transferSystemCollSharesAndLiquidatorReward(
             address _account,
             uint256 _shares,
             uint256 _liquidatorRewardShares
         ) external override {

 157:     function allocateSystemCollSharesToFeeRecipient(uint256 _shares) external override {

 194:     function increaseSystemDebt(uint256 _amount) external override {

 207:     function decreaseSystemDebt(uint256 _amount) external override {

 242:     function increaseSystemCollShares(uint256 _value) external override {

 261:     function flashLoan(
             IERC3156FlashBorrower receiver,
             address token,
             uint256 amount,
             bytes calldata data
         ) external override returns (bool) {

 317:     function flashFee(address token, uint256 amount) public view override returns (uint256) {

 328:     function maxFlashLoan(address token) public view override returns (uint256) {

 346:     function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {

```


```solidity
File: packages/contracts/contracts/BorrowerOperations.sol

 168:     function openCdp(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance
         ) external override nonReentrantSelfAndCdpM returns (bytes32) {

 187:     function openCdpFor(
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalance,
             address _borrower
         ) external override nonReentrantSelfAndCdpM returns (bytes32) {

 203:     function addColl(
             bytes32 _cdpId,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) external override nonReentrantSelfAndCdpM {

 219:     function withdrawColl(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 235:     function withdrawDebt(
             bytes32 _cdpId,
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 250:     function repayDebt(
             bytes32 _cdpId,
             uint256 _debt,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 270:     function adjustCdp(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint
         ) external override nonReentrantSelfAndCdpM {

 300:     function adjustCdpWithColl(
             bytes32 _cdpId,
             uint256 _stEthBalanceDecrease,
             uint256 _debtChange,
             bool _isDebtIncrease,
             bytes32 _upperHint,
             bytes32 _lowerHint,
             uint256 _stEthBalanceIncrease
         ) external override nonReentrantSelfAndCdpM {

 553:     function closeCdp(bytes32 _cdpId) external override {

 599:     function claimSurplusCollShares() external override {

 608:     function getPositionManagerApproval(
             address _borrower,
             address _positionManager
         ) external view override returns (PositionManagerApproval) {

 628:     function setPositionManagerApproval(
             address _positionManager,
             PositionManagerApproval _approval
         ) external override {

 647:     function revokePositionManagerApproval(address _positionManager) external override {

 653:     function renouncePositionManagerApproval(address _borrower) external override {

 665:     function domainSeparator() public view override returns (bytes32) {

 687:     function version() external pure override returns (string memory) {

 693:     function permitTypeHash() external pure override returns (bytes32) {

 706:     function permitPositionManagerApproval(
             address _borrower,
             address _positionManager,
             PositionManagerApproval _approval,
             uint256 _deadline,
             uint8 v,
             bytes32 r,
             bytes32 s
         ) external override {

 1077:     function flashLoan(
              IERC3156FlashBorrower receiver,
              address token,
              uint256 amount,
              bytes calldata data
          ) external override returns (bool) {

 1114:     function flashFee(address token, uint256 amount) public view override returns (uint256) {

 1124:     function maxFlashLoan(address token) public view override returns (uint256) {

```


```solidity
File: packages/contracts/contracts/CdpManager.sol

 66:     function getActiveCdpsCount() external view override returns (uint256) {

 73:     function getIdFromCdpIdsArray(uint256 _index) external view override returns (bytes32) {

 99:     function liquidate(bytes32 _cdpId) external override {

 109:     function partiallyLiquidate(
             bytes32 _cdpId,
             uint256 _partialAmount,
             bytes32 _upperPartialHint,
             bytes32 _lowerPartialHint
         ) external override {

 126:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

 320:     function redeemCollateral(
             uint256 _debt,
             bytes32 _firstRedemptionHint,
             bytes32 _upperPartialRedemptionHint,
             bytes32 _lowerPartialRedemptionHint,
             uint256 _partialRedemptionHintNICR,
             uint256 _maxIterations,
             uint256 _maxFeePercentage
         ) external override nonReentrantSelfAndBOps {
             RedemptionTotals memory totals;

 514:     function syncAccounting(bytes32 _cdpId) external virtual override {
             /// @audit Opening can cause invalid reordering of Cdps due to changing values without reInserting into sortedCdps

 523:     function updateStakeAndTotalStakes(bytes32 _cdpId) external override returns (uint256) {
             _requireCallerIsBorrowerOperations();

 538:     function closeCdp(
             bytes32 _cdpId,
             address _borrower,
             uint256 _debt,
             uint256 _coll
         ) external override {
             _requireCallerIsBorrowerOperations();

 580:     function getCachedTCR(uint256 _price) external view override returns (uint256) {
             return _getCachedTCR(_price);

 589:     function checkRecoveryMode(uint256 _price) external view override returns (bool) {
             return _checkRecoveryMode(_price);

 638:     function getRedemptionRate() public view override returns (uint256) {
             return _calcRedemptionRate(baseRate);

 643:     function getRedemptionRateWithDecay() public view override returns (uint256) {
             return _calcRedemptionRate(_calcDecayedBaseRate());

 661:     function getRedemptionFeeWithDecay(
             uint256 _stETHToRedeem
         ) external view override returns (uint256) {
             return _calcRedemptionFee(getRedemptionRateWithDecay(), _stETHToRedeem);

 856:     function getCdpStatus(bytes32 _cdpId) external view override returns (uint256) {
             return uint256(Cdps[_cdpId].status);

 863:     function getCdpStake(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].stake;

 871:     function getCdpDebt(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].debt;

 879:     function getCdpCollShares(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].coll;

 891:     function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view override returns (uint256) {
             return Cdps[_cdpId].liquidatorRewardShares;

```


```solidity
File: packages/contracts/contracts/CollSurplusPool.sol

 61:     function getTotalSurplusCollShares() external view override returns (uint256) {

 67:     function getSurplusCollShares(address _account) external view override returns (uint256) {

 77:     function increaseSurplusCollShares(address _account, uint256 _amount) external override {

 89:     function claimSurplusCollShares(address _account) external override {

 130:     function increaseTotalSurplusCollShares(uint256 _value) external override {

```


```solidity
File: packages/contracts/contracts/Dependencies/RolesAuthority.sol

 63:     function canCall(
            address user,
            address target,
            bytes4 functionSig
        ) public view virtual override returns (bool) {

```


```solidity
File: packages/contracts/contracts/EBTCToken.sol

 85:     function mint(address _account, uint256 _amount) external override {

 95:     function burn(address _account, uint256 _amount) external override {

 111:     function totalSupply() external view override returns (uint256) {

 115:     function balanceOf(address account) external view override returns (uint256) {

 119:     function transfer(address recipient, uint256 amount) external override returns (bool) {

 125:     function allowance(address owner, address spender) external view override returns (uint256) {

 129:     function approve(address spender, uint256 amount) external override returns (bool) {

 134:     function transferFrom(
             address sender,
             address recipient,
             uint256 amount
         ) external override returns (bool) {

 152:     function increaseAllowance(
             address spender,
             uint256 addedValue
         ) external override returns (bool) {

 160:     function decreaseAllowance(
             address spender,
             uint256 subtractedValue
         ) external override returns (bool) {

 182:     function domainSeparator() public view override returns (bytes32) {

 199:     function permit(
             address owner,
             address spender,
             uint256 amount,
             uint256 deadline,
             uint8 v,
             bytes32 r,
             bytes32 s
         ) external override {

 225:     function nonces(address owner) external view override(IERC2612, PermitNonce) returns (uint256) {

 331:     function name() external pure override returns (string memory) {

 337:     function symbol() external pure override returns (string memory) {

 343:     function decimals() external pure override returns (uint8) {

 349:     function version() external pure override returns (string memory) {

 355:     function permitTypeHash() external pure override returns (bytes32) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 63:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/LeverageMacroReference.sol

 44:     function owner() public override returns (address) {

```


```solidity
File: packages/contracts/contracts/PriceFeed.sol

 98:     function fetchPrice() external override returns (uint256) {

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 123:     function getOwnerAddress(bytes32 cdpId) public pure override returns (address) {

 130:     function nonExistId() public pure override returns (bytes32) {

 140:     function cdpOfOwnerByIndex(
             address owner,
             uint256 index
         ) external view override returns (bytes32) {

 155:     function cdpOfOwnerByIdx(
             address owner,
             uint256 index,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32, bool) {

 216:     function cdpCountOf(address owner) external view override returns (uint256) {

 227:     function getCdpCountOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (uint256, bytes32) {

 270:     function getCdpsOf(address owner) external view override returns (bytes32[] memory cdps) {

 286:     function getAllCdpsOf(
             address owner,
             bytes32 startNodeId,
             uint maxNodes
         ) external view override returns (bytes32[] memory, uint256, bytes32) {

 344:     function insert(
             address owner,
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external override returns (bytes32) {

 410:     function remove(bytes32 _id) external override {

 419:     function batchRemove(bytes32[] memory _ids) external override {

 498:     function reInsert(
             bytes32 _id,
             uint256 _newNICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external override {

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
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bool) {

 666:     function findInsertPosition(
             uint256 _NICR,
             bytes32 _prevId,
             bytes32 _nextId
         ) external view override returns (bytes32, bytes32) {

```

### <a name="NC-88"></a>[NC-88] Utility contracts can be made into libraries

 There are 3 instances:

 ```solidity
File: packages/contracts/contracts/CdpManager.sol

 16: contract CdpManager is CdpManagerStorage, ICdpManager, Proxy {

```


```solidity
File: packages/contracts/contracts/LeverageMacroDelegateTarget.sol

 40: contract LeverageMacroDelegateTarget is LeverageMacroBase {

```


```solidity
File: packages/contracts/contracts/LiquidationLibrary.sol

 13: contract LiquidationLibrary is CdpManagerStorage {

```

### <a name="NC-89"></a>[NC-89] Variables need not be initialized to zero
The default value for variables is zero, so initializing them to zero is superfluous.

 There are 18 instances:

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
File: packages/contracts/contracts/SortedCdps.sol

 182:         uint _currentIndex = 0;

 245:         uint _ownedCount = 0;

 246:         uint i = 0;

 311:         uint i = 0;

 432:         for (uint256 i = 0; i < _len; ++i) {

 449:         for (uint i = 0; i < _len; ++i) {

```

### <a name="NC-90"></a>[NC-90] Visibility should be set explicitly rather than defaulting to internal

 There are 6 instances:

 ```solidity
File: packages/contracts/contracts/CdpManagerStorage.sol

 128:     ICollSurplusPool immutable collSurplusPool;

```


```solidity
File: packages/contracts/contracts/Governor.sol

 17:     bytes32 NO_ROLES = bytes32(0);

```


```solidity
File: packages/contracts/contracts/LeverageMacroBase.sol

 37:     bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");

```


```solidity
File: packages/contracts/contracts/SimplifiedDiamondLike.sol

 39:     bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");

```


```solidity
File: packages/contracts/contracts/SortedCdps.sol

 60:     uint256 constant ADDRESS_SHIFT = 96; // 8 * 12; Puts the address at leftmost bytes32 position

 61:     uint256 constant BLOCK_SHIFT = 64; // 8 * 8; Puts the block value after the address

```