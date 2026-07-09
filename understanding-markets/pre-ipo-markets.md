---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Pre IPO Markets

{% hint style="warning" %}
No Pre IPO markets are currently live. This page describes how Pre IPO markets work for when they are listed.
{% endhint %}

## What are Pre IPO Markets?

Pre IPO markets are a market category for options-style valuation spreads unless the market rules specify different mechanics. They let you trade UP or DOWN exposure on the listing valuation of a private company before it goes public.

Pre IPO markets use the same valuation spread mechanic as Pre TGE markets. The only difference is the underlying asset is a company at IPO, not a token at TGE.

## How Spreads Work

Each market offers a set of valuation spreads. You pick the spread that matches your view on where the company will list. Your payout depends on where the market-defined listing valuation lands relative to your spread at settlement.

> **Example:** A pre IPO market on a private company offers spreads of $5B to $10B, $10B to $20B, and $20B to $50B. You believe the company will list above $10B. You buy UP on the $10B to $20B spread. If the company lists at $14B, UP receives a partial payout based on how far into the range it lands. If it lists at $20B or above, UP receives the maximum payout. If it lists below $10B, DOWN is the max-winning side.

## Payout Logic

Pre IPO spreads are directional instruments. UP behaves like exposure to a call spread, DOWN behaves like exposure to a put spread, and the two sides split a combined value of $1 at settlement.

| Final settlement valuation | UP payout          | DOWN payout        |
| -------------------------- | ------------------ | ------------------ |
| Below lower strike         | $0                 | $1                 |
| Inside strike range        | Linear from $0 to $1 | Linear from $1 to $0 |
| Above upper strike         | $1                 | $0                 |

## Settlement

Settlement is triggered by the market-defined listing event. The reference value and settlement methodology for each market are published in the Rules tab on the market page.

## Chain and Currency

Pre IPO markets run on MegaETH and settle in USDM according to the market rules.

## Fees

Pre IPO market fees follow the same schedule as Pre TGE markets: 0.05% maker, 0.10% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}
