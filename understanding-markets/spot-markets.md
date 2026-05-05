# Spot Markets

## What are Spot Markets?

Spot markets allow you to trade real tokens directly against USDM. Unlike prediction markets, there are no outcomes, probabilities, or settlement events. You are simply buying and selling assets at market prices.

> **Example:** WETH/USDM = buying or selling WETH using USDM.

## Key Characteristics

- No expiry: markets are perpetual.
- No resolution: positions do not settle to $0 or $1.
- Real assets: you hold tokens like WETH.
- Order book driven: trades only happen if counterparties exist.

## How Trading Works

**Buying:** You spend USDM, receive WETH, and match with someone selling WETH.

**Selling:** You give WETH, receive USDM, and match with someone buying WETH.

{% hint style="warning" %}
Trades only execute if there is liquidity. "No price available for market order" is a liquidity issue, not a balance issue.
{% endhint %}

## Maker vs Taker

| Role | Description |
|------|-------------|
| Maker | Places order first. Provides liquidity. |
| Taker | Matches existing order. Removes liquidity. |
