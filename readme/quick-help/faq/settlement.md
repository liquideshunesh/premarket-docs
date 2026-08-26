---
cover: ../../../.gitbook/assets/Default.png
coverY: 0
---

# Settlement FAQ

<details>

<summary><strong>Do I need to do anything at settlement?</strong></summary>

It depends on the product. Options-style MegaETH spread markets are cash-settled at expiry according to the market rules, and your portfolio updates once settlement confirms onchain. Covered Calls on Robinhood Chain settle in the underlying asset: LONG redeems the call payout and SHORT withdraws the remaining collateral.

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

Settlement in the main app typically completes within minutes of the expiry time, depending on onchain confirmation times. Covered Call settlement timing is not documented here.

</details>

<details>

<summary><strong>What happens if the outcome is ambiguous?</strong></summary>

Resolution follows the predefined rules for that market, which may rely on verified external sources. If the outcome cannot be determined fairly, the market may be cancelled and positions handled under its neutral settlement rules. A Covered Call marked with a null outcome splits the locked collateral equally between LONG and SHORT.

</details>

<details>

<summary><strong>Can a market be cancelled after I have traded?</strong></summary>

Yes. Markets can be cancelled if fair resolution is not possible. In this case your position is handled under the product's neutral settlement rules. A Covered Call marked with a null outcome splits the locked collateral equally between LONG and SHORT.

</details>

<details>

<summary><strong>What oracle sources does Premarket use?</strong></summary>

MegaETH token price spread markets use oracle/TWAP from approved sources defined in the market rules. Pre TGE and Pre IPO markets use market-defined valuation sources. For Covered Calls, check the market rules for the exact final price source and fallback hierarchy.

</details>

<details>

<summary><strong>Why is my settlement payout less than I expected?</strong></summary>

For MegaETH Options, Pre TGE, and Pre IPO spread markets, payout depends on where the final value lands relative to your spread. LONG and SHORT split a combined value of $1. Inside the range, payout transitions linearly between the two sides.

Covered Calls use a different payout. They divide one locked unit of the underlying between LONG and SHORT according to the final price and strike.

</details>

<details>

<summary><strong>Can I claim a payout manually?</strong></summary>

For Solana markets (Prediction Markets, Yield Farm), you must redeem manually through DFlow once your position expires and resolves normally. For MegaETH options-style markets, follow the payout handling described in the market rules and Portfolio state after settlement confirms. For Covered Calls, LONG redeems its share of the underlying and SHORT withdraws the remainder after expiry settlement.

</details>
