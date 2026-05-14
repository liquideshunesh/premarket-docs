---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# How Pricing Works

Premarket uses an orderbook-based pricing system. There are no fixed odds or platform-set prices. Every price you see is the result of real buy and sell orders placed by other users.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>Orderbook</p></figcaption></figure>

## Price is Market Consensus

Each outcome has a price that reflects what the market collectively believes. A share trading at $0.25 implies a roughly 25% chance of that outcome occurring. A share at $0.80 implies 80%. This is not a guarantee, it is a live consensus estimate that updates as orders are placed and filled.

## How the Orderbook Sets the Price

Buyers place bids at the price they are willing to pay. Sellers place asks at the price they are willing to accept. A trade executes when a bid and ask match. The price you see in the UI is typically the last traded price or a derived market price based on recent activity.

> Screenshot: Orderbook showing bids and asks with spread highlighted

## The Bid and Ask Spread

There is usually a gap between the highest bid and the lowest ask. This is called the spread.

> **Example:** Best bid 24c, best ask 26c. The spread is 2c.

## Slippage

For larger trades, your order may consume multiple price levels in the orderbook. This means your average execution price may differ from the price displayed when you entered. This is called slippage.

{% hint style="warning" %}
Slippage is more common in large orders, thin orderbooks, and new markets with limited participants.
{% endhint %}

## Shares Calculation

```
Shares = Amount / Price
Example: $5 at $0.25 = 20 shares
Each correct share pays $1 at settlement.
```

## Common Issues:

<table><thead><tr><th width="366.4609375">Issue</th><th>Reality</th></tr></thead><tbody><tr><td>The displayed price is what you'll pay</td><td>Execution depends on available liquidity</td></tr><tr><td>Yes price + No price always equals 100%</td><td>They often don't, due to spread and orderbook structure</td></tr><tr><td>Small trades always get the exact displayed price</td><td>Not guaranteed in low liquidity conditions</td></tr></tbody></table>

Head to [How FDV Bands](fdv-bands.md) Work for a breakdown of how pricing applies to pre-TGE band markets.
