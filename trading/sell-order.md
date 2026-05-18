---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Placing a Sell Order

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>Selling position</p></figcaption></figure>

A sell order lets you exit an existing position before settlement. You sell your shares back into the orderbook and receive USDM in return. Your profit or loss is locked in at the point of sale.

{% hint style="info" %}
You can only sell a position you already hold. There is no short selling on Premarket. Selling always means closing an existing position.
{% endhint %}

## How to Place a Sell Order

1. Go to your **Portfolio** and find the position you want to exit.
2. Click **Sell** next to the position.
3. Confirm the transaction.
4. Your shares are sold at the current bid price and you receive USDM in return.
5. Once confirmed onchain, the position disappears from active positions.

## Example

```
Buy 20 YES shares at $0.25 for $5
Price moves to $0.30
Click Sell, receive $6
Profit = $1 total, or $0.05 per share
Position closed. Realized P&L is final.
```

<table><thead><tr><th width="197.09375">Issue</th><th>Cause</th><th>Fix</th></tr></thead><tbody><tr><td>Sell button not visible</td><td>No position held in this market</td><td>Buy first</td></tr><tr><td>Transaction pending</td><td>On-chain confirmation delay</td><td>Wait for confirmation</td></tr><tr><td>Position still visible</td><td>UI sync delay</td><td>Refresh the page</td></tr></tbody></table>
