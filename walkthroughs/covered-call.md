---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Use a Covered Call

This walkthrough follows the Covered Call collateral and settlement lifecycle on Robinhood Chain. Covered Calls are part of Premarket and are accessed through [robinhood.premarket.xyz](http://robinhood.premarket.xyz/).

Covered Call account creation, wallet onboarding, and gas abstraction follow the same flow as Premarket on MegaETH. No KYC is required. Fund the account with the supported underlying token before placing an order.

## Step 1: Open the Covered Call Experience

Go to [robinhood.premarket.xyz](http://robinhood.premarket.xyz/), open the **Options** tab, and select a Covered Call market. Market cards show the underlying, expiry, available strikes, and any quoted LONG or SHORT prices.

## Step 2: Select an Expiry and Strike

Open the expiry tab in the option chain and compare the strike rows. Each row can show:

* Strike
* LONG quote
* SHORT quote
* Max payout

Select a strike to update the trade panel and target line on the price chart. The strike determines when the LONG claim begins to receive a payout.

## Step 3: Choose Your Role

Select **Buy**, then choose a side:

* **LONG:** acquires the call payoff above the strike for the quoted price.
* **SHORT:** takes the covered-call writer side, which receives the locked collateral minus the LONG payout.

When a new position pair is created, one unit of the underlying is locked per position and equal LONG and SHORT claims are created.

{% hint style="warning" %}
The SHORT obligation follows the SHORT claim. Transferring that claim transfers the obligation and the right to the remaining collateral.
{% endhint %}

## Step 4: Enter the Order

Choose the available order type. The screenshots confirm a **Market** order flow. Enter the amount using the underlying-denominated amount control or the 25%, 50%, 75%, and 100% balance shortcuts.

Before confirming, verify the selected strike, LONG or SHORT side, displayed quote, amount, available balance, and transaction details. The premium and any fees are paid in the underlying token. The applicable fee rate is not documented in this guide.

{% hint style="info" %}
If the trade panel shows **No liquidity on this side**, a Market order cannot be confirmed. Select another strike or side, or wait for liquidity.
{% endhint %}

## Step 5: Review Orders and Positions

Expand the selected strike to view the Order Book, Live Trades, Orders, History, Positions, and Chart tabs. The orderbook shows price, size, and total value. The balance panel separates your total balance, amount in orders, and available amount for the underlying and selected position side.

If an order does not match, it remains in the orderbook until it reaches its expiry or you cancel it.

## Step 6: Exit or Unwind Before Expiry

To exit one side, select **Sell** and place an order for the LONG or SHORT position you hold. The sale executes only when it matches available orderbook liquidity.

If you hold equal amounts of LONG and SHORT for the same strike and expiry, unwind the paired claims to receive the underlying token back.

## Step 7: Hold to Expiry

The underlying remains as collateral for the LONG and SHORT claims. At expiry, the market rules determine the final price.

## Step 8: Settle the Position

* At or below the strike, LONG receives nothing and SHORT receives the full underlying.
* Above the strike, LONG receives `(final price - strike) / final price` units of the underlying. SHORT receives the remainder.
* If no final price is available and the market is marked with a null outcome, LONG and SHORT each receive half of the collateral.

See [Covered Calls](../understanding-markets/covered-calls.md) for the payout example and important restrictions.
