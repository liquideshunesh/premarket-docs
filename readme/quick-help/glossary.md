---
coverY: 0
---

# Glossary

A quick reference for terms used across the Premarket platform. This glossary will expand as new features and market types are added, in the near future.

## General

<table><thead><tr><th width="183.6171875">Term</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Market</strong></td><td>A trading environment for a specific asset, event, or instrument</td></tr><tr><td><strong>Order Book</strong></td><td>List of active buy (or bids) and sell (or ask) orders in a market. </td></tr><tr><td><strong>Liquidity</strong></td><td>The availability of buyers and sellers in a market.</td></tr><tr><td><strong>Maker</strong></td><td>A trader who places an order that adds liquidity to the order book.</td></tr><tr><td><strong>Taker</strong></td><td>Trader who matches an existing order and removes liquidity from the orderbook.</td></tr><tr><td><strong>Spread</strong></td><td>The difference between the highest bid and the lowest ask in an orderbook.</td></tr><tr><td><strong>Slippage</strong></td><td>The difference between the <em>expected and the actual</em> execution price.</td></tr></tbody></table>

## Trading

<table><thead><tr><th width="184.3984375">Term</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Buy Order</strong></td><td>An instruction to purchase an asset or outcome.</td></tr><tr><td><strong>Sell Order</strong></td><td>An instruction to sell an asset or outcome.</td></tr><tr><td><strong>Market Order</strong></td><td>An instruction to buy or sell immediately at the best available price</td></tr><tr><td><strong>Limit Order</strong></td><td>An instruction to buy or sell only at a specified price.</td></tr><tr><td><strong>Position</strong></td><td>An active holding in a market.</td></tr><tr><td><strong>Position History</strong></td><td>A record of past trades and closed positions.</td></tr></tbody></table>

## Prediction Markets

<table><thead><tr><th width="186.80078125">Term</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Outcome</strong></td><td>A possible result of an event, for example YES or NO.</td></tr><tr><td><strong>Outcome Token</strong></td><td>A token representing a position in a specific outcome. Settles to $1 if correct and $0 if incorrect.</td></tr><tr><td><strong>Settlement</strong></td><td>The final resolution of a market based on the real world result.</td></tr><tr><td><strong>Payout</strong></td><td>The amount received after settlement.</td></tr><tr><td><strong>Implied Probability</strong></td><td>The market price interpreted as a probability. A price of $0.25 implies roughly a 25% chance.</td></tr></tbody></table>

## Pre-TGE Markets

<table><thead><tr><th width="186.80078125">Term</th><th>Definition</th></tr></thead><tbody><tr><td><strong>TGE</strong></td><td>Token Generation Event. The official launch of a token.</td></tr><tr><td></td><td></td></tr><tr><td></td><td></td></tr><tr><td></td><td></td></tr><tr><td></td><td></td></tr></tbody></table>

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
