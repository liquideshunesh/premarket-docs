---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Welcome to Premarket

Most assets only become tradable after they already exist. By the time a token lists, an IPO prices, or an event resolves, the earliest and most profitable window has already closed. The people who got in early made their conviction known when it mattered most and got paid for it. Everyone else arrived too late. Premarket exists to move trading earlier.

## Introduction

Premarket is a trading platform for assets and outcomes before they exist or resolve anywhere else. Before a token launches, before a company goes public, before an event resolves, you can already take a position on what you think will happen. The platform also supports trading on existing assets through options and tokenised real world assets.

## Market Types

Premarket supports six market categories across two chains.

### 1. Prediction Markets

Trade binary outcomes on real world events. Back the correct outcome and each share pays $1 at settlement. Runs on Solana with USDC.

> **Example:** You believe MegaETH will launch before the end of Q2. You buy YES. If it does, every share pays $1. If it does not, your shares expire at $0.

### 2. Yield Farm

A curated view on top of Prediction Markets. Yield Farm surfaces high probability outcome legs trading below $1, with the spread to $1 representing yield if the position resolves correctly. Same chain as Prediction Markets (Solana), same settlement currency (USDC).

> **Example:** A leg priced at 91¢ implies the market believes there is a 91% chance the outcome resolves YES. You buy at 91¢, hold to settlement, and if correct you collect $1. Yield is 9¢ per share.

### 3. Pre IPO Markets

Trade valuation spreads on private companies before they go public. You pick a spread and if the company lists within that range, your position pays out. Runs on MegaETH with USDM. No Pre IPO markets are currently live.

### 4. Pre TGE Markets

Trade valuation spreads on tokens before launch. Same mechanic as Pre IPO. You pick a spread and if the token launches within that range, your position pays out. Runs on MegaETH with USDM. No Pre TGE markets are currently live.

> **Example:** You believe a token will launch above $2B. You buy the $2B to $3B spread. If it lists at $2.4B, you receive a partial payout that scales with how far into the range it lands. If it lists at $3B or above, you receive the maximum payout. If it lists below $2B, you receive nothing.

### 5. Options Markets

Trade structured upside or downside on existing assets using predefined strike ranges. Each spread has two sides, Up and Down. Runs on MegaETH with USDM. Live markets are BTC/USD, ETH/USD, HYPE/USD, and ZEC/USD Spreads.

> **Example:** ETH is trading around $2,290. You believe it will settle between $2,400 and $2,500 at expiry. You buy Up on the $2,400 to $2,500 spread. If ETH settles within the range, payout scales linearly toward the upper strike. If it settles at $2,500 or above, you receive the maximum payout. If it settles below $2,400, the position expires worthless.

### 6. RWA Markets

Trade tokenised real world assets directly against USDM. These are perpetual spot markets with no expiry. Profit or loss is realised only when you sell. Runs on MegaETH. Live markets are Fullerene C60 99.5%, Fullerene C60 99.9%, Fullerene C70 98%, and Fullerene C70 99.9%, all per gram.

> **Example:** You buy 1g Fullerene C60 99.5% using USDM at the current market price. The market is perpetual with no expiry, so you hold the position as long as you want and sell back to USDM when you choose to exit. Your profit or loss is the difference between your buy and sell price.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Premarket app overview</p></figcaption></figure>

## How All Markets Work

All market types run on a live orderbook. Prices are not set by the platform, they emerge from real buy and sell orders. A higher price means the market collectively believes something is more likely. You can enter and exit positions freely before settlement, as long as someone is willing to take the other side.

{% hint style="warning" %}
**Before you start:**

* You can lose your full position if the outcome goes against you.
* Early exit depends on available liquidity, it is never guaranteed.
* Settlement at expiry is always guaranteed. Pre IPO, Pre TGE, Options, and RWA markets settle automatically to your smart account on MegaETH. Prediction Markets and Yield Farm run on Solana and require a manual redemption step via the DFlow contract.
* Prediction Markets and Yield Farm require identity verification and are not available in all regions. All other markets do not require verification.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Example market page</p></figcaption></figure>

Head to [Getting Started](setup.md) next, for steps on account setup and your first trade.
