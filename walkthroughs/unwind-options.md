---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Unwind an Options Position

Unwinding lets you exit an options position before expiry and recover your full collateral, provided you hold equal amounts of both PRM and oPRM tokens.

{% hint style="warning" %}
You can only unwind if you hold both PRM and oPRM tokens in equal amounts. If you have already sold your oPRM tokens, you must buy them back first.
{% endhint %}

## When to Unwind

* You want to exit before expiry without relying on a buyer in the orderbook.
* You hold both PRM and oPRM tokens and want your collateral back immediately.
* The market has moved and you want to redeploy capital elsewhere.

## How to Unwind

1. Go to your **Portfolio** and locate the options position you want to exit.
2. Confirm you hold equal amounts of PRM and oPRM for that position.
3. Click **Unwind** or **Withdraw** on the position.
4. Confirm the transaction.
5. Your full collateral is returned to your smart account in USDM.

## Example

```
You minted a position depositing $2,400 USDM collateral.
Received 1 PRM and 1 oPRM token.
Sold the oPRM for $50 premium.
Bought back the oPRM for $60 (net -$10).
Now hold 1 PRM and 1 oPRM.
Unwind: receive $2,400 collateral back.
Net result: -$10 on the premium trade, full collateral recovered.
```

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption><p>Unwind to collateral</p></figcaption></figure>

{% hint style="success" %}
Unwinding always returns your full original collateral regardless of market price, as long as you hold both tokens.
{% endhint %}
