# Trading Bot Foundations

A complete Python trading bot foundation built from scratch.

## What This Project Does
- Downloads live stock data using yfinance
- Calculates SMA and EMA moving averages
- Codes RSI indicator from scratch without libraries
- Detects SMA crossover buy and sell signals
- Backtests strategy with real P&L tracking
- Implements professional 1% risk position sizing
- Calculates max drawdown

## Results
- Tested on AAPL, SPY, QQQ, MSFT
- Combined SMA + RSI strategy achieved positive P&L on QQQ and SPY
- Max drawdown under 1% with proper position sizing

## Tech Stack
- Python 3.12
- pandas
- yfinance
- matplotlib

## How to Run
```bash
pip install pandas yfinance matplotlib
jupyter notebook day1.ipynb
```

## Key Files
- `day1.ipynb` — Data download and visualization
- `day2.ipynb` — Pandas price manipulation
- `day3.ipynb` — Moving averages and crossover signals
- `day4.ipynb` — RSI from scratch
- `day5.ipynb` — Backtesting engine
- `day6.ipynb` — Position sizing and max drawdown
- `day7.ipynb` — Combined SMA + RSI strategy

## Strategy Performance
| Ticker | Trades | P&L |
|--------|--------|-----|
| SPY    | 2      | +$47.44 |
| QQQ    | 4      | +$67.07 |
| MSFT   | 4      | -$43.31 |
