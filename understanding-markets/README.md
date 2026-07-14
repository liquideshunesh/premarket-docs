---
cover: ../.gitbook/assets/Understanding Markets.png
coverY: 0
---

# Understanding Markets

Premarket uses a similar trading interface across products, but the products work differently. Before you trade, understand which product you are using, how it settles, and which chain and currency it uses.

## What Markets Share

Premarket uses a similar orderbook interface across products, but payout logic, settlement, and infrastructure differ by product. The main shared mechanics are order matching, liquidity, and portfolio tracking.

* All trades require a counterparty. No counterparty means no execution.
* Makers place orders and add liquidity. Takers match existing orders and remove it.
* Orders are matched through Premarket's trading system, while ownership and settlement records are finalized onchain.
* Liquidity is never guaranteed. You may not always be able to enter or exit when you want to.

## Product Types and Market Categories

Premarket offers three main product types: Prediction Markets, Options Markets, and RWA / Spot Markets. Some labels in the app, such as Pre-TGE or Pre-IPO, describe market categories or underlyings rather than separate product mechanics.

* **Prediction Markets**
  * Binary YES/NO event markets
  * Run on Solana
  * Trade in USDC
  * Powered by DFlow, which tokenizes Kalshi markets on Solana
  * Winning shares are redeemed manually through DFlow after resolution
* **Options Markets**
  * LONG/SHORT spread markets with a defined range and expiry
  * Run on MegaETH
  * Trade in USDM
  * Cash-settled at expiry
  * LONG and SHORT split a combined value of $1 at settlement
* **RWA / Spot Markets**
  * Spot orderbooks for supported assets
  * Run on MegaETH
  * Use supported deposited assets and quote currencies
  * No expiry-based options settlement
  * Value is realised by buying, holding, and selling

Market labels such as Pre-TGE, Pre-IPO, and some crypto listings describe categories within options-style markets when they use the same LONG/SHORT spread mechanics. Yield Farm is a filtered view of prediction market legs, not a separate product.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>Markets interface showing the available market types and current listings.</p></figcaption></figure>

## Market Categories vs Product Types

Some market labels describe what the market is about, not how it works.

* **Prediction Markets** are a product type.
* **Options Markets** are a product type.
* **RWA / Spot Markets** are a product type.
* **Pre-TGE** and **Pre-IPO** usually describe categories within options-style markets when they use the same LONG/SHORT spread mechanics.
* **Yield Farm** is a discovery view for prediction market legs, not a separate contract type.

Start by identifying the product type first. Then read the market rules for the specific category or underlying.

## How to Read the Orderbook

The orderbook shows all active buy and sell orders for a market in a single unified book. On options-style spread markets, the LONG and SHORT sides share one orderbook. Bids are orders from buyers, asks are orders from sellers. The gap between the highest bid and the lowest ask is called the spread. A tight spread means the market is liquid and active. A wide spread means fewer participants and harder execution. If the orderbook is empty on one side, your order will not execute until someone else places a matching order.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>Market page showing bids, asks, spread, and trade</p></figcaption></figure>

## How Your Execution Price Is Determined

When you place a market order, it matches against the best available orders in the book. If your order is large relative to available liquidity, it will consume multiple price levels and your average execution price may differ from the price you saw when you entered. This is called slippage. Limit orders avoid slippage by only executing at your specified price, but they are not guaranteed to fill.

## What Onchain Settlement Means for You

Trades on Premarket are matched offchain for speed, but every fill and final settlement is recorded onchain. This means your trade execution is fast, but the canonical record of what you own and what you are owed lives onchain.

Settlement and post-trade handling differ by product:

* **Prediction Markets:** if the market resolves normally, winning shares are redeemable for $1 and losing shares expire at $0. Redemption is manual through DFlow.
* **Options Markets:** positions are cash-settled at expiry based on the market rules and final settlement value. LONG and SHORT split a combined value of $1.
* **RWA / Spot Markets:** these markets do not use expiry-based settlement. Users realise value by buying and selling supported assets through the orderbook.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption><p>Representative market page</p></figcaption></figure>

For MegaETH products, your smart account handles deposits, balances, open positions, and settlement proceeds. See [Smart Account and 1-Click Trading](../readme/getting-started/smart-account.md) for the current account setup flow.

After placing a trade, your position may briefly appear as pending in your portfolio while the fill is confirmed onchain. Once confirmed, it will show full position details.

Choose the guide that matches the product you want to trade:

1. [Prediction Markets](prediction-markets.md): binary YES/NO event markets on Solana, with manual redemption through DFlow.
2. [Options Markets](options-markets.md): LONG/SHORT spread markets on MegaETH, including categories such as Pre-TGE and Pre-IPO where the same mechanics apply.
3. [RWA / Spot Markets](rwa-markets.md): spot orderbook markets for supported assets on MegaETH.
4. [Yield Farm](yield-farm.md): a filtered view of prediction market legs, not a separate product type.
