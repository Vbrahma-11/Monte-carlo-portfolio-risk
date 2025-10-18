# Monte Carlo Portfolio Risk Analysis

A portfolio risk analyzer that simulates thousands of possible market outcomes. Built with Python, PyTorch, and real stock data.

## What This Does

This project analyzes investment risk for a tech stock portfolio (NVDA, AAPL, MSFT, TSLA, GOOGL). It:
- Downloads real historical stock data
- Runs Monte Carlo simulations to predict future portfolio values
- Calculates risk metrics like VaR and CVaR

## Key Features

- **Real Market Data**: Uses Yahoo Finance for actual stock prices
- **Risk Metrics**: Calculates Value at Risk (VaR) and Conditional VaR (CVaR)
- **Visualization**: Shows distribution of possible outcomes
- **Percentile Analysis**: Tracks best-case, worst-case, and median scenarios

## Requirements

- Python 3.8+
- CUDA-capable GPU (I used RTX 4070)
- Required packages: torch, numpy, pandas, matplotlib, yfinance, datetime, scipy, seaborn

## How to Run

Open monte_carlo_portfolio.ipynb in Jupyter Notebook and run the cells in order.

The notebook will:
1. Download historical stock data
2. Calculate portfolio statistics
3. Run Monte Carlo simulations on GPU
4. Display Monte Carlo sumulations
5. Display risk metrics and visualizations

## Portfolio Details

**Stocks**: NVDA, AAPL, MSFT, TSLA, GOOGL  
**Weights**: Equal-weighted (20% each)  
**Initial Investment**: $10,000  
**Simulation Period**: ~5 years forward  
**Number of Simulations**: 10,000

## Sample Results

Starting with $10,000:
- **5th Percentile** (worst case): ~$6,000 (VaR: $4,000 loss)
- **50th Percentile** (median): ~$15,000
- **95th Percentile** (best case): ~$35,000+

## What I Learned

- How Monte Carlo simulation works for portfolio analysis
- Using Cholesky decomposition for correlated stock returns
- Calculating and interpreting risk metrics (VaR, CVaR)
- GPU programming with PyTorch for financial modeling
- Working with real financial data from APIs
- Portfolio statistics (returns, volatility, Sharpe ratio)

## The Math Behind It

The project uses:
- **Historical Returns**: Actual stock performance data
- **Covariance Matrix**: How stocks move together
- **Cholesky Decomposition**: Simulates correlated random movements
- **Monte Carlo Method**: Generates thousands of possible futures

## Visualizations

The notebook includes:
- All simulation paths plotted together
- Distribution histogram of final portfolio values
- Percentile cone showing range of outcomes
- Risk metrics evolution over time

## Why I Built This

I wanted to understand portfolio risk and learn how investment firms analyze potential losses. This combines statistics, probability, and real market data.

## Future Improvements

- Add more asset classes (bonds, commodities)
- Implement portfolio optimization (find best weights)
- Add rebalancing strategies
- Test different risk-return profiles
- Include transaction costs

## Disclaimer

Disclaimer - This was just a fun educational personal project, please dont use for reeal life trading.

## Contact

- Vishal Brahma (Carnegie Mellon University 2029) 
- GitHub: @VBrahma-11
- Email: Vbrahma@andrew.cmu.edu

