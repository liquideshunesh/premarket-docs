---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Prediction Market Settlement

Prediction markets resolve to a binary outcome. Every position settles to either $1 or $0 per share depending on which outcome wins. Settlement is determined by the rules defined for that specific market, not by the last traded price.

The same logic applies to Yield Farm positions. Yield Farm uses the same prediction market contracts. The only difference is how the leg was sourced.

## How the Outcome is Determined

Each prediction market has a Rules section that defines exactly what constitutes a valid outcome. When the real world event occurs, the outcome is verified against those rules and payouts are distributed to your position.

## What Happens to Your Position

| Position                | Result                             |
| ----------------------- | ---------------------------------- |
| Holding winning outcome | $1 per share, redeemable via DFlow |
| Holding losing outcome  | Shares expire at $0                |
| Sold before settlement  | P\&L already realised              |

### Screenshot

**Screenshot placeholder:** Add a screenshot of a resolved Prediction Market or Yield Farm position.

_Caption:_ Binary settlement example showing the winning side and redeemable value.

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
Settlement is guaranteed. The worst case is holding to expiry and receiving the binary outcome. Solana prediction markets and Yield Farm positions require manual redemption via the DFlow contract.
{% endhint %}

### Screenshot

**Screenshot placeholder:** Add a screenshot of the manual redemption action through the position UI.

_Caption:_ Redemption flow showing how users claim USDC after a Solana market settles.
