---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Settlement Outcomes

Settlement does not always result in a full win or a full loss. Depending on the product and how your position resolves, the outcome can be a full payout, a partial payout, zero, or a neutral cancellation result.

## Prediction Markets

Prediction Markets are binary YES/NO markets powered by DFlow, which tokenizes Kalshi markets on Solana. If the market resolves normally, winning shares are redeemable for $1 and losing shares expire at $0. Redemption is manual through DFlow.

Yield Farm uses the same prediction-market settlement logic because it is a filtered view over prediction market legs, not a separate product.

| Position                | Result                             |
| ----------------------- | ---------------------------------- |
| Holding winning outcome | $1 per share, redeemable via DFlow |
| Holding losing outcome  | Shares expire at $0                |
| Sold before settlement  | P&L already realised               |

## Options Markets

Options Markets use LONG and SHORT spread tokens. LONG behaves like exposure to a call spread. SHORT behaves like exposure to a put spread. At settlement, LONG and SHORT split a combined value of $1.

| Final settlement price | LONG payout          | SHORT payout        | User interpretation                  |
| ---------------------- | ------------------ | ------------------ | ------------------------------------ |
| Below lower strike     | $0                 | $1                 | SHORT max win, LONG full loss           |
| Inside strike range    | Linear from $0 to $1 | Linear from $1 to $0 | Payout transitions between the sides |
| Above upper strike     | $1                 | $0                 | LONG max win, SHORT full loss           |

Do not treat "outside the band" as automatically a loss. Above the upper strike is a max win for LONG. Below the lower strike is a max win for SHORT.

## Pre TGE and Pre IPO Categories

Pre TGE and Pre IPO markets are market categories or underlyings for options-style valuation spreads unless the market rules specify different mechanics. They use the same LONG/SHORT settlement model when listed as valuation spreads.

The final valuation source is market-defined. Always read the Rules tab before trading.

## RWA / Spot Markets

RWA/Spot Markets do not use an expiry, LONG/SHORT payout curve, or settlement formula. Users deposit supported assets into the smart account, trade against the orderbook, and realise gains or losses based on the price at which they buy and sell.

## Cancellation

If a market cannot resolve normally, it may be cancelled according to the market rules. In that case, positions are handled using the cancellation rules for that product. See [Market Cancellation](cancellation.md) for details.
