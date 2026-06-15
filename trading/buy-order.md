---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Placing a Buy Order

A buy order lets you open a position on an outcome, spread, or asset. When you buy, you spend USDM (on MegaETH) or USDC (on Solana) and receive shares, position tokens, or asset tokens representing your exposure.

## Before You Buy

{% hint style="warning" %}
Make sure the following are in place before placing a buy order:

* Wallet is connected
* The settlement currency for that market is approved for spending (USDM for MegaETH markets, USDC for Solana markets)
* Smart account has a funded balance on the correct chain
{% endhint %}

## How to Place a Buy Order

1. Go to Markets and open any active market
2. Select the outcome, spread, or asset you want to buy

* Prediction Markets and Yield Farm: Buy Yes or Buy No

* Pre TGE and Pre IPO spread markets: select your target spread

* Options spread markets: select the spread and choose Up or Down
* RWA markets: select the asset and buy at the current ask

3. Enter the amount you want to spend
4. Review the trade details

5. Click the buy button to confirm. The label depends on the market type: Buy Yes or Buy No for Prediction Markets and Yield Farm, Up or Down for Pre TGE, Pre IPO, and Options spread markets, Buy for RWA markets.

## What Happens After You Buy

1. **If liquidity is available:** your order executes immediately. You receive shares at the current ask price. Your position appears in Portfolio showing shares held, cost, current value, maximum win, and unrealised P\&L.
2. **If liquidity is not available:** you will see "No price available for market order." Place a limit order at your target price and wait for a counterparty.

**Common Errors:**

| Error              | Cause                            | Fix                                     |
| ------------------ | -------------------------------- | --------------------------------------- |
| No price available | Orderbook is empty               | Try a limit order or wait for liquidity |
| Approval required  | Settlement currency not approved | Click Approve and retry                 |
