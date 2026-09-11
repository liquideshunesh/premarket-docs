---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Covered Options

Covered options are part of Premarket's Options Markets. The experience is available at [robinhood.premarket.xyz](http://robinhood.premarket.xyz/) because it is deployed on Robinhood Chain. It is another entry point to Premarket, not a separate application or product.

The current covered-options flow supports covered calls and cash-secured puts. Each position is fully backed by collateral, so there is no margin engine or liquidation.

## How the Position Works

Each option is represented by two transferable position tokens created from fixed collateral:

| Position | What it represents |
| --- | --- |
| Option leg | Receives the option payout at settlement. The interface labels this **Long** for calls and **Short** for puts. |
| LP leg | Receives the locked collateral that remains after the option payout. This is the writer side for both calls and puts. |

For a covered call, the collateral is the underlying token, such as AAPL. For a cash-secured put, the collateral is USDG. The two settlement payouts always add up to the collateral locked for the position.

The quoted premium is a separate USDG payment between traders. It is not part of the locked collateral and is not deducted from the settlement payout.

{% hint style="info" %}
The LP position carries the writer's collateral rights and settlement exposure. If the LP token changes hands, those rights and obligations move with it.
{% endhint %}

## Reading the Market

Covered-option markets appear under the **Options** view. Select an underlying, then use the option chain to:

* Switch between **Call** and **Put**.
* Choose an expiry.
* Compare strikes, bid and ask premiums, LP APR, and the displayed mark.
* Select a strike to open its trade ticket.
* Expand a strike to review the Order Book, Live Trades, Orders, History, and Positions.
* Use **Details** to review contract terms and **Builder** to inspect the displayed payoff for a selected position.

The mark is a reference value. Your actual premium is determined by the orderbook price at which your order fills.

The supplied market view shows CASHCAT, STONKBROKER, AAPL, AMZN, TSLA, and NVDA. Use the live market selector for the current list of supported underlyings and available expiries.

## Trading Actions

The trade ticket separates the option leg from the LP leg.

| Selected leg | Action | Result |
| --- | --- | --- |
| Long on a call or Short on a put | **Buy** | Pay a USDG premium to open or add to the option position. |
| Long on a call or Short on a put | **Sell** | Sell an option position you already hold and receive a USDG premium. |
| LP | **Write** | Lock the required collateral and receive a USDG premium when the order fills. |
| LP | **Burn** | Buy back the option exposure attached to your LP position, return the LP token, and unlock the full collateral. |

Both legs trade through the same premium orderbook. **Sell** and **Write** orders rest as asks; **Buy** and **Burn** orders rest as bids. A **Buy** order can fill against a writer creating a new covered position or a holder selling an existing option position.

An option buyer's maximum loss is the USDG premium paid. A writer receives the premium when the order fills, while the required collateral remains locked until expiry or a completed Burn.

## Before You Start

* Connect at [robinhood.premarket.xyz](http://robinhood.premarket.xyz/). Account creation, wallet onboarding, and gas abstraction follow the same flow as Premarket on MegaETH.
* Deposit USDG to pay premiums for buy-side orders.
* To write a covered call, hold the underlying token required as collateral.
* To write a cash-secured put, hold the required USDG collateral.
* Cash-secured puts require supported stablecoins for both collateral and settlement; the current flow uses USDG.
* Complete the one-time vault operator approval. An order can be signed without this approval, but it cannot fill.
* Review the option type, underlying, strike, expiry, order type, premium, and size before confirming.

Covered options do not require KYC. Geographic availability is not specified in this guide.

## Minting a Position Pair

The **Mint** position tool lets you create both legs directly:

1. Select the option contract.
2. Deposit its required collateral.
3. Receive equal amounts of the option leg and LP leg.

For example, minting one pair of the AAPL call shown in the interface deposits `1 AAPL` and creates one option position and one LP position. You can then:

* Sell the option leg to receive its premium and keep the LP writer position.
* Sell the LP leg and keep the option position.
* Keep both legs and unwind them later.

Minting does not itself pay a premium. Premium changes hands only when an order fills.

## Unwinding to Collateral

If you hold equal amounts of the option and LP legs for the same strike and expiry, use **Unwind** to burn the pair and redeem the associated collateral.

Unwinding returns the full collateral for the paired amount. It does not add or subtract premiums previously paid or received. If you hold only one leg, you must acquire the matching leg before you can unwind directly.

## Open Orders and Cancellation

Orders are signed offchain and remain open until they fill, reach their selected order expiry, or you cancel them. The interface currently offers `1h`, `24h`, `7d`, and `30d` order expiries.

Cancelling an unmatched order is free and immediate. If Premarket upgrades the exchange, an order signed for the previous exchange version may no longer fill; cancel it and create a new order.

## Exiting Before Expiry

Your exit depends on the leg you hold:

* Use **Sell** to close an option position through the orderbook.
* Use **Burn** to close an LP writer position and unlock its collateral.
* Use **Unwind** if you hold equal option and LP amounts and want to redeem the collateral directly.

Orderbook exits require matching liquidity. An unmatched exit order remains open until its order expiry or cancellation.

## Covered Call Settlement

Let `F` be the final price and `K` the strike for a call backed by one unit of its underlying token.

| Final price | Long option payout | LP payout |
| --- | --- | --- |
| At or below `K` | `0` underlying | `1` underlying |
| Above `K` | `(F - K) / F` underlying | `K / F` underlying |

For example, assume one AAPL is locked for a covered call with a `$250` strike:

| Final AAPL price | Long receives | LP receives |
| --- | --- | --- |
| `$250` | `0 AAPL` | `1 AAPL` |
| `$300` | `0.1667 AAPL`, worth `$50` | `0.8333 AAPL`, worth `$250` |
| `$500` | `0.5 AAPL`, worth `$250` | `0.5 AAPL`, worth `$250` |
| `$2,500` | `0.9 AAPL`, worth `$2,250` | `0.1 AAPL`, worth `$250` |

The premium is paid separately in USDG. Include the premium paid or received when calculating each trader's net result.

## Cash-Secured Put Settlement

For a cash-secured put with a `$250` strike, `$250` of USDG collateral backs each full position:

| Final underlying price | Short option payout | LP payout |
| --- | --- | --- |
| `$0` | `250 USDG` | `0 USDG` |
| `$125` | `125 USDG` | `125 USDG` |
| At or above `$250` | `0 USDG` | `250 USDG` |

The option leg is labelled **Short** because its payout increases as the underlying settles below the strike. The writer side remains **LP**.

## If No Final Price Is Available

If the oracle does not provide a final price and the market uses its fallback outcome, the option and LP legs each receive half of the locked collateral.

For a step-by-step trading flow, see [How to Trade Covered Options](../walkthroughs/covered-call.md).
