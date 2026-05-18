---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Prediction Market Settlement

Prediction markets resolve to a binary outcome. Every position settles to either $1 or $0 per share depending on which outcome wins. Settlement is determined by the rules defined for that specific market, not by the last traded price.

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption><p>Prediction Market outcome</p></figcaption></figure>

## How the Outcome is Determined

Each prediction market has a **Rules** section that defines exactly what constitutes a valid outcome. When the real world event occurs, the outcome is verified against those rules and payouts are distributed automatically to your smart account.

## What Happens to Your Position

| Position                | Result                                 |
| ----------------------- | -------------------------------------- |
| Holding winning outcome | $1 per share credited to smart account |
| Holding losing outcome  | Shares expire at $0                    |
| Sold before settlement  | P\&L already realized                  |

## Example

```
You bought YES on MegaETH launching before end of Q2.
You hold 18 shares.

If MegaETH launches in time:
18 shares x $1 = $18 credited to your account.

If it does not launch in time:
18 shares x $0 = $0.
```

{% hint style="info" %}
Settlement is guaranteed. The worst case is holding to expiry and receiving the binary outcome. Solana prediction markets require manual redemption via the DFlow contract.
{% endhint %}
