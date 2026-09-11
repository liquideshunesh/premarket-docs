---
cover: .gitbook/assets/Wallets and Funds.png
coverY: 0
---

# Wallet and Funds

Trading through [app.premarket.xyz](https://app.premarket.xyz/) uses a smart account. Your funds flow from your personal wallet into the smart account for trading, and back out to your personal wallet when you withdraw.

Covered options use [robinhood.premarket.xyz](http://robinhood.premarket.xyz/) on Robinhood Chain. Account creation, wallet onboarding, and gas abstraction follow the same flow used for Premarket on MegaETH. Premiums are paid separately in USDG. Covered calls lock the underlying token as collateral; cash-secured puts lock USDG.

For a product overview of the account flow, see [Smart Account and 1-Click Trading](readme/getting-started/smart-account.md).

## How the Wallet Structure Works

| Layer          | Role                                                                                                                                          |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Primary Wallet | Your personal wallet (e.g. MetaMask for MegaETH, Phantom for Solana). Fully controlled by you. Used to deposit funds and receive withdrawals. |
| Smart Account  | Your trading wallet on Premarket. All trades, positions, and settlements happen here.                                                         |
| Subkey         | A delegated key used by the system to enable gas abstraction and transaction batching. You do not interact with this directly.                |

## How Funds Flow

```
Deposit:    Primary Wallet > Smart Account > Trade
Settlement: Position > Settled or Redeemable > Smart Account or manual redemption flow
Withdrawal: Smart Account > Primary Wallet
```

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption><p>Wallet view showing balances, smart account details, and funding actions.</p></figcaption></figure>

## Networks and Currencies

| Network | Trading or collateral asset | Markets                              |
| ------- | --------------------------- | ------------------------------------ |
| MegaETH | USDM                        | Pre IPO, Pre TGE, price spreads, RWA |
| Solana  | USDC                        | Prediction Markets, Yield Farm       |
| Robinhood Chain | USDG and supported underlying tokens | Covered calls and cash-secured puts |

In the main app, you hold balances by chain and product context in your smart account. Make sure you are depositing on the chain that matches the market you intend to trade. For covered options, use the account and balance views shown in the Robinhood Chain experience.

## How to Deposit in the Main App

1. Go to your Portfolio.
2. Select the token you want to deposit.
3. Enter the amount.
4. Click Approve if this is your first deposit of that token.
5. Click Deposit and confirm in your wallet.

For covered options, fund the smart account at [robinhood.premarket.xyz](http://robinhood.premarket.xyz/) with USDG for premiums. Writers also need the supported underlying token for covered calls or enough USDG to collateralize cash-secured puts. Complete the one-time vault operator approval before placing an order; without it, an order can be signed but cannot fill.

<figure><img src=".gitbook/assets/image (24).png" alt=""><figcaption><p>Funding smart wallet</p></figcaption></figure>

## How to Withdraw from the Main App

1. Go to your Portfolio and find the Withdraw section.
2. Select the token and enter the amount. You can only withdraw funds not locked in active positions.
3. Click Withdraw and confirm the transaction.

{% hint style="warning" %}
**Common issues:**

* Withdraw button disabled: your available balance is zero or all of your funds are locked in active positions.
* Funds not visible: you may have an open position that has not yet settled.
* Cannot withdraw full balance: part of your funds is locked in active positions.
{% endhint %}

<figure><img src=".gitbook/assets/image (25).png" alt=""><figcaption><p>Withdrawing from smart wallet</p></figcaption></figure>
