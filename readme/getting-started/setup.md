---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Getting Started

Setting up on Premarket takes a few steps before you can place your first trade. You may need to verify your identity (only for Prediction Markets and Yield Farm), create a smart account, and deposit funds. This page walks you through each step in order.

## Step 1: Access the App

Go to [app.premarket.xyz](https://app.premarket.xyz) and navigate to the Markets section. You can browse active markets without any setup, but placing a trade requires completing the steps below.

## Step 2: Complete Identity Verification (Prediction Markets and Yield Farm only)

Prediction Markets and Yield Farm route through a liquidity partner that requires identity verification. You can start verification in two ways: click Buy Yes or Buy No on any prediction market, or go to your Portfolio and click Verify Identity. Either path redirects you to the identity verification provider. Submit a government issued ID and complete face verification if prompted. Once done, return to the app and your account will be enabled for trading.

{% hint style="info" %}
Identity verification is only required for Prediction Markets and Yield Farm. If you only trade Pre IPO, Pre TGE, Options, or RWA markets, skip this step and continue to Step 3.
{% endhint %}

## Step 3: Create Your Smart Account

Premarket uses a smart account as your trading wallet. Your funds flow from your personal wallet (Primary Wallet) into your smart account for trading, and back out when you withdraw. A subkey is delegated by the system to enable gas abstraction and transaction batching, so you can trade without signing every transaction manually.

Open your Portfolio, where your smart account is set up automatically, and wait for confirmation. All your funds, trades, and positions are managed through this account. You can export your subkey private key at any time from your Portfolio for self custody.

For more detail on how the wallet structure works, see [Wallet and Funds](../../wallet-and-funds.md).

## Step 4: Deposit Funds

Once your smart account is created, click Deposit and send supported assets to your smart account. Wait for your balance to update before placing a trade.

Make sure you are depositing on the correct network for the product you want to trade:

| Network | Markets | Currency |
| --- | --- | --- |
| MegaETH | Pre IPO, Pre TGE, Options, RWA | USDM |
| Solana | Prediction Markets, Yield Farm | USDC |

Depositing on the wrong network means your funds will not be available for the market you want to trade.

## Step 5: Place Your First Trade

Go to any active market and select an outcome. For Prediction Markets and Yield Farm, choose Buy Yes or Buy No. For Pre IPO, Pre TGE, and Options spread markets, select the spread and choose Up or Down. For RWA markets, select the asset and place a buy order. Enter an amount, review the price and potential payout, then place your order to execute.

## Step 6: Manage Your Position

After placing a trade, track it in your Portfolio. You can monitor price changes and exit early by selling your position before settlement, provided there is liquidity available on the other side.

If you hold to expiry, settlement depends on the market type. Pre IPO, Pre TGE, Options, and RWA markets settle automatically to your smart account. Prediction Markets and Yield Farm run on Solana and require a manual redemption step via the DFlow contract once your position expires. See [Receiving Your Payout](../../payouts-and-settlement/receiving-payout.md) for details.

If you have completed these steps and want to learn more, check out these pages:

* [Understanding Markets](../../understanding-markets/) for walkthroughs on market types and mechanics.
* [Quick Help](../quick-help/) if you need assistance or are stuck on one of the steps above.
* [Identity Verification](setup.md#step-2-complete-identity-verification-prediction-markets-and-yield-farm-only) if you want assistance with the verification step.
