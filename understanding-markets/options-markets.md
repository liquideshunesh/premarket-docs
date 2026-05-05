---
coverY: 0
---

# Options Markets

## What are Options Markets?

> Screenshot: Active options market showing available bands

Options markets on Premarket let you trade price ranges of an underlying asset over a defined time period. Rather than predicting a single direction, you are trading whether an asset will land within a specific price band at expiry.

> **Example:** ETH between $2,400 and $2,600 by expiry.

## How Options Are Structured

Each option represents a price band. You are not buying the asset itself. You are buying a conditional payout token that pays out if the asset settles within your chosen range at expiry. Each band is an independent tradable instrument with its own orderbook and price.

## Minting a Position

> Screenshot: Mint screen showing band selection and collateral input

To open a position in an options market you first mint PRM and oPRM tokens. Select the band you want to trade and click **Mint**. You deposit USDM as collateral and receive two tokens in return.

| Token | Role                                                                            |
| ----- | ------------------------------------------------------------------------------- |
| PRM   | Write position token. Represents your collateral claim.                         |
| oPRM  | Outcome token. Represents your directional position. Tradable on the orderbook. |

## Trading on the Orderbook

> Screenshot: Orderbook showing oPRM bids and asks

Once minted, you can sell your oPRM tokens on the orderbook via a limit order. Other users can then buy those tokens using USDM. Before placing a market order, check the orderbook to confirm there are active bids at your target price.

**Lifecycle:**

* **Mint:** Deposit USDM as collateral. Receive PRM and oPRM tokens.
* **Sell:** List your oPRM tokens on the orderbook at your chosen price.
* **Buy:** Purchase oPRM tokens from the orderbook using USDM.
* **Unwind:** Return equal amounts of PRM and oPRM to recover your full collateral before expiry.

## Settlement

Positions are auto-expired and auto-exercised at expiry. You do not need to take any manual action.

{% hint style="success" %}
If your band is in the money at expiry, the oPRM token holder receives the payout automatically. If it is out of the money, the oPRM expires worthless and the PRM token holder recovers their collateral.
{% endhint %}

Head to How Pricing Works for a detailed breakdown of how prices are set across all market types on Premarket.
