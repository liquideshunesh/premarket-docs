---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Exiting a Position

Exiting a position means closing your trade before the market resolves. You sell your shares or position tokens back into the orderbook, locking in your profit or loss without waiting for final settlement.

## When You Can Exit

You can exit any time before market resolution as long as the market is still active and there are buyers available on the other side of the orderbook. The position history tab provides a summary view of positions exited in a single area, as illustrated in the screenshot above.

{% hint style="info" %}
For options spread markets: selling on the orderbook automatically unwinds your position and releases your collateral when matched (merge match). If you hold both sides of a spread, you recover your full collateral directly.
{% endhint %}

For RWA markets, there is no expiry. The only way to exit is to sell back into the orderbook.

## Why Exit Early?

| Reason | When |
| --- | --- |
| Lock in profit | Price has moved in your favour |
| Cut losses | Market has moved against you |
| Reallocate capital | Free up funds for other trades |
| Avoid uncertainty | Exit before a resolution event |

## Example

```
Buy 20 YES shares at $0.25 for $5
Market moves against you
Position value drops to $4.41 (price now about $0.22 per share)
Click Sell, receive $4.41
Realised loss = $0.59 total, or about $0.03 per share
No further exposure to the outcome.
```
