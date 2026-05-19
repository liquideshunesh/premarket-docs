---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How to Mint and Sell an Options Position

This walkthrough covers the full lifecycle of an options position from minting through selling on the orderbook. Most users buy oPRM directly from the orderbook without minting. Minting is the path for users who want to write a position (provide the option and collect the premium).

## Step 1: Select a Band

Go to Markets, filter for Options, and open an active market (BTC/USD Spreads, ETH/USD Spreads, MEGA/USD Spreads, XAU/USD, XAG/USD, or CL/USD). Select the price band that matches your view on where the underlying will settle at expiry.

## Step 2: Mint Your Position

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>Mint position pair with band</p></figcaption></figure>

1. Click Mint on your chosen band.
2. Enter the amount of USDM you want to deposit as collateral.
3. Confirm the transaction.
4. You receive two tokens: PRM (write position) and oPRM (outcome token).

## Step 3: View Your Tokens in Portfolio

Go to Portfolio. You will see both your PRM and oPRM tokens listed with their current values.

## Step 4: Sell Your oPRM Tokens

1. Go to the market orderbook for your band.
2. Place a limit sell order for your oPRM tokens at your target price.
3. Wait for a buyer to match your order.
4. Once filled, you receive USDM as the premium.

{% hint style="info" %}
After selling your oPRM tokens, you hold only PRM tokens. At expiry, if the band is out of the money, you receive your full collateral back automatically via the PRM token. If in the money, the PRM holder's collateral covers the payout to the oPRM holder.
{% endhint %}
