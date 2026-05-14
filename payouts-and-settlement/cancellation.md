---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Market Cancellation

In rare cases a market may be cancelled before it can be settled. When this happens, open positions are closed and funds are distributed according to predefined rules.

## When a Market May Be Cancelled

| Reason                   | Description                                                        |
| ------------------------ | ------------------------------------------------------------------ |
| Invalid setup            | Market rules set up incorrectly or outcome definition is ambiguous |
| Oracle failure           | Data source unavailable or conflicting                             |
| Underlying event changed | Event cancelled or significantly altered                           |
| Market integrity         | Evidence of manipulation or abnormal behavior                      |

## What Happens to Your Position

If a market is cancelled it settles at 50/50. Funds are split equally between deposit token holders and outcome token holders. If you still hold your options, oPRM, or outcome tokens at the time of cancellation, you receive your full share of the split. Open orders are cancelled and the orderbook is cleared.

{% hint style="info" %}
Cancellation is rare but it is a real risk, particularly in pre-TGE and options markets where the underlying event may be delayed, changed, or cancelled entirely.
{% endhint %}
