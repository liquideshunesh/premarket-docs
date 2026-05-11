---
coverY: 0
---

# Pre-TGE Markets

## What are Pre-TGE Markets?

> Screenshot: Active pre-TGE market showing available FDV bands

Pre-TGE markets let you trade on the valuation of a token before it launches. Instead of a binary yes or no outcome, you are taking a position on whether a token's fully diluted valuation will land within a specific range at the time of its token generation event.

## What is FDV?

FDV stands for Fully Diluted Valuation. It is calculated as the token price at launch multiplied by the total token supply. This is the number used to determine which band your position falls into at settlement.

```
FDV = Token Price at Launch x Total Token Supply
```

## How Bands Work

> Screenshot: FDV band selection showing multiple bands with prices

Each market offers a set of valuation bands. You pick the band that matches your view on where the token will launch. Your payout depends on where the FDV lands relative to your band at settlement.

> **Example:** You believe Monad will launch at a $2B to $3B FDV. You buy the bull band. If Monad's FDV at launch is $2.4B, your position pays out partially. If it launches at $4B, above the upper strike, your position pays out at maximum.

## Payout Logic

FDV bands are directional spreads. Payout increases linearly as the FDV moves in your favour, and is capped at the maximum once it crosses the far strike in your direction.

| Scenario                                  | Result                                          |
| ----------------------------------------- | ----------------------------------------------- |
| FDV on wrong side of near strike          | $0. Full loss.                                  |
| FDV within the band                       | Payout increases linearly toward the far strike |
| FDV past the far strike in your direction | Maximum payout, capped at far strike value      |

## How to Trade

> Screenshot: Trade panel for FDV band market

Select the band you want to trade and click to open the trade panel. Enter the amount of USDM you want to spend and confirm. Before placing a market order, check the orderbook to confirm there are active orders on both sides. Your position tokens will appear in your portfolio once confirmed on-chain.

Continue exploring this section to understand how [options markets](options-markets.md) and [spot markets](spot-markets.md) work next, or head to [how to trade a Pre-TGE Band](../walkthroughs/pre-tge-band.md), to trade a Pre-TGE market. If you need assitance, check out [Quick Help](../readme/quick-help/) or join the community on [Telegram](https://t.me/premarket_xyz).
