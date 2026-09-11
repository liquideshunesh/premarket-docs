---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Trade Covered Options

This walkthrough covers covered calls and cash-secured puts on Robinhood Chain. They are part of Premarket and are available through [robinhood.premarket.xyz](http://robinhood.premarket.xyz/).

## Step 1: Connect and Fund Your Account

Connect your wallet and complete the same smart-account onboarding and gas-abstraction flow used by Premarket on MegaETH. No KYC is required.

Deposit the asset required for the action you plan to take:

* **Buying an option:** deposit USDG for the premium.
* **Writing a covered call:** deposit or hold the underlying token used as collateral.
* **Writing a cash-secured put:** deposit USDG for collateral.

Complete the one-time vault operator approval before trading. Without this approval, an order can be signed but cannot fill.

## Step 2: Choose a Market

Open the market selector, choose **Options**, and select an underlying. The interface currently shows CASHCAT, STONKBROKER, AAPL, AMZN, TSLA, and NVDA markets. Available markets can change, so use the live selector as the current list.

## Step 3: Select the Contract

Use the option chain to:

1. Choose **Call** or **Put**.
2. Select an expiry.
3. Compare the available strikes.
4. Review the bid, ask, LP APR, and mark shown for each strike.
5. Select a strike to open its trade ticket.

For calls, the option leg is labelled **Long**. For puts, it is labelled **Short**. The writer side is labelled **LP** for both.

## Step 4: Choose an Action

Use the option-leg or LP selector, then choose the action that matches your intent:

* **Buy Long** on a call or **Buy Short** on a put to open an option position. You pay the premium in USDG.
* **Sell Long** on a call or **Sell Short** on a put to close an option position you hold. You receive the premium in USDG.
* **Write LP** to open a fully collateralized writer position. The required call or put collateral is locked when the order fills, and you receive the premium in USDG.
* **Burn LP** to close a writer position. You pay the USDG premium required by the orderbook and unlock the full associated collateral.

## Step 5: Review and Confirm

Choose the order type, enter the size, and review the ticket. A Market order uses available resting liquidity; a Limit order rests at the price you set until it matches or expires. Depending on the action, the ticket can show your available balance, cost, strike at which the option starts paying, breakeven, and liquidity status.

{% hint style="info" %}
If the ticket shows **No liquidity on this side**, a Market order cannot execute. You can select another contract or wait for liquidity.
{% endhint %}

Before confirming, verify the underlying, call or put type, strike, expiry, selected leg, Buy/Sell or Write/Burn action, premium, size, and required approval.

## Step 6: Track the Order

Expand the selected strike to review the **Order Book**, **Live Trades**, **Orders**, **History**, and **Positions** tabs. Your Portfolio also separates positions, open orders, history, collateral, and spot balances.

Position history can label a completed **Write** action as **Mint LP**. Both names refer to opening the LP writer position.

An unmatched order remains open until it fills, reaches its selected order expiry, or you cancel it. Cancellation is free and immediate.

## Step 7: Mint or Unwind a Pair

Open the trade settings and select **Mint** to deposit the contract's collateral and receive equal amounts of its option and LP legs.

After minting, you can sell the option leg and keep the LP writer position, sell the LP leg and keep the option position, or retain both. Minting the pair does not itself pay a premium.

Use **Unwind** when you hold equal option and LP amounts for the same contract. The paired tokens are burned and the full associated collateral is returned. Premiums previously paid or received remain separate.

## Step 8: Exit or Hold to Expiry

Before expiry, use **Sell** for an option position, **Burn** for an LP position, or **Unwind** for an equal pair. Sell and Burn orders require matching orderbook liquidity.

If you hold the position through expiry:

* A call's Long leg receives the call payout above the strike, while LP receives the remaining underlying collateral.
* A put's Short leg receives the put payout below the strike, while LP receives the remaining USDG collateral.
* The two settlement payouts always add up to the collateral originally locked for the position.
* If no final oracle price is available, the option and LP legs each receive half of the locked collateral.

See [Covered Options](../understanding-markets/covered-calls.md) for numerical settlement examples and the complete position model.
