https://github.com/code-423n4/2023-10-badger/blob/f2f2e2cf9965a1020661d179af46cb49e993cb7e/packages/contracts/contracts/CdpManager.sol#L410C16-L418C1

Lines 410-418 can be written using more concise maths notation, therefore saving more on gas costs.

For example:

{
        totals.debtToRedeem = totals.debtToRedeem + singleRedemption.debtToRedeem;
                totals.collSharesDrawn += singleRedemption.collSharesDrawn;
                totals.remainingDebtToRedeem -= singleRedemption.debtToRedeem;
                totals.CollSharesSurplus += singleRedemption.collSurplus;
    }

