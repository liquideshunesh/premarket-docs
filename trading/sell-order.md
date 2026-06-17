---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Placing a Sell Order

A sell order lets you exit an existing position before settlement. You sell your shares back into the orderbook and receive USDM (on MegaETH markets) or USDC (on Solana markets) in return. Your profit or loss is locked in at the point of sale.

{% hint style="info" %}
You can only sell a position you already hold. There is no short selling on Premarket. Selling always means closing an existing position.
{% endhint %}

## How to Place a Sell Order

1. Go to your Portfolio or market where your position exists and find the position you want to exit.
2. Click Sell next to the position.
3. Confirm the transaction.
4. Your shares are sold at the current bid price and you receive the settlement currency in return.
5. Once confirmed onchain, the position disappears from active positions.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption><p>Portfolio position showing the Sell button</p></figcaption></figure>

## Example

```
Buy 20 YES shares at $0.25 for $5
Price moves to $0.30
Click Sell, receive $6
Profit = $1 total, or $0.05 per share
Position closed. Realised P&L is final.
```

| Issue                   | Cause                           | Fix                   |
| ----------------------- | ------------------------------- | --------------------- |
| Sell button not visible | No position held in this market | Buy first             |
| Transaction pending     | Onchain confirmation delay      | Wait for confirmation |
| Position still visible  | UI sync delay                   | Refresh the page      |

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>Position history after you sell</p></figcaption></figure>
