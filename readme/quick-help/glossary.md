---
cover: ../../.gitbook/assets/Default.png
coverY: 0
---

# Glossary

## General

| Term | Definition |
| --- | --- |
| **Market** | A trading environment for a specific asset, event, or instrument |
| **Order Book** | List of active buy (bids) and sell (ask) orders in a market |
| **Liquidity** | The availability of buyers and sellers in a market |
| **Maker** | A trader who places an order that adds liquidity to the order book |
| **Taker** | A trader who matches an existing order and removes liquidity from the orderbook |
| **Spread** | The difference between the highest bid and the lowest ask in an orderbook |
| **Slippage** | The difference between the expected and the actual execution price |

## Trading

| Term | Definition |
| --- | --- |
| **Buy Order** | An instruction to purchase an asset or outcome |
| **Sell Order** | An instruction to sell an asset or outcome |
| **Market Order** | An instruction to buy or sell immediately at the best available price |
| **Limit Order** | An instruction to buy or sell only at a specified price |
| **Position** | An active holding in a market |
| **Position History** | A record of past trades and closed positions |

## Prediction Markets and Yield Farm

| Term | Definition |
| --- | --- |
| **Outcome** | A possible result of an event, for example YES or NO |
| **Outcome Token** | A token representing a position in a specific outcome. Settles to $1 if correct and $0 if incorrect |
| **Settlement** | The final resolution of a market based on the real world result |
| **Payout** | The amount received after settlement |
| **Implied Probability** | The market price interpreted as roughly pricing an outcome, before fees, spreads, and liquidity conditions. A price of $0.25 can be read as roughly 25% |
| **Yield (Yield Farm)** | The spread between the entry price and $1, representing the return if the leg resolves correctly |

## Pre TGE and Pre IPO Markets

| Term | Definition |
| --- | --- |
| **TGE** | Token Generation Event. The official launch of a token |
| **IPO** | Initial Public Offering. The official listing of a private company's shares |
| **FDV** | Fully Diluted Valuation. Total value of a project assuming all tokens are in circulation |
| **FDV Band** | An FDV range with a lower strike and an upper strike |
| **LONG** | Call-spread-like exposure. Payout increases as settlement moves higher through the range and reaches max value above the upper strike |
| **SHORT** | Put-spread-like exposure. Payout increases as settlement moves lower through the range and reaches max value below the lower strike |

## Options Markets

| Term | Definition |
| --- | --- |
| **Option** | A conditional payout instrument tied to where an underlying asset settles relative to a strike or range at expiry |
| **Price Spread** | A price range with a lower strike and an upper strike. LONG and SHORT payouts depend on where the final price lands relative to the range |
| **Underlying** | The asset whose final price determines the option payout |
| **Strike** | The price used to determine whether and how much an option pays at expiry |
| **LONG / SHORT** | The two directional sides of a MegaETH price spread. Together they split a combined value of $1 at settlement |
| **Mint match** | When a LONG buy matches a SHORT buy on the orderbook, the position pair is minted automatically and each side receives the side they bought |
| **Merge match** | When a LONG sell matches a SHORT sell, the positions merge and collateral is released to each side automatically |
| **Expiry** | The time at which an options market resolves and positions are settled |
| **Inside the Range** | When the final settlement price lands between the lower and upper strike, so LONG and SHORT receive partial payouts |
| **Outside the Range** | When the final settlement price lands above the upper strike or below the lower strike. Which side wins depends on direction |

## Covered Options

| Term | Definition |
| --- | --- |
| **Covered Call** | A call position fully backed and settled by the underlying token. Long receives the call payout and LP receives the remaining collateral |
| **Cash-Secured Put** | A put position fully backed and settled by USDG. Short receives the put payout and LP receives the remaining collateral |
| **Option Leg** | The position that receives the option payout. It is labelled Long for calls and Short for puts |
| **LP Leg** | The covered writer position that receives collateral remaining after the option payout |
| **Premium** | The price paid by the option buyer to the seller or writer. Covered-option premiums are paid in USDG and are separate from collateral and settlement |
| **Write** | Opening an LP position by locking the contract's collateral and offering the option for a USDG premium |
| **Burn** | Closing an LP position by paying the orderbook premium, returning the LP token, and unlocking its full collateral |
| **Mint** | Depositing the contract's collateral to create equal amounts of its option and LP legs |
| **Unwind** | Burning equal option and LP amounts for the same contract to redeem their associated collateral |
| **Vault Operator Approval** | The one-time permission required before a covered-option order can fill |

## RWA / Spot Markets

| Term | Definition |
| --- | --- |
| **RWA** | Real World Asset. A tokenised representation of a physical or off chain asset |
| **Perpetual** | A market with no expiry. Positions remain open until sold |

## Wallet and Settlement

| Term | Definition |
| --- | --- |
| **USDM** | The stablecoin used for trading and settlement on MegaETH markets |
| **USDC** | The stablecoin used for trading and settlement on Solana markets (Prediction Markets, Yield Farm) |
| **USDG** | The stablecoin used for covered-option premiums and cash-secured-put collateral on Robinhood Chain |
| **Smart Account** | A delegated trading wallet that batches transactions and abstracts gas |
| **Subkey** | A delegated key that operates the smart account. Managed by the system |
| **Onchain Settlement** | Final execution of a trade or settlement recorded on the blockchain |
| **DFlow** | The infrastructure that tokenizes Kalshi markets on Solana for Prediction Markets. Manual redemption is required through DFlow |
