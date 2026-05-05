# Glossary

A quick reference for terms used across Premarket. This glossary will expand as new features and market types are added.

## General

**Market** - A trading environment for a specific asset, event, or instrument.

**Order Book** - A list of active buy and sell orders in a market. Bids are buy orders. Asks are sell orders.

**Liquidity** - The availability of buyers and sellers in a market. Low liquidity means harder execution and wider spreads.

**Maker** - A trader who places an order that adds liquidity to the orderbook.

**Taker** - A trader who matches an existing order and removes liquidity from the orderbook.

**Spread** - The difference between the highest bid and the lowest ask in an orderbook.

**Slippage** - The difference between the expected execution price and the actual execution price.

## Trading

**Buy Order** - An instruction to purchase an asset or outcome.

**Sell Order** - An instruction to sell an asset or outcome.

**Market Order** - An order that executes immediately against the best available orders in the book.

**Limit Order** - An order that executes only at a specified price. Not guaranteed to fill.

**Position** - Your active holding in a market.

**Position History** - A record of past trades and closed positions.

## Prediction Markets

**Outcome** - A possible result of an event, for example YES or NO.

**Outcome Token** - A token representing a position in a specific outcome. Settles to $1 if correct and $0 if incorrect.

**Settlement** - The final resolution of a market based on the real world result.

**Payout** - The amount received after settlement.

**Implied Probability** - The market price interpreted as a probability. A price of $0.25 implies roughly a 25% chance.

## Pre-TGE Markets

**TGE** - Token Generation Event. The official launch of a token.

**FDV** - Fully Diluted Valuation. Total value of a project assuming all tokens are in circulation.

**Band** - A valuation range used as a tradable outcome in pre-TGE markets.

**Bull** - A directional position betting the FDV will land at the upper end of or above the selected range.

**Bear** - A directional position betting the FDV will land at the lower end of or below the selected range.

## Options Markets

**Option** - A conditional payout instrument tied to whether an underlying asset lands within a defined price range at expiry.

**PRM Token** - The write position token received when minting an options position. Represents the collateral claim.

**oPRM Token** - The outcome token received when minting an options position. Tradable on the orderbook.

**Minting** - The process of depositing USDM as collateral to receive PRM and oPRM tokens.

**Unwind** - Returning equal amounts of PRM and oPRM tokens before expiry to recover full collateral.

**Writer** - A user who mints a position by depositing collateral and receives both PRM and oPRM tokens.

**Expiry** - The time at which an options market resolves and positions are settled.

**ITM (In the Money)** - When the underlying asset settles within the option's strike range at expiry.

**OTM (Out of the Money)** - When the underlying asset settles outside the option's strike range at expiry.

## Wallet and Settlement

**USDM** - The stable unit used for trading and settlement on Premarket.

**Smart Account** - A delegated trading wallet for gas abstraction and seamless execution.

**Subkey** - A delegated key that operates the smart account. Managed by the system.

**On-Chain Settlement** - Final execution of a trade or settlement recorded on the blockchain.

## Errors

**No price available for market order** - No matching orders on the other side of the orderbook. Place a limit order or wait for liquidity.

**Insufficient Balance** - Not enough funds to complete the trade. Check your smart account balance and deposit if needed.
