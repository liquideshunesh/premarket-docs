---
cover: ../.gitbook/assets/Payouts and Settlements.png
coverY: -102.81055543382998
---

# Payouts and Settlement

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>Settled market in portfolio history</p></figcaption></figure>

Most markets on Premarket eventually reach a point where trading ends, outcomes are determined, and positions are finalised. This is settlement. Your actual financial result is locked in here if you have not already exited your position early.

RWA markets are the exception. They are perpetual with no expiry and no settlement event. Your only exit is to sell back into the orderbook.

## Two Ways to Realise Value

**Exit Early (Trading):** sell your position into the orderbook before expiry. Profit or loss is based on sell price minus buy price. Requires a counterparty to execute.

**Hold to Settlement:** your position resolves based on the final outcome. Payout depends on the market type. No counterparty needed. Guaranteed at expiry. Not applicable to RWA markets.

## Settlement by Market Type

| Market Type | Settlement Trigger | Payout |
| --- | --- | --- |
| Prediction Markets | Event outcome confirmed | $1 winning, $0 losing per share |
| Yield Farm | Underlying prediction market resolves | $1 if leg resolves correctly, $0 if not |
| Pre IPO Markets | Company lists | Based on market capitalisation vs band |
| Pre TGE Markets | Token launch | Based on FDV vs band |
| Options Markets | Expiry time reached | Based on underlying price vs band |
| RWA Markets | None (perpetual) | Realised only on sell |

{% hint style="success" %}
Pre IPO, Pre TGE, Options, and RWA markets on MegaETH are auto redeemed at settlement. Proceeds are sent directly to your smart account and no manual action is needed.
{% endhint %}

{% hint style="info" %}
Prediction Markets and Yield Farm route through a liquidity partner on Solana and require manual redemption. Once your position expires, you interact with the DFlow contract to burn your shares and bridge your USDC back to your wallet.
{% endhint %}
