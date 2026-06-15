---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Pre IPO Markets

{% hint style="warning" %}
No Pre IPO markets are currently live. This page describes how Pre IPO markets work for when they are listed.
{% endhint %}

## What are Pre IPO Markets?

Pre IPO markets let you trade on the listing valuation of a private company before it goes public. Instead of waiting for the IPO to price and shares to start trading, you take a position now on where the company's market capitalisation will land at the moment of listing.

Pre IPO markets use the same valuation spread mechanic as Pre TGE markets. The only difference is the underlying asset is a company at IPO, not a token at TGE.

## How Spreads Work

Each market offers a set of valuation spreads. You pick the spread that matches your view on where the company will list. Your payout depends on where the listing market capitalisation lands relative to your spread at settlement.

> **Example:** A pre IPO market on a private company offers spreads of $5B to $10B, $10B to $20B, and $20B to $50B. You believe the company will list above $10B. You buy the $10B to $20B spread. If the company lists at $14B, your payout is proportional to how far into the range it lands. If it lists at $20B or above, you receive the maximum payout. If it lists below $10B, you receive nothing.

## Payout Logic

Pre IPO spreads are directional instruments. Payout increases linearly as the listing market capitalisation moves in your favour within the range, and is capped at the maximum once it crosses the far strike in your direction.

| Scenario                                            | Result                                          |
| --------------------------------------------------- | ----------------------------------------------- |
| Listing value on wrong side of near strike          | $0. Full loss.                                  |
| Listing value within the spread                     | Payout increases linearly toward the far strike |
| Listing value past the far strike in your direction | Maximum payout, capped at far strike value      |

## Settlement

Settlement is triggered by the listing event. The reference value is the company's market capitalisation at the moment shares begin trading on a recognised exchange. The settlement methodology for each market is published in the Rules tab on the market page.

## Chain and Currency

Pre IPO markets run on MegaETH and settle in USDM. Positions settle automatically to your smart account at expiry. No manual redemption is required.

## Fees

Pre IPO market fees follow the same schedule as Pre TGE markets: 0.05% maker, 0.10% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}
