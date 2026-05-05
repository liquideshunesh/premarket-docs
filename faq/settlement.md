# Settlement FAQ

**Do I need to do anything at settlement?**
No. All positions on Premarket are auto-expired and auto-exercised at expiry. Your portfolio balance updates automatically once settlement confirms on-chain.

**How long does settlement take?**
Settlement typically completes within minutes of the expiry time, depending on on-chain confirmation times.

**What happens if the outcome is ambiguous?**
Resolution follows the predefined rules for that market, which may rely on verified external sources. If the outcome cannot be determined fairly, the market may be cancelled and positions refunded.

**Can a market be cancelled after I have traded?**
Yes. Markets can be cancelled if fair resolution is not possible. In this case your position is refunded or settled at a neutral value.

**What oracle sources does Premarket use?**
For price-based markets, Premarket uses Bybit, Binance, Hyperliquid, and Chainlink as oracle sources.

**Why is my settlement payout less than I expected?**
For options and pre-TGE markets, payout depends on where the final value lands relative to your band. If the settlement is near the edge of your band, the payout is reduced accordingly.

**Can I claim a payout manually?**
All payouts are distributed automatically. You do not need to claim anything manually.
