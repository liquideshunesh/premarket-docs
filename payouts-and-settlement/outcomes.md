---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Settlement Outcomes

Settlement does not always result in a full win or a full loss. Depending on the market type and how your position resolves, the outcome can be a full payout, a partial payout, zero, or a 50/50 split if the market is cancelled.

## Outcome Types

**Full Win:** you receive the maximum payout. Prediction Markets and Yield Farm pay $1 per winning share. Options, Pre IPO, and Pre TGE markets pay the full amount if the condition is clearly satisfied at expiry.

**Partial Payout:** applies to structured markets such as Options, Pre IPO, and Pre TGE. If the outcome lands within the range but not at the optimal point, the payout is adjusted proportionally.

**Loss:** your position settles to zero value. In Prediction Markets and Yield Farm this means you backed the incorrect outcome. In Options markets this means the asset settled outside your band at expiry.

{% hint style="info" %}
**Cancelled Markets**

If a market is cancelled it settles at 50/50. The collateral pool is split equally between deposit token holders (PRM) and outcome token holders (oPRM). You receive your share based on which tokens you still hold at the time of cancellation. If you sold your outcome tokens before cancellation, you only receive the deposit token portion.
{% endhint %}

### Screenshot

**Screenshot placeholder:** Add a screenshot of a settled position with payout details.

_Caption:_ Position outcome showing whether the trade settled as a win, loss, or partial payout.

## Options Markets in Detail

If you hold both PRM and oPRM tokens before expiry, you can unwind your position and recover your full collateral without waiting for settlement. Otherwise, settlement plays out as follows:

| Scenario                           | PRM Holder                                  | oPRM Holder     |
| ---------------------------------- | ------------------------------------------- | --------------- |
| Expires OTM, oPRM not sold         | Withdraws full collateral                   | oPRM worthless  |
| Expires OTM, oPRM sold for premium | Withdraws full collateral and keeps premium | oPRM worthless  |
| Expires ITM                        | Collateral partially or fully consumed      | Receives payout |

{% hint style="info" %}
Oracle sources for price based markets (Options, Pre TGE, Pre IPO): Bybit, Binance, Hyperliquid, Chainlink.
{% endhint %}

### Screenshot

**Screenshot placeholder:** Add a screenshot of a cancelled market or neutral settlement state.

_Caption:_ Cancelled market state showing how positions are handled when resolution is not possible.

## RWA Markets

RWA markets do not settle. There is no payout structure, no oracle resolution, and no expiry based closure. Your profit or loss is the difference between buy price and sell price, minus fees. The only way to realise value is to sell back into the orderbook.
