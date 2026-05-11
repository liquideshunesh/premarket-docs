---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Market Cancellation

In rare cases a market may be cancelled before it can be settled. When this happens, open positions are closed and funds are returned according to predefined rules.

## When a Market May Be Cancelled

| Reason                   | Description                                                        |
| ------------------------ | ------------------------------------------------------------------ |
| Invalid setup            | Market rules set up incorrectly or outcome definition is ambiguous |
| Oracle failure           | Data source unavailable or conflicting                             |
| Underlying event changed | Event cancelled or significantly altered                           |
| Market integrity         | Evidence of manipulation or abnormal behavior                      |

## What Happens to Your Position

If a market is cancelled your position does not settle to a win or loss. Funds are typically refunded or settled at a neutral value. Open orders are cancelled and the orderbook is cleared.

{% hint style="info" %}
Cancellation is rare but it is a real risk, particularly in pre-TGE and options markets where the underlying event may be delayed, changed, or cancelled entirely.
{% endhint %}
