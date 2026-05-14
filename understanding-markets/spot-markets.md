---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Spot Markets

Spot markets allow you to trade real tokens directly against USDM. Unlike prediction markets, there are no outcomes, probabilities, or settlement events. You are simply buying and selling assets at market prices.

> **Example:** WETH/USDM = buying or selling WETH using USDM.

## **Key Characteristics**

1. **No expiry:** markets are perpetual.
2. **No resolution:** positions do not settle to $0 or $1.
3. **Real assets:** you hold tokens like WETH.
4. **Order book driven:** trades only happen if counterparties exist.

### **How Trading Works**

1. **Buying:** You spend USDM, receive WETH, and match with someone selling WETH.
2. **Selling:** You give WETH, receive USDM, and match with someone buying WETH.

Trades only execute if there is liquidity. "No price available for market order" is a liquidity issue, not a balance issue.

### **Maker vs Taker**

1. Maker: Places order first. Provides liquidity.
2. Taker: Matches existing order. Removes liquidity.

> **Example:** Buy 1g Fullerene C70 99.9% at 500 USDM Hold the position. No expiry, no settlement event. Price moves to 550 USDM Sell at 550 USDM, receive 550 USDM Profit = 50 USDM

You can hold the asset indefinitely. Profit or loss is realised only when you sell.

## **Settlement**

Spot markets have no expiry and no settlement event. Your position stays open until you sell it back into the orderbook. There is no automatic payout, no oracle resolution, and no expiry-based closure. The only way to close a spot position is to place a sell order and match with a buyer.

### **What this means in practice**

No time pressure. Your position does not expire, so you can hold as long as you want.

Exit depends on liquidity. You can only sell if there is a buyer on the orderbook. If liquidity is thin, you may not be able to exit at your target price. No payout structure. Your profit or loss is simply the difference between buy price and sell price, minus any fees.
