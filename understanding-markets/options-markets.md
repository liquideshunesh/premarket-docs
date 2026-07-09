---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Options Markets

Premarket Options Markets let users trade UP and DOWN tokens on a defined price range and expiry. UP behaves like exposure to a call spread. DOWN behaves like exposure to a put spread. At settlement, UP and DOWN split a combined value of $1.

If the final settlement price is above the upper strike, UP receives $1 and DOWN receives $0. If the final settlement price is below the lower strike, DOWN receives $1 and UP receives $0. If the final settlement price lands inside the range, both sides receive a partial payout based on where the price lands.

Users do not use margin or leverage in the standard trading flow. The most a user can lose is the amount paid for the position.

> **Example:** ETH has a $2,400 to $2,500 spread. Buy UP if you want exposure that increases as ETH settles higher through the range and reaches max payout above $2,500. Buy DOWN if you want exposure that increases as ETH settles lower through the range and reaches max payout below $2,400.

## Live Markets

The following options spread markets are live on MegaETH and paired against USDM:

| Market           | Underlying | Sides     |
| ---------------- | ---------- | --------- |
| BTC/USD Spreads  | Bitcoin    | UP / DOWN |
| ETH/USD Spreads  | Ether      | UP / DOWN |
| HYPE/USD Spreads | HYPE       | UP / DOWN |
| ZEC/USD Spreads  | Zcash      | UP / DOWN |

Each market lists weekly expiries with multiple strike spreads. You choose a spread and a side.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>Live option market</p></figcaption></figure>

## How UP/DOWN Payouts Work

Each spread represents a price range with two sides. You are not buying the asset itself. You are taking a position that pays out based on where the final settlement price lands relative to your chosen range at expiry. Each spread is an independent tradable instrument with its own orderbook and price.

| Final settlement price | UP payout          | DOWN payout        | User interpretation                  |
| ---------------------- | ------------------ | ------------------ | ------------------------------------ |
| Below lower strike     | $0                 | $1                 | DOWN max win, UP full loss           |
| Inside strike range    | Linear from $0 to $1 | Linear from $1 to $0 | Payout transitions between the sides |
| Above upper strike     | $1                 | $0                 | UP max win, DOWN full loss           |

Never treat "outside the band" as automatically a loss. Outcome depends on the side: UP wins above the upper strike, while DOWN wins below the lower strike.

## How to Trade

The default flow is simple: select a spread, pick UP or DOWN, and place an order on the orderbook. You do not need to mint or unwind anything manually. When your order matches, the platform handles the paired-token mechanics as part of the match.

1. Select the spread you want to trade.
2. Choose UP or DOWN.
3. Enter your amount and place a market or limit order.
4. Your position appears in Portfolio once the order fills.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Options trade panel</p></figcaption></figure>

## How Matching Works Behind the Scenes

The UP and DOWN sides share a single orderbook. When orders match, the platform handles the underlying paired-token flow for you:

* **Mint match:** when an UP buy matches a DOWN buy, collateral from both is combined to mint the position pair, and each side receives the token for the side they bought. You get exposure without a separate mint step.
* **Merge match:** when an UP sell matches a DOWN sell, the two positions are merged and the released collateral is returned to each side. You exit without a separate unwind step.

You never have to mint or unwind manually. Placing an order on the book does it for you.

## Advanced: Minting UP/DOWN Pairs

If you want to provide liquidity, you can still mint a position pair directly. Minting deposits USDM as collateral and gives you both sides of the spread, UP and DOWN, which you can then sell on the orderbook. This advanced path is optional.

| Token | Role |
| ----- | ---- |
| UP    | Call-spread-like exposure that receives more value as settlement moves higher through the range |
| DOWN  | Put-spread-like exposure that receives more value as settlement moves lower through the range |

## Settlement

Positions are cash-settled at expiry according to the market rules.

{% hint style="success" %}
At settlement, UP and DOWN always split a combined value of $1. Token price markets use oracle + TWAP rules, and the exact source should be checked in the market rules.
{% endhint %}

## Fees

Options market fees: 0.15% maker, 0.40% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}
