---
cover: .gitbook/assets/wallets-and-funds-new.png
coverY: 83.05176132278936
---

# Wallet and Funds

All trading on Premarket happens through a smart account. Your funds flow from your personal wallet into the smart account for trading, and back out to your personal wallet when you withdraw.

> Screenshot: Wallet page showing smart account balance and withdraw section

## How the Wallet Structure Works

| Layer          | Role                                                                                                                           |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Primary Wallet | Your personal wallet (e.g., MetaMask). Fully controlled by you. Used to deposit funds and receive withdrawals.                 |
| Smart Account  | Your trading wallet on Premarket. All trades, positions, and settlements happen here.                                          |
| Subkey         | A delegated key used by the system to enable gas abstraction and transaction batching. You do not interact with this directly. |

## How Funds Flow

```
Deposit:    Primary Wallet > Smart Account > Trade
Settlement: Position > Settled > Funds credited to Smart Account
Withdrawal: Smart Account > Primary Wallet
```

## How to Deposit

1. Go to the **Wallet** page.
2. Select the token you want to deposit.
3. Enter the amount.
4. Click **Approve** if this is your first deposit of that token.
5. Click **Deposit** and confirm in your wallet.

## How to Withdraw

1. Go to the **Wallet** page and find the **Withdraw** section.
2. Select the token and enter the amount. You can only withdraw funds not locked in active positions.
3. Click **Withdraw** and confirm the transaction.

{% hint style="warning" %}
**Common issues:**

* Withdraw button disabled: your available balance is zero or KYC is incomplete.
* Funds not visible: you may have an open position that has not yet settled.
* Cannot withdraw full balance: part of your funds is locked in active positions.
{% endhint %}
