## [G-01] Splitting require() statements that use && saves gas

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

## [G-02] Use constants instead of type(uintx).max

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

```solidity
File: contracts/contracts/Governor.sol

76        for (uint8 i = 0; i < type(uint8).max; i++) {

84            for (uint8 i = 0; i < type(uint8).max; i++) {

98        for (uint8 i = 0; i < type(uint8).max; i++) {

107            for (uint8 i = 0; i < type(uint8).max; i++) {
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L76

## [G-03] Use hardcode address instead address(this)

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

## [G-04] Expressions for constant values such as a call to keccak256(), should use immutable rather than constant

```solidity
File: contracts/contracts/LeverageMacroBase.sol

37    bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37

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
File: contracts/contracts/SimplifiedDiamondLike.sol

39    bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39

## [G-05] Internal functions only called once can be inlined to save gas

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

## [G-06] Use nested If and avoid multiple check combinations &&

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

## [G-07] abi.encode() is less efficient than abi.encodePacked()

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

## [G-08] MULTIPLE ADDRESS/ID MAPPINGS CAN BE COMBINED INTO A SINGLE MAPPING OF AN ADDRESS/ID TO A STRUCT, WHERE APPROPRIATE

```solidity
File: contracts/Dependencies/RolesAuthority.sol

34    mapping(address => mapping(bytes4 => CapabilityFlag)) public capabilityFlag;

36    mapping(address => mapping(bytes4 => bytes32)) public getRolesWithCapability;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L34

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

## [G-09] Do not calculate constants

```solidity
File: contracts/contracts/CdpManagerStorage.sol

141    uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L141

## [G-10] Use Assembly to write Address Storage Value

```solidity
File: contracts/contracts/CdpManagerStorage.sol

126    address public immutable borrowerOperationsAddress;

132    address public immutable liquidationLibrary;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L126

```solidity
File: contracts/contracts/ActivePool.sol

26    address public immutable borrowerOperationsAddress;

27    address public immutable cdpManagerAddress;

28    address public immutable collSurplusPoolAddress;

29    address public feeRecipientAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L26

```solidity
File: contracts/contracts/CollSurplusPool.sol

21    address public immutable borrowerOperationsAddress;

22    address public immutable cdpManagerAddress;

23    address public immutable activePoolAddress;

24    address public immutable feeRecipientAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L21

```solidity
File: contracts/SimplifiedDiamondLike.sol

42    address public immutable owner;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L42

```solidity
File: contracts/contracts/EBTCToken.sol

55    address public immutable cdpManagerAddress;

56    address public immutable borrowerOperationsAddress;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L55

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
File: contracts/contracts/LeverageMacroFactory.sol

12    address public immutable borrowerOperations;

13    address public immutable activePool;

14    address public immutable cdpManager;

15    address public immutable ebtcToken;

16    address public immutable stETH;

17    address public immutable sortedCdps;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroFactory.sol#L12

## [G-11] Using delete statement can save gas

```solidity
File: contracts/contracts/HintHelpers.sol

105                        partialRedemptionHintNICR = 0; //reset to 0 as there is no partial redemption in this case

106                        partialRedemptionNewColl = 0;

109                        vars.remainingEbtcToRedeem = 0;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L105

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

## [G-12] Using fixed bytes is cheaper than using string

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
File: contracts/contracts/SortedCdps.sol

52    string public constant NAME = "SortedCdps";
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L52

## [G-13] BEFORE SOME FUNCTIONS, WE SHOULD CHECK SOME VARIABLES FOR POSSIBLE GAS SAVE

```solidity
File: contracts/contracts/BorrowerOperations.sol

785        collateral.transferFrom(msg.sender, address(activePool), _stEthBalance);

1100        ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L785

```solidity
File: contracts/contracts/ActivePool.sol

183        collateral.transferShares(_account, _shares);


274        collateral.transfer(address(receiver), amount);

283        collateral.transferFrom(address(receiver), address(this), amountWithFee);

286        collateral.transfer(feeRecipientAddress, fee);

362        collateral.transferShares(feeRecipientAddress, _shares);
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L181

## [G-14] Setting the constructor to Payable

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

## [G-15] <X> += <Y> costs more gas than <X> = <X> + <Y> for state variables

```solidity
File: contracts/contracts/CdpManager.sol

697            lastRedemptionTimestamp += _minutesPassedSinceLastRedemption() * SECONDS_IN_ONE_MINUTE;
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L697

## [G-16] Shorten the array rather than copying to a new one

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

## [G-17] Using storage instead of memory for Structs/Arrays Save Gas

When fetching data from a storage location, assigning the data to a memory variable causes all fields of the struct/array to be read from
storage, which incurs a Gcoldsload (2100 gas) for each field of the struct/array.

If the fields are read from the new memory variable, they incur an additional MLOAD rather than a cheap stack read.

Instead of declearing the variable with the memory keyword, declaring the variable with the storage keyword and caching any fields that need to
be re-read in stack variables, will be much cheaper, only incuring the Gcoldsload for the fields actually read.

The only time it makes sense to read the whole struct/array into a memory variable, is if the full struct/array is being returned by the function, is being passed to a function that requires memory, or if the array/struct is being read from another memory array/struct

```solidity
File: contracts/contracts/LeverageMacroBase.sol

339        LeverageMacroOperation memory leverageMacroData = abi.decode(data, (LeverageMacroOperation));

374        LeverageMacroOperation memory operation = decodeFLData(data);

461        OpenCdpOperation memory flData = abi.decode(data, (OpenCdpOperation));

475        CloseCdpOperation memory flData = abi.decode(data, (CloseCdpOperation));

483        AdjustCdpOperation memory flData = abi.decode(data, (AdjustCdpOperation));
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L339

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

## [G-18] A modifier used only once and not being inherited should be inlined to save gas

```solidity
File: contracts/contracts/Dependencies/Auth.sol


26    modifier requiresAuth() virtual {
27        require(isAuthorized(msg.sender, msg.sig), "Auth: UNAUTHORIZED");
28
29        _;
30    }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L26-L30

## [G-19] Avoid contract existence checks by using low level calls

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
File: contracts/contracts/LiquidationLibrary.sol

530        ebtcToken.burn(msg.sender, totalDebtToBurn);

533        activePool.decreaseSystemDebt(totalDebtToBurn);

536        activePool.transferSystemCollSharesAndLiquidatorReward(
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L530