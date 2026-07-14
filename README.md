# Statistical Arbitrage in Cryptocurrencies

This project studies whether BTC/USD recent price movement can be used to build a disciplined momentum trading strategy.

The final strategy is a 30-day long-only Bitcoin momentum rule. If Bitcoin was up over the past 30 days, the strategy holds BTC for the next day. Otherwise, it stays in cash.

## Submission Files

The final submission files are in the `output/` folder:

- `Shruti_Narmeti_Project.pdf` - final project report
- `Shruti_Narmeti_Project.ipynb` - self-contained notebook
- `Statistical-Arbitrage-in-Cryptocurrencies (1).pdf` - final presentation deck

## Project Summary

The project uses historical Bitstamp BTC/USD minute-level OHLCV data from 2012 through early 2025. The data is cleaned, converted into complete daily observations, and used to test momentum and reversal signals across multiple lookback horizons.

The analysis includes:

- Data cleaning and daily resampling
- Momentum/reversal horizon scan
- Activity and weekday/weekend seasonality tests
- Validation-based strategy selection
- Held-out test-period backtest
- Trading cost sensitivity
- Performance comparison against BTC buy-and-hold

## Final Strategy

Selected rule:

- Lookback horizon: 30 days
- Position type: long only
- Activity filter: no
- Trading cost assumption: 20 basis points per unit of turnover

Held-out test period:

- 2022-01-01 to 2025-01-06

## Key Results

During the held-out test period:

| Metric | Selected Strategy | BTC Buy-and-Hold |
|---|---:|---:|
| Total Return | 90.3% | 119.3% |
| CAGR | 23.8% | 29.7% |
| Annualized Volatility | 36.7% | 53.7% |
| Sharpe Ratio | 0.76 | 0.75 |
| Maximum Drawdown | -40.2% | -66.8% |

The strategy did not beat BTC buy-and-hold on total return, but it had lower volatility, smaller drawdowns, and a slightly higher Sharpe ratio.

## How to Run the Notebook

Open and run:

```text
output/Shruti_Narmeti_Project.ipynb
