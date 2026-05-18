---
cover: ../.gitbook/assets/Understanding Markets.png
coverY: 2.158858731375986
---

# Understanding Markets

Premarket is an orderbook-based platform. Before you trade, it helps to understand how the orderbook works, what liquidity means in practice, and what happens at settlement.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>All Markets</p></figcaption></figure>

## What All Markets Have in Common

Regardless of which market you trade on Premarket, the same core mechanics apply across all of them. Each market type has its own payout structure and settlement logic but the underlying infrastructure is shared.

* All trades require a counterparty. No counterparty means no execution.
* Makers place orders and add liquidity. Takers match existing orders and remove it.
* Order matching happens offchain. Final settlement is always recorded onchain.
* Liquidity is never guaranteed. You may not always be able to enter or exit when you want to.

Although the core mechanics are shared, each market type behaves differently at settlement. Treating all markets the same is the most common mistake, prediction markets and FDV band markets look similar in the UI but resolve in fundamentally different ways. Here is how they compare:

<table><thead><tr><th width="179.234375">Feature</th><th width="278.08203125">Prediction Markets</th><th>FDV Bands</th></tr></thead><tbody><tr><td>Outcome type</td><td>Binary YES/NO</td><td>Directional spread</td></tr><tr><td>Payout</td><td>Fixed $1 or $0 per share</td><td>Linearly scaled within range, capped at max</td></tr><tr><td>Resolution</td><td>Real-world event outcome</td><td>Token FDV at launch</td></tr><tr><td>Settlement source</td><td>Verified event source</td><td>Oracle (Bybit, Binance, Hyperliquid, Chainlink)</td></tr><tr><td>Network</td><td>Solana</td><td>MegaETH</td></tr><tr><td>KYC required</td><td>Yes</td><td>No</td></tr><tr><td>Settlement action</td><td>Manual redemption via DFlow</td><td>Automatic to smart account</td></tr></tbody></table>

## How to Read the Orderbook

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>Order book</p></figcaption></figure>

The orderbook shows all active buy and sell orders for a market. Bids are orders from buyers, asks are orders from sellers. The gap between the highest bid and the lowest ask is called the spread. A tight spread means the market is liquid and active. A wide spread means fewer participants and harder execution. If the orderbook is empty on one side, your order will not execute until someone else places a matching order.

## How Your Execution Price Is Determined

When you place a market order, it matches against the best available orders in the book. If your order is large relative to available liquidity, it will consume multiple price levels and your average execution price may differ from the price you saw when you entered. This is called slippage. Limit orders avoid slippage by only executing at your specified price, but they are not guaranteed to fill.

## What Onchain Settlement Means for You

Trades on Premarket are matched offchain for speed, but every fill and final settlement is recorded onchain. This means your trade execution is fast, but the canonical record of what you own and what you're owed lives onchain.

Settlement at expiry varies by product:

* MegaETH markets (Pre-TGE, Pre-IPO, Options, RWA): Positions settle automatically at expiry and proceeds are sent directly to your smart account. No action required.
* Solana markets (Prediction Markets): Positions require manual redemption via the DFlow contract once expired. This burns your shares and bridges USDC back to your wallet.

After placing a trade, your position may briefly appear as pending in your portfolio while the fill is confirmed onchain. Once confirmed, it will show full position details.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>Portfolio after fill</p></figcaption></figure>

Each market type has its own payout structure, liquidity profile, and settlement logic. Read the guide for the market type you plan to trade, next:

1. [Prediction Markets](prediction-markets.md): binary YES/NO outcomes on real-world events. Solana, KYC required.
2. [Pre-TGE Markets](pre-tge-markets.md): valuation bands on tokens before launch. MegaETH. Pre-IPO markets use the same mechanics.
3. [Options Markets](options-markets.md): price range bands on existing assets with PRM/oPRM token mechanics. MegaETH.
4. [RWA Markets](spot-markets.md): perpetual spot trading of tokenised real world assets (RWAs). MegaETH.
