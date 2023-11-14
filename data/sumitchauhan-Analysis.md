Medium risk issues:- 
1. Arbitrary from in transferFrom
ActivePool.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) uses arbitrary from in transferFrom: collateral.transferFrom(address(receiver),address(this),amountWithFee)
BorrowerOperations.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) uses arbitrary from in transferFrom: ebtcToken.transferFrom(address(receiver),feeRecipientAddress,fee + amount) 

2. Unchecked transfer
ActivePool.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) ignores return value by collateral.transfer(address(receiver),amount) 
ActivePool.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) ignores return value by collateral.transferFrom(address(receiver),address(this),amountWithFee) 
ActivePool.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) ignores return value by collateral.transfer(feeRecipientAddress,fee) 
BorrowerOperations._activePoolAddColl(uint256,uint256) ignores return value by collateral.transferFrom(msg.sender,address(activePool),_stEthBalance) 
BorrowerOperations.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) ignores return value by ebtcToken.transferFrom(address(receiver),feeRecipientAddress,fee + amount)
LeverageMacroBase.sweepToCaller() ignores return value by ebtcToken.transfer(msg.sender,ebtcBal) 

3. Unused return
ActivePool._transferCollSharesWithContractHooks(address,uint256) ignores return value by collateral.transferShares(_account,_shares) 
ActivePool.claimFeeRecipientCollShares(uint256) ignores return value by collateral.transferShares(feeRecipientAddress,_shares) 
LeverageMacroBase.doOperation(LeverageMacroBase.FlashLoanType,uint256,LeverageMacroBase.LeverageMacroOperation,LeverageMacroBase.PostOperationCheck,LeverageMacroBase.PostCheckParams) ignores return value by IERC3156FlashLender(address(borrowerOperations)).flashLoan(IERC3156FlashBorrower(address(this)),address(ebtcToken),borrowAmount,abi.encode(operation)) 
LeverageMacroBase.doOperation(LeverageMacroBase.FlashLoanType,uint256,LeverageMacroBase.LeverageMacroOperation,LeverageMacroBase.PostOperationCheck,LeverageMacroBase.PostCheckParams) ignores return value by IERC3156FlashLender(address(activePool)).flashLoan(IERC3156FlashBorrower(address(this)),address(stETH),borrowAmount,abi.encode(operation)) 
LeverageMacroBase.sweepToCaller() ignores return value by stETH.transferShares(msg.sender,collateralBal)
RolesAuthority.setRoleCapability(uint8,address,bytes4,bool) ignores return value by enabledFunctionSigsByTarget[target].add(bytes32(functionSig))
RolesAuthority.setRoleCapability(uint8,address,bytes4,bool) ignores return value by targets.add(target) 
RolesAuthority.setRoleCapability(uint8,address,bytes4,bool) ignores return value by enabledFunctionSigsByTarget[target].remove(bytes32(functionSig))
RolesAuthority.setRoleCapability(uint8,address,bytes4,bool) ignores return value by targets.remove(target) 
RolesAuthority.setUserRole(address,uint8,bool) ignores return value by users.add(user) 
RolesAuthority.setUserRole(address,uint8,bool) ignores return value by users.remove(user) 
 
4. Uninitialized state variable
CdpManagerStorage.systemDebtRedistributionIndex is never initialized. It is used in:
        - CdpManagerStorage._getPendingRedistributedDebt(bytes32) 
        - CdpManagerStorage._hasRedistributedDebt(bytes32) 
        - CdpManagerStorage._updateRedistributedDebtIndex(bytes32)
CdpManagerStorage.stakingRewardSplit is never initialized. It is used in:
        - CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) 
CdpManagerStorage.systemDebtRedistributionIndex is never initialized. It is used in:
        - CdpManagerStorage._getPendingRedistributedDebt(bytes32) 
        - CdpManagerStorage._hasRedistributedDebt(bytes32) 
        - CdpManagerStorage._updateRedistributedDebtIndex(bytes32) 

5. Uninitialized local variable
BorrowerOperations._openCdp(uint256,bytes32,bytes32,uint256,address).vars is a local variable never initialized
BorrowerOperations._adjustCdpInternal(bytes32,uint256,uint256,bool,bytes32,bytes32,uint256).vars is a local variable never initialized
LeverageMacroBase.doOperation(LeverageMacroBase.FlashLoanType,uint256,LeverageMacroBase.LeverageMacroOperation,LeverageMacroBase.PostOperationCheck,LeverageMacroBase.PostCheckParams).initialCdpIndex is a local variable never initialized
HintHelpers.getRedemptionHints(uint256,uint256,uint256).vars is a local variable never initialized
HintHelpers.getRedemptionHints(uint256,uint256,uint256).vars is a local variable never initialized
Governor.getRolesForUser(address).count is a local variable never initialized
Governor.getUsersByRole(uint8).count is a local variable never initialized
Governor.getRolesFromByteMap(bytes32).count is a local variable never initialized

6. Divide before multiply
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) performs a multiplication on the result of a division:
        - deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT 
        - _deltaFeeSplit = deltaIndexFees * getSystemCollShares() 
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) performs a multiplication on the result of a division:
        - _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION 
        - _deltaFeeSplitShare = (_feeTaken * DECIMAL_PRECISION) + systemStEthFeePerUnitIndexError 
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) performs a multiplication on the result of a division:
        - _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes (contracts/ActivePool.sol#1554)
        - _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes) 
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) performs a multiplication on the result of a division:
        - deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT 
        - _deltaFeeSplit = deltaIndexFees * getSystemCollShares() 
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) performs a multiplication on the result of a division:
        - _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION 
        - _deltaFeeSplitShare = (_feeTaken * DECIMAL_PRECISION) + systemStEthFeePerUnitIndexError 
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) performs a multiplication on the result of a division:
        - _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes 
        - _perUnitError = _deltaFeeSplitShare - (_deltaFeePerUnit * _cachedAllStakes) 


Low issues:-
1. Reentrancy
Reentrancy in ActivePool.claimFeeRecipientCollShares(uint256) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        State variables written after the call(s):
        - feeRecipientCollShares = cachedFeeRecipientCollShares 
Reentrancy in ActivePool.setFeeBps(uint256) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        State variables written after the call(s):
        - feeBps = uint16(_newFee) 
Reentrancy in ActivePool.setFeeRecipientAddress(address) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        State variables written after the call(s):
        - feeRecipientAddress = _feeRecipientAddress 
Reentrancy in ActivePool.setFlashLoansPaused(bool) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        State variables written after the call(s):
        - flashLoansPaused = _paused 
Reentrancy in ActivePool.claimFeeRecipientCollShares(uint256) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        Event emitted after the call(s):
        - FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares,_shares)
Reentrancy in ActivePool.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) :
        External calls:
        - collateral.transfer(address(receiver),amount) 
        - require(bool,string)(receiver.onFlashLoan(msg.sender,token,amount,fee,data) == FLASH_SUCCESS_VALUE,ActivePool: IERC3156: Callback failed) 
        - collateral.transferFrom(address(receiver),address(this),amountWithFee) 
        - collateral.transfer(feeRecipientAddress,fee) 
        Event emitted after the call(s):
        - FlashLoanSuccess(address(receiver),token,amount,fee) 
Reentrancy in ActivePool.setFeeBps(uint256) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        Event emitted after the call(s):
        - FlashFeeSet(msg.sender,_oldFee,_newFee) 
Reentrancy in ActivePool.setFeeRecipientAddress(address) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        Event emitted after the call(s):
        - FeeRecipientAddressChanged(_feeRecipientAddress) 
Reentrancy in ActivePool.setFlashLoansPaused(bool) :
        External calls:
        - ICdpManagerData(cdpManagerAddress).syncGlobalAccountingAndGracePeriod() 
        Event emitted after the call(s):
        - FlashLoansPaused(msg.sender,_paused) 
Reentrancy in BorrowerOperations.setFeeBps(uint256) :
        External calls:
        - cdpManager.syncGlobalAccounting() 
        State variables written after the call(s):
        - feeBps = uint16(_newFee) 
Reentrancy in BorrowerOperations.setFeeRecipientAddress(address) :
        External calls:
        - cdpManager.syncGlobalAccounting() 
        State variables written after the call(s):
        - feeRecipientAddress = _feeRecipientAddress 
Reentrancy in BorrowerOperations.setFlashLoansPaused(bool) :
        External calls:
        - cdpManager.syncGlobalAccounting() 
        State variables written after the call(s):
        - flashLoansPaused = _paused 
Reentrancy in BorrowerOperations.flashLoan(IERC3156FlashBorrower,address,uint256,bytes) :
        External calls:
        - ebtcToken.mint(address(receiver),amount) 
        - require(bool,string)(receiver.onFlashLoan(msg.sender,token,amount,fee,data) == FLASH_SUCCESS_VALUE,IERC3156: Callback failed) 
        - ebtcToken.transferFrom(address(receiver),feeRecipientAddress,fee + amount) 
        - ebtcToken.burn(feeRecipientAddress,amount) 
        Event emitted after the call(s):
        - FlashLoanSuccess(address(receiver),token,amount,fee) 
Reentrancy in BorrowerOperations.setFeeBps(uint256) :
        External calls:
        - cdpManager.syncGlobalAccounting() 
        Event emitted after the call(s):
        - FlashFeeSet(msg.sender,_oldFee,_newFee) 
Reentrancy in BorrowerOperations.setFeeRecipientAddress(address) :
        External calls:
        - cdpManager.syncGlobalAccounting() 
        Event emitted after the call(s):
        - FeeRecipientAddressChanged(_feeRecipientAddress) 
Reentrancy in BorrowerOperations.setFlashLoansPaused(bool) :
        External calls:
        - cdpManager.syncGlobalAccounting() 
        Event emitted after the call(s):
        - FlashLoansPaused(msg.sender,_paused) 


2. Block timestamp
BorrowerOperations.permitPositionManagerApproval(address,address,IPositionManagers.PositionManagerApproval,uint256,uint8,bytes32,bytes32) uses timestamp for comparisons
        Dangerous comparisons:
        - require(bool,string)(_deadline >= block.timestamp,BorrowerOperations: Position manager permit expired) 

3. Calls inside a loop
CdpManagerStorage._readStEthIndex() has external calls inside a loop: (stEthIndex,collateral.getPooledEthByShares(DECIMAL_PRECISION)) 
EbtcBase.getSystemCollShares() has external calls inside a loop: (activePool.getSystemCollShares()) 
CdpManagerStorage.calcFeeUponStakingReward(uint256,uint256) has external calls inside a loop: _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION 
CdpManagerStorage._takeSplitAndUpdateFeePerUnit(uint256,uint256,uint256) has external calls inside a loop: require(bool,string)(activePool.getSystemCollShares() > _feeTaken,CDPManager: fee split is too big) 
CdpManagerStorage._takeSplitAndUpdateFeePerUnit(uint256,uint256,uint256) has external calls inside a loop: activePool.allocateSystemCollSharesToFeeRecipient(_feeTaken) CdpManagerStorage._updateSystemSnapshotsExcludeCollRemainder(uint256) has external calls inside a loop: _totalCollateralSnapshot = activePool.getSystemCollShares() - _collRemainder 
CdpManagerStorage._syncAccounting(bytes32) has external calls inside a loop: CdpUpdated(_cdpId,ISortedCdps(sortedCdps).getOwnerAddress(_cdpId),msg.sender,prevDebt,prevCollShares,_newDebt,_newColl,_cdp.stake,CdpOperation.syncAccounting) 
CdpManager._redeemCollateralFromCdp(ICdpManagerData.SingleRedemptionInputs) has external calls inside a loop: singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth((singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price) 
CdpManager._redeemCollateralFromCdp(ICdpManagerData.SingleRedemptionInputs) has external calls inside a loop: _borrower = sortedCdps.getOwnerAddress(_redeemColFromCdp.cdpId) 
CdpManagerStorage._requireMoreThanOneCdpInSystem(uint256) has external calls inside a loop: require(bool,string)(CdpOwnersArrayLength > 1 && sortedCdps.getSize() > 1,CdpManager: Only one cdp in the system) 
CdpManager._closeCdpByRedemption(bytes32,uint256,uint256,uint256,address) has external calls inside a loop: activePool.decreaseSystemDebt(_EBTC) 
CdpManager._closeCdpByRedemption(bytes32,uint256,uint256,uint256,address) has external calls inside a loop: collSurplusPool.increaseSurplusCollShares(_borrower,_collSurplus + _liquidatorRewardShares) 
CdpManager._closeCdpByRedemption(bytes32,uint256,uint256,uint256,address) has external calls inside a loop: activePool.transferSystemCollSharesAndLiquidatorReward(address(collSurplusPool),_collSurplus,_liquidatorRewardShares) 
CdpManager._redeemCollateralFromCdp(ICdpManagerData.SingleRedemptionInputs) has external calls inside a loop: newNICR != _redeemColFromCdp.partialRedemptionHintNICR || collateral.getPooledEthByShares(newColl) < MIN_NET_STETH_BALANCE 
CdpManager._redeemCollateralFromCdp(ICdpManagerData.SingleRedemptionInputs) has external calls inside a loop: sortedCdps.reInsert(_redeemColFromCdp.cdpId,newNICR,_redeemColFromCdp.upperPartialRedemptionHint,_redeemColFromCdp.lowerPartialRedemptionHint) 
CdpManager._redeemCollateralFromCdp(ICdpManagerData.SingleRedemptionInputs) has external calls inside a loop: CdpUpdated(_redeemColFromCdp.cdpId,ISortedCdps(sortedCdps).getOwnerAddress(_redeemColFromCdp.cdpId),msg.sender,_oldDebtAndColl.debt,_oldDebtAndColl.collShares,newDebt,newColl,Cdps[_redeemColFromCdp.cdpId].stake,CdpOperation.redeemCollateral) 
CdpManager.redeemCollateral(uint256,bytes32,bytes32,bytes32,uint256,uint256,uint256) has external calls inside a loop: _nextId = sortedCdps.getPrev(_cId) 
CdpManager.redeemCollateral(uint256,bytes32,bytes32,bytes32,uint256,uint256,uint256) has external calls inside a loop: nextUserToCheck = sortedCdps.getOwnerAddress(_nextId) 
CdpManagerStorage._calculateCR(uint256,uint256,uint256) has external calls inside a loop: _underlyingCollateral = collateral.getPooledEthByShares(currentCollShare) 
CdpManager.redeemCollateral(uint256,bytes32,bytes32,bytes32,uint256,uint256,uint256) has external calls inside a loop: _cId = sortedCdps.getPrev(_cId) 
CdpManager.redeemCollateral(uint256,bytes32,bytes32,bytes32,uint256,uint256,uint256) has external calls inside a loop: currentBorrower = sortedCdps.getOwnerAddress(_cId) 

Non-critical issues-
1. Usage of `uint`/`int` smaller than 32 bytes (256 bits) incurs overhead:
  ActivePool.sol => function decimals() external view returns (uint8);
  ActivePool.sol => uint8 v,
  ActivePool.sol => event NodeAdded(bytes32 _id, uint _NICR);
  ActivePool.sol => uint maxNodes
  ActivePool.sol => uint maxNodes
  ActivePool.sol => uint maxNodes
  ActivePool.sol => uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance
  ActivePool.sol => uint _debt,
  ActivePool.sol => uint _collShares,
  ActivePool.sol => uint _premiumToLiquidator
  ActivePool.sol => uint _premiumToLiquidator
  ActivePool.sol=> uint128 arrayIndex;
  ActivePool.sol=> feeBps = uint16(_newFee);
  BorrowerOperations.sol => function decimals() external view returns (uint8);
  BorrowerOperations.sol => uint8 v,
  BorrowerOperations.sol => uint _deadline,
  BorrowerOperations.sol => uint8 v,
  BorrowerOperations.sol => event NodeAdded(bytes32 _id, uint _NICR);
  BorrowerOperations.sol => uint maxNodes
  BorrowerOperations.sol => uint maxNodes
  BorrowerOperations.sol => uint maxNodes
  BorrowerOperations.sol => uint16 public feeBps = 3; // may be subject to future adjustments through protocol governance
  BorrowerOperations.sol => function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {
  BorrowerOperations.sol => function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {
  BorrowerOperations.sol => uint _EBTCAmount,
  BorrowerOperations.sol => uint _collAmount,
  BorrowerOperations.sol => uint _debt,
  BorrowerOperations.sol => uint _collShares,
  BorrowerOperations.sol => uint _premiumToLiquidator
  BorrowerOperations.sol => uint _premiumToLiquidator
  BorrowerOperations.sol => uint128 arrayIndex;
  BorrowerOperations.sol => "PermitPositionManagerApproval(address borrower,address positionManager,uint8 status,uint256 nonce,uint256 deadline)"
  BorrowerOperations.sol => uint8 v,
  BorrowerOperations.sol => uint status = cdpManager.getCdpStatus(_cdpId);
  BorrowerOperations.sol => function _requireNonZeroDebtChange(uint _debtChange) internal pure {
  BorrowerOperations.sol => feeBps = uint16(_newFee);
  BorrowerOperations.sol => function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
  CdpManager.sol => function decimals() external view returns (uint8);
  CdpManager.sol => uint8 v,
  CdpManager.sol => event NodeAdded(bytes32 _id, uint _NICR);
  CdpManager.sol => uint maxNodes
  CdpManager.sol => uint maxNodes
  CdpManager.sol => uint maxNodes
  CdpManager.sol => function _checkICRAgainstLiqThreshold(uint256 _icr, uint _tcr) internal view returns (bool) {
  CdpManager.sol => function _checkICRAgainstTCR(uint256 _icr, uint _tcr) internal view returns (bool) {
  CdpManager.sol => uint _debt,
  CdpManager.sol => uint _collShares,
  CdpManager.sol => uint _premiumToLiquidator
  CdpManager.sol => uint _premiumToLiquidator
  CdpManager.sol => uint128 arrayIndex;
  CdpManager.sol => uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
  CdpManager.sol => uint128 public constant MINIMUM_GRACE_PERIOD = 15 minutes;
  CdpManager.sol => uint128 public lastGracePeriodStartTimestamp = UNSET_TIMESTAMP; // use max to signify
  CdpManager.sol => uint128 public recoveryModeGracePeriodDuration = MINIMUM_GRACE_PERIOD;
  CdpManager.sol => lastGracePeriodStartTimestamp = uint128(block.timestamp);
  CdpManager.sol => function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
  CdpManager.sol => uint _pendingDebt,
  CdpManager.sol => uint prevCollShares = _cdp.coll;
  CdpManager.sol => uint128 index = Cdps[_cdpId].arrayIndex;
  CdpManager.sol => uint128 cachedLastGracePeriodStartTimestamp = lastGracePeriodStartTimestamp;
  CdpManager.sol => function getCdpLiquidatorRewardShares(bytes32 _cdpId) external view returns (uint);
  CdpManager.sol => function _addCdpIdToArray(bytes32 _cdpId) internal returns (uint128 index) {
  CdpManager.sol => index = uint128(CdpIds.length - 1);


2. Using `bool`s for storage incurs overhead:
  ActivePool.sol => _authorityInitialized = true;
  ActivePool.sol => _authorityInitialized = true;
  BorrowerOperations.sol => _authorityInitialized = true;
  BorrowerOperations.sol => _authorityInitialized = true;
  BorrowerOperations.sol => isCollIncrease = true;
  CdpManager.sol => _authorityInitialized = true;
  CdpManager.sol => _authorityInitialized = true;
  CdpManager.sol => singleRedemption.fullRedemption = true;
  CdpManager.sol => singleRedemption.cancelledPartial = true;


3. Bytes constants are more efficient than string constants:
  ActivePool.sol => string public constant NAME = "ActivePool";


4. Constants in comparisons should appear on the left side:
  ActivePool.sol => if (returndata.length == 0) {
  ActivePool.sol => if (returndata.length > 0) {
  ActivePool.sol => require(address(_authority) == address(0), "Auth: authority is non-zero");
  ActivePool.sol => if (_authorityAddress != address(0)) {
  ActivePool.sol => require(amount > 0, "ActivePool: 0 Amount");
  ActivePool.sol => require(token == address(collateral), "ActivePool: collateral Only");
  ActivePool.sol => if (token != address(collateral)) {
  ActivePool.sol => require(token != address(collateral), "ActivePool: Cannot Sweep Collateral");
  BorrowerOperations.sol => require(address(_authority) == address(0), "Auth: authority is non-zero");
  BorrowerOperations.sol => * -round product up if 19'th mantissa digit >= 5
  BorrowerOperations.sol => * -round product down if 19'th mantissa digit < 5
  BorrowerOperations.sol => * In function 2), the difference in tokens issued at 1000 years and any time > 1000 years, will be negligible
  BorrowerOperations.sol => if (_minutes > 525600000) {
  BorrowerOperations.sol => if (_minutes == 0) {
  BorrowerOperations.sol => if (n % 2 == 0) {
  BorrowerOperations.sol => if (_debt > 0) {
  BorrowerOperations.sol => if (_debt > 0) {
  BorrowerOperations.sol => require(newOwner != address(0), "Ownable: new owner is the zero address");
  BorrowerOperations.sol => if (_authorityAddress != address(0)) {
  BorrowerOperations.sol => if (!_isDebtIncrease && _debtChange > 0) {
  BorrowerOperations.sol => require(vars.netStEthBalance > 0, "BorrowerOperations: zero collateral for openCdp()!");
  BorrowerOperations.sol => if (_collReceived != 0) {
  BorrowerOperations.sol => require(status == 1, "BorrowerOperations: Cdp does not exist or is closed");
  BorrowerOperations.sol => require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");
  BorrowerOperations.sol => require(_debtChange > 0, "BorrowerOperations: Debt increase requires non-zero debtChange");
  BorrowerOperations.sol => require(_debt > 0, "BorrowerOperations: Debt must be non-zero");
  BorrowerOperations.sol => require(amount > 0, "BorrowerOperations: 0 Amount");
  BorrowerOperations.sol => require(token == address(ebtcToken), "BorrowerOperations: EBTC Only");
  BorrowerOperations.sol => if (token != address(ebtcToken)) {
  CdpManager.sol => require(address(_authority) == address(0), "Auth: authority is non-zero");
  CdpManager.sol => * -round product up if 19'th mantissa digit >= 5
  CdpManager.sol => * -round product down if 19'th mantissa digit < 5
  CdpManager.sol => * In function 2), the difference in tokens issued at 1000 years and any time > 1000 years, will be negligible
  CdpManager.sol => if (_minutes > 525600000) {
  CdpManager.sol => if (_minutes == 0) {
  CdpManager.sol => if (n % 2 == 0) {
  CdpManager.sol => if (_debt > 0) {
  CdpManager.sol => if (_debt > 0) {
  CdpManager.sol => if (_debtIndexDiff > 0) {
  CdpManager.sol => if (_feeSplitDistributed > 0 || _debtIndexDelta > 0) {
  CdpManager.sol => if (_feeSplitDistributed > 0) {
  CdpManager.sol => if (_debtIndexDelta > 0) {
  CdpManager.sol => if (totalCollateralSnapshot == 0) {
  CdpManager.sol => require(totalStakesSnapshot > 0, "CdpManagerStorage: zero totalStakesSnapshot!");
  CdpManager.sol => if (_newIndex > _oldIndex && totalStakes > 0) {
  CdpManager.sol => if (_newIndex > _oldIndex && totalStakes > 0) {
  CdpManager.sol => if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
  CdpManager.sol => if (pendingDebtRedistributed > 0) {
  CdpManager.sol => if (_feeTaken > 0) {
  CdpManager.sol => if (newDebt == 0) {
  CdpManager.sol => if (_maxIterations == 0) {
  CdpManager.sol => require(totals.collSharesDrawn > 0, "CdpManager: Unable to redeem any amount");
  CdpManager.sol => if (_numCdpsFullyRedeemed == 1) {
  CdpManager.sol => } else if (_numCdpsFullyRedeemed > 1) {
  CdpManager.sol => require(newBaseRate > 0, "CdpManager: new baseRate is zero!"); // Base rate is always non-zero after redemption
  CdpManager.sol => require(_amount > 0, "CdpManager: Amount must be greater than zero");

 
5. Unsafe casting may overflow:
  ActivePool.sol => feeBps = uint16(_newFee);
  
 


### Time spent:
8 hours