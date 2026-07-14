---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Market Cancellation

In rare cases a market may be cancelled before it can be settled. When this happens, open positions are closed and funds are distributed according to predefined rules.

This does not apply to RWA markets, which have no settlement event.

## When a Market May Be Cancelled

| Reason | Description |
| --- | --- |
| Invalid setup | Market rules set up incorrectly or outcome definition is ambiguous |
| Oracle failure | Data source unavailable or conflicting |
| Underlying event changed | Event cancelled or significantly altered |
| Market integrity | Evidence of manipulation or abnormal behavior |

## What Happens to Your Position

If a market is cancelled it settles at 50/50 or another neutral value defined in the market rules. Funds are split according to the cancellation rules for that product. If you still hold LONG, SHORT, or prediction outcome tokens at the time of cancellation, you receive your share of the cancellation settlement. Open orders are cancelled and the orderbook is cleared.

{% hint style="info" %}
Cancellation is rare but it is a real risk, particularly in Pre TGE, Pre IPO, and Options markets where the underlying event may be delayed, changed, or cancelled entirely.
{% endhint %}
