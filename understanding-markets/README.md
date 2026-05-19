---
cover: ../.gitbook/assets/Understanding Markets.png
coverY: 2.158858731375986
---

# Understanding Markets

Premarket is an orderbook based platform. Before you trade, it helps to understand how the orderbook works, what liquidity means in practice, and how each market type settles.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>All Markets</p></figcaption></figure>

## What All Markets Have in Common

Regardless of which market you trade on Premarket, the same core mechanics apply across all of them. Each market type has its own payout structure and settlement logic but the underlying infrastructure is shared.

* All trades require a counterparty. No counterparty means no execution.
* Makers place orders and add liquidity. Takers match existing orders and remove it.
* Order matching happens offchain. Final settlement is always recorded onchain.
* Liquidity is never guaranteed. You may not always be able to enter or exit when you want to.

## The Six Market Types

Although the core mechanics are shared, each market type behaves differently at settlement. Treating all markets the same is the most common mistake. Here is how they compare.

| Market | Chain | Currency | Settlement | Identity verification | Currently live |
| --- | --- | --- | --- | --- | --- |
| Prediction Markets | Solana | USDC | Manual via DFlow | Required | Yes |
| Yield Farm | Solana | USDC | Manual via DFlow | Required | Yes |
| Pre IPO Markets | MegaETH | USDM | Automatic to smart account | Not required | No live markets |
| Pre TGE Markets | MegaETH | USDM | Automatic to smart account | Not required | No live markets |
| Options Markets | MegaETH | USDM | Automatic to smart account | Not required | Yes |
| RWA Markets | MegaETH | USDM | Perpetual, no settlement | Not required | Yes |

## How to Read the Orderbook

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>Orderbook</p></figcaption></figure>

The orderbook shows all active buy and sell orders for a market. Bids are orders from buyers, asks are orders from sellers. The gap between the highest bid and the lowest ask is called the spread. A tight spread means the market is liquid and active. A wide spread means fewer participants and harder execution. If the orderbook is empty on one side, your order will not execute until someone else places a matching order.

## How Your Execution Price Is Determined

When you place a market order, it matches against the best available orders in the book. If your order is large relative to available liquidity, it will consume multiple price levels and your average execution price may differ from the price you saw when you entered. This is called slippage. Limit orders avoid slippage by only executing at your specified price, but they are not guaranteed to fill.

## What Onchain Settlement Means for You

Trades on Premarket are matched offchain for speed, but every fill and final settlement is recorded onchain. This means your trade execution is fast, but the canonical record of what you own and what you are owed lives onchain.

Settlement at expiry varies by product:

* MegaETH markets (Pre IPO, Pre TGE, Options, RWA): positions settle automatically at expiry and proceeds are sent directly to your smart account. No action required.
* Solana markets (Prediction Markets, Yield Farm): positions require manual redemption via the DFlow contract once expired. This burns your shares and bridges USDC back to your wallet.

After placing a trade, your position may briefly appear as pending in your portfolio while the fill is confirmed onchain. Once confirmed, it will show full position details.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>Portfolio after fill</p></figcaption></figure>

Each market type has its own payout structure, liquidity profile, and settlement logic. Read the guide for the market type you plan to trade:

1. [Prediction Markets](prediction-markets.md): binary YES/NO outcomes on real world events. Solana, USDC, identity verification required.
2. [Yield Farm](yield-farm.md): curated view of high probability prediction market legs. Solana, USDC, identity verification required.
3. [Pre IPO Markets](pre-ipo-markets.md): valuation bands on private companies before listing. MegaETH, USDM.
4. [Pre TGE Markets](pre-tge-markets.md): valuation bands on tokens before launch. MegaETH, USDM.
5. [Options Markets](options-markets.md): price range bands on existing assets with PRM/oPRM token mechanics. MegaETH, USDM.
6. [RWA Markets](rwa-markets.md): perpetual spot trading of tokenised real world assets. MegaETH, USDM.
