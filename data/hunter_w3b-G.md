# Gas-Optimization For Badger eBTC

## [G-01] Avoid contract existence checks by using low level calls

**Issue Description**\
Prior versions of Solidity inserted unnecessary contract existence checks for external function calls, wasting gas.

**Proposed Optimization**\
Avoid contract existence checks by using low level calls.For functions that make external calls with return values in Solidity <0.8.10, optimize the code to use low-level calls instead of regular calls. Low-level calls skip the unnecessary contract existence check.

Example:

```solidity
//Before:

contract C {
  function f() external returns(uint) {
    address(otherContract).call(abi.encodeWithSignature("func()"));
  }
}


//After:

contract C {
  function f() external returns(uint) {
    (bool success,) = address(otherContract).call(abi.encodeWithSignature("func()"));
    require(success);
    return decodeReturnValue();
  }
}
```

**Estimated Gas Savings**\
Up to 100 gas per external call by avoiding the EXTCODESIZE check for contract existence.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

183        collateral.transferShares(_account, _shares);

186            ICollSurplusPool(_account).increaseTotalSurplusCollShares(_shares);

272        uint256 oldRate = collateral.getPooledEthByShares(DECIMAL_PRECISION);

274        collateral.transfer(address(receiver), amount);

283        collateral.transferFrom(address(receiver), address(this), amountWithFee);

286        collateral.transfer(feeRecipientAddress, fee);

362        collateral.transferShares(feeRecipientAddress, _shares);

376        uint256 balance = IERC20(token).balanceOf(address(this));

381        IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L183

```solidity
File: contracts/contracts/BorrowerOperations.sol

363        vars.debt = cdpManager.getCdpDebt(_cdpId);

364        vars.collShares = cdpManager.getCdpCollShares(_cdpId);

564        uint256 collShares = cdpManager.getCdpCollShares(_cdpId);

565        uint256 debt = cdpManager.getCdpDebt(_cdpId);

566        uint256 liquidatorRewardShares = cdpManager.getCdpLiquidatorRewardShares(_cdpId);

792        ebtcToken.mint(_account, _debt);

798        ebtcToken.burn(_account, _debt);

1088        ebtcToken.mint(address(receiver), amount);

1100        ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

1103        ebtcToken.burn(feeRecipientAddress, amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L363

```solidity
File: contracts/contracts/CdpManager.sol

163                address _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId);

222                ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),

257        collSurplusPool.increaseSurplusCollShares(_borrower, _collSurplus + _liquidatorRewardShares);

742        uint256 callerBalance = ebtcToken.balanceOf(_redeemer);

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L163

```solidity
File: contracts/contracts/CollSurplusPool.sol

52        feeRecipientAddress = IActivePool(activePoolAddress).feeRecipientAddress();

107        collateral.transferShares(_account, claimableColl);

145        uint256 balance = IERC20(token).balanceOf(address(this));

148        IERC20(token).safeTransfer(feeRecipientAddress, amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L52

```solidity
File: contracts/contracts/Dependencies/EbtcBase.sol

89        uint256 _systemStEthBalance = collateral.getPooledEthByShares(systemCollShares);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L89

```solidity
File: contracts/contracts/HintHelpers.sol

66            vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

72                vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

73                vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

90                uint256 currentCdpDebt = cdpManager.getSyncedCdpDebt(vars.currentCdpId);

116                vars.currentCdpId = sortedCdps.getPrev(vars.currentCdpId);

117                vars.currentCdpUser = sortedCdps.getOwnerAddress(vars.currentCdpId);

141        uint256 newCollShare = cdpManager.getSyncedCdpCollShares(vars.currentCdpId);

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L66

```solidity
File: contracts/contracts/LeverageMacroBase.sol

129            IERC20(operation.tokenToTransferIn).safeTransferFrom(

148            IERC3156FlashLender(address(borrowerOperations)).flashLoan(

155            IERC3156FlashLender(address(activePool)).flashLoan(

220        uint256 ebtcBal = ebtcToken.balanceOf(address(this));

221        uint256 collateralBal = stETH.sharesOf(address(this));

228            stETH.transferShares(msg.sender, collateralBal);

237        IERC20(token).safeTransfer(msg.sender, amount);

405        IERC20(swapData.tokenForSwap).safeApprove(

427        IERC20(swapData.tokenForSwap).safeApprove(swapData.addressForApprove, 0);

441                    IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129

```solidity
File: contracts/contracts/LeverageMacroReference.sol

39        ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);

40        stETH.approve(_borrowerOperationsAddress, type(uint256).max);

41        stETH.approve(_activePool, type(uint256).max);

53        ebtcToken.approve(address(borrowerOperations), type(uint256).max);

54        stETH.approve(address(borrowerOperations), type(uint256).max);

55        stETH.approve(address(activePool), type(uint256).max);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39

```solidity
File: contracts/contracts/LiquidationLibrary.sol

530        ebtcToken.burn(msg.sender, totalDebtToBurn);

533        activePool.decreaseSystemDebt(totalDebtToBurn);

536        activePool.transferSystemCollSharesAndLiquidatorReward(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L530

## [G-02] Internal functions only called once can be inlined to save gas

**Issue Description**\
Internal functions that are only called once incur unnecessary gas costs due to function call overhead.

Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

**Proposed Optimization**\
Inline internal functions that are only called once to remove function call overhead and save gas.

**Estimated Gas Savings**\
20 to 40 gas per inlined internal function call by avoiding the extra JUMP instructions and stack operations.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

219    function _requireCallerIsBorrowerOperations() internal view {

235    function _requireCallerIsCdpManager() internal view {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L219

```solidity
File: contracts/contracts/Dependencies/Auth.sol

32    function isAuthorized(address user, bytes4 functionSig) internal view virtual returns (bool) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L32

```solidity
File: contracts/contracts/BorrowerOperations.sol

744    function _getCollSharesChangeFromStEthChange(

760    function _processTokenMovesFromAdjustment(MoveTokensParams memory _varMvTokens) internal {

783    function _activePoolAddColl(uint256 _stEthBalance, uint256 _sharesToTrack) internal {

803    function _requireSingularCollChange(

813    function _requireNonZeroAdjustment(

829    function _requireCdpIsNonExistent(bytes32 _cdpId) internal view {

834    function _requireNonZeroDebtChange(uint _debtChange) internal pure {

838    function _requireNotInRecoveryMode(uint256 _tcr) internal view {

845    function _requireNoStEthBalanceDecrease(uint256 _stEthBalanceDecrease) internal pure {

852    function _requireValidAdjustmentInCurrentMode(

946    function _requireValidDebtRepayment(uint256 _currentDebt, uint256 _debtRepayment) internal pure {

986    function _getNewNominalICRFromCdpChange(

1004    function _getNewICRFromCdpChange(

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L744

```solidity
File: contracts/contracts/CdpManager.sol

135    function _redeemCollateralFromCdp(

244    function _closeCdpByRedemption(

272    function _isValidFirstRedemptionHint(

489    function _getCdpIdsToRemove(

550    function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {

595    function _checkPotentialRecoveryMode(

612    function _updateBaseRateFromRedemption(

655    function _getRedemptionFee(uint256 _ETHDrawn) internal view returns (uint256) {

737    function _requireEbtcBalanceCoversRedemptionAndWithinSupply(

753    function _requireAmountGreaterThanZero(uint256 _amount) internal pure {

757    function _requireTCRisNotBelowMCR(uint256 _price, uint256 _TCR) internal view {

761    function _requireValidMaxFeePercentage(uint256 _maxFeePercentage) internal view {

977    function _setCdpCollShares(bytes32 _cdpId, uint256 _newColl) internal {

984    function _setCdpDebt(bytes32 _cdpId, uint256 _newDebt) internal {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L135

```solidity
File: contracts/contracts/CdpManagerStorage.sol

260    function _closeCdpWithoutRemovingSortedCdps(bytes32 _cdpId, Status closedStatus) internal {

293    function _updateSystemSnapshotsExcludeCollRemainder(uint256 _collRemainder) internal {

327    function _hasRedistributedDebt(bytes32 _cdpId) internal view returns (bool) {

336    function _updateRedistributedDebtIndex(bytes32 _cdpId) internal {

410    function _removeStake(bytes32 _cdpId) internal {

431    function _updateStakeForCdp(bytes32 _cdpId) internal returns (uint256, uint256) {

441    function _computeNewStake(uint256 _coll) internal view returns (uint256) {

463    function _removeCdp(bytes32 _cdpId, uint256 cdpIdsArrayLength) internal {

539    function _syncStEthIndex(uint256 _oldIndex, uint256 _newIndex) internal {

574    function _takeSplitAndUpdateFeePerUnit(

592    function _applyAccumulatedFeeSplit(

652    function _requireMoreThanOneCdpInSystem(uint256 CdpOwnersArrayLength) internal view {

895    function _recoveryModeGracePeriodPassed() internal view returns (bool) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L260

```solidity
File: contracts/contracts/CollSurplusPool.sol

112    function _requireCallerIsBorrowerOperations() internal view {

119    function _requireCallerIsCdpManager() internal view {

123    function _requireCallerIsActivePool() internal view {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L112

```solidity
File: contracts/contracts/Dependencies/EbtcBase.sol

75    function _getSystemDebt() internal view returns (uint256 entireSystemDebt) {

79    function _getCachedTCR(uint256 _price) internal view returns (uint256 TCR) {

83    function _getTCRWithSystemDebtAndCollShares(

134    function _checkICRAgainstMCR(uint256 _icr) internal view returns (bool) {

140    function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L75

```solidity
File: contracts/contracts/LeverageMacroBase.sol

450    function _ensureNotSystem(address addy) internal {

460    function _openCdpCallback(bytes memory data) internal {

474    function _closeCdpCallback(bytes memory data) internal {

482    function _adjustCdpCallback(bytes memory data) internal {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L450

```solidity
File: contracts/contracts/LiquidationLibrary.sol

450    function _partiallyReduceCdpDebt(

466    function _reInsertPartialLiquidation(

642    function _getLiquidationValuesRecoveryMode(

733    function _getTotalFromBatchLiquidate_RecoveryMode(

807    function _getTotalsFromBatchLiquidate_NormalMode(

862    function _redistributeDebt(uint256 _debt) internal {

896    function _requirePartialLiqDebtSize(

908    function _requirePartialLiqCollSize(uint256 _entireColl) internal pure {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L450

## [G-03] `<X> += <Y>` costs more gas than `<X> = <X> + <Y>` for state variables

**Issue Description**\
The compound assignment operators like +=, -= incur additional gas costs when used on state variables compared to regular assignment operators.

**Proposed Optimization**\
Use regular assignment operators instead of compound operators when modifying state variables.

**Estimated Gas Savings**\
100 gas saved per operation by avoiding the compound assignment operator on state variables.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/CdpManager.sol

697            lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L697

## [G-04] Splitting `require()` statements that use && saves gas

**Issue Description**\
Using the && operator in a single require statement incurs additional gas costs compared to splitting it into multiple requires.

**Proposed Optimization**\
For require statements using &&, split them into multiple require statements to avoid the && operator.

**Estimated Gas Savings**\
No estimate provided, but splitting && requires should save gas compared to a single require with &&.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

734       require(
735            recoveredAddress != address(0) && recoveredAddress == _borrower,
736            "BorrowerOperations: Invalid signature"
737        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L734-L737

```solidity
File: contracts/contracts/CdpManager.sol

762        require(
763            _maxFeePercentage >= redemptionFeeFloor && _maxFeePercentage <= DECIMAL_PRECISION,
764            "Max fee percentage must be between redemption fee floor and 100%"
765        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L762

```solidity
File: contracts/contracts/CdpManagerStorage.sol

261        require(
262            closedStatus != Status.nonExistent && closedStatus != Status.active,
263            "CdpManagerStorage: close non-exist or non-active CDP!"
264        );


466        require(
467            cdpStatus != Status.nonExistent && cdpStatus != Status.active,
468            "CdpManagerStorage: remove non-exist or non-active CDP!"
469        );

653     require(
654            CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,
655            "CdpManager: Only one cdp in the system"
656        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L261

```solidity
File: contracts/contracts/EBTCToken.sol

296        require(
297            _recipient != address(0) && _recipient != address(this),
298            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
299        );


300        require(
301            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
302            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
303        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L296

```solidity
File: contracts/contracts/PriceFeed.sol

79        require(
80            !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
81                !_chainlinkIsFrozen(chainlinkResponse),
82            "PriceFeed: Chainlink must be working and current"
83        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L79

## [G-05] Using fixed bytes is cheaper than using string

**Issue Description**\
Using fixed-size byte types like bytes1-bytes32 is more efficient in Solidity than flexible-size bytes or string types.

**Proposed Optimization**\
For data that can fit into a fixed size of 1-32 bytes, use the corresponding bytes1-bytes32 type rather than bytes or string.

**Estimated Gas Savings**\
No estimate provided, but fixed-size byte types are intrinsically more gas efficient to use and evaluate than variable-size bytes or string.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

24    string public constant NAME = "ActivePool";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L24

```solidity
File: contracts/contracts/BorrowerOperations.sol

29    string public constant NAME = "BorrowerOperations";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L29

```solidity
File: contracts/contracts/CdpManagerStorage.sol

122    string public constant NAME = "CdpManager";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L122

```solidity
File: contracts/contracts/CollSurplusPool.sol

19    string public constant NAME = "CollSurplusPool";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L19

```solidity
File: contracts/contracts/HintHelpers.sol

12    string public constant NAME = "HintHelpers";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L12

```solidity
File: contracts/contracts/PriceFeed.sol

22    string public constant NAME = "PriceFeed";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L22

```solidity
File: contracts/contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52

## [G-06] Make constructors payable

**Issue Description**\
Making the constructor payable saved 200 gas on deployment. This is because non-payable functions have an implicit require(msg.value == 0) inserted in them. Additionally, fewer bytecode at deploy time mean less gas cost due to smaller calldata.

There are good reasons to make a regular functions non-payable, but generally a contract is deployed by a privileged address who you can reasonably assume won’t send ether. This might not apply if inexperienced users are deploying the contract.

**Proposed Optimization**\
Make the constructor function payable to avoid the implicit require(msg.value == 0) check and reduce bytecode size for deployment.

Example:

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity 0.8.20;

contract A {}

contract B {
    constructor() payable {}
}
```

**Estimated Gas Savings**\
200 gas saved per deployment by making the constructor payable.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

46    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L46

```solidity
File: contracts/contracts/Dependencies/Auth.sol

18    constructor(address _owner, Authority _authority) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L18

```solidity
File: contracts/contracts/BorrowerOperations.sol

107    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L107

```solidity
File: ontracts/contracts/CdpManager.sol

30    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L30

```solidity
File: contracts/contracts/CdpManagerStorage.sol

217    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L217

```solidity
File: contracts/contracts/CollSurplusPool.sol

42    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L42

```solidity
File: contracts/contracts/Dependencies/EbtcBase.sol

52    constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L52

```solidity
File: contracts/contracts/EBTCToken.sol

61    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L61

```solidity
File: contracts/contracts/Governor.sol

36    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L36

```solidity
File: contracts/contracts/HintHelpers.sol

27    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L27

```solidity
File: contracts/contracts/LeverageMacroBase.sol

51    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L51

```solidity
File: contracts/contracts/LeverageMacroDelegateTarget.sol

41    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L41

```solidity
File: contracts/contracts/LeverageMacroFactory.sol

21    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L21

```solidity
File: contracts/LeverageMacroReference.sol

17    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L17

```solidity
File: contracts/LiquidationLibrary.sol

14    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L14

```solidity
File: contracts/contracts/PriceFeed.sol

57    constructor(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L57

```solidity
File: contracts/contracts/Dependencies/RolesAuthority.sol

20    constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L20

```solidity
File: contracts/contracts/SimplifiedDiamondLike.sol

44    constructor(address _owner) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L44

```solidity
File: contracts/SortedCdps.sol

88    constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L88

## [G-07] Expressions for constant values such as a call to keccak256(), should use immutable rather than constant

**Issue Description**\
The code is declaring a value computed from keccak256 as constant. However, constant implies the value can be evaluated at compile time, which is not the case for keccak256. immutable is more appropriate since it indicates the value is set once at deployment and cannot change after that.

**Proposed Optimization**\
Change bytes32 private constant to bytes32 private immutable for `_PERMIT_POSITION_MANAGER_TYPEHASH`

**Estimated Gas Savings**\
Using immutable rather than constant for values computed at deployment like keccak256 hashes avoids re-evaluating the expression each time the state is accessed. This could save up to ~200 gas per access depending on the specific expression.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

32    bytes32 private constant _PERMIT_POSITION_MANAGER_TYPEHASH =
33        keccak256(
34            "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
35        );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L32-L35

```solidity
File: contracts/Dependencies/ERC3156FlashLender.sol

11    bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11

```solidity
File: contracts/contracts/LeverageMacroBase.sol

37    bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37

```solidity
File: contracts/contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39

## [G-08] Mulitiple `Address/Id` mappings can be combined into a single mapping of an `Address/Id `to a struct

**Issue Description**\
The contract declares separate mappings for position managers and their approval status:

```solidity
mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;
```

This uses multiple storage slots that could potentially be combined.

**Proposed Optimization**\
Combine the mappings into a single mapping from an owner to a struct containing the manager and approval status:

```solidity
struct ManagerApproval {
  address manager;
  PositionManagerApproval status;
}

mapping(address => ManagerApproval[]) public managerApprovals;
```

**Estimated Gas Savings**\
Saves 1 storage slot per owner
Writes and reads of related data avoided ~42 gas per access vs separate mappings
Initial setup avoids 20,000 gas (Gset) per mapping

Potential savings of ~20,000 - 42 gas per transaction that reads or writes both fields for an owner.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

65    mapping(address => mapping(address => PositionManagerApproval)) public positionManagers;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L65

```solidity
File: contracts/contracts/EBTCToken.sol

52    mapping(address => mapping(address => uint256)) private _allowances;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L52

```solidity
File: contracts/Dependencies/RolesAuthority.sol

34    mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36    mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34

## [G-09] Avoid zero transfer to save Gas

**Issue Description**\
The `_transferCollSharesWithContractHooks` function transfers collateral shares without first checking if the amount is zero. This wastes gas by still executing the transfer even if no shares are being transferred.

**Proposed Optimization**\
Add a check before the transfer to avoid it if the amount is zero:

```solidity
function _transferCollSharesWithContractHooks(address _account, uint256 _shares) internal {

  if (_shares == 0) {
    return;
  }

  // transfer shares
  collateral.transferShares(_account, _shares);

  // rest of function
}
```

**Estimated Gas Savings**\
Executing an unnecessary transfer wastes at minimum:

collateral.transferShares() function call gas (~600 gas) Plus any additional code inside the transfer function Could save 600+ gas per call if amount is zero.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

183        collateral.transferShares(_account, _shares);


274        collateral.transfer(address(receiver), amount);

283        collateral.transferFrom(address(receiver), address(this), amountWithFee);

286        collateral.transfer(feeRecipientAddress, fee);

362        collateral.transferShares(feeRecipientAddress, _shares);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L181

```solidity
File: contracts/contracts/BorrowerOperations.sol

785        collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

1100        ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785

## [G-10] Using storage instead of memory for Structs/Arrays Save Gas

**Issue Description**\
When fetching data from storage into a memory variable, it incurs a gas cost (Gcoldsload of 2100 gas) to read each field of the struct/array from storage into memory.

If fields are then accessed from the memory variable, it incurs an additional MLOAD gas cost rather than a cheaper stack read.

**Proposed Optimization**\
Instead of declaring the variable with memory, declare it with storage and cache any repeatedly read fields in stack variables. This only incurs the single Gcoldsload cost to fetch the struct/array, rather than per field.

**Estimated Gas Savings**\
Savings of 2100 gas per avoided Gcoldsload operation.

For a struct/array with multiple fields, the total savings would be `2100 * (number of fields - 1)`.
**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

345        AdjustCdpLocals memory vars;

427            MoveTokensParams memory _varMvTokens = MoveTokensParams(

449        OpenCdpLocals memory vars;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L345

```solidity
File: contracts/contracts/HintHelpers.sol

62        LocalVariables_getRedemptionHints memory vars;

134        LocalVariables_getRedemptionHints memory vars,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L62

```solidity
File: contracts/contracts/LeverageMacroBase.sol

339        LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

374        LeverageMacroOperation memory operation = decodeFLData(data);

461        OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

475        CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483        AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339

## [G-11] Use constants instead of `type(uintx).max`

**Issue Description**\
Using type(uint).max (or other max values like type(uint256).max) to represent a maximum value incurs unnecessary gas costs compared to using a constant.

**Proposed Optimization**\
Define constants for common max values rather than querying the type info on each use:

```solidity
uint256 private constant MAX_UINT256 = 2**256 - 1;
```

**Estimated Gas Savings**

- Type queries like type(T).max cost ~200 gas each time
- Referencing a constant is essentially free

Gas savings of ~200 gas per usage of the max value.

For frequently used values this can amount to thousands of gas saved per transaction.
Example

Before:

```solidity
function sample(uint x) public {
  if (x > type(uint256).max) {
   //...
  }
}
```

After:

```solidity
uint256 private constant MAX_UINT256 = 2**256 - 1;

function sample(uint x) public {
  if (x > MAX_UINT256) {
   //...
  }
}
```

This avoids an unnecessary 200 gas type query on each call.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/Governor.sol

76        for (uint8 i = 0; i < type(uint8).max; i++) {

84            for (uint8 i = 0; i < type(uint8).max; i++) {

98        for (uint8 i = 0; i < type(uint8).max; i++) {

107            for (uint8 i = 0; i < type(uint8).max; i++) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76

```solidity
File: contracts/contracts/LeverageMacroReference.sol

39        ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);

40        stETH.approve(_borrowerOperationsAddress, type(uint256).max);

41        stETH.approve(_activePool, type(uint256).max);

53        ebtcToken.approve(address(borrowerOperations), type(uint256).max);

54        stETH.approve(address(borrowerOperations), type(uint256).max);

55        stETH.approve(address(activePool), type(uint256).max);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39

```solidity
File: contracts/contracts/EBTCToken.sol

143        if (cachedAllowance != type(uint256).max) {

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L143

```solidity
File: contracts/contracts/HintHelpers.sol

79            _maxIterations = type(uint256).max;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L79

## [G-12] Use nested If and avoid multiple check combinations &&

**Issue Description**\
When multiple conditions are checked using &&, the second condition is evaluated even if the first fails, wasting gas.

**Proposed Optimization**\
Replace multiple && checks with nested if statements to short-circuit evaluation:

```solidity
// Before
if (cond1 && cond2) {
  //...
}

// After
if (cond1) {
  if (cond2) {
    //...
  }
}
```

**Estimated Gas Savings**\
Each avoided condition check saves ~3 gas for the evaluation.

For 'n' conditions checked, total gas savings is ~3n gas.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

393        if (!_isDebtIncrease && _debtChange > 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L393

```solidity
File:  contracts/contracts/CdpManagerStorage.sol

512        if (_newIndex > _oldIndex && totalStakes > 0) {

765        if (_newIndex > _oldIndex && totalStakes > 0) {

796        if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L512

```solidity
File: contracts/contracts/LiquidationLibrary.sol

157            if (
158                liquidationValues.totalCollToSendToLiquidator == 0 &&
159                liquidationValues.debtToBurn == 0
160            ) {

756            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {

759                if (
760                    !vars.backToNormalMode &&
761                    (_checkICRAgainstMCR(vars.ICR) || canLiquidateRecoveryMode(vars.ICR, _TCR))
762                ) {

790                } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {

819            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L157

```solidity
File: contracts/contracts/PriceFeed.sol

226                if (
227                    !_chainlinkIsBroken(chainlinkResponse, prevChainlinkResponse) &&
228                    !_chainlinkIsFrozen(chainlinkResponse)
229                ) {


372                if (
373                    !_fallbackIsBroken(fallbackResponse) &&
374                    !_responseTimeout(fallbackResponse.timestamp, newFallbackCaler.fallbackTimeout())
375                ) {


666        if (
667            _checkHealthyCLResponse(chainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
668            _checkHealthyCLResponse(chainlinkResponse.roundStEthEthId, stEthEthAnswer)
669        ) {


754        if (
755            _checkHealthyCLResponse(prevChainlinkResponse.roundEthBtcId, ethBtcAnswer) &&
756            _checkHealthyCLResponse(prevChainlinkResponse.roundStEthEthId, stEthEthAnswer)
757        ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L226

```solidity
File: contracts/contracts/SortedCdps.sol

202            if (maxNodes > 0 && i >= maxNodes) {

259            if (maxNodes > 0 && i >= maxNodes) {

330            if (maxNodes > 0 && i >= maxNodes) {

382        if (prevId == dummyId && nextId == dummyId) {

596        if (_prevId == dummyId && _nextId == dummyId) {

621        if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {

644        if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {

696        if (prevId == dummyId && nextId == dummyId) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L202

## [G-13] Use Assembly to write Address Storage Value

**Issue Description**\
Storing an address value to storage using the regular assignment operator = compiles to an SSTORE opcode with a doubled storage slot.

**Proposed Optimization**\
Use inline assembly to write address values directly to storage with a single slot:

assembly:

```solidity
function setAddress(address _addr) external {
  assembly {
    sstore(0, _addr)
  }
}
```

**Estimated Gas Savings**\

- Regular assignment compiles to a double slot SSTORE costing 20000 gas
- Using direct assembly costs 5000 gas for a single slot SSTORE

Savings of 15000 gas per address storage write.
**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

26    address public immutable borrowerOperationsAddress;

27    address public immutable cdpManagerAddress;

28    address public immutable collSurplusPoolAddress;

29    address public feeRecipientAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L26

```solidity
File: contracts/Dependencies/Auth.sol

14    address public owner;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L14

```solidity
File: contracts/BorrowerOperations.sol

57    address public feeRecipientAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L57

```solidity
File: contracts/contracts/CdpManagerStorage.sol

126    address public immutable borrowerOperationsAddress;

132    address public immutable liquidationLibrary;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L126

```solidity
File: contracts/contracts/CollSurplusPool.sol

21    address public immutable borrowerOperationsAddress;

22    address public immutable cdpManagerAddress;

23    address public immutable activePoolAddress;

24    address public immutable feeRecipientAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L21

```solidity
File: contracts/contracts/EBTCToken.sol

55    address public immutable cdpManagerAddress;

56    address public immutable borrowerOperationsAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L55

```solidity
File: contracts/contracts/LeverageMacroFactory.sol

12    address public immutable borrowerOperations;
13    address public immutable activePool;
14    address public immutable cdpManager;
15    address public immutable ebtcToken;
16    address public immutable stETH;
17    address public immutable sortedCdps;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12

```solidity
File: contracts/SimplifiedDiamondLike.sol

42    address public immutable owner;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L42

## [G-14] A modifier used only once and not being inherited should be inlined to save gas

**Issue Description**\
Declaring a modifier that is only used once in a contract wastes gas, as it requires jump code to be inserted.

**Proposed Optimization**\
For modifiers used only once locally, inline the code directly rather than using a modifier.

**Estimated Gas Savings**\

- Modifier declaration costs ~5000 gas
- Each use inserts ~3 gas for a jump

Savings of 5000 gas for single use modifier.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/Dependencies/Auth.sol

// @audit this modifier is onle used once
26    modifier requiresAuth() virtual {
27        require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");
28
29        _;
30    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L26-L30

## [G-15] `abi.encode()` is less efficient than `abi.encodePacked()`

**Issue Description**\
Using abi.encode() to encode function arguments inserts padding between parameters to ensure 32-byte alignment, making it less gas efficient than abi.encodePacked().

**Proposed Optimization**\
Use abi.encodePacked() instead of abi.encode() when encoding function call data, unless the calling contract expects 32-byte alignment.

**Estimated Gas Savings**\

- abi.encode() includes padded zero bytes between parameters
- abi.encodePacked() packs parameters together tightly
- Padding can increase encoded size by up to 3x
- Encoding consumes 5-10 gas per byte

Potential savings of 5-30 gas per encoded parameter set.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

682        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

722                    abi.encode(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682

```solidity
File: contracts/contracts/EBTCToken.sol

214                    abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)

240        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L214

```solidity
File: contracts/contracts/LeverageMacroBase.sol

152                abi.encode(operation)

159                abi.encode(operation)
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L152

## [G-16] Do not calculate constants

**Issue Description**\
Calculating values at compile time that can be declared as constants wastes gas.

**Proposed Optimization**\
Declare common calculations as constants rather than computing them dynamically.

**Estimated Gas Savings**\

- Calculating a value costs gas each time
- Referencing a constant is essentially free

Savings of a few hundred gas or more per avoided calculation.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141

## [G-17] Use hardcode address instead address(this)

**Issue Description**\
The code is using address(this) to reference the contract itself. This requires a SLOAD to lookup the contract address on each call, wasting gas.

**Proposed Optimization**\
Hardcode the contract address save to a state variable then used that state variable rather than using address(this).

**Estimated Gas Savings**\
An SLOAD operation costs approximately 200 gas. By hardcoding the address, it avoids this lookup on every call, saving 200 gas per avoidance.

For contracts with many internal calls between addresses, the potential savings could reach thousands of gas.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

283        collateral.transferFrom(address(receiver), address(this), amountWithFee);

295            collateral.balanceOf(address(this)) >= collateral.getPooledEthByShares(systemCollShares),

299            collateral.sharesOf(address(this)) >= systemCollShares,

337        return collateral.balanceOf(address(this));

376        uint256 balance = IERC20(token).balanceOf(address(this));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L283

```solidity
File: contracts/contracts/Dependencies/Auth.sol

38            (address(auth) != address(0) && auth.canCall(user, address(this), functionSig)) ||

45        require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L38

```solidity
File: contracts/contracts/Dependencies/AuthNoOwner.sol

35        return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));

41        require(_authority.canCall(msg.sender, address(this), msg.sig));

62        emit AuthorityUpdated(address(this), Authority(newAuthority));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L35

```solidity
File: contracts/contracts/EBTCToken.sol

240        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));

297            _recipient != address(0) && _recipient != address(this),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240

```solidity
File: contracts/contracts/LeverageMacroBase.sol

131                address(this),

143            initialCdpIndex = sortedCdps.cdpCountOf(address(this));

149                IERC3156FlashBorrower(address(this)),

156                IERC3156FlashBorrower(address(this)),

173            bytes32 cdpId = sortedCdps.cdpOfOwnerByIndex(address(this), initialCdpIndex);

220        uint256 ebtcBal = ebtcToken.balanceOf(address(this));

221        uint256 collateralBal = stETH.sharesOf(address(this));

352        require(initiator == address(this), "LeverageMacroReference: wrong initiator for flashloan");

441                    IERC20(swapChecks[i].tokenToCheck).balanceOf(address(this)) >

456        require(addy != address(this)); // If it could call this it could fake the forwarded caller
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L131

## [G-18] Using delete statement can save gas

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/CdpManagerStorage.sol

272        Cdps[_cdpId].coll = 0;

273        Cdps[_cdpId].debt = 0;

274        Cdps[_cdpId].liquidatorRewardShares = 0;

276        cdpDebtRedistributionIndex[_cdpId] = 0;

277        cdpStEthFeePerUnitIndex[_cdpId] = 0;

413        Cdps[_cdpId].stake = 0;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L272

```solidity
File: contracts/contracts/HintHelpers.sol

105                        partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

106                        partialRedemptionNewColl = 0;

109                        vars.remainingEbtcToRedeem = 0;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105

## [G-19] Shorten the array rather than copying to a new one

**Issue Description**\
When an element is removed from an array, Solidity currently creates a new, shorter array and copies the remaining elements over. This wastes gas.

**Proposed Optimization**\
Instead of copying to a new array, use inline assembly to directly modify the length slot of the array. This shortens the array in-place without needing to copy elements.

**Estimated Gas Savings**\
Creating and copying a new array is very expensive - it costs O(n) gas where n is the number of elements.

Modifying the length slot directly is a constant gas cost regardless of array size.

For even moderately sized arrays, this can save thousands of gas or more per remove operation.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/CdpManager.sol

496        bytes32[] memory _toRemoveIds = new bytes32[](_total);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L496

```solidity
File: contracts/contracts/Governor.sol

106            roleIds = new uint8[](count);

136            _funcs = new bytes4[](_sigs.length);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L106

```solidity
File: contracts/contracts/LeverageMacroBase.sol

508        bytes memory _returnData = new bytes(_maxCopy);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L508

```solidity
File: contracts/contracts/LiquidationLibrary.sol

751        bool[] memory _liqFlags = new bool[](_cnt);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L751

```solidity
File: contracts/contracts/SortedCdps.sol

310        bytes32[] memory userCdps = new bytes32[](maxArraySize);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L310

## [G-20] Use assembly to validate msg.sender

**Issue Description**\
Validating msg.sender on every function call using Solidity require() wastes gas due to overhead of the require function.

**Proposed Optimization**\
Use inline assembly to directly compare msg.sender to the expected address, avoiding the overhead of require().

Example:

Solidity validation:

```solidity
function foo() public {
  require(msg.sender == owner, "Not owner");
}
```

Assembly validation:

```solidity
function foo() public {
  let x := caller()
  let y := ownerAddress
  if eq(x, y) {
    //...
  } else {
    revert(0,0)
  }
}
```

**Estimated Gas Savings**

- require() costs ~500 gas overhead per validation
- A direct assembly comparison is ~200 gas

Potential savings of 300 gas or more per msg.sender validation.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

220     require(
221            msg.sender == borrowerOperationsAddress,
222            "ActivePool: Caller is not BorrowerOperations"
223        );

229            msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,

236        require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L221

```solidity
File: contracts/contracts/Dependencies/Auth.sol

45        require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L45

```solidity
File: contracts/contracts/CdpManagerStorage.sol

661            msg.sender == borrowerOperationsAddress,
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L661

```solidity
File: contracts/contracts/CollSurplusPool.sol

114            msg.sender == borrowerOperationsAddress,

120        require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124        require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L114

```solidity
File: contracts/contracts/EBTCToken.sol

308            msg.sender == borrowerOperationsAddress,

316            msg.sender == borrowerOperationsAddress ||
317                msg.sender == cdpManagerAddress ||

324        require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L308

```solidity
File: contracts/contracts/LeverageMacroBase.sol

357                msg.sender == address(borrowerOperations),

363                msg.sender == address(activePool),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L357

```solidity
File: contracts/contracts/SimplifiedDiamondLike.sol

52        require(msg.sender == owner);

67        require(msg.sender == owner);

77        require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111        require(msg.sender == owner, "Must be owner");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52

```solidity
File: contracts/contracts/SortedCdps.sol

715        require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

721            msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L715

## [G-21] Make 3 event parameters indexed when possible

**Issue Description**\
Events with non-indexed parameters are expensive to filter on. It's more gas efficient to make parameters indexed when filtering is needed.

It's the most gas efficient to make up to 3 event parameters indexed. If there are less than 3 parameters, you need to make all parameters indexed.

**Proposed Optimization**\
Audit events to identify opportunities to make up to 3 parameters indexed to optimize for filtering use cases.

**Estimated Gas Savings**

- Non-indexed parameters cost 800 gas to insert
- Indexed parameters cost 200 gas

Savings of 600 gas per parameter indexed in an event that is frequently filtered.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/Interfaces/IActivePool.sol

9     event ActivePoolEBTCDebtUpdated(uint256 _EBTCDebt);
10    event SystemCollSharesUpdated(uint256 _coll);
12    event FeeRecipientClaimableCollSharesIncreased(uint256 _coll, uint256 _fee);
13    event FeeRecipientClaimableCollSharesDecreased(uint256 _coll, uint256 _fee);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IActivePool.sol#L

```solidity
File: contracts/contracts/Interfaces/ICdpManagerData.sol

17    event StakingRewardSplitSet(uint256 _stakingRewardSplit);
18    event RedemptionFeeFloorSet(uint256 _redemptionFeeFloor);
19    event MinuteDecayFactorSet(uint256 _minuteDecayFactor);
20    event BetaSet(uint256 _beta);
21    event RedemptionsPaused(bool _paused);

23    event Liquidation(uint256 _liquidatedDebt, uint256 _liquidatedColl, uint256 _liqReward);
24    event Redemption(
        uint256 _debtToRedeemExpected,
        uint256 _debtToRedeemActual,
        uint256 _collSharesSent,
        uint256 _feeCollShares,
        address indexed _redeemer
    );

60    event BaseRateUpdated(uint256 _baseRate);
61    event LastRedemptionTimestampUpdated(uint256 _lastFeeOpTime);
62    event TotalStakesUpdated(uint256 _newTotalStakes);
63    event SystemSnapshotsUpdated(uint256 _totalStakesSnapshot, uint256 _totalCollateralSnapshot);
64    event SystemDebtRedistributionIndexUpdated(uint256 _systemDebtRedistributionIndex);
65    event CdpDebtRedistributionIndexUpdated(bytes32 _cdpId, uint256 _cdpDebtRedistributionIndex);
66    event CdpArrayIndexUpdated(bytes32 _cdpId, uint256 _newIndex);
67    event StEthIndexUpdated(uint256 _oldIndex, uint256 _newIndex, uint256 _updTimestamp);
68    event CollateralFeePerUnitUpdated(uint256 _oldPerUnit, uint256 _newPerUnit, uint256 _feeTaken);
69    event CdpFeeSplitApplied(
70        bytes32 _cdpId,
71        uint256 _oldPerUnitCdp,
72        uint256 _newPerUnitCdp,
73        uint256 _collReduced,
74        uint256 _collLeft
75    );
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ICdpManagerData.sol#L17

```solidity
File: contracts/Interfaces/IERC3156FlashLender.sol

8    event FlashFeeSet(address indexed _setter, uint256 _oldFee, uint256 _newFee);
9    event MaxFlashFeeSet(address indexed _setter, uint256 _oldMaxFee, uint256 _newMaxFee);
10    event FlashLoansPaused(address indexed _setter, bool _paused);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L8

```solidity
File: contracts/Interfaces/ISortedCdps.sol

9    event NodeAdded(bytes32 _id, uint _NICR);
10    event NodeRemoved(bytes32 _id);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Interfaces/ISortedCdps.sol#L9

## [G-22] Using mappings instead of arrays to avoid length checks

**Issue Description**\
When storing a list or group of items that you wish to organize in a specific order and fetch with a fixed key/index, it’s common practice to use an array data structure. This works well, but did you know that a trick can be implemented to save 2,000+ gas on each read using a mapping?

**Proposed Optimization**\
Proposed Optimization: Use a mapping instead of an array to store items indexed by ID, avoiding length checks on reads.

See the example below

```solidity

/// get(0) gas cost: 4860
contract Array {
    uint256[] a;

    constructor() {
        a.push() = 1;
        a.push() = 2;
        a.push() = 3;
    }

    function get(uint256 index) external view returns(uint256) {
        return a[index];
    }
}

/// get(0) gas cost: 2758
contract Mapping {
    mapping(uint256 => uint256) a;

    constructor() {
        a[0] = 1;
        a[1] = 2;
        a[2] = 3;
    }

    function get(uint256 index) external view returns(uint256) {
        return a[index];
    }
}
```

Just by using a mapping, we get a gas saving of 2102 gas. Why? Under the hood when you read the value of an index of an array, solidity adds bytecode that checks that you are reading from a valid index (i.e an index strictly less than the length of the array) else it reverts with a panic error (Panic(0x32) to be precise). This prevents from reading unallocated or worse, allocated storage/memory locations.

Due to the way mappings are (simply a key => value pair), no check like that exists and we are able to read from the a storage slot directly. It’s important to note that when using mappings in this manner, your code should ensure that you are not reading an out of bound index of your canonical array.

**Estimated Gas Savings**\
This trick can be implemented to save 2,000+ gas on each read using a mapping

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/CdpManagerStorage.sol

205    bytes32[] public CdpIds;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L205

## [G-23] Understand the trade-offs when choosing between internal functions and modifiers

**Issue Description**\
Modifiers inject its implementation bytecode where it is used while internal functions jump to the location in the runtime code where the its implementation is. This brings certain trade-offs to both options.

Using modifiers more than once means repetitiveness and increase in size of the runtime code but reduces gas cost because of the absence of jumping to the internal function execution offset and jumping back to continue. This means that if runtime gas cost matter most to you, then modifiers should be your choice but if deployment gas cost and/or reducing the size of the creation code is most important to you then using internal functions will be best.

However, modifiers have the tradeoff that they can only be executed at the start or end of a functon. This means executing it at the middle of a function wouldn’t be directly possible, at least not without internal functions which kill the original purpose. This affects it’s flexibility. Internal functions however can be called at any point in a function.

**Estimated Gas Savings**

```solidity

Example showing difference in gas cost using modifiers and an internal function

// SPDX-License-Identifier: MIT
pragma solidity 0.8.19;

/** deployment gas cost: 195435
    gas per call:
              restrictedAction1: 28367
              restrictedAction2: 28377
              restrictedAction3: 28411
 */
 contract Modifier {
    address owner;
    uint256 val;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner() {
        require(msg.sender == owner);
        _;
    }

    function restrictedAction1() external onlyOwner {
        val = 1;
    }

    function restrictedAction2() external onlyOwner {
        val = 2;
    }

    function restrictedAction3() external onlyOwner {
        val = 3;
    }
}



/** deployment gas cost: 159309
    gas per call:
              restrictedAction1: 28391
              restrictedAction2: 28401
              restrictedAction3: 28435
 */
 contract InternalFunction {
    address owner;
    uint256 val;

    constructor() {
        owner = msg.sender;
    }

    function onlyOwner() internal view {
        require(msg.sender == owner);
    }

    function restrictedAction1() external {
        onlyOwner();
        val = 1;
    }

    function restrictedAction2() external {
        onlyOwner();
        val = 2;
    }

    function restrictedAction3() external {
        onlyOwner();
        val = 3;
    }
}
```

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/Dependencies/Auth.sol

26    modifier requiresAuth() virtual {
27        require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");
28
29        _;
30    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L26-L30

```solidity
File: contracts/contracts/Dependencies/AuthNoOwner.sol

16    modifier requiresAuth() virtual {
17        require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");
18
19        _;
20    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L16

```solidity
File: contracts/contracts/BorrowerOperations.sol

144    modifier nonReentrantSelfAndCdpM() {
145        require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");
146        require(
147            ReentrancyGuard(address(cdpManager)).locked() == OPEN,
148            "CdpManager: Reentrancy in nonReentrant call"
149        );
150
151        locked = LOCKED;
152
153        _;
154
155        locked = OPEN;
156    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L144

```solidity
File: contracts/contracts/CdpManagerStorage.sol

241    modifier nonReentrantSelfAndBOps() {
242        require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");
243        require(
244            ReentrancyGuard(borrowerOperationsAddress).locked() == OPEN,
245            "BorrowerOperations: Reentrancy in nonReentrant call"
246        );
247
248        locked = LOCKED;
249
250        _;
251
252        locked = OPEN;
253    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L241

## [G-24] Using assembly to revert with an error message

**Issue Description**\
When reverting in solidity code, it is common practice to use a require or revert statement to revert execution with an error message. This can in most cases be further optimized by using assembly to revert with the error message.

**Proposed Optimization**\
Use inline assembly to directly revert with an error message instead of Solidity require/revert.

Here’s an example;

```solidity
/// calling restrictedAction(2) with a non-owner address: 24042
contract SolidityRevert {
    address owner;
    uint256 specialNumber = 1;

    constructor() {
        owner = msg.sender;
    }

    function restrictedAction(uint256 num)  external {
        require(owner == msg.sender, "caller is not owner");
        specialNumber = num;
    }
}

/// calling restrictedAction(2) with a non-owner address: 23734
contract AssemblyRevert {
    address owner;
    uint256 specialNumber = 1;

    constructor() {
        owner = msg.sender;
    }

    function restrictedAction(uint256 num)  external {
        assembly {
            if sub(caller(), sload(owner.slot)) {
                mstore(0x00, 0x20) // store offset to where length of revert message is stored
                mstore(0x20, 0x13) // store length (19)
                mstore(0x40, 0x63616c6c6572206973206e6f74206f776e657200000000000000000000000000) // store hex representation of message
                revert(0x00, 0x60) // revert with data
            }
        }
        specialNumber = num;
    }
}
```

**Estimated Gas Savings**\

- Solidity require/revert costs ~1000 gas overhead
- Assembly revert is ~200 gas

Potential savings of 800 gas or more per revert.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/ActivePool.sol

104        require(cachedSystemCollShares >= _shares, "!ActivePoolBal");

137        require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

162        require(cachedSystemCollShares >= _shares, "ActivePool: Insufficient collateral shares");

220        require(

228        require(

236        require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");

267        require(amount > 0, "ActivePool: 0 Amount");

269        require(amount <= maxFlashLoan(token), "ActivePool: Too much");

277        require(

294        require(

298        require(

302        require(

318        require(token == address(collateral), "ActivePool: collateral Only");

319        require(!flashLoansPaused, "ActivePool: Flash Loans Paused");

350        require(

374        require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");

377        require(amount <= balance, "ActivePool: Attempt to sweep more than balance");

393        require(

407        require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L104

```solidity
File: contracts/contracts/Dependencies/Auth.sol

27        require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

45        require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L27

```solidity
File: contracts/contracts/Dependencies/AuthNoOwner.sol

17        require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");

41        require(_authority.canCall(msg.sender, address(this), msg.sig));

56        require(address(_authority) == address(0), "Auth: authority is non-zero");

57        require(!_authorityInitialized, "Auth: authority already initialized");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L17

```solidity
File: contracts/contracts/BorrowerOperations.sol

145        require(locked == OPEN, "BorrowerOperations: Reentrancy in nonReentrant call");

146        require(

368        require(

463        require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");

541        require(

715        require(_deadline >= block.timestamp, "BorrowerOperations: Position manager permit expired");

734        require(

807        require(

818        require(

826        require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");

831        require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");

835        require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");

839        require(

846        require(

911        require(

918        require(_newICR >= CCR, "BorrowerOperations: Operation must leave cdp with ICR >= CCR");

922        require(

929        require(

936        require(_debt > 0, "BorrowerOperations: Debt must be non-zero");

940        require(

947        require(

957        require(

970        require(

1083        require(amount > 0, "BorrowerOperations: 0 Amount");

1085        require(amount <= maxFlashLoan(token), "BorrowerOperations: Too much");

1091        require(

1115        require(token == address(ebtcToken), "BorrowerOperations: EBTC Only");

1116        require(!flashLoansPaused, "BorrowerOperations: Flash Loans Paused");

1141        require(

1155        require(_newFee <= MAX_FEE_BPS, "ERC3156FlashLender: _newFee should <= MAX_FEE_BPS");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L145

```solidity
File: contracts/contracts/CdpManager.sol

332        require(redemptionsPaused == false, "CdpManager: Redemptions Paused");

431        require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");

502        require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

503        require(

626        require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption

672        require(redemptionFee < _ETHDrawn, "CdpManager: Fee would eat up all returned collateral");

678        require(decayedBaseRate <= DECIMAL_PRECISION, "CdpManager: baseRate too large!"); // The baseRate can decay to 0

743        require(

747        require(

754        require(_amount > 0, "CdpManager: Amount must be greater than zero");

758        require(_TCR >= MCR, "CdpManager: Cannot redeem when TCR < MCR");

762        require(

774        require(

789        require(

793        require(

808        require(

812        require(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#332

```solidity
File: contracts/contracts/CdpManagerStorage.sol

112        require(

242        require(locked == OPEN, "CdpManager: Reentrancy in nonReentrant call");

243        require(

261        require(

453            require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");

466        require(

475        require(index <= idxLast, "CdpManagerStorage: CDP indexing overflow!");

556        require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");

584        require(activePool.getSystemCollShares() > _feeTaken, "CDPManager: fee split is too big");

649        require(Cdps[_cdpId].status == Status.active, "CdpManager: Cdp does not exist or is closed");

653        require(

660        require(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#112

```solidity
File: contracts/contracts/CollSurplusPool.sol

92        require(claimableColl > 0, "CollSurplusPool: No collateral available to claim");

99        require(cachedTotalSurplusCollShares >= claimableColl, "!CollSurplusPoolBal");

113        require(

120        require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");

124        require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");

143        require(token != address(collateral), "CollSurplusPool: Cannot Sweep Collateral");

146        require(amount <= balance, "CollSurplusPool: Attempt to sweep more than balance");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol

```solidity
File: contracts/contracts/EBTCToken.sol

144            require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");

165        require(cachedAllowances >= subtractedValue, "ERC20: decreased allowance below zero");

208        require(deadline >= block.timestamp, "EBTC: expired deadline");

219        require(recoveredAddress == owner, "EBTC: invalid signature");

247        require(sender != address(0), "EBTCToken: zero sender!");

248        require(recipient != address(0), "EBTCToken: zero recipient!");

251        require(cachedSenderBalances >= amount, "ERC20: transfer amount exceeds balance");

263        require(account != address(0), "EBTCToken: mint to zero recipient!");

271        require(account != address(0), "EBTCToken: burn from zero account!");

274        require(cachedBalance >= amount, "ERC20: burn amount exceeds balance");

286        require(owner != address(0), "EBTCToken: zero approve owner!");

287        require(spender != address(0), "EBTCToken: zero approve spender!");

296        require(

300        require(

307        require(

315        require(

324        require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L144

```solidity
File: contracts/contracts/LeverageMacroBase.sol

45        require(owner() == msg.sender, "Must be owner");

179            require(

191            require(

201            require(

249            require(check.value >= valueToCheck, "!LeverageMacroReference: gte post check");

251            require(check.value <= valueToCheck, "!LeverageMacroReference: let post check");

253            require(check.value == valueToCheck, "!LeverageMacroReference: equal post check");

356            require(

362            require(

421        require(success, "Call has failed");

440                require(

452        require(addy != address(borrowerOperations));

453        require(addy != address(sortedCdps));

454        require(addy != address(activePool));

455        require(addy != address(cdpManager));

456        require(addy != address(this)); // If it could call this it could fake the forwarded caller

```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L45

```solidity
File: contracts/contracts/LiquidationLibrary.sol

56        require(_partialAmount != 0, "LiquidationLibrary: use `liquidate` for 100%");

82            require(

89            require(

93            require(

477            require(

680        require(

710        require(totals.totalDebtInSequence > 0, "LiquidationLibrary: nothing to liquidate");

901        require(

909        require(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L56

```solidity
File: contracts/contracts/SimplifiedDiamondLike.sol

52        require(msg.sender == owner);

56        require(sig != 0x94b24d09);

67        require(msg.sender == owner);

77        require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag

111        require(msg.sender == owner, "Must be owner");

154            require(success);

179            require(ds.settings.callbackEnabledForCall, "Only Enabled Callbacks");

187        require(facet != address(0), "Diamond: Function does not exist");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L52

```solidity
File: contracts/contracts/SortedCdps.sol

352        require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");

365        require(!isFull(), "SortedCdps: List is full");

367        require(!contains(_id), "SortedCdps: List already contains the node");

369        require(_id != dummyId, "SortedCdps: Id cannot be zero");

371        require(_NICR > 0, "SortedCdps: NICR must be positive");

422        require(_len > 1, "SortedCdps: batchRemove() only apply to multiple cdpIds!");

427        require(

433            require(contains(_ids[i]), "SortedCdps: List does not contain the id");

458        require(contains(_id), "SortedCdps: List does not contain the id");

506        require(contains(_id), "SortedCdps: List does not contain the id");

508        require(_newNICR > 0, "SortedCdps: NICR must be positive");

715        require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");

720        require(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L352

## [G-25] Do-While loops are cheaper than for loops

**Issue Description**\
If you want to push optimization at the expense of creating slightly unconventional code, Solidity do-while loops are more gas efficient than for loops, even if you add an if-condition check for the case where the loop doesn’t execute at all.

**Proposed Optimization**\

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.20;

// times == 10 in both tests
contract Loop1 {
    function loop(uint256 times) public pure {
        for (uint256 i; i < times;) {
            unchecked {
                ++i;
            }
        }
    }
}

contract Loop2 {
    function loop(uint256 times) public pure {
        if (times == 0) {
            return;
        }

        uint256 i;

        do {
            unchecked {
                ++i;
            }
        } while (i < times);
    }
}
```

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/Governor.sol

46        for (uint256 i = 0; i < users.length(); i++) {

57            for (uint256 i = 0; i < _usrs.length; i++) {

76        for (uint8 i = 0; i < type(uint8).max; i++) {

84            for (uint8 i = 0; i < type(uint8).max; i++) {

98        for (uint8 i = 0; i < type(uint8).max; i++) {

107            for (uint8 i = 0; i < type(uint8).max; i++) {

122        for (uint8 i = 0; i < roleIds.length; i++) {

137            for (uint256 i = 0; i < _sigs.length; ++i) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L46

```solidity
File: contracts/contracts/LeverageMacroBase.sol

385        for (uint256 i; i < swapLength; ) {

438            for (uint256 i; i < length; ++i) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L385

```solidity
File: contracts/contracts/LiquidationLibrary.sol

753        for (vars.i = _start; ; ) {

816        for (vars.i = _start; ; ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L753

```solidity
File: contracts/contracts/SimplifiedDiamondLike.sol

114        for (uint256 i; i < length; ) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L114

```solidity
File: contracts/contracts/SortedCdps.sol

432        for (uint256 i = 0; i < _len; ++i) {

449        for (uint i = 0; i < _len; ++i) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L432

## [G-26] Use assembly for small keccak256 hashes, in order to save gas

**Issue Description**\
Calling keccak256(abi.encodePacked(...)) in Solidity is inefficient for small arguments that fit in scratch space.

**Proposed Optimization**\
For arguments <= 2 words, use inline assembly to directly hash inputs without ABI encoding overhead.

**Estimated Gas Savings**\

- ABI encoding + hash costs 1200+ gas
- Assembly hash is 80 gas

Savings of 1000+ gas per small keccak256 hash optimized with assembly.

**Attachments**

- **Code Snippets**

```solidity
File: contracts/contracts/BorrowerOperations.sol

682        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L682

```solidity
File: contracts/contracts/EBTCToken.sol

240        return keccak256(abi.encode(typeHash, name, version, _chainID(), address(this)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L240

```solidity
File: contracts/contracts/HintHelpers.sol

182            latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182

## [G-27] Consider using alternatives to OpenZeppelin

OpenZeppelin is a great and popular smart contract library, but there are other alternatives that are worth considering. These alternatives offer better gas efficiency and have been tested and recommended by developers.

Two examples of such alternatives are Solmate and Solady.

Solmate is a library that provides a number of gas-efficient implementations of common smart contract patterns. Solady is another gas-efficient library that places a strong emphasis on using assembly.

## [G-28] Use solidity version 0.8.20 to gain some gas boost

Upgrade to the latest solidity version 0.8.20 to get additional gas savings.
