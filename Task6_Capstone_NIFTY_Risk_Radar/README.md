# Task 6: Final Data Science Capstone

**NIFTY 50 Risk Radar: risk profiling, high-volatility alerts and portfolio back-testing**

## Problem
Investors often judge a stock only by its past return. This project builds a small risk system for an advisory team: which stocks are risky, when is a stock likely to become unusually volatile, and can a calmer portfolio be built?

## Data
- Daily prices and volume of 25 NIFTY 50 stocks, the NIFTY 50 index and India VIX (Yahoo Finance, via yfinance)
- 4 Jan 2016 to 30 Oct 2026, 2,674 trading days after cleaning, no missing values
- `nifty_prices_clean.csv` is the cleaned data

## What I did
1. Risk KPIs for each stock: return, volatility, Sharpe ratio, maximum drawdown, beta
2. Grouped the stocks into 5 risk profiles with KMeans
3. Built an alert model (Logistic Regression and Random Forest) that predicts whether the next 5 days will be unusually volatile. 13 features, 60,375 stock-days, train 2017 to 2022, test 2023 to 2026 (split by time, with a gap)
4. Back-tested equal-weight and capped minimum-variance portfolios (monthly rebalancing) against the NIFTY 50 index

## Key results
- Every stock (22% to 36% volatility) is riskier than the index (16.1%) because average correlation is only 0.28
- 5 risk groups: Group 1 is the steady core (worst fall 37.5%); Bajaj Finance and Tata Steel are high risk and high return
- Alert model: ROC-AUC 0.592 vs 0.583 for a simple persistence baseline. The top 10% of alert scores were high-volatility days 41.1% of the time vs 26.3% overall
- Market-wide features (VIX, NIFTY moves) hold about 54% of the model's importance
- Minimum-variance portfolio: 15.4% a year, 13.5% volatility, Sharpe 0.70 vs index 10.9%, 16.3%, 0.30. In the COVID crash it fell 24.7% vs 36.5% for the index

## Honest limits
Survivorship bias (stocks chosen from today's NIFTY 50), dividends included in stocks but not in the index, a modest alert model, no trading costs, and the minimum-variance portfolio lagged in 2026. This is an educational project, not investment advice.

## Files
| File | Description |
|---|---|
| `Task6_Capstone_NIFTY_Risk_Radar.ipynb` | Colab notebook with code, outputs and charts |
| `nifty_prices_clean.csv` | Cleaned daily prices (25 stocks, index, VIX) |
| `Task6_Report.docx` | Full capstone report |
| `Task6_Presentation.pdf` | Presentation slides |

## Tools
Python, pandas, NumPy, scikit-learn, SciPy, Matplotlib, Seaborn, yfinance, Google Colab
