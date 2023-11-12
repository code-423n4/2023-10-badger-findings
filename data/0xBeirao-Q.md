# [L-01] Bullish scenario makes eBTC less and less accesible

## Impact

The `MIN_NET_STETH_BALANCE` is at 2 stETH, which is a decent amount of money, but still accessible. This value must be enough to incentivize the liquidator to liquidate and not create bad debt. If we consider a bullish scenario on the ETH/USD value. eBTC debt positions will become inaccessible for retail investors. (ex: 1 stETH = 10k$ ⇒ minimum balance is 20k$)

## Recommended Mitigation Steps

Make `MIN_NET_STETH_BALANCE` configurable.