---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Trade an Options Spread

This walkthrough covers trading an options spread from entry to exit. The default flow is to place an order on the orderbook, and the platform handles the underlying paired-token mechanics for you. A separate advanced flow for users who want to mint UP/DOWN pairs manually is covered at the end.

## Step 1: Select a Spread

Go to Markets, filter for Options, and open an active market (BTC/USD, ETH/USD, HYPE/USD, or ZEC/USD Spreads). Select the price spread that matches your view on where the underlying will settle at expiry.

## Step 2: Choose UP or DOWN

Pick a side. UP behaves like exposure to a call spread and reaches max payout above the upper strike. DOWN behaves like exposure to a put spread and reaches max payout below the lower strike. Inside the range, UP and DOWN split the payout linearly.

## Step 3: Place Your Order

1. Enter the amount you want to trade.
2. Choose market or limit. With limit you can select your price directly from the orderbook.
3. Place the order.
4. When it matches, your position is created without a separate mint step.

## Step 4: View and Manage in Portfolio

Go to Portfolio. Your position shows with current value, size, and unrealised P\&L. You can also view your open positions and orders directly from the market page.

## Step 5: Exit

To exit, place a sell order on the same spread. When your sell matches an opposite sell, the positions merge and collateral is released back to you without a separate unwind step. Alternatively, hold to expiry and the position settles according to the market rules.

## Advanced: Minting UP/DOWN Pairs

If you want to provide liquidity and collect premium rather than take a directional view, you can mint a position pair directly:

1. Open the spread and choose to mint.
2. Enter the USDM amount to deposit as collateral.
3. Confirm. You receive both sides of the spread: UP and DOWN.
4. Sell the side you do not want to hold on the orderbook to collect premium.

{% hint style="info" %}
Manual minting is optional. Most users never mint manually because placing an order on the book handles the paired-token flow for you.
{% endhint %}
