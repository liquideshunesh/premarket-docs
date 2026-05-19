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
| **Implied Probability** | The market price interpreted as a probability. A price of $0.25 implies roughly a 25% chance |
| **Yield (Yield Farm)** | The spread between the entry price and $1, representing the return if the leg resolves correctly |

## Pre TGE and Pre IPO Markets

| Term | Definition |
| --- | --- |
| **TGE** | Token Generation Event. The official launch of a token |
| **IPO** | Initial Public Offering. The official listing of a private company's shares |
| **FDV** | Fully Diluted Valuation. Total value of a project assuming all tokens are in circulation |
| **Band** | A valuation range used as a tradable outcome in pre TGE and pre IPO markets |
| **Bull** | A directional position betting the valuation will land within or above the selected range |
| **Bear** | A directional position betting the valuation will land within or below the selected range |

## Options Markets

| Term | Definition |
| --- | --- |
| **Option** | A conditional payout instrument tied to whether an underlying asset lands within a defined price range at expiry |
| **PRM Token** | The write position token received when minting an options position. Represents the collateral claim |
| **oPRM Token** | The outcome token received when minting an options position. Tradable on the orderbook |
| **Minting** | The process of depositing USDM as collateral to receive PRM and oPRM tokens |
| **Unwind** | Returning equal amounts of PRM and oPRM tokens before expiry to recover full collateral |
| **Writer** | A user who mints a position by depositing collateral and receives both PRM and oPRM tokens |
| **Expiry** | The time at which an options market resolves and positions are settled |
| **ITM (In the Money)** | When the underlying asset settles within the option's strike range at expiry |
| **OTM (Out of the Money)** | When the underlying asset settles outside the option's strike range at expiry |

## RWA Markets

| Term | Definition |
| --- | --- |
| **RWA** | Real World Asset. A tokenised representation of a physical or off chain asset |
| **Perpetual** | A market with no expiry. Positions remain open until sold |

## Wallet and Settlement

| Term | Definition |
| --- | --- |
| **USDM** | The stablecoin used for trading and settlement on MegaETH markets |
| **USDC** | The stablecoin used for trading and settlement on Solana markets (Prediction Markets, Yield Farm) |
| **Smart Account** | A delegated trading wallet that batches transactions and abstracts gas |
| **Subkey** | A delegated key that operates the smart account. Managed by the system |
| **Onchain Settlement** | Final execution of a trade or settlement recorded on the blockchain |
| **DFlow** | The liquidity partner for Prediction Markets and Yield Farm on Solana. Manual redemption is required via the DFlow contract |
