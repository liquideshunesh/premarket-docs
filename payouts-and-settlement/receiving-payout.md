---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Receiving Your Payout

After a market settles, your position has a fixed value. How you receive your payout depends on which product you traded.

## Prediction Markets

Prediction markets run on Solana and are powered by DFlow, which tokenizes Kalshi markets on Solana. Settlement is not automatic. Once your position expires and the market resolves normally, you need to redeem manually through DFlow. Winning shares redeem for $1 and losing shares expire at $0.

## Yield Farm

Yield Farm positions run on Solana and use the same prediction market settlement flow. Yield Farm is a view over prediction market legs, not a separate product. Once your position expires and resolves normally, redeem manually through DFlow.

## Pre IPO and Pre TGE Markets

Pre IPO and Pre TGE markets run on MegaETH when listed as options-style valuation spreads. Payout depends on where the market-defined valuation lands relative to your strike range. LONG and SHORT split a combined value of $1 at settlement.

## Options Markets

Price spread options markets run on MegaETH. LONG behaves like exposure to a call spread. SHORT behaves like exposure to a put spread. If the final settlement price is above the upper strike, LONG receives $1 and SHORT receives $0. If the final settlement price is below the lower strike, SHORT receives $1 and LONG receives $0. Inside the range, payout transitions linearly between the two sides.

Settlement proceeds are reflected according to the market rules once settlement confirms.

## Covered Options

Covered options run on Robinhood Chain. A covered call's Long option leg and LP leg divide the locked underlying token. At or below the strike, Long receives nothing and LP receives the full underlying. Above the strike, Long redeems `(final price - strike) / final price` units of the underlying and LP receives the remainder.

A cash-secured put's Short option leg and LP leg divide its locked USDG. Below the strike, Short receives the put payout and LP receives the remainder. At or above the strike, LP receives the full collateral.

Before expiry, use **Sell** to close an option position or **Burn** to close an LP writer position when liquidity is available. A holder with equal option and LP amounts for the same contract can **Unwind** the pair back into its collateral.

## RWA / Spot Markets

RWA markets do not settle. There is no expiry and no automatic redemption. To realise profit or loss, sell back into the orderbook. Proceeds are credited to your smart account in USDM.

## Common Issues

| Issue                             | Cause                                         | Fix                                 |
| --------------------------------- | --------------------------------------------- | ----------------------------------- |
| Nothing happened after settlement | Blockchain confirmation delay                 | Wait a few minutes and refresh      |
| Cannot withdraw                   | Funds are still locked in an active position  | Close or wait for the position      |
| Zero payout                       | Position resolved out of the money            | Expected outcome, no action needed  |
| Solana position not auto credited | Manual redemption required via DFlow          | Initiate redemption on the position |
| Covered-option payout differs from `$1` spread | Covered options divide their locked collateral | Check the option type, strike, and final price |
