---
cover: ../../../.gitbook/assets/Default.png
coverY: 0
---

# Settlement FAQ

<details>

<summary><strong>Do I need to do anything at settlement?</strong></summary>

It depends on the product. Options-style MegaETH markets are cash-settled at expiry according to the market rules, and your portfolio updates once settlement confirms onchain.

Prediction Markets and Yield Farm run on Solana through DFlow. Once your position expires and resolves normally, you need to redeem manually through DFlow.

RWA markets do not settle. There is no expiry. You exit by selling back into the orderbook.

</details>

<details>

<summary><strong>What is the resolution mechanism?</strong></summary>

For token price options markets, the final settlement price can use oracle + TWAP rules over a defined period around market expiry.

To reduce the impact of short term price spikes, manipulation, or source-specific outages, market rules may use pricing data from approved sources, including:

* Centralized exchanges (CEXs)
* Decentralized exchanges (DEXs)
* Onchain oracle providers

The TWAP from approved sources is aggregated according to the market rules to determine the final settlement price used for market resolution.

**Example:**\
If a token price market expires at 12:00 UTC, the market rules may calculate a TWAP using approved exchange and oracle data around expiry. The resulting price is used as the official settlement price for that market.

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

Token price markets use oracle/TWAP from approved sources defined in the market rules. Pre TGE and Pre IPO markets use market-defined valuation sources. Always check the Rules tab for the exact source and fallback hierarchy.

</details>

<details>

<summary><strong>Why is my settlement payout less than I expected?</strong></summary>

For Options, Pre TGE, and Pre IPO markets, payout depends on where the final value lands relative to your spread. UP and DOWN split a combined value of $1. Inside the range, payout transitions linearly between the two sides.

</details>

<details>

<summary><strong>Can I claim a payout manually?</strong></summary>

For Solana markets (Prediction Markets, Yield Farm), you must redeem manually through DFlow once your position expires and resolves normally. For MegaETH options-style markets, follow the payout handling described in the market rules and Portfolio state after settlement confirms.

</details>
