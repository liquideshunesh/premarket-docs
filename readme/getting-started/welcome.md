---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Welcome to Premarket

Most assets only become tradable after they already exist. By the time a token lists, an IPO prices, or an event resolves, the earliest and most profitable window has already closed. The people who got in early made their conviction known when it mattered most and got paid for it. Everyone else arrived too late. Premarket exists to move trading earlier.

## Introduction

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Premarket application homepage</p></figcaption></figure>

Premarket is a trading platform for assets and outcomes that do not exist yet. Before a token launches, before a company goes public, before an event resolves, you can already take a position on what you think will happen.

## Market Types

Premarket currently supports multiple market categories:

### **1. FDV Band Markets**

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p><strong>FDV Band Markets with buy and sell options</strong></p></figcaption></figure>

Trade valuation ranges on pre-TGE tokens and pre-IPO assets. You pick a band and if the asset launches within that range, you get paid.

> **Example:** You believe Monad will launch above $2B. You buy the $2B to $3B band. If Monad lists at $2.4B, you receive a partial payout that scales with how far into the range it lands. If it lists at $3B or above, you receive the maximum payout. If it lists below $2B, you receive nothing..

### **2. Prediction Markets**

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p><strong>Prediction Market page with outcomes</strong></p></figcaption></figure>

Trade binary outcomes on real world events. Back the correct outcome and each share pays $1 at settlement.

> **Example:** You believe MegaETH will launch before the end of Q2. You buy YES. If it does, every share pays $1. If it does not, your shares expire at $0.

### **3. Option Markets**

Trade structured upside or downside exposure using predefined strike ranges. These markets use option style mechanics with collateral, outcome tokens, and write positions.

> **Example:** ETH is currently trading around $2,290. You believe it will rise and settle between $2,400 and $2,500 at expiry. You buy the $2,400–$2,500 CALL band. If ETH settles within the range, payout scales linearly toward the upper strike. If it settles at $2,500 or above, you receive the maximum payout. If it settles below $2,400, the position expires worthless.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption><p><strong>Options chain with buy and sell choices</strong></p></figcaption></figure>

### **4. RWA Markets**

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption><p>RWA market example with buy and sell options</p></figcaption></figure>

Trade Real World Assets(RWAs) pairs directly using live market pricing. These markets behave similarly to traditional exchanges where traders exchange one asset for another.

> **Example:** You buy 1g fullerene c60 99.5% using USDM at the current market price. The market is perpetual with no expiry, so you hold the position as long as you want and sell back to USDM when you choose to exit. Your profit or loss is simply the difference between your buy and sell price.

All market types run on a live orderbook. Prices are not set by the platform, they emerge from real buy and sell orders. A higher price means the market collectively believes something is more likely. You can enter and exit positions freely before settlement, as long as someone is willing to take the other side.

{% hint style="warning" %}
**Before you start:**

* You can lose your full position if the outcome goes against you.
* Early exit depends on available liquidity, it is never guaranteed.
* Settlement at expiry is always guaranteed. Pre-IPO, Pre-TGE, Options, and RWA markets settle automatically to your smart account. Prediction markets settle on Solana and require a manual redemption step via the DFlow contract.
* Prediction markets require KYC verification and are not available in all regions. All other markets do not require KYC.
{% endhint %}

Head to [Getting Started](setup.md) next, for steps on account setup and get ready to place your first trade.
