---
coverY: 0
---

# Placing a Buy Order

A buy order lets you open a position on an outcome or band. When you buy, you spend USDM and receive shares or position tokens representing your exposure.

> Screenshot: Trade panel in buy mode with outcome selected

## Before You Buy

{% hint style="warning" %}
Make sure the following are in place before placing a buy order:

* Wallet is connected
* USDM is approved for spending
* Smart account has a funded balance
{% endhint %}

## How to Place a Buy Order

1. Go to **Markets** and open any active market.
2. Select the outcome you want to buy.
   * Prediction markets: **Buy Yes** or **Buy No**
   * Pre-TGE band markets: select your target band
   * Options markets: select the band and mint your position
3. Enter the amount of USDM you want to spend.
4. Click **Buy** to confirm.

> Screenshot: Step by step buy flow

## What Happens After You Buy

**Liquidity Available:** Your order executes immediately. You receive shares at the current ask price. Your position appears in Portfolio showing shares held, cost, current value, maximum win, and unrealized P\&L.

**No Liquidity:** You will see "No price available for market order." Place a limit order at your target price and wait for a counterparty.

| Error              | Cause              | Fix                                     |
| ------------------ | ------------------ | --------------------------------------- |
| No price available | Orderbook is empty | Try a limit order or wait for liquidity |
| Approval required  | USDM not approved  | Click Approve USDM and retry            |
