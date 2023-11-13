# [L-01] `ActivePool.feeRecipientAddress` lacks of check that `feeRecipientAddress` should be greater than address(0)
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L57
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L286C2-L286C2
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L362
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/ActivePool.sol#L381
Impact:
`ActivePool.feeRecipientAddress` lacks of check > address(0) in `constructor` function. If `ActivePool.feeRecipientAddress` is set to `address(0)`, any stETH transfer (like ActivePool.flashLoan, ActivePool.claimFeeRecipientCollShares, ActivePool.sweepToken) before calling `ActivePool.setFeeRecipientAddress` will be sent to address(0)

# [L-02] Sanity check in BorrowerOperations.sol#L463 can be removed
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L463
Impact:
The [sanity check](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L463) can be removed because the check has been done in [BorrowerOperations.sol#L454](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L454)

# [L-03] comments don't comform with code in BorrowerOperations.sol
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L865
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L884
Impact:
Quoting from [coments](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L865)
 > A debt increase combined with a collateral top-up which makes the ICR >= 150% and improves the ICR (and by extension improves the TCR).

But in the source code, the ICR is compared against CCR
```solidity
 881         if (_isRecoveryMode) {
 882             _requireNoStEthBalanceDecrease(_stEthBalanceDecrease);
 883             if (_isDebtIncrease) {
 884                 _requireICRisNotBelowCCR(_vars.newICR);   <<<--------- here
 885                 _requireNoDecreaseOfICR(_vars.newICR, _vars.oldICR);
 886             }
 887
            ...
```

# [L-04] `BorrowerOperations.maxFlashLoan` might be too large for BTC
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/BorrowerOperations.sol#L1124-L1134

Impact:
Quoting from [eip-3156](https://eips.ethereum.org/EIPS/eip-3156):
> The `maxFlashLoan` function MUST return the maximum loan possible for token. If a token is not currently supported maxFlashLoan MUST return 0, instead of reverting.
And quoting from [Overview](https://github.com/code-423n4/2023-10-badger#overview)
> eBTC is a collateralized crypto asset soft pegged to the price of Bitcoin and built on the Ethereum network And the BTC max supply is 21 million coins, which is far less than `type(uint112).max / 1e18`.

So I think maybe it's better to set `maxFlashLoan` to a smaller number

# [L-05] `CdpManagerStorage.getAccumulatedFeeSplitApplied` can reduce the system losses 
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManagerStorage.sol#L641-L644
Impact:
Current's implementation, in extreme unlikely case when `_scaledCdpColl <= _feeSplitDistributed`, the system won't apply split fee, and the CDP can keep all its collateral. I think we can do some change to make the system more robust.
```diff
diff --git a/packages/contracts/contracts/CdpManagerStorage.sol b/packages/contracts/contracts/CdpManagerStorage.sol
index cd11ee4..d7eefac 100644
--- a/packages/contracts/contracts/CdpManagerStorage.sol
+++ b/packages/contracts/contracts/CdpManagerStorage.sol
@@ -640,7 +640,7 @@ contract CdpManagerStorage is EbtcBase, ReentrancyGuard, ICdpManagerData, AuthNo
             );
         } else {
             // extreme unlikely case to skip fee split on this CDP to avoid revert
-            return (0, _cdpCol);
+            return (_scaledCdpColl, 0);
         }
     }
```

# [L-06] i in `HintHelpers.getApproxHint` should start with 0
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L179
Impact:
The [i](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/HintHelpers.sol#L179) in `HintHelpers.getApproxHint` should start with __0__ instead of __1__

# [L-07] `LeverageMacroBase.doOperation` doesn't check flashLoan return value.
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L148
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L155
Impact:
According to [IERC3156FlashLender.sol](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/Interfaces/IERC3156FlashLender.sol#L28-L33), function `flashLoan` contains a return value the caller should check.

# [L-08] some weird ERC20 should approve 0 first in `LeverageMacroBase._doSwap`
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/LeverageMacroBase.sol#L405-L408
Impact:
There are some token should approve 0 first, otherwise the caller function will revert

# [L-09] `PriceFeed.fetchPrice` lacks of check while the system status is `Status.bothOraclesUntrusted`
File:
https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L224-L233
Impact:
While the system is in `Status.bothOraclesUntrusted`, and `fallbackCaller` is set to **address(0)**, the system only checks if chainlink is [broken or forzen](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L226-L232), I think it' better to check [_chainlinkPriceChangeAboveMax](https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/PriceFeed.sol#L445-L463) to make sure chainlink works as expected, because we're current in **bothOraclesUntrusted** status.