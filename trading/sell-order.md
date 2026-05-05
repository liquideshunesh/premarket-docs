---
coverY: 0
---

# Placing a Sell Order

A sell order lets you exit an existing position before settlement. You sell your shares back into the orderbook and receive USDM in return. Your profit or loss is locked in at the point of sale.

> Screenshot: Portfolio showing active position with sell button visible

{% hint style="info" %}
You can only sell a position you already hold. There is no short selling on Premarket. Selling always means closing an existing position.
{% endhint %}

## How to Place a Sell Order

1. Go to your **Portfolio** and find the position you want to exit.
2. Click **Sell** next to the position.
3. Confirm the transaction.
4. Your shares are sold at the current bid price and you receive USDM in return.
5. Once confirmed on-chain, the position disappears from active positions.

## Example

```
Buy YES at $0.25 for $5
Price moves to $0.30
Click Sell, shares sold at $0.30
Profit = $0.05 per share
Position closed. Realized P&L is final.
```

| Issue                   | Cause                           | Fix                   |
| ----------------------- | ------------------------------- | --------------------- |
| Sell button not visible | No position held in this market | Buy first             |
| Transaction pending     | On-chain confirmation delay     | Wait for confirmation |
| Position still visible  | UI sync delay                   | Refresh the page      |
