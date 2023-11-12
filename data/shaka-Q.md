# Low Risk Issues

| ID |Title|Instances|
|:--:|:-------|:--:|
|[L-01]| Misleading comments for protocol integrations | 1 |

## [L-01] Misleading comments for protocol integrations

```solidity
File: SortedCdps.sol
134:     /// @notice Find a specific CDP for a given owner, indexed by it's place in the linked list relative to other Cdps owned by the same address
135:     /// @notice Reverts if the index exceeds the number of active Cdps owned by the given owner 👈
136:     /// @dev Intended for off-chain use, O(n) operation on size of SortedCdps linked list
137:     /// @param owner address of CDP owner
138:     /// @param index index of CDP, ordered by position in linked list relative to Cdps of the same owner
139:     /// @return CDP Id if found
140:     function cdpOfOwnerByIndex(
```

The comment `Reverts if the index exceeds the number of active Cdps owned by the given owner` is not correct. If the index exceeds the number of active Cdps owned by the given owner, the function returns `dummyId` instead of reverting.

The only place where it is used is `LeverageMacroBase` and there are checks in place to ensure that the CDP is valid, but it is recommended either updating natspec or adding a require statement to avoid wrong assumptions in future integrations.

# Non-Critical Issues

| ID |Title|Instances|
|:--:|:-------|:--:|
|[N-01]| Unused or unnecessary variables | 3 |
|[N-02]| Unused functions | 2 |
|[N-03]| Incorrect comments and erratas | 16 |


## [N-01] Unused or unnecessary variables

```solidity
File: CdpManager.sol
244:     function _closeCdpByRedemption(
245:         bytes32 _cdpId,
246:         uint256 _EBTC, 👈 always 0
247:         uint256 _collSurplus,
248:         uint256 _liquidatorRewardShares,
249:         address _borrower
250:     ) internal {
```

```solidity
File: HintHelpers.sol
19:     struct LocalVariables_getRedemptionHints {
20:         uint256 remainingEbtcToRedeem;
21:         uint256 minNetDebtInBTC; 👈
22:         bytes32 currentCdpId;
23:         address currentCdpUser;
24:     }
```

```solidity
File: HintHelpers.sol
133:     function _calculateCdpStateAfterPartialRedemption(
134:         LocalVariables_getRedemptionHints memory vars,
135:         uint256 currentCdpDebt,
136:         uint256 _price
137:     ) internal view returns (uint256, uint256) {
138:         // maxReemable = min(remainingToRedeem, currentDebt)
139:         uint256 maxRedeemableEBTC = EbtcMath._min(vars.remainingEbtcToRedeem, currentCdpDebt); 👈 This is called when currentCdpDebt > remainingEbtcToRedeem, so always maxRedeemableEBTC = remainingEbtcToRedeem
```

## [N-02] Unused functions

```solidity
File: EBTCToken.sol
306:     function _requireCallerIsBorrowerOperations() internal view {
307:         require(
308:             msg.sender == borrowerOperationsAddress,
309:             "EBTCToken: Caller is not BorrowerOperations"
310:         );
311:     }
```

```solidity
File: EBTCToken.sol
323:     function _requireCallerIsCdpM() internal view {
324:         require(msg.sender == cdpManagerAddress, "EBTC: Caller is not CdpManager");
325:     }
```

## [N-03] Incorrect comments and erratas

```solidity
File: CdpManager.sol
315:     /// @param _upperPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)
316:     /// @param _lowerPartialRedemptionHint The first CdpId to be considered for redemption, could get from HintHelper.getApproxHint(_partialRedemptionHintNICR) then SortedCdps.findInsertPosition(_partialRedemptionHintNICR)
```

```solidity
File: CdpManager.sol
593:     // Check whether or not the system *would be* in Recovery Mode,
594:     // given an ETH:USD price, and the entire system coll and debt. 👈 should be `stETH:BTC`
595:     function _checkPotentialRecoveryMode(
```

```solidity
File: CdpManager.sol
619:         /* Convert the drawn ETH back to EBTC at face value rate (1 EBTC:1 USD), in order to get 👈 should be `1 EBTC = 1 BTC`
620:          * the fraction of total supply that was redeemed at face value. */
621:         uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
622:             _totalEBTCSupply;
```

```solidity
File: CdpManager.sol
721:     /// @notice Check whether or not the system *would be* in Recovery Mode,
722:     /// @notice given an ETH:eBTC price, and the entire system coll and debt. 👈 should be `stETH:BTC`
```

```solidity
File: CdpManagerStorage.sol
134:     // A doubly linked list of Cdps, sorted by their sorted by their collateral ratios 👈 `sorted by their` repeated
135:     ISortedCdps public immutable sortedCdps;
```

```solidity
File: CollSurplusPool.sol
34:     /**
35:      * @notice Sets the addresses of the contracts and renounces ownership
36:      * @dev One-time initialization function. Can only be called by the owner as a security measure. Ownership is renounced after the function is called. 👈 not applicable
37:      * @param _borrowerOperationsAddress The address of the BorrowerOperations
38:      * @param _cdpManagerAddress The address of the CDPManager
39:      * @param _activePoolAddress The address of the ActivePool
40:      * @param _collTokenAddress The address of the CollateralToken
41:      */
``````

```solidity
File: HintHelpers.sol
207:     /// @notice Compute CR for a specified collateral, debt amount, and price
208:     /// @param _coll The collateral amount, in shares 👈 it is collateral balance, not shares
209:     /// @param _debt The debt amount
210:     /// @param _price The current price
211:     /// @return The computed CR for the given parameters
```

```solidity
File: LeverageMacroBase.sol
462:         /**
463:          * Open CDP and Emit event 👈 no event emitted
464:          */
465:         bytes32 _cdpId = borrowerOperations.openCdp(
466:             flData.eBTCToMint,
467:             flData._upperHint,
468:             flData._lowerHint,
469:             flData.stETHToDeposit
470:         );
```

```solidity
File: LeverageMacroDelegateTarget.sol
26: /**
27:  * @title Implementation of the LeverageMacro, meant to be called via a delegatecall by a SC Like Wallet
28:  * @notice The Caller MUST implement the `function owner() external view returns (address)`
29:  * @notice to use this contract:
30:  *      Add this logic address to `callbackHandler` for the function `onFlashLoan`
31:  *      Add the inteded allowances (see above) 👈 typo in `inteded`, should be `intended`
32:  *      Toggle the `callbackEnabledForCall` for the current call, by adding a call to `enableCallbackForCall`
33:  *      Perform the operation
```

```solidity
File: LiquidationLibrary.sol
36:     /// @notice Fully liquidate a single Cdp by ID. Cdp must meet the criteria for liquidation at the time of execution.
37:     /// @notice callable by anyone, attempts to liquidate the CdpId. Executes successfully if Cdp meets the conditions for liquidation (e.g. in Normal Mode, it liquidates if the Cdp's ICR < the system MCR).
38:     /// @dev forwards msg.data directly to the liquidation library using OZ proxy core delegation function 👈 not applicable
39:     /// @param _cdpId ID of the Cdp to liquidate.
40:     function liquidate(bytes32 _cdpId) external nonReentrantSelfAndBOps {
```

```solidity
File: LiquidationLibrary.sol
44:     /// @notice Partially liquidate a single Cdp.
45:     /// @dev forwards msg.data directly to the liquidation library using OZ proxy core delegation function 👈 not applicable
46:     /// @param _cdpId ID of the Cdp to partially liquidate.
47:     /// @param _partialAmount Amount to partially liquidate.
48:     /// @param _upperPartialHint Upper hint for reinsertion of the Cdp into the linked list.
49:     /// @param _lowerPartialHint Lower hint for reinsertion of the Cdp into the linked list.
50:     function partiallyLiquidate(
```

```solidity
File: LiquidationLibrary.sol
673:     /// @notice Attempt to liquidate a custom list of Cdps provided by the caller
674:     /// @notice Callable by anyone, accepts a custom list of Cdps addresses as an argument.
675:     /// @notice Steps through the provided list and attempts to liquidate every Cdp, until it reaches the end or it runs out of gas.
676:     /// @notice A Cdp is liquidated only if it meets the conditions for liquidation.
677:     /// @dev forwards msg.data directly to the liquidation library using OZ proxy core delegation function 👈 not applicable
678:     /// @param _cdpArray Array of Cdps to liquidate.
679:     function batchLiquidateCdps(bytes32[] memory _cdpArray) external nonReentrantSelfAndBOps {
```

```solidity
File: SortedCdps.sol
21:  * The list relies on the fact that liquidation events preserve ordering: a liquidation decreases the NICRs of all active Cdps,
22:  * but maintains their order. A node inserted based on current NICR will maintain the correct position,
23:  * relative to it's peers, as rewards accumulate, as long as it's raw collateral and debt have not changed. 👈 typo in `it's`, should be `its`
24:  * Thus, Nodes remain sorted by current NICR.
```

```solidity
File: AuthNoOwner.sol
33:         // Checking if the caller is the owner only after calling the authority saves gas in most cases, but be
34:         // aware that this makes protected functions uncallable even to the owner if the authority is out of order. 👈 not applicable
35:         return (address(auth) != address(0) && auth.canCall(user, address(this), functionSig));
```

```solidity
File: AuthNoOwner.sol
39:         // We check if the caller is the owner first because we want to ensure they can
40:         // always swap out the authority even if it's reverting or using up a lot of gas. 👈 not applicable
41:         require(_authority.canCall(msg.sender, address(this), msg.sig));
```

```solidity
File: EbtcBase.sol
35:     uint256 public constant BORROWING_FEE_FLOOR = 0; // 0.5%
```