

## LOW Risk

| Number | Issue | Instances |
|--------|-------|-----------|
|[L-01]| Use of transfer instead of safeTransfer   | 4 |
|[L-02]| Use descriptive constant instead of 0 as a parameter  | 27 |
|[L-03]| Execution at deadlines should be allowed   | 3 |
|[L-04]| Constant array index within iteration  | 2 |
|[L-05]| payable function does not transfer ETH   | 2 |
|[L-06]| Functions calling contracts with transfer hooks are missing reentrancy guards   | 1 |
|[L-07]| Subtraction may underflow if multiplication is too large   | 3 |
|[L-08]| Use of abi.encodePacked with dynamic types inside keccak256   | 1 |
|[L-09]| Loss of precision on division   | 10 |
|[L-10]| No access control on receive/payable fallback   | 2 |
|[L-11]| Array is push()ed but not pop()ed   | 1 |
|[L-12]| Missing checks for address(0) when updating state variables   | 5 |
|[L-13]| Array lengths not checked   | 7 |
|[L-14]| Unused/empty receive/fallback   | 1 |
|[L-15]| Missing checks for address(0) in constructor   | 14 |
|[L-16]| Return values of approve not checked   | 6 |
|[L-17]| Use of ecrecover is susceptible to signature malleability   | 2 |
|[L-18]| Missing zero address check in initializer   | 2 |
|[L-19]| Named return variable used before assignment   | 1 |
|[L-20]| Revert on transfer to the zero address   | 2 |


## [L-01] Use of transfer instead of safeTransfer

It is good to add a require statement that checks the return value of token transfers, or to use something like OpenZeppelin's safeTransfer/safeTransferFrom, even if one is sure that the given token reverts in case of a failure.

This reduces the risk to zero even if these contracts are upgreadable, and it also helps with security reviews, as the auditor will not have to check this specific edge case.

```solidity
file:  main/packages/contracts/contracts/ActivePool.sol

381    IERC20(token).safeTransfer(cachedFeeRecipientAddress, amount);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L381

```solidity
file:  main/packages/contracts/contracts/CollSurplusPool.sol

148    IERC20(token).safeTransfer(feeRecipientAddress, amount);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L148

```solidity
file:  main/packages/contracts/contracts/LeverageMacroBase.sol

237   IERC20(token).safeTransfer(msg.sender, amount);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L237

```solidity
file:  main/packages/contracts/contracts/LeverageMacroBase.sol

129     IERC20(operation.tokenToTransferIn).safeTransferFrom(
                msg.sender,
                address(this),
                operation.amountToTransferIn
            );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L129-L133

## [L‑02] Use descriptive constant instead of 0 as a parameter

Passing 0 or 0x0 as a function argument can sometimes result in a security issue(e.g. passing zero as the slippage parameter). A historical example is the infamous 0x0 address bug where numerous tokens were lost. This happens because 0 can be interpreted as an uninitialized address, leading to transfers to the 0x0 address, effectively burning tokens. Moreover, 0 as a denominator in division operations would cause a runtime exception. It's also often indicative of a logical error in the caller's code.

Consider using a constant variable with a descriptive name, so it's clear that the argument is intentionally being used, and for the right reasons.

```solidity
file:  main/packages/contracts/contracts/BorrowerOperations.sol

209   _adjustCdpInternal(_cdpId, 0, 0, false, _upperHint, _lowerHint, _stEthBalanceIncrease);

225   _adjustCdpInternal(_cdpId, _stEthBalanceDecrease, 0, false, _upperHint, _lowerHint, 0);

256   _adjustCdpInternal(_cdpId, 0, _debt, false, _upperHint, _lowerHint, 0);

807     require(
            _stEthBalanceIncrease == 0 || _stEthBalanceDecrease == 0,
            "BorrowerOperations: Cannot add and withdraw collateral in same operation"
        );

818     require(
            _stEthBalanceIncrease != 0 || _stEthBalanceDecrease != 0 || _debtChange != 0,
            "BorrowerOperations: There must be either a collateral change or a debt change"
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L209


```slidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

144   success := delegatecall(txGas, to, add(data, 0x20), mload(data), 0, 0) 

149   success := call(txGas, to, value, add(data, 0x20), mload(data), 0, 0)

190   calldatacopy(0, 0, calldatasize())

191   let result := delegatecall(gas(), facet, 0, calldatasize(), 0, 0)

192   returndatacopy(0, 0, returndatasize())

195   revert(0, returndatasize())

198   return(0, returndatasize())

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L144


```solidity
file:  main/packages/contracts/contracts/SortedCdps.sol

275   (bytes32[] memory _allCdps, , ) = _getCdpsOf(owner, dummyId, 0, _ownedCount);

306   return (new bytes32[](0), 0, dummyId);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L275

```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

41    _liquidateIndividualCdpSetup(_cdpId, 0, _cdpId, _cdpId);

101    LiquidationLocals memory _liqState = LiquidationLocals(
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
        );

117    LiquidationRecoveryModeLocals memory _rs = LiquidationRecoveryModeLocals(
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
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L41


```solidity
file:  main/packages/contracts/contracts/LeverageMacroBase.sol

414    (bool success, ) = excessivelySafeCall(
            swapData.addressForSwap,
            gasleft(),
            0,
            0,
            swapData.calldataForSwap
        );

514     _success := call(
                _gas, // gas
                _target, // recipient
                _value, // ether value
                add(_calldata, 0x20), // inloc
                mload(_calldata), // inlen
                0, // outloc
                0 // outlen
            )

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L414-L420

```solidity
file:  main/packages/contracts/contracts/CdpManager.sol

171   _closeCdpByRedemption(
                    _redeemColFromCdp.cdpId,
                    0,
                    newColl,
                    _liquidatorRewardShares,
                    _borrower
                );

179   emit CdpUpdated(
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
    
545  emit CdpUpdated(_cdpId, _borrower, msg.sender, _debt, _coll, 0, 0, 0, CdpOperation.closeCdp);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L171-L177

```solidity
file: main/packages/contracts/contracts/CdpManagerStorage.sol

310   return (0, 0);

318   return (0, 0);

628   return (0, _cdpCol);

643   return (0, _cdpCol);

777   return (0, systemStEthFeePerUnitIndex, systemStEthFeePerUnitIndexError);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L310

## [L-03] Execution at deadlines should be allowed

The condition may be wrong in these cases, as when block.timestamp is equal to the compared > or < variable these blocks will not be executed.

There are 3 instances of this issue.

```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

93   require(
                block.timestamp >
                    cachedLastGracePeriodStartTimestamp + recoveryModeGracePeriodDuration,
                "LiquidationLibrary: Recovery mode grace period still in effect"
            );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L93-L97


```solidity
file:  main/packages/contracts/contracts/PriceFeed.sol

419  if (
            _response.timestampEthBtc == 0 ||
            _response.timestampEthBtc > block.timestamp ||
            _response.timestampStEthEth == 0 ||
            _response.timestampStEthEth > block.timestamp
        ) {

471   if (_response.timestamp == 0 || _response.timestamp > block.timestamp) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L419-L424




## [L-04] Constant array index within iteration

Using constant array indexes within for loops is error prone as typically [i] is used instead as by using a constant index such as [0] means that only one value will be used/modified within an array, historically many bugs have been introduced through using a constant index rather than the array iteration index i.e i,j. Provided this is intentional and not a typo consider using enum values to make this distinction clear.

```solidity
file:  main/packages/contracts/contracts/CdpManager.sol

502   require(_toRemoveIds[0] == _start, "CdpManager: batchRemoveSortedCdpIds check start error");

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L502

```solidity
file: main/packages/contracts/contracts/SortedCdps.sol

424   bytes32 _firstPrev = data.nodes[_ids[0]].prevId;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SortedCdps.sol#L424 

## [L-05] payable function does not transfer ETH

The following functions can be called by any user, who may also send some funds by mistake. In that case, those funds will be lost.

There is 2 instance of this issue.

```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol

160  receive() external payable {
        // PHP is my favourite language
    }

164   fallback() external payable {
        _fallback();
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160-L162

## [L-06] Functions calling contracts with transfer hooks are missing reentrancy guards

Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks will open the users of this protocol up to read-only reentrancies with no way to protect against it, except by block-listing the whole protocol.

There is 1 instance of this issue.

```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

234   function sweepToken(address token, uint256 amount) public {
        _assertOwner();

        IERC20(token).safeTransfer(msg.sender, amount);
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L234-L238

## [L-07] Subtraction may underflow if multiplication is too large

The following expressions may underflow, as the subtrahend could be greater than the minuend in case the former is multiplied by a large number.

There are 3 instances of this issue.

```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

555   _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

579   _incentiveColl = (_totalDebtToBurn * (_ICR > MCR ? MCR : _ICR)) / _price;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L555

```solidity
file: main/packages/contracts/contracts/PriceFeed.sol

458   ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L458

## [L-08] Use of abi.encodePacked with dynamic types inside keccak256

abi.encodePacked should not be used with dynamic types when passing the result to a hash function such as keccak256. Use abi.encode instead, which will pad items to 32 bytes, to prevent any hash collisions.

There is 1 instance of this issue.

```solidity
file: main/packages/contracts/contracts/HintHelpers.sol

182   latestRandomSeed = uint256(keccak256(abi.encodePacked(latestRandomSeed)));

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L182

## [L-09] Loss of precision on division

Solidity doesn't support fractions, so divisions by large numbers could result in the quotient being zero.

To avoid this, it's recommended to require a minimum numerator amount to ensure that it is always greater than the denominator.

There are 10 instances of this issue.

```solidity
file: main/packages/contracts/contracts/Dependencies/EbtcBase.sol

108   uint256 feePercentage = (_fee * DECIMAL_PRECISION) / _amount;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/EbtcBase.sol#L108

```solidity
file:  main/packages/contracts/contracts/CdpManager.sol

146   (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price

624   uint256 newBaseRate = decayedBaseRate + (redeemedEBTCFraction / beta);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L146

```solidity
file:  main/packages/contracts/contracts/CdpManagerStorage.sol

454   stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;

567   uint256 _deltaFeePerUnit = _deltaFeeSplitShare / _cachedAllStakes;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L454

```solidity
file:  main/packages/contracts/contracts/HintHelpers.sol

145   (maxRedeemableEBTC * DECIMAL_PRECISION) / _price

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L145

```solidity
file: main/packages/contracts/contracts/LiquidationLibrary.sol

278   uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _liqState.price;

365   uint _debtToColl = (_totalDebtToBurn * DECIMAL_PRECISION) / _recoveryState.price;

435   uint _debtToColl = (_partialDebt * DECIMAL_PRECISION) / _partialState.price;

882   uint256 EBTCDebtRewardPerUnitStaked = EBTCDebtNumerator / _totalStakes;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L278

## [L-10] No access control on receive/payable fallback

Users may send ETH by mistake to these contracts. As there is no access control on these functions, the funds will be permanently lost.

There is 2 instance of this issue.

```solidity
file:  main/packages/contracts/contracts/SimplifiedDiamondLike.sol

160   receive() external payable {
        // PHP is my favourite language
    }

164  fallback() external payable {
        _fallback();
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160

## [L‑11] Array is push()ed but not pop()ed

Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed. Cases where there are specific potential problems will be flagged separately under a different issue.

There is 1 instance:

```solidity
file:  main/packages/contracts/contracts/CdpManager.sol
 
556    CdpIds.push(_cdpId);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L556

## [L-12] Missing checks for address(0) when updating state variables

Check for zero-address to avoid the risk of setting address(0) for state variables after an update.

There are 5 instances of this issue.

```solidity
file:  main/packages/contracts/contracts/ActivePool.sol

398    feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L398

```solidity
file: main/packages/contracts/contracts/Dependencies/Auth.sol

53   owner = newOwner;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L53

```solidity
file:  main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

43    _authority = Authority(newAuthority);

59    _authority = Authority(newAuthority);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L43

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

1148  feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1148



## [L-13] Array lengths not checked

If the length of the arrays are not required to be of the same length, user operations may not be fully executed.

There are 7 instances of this issue.

```solidity
file: main/packages/contracts/contracts/CdpManager.sol
 
126    function batchLiquidateCdps(bytes32[] memory _cdpArray) external override {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L126


```solidity
file: main/packages/contracts/contracts/Governor.sol

120  function getByteMapFromRoles(uint8[] memory roleIds) public pure returns (bytes32) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Governor.sol#L120


```solidity
file: main/packages/contracts/contracts/LeverageMacroBase.sol

382   function _doSwaps(SwapOperation[] memory swapData) internal {

435   function _doSwapChecks(SwapCheck[] memory swapChecks) internal {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L382


```solidity
file:  main/packages/contracts/contracts/LiquidationLibrary.sol

679    function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {

733     function _getTotalFromBatchLiquidate_RecoveryMode(
        uint256 _price,
        uint256 _systemCollShares,
        uint256 _systemDebt,
        bytes32[] memory _cdpArray
    ) internal returns (LiquidationTotals memory totals) {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LiquidationLibrary.sol#L679

## [L-14] Unused/empty receive/fallback

If the intention is for the ETH to be used, the function should call another function, otherwise it should revert (e.g. require(msg.sender == address(weth)))

There is 1 instance of this issue.

```solidity
file:  main/packages/contracts/contracts/SimplifiedDiamondLike.sol

160   receive() external payable {
        // PHP is my favourite language
    }

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L160

## [L-15] Missing checks for address(0) in constructor

Check for zero-address to avoid the risk of setting address(0) for state variables when deploying.

There are 14 instances of this issue.

```solidity
file: main/packages/contracts/contracts/SimplifiedDiamondLike.sol
 
45   owner = _owner;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L45

```solidity
file:  main/packages/contracts/contracts/Dependencies/Auth.sol

19    owner = _owner;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/Auth.sol#L19

```solidity
file:  main/packages/contracts/contracts/CdpManagerStorage.sol

229   liquidationLibrary = _liquidationLibraryAddress;

233   borrowerOperationsAddress = _borrowerOperationsAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L229


```solidity
file:  main/packages/contracts/contracts/EBTCToken.sol

68     cdpManagerAddress = _cdpManagerAddress;

69     borrowerOperationsAddress = _borrowerOperationsAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L68

```solidity
file:  main/packages/contracts/contracts/CollSurplusPool.sol

48     borrowerOperationsAddress = _borrowerOperationsAddress;

49     cdpManagerAddress = _cdpManagerAddress;

50     activePoolAddress = _activePoolAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CollSurplusPool.sol#L48

```solidity
file:  main/packages/contracts/contracts/ActivePool.sol

53      borrowerOperationsAddress = _borrowerOperationsAddress;

54      cdpManagerAddress = _cdpManagerAddress;

55      collateral = ICollateralToken(_collTokenAddress);

56      collSurplusPoolAddress = _collSurplusAddress;

57      feeRecipientAddress = _feeRecipientAddress;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L53


## [L-16] Return values of approve not checked

Not all IERC20 implementations (e.g. USDT, KNC) revert when there's a failure in approve. The function signature has a boolean return value and they indicate errors that way instead.

By not checking the return value, operations that should have marked as failed, may potentially go through without actually approving anything.

There is 6 instance of this issue.

```solidity
file:  main/packages/contracts/contracts/LeverageMacroReference.sol

39      ebtcToken.approve(_borrowerOperationsAddress, type(uint256).max);

40      stETH.approve(_borrowerOperationsAddress, type(uint256).max);

41      stETH.approve(_activePool, type(uint256).max);

53      ebtcToken.approve(address(borrowerOperations), type(uint256).max);

54      stETH.approve(address(borrowerOperations), type(uint256).max);

55      stETH.approve(address(activePool), type(uint256).max);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroReference.sol#L39

## [L‑17] Use of ecrecover is susceptible to signature malleability

The built-in EVM precompile ecrecover is susceptible to signature malleability, which could lead to replay attacks. References: https://swcregistry.io/docs/SWC-117, https://swcregistry.io/docs/SWC-121, and https://medium.com/cryptronics/signature-replay-vulnerabilities-in-smart-contracts-3b6f7596df57.

While this is not immediately exploitable, this may become a vulnerability if used elsewhere.

There is 2 instance:

```solidity
file: main/packages/contracts/contracts/BorrowerOperations.sol

733  address recoveredAddress = ecrecover(digest, v, r, s);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L733


```solidity
file: main/packages/contracts/contracts/EBTCToken.sol

218  address recoveredAddress = ecrecover(digest, v, r, s);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L218


## [L‑18] Missing zero address check in initializer

There are 2 instances (click to show):

```solidity
file: main/packages/contracts/contracts/CdpManager.sol

905    function initializeCdp(
        bytes32 _cdpId,
        uint256 _debt,
        uint256 _coll,
        uint256 _liquidatorRewardShares,
        address _borrower
    ) external {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L905-L911


```solidity
file: main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol

55  function _initializeAuthority(address newAuthority) internal {

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/AuthNoOwner.sol#L55

## [L‑19] Named return variable used before assignment

As no value is written to the variable, the default value is always read. This is usually due to a bug in the code logic that causes an invalid value to be used.

```solidity
file: main/packages/contracts/contracts/CdpManager.sol

233   return singleRedemption;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L233

## [L‑20] Revert on transfer to the zero address

It's good practice to revert a token transfer transaction if the recipient's address is the zero address. This can prevent unintentional transfers to the zero address due to accidental operations or programming errors. Many token contracts implement such a safeguard, such as OpenZeppelin - ERC20, OpenZeppelin - ERC721.

There are 2 instances:


```solidity
file: main/packages/contracts/contracts/CdpManager.sol

283   collateral.transferFrom(address(receiver), address(this), amountWithFee);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L283


```solidity
file:  main/packages/contracts/contracts/BorrowerOperations.sol

1100  ebtcToken.transferFrom(address(receiver), feeRecipientAddress, fee + amount);

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/BorrowerOperations.sol#L1100