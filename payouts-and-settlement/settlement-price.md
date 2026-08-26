---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How Settlement Price is Determined

Settlement price is the final value applied to your position when a market resolves. It is not based on the last traded price. It is based on the rules defined for the market and verified external data sources.

## The Core Principle

| Concept          | Source           | Meaning                |
| ---------------- | ---------------- | ---------------------- |
| Market Price     | Order book       | What traders believe   |
| Settlement Price | Market rules     | What actually happened |

## Prediction Markets and Yield Farm

Prediction Markets are powered by DFlow, which tokenizes Kalshi markets on Solana. Settlement is rule based. No price feed or token oracle is required for the YES/NO outcome.

```
Event occurs
Outcome resolves according to the underlying market rules
Winning shares redeem for $1
Losing shares expire at $0
Manual redemption happens through DFlow
```

Yield Farm follows the same logic because it is a filtered view over prediction market legs.

## Token Price Options Markets

For token price options markets, settlement depends on the final value of the underlying asset at expiry. These markets can use oracle + TWAP rules. The exact sources, time window, and fallback hierarchy should be checked in the Rules tab for that market.

Do not use the last traded orderbook price as the settlement price.

## Covered Calls

Covered Calls use the final price of the underlying at expiry and the instrument's strike to divide the locked underlying between LONG and SHORT. Check the market rules shown in the [Robinhood Chain experience](http://robinhood.premarket.xyz/) for the exact price source, time window, and fallback hierarchy.

## Pre TGE Markets

For Pre TGE valuation spreads, settlement depends on the market-defined valuation source for the token's launch. The Rules tab should define how FDV is measured and which sources are used.

## Pre IPO Markets

For Pre IPO valuation spreads, settlement depends on the market-defined listing valuation source. The Rules tab should define the reference event, valuation calculation, and data source.

## RWA / Spot Markets

RWA/Spot Markets do not have an expiry-based settlement price. The value of the position is realised by selling or holding the asset, depending on the product and available orderbook liquidity.

## Settlement Flow

1. Market reaches expiry and trading stops.
2. The applicable market rules determine the reference outcome, price, or valuation.
3. The settlement formula is applied.
4. Positions update or become claimable according to the product flow once settlement confirms. Solana prediction markets require manual redemption through DFlow. Covered Call LONG and SHORT claims redeem or withdraw their respective shares of the underlying.

{% hint style="warning" %}
If data sources conflict or no reliable data is available, the market rules determine the fallback path. The market may be cancelled if it cannot resolve normally.
{% endhint %}
