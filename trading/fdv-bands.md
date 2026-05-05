# How FDV Bands Work

FDV bands are the pricing instrument used in pre-TGE markets. Instead of a simple yes or no outcome, you are trading whether a token's fully diluted valuation falls within a specific range at launch.

## What is FDV?

```
FDV = Token Price at Launch x Total Token Supply
```

## What is a Band?

A band is a valuation range. Each band represents a separate tradable outcome with its own orderbook and price.

> Screenshot: Band selection showing multiple ranges with prices

## Bull and Bear Directions

| Direction | Meaning |
|-----------|---------|
| Bull | You believe FDV will land within or above the range |
| Bear | You believe FDV will land within or below the range |

## Payout Logic

FDV bands are directional spreads, not binary markets. Payout increases linearly as the FDV moves in your favour within the range, and is capped at maximum once it crosses the far strike.

**Bull position:**

| Scenario | Result |
|----------|--------|
| FDV below lower strike | $0. Full loss. |
| FDV within the range | Payout increases linearly toward the upper strike |
| FDV above upper strike | Maximum payout. Capped at the upper strike value. |

**Bear position:**

| Scenario | Result |
|----------|--------|
| FDV above upper strike | $0. Full loss. |
| FDV within the range | Payout increases linearly toward the lower strike |
| FDV below lower strike | Maximum payout. Capped at the lower strike value. |

## Example Trade

```
You buy: Bull $200M to $250M band
Price: $0.40 USDM per share
Amount: $10 USDM
Shares received: 25

Final FDV $180M: $0. Below lower strike, full loss.
Final FDV $205M: Partial payout. Linearly increasing from lower strike.
Final FDV $230M: Larger partial payout. Further into range.
Final FDV $270M: Maximum payout. Above upper strike, capped at max win.
```

| Feature | Prediction Markets | FDV Bands |
|---------|------------------|-----------|
| Outcome type | Binary YES/NO | Directional spread |
| Payout | Fixed $1 or $0 | Linearly scaled, capped at max |
| Complexity | Low | Higher |
