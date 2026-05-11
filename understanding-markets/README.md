---
cover: ../.gitbook/assets/cover-main (7).png
coverY: 205.52754237288138
---

# Understanding Markets

Premarket is an orderbook-based platform. Before you trade, it helps to understand how the orderbook works, what liquidity means in practice, and what happens when your order hits the chain.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

## What All Markets Have in Common

Regardless of which market you trade on Premarket, the same core mechanics apply across all of them. Each market type has its own payout structure and settlement logic but the underlying infrastructure is shared.

* All trades require a counterparty. No counterparty means no execution.
* Makers place orders and add liquidity. Takers match existing orders and remove it.
* Order matching happens off-chain. Final settlement is always recorded on-chain.
* Liquidity is never guaranteed. You may not always be able to enter or exit when you want to.
* Treating all markets the same is the most common mistake. Prediction markets and FDV band markets look similar in the UI but behave very differently at settlement.

## How to Read the Orderbook

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

The orderbook shows all active buy and sell orders for a market. Bids are orders from buyers, asks are orders from sellers. The gap between the highest bid and the lowest ask is called the spread. A tight spread means the market is liquid and active. A wide spread means fewer participants and harder execution. If the orderbook is empty on one side, your order will not execute until someone else places a matching order.

## How Your Execution Price Is Determined

When you place a market order, it matches against the best available orders in the book. If your order is large relative to available liquidity, it will consume multiple price levels and your average execution price may differ from the price you saw when you entered. This is called slippage. Limit orders avoid slippage by only executing at your specified price, but they are not guaranteed to fill.

## What Onchain Settlement Means for You

Trades on Premarket are matched offchain for speed but settled on-chain for finality. After a trade executes you will see a short confirmation period while the transaction is recorded on the blockchain. During this time your position may appear as pending. Once confirmed it will appear in your portfolio with full position details. Settlement at expiry follows the same process and is handled automatically.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Each market type has its own payout structure, liquidity profile, and settlement logic. Read the individual guides below to understand exactly what to expect with each market type:

1. [Prediction Markets](prediction-markets.md#what-are-prediction-markets)
2. [Pre-TGE Markets](pre-tge-markets.md#what-are-pre-tge-markets)
3. [Options Markets](options-markets.md#what-are-options-markets)
4. [Spot Markets](spot-markets.md#what-are-spot-markets)
