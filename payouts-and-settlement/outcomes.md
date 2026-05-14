---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Settlement Outcomes

Settlement does not always result in a full win or a full loss. Depending on the market type and how your position resolves, the outcome can be a full payout, a partial payout, zero, or a 50/50 split if the market is cancelled.

## Outcome Types

**Full Win:** You receive the maximum payout. Prediction markets pay $1 per winning share. Options and pre-TGE pay the full amount if the condition is clearly satisfied at expiry.

**Partial Payout:** Applies to structured markets such as options and pre-TGE. If the outcome lands within the range but not at the optimal point, the payout is adjusted proportionally.

**Loss:** Your position settles to zero value. In prediction markets this means you backed the incorrect outcome. In options markets this means the asset settled outside your band at expiry.

{% hint style="info" %}
**Cancelled Markets**

If a market is cancelled it settles at 50/50. The collateral pool is split equally between deposit token holders (PRM) and outcome token holders (oPRM). You receive your share based on which tokens you still hold at the time of cancellation. If you sold your outcome tokens before cancellation, you only receive the deposit token portion.
{% endhint %}

## Options Markets in Detail

| Scenario                           | PRM Holder                                | oPRM Holder     |
| ---------------------------------- | ----------------------------------------- | --------------- |
| Expires OTM, oPRM not sold         | Withdraws full collateral                 | oPRM worthless  |
| Expires OTM, oPRM sold for premium | Withdraws full collateral + keeps premium | oPRM worthless  |
| Expires ITM                        | Collateral partially/fully consumed       | Receives payout |

{% hint style="info" %}
If you hold both PRM and oPRM tokens before expiry, you can unwind your position and recover your full collateral without waiting for settlement.
{% endhint %}

Oracle Sources for price based markets: Bybit, Binance, Hyperliquid, Chainlink.
