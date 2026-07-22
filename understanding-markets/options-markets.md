---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Options Markets

Premarket Options Markets let users trade LONG and SHORT tokens on a defined price range and expiry. LONG behaves like exposure to a call spread. SHORT behaves like exposure to a put spread. At settlement, LONG and SHORT split a combined value of $1.

If the final settlement price is above the upper strike, LONG receives $1 and SHORT receives $0. If the final settlement price is below the lower strike, SHORT receives $1 and LONG receives $0. If the final settlement price lands inside the range, both sides receive a partial payout based on where the price lands.

Users do not use margin or leverage in the standard trading flow. The most a user can lose is the amount paid for the position.

> **Example:** ETH has a $2,400 to $2,500 spread. Buy LONG if you want exposure that increases as ETH settles higher through the range and reaches max payout above $2,500. Buy SHORT if you want exposure that increases as ETH settles lower through the range and reaches max payout below $2,400.

## Live Markets

The following options spread markets are live on MegaETH and paired against USDM:

| Market           | Underlying | Sides        |
| ---------------- | ---------- | ------------ |
| BTC/USD Spreads  | Bitcoin    | LONG / SHORT |
| ETH/USD Spreads  | Ether      | LONG / SHORT |
| HYPE/USD Spreads | HYPE       | LONG / SHORT |
| ZEC/USD Spreads  | Zcash      | LONG / SHORT |

Each market lists weekly expiries with multiple strike spreads. You choose a spread and a side.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>Live option market</p></figcaption></figure>

## How LONG/SHORT Payouts Work

Each spread represents a price range with two sides. You are not buying the asset itself. You are taking a position that pays out based on where the final settlement price lands relative to your chosen range at expiry. Each spread is an independent tradable instrument with its own orderbook and price.

| Final settlement price | LONG payout          | SHORT payout         | User interpretation                  |
| ---------------------- | -------------------- | -------------------- | ------------------------------------ |
| Below lower strike     | $0                   | $1                   | SHORT max win, LONG full loss        |
| Inside strike range    | Linear from $0 to $1 | Linear from $1 to $0 | Payout transitions between the sides |
| Above upper strike     | $1                   | $0                   | LONG max win, SHORT full loss        |

Never treat "outside the band" as automatically a loss. Outcome depends on the side: LONG wins above the upper strike, while SHORT wins below the lower strike.

## How to Trade

The default flow is simple: select a spread, pick LONG or SHORT, and place an order on the orderbook. You do not need to mint or unwind anything manually. When your order matches, the platform handles the paired-token mechanics as part of the match.

1. Select the spread you want to trade.
2. Choose LONG or SHORT.
3. Enter your amount and place a market or limit order.
4. Your position appears in Portfolio once the order fills.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Options trade panel</p></figcaption></figure>

## How Matching Works Behind the Scenes

The LONG and SHORT sides share a single orderbook. When orders match, the platform handles the underlying paired-token flow for you:

* **Mint match:** when a LONG buy matches a SHORT buy, collateral from both is combined to mint the position pair, and each side receives the token for the side they bought. You get exposure without a separate mint step.
* **Merge match:** when a LONG sell matches a SHORT sell, the two positions are merged and the released collateral is returned to each side. You exit without a separate unwind step.

You never have to mint or unwind manually. Placing an order on the book does it for you.

## Advanced: Minting LONG/SHORT Pairs

If you want to provide liquidity, you can still mint a position pair directly. Minting deposits USDM as collateral and gives you both sides of the spread, LONG and SHORT, which you can then sell on the orderbook. This advanced path is optional.

| Token | Role |
| ----- | ---- |
| LONG  | Call-spread-like exposure that receives more value as settlement moves higher through the range |
| SHORT | Put-spread-like exposure that receives more value as settlement moves lower through the range  |

## Settlement

Positions are cash-settled at expiry according to the market rules.

{% hint style="success" %}
At settlement, LONG and SHORT always split a combined value of $1. Token price markets use oracle + TWAP rules, and the exact source should be checked in the market rules.
{% endhint %}

## Fees

Options market fees: 0.15% maker, 0.40% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}
