---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Getting Started

Setting up on Premarket takes a few steps before you can place your first trade. You may need to verify your identity (only for Prediction Markets and Yield Farm), create a smart account, and deposit funds. This page walks you through each step in order.

## Step 1: Access the App

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption><p>Premarket application homepage</p></figcaption></figure>

Use [app.premarket.xyz](https://app.premarket.xyz/) for Premarket on MegaETH and Solana. For Covered Calls, use [robinhood.premarket.xyz](http://robinhood.premarket.xyz/). Covered Calls are part of Premarket; the separate entry point exists because that experience is deployed on Robinhood Chain.

{% hint style="info" %}
The remaining account setup steps describe the main Premarket app. Covered Calls on Robinhood Chain use the same smart-account onboarding and gas-abstraction flow as Premarket on MegaETH. Fund the account with the supported underlying token for the Covered Call you want to trade.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Premarket app entry</p></figcaption></figure>

## Step 2: Complete Identity Verification (Prediction Markets and Yield Farm only)

Prediction Markets and Yield Farm use DFlow/Kalshi market infrastructure that requires identity verification. You can start verification in two ways: click Buy Yes or Buy No on any prediction market, or go to your Portfolio and click Verify Identity. Either path redirects you to the identity verification provider. Submit a government issued ID and complete face verification if prompted. Once done, return to the app and your account will be enabled for trading.

{% hint style="info" %}
Identity verification is only required for Prediction Markets and Yield Farm in the main app. If you only trade Pre IPO, Pre TGE, MegaETH price spreads, RWA markets, or Covered Calls, skip this step and continue to Step 3. Covered Calls do not require KYC.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Identity verification prompt shown before trading Prediction Markets or Yield Farm.</p></figcaption></figure>

## Step 3: Create Your Smart Account

Premarket uses a smart account as your trading wallet. Your funds flow from your personal wallet (Primary Wallet) into your smart account for trading, and back out when you withdraw. A subkey is delegated by the system to enable gas abstraction and transaction batching, so you can trade without signing every transaction manually.

Open your Portfolio, where your smart account is set up automatically, and wait for confirmation. All your funds, trades, and positions are managed through this account. You can export your subkey private key at any time from your Portfolio for self custody.

For more detail on how the account works, see [Smart Account and 1-Click Trading](smart-account.md) and [Wallet and Funds](../../wallet-and-funds.md).

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Portfolio view showing smart account setup</p></figcaption></figure>

## Step 4: Deposit Funds

Once your smart account is created, click Deposit and send supported assets to your smart account. Wait for your balance to update before placing a trade.

Make sure you are depositing on the correct network for the product you want to trade:

| Network | Markets                              | Trading or collateral asset |
| ------- | ------------------------------------ | --------------------------- |
| MegaETH | Pre IPO, Pre TGE, price spreads, RWA | USDM                        |
| Solana  | Prediction Markets, Yield Farm       | USDC                        |
| Robinhood Chain | Covered Calls                | Supported underlying asset  |

Depositing on the wrong network means your funds will not be available for the market you want to trade.

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Deposit flow showing asset </p></figcaption></figure>

## Step 5: Place Your First Trade

Go to any active market and select an outcome. For Prediction Markets and Yield Farm, choose Buy Yes or Buy No. For Pre IPO, Pre TGE, and Options spread markets, select the spread and choose LONG or SHORT. For RWA markets, select the asset and place a buy order. For Covered Calls, review the underlying, strike, expiry, collateral, and premium before choosing the LONG or SHORT role. See [How to Use a Covered Call](../../walkthroughs/covered-call.md) for the supported lifecycle.

## Step 6: Manage Your Position

After placing a trade in the main app, track it in your Portfolio. You can monitor price changes and exit early by selling your position before settlement, provided there is liquidity available on the other side. For Covered Calls, sell a LONG or SHORT position through the orderbook, or unwind equal LONG and SHORT amounts back into the underlying token.

If you hold to expiry, settlement depends on the market type. Options-style MegaETH markets are cash-settled according to their market rules. Covered Calls on Robinhood Chain divide the locked underlying between LONG and SHORT. Prediction Markets and Yield Farm run on Solana and require a manual redemption step through DFlow once your position expires. RWA markets do not have expiry-based settlement; you realise value by selling or holding the asset. See [Receiving Your Payout](../../payouts-and-settlement/receiving-payout.md) for details.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Active Portfolio</p></figcaption></figure>

If you have completed these steps and want to learn more, check out these pages:

* [Understanding Markets](../../understanding-markets/) for walkthroughs on market types and mechanics.
* [Quick Help](../quick-help/) if you need assistance or are stuck on one of the steps above.
* [Smart Account and 1-Click Trading](smart-account.md) if you want more detail on deposits, balances, and portfolio management.
* [Identity Verification](setup.md#step-2-complete-identity-verification-prediction-markets-and-yield-farm-only) if you want assistance with the verification step.
