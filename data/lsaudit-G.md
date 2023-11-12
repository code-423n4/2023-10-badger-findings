# [G-01] Using bools for storage incurs overhead
Booleans are more expensive than uint256 or any type that takes up a full word because each write operation emits an extra SLOAD to first read the slot's contents, replace the bits taken up by the boolean, and then write back. This is the compiler's defense against contract upgrades and pointer aliasing, and it cannot be disabled. Use uint256(0) and uint256(1) for true/false to avoid a Gwarmaccess (100 gas) for the extra SLOAD.


```
./CdpManagerStorage.sol:143:    bool public redemptionsPaused;
./ERC3156FlashLender.sol:15:    bool public flashLoansPaused;
./LeverageMacroBase.sol:35:    bool internal immutable willSweep;
./AuthNoOwner.sol:14:    bool private _authorityInitialized;
```

# [G‑02] Constructors can be marked as payable to save deployment gas
Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. A constructor can be safely marked as payable, because only the deployer would be able to pass funds, and the project itself would not pass any funds.

```
./Auth.sol:18:    constructor(address _owner, Authority _authority) {
./RolesAuthority.sol:20:    constructor(address _owner, Authority _authority) Auth(_owner, _authority) {}
./Governor.sol:36:    constructor(address _owner) RolesAuthority(_owner, Authority(address(this))) {}
./EbtcBase.sol:52:    constructor(address _activePoolAddress, address _priceFeedAddress, address _collateralAddress) {
./SortedCdps.sol:88:    constructor(uint256 _size, address _cdpManagerAddress, address _borrowerOperationsAddress) {
./SimplifiedDiamondLike.sol:44:    constructor(address _owner) {

```

# [G‑03] Functions that revert when called by normal users can be marked payable

If a function modifier such as onlyOwner is used, the function will revert if a normal user tries to pay the function. Marking the function as payable will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided. The extra opcodes avoided are: CALLVALUE(2), DUP1(3), ISZERO(3), PUSH2(3), JUMPI(10), PUSH1(3), DUP1(3), REVERT(0), JUMPDEST(1), POP(2) which cost an average of about 21 gas per call to the function, in addition to the extra deployment cost.

```
./Auth.sol:52:    function transferOwnership(address newOwner) public virtual requiresAuth {
./RolesAuthority.sol:133:    function burnCapability(address target, bytes4 functionSig) public virtual requiresAuth {
./RolesAuthority.sol:147:    function setUserRole(address user, uint8 role, bool enabled) public virtual requiresAuth {
./CdpManager.sol:773:    function setStakingRewardSplit(uint256 _stakingRewardSplit) external requiresAuth {
./CdpManager.sol:788:    function setRedemptionFeeFloor(uint256 _redemptionFeeFloor) external requiresAuth {
./CdpManager.sol:807:    function setMinuteDecayFactor(uint256 _minuteDecayFactor) external requiresAuth {
./CdpManager.sol:830:    function setBeta(uint256 _beta) external requiresAuth {
./CdpManager.sol:843:    function setRedemptionsPaused(bool _paused) external requiresAuth {
./Governor.sol:154:    function setRoleName(uint8 role, string memory roleName) external requiresAuth {
./PriceFeed.sol:358:    function setFallbackCaller(address _fallbackCaller) external requiresAuth {
./CdpManagerStorage.sol:111:    function setGracePeriod(uint128 _gracePeriod) external requiresAuth {
./BorrowerOperations.sol:1140:    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
./BorrowerOperations.sol:1154:    function setFeeBps(uint256 _newFee) external requiresAuth {
./BorrowerOperations.sol:1167:    function setFlashLoansPaused(bool _paused) external requiresAuth {
./CollSurplusPool.sol:142:    function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
./ActivePool.sol:346:    function claimFeeRecipientCollShares(uint256 _shares) external override requiresAuth {
./ActivePool.sol:371:    function sweepToken(address token, uint256 amount) public nonReentrant requiresAuth {
./ActivePool.sol:390:    function setFeeRecipientAddress(address _feeRecipientAddress) external requiresAuth {
./ActivePool.sol:404:    function setFeeBps(uint256 _newFee) external requiresAuth {
./ActivePool.sol:417:    function setFlashLoansPaused(bool _paused) external requiresAuth {
```



# [G-04] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary

```
./Auth.sol:        require(msg.sender == owner || authority.canCall(msg.sender, address(this), msg.sig));
./EBTCToken.sol:            msg.sender == borrowerOperationsAddress,
./EBTCToken.sol:            msg.sender == borrowerOperationsAddress ||
./EBTCToken.sol:                msg.sender == cdpManagerAddress ||
./EBTCToken.sol:        require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
./CdpManagerStorage.sol:            msg.sender == borrowerOperationsAddress,
./SortedCdps.sol:        require(msg.sender == address(cdpManager), "SortedCdps: Caller is not the CdpManager");
./SortedCdps.sol:            msg.sender == borrowerOperationsAddress || msg.sender == address(cdpManager),
./LeverageMacroBase.sol:        require(owner() == msg.sender, "Must be owner");
./LeverageMacroBase.sol:                msg.sender == address(borrowerOperations),
./LeverageMacroBase.sol:                msg.sender == address(activePool),
./BorrowerOperations.sol:        if (_borrower == msg.sender) {
./CollSurplusPool.sol:            msg.sender == borrowerOperationsAddress,
./CollSurplusPool.sol:        require(msg.sender == cdpManagerAddress, "CollSurplusPool: Caller is not CdpManager");
./CollSurplusPool.sol:        require(msg.sender == activePoolAddress, "CollSurplusPool: Caller is not Active Pool");
./ActivePool.sol:            msg.sender == borrowerOperationsAddress,
./ActivePool.sol:            msg.sender == borrowerOperationsAddress || msg.sender == cdpManagerAddress,
./ActivePool.sol:        require(msg.sender == cdpManagerAddress, "ActivePool: Caller is not CdpManager");
./SimplifiedDiamondLike.sol:        require(msg.sender == owner);
./SimplifiedDiamondLike.sol:        require(msg.sender == owner);
./SimplifiedDiamondLike.sol:        require(msg.sender == address(this)); // Must call this via `execute` to explicitly set the flag
./SimplifiedDiamondLike.sol:        require(msg.sender == owner, "Must be owner");
```


# [G-05] Using assembly to check for zero can save gas
Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.

```
./RolesAuthority.sol:124:            if (enabledFunctionSigsByTarget[target].length() == 0) {
./CdpManager.sol:159:        if (newDebt == 0) {
./CdpManager.sol:377:        if (_maxIterations == 0) {
./PriceFeed.sol:420:            _response.timestampEthBtc == 0 ||
./PriceFeed.sol:422:            _response.timestampStEthEth == 0 ||
./PriceFeed.sol:471:        if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {
./PriceFeed.sol:475:        if (_response.answer == 0) {
./PriceFeed.sol:532:        if (minPrice == 0) return false;
./PriceFeed.sol:695:        if (_currentRoundEthBtcId == 0 || _currentRoundStEthEthId == 0) {
./PriceFeed.sol:777:        if (_roundId == 0) return false;
./EbtcMath.sol:64:        if (_minutes == 0) {
./EbtcMath.sol:74:            if (n % 2 == 0) {
./EbtcMath.sol:98:            // if (_debt == 0)
./EbtcMath.sol:116:            // if (_debt == 0)
./CdpManagerStorage.sol:443:        if (totalCollateralSnapshot == 0) {
./CdpManagerStorage.sol:624:            _cdpStEthFeePerUnitIndex == 0 ||
./CdpManagerStorage.sol:625:            _cdpCol == 0 ||
./SortedCdps.sol:89:        if (_size == 0) {
./SortedCdps.sol:305:        if (maxArraySize == 0) {
./SortedCdps.sol:352:        require(cdpManager.getCdpStatus(_id) == 0, "SortedCdps: new id is NOT nonExistent!");
./SortedCdps.sol:537:        return data.size == 0;
./LiquidationLibrary.sol:144:        if (_liqState.partialAmount == 0) {
./LiquidationLibrary.sol:158:                liquidationValues.totalCollToSendToLiquidator == 0 &&
./LiquidationLibrary.sol:159:                liquidationValues.debtToBurn == 0
./LiquidationLibrary.sol:417:        if (newColl == 0) {
./LiquidationLibrary.sol:863:        if (_debt == 0) {
./BorrowerOperations.sol:808:            _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
./BorrowerOperations.sol:831:        require(status == 0, "BorrowerOperations: Cdp is active or has been previously closed");
./BorrowerOperations.sol:847:            _stEthBalanceDecrease == 0,
./HintHelpers.sol:78:        if (_maxIterations == 0) {
./HintHelpers.sol:171:        if (arrayLength == 0) {

```

# [G-06] Use assembly to emit events

To efficiently emit events, it's possible to utilize assembly by making use of scratch space and the free memory pointer. This approach has the advantage of potentially avoiding the costs associated with memory expansion.

However, it's important to note that in order to safely optimize this process, it is preferable to cache and restore the free memory pointer.

A good example of such practice can be seen in Solady's codebase.

```
./Auth.sol:22:        emit OwnershipTransferred(msg.sender, _owner);
./Auth.sol:23:        emit AuthorityUpdated(msg.sender, _authority);
./Auth.sol:49:        emit AuthorityUpdated(msg.sender, newAuthority);
./Auth.sol:55:        emit OwnershipTransferred(msg.sender, newOwner);
./RolesAuthority.sol:101:        emit PublicCapabilityUpdated(target, functionSig, enabled);
./RolesAuthority.sol:129:        emit RoleCapabilityUpdated(role, target, functionSig, enabled);
./RolesAuthority.sol:140:        emit CapabilityBurned(target, functionSig);
./RolesAuthority.sol:163:        emit UserRoleUpdated(user, role, enabled);
./CdpManager.sol:55:        emit StakingRewardSplitSet(stakingRewardSplit);
./CdpManager.sol:179:                emit CdpUpdated(
./CdpManager.sol:220:            emit CdpUpdated(
./CdpManager.sol:466:        emit Redemption(
./CdpManager.sol:545:        emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);
./CdpManager.sol:630:        emit BaseRateUpdated(newBaseRate);
./CdpManager.sol:681:        emit BaseRateUpdated(decayedBaseRate);
./CdpManager.sol:698:            emit LastRedemptionTimestampUpdated(block.timestamp);
./CdpManager.sol:782:        emit StakingRewardSplitSet(_stakingRewardSplit);
./CdpManager.sol:801:        emit RedemptionFeeFloorSet(_redemptionFeeFloor);
./CdpManager.sol:824:        emit MinuteDecayFactorSet(_minuteDecayFactor);
./CdpManager.sol:836:        emit BetaSet(_beta);
./CdpManager.sol:848:        emit RedemptionsPaused(_paused);
./CdpManager.sol:925:        emit CdpUpdated(
./CdpManager.sol:961:        emit CdpUpdated(
./Governor.sol:157:        emit RoleNameSet(role, roleName);
./LeverageMacroFactory.sol:56:        emit DeployNewMacro(_owner, addy);
./PriceFeed.sol:67:        emit FallbackCallerChanged(address(0), _fallbackCallerAddress);
./PriceFeed.sol:378:                    emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
./PriceFeed.sol:381:                emit UnhealthyFallbackCaller(_fallbackCaller, block.timestamp);
./PriceFeed.sol:387:            emit FallbackCallerChanged(oldFallbackCaller, _fallbackCaller);
./PriceFeed.sol:548:        emit PriceFeedStatusChanged(_status);
./PriceFeed.sol:555:        emit LastGoodPriceUpdated(_currentPrice);
./EBTCToken.sol:259:        emit Transfer(sender, recipient, amount);
./EBTCToken.sol:267:        emit Transfer(address(0), account, amount);
./EBTCToken.sol:282:        emit Transfer(account, address(0), amount);
./EBTCToken.sol:290:        emit Approval(owner, spender, amount);
./CdpManagerStorage.sol:50:        emit TCRNotified(_tcr);
./CdpManagerStorage.sol:55:            emit GracePeriodStart();
./CdpManagerStorage.sol:64:        emit TCRNotified(_tcr);
./CdpManagerStorage.sol:69:            emit GracePeriodEnd();
./CdpManagerStorage.sol:119:        emit GracePeriodDurationSet(_gracePeriod);
./CdpManagerStorage.sol:300:        emit SystemSnapshotsUpdated(_totalStakesSnapshot, _totalCollateralSnapshot);
./CdpManagerStorage.sol:340:        emit CdpDebtRedistributionIndexUpdated(_cdpId, _systemDebtRedistributionIndex);
./CdpManagerStorage.sol:390:            emit CdpUpdated(
./CdpManagerStorage.sol:414:        emit TotalStakesUpdated(_newTotalStakes);
./CdpManagerStorage.sol:425:        emit TotalStakesUpdated(_newTotalStakes);
./CdpManagerStorage.sol:481:        emit CdpArrayIndexUpdated(idToMove, index);
./CdpManagerStorage.sol:542:            emit StEthIndexUpdated(_oldIndex, _newIndex, block.timestamp);
./CdpManagerStorage.sol:587:        emit CollateralFeePerUnitUpdated(_oldPerUnit, _newPerUnit, _feeTaken);
./CdpManagerStorage.sol:602:        emit CdpFeeSplitApplied(
./SortedCdps.sol:405:        emit NodeAdded(_id, _NICR);
./SortedCdps.sol:451:            emit NodeRemoved(_ids[i]);
./SortedCdps.sol:490:        emit NodeRemoved(_id);
./LiquidationLibrary.sol:238:        emit CdpUpdated(
./LiquidationLibrary.sol:281:        emit CdpLiquidated(
./LiquidationLibrary.sol:312:        emit CdpUpdated(
./LiquidationLibrary.sol:367:        emit CdpLiquidated(
./LiquidationLibrary.sol:437:            emit CdpPartiallyLiquidated(
./LiquidationLibrary.sol:490:        emit CdpUpdated(
./LiquidationLibrary.sol:516:        emit Liquidation(totalDebtToBurn, totalCollSharesToSend, totalLiquidatorRewardCollShares);
./LiquidationLibrary.sol:891:        emit SystemDebtRedistributionIndexUpdated(systemDebtRedistributionIndex);
./BorrowerOperations.sol:136:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
./BorrowerOperations.sol:641:        emit PositionManagerApprovalSet(_borrower, _positionManager, _approval);
./BorrowerOperations.sol:1105:        emit FlashLoanSuccess(address(receiver), token, amount, fee);
./BorrowerOperations.sol:1149:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
./BorrowerOperations.sol:1162:        emit FlashFeeSet(msg.sender, _oldFee, _newFee);
./BorrowerOperations.sol:1171:        emit FlashLoansPaused(msg.sender, _paused);
./CollSurplusPool.sol:83:        emit SurplusCollSharesUpdated(_account, newAmount);
./CollSurplusPool.sol:95:        emit SurplusCollSharesUpdated(_account, 0);
./CollSurplusPool.sol:104:        emit CollSharesTransferred(_account, claimableColl);
./CollSurplusPool.sol:150:        emit SweepTokenSuccess(token, amount, feeRecipientAddress);
./ActivePool.sol:65:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
./ActivePool.sol:112:        emit SystemCollSharesUpdated(cachedSystemCollShares);
./ActivePool.sol:113:        emit CollSharesTransferred(_account, _shares);
./ActivePool.sol:145:        emit SystemCollSharesUpdated(cachedSystemCollShares);
./ActivePool.sol:146:        emit CollSharesTransferred(_account, totalShares);
./ActivePool.sol:173:        emit SystemCollSharesUpdated(cachedSystemCollShares);
./ActivePool.sol:174:        emit FeeRecipientClaimableCollSharesIncreased(cachedFeeRecipientCollShares, _shares);
./ActivePool.sol:200:        emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
./ActivePool.sol:213:        emit ActivePoolEBTCDebtUpdated(cachedSystemDebt);
./ActivePool.sol:247:        emit SystemCollSharesUpdated(cachedSystemCollShares);
./ActivePool.sol:307:        emit FlashLoanSuccess(address(receiver), token, amount, fee);
./ActivePool.sol:360:        emit FeeRecipientClaimableCollSharesDecreased(cachedFeeRecipientCollShares, _shares);
./ActivePool.sol:383:        emit SweepTokenSuccess(token, amount, cachedFeeRecipientAddress);
./ActivePool.sol:399:        emit FeeRecipientAddressChanged(_feeRecipientAddress);
./ActivePool.sol:412:        emit FlashFeeSet(msg.sender, _oldFee, _newFee);
./ActivePool.sol:421:        emit FlashLoansPaused(msg.sender, _paused);
./AuthNoOwner.sol:50:        emit AuthorityUpdated(msg.sender, Authority(newAuthority));
./AuthNoOwner.sol:62:        emit AuthorityUpdated(address(this), Authority(newAuthority));

```


# [G-07] Using a double if statement instead of a logical AND(&&)

Using a double if statement instead of a logical AND (&&) can provide similar short-circuiting behavior whereas double if is slightly more gas efficient.

```
./CdpManagerStorage.sol:512:        if (_newIndex > _oldIndex && totalStakes > 0) {
./CdpManagerStorage.sol:765:        if (_newIndex > _oldIndex && totalStakes > 0) {
./CdpManagerStorage.sol:796:        if (_cdpPerUnitIdx != _systemStEthFeePerUnitIndex && _cdpPerUnitIdx > 0) {
./SortedCdps.sol:202:            if (maxNodes > 0 && i >= maxNodes) {
./SortedCdps.sol:259:            if (maxNodes > 0 && i >= maxNodes) {
./SortedCdps.sol:330:            if (maxNodes > 0 && i >= maxNodes) {
./SortedCdps.sol:382:        if (prevId == dummyId && nextId == dummyId) {
./SortedCdps.sol:596:        if (_prevId == dummyId && _nextId == dummyId) {
./SortedCdps.sol:621:        if (data.head == _startId && _NICR >= cdpManager.getCachedNominalICR(_startId)) {
./SortedCdps.sol:644:        if (data.tail == _startId && _NICR <= cdpManager.getCachedNominalICR(_startId)) {
./SortedCdps.sol:696:        if (prevId == dummyId && nextId == dummyId) {
./LiquidationLibrary.sol:756:            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
./LiquidationLibrary.sol:790:                } else if (vars.backToNormalMode && _checkICRAgainstMCR(vars.ICR)) {
./LiquidationLibrary.sol:819:            if (vars.cdpId != bytes32(0) && Cdps[vars.cdpId].status == Status.active) {
./BorrowerOperations.sol:393:        if (!_isDebtIncrease && _debtChange > 0) {

```


# [G-08] Add unchecked blocks for divisions where the operands cannot overflow

uint divisions can't overflow, while int divisions can overflow only in one specific case.

Consider adding an unchecked block to have some gas savings.

```
./CdpManager.sol:621:        uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
./CdpManager.sol:624:        uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);
./CdpManager.sol:671:        uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;
./EbtcBase.sol:108:        uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;
./PriceFeed.sol:534:        uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /
./EbtcMath.sol:110:            uint256 newCollRatio = (_stEthBalance * _price) / _debt;
./CdpManagerStorage.sol:558:        uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;
./CdpManagerStorage.sol:564:        uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;
./CdpManagerStorage.sol:567:        uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;
./LiquidationLibrary.sol:278:        uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;
./LiquidationLibrary.sol:365:        uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;
./LiquidationLibrary.sol:435:            uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;
./LiquidationLibrary.sol:592:            uint256 _debtToRepay = (_incentiveColl * _price) / LICR;
./LiquidationLibrary.sol:882:        uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;
```


# [G-09] Structs can be packed into fewer storage slots
Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

* [File: SimplifiedDiamondLike.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SimplifiedDiamondLike.sol#L99-L107)
```
struct Operation {
        address to; // Target to call
        bool checkSuccess; // If false we will ignore a revert
        uint128 value; // How much ETH to send
        uint128 gas; // How much gas to send
        bool capGas; // true to use above "gas" setting or we send gasleft()
        OperationType opType; // See `OperationType`
        bytes data; // Calldata to send (funsig + data)
    }
```

Uses 4 slots.
To save one slot change to:

```
    struct Operation {
        address to; // Target to call
        bool checkSuccess; // If false we will ignore a revert
        bool capGas; // true to use above "gas" setting or we send gasleft()
        OperationType opType; // See `OperationType`
        uint128 value; // How much ETH to send
        uint128 gas; // How much gas to send
        
        bytes data; // Calldata to send (funsig + data)
    }
```

* [File: IPriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L17-L24)
```
  struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
        uint256 answer;
        uint256 timestampEthBtc;
        uint256 timestampStEthEth;
        bool success;
    }
```

Uses 5 slots.
To save one slot change to:

```
  struct ChainlinkResponse {
        uint80 roundEthBtcId;
        uint80 roundStEthEthId;
        bool success;
        uint256 answer;
        uint256 timestampEthBtc;
        uint256 timestampStEthEth;
        
    }
```


* [File: BorrowerOperations.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L97-L104)
```
 struct MoveTokensParams {
        address user;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
        bool isCollIncrease;
        uint256 netDebtChange;
        bool isDebtIncrease;
    }
```

Uses 6 slots.
To save two slots change to:

```
  struct MoveTokensParams {
        address user;
        bool isCollIncrease;
        bool isDebtIncrease;
        uint256 collSharesChange;
        uint256 collAddUnderlying; // ONLY for isCollIncrease=true
        uint256 netDebtChange;
        
    }
```

* [File: LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L259C10-L259C10)
```
 struct LeverageMacroOperation {
        address tokenToTransferIn;
        uint256 amountToTransferIn;
        SwapOperation[] swapsBefore; // Empty to skip
        SwapOperation[] swapsAfter; // Empty to skip
        OperationType operationType; // Open, Close, etc..
        bytes OperationData; // Generic Operation Data, which we'll decode to use
    }
```

Uses 6 slot.
To save one slot change to:

```
   struct LeverageMacroOperation {
        address tokenToTransferIn;
        OperationType operationType; // Open, Close, etc..
        uint256 amountToTransferIn;
        SwapOperation[] swapsBefore; // Empty to skip
        SwapOperation[] swapsAfter; // Empty to skip
        bytes OperationData; // Generic Operation Data, which we'll decode to use
        
    }
```


# [G-10] Consider redeisign of structs, so they can be packed into fewer storage slots

* [File: Governor.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Governor.sol#L19-L21)
```
 struct Role {
        uint8 roleId;
        string roleName;
    }
```

Uses 2 slots.
Please consider, if the name of the role (`roleName`) must be `string`. Consider restirction of `roleName` lengths, e.g. to 31 bytes. That way, below struct will use 1 slot, instead of two:

```
 struct Role {
        uint8 roleId;
        bytes31 roleName;
    }
```

* [File: IPriceFeed.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IPriceFeed.sol#L26)
```
    struct FallbackResponse {
        uint256 answer;
        uint256 timestamp;
        bool success;
    }
```

Since one of the field is `timestamp`, consider changing `uint256` to `uint128`. The max value of `uint128` is big enough, so `block.timestamp` will never overflow it.


* [File: LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L94)
```
    struct PostCheckParams {
        CheckValueAndType expectedDebt;
        CheckValueAndType expectedCollateral;
        // Used only if cdpStats || isClosed
        bytes32 cdpId;
        // Used only to check status
        ICdpManagerData.Status expectedStatus; // NOTE: THIS IS SUPERFLUOUS
    }
```

Field `expectedStatus` is redundant and can be removed to save one more slot.


# [G-11] Do not check if set `contains()` element before adding it in `RolesAuthority.sol`


[File: RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L116-L117)
```
if (!targets.contains(target)) {
                targets.add(target);
```

[File: RolesAuthority.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/RolesAuthority.sol#L151-L152)
```

            if (!users.contains(user)) {
                users.add(user);
            }
```

`RolesAuthority.sol` uses `EnumerableSet` from OpenZeppelin. Its implementation already checks if set contains the element, before adding it to the set. According to OZ implementation, function `add()` returns true when it adds new element to the set, and false - when element is already in the set, thus it's not added. This implies, that performing additional `contains()` call is not required. If `target` or `user` is already in the set, it won't be added.



# [G-12] Use constants instead of `type(uintX).max`

When you use type(uintX).max - it may result in higher gas costs because it involves a runtime operation to calculate the `type(uintX).max` at runtime. This calculation is performed every time the expression is evaluated.

To save gas, it is recommended to use constants to represent the maximum value. Declaration of a constant with the maximum value means that the value is known at compile-time and does not require any runtime calculations.


```
./CdpManager.sol:378:            _maxIterations = type(uint256).max;
./LeverageMacroReference.sol:39:        ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
./LeverageMacroReference.sol:40:        stETH.approve(_borrowerOperationsAddress, type(uint256).max);
./LeverageMacroReference.sol:41:        stETH.approve(_activePool, type(uint256).max);
./LeverageMacroReference.sol:53:        ebtcToken.approve(address(borrowerOperations), type(uint256).max);
./LeverageMacroReference.sol:54:        stETH.approve(address(borrowerOperations), type(uint256).max);
./LeverageMacroReference.sol:55:        stETH.approve(address(activePool), type(uint256).max);
./LeverageMacroDelegateTarget.sol:21:    ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);
./LeverageMacroDelegateTarget.sol:22:    stETH.approve(_borrowerOperationsAddress, type(uint256).max);
./LeverageMacroDelegateTarget.sol:23:    stETH.approve(_activePool, type(uint256).max);
./Governor.sol:76:        for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:84:            for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:98:        for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:107:            for (uint8 i = 0; i < type(uint8).max; i++) {
./EBTCToken.sol:143:        if (cachedAllowance != type(uint256).max) {
./EbtcMath.sol:7:    uint256 public constant MAX_TCR = type(uint256).max;
./CdpManagerStorage.sol:21:    uint128 public constant UNSET_TIMESTAMP = type(uint128).max;
./SortedCdps.sol:90:            _size = type(uint256).max;
./BorrowerOperations.sol:1133:        return type(uint112).max;
./HintHelpers.sol:79:            _maxIterations = type(uint256).max;
```


# [G-13] Calculations which use constants can be precalculated

[File: EbtcMath.so](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L38)
```
 decProd = (prod_xy + (DECIMAL_PRECISION / 2)) / DECIMAL_PRECISION;
```

Since `DECIMAL_PRECISION` is already defined as constant: `DECIMAL_PRECISION = 1e18`, `DECIMAL_PRECISION / 2` can be pre-calculated


[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L141)
```
uint256 public constant MIN_REDEMPTION_FEE_FLOOR = (DECIMAL_PRECISION * 5) / 1000; // 0.5%
```

Since `DECIMAL_PRECISION` is already defined as constant, `(DECIMAL_PRECISION * 5) / 1000` can be pre-calculated


# [G-14] Use bit shifts instead of division by 2

[File: EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L76-L81)
```
  n = n / 2;
(...)
  n = (n - 1) / 2;
```


# [G-15] Operations which won't underflow can be unchecked

[File: EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L81)
```
 n = (n - 1) / 2;
```

Above line is being executed in `while (n > 1)` loop, which implies, that `n > 1`, so `(n - 1)` won't underflow, thus it can be unchecked


[File: EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L89)
```
return (_a >= _b) ? (_a - _b) : (_b - _a);
```

Condition `_a >= _b` implies, that this line can be unchecked (if `_a >= _b`, then `_a - _b` won't underflow, if `_b > _a`, then `_b - _a` won't underflow).


# [G-16] `if`-`else` condition is not needed in `EbtcMath.sol` in `_computeCR()` and `_computeNominalCR()`

[File: EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L109-L118)
```
 if (_debt > 0) {
            uint256 newCollRatio = (_stEthBalance * _price) / _debt;

            return newCollRatio;
        }
        // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
        else {
            // if (_debt == 0)
            return MAX_TCR;
        }
```

Since `_dept` is `uint256`, it can either be equal to 0, or greater than zero. This implies, that there's no need for `else` condition and code can be rewritten:
```
 if (_debt > 0) {
            uint256 newCollRatio = (_stEthBalance * _price) / _debt;

            return newCollRatio;
        }
       
            return MAX_TCR;
 
```

The same issue occurs in `_computeNominalCR()`

[File: EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L93-L99)
```
if (_debt > 0) {
            return (_collShares * NICR_PRECISION) / _debt;
        }
        // Return the maximal value for uint256 if the Cdp has a debt of 0. Represents "infinite" CR.
        else {
            // if (_debt == 0)
            return MAX_TCR;
```


# [G-17] Redundant variable declaration in `EbtcMath.sol`

[File: EbtcMath.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcMath.sol#L110-L112)
```
 uint256 newCollRatio = (_stEthBalance * _price) / _debt;

            return newCollRatio;
```

`newCollRatio` is used only one, thus there's no need to declare it at all:

```
return (_stEthBalance * _price) / _debt;
```


# [G-18] Redundant variable declaration in `EbtcBase.sol`

[File: EbtcBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Dependencies/EbtcBase.sol#L108-L109)
```
 uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;
        require(feePercentage <= _maxFeePercentage, "Fee exceeded provided maximum");
```

`feePercentage` is used only once, which means it doesn't need to be declared at all:
```
require((_fee * DECIMAL_PRECISION) / _amount <= _maxFeePercentage, "Fee exceeded provided maximum");
```

# [G-19] Redundant variable declaration in `LeverageMacroDelegateTarget.sol`

[File: LeverageMacroDelegateTarget.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroDelegateTarget.sol#L64-L65)
```
        address _owner = IOwnerLike(address(this)).owner();
        return _owner;
```

Variable `_owner` is used only once, which means it doesn't need to be declared at all:

```
return IOwnerLike(address(this)).owner();
```


# [G-20] Redundant variable declaration int `LeverageMacroBase.sol`

[File: LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L292-L293)
```
 uint256 beforeSwapsLength = operation.swapsBefore.length;
        if (beforeSwapsLength > 0) {
```

`beforeSwapsLength` is used only once, which means it does not need to be declared at all:

```
if (operation.swapsBefore.length > 0) {
```

[File: LeverageMacroBase.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L306-L307)
```
        uint256 afterSwapsLength = operation.swapsAfter.length;
        if (afterSwapsLength > 0) {
```

`afterSwapsLength` is used only once, which means it does not need to be declared at all:

```
        if (operation.swapsAfter.length > 0) {
```


# [G-21] Calculations which won't underflow in `HintHelpers.sol` can be unchecked

[File: HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L113)
```
 vars.remainingEbtcToRedeem = vars.remainingEbtcToRedeem - currentCdpDebt;
```

Above line of code can be unchecked, since it won't underflow. Please notice, that this line of code is inside `else`-block. The `if`-condition checks if `currentCdpDebt > vars.remainingEbtcToRedeem`.
This implies, that `else` is: `currentCdpDebt <= vars.remainingEbtcToRedeem`, thus `vars.remainingEbtcToRedeem - currentCdpDebt` cannot underflow and can be unchecked.


[File: HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L143)
```
 vars.remainingEbtcToRedeem = vars.remainingEbtcToRedeem - maxRedeemableEBTC;
```

Please, notice that in line 139, `maxRedeemableEBTC` is defined as: `EbtcMath._min(vars.remainingEbtcToRedeem, currentCdpDebt)`.
This implies that: 
* If `maxRedeemableEBTC = EbtcMath._min(vars.remainingEbtcToRedeem, currentCdpDebt) = vars.remainingEbtcToRedeem`, then `vars.remainingEbtcToRedeem - maxRedeemableEBTC = 0` and calculation can be unchecked.
* If `maxRedeemableEBTC = EbtcMath._min(vars.remainingEbtcToRedeem, currentCdpDebt) = currentCdpDebt`, then `vars.remainingEbtcToRedeem - maxRedeemableEBTC > 0` and calculation can be unchecked.

# [G-22] Redundant variables in `HintHelpers.sol`

[File: HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L141-L148)
```
uint256 newCollShare = cdpManager.getSyncedCdpCollShares(vars.currentCdpId);

        vars.remainingEbtcToRedeem = vars.remainingEbtcToRedeem - maxRedeemableEBTC;
        uint256 collShareToReceive = collateral.getSharesByPooledEth(
            (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
        );

        uint256 _newCollShareAfter = newCollShare - collShareToReceive;

```

`newCollShare` is used only once, which means they don't need to be declated at all:

```

        vars.remainingEbtcToRedeem = vars.remainingEbtcToRedeem - maxRedeemableEBTC;
        uint256 collShareToReceive = collateral.getSharesByPooledEth(
            (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
        );

        uint256 _newCollShareAfter = cdpManager.getSyncedCdpCollShares(vars.currentCdpId) - collShareToReceive;
        
```

[File: HintHelpers.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L184-L189)
```
 uint256 arrayIndex = latestRandomSeed % arrayLength;
            bytes32 _cId = cdpManager.getIdFromCdpIdsArray(arrayIndex);
            uint256 currentNICR = cdpManager.getSyncedNominalICR(_cId);

            // check if abs(current - CR) > abs(closest - CR), and update closest if current is closer
            uint256 currentDiff = EbtcMath._getAbsoluteDifference(currentNICR, _CR);
```

`arrayIndex` and `currentNICR` are used only once, which means they do not need to be declared at all:

```
            bytes32 _cId = cdpManager.getIdFromCdpIdsArray(latestRandomSeed % arrayLength);

            // check if abs(current - CR) > abs(closest - CR), and update closest if current is closer
            uint256 currentDiff = EbtcMath._getAbsoluteDifference(cdpManager.getSyncedNominalICR(_cId), _CR);
```


# [G-23] Redundant variables in `SortedCdps.sol`
`_tmp` is used only once, which means it does not need to be declared at all:

[File: SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L124-L125)
```
uint256 _tmp = uint256(cdpId) >> ADDRESS_SHIFT;
        return address(uint160(_tmp));
```

can be changed to:

```
        return address(uint160(uint256(cdpId) >> ADDRESS_SHIFT));
```


# [G-24] Change order of `require` statemens in `_insert()` in `SortedCdps.sol`

[File: SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L365-L371)
```
        require(!isFull(), "SortedCdps: List is full");
        // List must not already contain node
        require(!contains(_id), "SortedCdps: List already contains the node");
        // Node id must not be null
        require(_id != dummyId, "SortedCdps: Id cannot be zero");
        // NICR must be non-zero
        require(_NICR > 0, "SortedCdps: NICR must be positive");
```

There are multiple of fixes which could save some gas
* It's not possible to insert `_id` when it's `dummyId`. This implies, that if `_id == dummyId`, then the first require will return true: `require(!contains(_id))`  (since it does not contain `_id`), and function will return on the second require: `require(_id != dummyId)`. It means, that it's better to check if `_id != dummyId` first, and then check if `!contains(_id)`.

* First reverts should use less gas then the last ones. This implies that `require(_NICR > 0)` and `require(_id != dummyId` should be executed first:

```
        // Node id must not be null
        require(_id != dummyId, "SortedCdps: Id cannot be zero");
        // NICR must be non-zero
        require(_NICR > 0, "SortedCdps: NICR must be positive");
        require(!isFull(), "SortedCdps: List is full");
        // List must not already contain node
        require(!contains(_id), "SortedCdps: List already contains the node");

```


# [G-25] Use tautology to save gas in `_requireValidRecipient()` in `EBTCToken.sol`

`!A && !B == !(A || B)`
We can rewrite require statements in function `_requireValidRecipient()` from `EBTCToken.sol` to save one negation.

A quick test in Remix IDE was done:

```
function requireValidRecipientV1(address _recipient) public view {
        uint gas = gasleft();
        require(
            _recipient != address(0) && _recipient != address(this),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );
         require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );
        console.log(gas - gasleft());
 }

  function requireValidRecipientV2(address _recipient) public view {
        uint gas = gasleft();
        require(
            !(_recipient == address(0) || _recipient == address(this)),
            "EBTC: Cannot transfer tokens directly to the EBTC token contract or the zero address"
        );
         require(
            _recipient != cdpManagerAddress && _recipient != borrowerOperationsAddress,
            "EBTC: Cannot transfer tokens directly to the CdpManager or BorrowerOps"
        );
        console.log(gas - gasleft());
 }
```

`requireValidRecipientV1()` used 4446 gas
`requireValidRecipientV2()` used 4440 gas
This implies, that the 2nd version is more optimized.


# [G-26] Redundant variables in `_syncGracePeriod()` in `CdpManagerStorage.sol`

[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L73)
```
 function _syncGracePeriod() internal {
        uint256 price = priceFeed.fetchPrice();
        uint256 tcr = _getCachedTCR(price);
        bool isRecoveryMode = _checkRecoveryModeForTCR(tcr);

        if (isRecoveryMode) {
            _startGracePeriod(tcr);
        } else {
            _endGracePeriod(tcr);
        }
    }
```

`isRecoveryMode` and `price` variables are used only once, which implies that above code can be changed to:

```
 function _syncGracePeriod() internal {
        uint256 tcr = _getCachedTCR(priceFeed.fetchPrice());

        if (_checkRecoveryModeForTCR(tcr)) {
            _startGracePeriod(tcr);
        } else {
            _endGracePeriod(tcr);
        }
    }
```

# [G-27] Use tautology to save gas in  `CdpManagerStorage.sol`

`!A && !B == !(A || B)`
We can rewrite require statements to save one negation:

[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L262)
```
        require(
            closedStatus != Status.nonExistent && closedStatus != Status.active,
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
```

can be changed to:
```
        require(
            !(closedStatus == Status.nonExistent || closedStatus == Status.active),
            "CdpManagerStorage: close non-exist or non-active CDP!"
        );
```

[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L467)
```
cdpStatus != Status.nonExistent && cdpStatus != Status.active,
```

can be changed to:

```
!(cdpStatus == Status.nonExistent || cdpStatus == Status.active),
```


# [G-28] Redundant variable in `_computeTCRWithGivenSystemValues()` in `CdpManagerStorage.sol`

[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L494-L495)
```
 uint256 _totalColl = collateral.getPooledEthByShares(_systemCollShares);
        return EbtcMath._computeCR(_totalColl, _systemDebt, _price);
```

`_totalColl` is used only once which means it dosn't need to be declared at all:

```
        return EbtcMath._computeCR(collateral.getPooledEthByShares(_systemCollShares), _systemDebt, _price);
```


# [G-29] Redundant variables in `_calcDecayedBaseRate()` in `CdpManager.sol`

[File: CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L703-L706)
```
uint256 minutesPassed = _minutesPassedSinceLastRedemption();
        uint256 decayFactor = EbtcMath._decPow(minuteDecayFactor, minutesPassed);

        return (baseRate * decayFactor) / DECIMAL_PRECISION;
```

`minutesPassed` and `decayFactor` are used only once which means they don't need to be declared at all:

```
        return (baseRate * EbtcMath._decPow(minuteDecayFactor, _minutesPassedSinceLastRedemption())) / DECIMAL_PRECISION;
```


# [G-30] Substraction in `_addCdpIdToArray()` in `CdpManager.sol` can be unchecked

[File: CdpManager.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L555)
```
 CdpIds.push(_cdpId);

        // Record the index of the new Cdpowner on their Cdp struct
        index = uint128(CdpIds.length - 1);
```

Beacause of `CdpIds.push(_cdpId)`, we know that `CdpIds` has at least one element, thus `CdpIds.length - 1` won't overflow and can be unchecked.



# [G-31] Iterators in loop can be unchecked and post-incremented

```
./Governor.sol:46:        for (uint256 i = 0; i < users.length(); i++) {
./Governor.sol:57:            for (uint256 i = 0; i < _usrs.length; i++) {
./Governor.sol:62:                    j++;
./Governor.sol:76:        for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:84:            for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:87:                    j++;
./Governor.sol:98:        for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:107:            for (uint8 i = 0; i < type(uint8).max; i++) {
./Governor.sol:111:                    j++;
./Governor.sol:122:        for (uint8 i = 0; i < roleIds.length; i++) {
./Governor.sol:137:            for (uint256 i = 0; i < _sigs.length; ++i) {
./EBTCToken.sol:214:                    abi.encode(_PERMIT_TYPEHASH, owner, spender, amount, _nonces[owner]++, deadline)
./SortedCdps.sol:196:            ++i;
./SortedCdps.sol:253:            ++i;
./SortedCdps.sol:322:                ++_cdpRetrieved;
./SortedCdps.sol:324:            ++i;
./SortedCdps.sol:357:            ++nextCdpNonce;
./SortedCdps.sol:432:        for (uint256 i = 0; i < _len; ++i) {
./SortedCdps.sol:449:        for (uint i = 0; i < _len; ++i) {
./LiquidationLibrary.sol:800:            ++vars.i;
./LiquidationLibrary.sol:830:            ++vars.i;
./LeverageMacroBase.sol:388:                ++i;
./LeverageMacroBase.sol:438:            for (uint256 i; i < length; ++i) {
./BorrowerOperations.sol:727:                        _nonces[_borrower]++,
./HintHelpers.sol:195:            i++;
./SimplifiedDiamondLike.sol:118:                ++i;
./CdpManager.sol:429:            _maxIterations--;
```


# [G-32] Substraction in `_remove()` in `SortedCdps.sol` can be unchecked

[File: SortedCdps.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/SortedCdps.sol#L489)
```
data.size = data.size - 1;
```

Because of the `require(contains(_id), "SortedCdps: List does not contain the id");` at line 458, we know, that `data.size >= 1`, thus `data.size - 1` won't underflow and can be unchecked.

# [G-33] Redundant variables in `calcFeeUponStakingReward()` in `CdpManagerStorage.sol`

Variables `deltaIndex`, `deltaIndexFees` and `_deltaFeeSplit` are used only once, which means they don't need to be declared at all.
Below code:
[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L557)
```
        uint256 deltaIndex = _newIndex - _prevIndex;
        uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;

        // we take the fee for all CDPs immediately which is scaled by index precision
        uint256 _deltaFeeSplit = deltaIndexFees * getSystemCollShares();
        uint256 _cachedAllStakes = totalStakes;
        // return the values to update the global fee accumulator
        uint256 _feeTaken = collateral.getSharesByPooledEth(_deltaFeeSplit) / DECIMAL_PRECISION;
```

can be changed to:

```

        uint256 _cachedAllStakes = totalStakes;
        // return the values to update the global fee accumulator
        uint256 _feeTaken = collateral.getSharesByPooledEth(((_newIndex - _prevIndex * stakingRewardSplit) / MAX_REWARD_SPLIT) * getSystemCollShares()) / DECIMAL_PRECISION;

```

# [G-34] Substraction in `calcFeeUponStakingReward` in `CdpManagerStorage.sol` can be unchecked

[File: CdpManagerStorage.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L557)
```
 uint256 deltaIndex = _newIndex - _prevIndex;
```

Line `require(_newIndex > _prevIndex, "CDPManager: only take fee with bigger new index");` implies, that `_newIndex > _prevIndex`, thus `uint256 deltaIndex = _newIndex - _prevIndex;` can be unchecked.

# [G-35] Perform allowance check before transfer in `EBTCToken.sol`

[File: EBTCToken.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/EBTCToken.sol#L134)
```
    function transferFrom(
        address sender,
        address recipient,
        uint256 amount
    ) external override returns (bool) {
        _requireValidRecipient(recipient);
        _transfer(sender, recipient, amount);

        uint256 cachedAllowance = _allowances[sender][msg.sender];
        if (cachedAllowance != type(uint256).max) {
            require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");
            unchecked {
                _approve(sender, msg.sender, cachedAllowance - amount);
            }
        }
        return true;
    }
```

Current implementation firstly performs transfer: `_transfer(sender, recipient, amount)` and later - checks for allowances: `require(cachedAllowance >= amount, "ERC20: transfer amount exceeds allowance");`.
This is a waste of gas, when transfer is not approved. Firstly, we will waste gas on `_transfer()`, and then, function will perform allowance check and revert.
Much better idea would be to firstly check for allowance, and then, perform `_transfer()`. This is exactly how it's done in Open Zeppelin ERC-20 implementation.