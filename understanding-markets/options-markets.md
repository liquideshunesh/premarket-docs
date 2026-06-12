---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Options Markets

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption><p>Option Market Example</p></figcaption></figure>

Options markets on Premarket let you trade price ranges of an underlying asset over a defined time period. Rather than predicting a single direction, you are trading whether an asset will land within a specific price spread at expiry.

> **Example:** ETH between $2,400 and $2,500 by expiry.

## Live Markets

The following options markets are currently live, all on MegaETH and paired against USDM:

| Market           | Underlying         | Type                 |
| ---------------- | ------------------ | -------------------- |
| BTC/USD Spreads  | Bitcoin            | Call and put spreads |
| ETH/USD Spreads  | Ether              | Call and put spreads |
| MEGA/USD Spreads | MEGA token         | Call and put spreads |
| XAU/USD          | Gold (per ounce)   | Call and put spreads |
| XAG/USD          | Silver (per ounce) | Call and put spreads |
| CL/USD           | Crude oil          | Call and put spreads |

Each market lists weekly expiries with multiple strike spreads on both the call and put side.

## How Options Are Structured

Each option represents a price spread. You are not buying the asset itself. You are buying a conditional payout token that pays out if the asset settles within your chosen range at expiry. Each spread is an independent tradable instrument with its own orderbook and price.

## Minting a Position

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>Mint showing spread selection and collateral input</p></figcaption></figure>

To open a position in an options market you first mint PRM and oPRM tokens. Select the spread you want to trade and click Mint. You deposit USDM as collateral and receive two tokens in return.

| Token | Role                                                                            |
| ----- | ------------------------------------------------------------------------------- |
| PRM   | Write position token. Represents your collateral claim.                         |
| oPRM  | Outcome token. Represents your directional position. Tradable on the orderbook. |

Most users buy oPRM directly from the orderbook without minting. Minting is the path for users who want to write a position (provide the option and collect the premium).

## Trading on the Orderbook

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>Order Book</p></figcaption></figure>

Once minted, you can sell your oPRM tokens on the orderbook via a limit order. Other users can then buy those tokens using USDM. Before placing a market order, check the orderbook to confirm there are active bids at your target price.

**Lifecycle:**

* **Mint:** deposit USDM as collateral. Receive PRM and oPRM tokens.
* **Sell:** list your oPRM tokens on the orderbook at your chosen price.
* **Buy:** purchase oPRM tokens from the orderbook using USDM.
* **Unwind:** return equal amounts of PRM and oPRM to recover your full collateral before expiry. Any profit or loss from trading oPRM along the way is separate.

## Settlement

Positions are auto expired and auto exercised at expiry. You do not need to take any manual action.

{% hint style="success" %}
If your spread is in the money at expiry, the oPRM token holder receives the payout automatically. If it is out of the money, the oPRM expires worthless and the PRM token holder recovers their collateral.
{% endhint %}

## Fees

Options market fees: 0.15% maker, 0.40% taker.
