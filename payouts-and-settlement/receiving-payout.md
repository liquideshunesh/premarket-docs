---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# Receiving Your Payout

After a market settles, your position has a fixed value. How you receive your payout depends on which product you traded.

## Prediction Markets

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>Settled Position</p></figcaption></figure>

Prediction markets run on Solana. Settlement is not automatic. Once your position expires, you need to interact with the DFlow contract to burn your shares. USDC is then bridged back to your wallet. You must initiate this manually.

## Yield Farm

Yield Farm positions run on Solana and use the same prediction market contracts. Settlement works the same way. Once your position expires, you interact with the DFlow contract to burn your shares and bridge USDC back to your wallet.

## Pre IPO and Pre TGE Markets

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption><p>Settled positions</p></figcaption></figure>

Pre IPO and Pre TGE markets run on MegaETH. All positions are automatically redeemed at expiry and proceeds are sent directly to your smart account in USDM. Payout depends on where the asset's valuation lands at listing relative to your band. No action is needed.

## Options Markets

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption><p>Settled Positions</p></figcaption></figure>

Options markets run on MegaETH. All positions are automatically redeemed at expiry. If your band was in the money, the oPRM token holder receives the payout automatically. If out of the money, the oPRM expires worthless and the PRM holder recovers their collateral automatically. If you hold both tokens before expiry, you can unwind at any time to recover your full collateral without waiting for settlement.

## RWA Markets

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>RWA positions</p></figcaption></figure>

RWA markets do not settle. There is no expiry and no automatic redemption. To realise profit or loss, sell back into the orderbook. Proceeds are credited to your smart account in USDM.

## Common Issues

| Issue | Cause | Fix |
| --- | --- | --- |
| Nothing happened after settlement | Blockchain confirmation delay | Wait a few minutes and refresh |
| Cannot withdraw | Missing required token for options withdrawal | Check you hold the correct token |
| Zero payout | Position resolved out of the money | Expected outcome, no action needed |
| Solana position not auto credited | Manual redemption required via DFlow | Initiate redemption on the position |
