---
cover: ../.gitbook/assets/Default.png
coverY: 0
---

# How FDV Spreads Work

FDV spreads are the pricing instrument used in Pre TGE and Pre IPO markets. Instead of a simple yes or no outcome, you are trading whether an asset's valuation falls within a specific range at launch.

For Pre TGE markets, the valuation is the token's fully diluted valuation at TGE. For Pre IPO markets, the valuation is the company's market capitalisation at listing. The mechanic is identical.

## What is FDV?

```
FDV = Token Price at Launch x Total Token Supply
```

For Pre IPO markets, substitute share price at listing multiplied by total shares outstanding.

## What is a Spread?

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption><p>FDV ranges with prices</p></figcaption></figure>

A spread is a valuation range. Each spread represents a separate tradable outcome with its own orderbook and price.

## Bull and Bear Directions

| Direction | Meaning                                             |
| --------- | --------------------------------------------------- |
| Bull      | You believe FDV will land within or above the range |
| Bear      | You believe FDV will land within or below the range |

## Payout Logic

FDV spreads are directional instruments, not binary markets. Payout increases linearly as the FDV moves in your favour within the range, and is capped at maximum once it crosses the far strike.

**Bull position:**

| Scenario               | Result                                            |
| ---------------------- | ------------------------------------------------- |
| FDV below lower strike | $0. Full loss.                                    |
| FDV within the range   | Payout increases linearly toward the upper strike |
| FDV above upper strike | Maximum payout. Capped at the upper strike value. |

**Bear position:**

| Scenario               | Result                                            |
| ---------------------- | ------------------------------------------------- |
| FDV above upper strike | $0. Full loss.                                    |
| FDV within the range   | Payout increases linearly toward the lower strike |
| FDV below lower strike | Maximum payout. Capped at the lower strike value. |

## Example Trade

```
You buy: Bull $2B to $3B spread
Price: $0.40 USDM per share
Amount: $10 USDM
Shares received: 25
Final FDV $1.8B: $0. Below lower strike, full loss.
Final FDV $2.1B: Partial payout. Linearly increasing from lower strike.
Final FDV $2.6B: Larger partial payout. Further into range.
Final FDV $3.2B: Maximum payout. Above upper strike, capped at max win.
```
