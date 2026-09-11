---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Placing a Sell Order

A sell order lets you exit an existing position before settlement. You sell your shares back into the orderbook and receive USDM (on MegaETH markets) or USDC (on Solana markets) in return. Your profit or loss is locked in at the point of sale.

This page describes the orderbook flow at [app.premarket.xyz](https://app.premarket.xyz/). In the covered-options experience, use **Sell** to close a Long call or Short put position you hold and receive its premium in USDG. Use **Burn** to close an LP writer position and unlock its collateral. If you hold equal option and LP amounts for the same contract, you can instead **Unwind** the pair directly back into collateral.

{% hint style="info" %}
In the standard trading flow, you can only sell a position you already hold. Selling closes or reduces an existing position.
{% endhint %}

## How to Place a Sell Order

1. Go to your Portfolio or market where your position exists and find the position you want to exit.
2. Click Sell next to the position.
3. Confirm the transaction.
4. Your shares are sold at the current bid price and you receive the settlement currency in return.
5. Once confirmed onchain, the position disappears from active positions.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption><p>Portfolio position showing the Sell button</p></figcaption></figure>

## Prediction Market Example

```
Buy 20 YES shares at $0.25 for $5
Price moves to $0.30
Click Sell, receive $6
Profit = $1 total, or $0.05 per share
Position closed. Realised P&L is final.
```

## Options Market Example

```
Buy 20 LONG tokens at $0.40 for $8
Price moves to $0.55
Click Sell, receive $11
Profit = $3 total, or $0.15 per token
Position reduced or closed. Realised P&L is final for the amount sold.
```

| Issue                   | Cause                           | Fix                   |
| ----------------------- | ------------------------------- | --------------------- |
| Sell button not visible | No position held in this market | Buy first             |
| Transaction pending     | Onchain confirmation delay      | Wait for confirmation |
| Position still visible  | UI sync delay                   | Refresh the page      |

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>Position history after you sell</p></figcaption></figure>
