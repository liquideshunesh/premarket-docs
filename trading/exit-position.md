---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Exiting a Position

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption><p>Active position</p></figcaption></figure>

Exiting a position means closing your trade before the market resolves. You sell your shares or position tokens back into the orderbook, locking in your profit or loss without waiting for final settlement.

## When You Can Exit

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>Position History</p></figcaption></figure>

You can exit any time before market resolution as long as the market is still active and there are buyers available on the other side of the orderbook. The position history tab provides a summary view of positions exited in a single area, as illustrated in the screenshot above.

{% hint style="info" %}
For options markets: if you hold equal amounts of PRM and oPRM tokens, you can unwind your position to recover your full collateral directly without needing a buyer.
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
