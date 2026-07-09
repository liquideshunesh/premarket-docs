---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Pre TGE Markets

{% hint style="warning" %}
No Pre TGE markets are currently live. This page describes how Pre TGE markets work for when they are listed.
{% endhint %}

## What are Pre TGE Markets?

Pre TGE markets are a market category for options-style valuation spreads unless the market rules specify different mechanics. They let you trade UP or DOWN exposure on the valuation of a token before it launches.

## What is FDV?

FDV stands for Fully Diluted Valuation. It is calculated as the token price at launch multiplied by the total token supply. This is the number used to determine settlement value when the market rules define FDV as the reference valuation.

```
FDV = Token Price at Launch x Total Token Supply
```

## How Spreads Work

Each market offers a set of valuation spreads. You pick the spread that matches your view on where the token will launch. Your payout depends on where the market-defined valuation lands relative to your spread at settlement.

> **Example:** A pre TGE market on a new token offers spreads of $500M to $1B, $1B to $2B, and $2B to $5B. You believe the token will launch above $1B. You buy UP on the $1B to $2B spread. If it lists at $1.4B, UP receives a partial payout based on how far into the range it lands. If it lists at $2B or above, UP receives the maximum payout. If it lists below $1B, DOWN is the max-winning side.

## Payout Logic

Valuation spreads are directional instruments. UP behaves like exposure to a call spread, DOWN behaves like exposure to a put spread, and the two sides split a combined value of $1 at settlement.

| Final settlement valuation | UP payout          | DOWN payout        |
| -------------------------- | ------------------ | ------------------ |
| Below lower strike         | $0                 | $1                 |
| Inside strike range        | Linear from $0 to $1 | Linear from $1 to $0 |
| Above upper strike         | $1                 | $0                 |

## How to Trade

Select the spread you want to trade and click to open the trade panel. Enter the amount of USDM you want to spend and confirm. Before placing a market order, check the orderbook to confirm there are active orders on both sides. Your position tokens will appear in your portfolio once confirmed onchain.

## Chain and Currency

Pre TGE markets run on MegaETH and settle in USDM according to the market rules.

## Fees

Pre TGE market fees: 0.05% maker, 0.10% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}

Continue to [Options Markets](options-markets.md) or [RWA / Spot Markets](rwa-markets.md) for other market types, or head to [How to Trade a Pre TGE Spread](../walkthroughs/pre-tge-band.md) for a full walkthrough. If you need assistance, check out [Quick Help](../readme/quick-help/) or join the community on [Telegram](https://t.me/premarket_xyz).
