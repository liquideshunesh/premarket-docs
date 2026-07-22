---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How Valuation Spreads Work

Valuation spreads are the pricing instrument used in Pre TGE and Pre IPO market categories. Instead of a simple yes or no outcome, you trade LONG or SHORT exposure on a defined valuation range and expiry.

For Pre TGE markets, the valuation is the token's fully diluted valuation at TGE. For Pre IPO markets, the valuation is the company's market capitalisation at listing. The exact valuation source and methodology must be defined in the market rules.

## What is the Reference Valuation?

```
FDV = Token Price at Launch x Total Token Supply
```

For Pre IPO markets, substitute the market-defined listing valuation source described in the Rules tab. Do not assume the same source applies to every market.

## What is a Spread?

A spread is a valuation range with a lower strike and an upper strike. Each spread has two sides, LONG and SHORT, with its own orderbook and price.

## LONG and SHORT Directions

| Direction | Meaning |
| --------- | ------- |
| LONG      | Call-spread-like exposure. Payout increases as the final valuation moves higher through the range and reaches max value above the upper strike. |
| SHORT     | Put-spread-like exposure. Payout increases as the final valuation moves lower through the range and reaches max value below the lower strike. |

## Payout Logic

Valuation spreads are directional instruments, not binary markets. At settlement, LONG and SHORT split a combined value of $1.

| Final settlement valuation | LONG payout          | SHORT payout         | User interpretation                  |
| -------------------------- | -------------------- | -------------------- | ------------------------------------ |
| Below lower strike         | $0                   | $1                   | SHORT max win, LONG full loss        |
| Inside strike range        | Linear from $0 to $1 | Linear from $1 to $0 | Payout transitions between the sides |
| Above upper strike         | $1                   | $0                   | LONG max win, SHORT full loss        |

Inside the range, payout is based on where the final valuation lands between the strikes:

```
LONG payout = (Final valuation - Lower strike) / (Upper strike - Lower strike)
SHORT payout = 1 - LONG payout
```

The formula is capped at $0 and $1. Above the upper strike, LONG receives $1. Below the lower strike, SHORT receives $1.

## Example Trade

```
You buy: LONG on a $2B to $3B valuation spread
Price: $0.40 USDM per share
Amount: $10 USDM
Shares received: 25
Final valuation $1.8B: LONG pays $0, SHORT pays $1.
Final valuation $2.1B: LONG pays $0.10, SHORT pays $0.90.
Final valuation $2.6B: LONG pays $0.60, SHORT pays $0.40.
Final valuation $3.2B: LONG pays $1, SHORT pays $0.
```

The most a LONG or SHORT buyer can lose in the standard trading flow is the amount paid for the position.
