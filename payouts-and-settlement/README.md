---
cover: ../.gitbook/assets/Payouts and Settlements.png
coverY: 0
---

# Payouts and Settlement

Most markets on Premarket eventually reach a point where trading ends, outcomes are determined, and positions are finalised. This is settlement. Your actual financial result is locked in here if you have not already exited your position early.

RWA markets are the exception. They are perpetual with no expiry and no settlement event. Your only exit is to sell back into the orderbook.

## Two Ways to Realise Value

**Exit Early (Trading):** sell your position into the orderbook before expiry. Profit or loss is based on sell price minus buy price. Requires a counterparty to execute.

**Hold to Settlement:** your position resolves based on the final outcome if the market resolves normally. Payout depends on the product and market rules. Not applicable to RWA markets.

## Settlement by Market Type

| Market Type        | Settlement Trigger                    | Payout                                  |
| ------------------ | ------------------------------------- | --------------------------------------- |
| Prediction Markets | Event outcome confirmed               | $1 winning, $0 losing per share         |
| Yield Farm         | Underlying prediction market resolves | $1 if leg resolves correctly, $0 if not |
| Pre IPO Markets    | Market-defined listing event          | LONG/SHORT valuation spread payout         |
| Pre TGE Markets    | Market-defined token launch event     | LONG/SHORT valuation spread payout         |
| Options Markets    | Expiry time reached                   | LONG/SHORT price spread payout             |
| RWA / Spot Markets | None (perpetual)                      | Realised only on sell                   |

{% hint style="success" %}
Options-style MegaETH markets are cash-settled at expiry according to the market rules. LONG and SHORT split a combined value of $1.
{% endhint %}

{% hint style="info" %}
Prediction Markets and Yield Farm route through DFlow on Solana and require manual redemption. Once your position expires and resolves normally, redeem through DFlow.
{% endhint %}
