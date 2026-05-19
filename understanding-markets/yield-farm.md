---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Yield Farm

## What is Yield Farm?

Yield Farm is a curated view on top of Prediction Markets. It surfaces high probability outcome legs that are trading below $1. If the outcome resolves correctly, the position settles at $1 and you collect the difference between your entry price and $1 as yield.

Yield Farm is not a separate product type. It uses the same Solana prediction market contracts and the same USDC settlement. It is a different way to discover and filter the same markets.

## How it Works

Every Prediction Market has a YES side and a NO side, each priced between $0 and $1. The Yield Farm view filters for legs trading close to $1, where the implied probability of the outcome is high. You buy the leg, hold until the market settles, and collect $1 per share if the outcome resolves in your favour.

> **Example:** Tottenham relegation NO is trading at 91¢. The market believes there is a 91% chance Tottenham does not get relegated. You buy at 91¢, hold to settlement, and if they avoid relegation you receive $1. Yield is 9¢ per share, or about 9.9% on capital deployed over the holding period.

## How to Read the Yield Farm Table

The Yield Farm page lists each leg with:

| Column | Meaning |
| --- | --- |
| Market | The underlying prediction market |
| Side | YES or NO leg |
| Entry | Current ask price in cents |
| Yield | Spread between entry price and $1 |
| APR | Yield annualised based on time to expiry |
| Expiry | When the underlying market resolves |
| Liquidity | Available size at current price |

## How to Trade

Open the Yield Farm tab, sort by APR or by expiry, and select a leg you have conviction on. Trading mechanics are identical to Prediction Markets. You spend USDC, receive outcome shares, and hold to settlement. Settlement requires a manual redemption step on Solana via the DFlow contract.

## Risk

The implied probability is the market consensus, not a guarantee. A leg priced at 95¢ can still resolve at $0. Losses are capped at your entry price per share. The lower the entry price relative to $1, the higher the implied risk.

{% hint style="info" %}
Yield Farm shares the same chain (Solana), settlement currency (USDC), identity verification requirement, and geographic restrictions as Prediction Markets.
{% endhint %}
