---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Prediction Markets

## What are Prediction Markets?

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Prediction market example</p></figcaption></figure>

Prediction markets let you trade on the outcome of real world events. Each market poses a question and you take a position on whether it will resolve yes or no. If you back the correct outcome and hold to settlement, each share pays $1. If you are wrong, your shares expire at $0.

Prediction markets run on Solana and settle in USDC. They require identity verification and are restricted in certain jurisdictions.

## How Pricing Works

In prediction markets, the price of a share reflects the market's implied probability of that outcome. A share trading at $0.25 means the market collectively believes there is roughly a 25% chance of YES. At $0.80, it implies 80%. This is a consensus estimate driven by real buy and sell orders, not a guarantee. Prices move as sentiment shifts and new information enters the market.

| Price | Implied Probability |
| --- | --- |
| $0.10 | about 10% chance |
| $0.25 | about 25% chance |
| $0.50 | about 50% chance |
| $0.75 | about 75% chance |
| $0.90 | about 90% chance |

For details on how the orderbook sets prices, spread, and slippage, see [How Pricing Works](../trading/pricing.md) in [Trading Mechanics](../trading/).

## How to Buy

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>Buying Yes or No</p></figcaption></figure>

Before placing a trade, click the Rules tab on the market page. This defines exactly what outcome must occur for YES to resolve at $1. Read it carefully, since the resolution criteria may be stricter or narrower than the market headline suggests.

To open a position, select an outcome and click Buy Yes or Buy No. Enter the amount of USDC you want to spend and confirm the trade. You will receive outcome shares at the current ask price. Check the orderbook before placing a market order to confirm there are active sellers at your target price.

> **Example:** Buy YES at $0.25. If YES resolves correctly, each share pays $1. Your profit is $0.75 per share.

## How to Sell

You can exit your position before settlement by selling your shares back into the orderbook. Navigate to your portfolio, find the position, and click Sell. Your shares are sold at the current bid price and you receive USDC in return. Selling locks in your profit or loss based on the price difference, not the final outcome. Once you sell, you no longer have exposure to how the market resolves.

> **Example:** Buy 20 YES shares at $0.25 for $5. Sell at $0.30 and receive $6. Profit is $1 total, or $0.05 per share, regardless of final outcome.

## Settlement

If you hold your position to expiry, the winning outcome pays $1 per share and the losing outcome pays $0. Prediction markets route through a liquidity partner on Solana, so once your position expires you need to redeem it manually via the DFlow contract. This burns your shares, redeems the USDC, and bridges it back to your wallet.

{% hint style="success" %}
Settlement is always guaranteed at expiry, even if you could not exit early due to low liquidity.
{% endhint %}

## Yield Farm View

If you are looking for high probability legs trading below $1, the [Yield Farm](yield-farm.md) view filters prediction market legs by implied probability and shows the yield to settlement. Same contracts, same chain, same settlement currency.
