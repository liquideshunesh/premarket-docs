---
cover: ../../../.gitbook/assets/Default.png
coverY: 0
---

# Trading FAQ

These answers describe the orderbook at [app.premarket.xyz](https://app.premarket.xyz/) unless covered options are mentioned explicitly.

<details>

<summary><strong>Why can I not place a trade?</strong></summary>

The most common reason is an empty orderbook. If there are no matching orders on the other side, your market order will not execute. Try placing a limit order at your target price and waiting for a counterparty.

</details>

<details>

<summary><strong>Why is my execution price different from what I saw?</strong></summary>

Your order matched the best available liquidity at the time of execution, which may have changed since you saw the displayed price. This is called slippage and is more common in thinner markets.

</details>

<details>

<summary><strong>Why did the price move after I traded?</strong></summary>

Your trade consumed liquidity from the orderbook and changed the available orders. Larger trades have more price impact than smaller ones.

</details>

<details>

<summary><strong>Can I cancel an order?</strong></summary>

For orderbook markets at [app.premarket.xyz](https://app.premarket.xyz/), you can cancel an open order directly from the UI or through the smart contracts if you prefer to interact onchain. Covered-option orders are signed offchain and remain open until they fill, reach their selected order expiry, or you cancel them. Cancellation is free and immediate.

</details>

<details>

<summary><strong>What is the difference between a market order and a limit order?</strong></summary>

A market order executes immediately against the best available orders in the book. A limit order only executes at your specified price and is not guaranteed to fill.

</details>

<details>

<summary><strong>What are maker and taker fees?</strong></summary>

Each market has a maker fee paid by the order placer and a taker fee paid by the order matcher. Fee rates vary by market type.

| Market Type                     | Maker           | Taker           |
| ------------------------------- | --------------- | --------------- |
| Pre TGE / Pre IPO               | 0.05%           | 0.10%           |
| MegaETH Options Spreads        | 0.15%           | 0.40%           |
| RWA                             | 0.20%           | 0.30%           |
| Prediction Markets / Yield Farm | To be confirmed | To be confirmed |

**Fees in the table are 0% at launch** in the main app. The rates above are the standard schedule that applies once fees are switched on.

The table does not define a fee rate for covered options on Robinhood Chain.

</details>

<details>

<summary><strong>Can I sell short or borrow against a market?</strong></summary>

No. In the standard trading flow, you can only sell positions you already hold. Selling closes or reduces an existing position.

Some options-style markets have a SHORT side. Buying SHORT is a directional position in that spread; it is not the same as borrowing an asset or opening a naked short sale.

For Robinhood Chain covered options, **Short** is the user-facing name of the put option leg. The writer side is labelled **LP** for both calls and puts. LP positions are fully collateralized; transferring LP transfers its settlement exposure and rights to the remaining collateral.

</details>

<details>

<summary><strong>What happens if there is no liquidity when I want to exit?</strong></summary>

You will not be able to sell your position before expiry. For markets with settlement, hold to expiry and your position resolves according to the market rules if the market resolves normally. For RWA markets there is no expiry-based settlement, so the only exit is to wait for a buyer. For covered options, you can also unwind equal option and LP amounts for the same contract back into collateral without selling either leg separately.

</details>

<details>

<summary><strong>Why was my covered-option order signed but not filled?</strong></summary>

Check the one-time vault operator approval. Without it, an order can be signed but cannot fill. Also confirm that the order has matching liquidity and was created for the current exchange version. After an exchange upgrade, cancel any stale order and create it again.

</details>
