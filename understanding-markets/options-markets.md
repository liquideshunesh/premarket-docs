---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Options Markets

Options markets on Premarket let you trade price ranges of an underlying asset over a defined time period. Rather than predicting a single direction, you are trading whether an asset will land within a specific price spread at expiry. Each spread has two sides, Up and Down.

> **Example:** ETH between $2,400 and $2,500 by expiry. Buy Up if you think it settles within or above the range, Down if you think it settles within or below.

## Live Markets

The following options spread markets are live, all on MegaETH and paired against USDM:

| Market           | Underlying | Sides     |
| ---------------- | ---------- | --------- |
| BTC/USD Spreads  | Bitcoin    | Up / Down |
| ETH/USD Spreads  | Ether      | Up / Down |
| HYPE/USD Spreads | HYPE       | Up / Down |
| ZEC/USD Spreads  | Zcash      | Up / Down |

Each market lists weekly expiries with multiple strike spreads. You choose a spread and a side.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>Live option market</p></figcaption></figure>

## How Spread Markets Work

Each spread represents a price range with two sides. You are not buying the asset itself. You are taking a position that pays out based on where the asset settles relative to your chosen range at expiry. Each spread is an independent tradable instrument with its own orderbook and price.

| Side | Meaning                                                   |
| ---- | --------------------------------------------------------- |
| Up   | You profit as the asset settles within or above the range |
| Down | You profit as the asset settles within or below the range |

## How to Trade

The default flow is simple: select a spread, pick Up or Down, and place an order on the orderbook. You do not need to mint or unwind anything manually. When your order matches, the platform mints or unwinds the underlying tokens automatically as part of the match.

1. Select the spread you want to trade.
2. Choose Up or Down.
3. Enter your amount and place a market or limit order.
4. Your position appears in Portfolio once the order fills.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Options trade panel</p></figcaption></figure>

## How Matching Works Behind the Scenes

The Up and Down sides share a single orderbook. When orders match, the platform settles the underlying tokens for you automatically:

* **Mint match:** when an Up buy matches a Down buy, collateral from both is combined to mint the position pair, and each side receives the token for the side they bought. You get exposure without a separate mint step.
* **Merge match:** when an Up sell matches a Down sell, the two positions are merged and the released collateral is returned to each side. You exit without a separate unwind step.

You never have to mint or unwind manually. Placing an order on the book does it for you.

## Advanced: Writing a Position

If you want to provide liquidity and collect premium, you can still mint a position pair directly. Minting deposits USDM as collateral and gives you both sides of the spread, which you can then sell on the orderbook. This is the writer path and is optional.

| Token | Role                                                                         |
| ----- | ---------------------------------------------------------------------------- |
| PRM   | The Down side. Represents the write position and collateral claim.           |
| oPRM  | The Up side. Represents the directional position. Tradable on the orderbook. |

## Settlement

Positions are auto expired and auto exercised at expiry. You do not need to take any manual action.

{% hint style="success" %}
If your spread is in the money at expiry, the Up holder receives the payout automatically. If it is out of the money, the Down (write) holder recovers their collateral.
{% endhint %}

## Fees

Options market fees: 0.15% maker, 0.40% taker.

{% hint style="info" %}
**Fees are 0% at launch.** Trading fees are waived across all markets for the launch period. The schedule above is the standard rate that applies once fees are switched on.
{% endhint %}
