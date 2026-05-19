---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Trade a Yield Farm Position

This walkthrough covers buying a high probability leg on the Yield Farm view, holding to settlement, and redeeming your payout.

## Step 1: Open the Yield Farm View

Go to Markets and select the Yield Farm category. The view lists outcome legs from active Prediction Markets that are trading below $1 at high implied probability.

## Step 2: Sort and Filter

Sort by APR if you want the highest annualised yield, or by expiry if you want the shortest time to settlement. Each row shows the underlying market, the YES or NO leg, entry price, yield to settlement, APR, expiry, and available liquidity.

## Step 3: Read the Underlying Market Rules

Click the underlying market to open the full Prediction Market page. Read the Rules tab carefully. Yield Farm surfaces these legs as high probability bets but the resolution criteria still determine whether your leg pays out.

## Step 4: Place Your Trade

1. Confirm there is liquidity at your target entry price.
2. Select Buy on the leg.
3. Enter the amount of USDC you want to spend.
4. Review shares and the implied yield at settlement.
5. Confirm the trade.

## Step 5: Hold to Settlement

Yield Farm positions are designed to be held. Profit is realised when the underlying market settles and your leg resolves at $1. You can still sell back into the orderbook before expiry if you change your view, subject to available liquidity.

## Step 6: Redeem Your Payout

Yield Farm runs on Solana through a liquidity partner. Once the underlying market settles, redeem manually by interacting with the DFlow contract. This burns your shares and bridges the USDC payout back to your wallet.

{% hint style="warning" %}
A high implied probability is not a guarantee. A leg trading at 95¢ can still resolve at $0. Treat Yield Farm as a yield wrapper over Prediction Markets, with the same risk profile.
{% endhint %}
