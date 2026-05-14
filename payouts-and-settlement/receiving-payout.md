---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Receiving Your Payout

After a market settles, your position has a fixed value. How you receive your payout depends on which product you traded.

### Prediction Markets

> Screenshot: Relevant market settled position

Prediction markets run on Solana. Settlement is not automatic. Once your position expires, you need to interact with the DFlow contract to burn your shares. USDC is then bridged back to your wallet. You must initiate this manually.

### Yield Farms

Yield farms run on Solana. Settlement works the same way as prediction markets. Once your position expires, you interact with the DFlow contract to burn your shares and bridge USDC back to your wallet.

### Pre-IPO and Pre-TGE Markets

> Screenshot: Relevant market settled position

Pre-IPO and pre-TGE markets run on MegaETH. All positions are automatically redeemed at expiry and proceeds are sent directly to your smart account. Payout depends on where the asset's valuation lands at launch relative to your band. No action is needed.

### Options Markets

> Screenshot: Relevant market settled position

Options markets run on MegaETH. All positions are automatically redeemed at expiry. If your band was in the money, the oPRM token holder receives the payout automatically. If out of the money, the oPRM expires worthless and the PRM holder recovers their collateral automatically. If you hold both tokens before expiry, you can unwind at any time to recover your full collateral without waiting for settlement.

### RWA Markets

> Screenshot: Relevant market settled position

RWA markets run on MegaETH. All positions are automatically redeemed at expiry and proceeds are sent directly to your smart account. Payout is based on where the underlying asset price settles relative to your position at expiry.

| Issue                             | Cause                                         | Fix                                |
| --------------------------------- | --------------------------------------------- | ---------------------------------- |
| Nothing happened after settlement | Blockchain confirmation delay                 | Wait a few minutes and refresh     |
| Cannot withdraw                   | Missing required token for options withdrawal | Check you hold the correct token   |
| Zero payout                       | Position resolved out of the money            | Expected outcome, no action needed |
