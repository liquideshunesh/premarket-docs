---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Prediction Market Settlement

Prediction markets on Premarket are powered by DFlow, which tokenizes Kalshi markets on Solana. Premarket provides the trading interface, while market rules, resolution, and redemption follow the underlying DFlow/Kalshi market infrastructure.

Prediction markets resolve to a binary outcome. If the market resolves normally, every position settles to either $1 or $0 per share depending on which outcome wins. Settlement is determined by the rules defined for that specific market, not by the last traded price.

The same logic applies to Yield Farm positions. Yield Farm is a curated view over prediction market legs, not a separate product or contract.

## How the Outcome is Determined

Each prediction market has a Rules section that defines exactly what constitutes a valid outcome. When the real world event occurs, the outcome resolves against those rules. Users should always read the Rules section before trading.

## What Happens to Your Position

| Position                | Result                             |
| ----------------------- | ---------------------------------- |
| Holding winning outcome | $1 per share, redeemable via DFlow |
| Holding losing outcome  | Shares expire at $0                |
| Sold before settlement  | P\&L already realised              |

## Example

```
You bought YES on an event resolving in your favour.
You hold 18 shares.

If the event resolves YES:
18 shares x $1 = $18 redeemable to your wallet.

If it does not:
18 shares x $0 = $0.
```

{% hint style="info" %}
If the market resolves normally, settlement and redemption follow the market rules. Solana prediction markets and Yield Farm positions require manual redemption through DFlow.
{% endhint %}
