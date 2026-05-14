---
cover: ../.gitbook/assets/cover-main (4).png
coverY: 118.48887711864407
---

# Payouts and Settlement

Every market on Premarket eventually reaches a point where trading ends, outcomes are determined, and positions are finalized. This is settlement. Your actual financial result is locked in here if you have not already exited your position early.

> Screenshot: Settled market in portfolio history

## Two Ways to Realize Value

**Exit Early (Trading):** Sell your position into the orderbook before expiry. Profit or loss is based on sell price minus buy price. Requires a counterparty to execute.

**Hold to Settlement:** Your position resolves based on the final outcome. Payout depends on the market type. No counterparty needed. Guaranteed at expiry.

## Settlement by Market Type

| Market Type        | Settlement Trigger      | Payout                            |
| ------------------ | ----------------------- | --------------------------------- |
| Prediction Markets | Event outcome confirmed | $1 winning / $0 losing per share  |
| Pre-TGE Markets    | Token launch            | Based on FDV band result          |
| Options Markets    | Expiry time reached     | Based on underlying price vs band |

{% hint style="success" %}
All positions on Premarket are auto-redeemed at settlement. Proceeds are sent directly to your smart account. No manual action is needed.
{% endhint %}

{% hint style="info" %}
Note: Only Solana prediction markets require manual redemption. You will need to interact with the DFlow contract to burn your shares and bridge your USDC back.
{% endhint %}
