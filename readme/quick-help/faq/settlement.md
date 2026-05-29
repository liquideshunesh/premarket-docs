---
cover: ../../../.gitbook/assets/Default.png
coverY: 0
---

# Settlement FAQ

<details>

<summary><strong>Do I need to do anything at settlement?</strong></summary>

It depends on the market. Pre IPO, Pre TGE, Options, and RWA markets run on MegaETH and are auto expired and auto exercised at expiry. Proceeds are sent directly to your smart account and your portfolio updates automatically once settlement confirms onchain.

Prediction Markets and Yield Farm are the exception. They run on Solana through a liquidity partner. Once your position expires, you need to interact with the DFlow contract to burn your shares and bridge USDC back to your wallet. This step must be initiated manually.

RWA markets do not settle. There is no expiry. You exit by selling back into the orderbook.

</details>

<details>

<summary><strong>What is the resolution mechanism?</strong></summary>

The final settlement price is determined using a Time Weighted Average Price (TWAP) calculated over a 1 hour period around market expiry.

To reduce the impact of short term price spikes, manipulation, or exchange specific outages, Premarket uses pricing data from multiple sources, including:

* Centralized exchanges (CEXs)
* Decentralized exchanges (DEXs)
* Onchain oracle providers

The TWAP from these sources is aggregated to determine the final settlement price used for market resolution.

**Example:**\
If a market expires at 12:00 UTC, Premarket calculates a 1 hour TWAP using approved exchange and oracle data around expiry. The resulting price is used as the official settlement price for the market.

</details>

<details>

<summary><strong>How long does settlement take?</strong></summary>

Settlement typically completes within minutes of the expiry time, depending on onchain confirmation times.

</details>

<details>

<summary><strong>What happens if the outcome is ambiguous?</strong></summary>

Resolution follows the predefined rules for that market, which may rely on verified external sources. If the outcome cannot be determined fairly, the market may be cancelled and positions refunded.

</details>

<details>

<summary><strong>Can a market be cancelled after I have traded?</strong></summary>

Yes. Markets can be cancelled if fair resolution is not possible. In this case your position is refunded or settled at a neutral value.

</details>

<details>

<summary><strong>What oracle sources does Premarket use?</strong></summary>

For price based markets (Options, Pre TGE, Pre IPO), Premarket uses Bybit, Binance, Hyperliquid, and Chainlink as oracle sources.

</details>

<details>

<summary><strong>Why is my settlement payout less than I expected?</strong></summary>

For Options, Pre TGE, and Pre IPO markets, payout depends on where the final value lands relative to your band. If the settlement is near the edge of your band, the payout is reduced accordingly.

</details>

<details>

<summary><strong>Can I claim a payout manually?</strong></summary>

For MegaETH markets (Pre IPO, Pre TGE, Options), payouts are distributed automatically and you do not need to claim anything. For Solana markets (Prediction Markets, Yield Farm), you must redeem manually via the DFlow contract once your position expires.

</details>
