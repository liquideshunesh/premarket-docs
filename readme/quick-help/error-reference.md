---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Error Reference

## Trading Errors

| Error                               | Cause                                                      | Fix                                                            |
| ----------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------- |
| No price available for market order | The orderbook is empty on the side you are trying to trade | Place a limit order at your target price or wait for liquidity |
| Approval required                   | You have not approved USDM for spending                    | Click Approve USDM in the trade panel and retry                |
| Insufficient balance                | Your smart account does not have enough USDM               | Deposit more USDM via the Wallet page                          |
| Transaction failed                  | Onchain transaction was rejected                           | Check your network connection and try again                    |

## Wallet Errors

| Error                        | Cause                                                        | Fix                                                           |
| ---------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------- |
| Withdraw button disabled     | Available balance is zero or KYC incomplete                  | Complete KYC or ensure funds are not locked in open positions |
| Funds not visible            | Open position not yet settled, or deposited on wrong network | Wait for settlement or check deposit network                  |
| Cannot withdraw full balance | Part of funds locked in active positions                     | Close or wait for active positions to settle                  |

## KYC Errors

| Error                                   | Cause                                                   | Fix                                                |
| --------------------------------------- | ------------------------------------------------------- | -------------------------------------------------- |
| Verification failed                     | Document not accepted or face verification unsuccessful | Retry with a different document or better lighting |
| Trading still locked after verification | Smart account not created or no funds deposited         | Complete remaining setup steps in Getting Started  |

{% hint style="info" %}
KYC is only required to trade prediction markets. If you are trading Pre-TGE, Options, Pre-IPO, or RWA markets, KYC is not required.
{% endhint %}

## Position Errors

| Error                             | Cause                                         | Fix                                                    |
| --------------------------------- | --------------------------------------------- | ------------------------------------------------------ |
| Sell button not visible           | You do not hold a position in this market     | Buy first before attempting to sell                    |
| Position still showing after sell | UI sync delay                                 | Refresh the page and wait for onchain confirmation     |
| Cannot unwind                     | You do not hold equal amounts of PRM and oPRM | Buy back the missing token before attempting to unwind |
