---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# RWA Markets

Real World Asset markets let you trade tokenised real world items directly against USDM. Unlike prediction markets, there are no outcomes, probabilities, or settlement events. You are buying and selling assets at market prices on a perpetual orderbook.

## Live Markets

The following RWA markets are currently live, all on MegaETH and paired against USDM:

| Market                 | Asset                            |
| ---------------------- | -------------------------------- |
| Fullerene C60 99.5% 1g | 1 gram of 99.5% purity Carbon 60 |
| Fullerene C60 99.9% 1g | 1 gram of 99.9% purity Carbon 60 |
| Fullerene C70 98% 1g   | 1 gram of 98% purity Carbon 70   |
| Fullerene C70 99.9% 1g | 1 gram of 99.9% purity Carbon 70 |

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption><p>RWA market</p></figcaption></figure>

## Key Characteristics

1. **No expiry:** markets are perpetual.
2. **No resolution:** positions do not settle to $0 or $1.
3. **Real assets:** you hold tokens representing the underlying asset.
4. **Orderbook driven:** trades only happen if counterparties exist.

## How Trading Works

1. **Buying:** you spend USDM, receive the asset token, and match with someone selling.
2. **Selling:** you give the asset token, receive USDM, and match with someone buying.

Trades only execute if there is liquidity. "No price available for market order" is a liquidity issue, not a balance issue.

## Maker vs Taker

* Maker: places order first. Provides liquidity.
* Taker: matches existing order. Removes liquidity.

> **Example:** Buy 1g Fullerene C70 99.9% at 500 USDM. Hold the position. No expiry, no settlement event. Price moves to 550 USDM. Sell at 550 USDM, receive 550 USDM. Profit is 50 USDM.

You can hold the asset indefinitely. Profit or loss is realised only when you sell.

## Settlement

RWA markets have no expiry and no settlement event. Your position stays open until you sell it back into the orderbook. There is no automatic payout, no oracle resolution, and no expiry based closure. The only way to close an RWA position is to place a sell order and match with a buyer.

### What this means in practice

No time pressure. Your position does not expire, so you can hold as long as you want.

Exit depends on liquidity. You can only sell if there is a buyer on the orderbook. If liquidity is thin, you may not be able to exit at your target price. There is no payout structure. Your profit or loss is the difference between buy price and sell price, minus any fees.

## Fees

RWA market fees: 0.20% maker, 0.30% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}
