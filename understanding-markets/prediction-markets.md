---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Prediction Markets

## What are Prediction Markets?

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Prediction market example</p></figcaption></figure>

Prediction markets let you trade on the outcome of real world events. Each market poses a question and you take a position on whether it will resolve yes or no. If you back the correct outcome and hold to settlement, each share pays $1. If you are wrong, your shares expire at $0.

## How Pricing Works

Prices in prediction markets reflect implied probability. A share trading at $0.25 means the market collectively believes there is roughly a 25% chance of that outcome occurring. This is not a guarantee, it is a consensus estimate based on real buy and sell orders. Prices move as sentiment shifts and new information enters the market.

| Price | Implied Probability |
| ----- | ------------------- |
| $0.10 | \~10% chance        |
| $0.25 | \~25% chance        |
| $0.50 | \~50% chance        |
| $0.75 | \~75% chance        |
| $0.90 | \~90% chance        |

## How to Buy

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>Buying 'Yes' or 'No'</p></figcaption></figure>

To open a position, select an outcome and click "Buy Yes" or "Buy No". Enter the amount of USDM you want to spend and confirm the trade. You will receive outcome shares at the current ask price. Check the orderbook before placing a market order to confirm there are active sellers at your target price.

* You pay USDM and receive outcome shares.

> **Example:** Buy YES at $0.25. If YES resolves correctly, each share pays $1. Your profit is $0.75 per share.

## How to Sell

You can exit your position before settlement by selling your shares back into the orderbook. Navigate to your portfolio, find the position, and click **Sell**. Your shares are sold at the current bid price and you receive USDM in return.

> **Example**: Buy 20 YES shares at $0.25 for $5. Sell at $0.30 and receive $6. Profit is $1 total, or $0.05 per share, regardless of final outcome.

## Settlement

> Screenshot: Settled position in portfolio history

If you hold your position to expiry, the winning outcome pays $1 per share and the losing outcome pays $0. Prediction markets currently route through a liquidity partner on Solana, so once your position expires you need to redeem it manually via the DFlow contract. This burns your shares, redeems the USDC, and bridges it back to your wallet.

Settlement is always guaranteed at expiry, even if you could not exit early due to low liquidity.and the losing outcome pays $0. You do not need to take any action.

{% hint style="success" %}
Settlement is always guaranteed at expiry, even if you could not exit early due to low liquidity.
{% endhint %}
