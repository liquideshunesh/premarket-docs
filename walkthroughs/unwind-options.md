---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Unwind an Options Position

Unwinding lets you exit an options position before expiry and recover your collateral. In most cases this happens automatically: when you sell on the orderbook and match an opposite sell, the positions merge and your collateral is released (merge match). You only need the manual unwind below if you hold both sides of a spread and want to recover collateral directly without a counterparty.

{% hint style="warning" %}
You can only unwind directly if you hold both LONG and SHORT tokens in equal amounts. If you have already sold one side, you must buy it back first.
{% endhint %}

## When to Unwind

* You want to exit before expiry without relying on a buyer in the orderbook.
* You hold both LONG and SHORT tokens and want your collateral back immediately.
* The market has moved and you want to redeploy capital elsewhere.

## How to Unwind

1. Go to your Portfolio and locate the options position you want to exit.
2. Confirm you hold equal amounts of LONG and SHORT for that position.
3. Click Unwind or Withdraw on the position.
4. Confirm the transaction.
5. Your full collateral is returned to your smart account in USDM.

## Example

```
You minted a position depositing $2,400 USDM collateral.
Received 1 LONG and 1 SHORT token.
Sold the LONG for $50 premium.
Bought back the LONG for $60 (net loss of $10).
Now hold 1 LONG and 1 SHORT.
Unwind: receive $2,400 collateral back.
Net result: $10 loss on the premium trade, full collateral recovered.
```

{% hint style="success" %}
Unwinding always returns your full original collateral regardless of market price, as long as you hold both tokens.
{% endhint %}
