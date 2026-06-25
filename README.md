# Mean Reversion Strategy Backtesting using DJIA Stocks


This project backtests a mean reversion trading strategy using historical data from the Dow Jones Industrial Average (DJIA). The objective is to evaluate whether stocks that perform poorly on one trading day tend to rebound on the following day.

The strategy is tested on approximately 10 years of historical data, and its performance is compared against the DIA ETF, which tracks the DJIA index.

⸻

## What is the Dow Jones Industrial Average (DJIA)?

The Dow Jones Industrial Average (DJIA) is one of the oldest and most widely followed stock market indices in the world. It consists of 30 large, publicly traded U.S. companies representing various sectors such as technology, finance, healthcare, consumer goods, and manufacturing.

Unlike the S&P 500, which is weighted by market capitalization, the DJIA is a price-weighted index, meaning stocks with higher share prices have a greater influence on the index’s movement.

### Some companies included in the DJIA are:

* Apple (AAPL)
* Microsoft (MSFT)
* JPMorgan Chase (JPM)
* Coca-Cola (KO)
* Goldman Sachs (GS)
* Visa (V)

#### The DJIA is commonly used as a benchmark to measure the overall performance of the U.S. stock market.



### Strategy

This project implements a mean reversion strategy based on the assumption that short-term price movements often overreact and may partially reverse on the next trading day.

The strategy follows these steps every trading day:

1. Calculate the daily return for every DJIA stock.
2. Rank all stocks based on their daily returns.
3. Select the 10 worst-performing stocks (largest daily losers).
4. Allocate the portfolio equally among these 10 stocks.
5. Buy the selected stocks at the closing price of the current trading day.
6. Hold the positions overnight.
7. Sell all positions at the closing price of the next trading day.
8. Repeat the process using the updated portfolio value.




## Data Collection

### Historical stock prices are obtained using the Yahoo Finance API (yfinance).

The list of DJIA constituent companies is retrieved from Wikipedia, after which historical OHLCV (Open, High, Low, Close, Volume) data is downloaded for each company.



## Performance Evaluation

### The strategy is evaluated using several commonly used quantitative finance metrics:

* Total Return – Overall percentage gain or loss over the entire backtest period.
* Annualized Return – Expected yearly return assuming returns compound over time.
* Annualized Volatility – Measures the variability (risk) of returns.
* Sharpe Ratio – Evaluates the return earned for each unit of risk taken.
* Cumulative Return – Tracks the portfolio’s growth throughout the backtest.



## Benchmark Comparison

To determine whether the strategy adds value, its performance is compared against the DIA ETF, an Exchange-Traded Fund designed to closely track the performance of the Dow Jones Industrial Average.

The comparison includes:

* Annualized Return
* Annualized Volatility
* Sharpe Ratio
* Portfolio Growth



## Technologies Used

* Python
* Pandas
* NumPy
* yfinance
* Matplotlib / Plotly
* Jupyter Notebook
