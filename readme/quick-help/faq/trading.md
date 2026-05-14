---
cover: ../../../.gitbook/assets/banner-generic.png
coverY: 0
---

# Trading FAQ

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

Yes. You can cancel an open order directly from the UI or through the smart contracts if you prefer to interact on-chain.

</details>

<details>

<summary><strong>What is the difference between a market order and a limit order?</strong></summary>

A market order executes immediately against the best available orders in the book. A limit order only executes at your specified price and is not guaranteed to fill.

</details>

<details>

<summary><strong>What are maker and taker fees?</strong></summary>

Fees are currently set to zero. When fees are introduced, each market will have a maker fee (paid by the order placer) and a taker fee (paid by the order matcher). Fee rates vary by market type. Pre-TGE markets will have a 0.05% maker fee and 0.10% taker fee. Options markets will have a 0.15% maker fee and 0.40% taker fee. RWA markets will have a 0.20% maker fee and 0.30% taker fee.

</details>

<details>

<summary><strong>Can I short a market?</strong></summary>

No. You can only sell positions you already hold. There is no short selling on Premarket.

</details>

<details>

<summary><strong>What happens if there is no liquidity when I want to exit?</strong></summary>

You will not be able to sell your position before expiry. Hold to settlement and your position will be resolved automatically at expiry based on the final outcome.

</details>
