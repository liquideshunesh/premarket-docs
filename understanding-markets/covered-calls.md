---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Covered Calls

Covered Calls are part of Premarket's Options Markets. The experience is available at [robinhood.premarket.xyz](http://robinhood.premarket.xyz/) because it is deployed on Robinhood Chain. It is another entry point to Premarket, not a separate application or product.

## What is a Covered Call?

A Covered Call lets a holder lock an underlying asset and sell the LONG claim on price gains above a chosen strike. The premium provides value to the SHORT side when the LONG claim changes hands, while the locked underlying fully backs the position.

Premarket Covered Calls settle in the underlying asset. They do not use the `$1` LONG/SHORT payout model used by Premarket's MegaETH spread markets.

## Roles

| Role | What the position represents |
| --- | --- |
| Position creator | Locks the underlying and receives equal LONG and SHORT claims |
| LONG holder | Holds the call payoff above the strike |
| SHORT holder | Holds the locked collateral minus the LONG payout |

Creating the pair is direction-neutral. A typical covered call writer keeps the SHORT claim and sells the LONG claim to collect the quoted premium. The obligation follows the SHORT claim, not the person who originally created the position. Transferring the SHORT claim transfers that obligation with it.

## Reading the Market

Covered Call markets appear under the **Options** tab. A market card identifies the underlying, available expiry, strike rows, and any quoted LONG or SHORT prices. A dash means no price is currently displayed for that side.

Inside a market, the price history shows the current spot price when available and marks the selected strike as the target. Use the option chain to review the instrument:

* Choose an expiry tab.
* Compare the available strikes.
* Review the quoted LONG price, SHORT price, and displayed max payout for each strike.
* Select a strike to open its trade panel and expanded market details.
* Use the Order Book, Live Trades, Orders, History, Positions, and Chart tabs to review activity for the selected instrument.

The orderbook displays price, size, and total value. Available prices and sizes can differ between LONG and SHORT.

## Supported Underlyings

The current Covered Call market view includes:

* AAPL
* AMZN
* CASHCAT
* NVDA
* STONKBROKERS
* TSLA

Check the **Options** tab for the strikes and expiries available for each underlying.

## Before You Start

* Open the Covered Call experience at [robinhood.premarket.xyz](http://robinhood.premarket.xyz/).
* Account creation, wallet onboarding, and gas abstraction follow the same flow used for Premarket on MegaETH.
* Covered Calls do not require KYC.
* Confirm the underlying asset, strike, expiry, and settlement rules for the instrument.
* To create one full position, have one unit of the underlying available for each position you want to create.
* Review the selected side's quote, your available underlying balance, fees, and transaction details. The premium and any fees are paid in the underlying token. The fee rate is not documented here.

## Position Lifecycle

1. A position creator locks one unit of the underlying per position.
2. The position creates equal LONG and SHORT claims.
3. The LONG claim can pass to a buyer for the quoted premium. The covered call writer normally keeps the SHORT claim.
4. The underlying remains locked as collateral for the two claims.
5. At expiry, the market's final price is compared with the strike.
6. The LONG holder redeems the call payout. The SHORT holder withdraws the remaining underlying. Together, the two payouts equal the underlying locked for the position.

{% hint style="info" %}
If the selected side has no liquidity, the trade panel shows **No liquidity on this side** and the order cannot be confirmed as a Market order.
{% endhint %}

## Open Orders and Cancellation

An unmatched order remains in the orderbook until it reaches its expiry or you cancel it.

## Exit or Unwind Before Expiry

You can exit a LONG or SHORT position by selling it through the orderbook. The order must match available liquidity before the sale executes.

If you hold equal amounts of LONG and SHORT for the same strike and expiry, you can unwind those paired claims back into the underlying token. Only the matched LONG and SHORT amount can be unwound.

## Settlement

Let `F` be the final settlement price and `K` the strike price for a position backed by one unit of the underlying.

| Final price | LONG payout | SHORT payout |
| --- | --- | --- |
| At or below the strike | `0` underlying | `1` underlying |
| Above the strike | `(F - K) / F` underlying | `K / F` underlying |

The payouts are made in the underlying asset and always add up to the one unit originally locked. There is no margin engine or liquidation step for this flow.

## Example

Assume a Covered Call has a `$250` strike and one AAPL is locked as collateral.

| Final AAPL price | LONG receives | SHORT receives |
| --- | --- | --- |
| `$250` | `0 AAPL` | `1 AAPL` |
| `$300` | `0.1667 AAPL`, worth `$50` | `0.8333 AAPL`, worth `$250` |
| `$500` | `0.5 AAPL`, worth `$250` | `0.5 AAPL`, worth `$250` |

The LONG holder also subtracts the premium paid when calculating net profit. The SHORT holder adds the premium received. Premiums vary and are not part of the expiry payout formula, so use the quoted premium to calculate each side's net result.

## Null Outcome

If the market has no final price and is marked with a null outcome, each claim receives half of the locked collateral. For a position backed by one unit of the underlying, LONG receives `0.5` and SHORT receives `0.5` of that asset.

## Important Behaviors

* The position is fully collateralised with the underlying. It is not a naked call.
* Collateral follows the claim. Selling the SHORT claim transfers the short obligation.
* Small differences can arise from conservative rounding when collateral and liabilities are calculated.
* Selling a LONG or SHORT position depends on orderbook liquidity. Unwinding equal LONG and SHORT amounts returns the paired collateral in the underlying token.

For the lifecycle in checklist form, see [How to Use a Covered Call](../walkthroughs/covered-call.md).
