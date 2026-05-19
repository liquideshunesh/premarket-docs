---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Trade a Prediction Market

This walkthrough covers the full flow from opening a market to settlement.

## Step 1: Find a Market

Go to [app.premarket.xyz](https://app.premarket.xyz) and open the Markets section. Filter for Prediction Markets. Browse the active list. Each market shows the current Yes and No prices, volume, and expiry date.

## Step 2: Read the Market Rules

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Market Rules example</p></figcaption></figure>

Before trading, click the Rules tab on the market page. This defines exactly what outcome must occur for YES to resolve at $1. Read this carefully before placing any trade.

## Step 3: Check the Orderbook

Click the Orderbook tab. Confirm there are active bids and asks on both sides. If one side is empty, you may not be able to execute at a market order.

## Step 4: Place Your Trade

1. Select Buy Yes or Buy No depending on your view.
2. Enter the amount of USDC you want to spend.
3. Review the shares you will receive and the maximum payout.
4. Click Buy Yes or Buy No to confirm.

## Step 5: Track Your Position

Go to Portfolio. Your position appears with current value, shares held, and unrealised P\&L. Monitor it as the market moves.

## Step 6: Exit Early or Hold to Settlement

1. To exit early: click Sell next to your position in Portfolio. Confirm the transaction. Your P\&L is locked in immediately.
2. To hold to settlement: when the event resolves, winning shares pay $1 and losing shares pay $0. Prediction markets route through a liquidity partner on Solana, so once your position expires you need to redeem it manually via the DFlow contract. This burns your shares, redeems the USDC, and bridges it back to your wallet.
