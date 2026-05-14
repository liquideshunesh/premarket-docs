---
cover: ../.gitbook/assets/banner-generic.png
coverY: 0
---

# Receiving Your Payout

After a market settles, your position has a fixed value. All positions on Premarket are automatically redeemed at expiry and proceeds are sent directly to your smart account. You do not need to manually claim or trigger settlement.

> Screenshot: Portfolio showing settled position

## How Settlement Works Across Market Types

**Prediction Markets:** If you backed the winning outcome, each share pays $1 and funds are credited to your smart account automatically. If you backed the losing outcome, your shares expire at $0.

**Options Markets:** If your band was in the money at expiry, the oPRM token holder receives the payout automatically. If out of the money, the oPRM expires worthless and the PRM holder recovers their collateral. If you hold both tokens before expiry, you can unwind to recover full collateral.

**Pre-TGE Markets:** Payout depends on where the token's FDV lands at launch relative to your band. Settlement is automatic.

{% hint style="warning" %}
Solana prediction markets work differently. Once your position expires, you need to interact with the DFlow contract to burn your shares and bridge your USDC back. This is not handled automatically.
{% endhint %}

| Issue                             | Cause                                         | Fix                                |
| --------------------------------- | --------------------------------------------- | ---------------------------------- |
| Nothing happened after settlement | Blockchain confirmation delay                 | Wait a few minutes and refresh     |
| Cannot withdraw                   | Missing required token for options withdrawal | Check you hold the correct token   |
| Zero payout                       | Position resolved out of the money            | Expected outcome, no action needed |
