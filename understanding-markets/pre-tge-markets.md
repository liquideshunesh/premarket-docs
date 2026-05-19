---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Pre TGE Markets

{% hint style="warning" %}
No Pre TGE markets are currently live. This page describes how Pre TGE markets work for when they are listed.
{% endhint %}

## What are Pre TGE Markets?

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>Pre TGE Market Example</p></figcaption></figure>

Pre TGE markets let you trade on the valuation of a token before it launches. Instead of a binary yes or no outcome, you are taking a position on whether a token's fully diluted valuation will land within a specific range at the time of its token generation event.

## What is FDV?

FDV stands for Fully Diluted Valuation. It is calculated as the token price at launch multiplied by the total token supply. This is the number used to determine which band your position falls into at settlement.

```
FDV = Token Price at Launch x Total Token Supply
```

## How Bands Work

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption><p>FDV Bands</p></figcaption></figure>

Each market offers a set of valuation bands. You pick the band that matches your view on where the token will launch. Your payout depends on where the FDV lands relative to your band at settlement.

> **Example:** A pre TGE market on a new token offers bands of $500M to $1B, $1B to $2B, and $2B to $5B. You believe the token will launch above $1B. You buy the $1B to $2B band. If it lists at $1.4B, your payout is proportional to how far into the range it lands. If it lists at $2B or above, you receive the maximum payout. If it lists below $1B, you receive nothing.

## Payout Logic

FDV bands are directional spreads. Payout increases linearly as the FDV moves in your favour, and is capped at the maximum once it crosses the far strike in your direction.

| Scenario | Result |
| --- | --- |
| FDV on wrong side of near strike | $0. Full loss. |
| FDV within the band | Payout increases linearly toward the far strike |
| FDV past the far strike in your direction | Maximum payout, capped at far strike value |

## How to Trade

<figure><img src="../.gitbook/assets/image (25).png" alt="" width="375"><figcaption><p>FDV band market buy</p></figcaption></figure>

Select the band you want to trade and click to open the trade panel. Enter the amount of USDM you want to spend and confirm. Before placing a market order, check the orderbook to confirm there are active orders on both sides. Your position tokens will appear in your portfolio once confirmed onchain.

## Chain and Currency

Pre TGE markets run on MegaETH and settle in USDM. Positions settle automatically to your smart account at expiry. No manual redemption is required.

## Fees

Pre TGE market fees: 0.05% maker, 0.10% taker.

Continue to [Options Markets](options-markets.md) or [RWA Markets](rwa-markets.md) for other market types, or head to [How to Trade a Pre TGE Band](../walkthroughs/pre-tge-band.md) for a full walkthrough. If you need assistance, check out [Quick Help](../readme/quick-help/) or join the community on [Telegram](https://t.me/premarket_xyz).
