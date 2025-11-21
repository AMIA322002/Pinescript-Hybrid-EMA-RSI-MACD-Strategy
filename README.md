# Hybrid EMA + RSI + MACD Strategy

A hybrid trend-following and momentum strategy that combines EMA trend
structure, RSI strength filtering, and MACD histogram confirmation.
Includes an optional ATR-based stop-loss and take-profit system.
Designed for clean confluence entries, strong trend alignment, and
customizable risk management.

------------------------------------------------------------------------

## Trend Detection

Fast EMA and Slow EMA determine market direction.\
Long signals require Fast EMA \> Slow EMA.\
Short signals require Fast EMA \< Slow EMA.

## Momentum Filtering

RSI must be above or below a selected threshold (default 50) to confirm
trend strength.

## MACD Confirmation

MACD histogram must be positive (bullish) or negative (bearish) to avoid
weak signals.

------------------------------------------------------------------------

# Entry Logic

### Long Entry:

-   Fast EMA above Slow EMA\
-   RSI \> threshold\
-   MACD histogram \> 0\
-   Optional: price must be above both EMAs

### Short Entry:

-   Fast EMA below Slow EMA\
-   RSI \< threshold\
-   MACD histogram \< 0\
-   Optional: price must be below both EMAs

------------------------------------------------------------------------

# Exit Logic (Optional ATR-Based)

If ATR stops are enabled:\
- Long SL = Close − ATR × Stop Multiplier\
- Long TP = Close + ATR × TP Multiplier\
- Short SL = Close + ATR × Stop Multiplier\
- Short TP = Close − ATR × TP Multiplier

ATR volatility makes stops adaptive to market conditions.

------------------------------------------------------------------------

# Position Sizing

Two sizing modes:\
- Percent of equity (dynamic sizing recommended)\
- Fixed contract quantity (scalping or fixed-lot users)

------------------------------------------------------------------------

# Alerts

The script fires alerts automatically on real-time bars:\
- LONG signal detected\
- SHORT signal detected

To enable: 1. Add the strategy to your chart\
2. Click Create Alert\
3. Choose this script as the alert source\
4. Set alert frequency (e.g., once per bar)

------------------------------------------------------------------------

# Visual Features

-   EMA plot lines\
-   Optional long/short markers\
-   Optional stop loss and take profit labels\
-   Hidden ATR bands for debugging

------------------------------------------------------------------------

# Inputs (Fully Customizable)

-   EMA lengths\
-   RSI length + threshold\
-   MACD fast/slow/signal\
-   ATR stop/TP multipliers\
-   Long/short toggles\
-   Price-beyond-EMA filter\
-   Position sizing mode\
-   Label and plot visibility

------------------------------------------------------------------------

# Notes

This strategy is built for clarity, flexibility, and consistent
trend-following logic.\
Always forward-test on a demo account before applying it to live
trading.

------------------------------------------------------------------------
