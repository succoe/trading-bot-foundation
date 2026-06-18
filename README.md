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

- # Forex Trading Bot

A professional automated forex trading bot built with Python and 
MetaTrader 5. Trades EUR/USD, GBP/USD, XAU/USD and BTC/USD 
automatically using a multi-signal strategy with ML filtering.

## What This Bot Does
- Connects to MetaTrader 5 via Python API
- Scans 4 pairs simultaneously every 60 seconds
- Places BUY/SELL orders automatically with stop loss and take profit
- Sends Telegram alerts on every trade and risk event
- Implements FTMO prop firm risk rules

## Strategy
Multi-signal scoring system combining:
- SMA20/SMA50 crossover trend filter
- Bollinger Bands mean reversion (85%+ win rate on EUR/USD)
- RSI overbought/oversold filter
- Random Forest ML signal confirmation
- Session filter: London and New York hours only

## Risk Management
- Max daily loss: 4% (FTMO compliant)
- Max total drawdown: 8% (FTMO compliant)
- Max open trades: 3 simultaneously
- Weekend gap protection: closes all Friday 9pm UTC
- Circuit breaker: halts trading automatically on limit breach

## Backtest Results
| Pair | Strategy | Trades | Win Rate | Total Pips |
|------|----------|--------|----------|------------|
| EUR/USD | Bollinger Bands | 7 | 85.7% | +122.9 |
| GBP/USD | Bollinger Bands | 6 | 83.3% | +130.2 |
| XAU/USD | Bollinger Bands | 6 | 66.7% | +positive |
| BTC/USD | BB + Scanner | 4 | 75.0% | +positive |

## Tech Stack
- Python 3.12
- MetaTrader 5
- pandas, numpy
- scikit-learn (Random Forest)
- Telegram Bot API
- Exness demo account

## Setup
```bash
pip install MetaTrader5 pandas numpy scikit-learn requests pytz
```

1. Install MetaTrader 5 desktop app
2. Create free Exness demo account
3. Log MT5 into Exness
4. Add your Telegram token and chat ID
5. Run the bot

```bash
python forex_bot.py
```

## Architecture

## Pairs Traded
- EUR/USD — primary pair, ML filter active
- GBP/USD — high win rate with BB strategy  
- XAU/USD — Gold, Bollinger Bands strategy
- BTC/USD — crypto CFD via Exness

## Risk Warning
This bot trades on a demo account. Never risk real money 
without extensive live testing first.

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
