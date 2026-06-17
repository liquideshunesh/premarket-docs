---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Trade an Options Spread

This walkthrough covers trading an options spread from entry to exit. The default flow is to place an order on the orderbook, the platform mints or unwinds the underlying tokens for you automatically. A separate advanced flow for writers who want to mint manually is covered at the end.

## Step 1: Select a Spread

Go to Markets, filter for Options, and open an active market (BTC/USD, ETH/USD, HYPE/USD, or ZEC/USD Spreads). Select the price spread that matches your view on where the underlying will settle at expiry.

## Step 2: Choose Up or Down

Pick a side. Up profits as the asset settles within or above the range. Down profits as it settles within or below the range.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the options market with spread selection visible.

_Caption:_ Options market showing the selected expiry, spread, and Up or Down choices.

## Step 3: Place Your Order

1. Enter the amount you want to trade.
2. Choose market or limit. With limit you can select your price directly from the orderbook.
3. Place the order.
4. When it matches, your position is created automatically, no separate mint step.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the order entry flow for an options spread.

_Caption:_ Options trade panel showing amount entry, order type, and confirmation.

## Step 4: View and Manage in Portfolio

Go to Portfolio. Your position shows with current value, size, and unrealised P\&L. You can also view your open positions and orders directly from the market page.

## Step 5: Exit

To exit, place a sell order on the same spread. When your sell matches an opposite sell, the positions merge and your collateral is released back to you automatically, no separate unwind step. Alternatively, hold to expiry and the position settles automatically.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the active options position in Portfolio.

_Caption:_ Options position showing current value, exit action, and settlement path.

## Advanced: Writing a Position

If you want to provide liquidity and collect premium rather than take a directional view, you can mint a position pair directly:

1. Open the spread and choose to mint.
2. Enter the USDM amount to deposit as collateral.
3. Confirm. You receive both sides of the spread (the Down/write side and the Up side).
4. Sell the side you do not want to hold on the orderbook to collect premium.

### Screenshot

**Screenshot placeholder:** Add a screenshot of the advanced mint flow for writers.

_Caption:_ Writer flow showing collateral deposit and both sides of the minted position.

{% hint style="info" %}
Writing is optional. Most users never mint manually, placing an order on the book mints and unwinds for you.
{% endhint %}
