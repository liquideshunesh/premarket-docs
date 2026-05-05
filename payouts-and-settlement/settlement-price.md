# How Settlement Price is Determined

Settlement price is the final value applied to your position when a market resolves. It is not based on the last traded price. It is based on the rules defined for the market and verified external data sources.

## The Core Principle

| Concept | Source | Meaning |
|---------|--------|---------|
| Market Price | Order book | What traders believe |
| Settlement Price | Rules and Oracle | What actually happened |

## For Prediction Markets

Settlement is rule-based. No price feed or oracle is required.

```
Event occurs
Outcome verified via official source
Smart contract assigns $1 to winner, $0 to loser
```

## For Price-Based Markets

For options and pre-TGE markets, settlement depends on the final price of the underlying asset at expiry, obtained via oracle.

**Oracle sources:** Bybit, Binance, Hyperliquid, Chainlink.

## Settlement Flow

1. Market reaches expiry and trading stops.
2. Oracle fetches final reference price.
3. Market rules are applied.
4. Smart contracts compute and distribute payouts.
5. Positions update in your Portfolio automatically.

{% hint style="warning" %}
If data sources conflict, a predefined hierarchy determines which source wins. If no reliable data is available, the market may be cancelled and positions refunded.
{% endhint %}
