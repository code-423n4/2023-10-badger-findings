## [L-01] Stop Using Solidity's transfer() Now
**Proof Of Concept**
https://consensys.io/diligence/blog/2019/09/stop-using-soliditys-transfer-now/
```
  collateral.transfer(address(receiver), amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L274C7-L274C56

```
  collateral.transfer(feeRecipientAddress, fee);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/ActivePool.sol#L286C7-L286C55

```
 function transfer(address recipient, uint256 amount) external override returns (bool) {
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L119C4-L119C92

```
  emit Transfer(account, address(0), amount);
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/EBTCToken.sol#L282C7-L282C52

```
 ebtcToken.transfer(msg.sender, ebtcBal);
        }
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L224C12-L225C10

## [L-02] Keccak Constant values should used to immutable rather than constant
There is a difference between constant variables and immutable variables, and they should each be used in their appropriate contexts.

While it doesn’t save any gas because the compiler knows that developers often make this mistake, it’s still best to use the right tool for the task at hand.

```
  bytes32 constant FLASH_LOAN_SUCCESS = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/LeverageMacroBase.sol#L37C3-L37C89

```
 bytes32 constant DIAMOND_STORAGE_POSITION = keccak256("diamond.standard.diamond.storage");
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/SimplifiedDiamondLike.sol#L39C4-L39C95

```
 bytes32 public constant FLASH_SUCCESS_VALUE = keccak256("ERC3156FlashBorrower.onFlashLoan");
```

https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/Dependencies/ERC3156FlashLender.sol#L11C4-L11C97

## [L-03] Divide before multiply
Solidity's integer division truncates. Thus, performing division before multiplication can lead to precision loss.

```
 singleRedemption.collSharesDrawn = collateral.getSharesByPooledEth(
            (singleRedemption.debtToRedeem * DECIMAL_PRECISION) / _redeemColFromCdp.price
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L145C8-L146C90

```
  uint256 redeemedEBTCFraction = (collateral.getPooledEthByShares(_ETHDrawn) * _price) /
            _totalEBTCSupply;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L621C7-L622C30


```
  uint256 redemptionFee = (_redemptionRate * _ETHDrawn) / DECIMAL_PRECISION;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManager.sol#L671C7-L671C83

```
   if (_debtIndexDiff > 0) {
            pendingEBTCDebtReward = (cdp.stake * _debtIndexDiff) / DECIMAL_PRECISION;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L315C6-L316C86

```
stake = (_coll * totalStakesSnapshot) / totalCollateralSnapshot;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L454C13-L454C77

```
  uint256 deltaIndexFees = (deltaIndex * stakingRewardSplit) / MAX_REWARD_SPLIT;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/CdpManagerStorage.sol#L558C7-L558C87

```
 uint256 percentDeviation = maxPrice > 0
            ? ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) / maxPrice
            : 0;

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L457C8-L460C1

```
 uint256 percentPriceDifference = ((maxPrice - minPrice) * EbtcMath.DECIMAL_PRECISION) /
            minPrice;
```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/PriceFeed.sol#L534C8-L535C22

```
 uint256 collShareToReceive = collateral.getSharesByPooledEth(
            (maxRedeemableEBTC * DECIMAL_PRECISION) / _price
        );

```
https://github.com/code-423n4/2023-10-badger/blob/main/packages/contracts/contracts/HintHelpers.sol#L144C8-L147C1

# Non- Critical

## [N-01] Use SMTChecker

The highest tier of smart contract behavior assurance is formal mathematical verification. All assertions that are made are guaranteed to be true across all inputs → The quality of your asserts is the quality of your verification.

https://twitter.com/0xOwenThurm/status/1614359896350425088?t=dbG9gHFigBX85Rv29lOjIQ&s=19

## [N-02] Assembly Codes Specific – Should Have Comments

Since this is a low level language that is more difficult to parse by readers, include extensive documentation, comments on the rationale behind its use, clearly explaining what each assembly instruction does.

This will make it easier for users to trust the code, for reviewers to validate the code, and for developers to build on or update the code.

Note that using Assembly removes several important security features of
Solidity, which can make the code more insecure and more error-prone.

## [N-03] Use the delete keyword instead of assigning a value of 0

Using the ‘delete’ keyword instead of assigning a ‘0’ value is a detailed optimization that increases code readability and audit quality, and clearly indicates the intent.

Other hand, if use delete instead 0 value assign , it will be gas saved.