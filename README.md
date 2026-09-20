# Yield Curve Monitor
### Fixed Income Relative Value Tool | Sidney Pratt

## Overview
This model tracks the US Treasury yield curve across four maturities
(3-month, 5-year, 10-year, 30-year) and classifies the current regime
as Steep, Normal, Flat, Inverted, or Deeply Inverted based on the
classic 10Y minus 3M spread.

Built specifically to complement a fixed income relative value
research portfolio — directly relevant to rates, credit, and
mortgage trading desks.

## Key Features
- Live Treasury yield data downloaded fresh on every run
- Regime classification across 5 curve states
- Plain English interpretation of what the curve is saying
- Dynamic recommendations that update with the regime
- 30-day and 90-day trend detection
- Backtest of a TLT strategy using curve signals
- Key historical event annotations

## Current Reading — September 18, 2026
- 3-Month: 3.98%
- 10-Year: 5.00%
- 10Y minus 3M Spread: +1.02%
- Regime: NORMAL
- Percentile: 39th percentile since 2000
- Strategy Signal: HOLD TLT

## Regime Classification
| Regime | Spread | Signal |
|--------|--------|--------|
| Steep | Above +1.50% | Hold TLT |
| Normal | +0.50% to +1.50% | Hold TLT |
| Flat | -0.50% to +0.50% | Move to Cash |
| Inverted | -0.50% to 0% | Move to Cash |
| Deeply Inverted | Below -0.50% | Move to Cash |

## Backtest Results — TLT 2003 to 2026
| Metric | Strategy | Buy & Hold |
|--------|----------|------------|
| Total Return | 91.5% | 111.2% |
| Ann. Return | 2.8% | 3.2% |
| Sharpe Ratio | 0.23 | 0.22 |
| Max Drawdown | -33.0% | -48.4% |

Key result: 15.3% reduction in max drawdown by moving to cash
during inversion and flat curve periods.

## Charts
![Yield Curve Monitor](yield_curve_monitor.png)
![Yield Curve Backtest](yield_curve_backtest.png)

## Why This Matters for Fixed Income
The yield curve is the single most watched indicator across all
fixed income desks — rates, credit, and mortgages. Every desk
at every major fixed income firm tracks the 2yr/10yr spread daily.

- Rates desk: curve shape determines bond strategy
- Credit desk: inversions predict credit stress
- Mortgage desk: curve affects prepayment speeds and MBS pricing

## Tools & Technologies
- Python
- yfinance — live Treasury yield data
- pandas, numpy — data processing
- matplotlib — visualization
- Google Colab — development environment

## About
Sidney Pratt is a Finance and Economics student at Western Michigan
University and an ACHA D1 hockey player building a quantitative
research portfolio targeted at fixed income trading internships.

sidneyppratt.com | github.com/sidneyppratt-svg
