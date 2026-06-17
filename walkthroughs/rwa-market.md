---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Trade an RWA Market

This walkthrough covers buying and selling positions on an RWA market from entry to exit. RWA markets are perpetual, so there is no settlement event. You exit by selling back into the orderbook.

## Step 1: Find an RWA Market

Go to Markets and filter for RWAs. Select the asset you want to trade.

Each market shows:

* available tokens
* current prices
* recent trades
* orderbook liquidity

## Step 2: Select an Asset

Choose the token you want to trade from the market list.

Examples:

* 1g Fullerene C60 99.5%
* 1g Fullerene C60 99.9%
* 1g Fullerene C70 98%
* 1g Fullerene C70 99.9%

Selecting a token updates the buy and sell panel and the orderbook.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the RWA market page after selecting an asset.

_Caption:_ RWA market showing the selected token, current price, and market details.

## Step 3: Check the Orderbook

Open the orderbook and confirm there is active liquidity.

* Bids are buyers
* Asks are sellers

If no matching orders exist, market orders cannot execute.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the RWA orderbook with bids and asks visible.

_Caption:_ RWA orderbook showing the available liquidity before placing a trade.

## Step 4: Buy the Market

Select Buy. Enter the amount of USDM you want to spend. Review estimated shares and execution price and proceed to confirm the trade. If matching sell orders exist, the order executes immediately.

## Step 5: Sell or Hold

Track your position inside Portfolio. If you want to sell:

* select Sell
* enter the amount to sell
* execute against available buyers

If no buyers exist, the order cannot execute until liquidity becomes available.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the Portfolio position and sell flow for an RWA market.

_Caption:_ RWA position showing the current holding and the steps to exit through the orderbook.

## Fees and Chain

RWA markets run on MegaETH. Maker fee is 0.20% and taker fee is 0.30%.

{% hint style="info" %}
Always review the Rules section before trading to confirm the specific market parameters for the asset you are trading.
{% endhint %}
