---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Smart Account and 1-Click Trading

Premarket uses a smart account as the trading account that holds balances, positions, open orders, and claimable settlement proceeds. It is designed to make the trading flow smoother after you have created the account, deposited funds, and set the required permissions.

{% hint style="info" %}
This page describes the account flow at [app.premarket.xyz](https://app.premarket.xyz/). Covered options use [robinhood.premarket.xyz](http://robinhood.premarket.xyz/) on Robinhood Chain with the same smart-account onboarding and gas-abstraction flow used on MegaETH.
{% endhint %}

## Account Creation

Users can create a trading account through social login and simplified wallet onboarding. After setup, your smart account is the account used for trading, deposits, balances, and portfolio management inside Premarket.

## 1-Click Trading

The smart account allows a smoother trading flow after funds are deposited and permissions are set. Instead of signing every trading step manually, the smart account can support faster order placement and portfolio updates through the permissions configured during onboarding.

## Deposits

Users can deposit supported currencies and assets into the smart account. This includes USDM for MegaETH markets, USDC for Solana prediction markets where relevant, supported spot/RWA assets if available for deposit and trading, and USDG for covered-option premiums on Robinhood Chain. Covered-call writers also need the supported underlying token, while cash-secured-put writers use USDG as collateral.

Covered-option users must complete a one-time vault operator approval. Without it, an order can be signed but cannot fill.

Always check that you are depositing the asset and network supported by the product you want to trade.

## Portfolio

Positions, open orders, balances, and claimable settlements are managed from the smart account. Use the Portfolio page to review active positions, pending orders, available balances, and withdrawal options.

## Security Expectations

The smart account is designed to simplify the trading experience, but users should still understand approvals, balances, and the withdrawal flow before depositing funds. Do not approve transactions or permissions you do not understand.

For the full setup flow, see [Getting Started](setup.md). For deposits and withdrawals, see [Wallet and Funds](../../wallet-and-funds.md).
