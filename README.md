# Copper Futures Analysis

## Overview

This project performs a comprehensive analysis of copper futures markets, comparing MCX (India) and COMEX (US) copper futures, along with their correlation to major copper mining stocks. The analysis spans from January 2010 to June 2025, providing insights into price trends, volatility patterns, and market relationships.

## Key Analyses

### 1. **MCX Copper Futures Analysis**
- Loads and processes multiple CSV/Excel files containing MCX copper futures data
- Handles historical lot size changes (1 MT pre-June 2019, 2.5 MT post-June 2019)
- Calculates average daily prices in INR/kg
- Computes log returns and rolling 30-day annualized volatility
- Visualizes normalized price trends and volatility patterns

### 2. **COMEX Copper Futures Analysis**
- Downloads COMEX copper futures data via Yahoo Finance (ticker: `HG=F`)
- Calculates log returns and rolling 30-day annualized volatility
- Uses 252 trading days per year for annualization
- Plots normalized price trends and volatility

### 3. **Comparative Analysis**
- Side-by-side comparison of MCX and COMEX normalized prices
- Correlation analysis of daily log returns between both markets
- Scatter plot visualization showing relationship between markets
- Correlation coefficient: **0.5780** (moderate positive correlation)

### 4. **Copper Mining Stocks Analysis**
- Analyzes 11 major copper mining companies:
  - Freeport-McMoRan (FCX)
  - BHP Group (BHP)
  - Southern Copper Corp. (SCCO)
  - Glencore (GLEN.L)
  - Zijin Mining (2899.HK, 601899.SS)
  - Anglo American (AAL.L)
  - KGHM Polska (KGH.WA)
  - Antofagasta (ANTO.L)
  - First Quantum Minerals (FM.TO)
  - Hindustan Copper (HINDCOPPER.NS)

- Downloads historical adjusted close prices from Yahoo Finance
- Calculates daily returns and correlation matrices
- Visualizes normalized stock price trends over the 15-year period

## Data Sources

- **MCX Copper Futures**: Local CSV/Excel files (user-provided)
- **COMEX Copper Futures**: Yahoo Finance (`HG=F`)
- **Copper Mining Stocks**: Yahoo Finance (multiple tickers)

## Key Outputs

1. **Merged MCX data** saved as `merged_mcx_copper.csv`
2. **Copper equity data** saved as `copper_equity_adj_close_2010_2025.csv`
3. Visualization plots for:
   - MCX normalized price trends and volatility
   - COMEX normalized price trends and volatility
   - Side-by-side comparison charts
   - Volatility comparison (MCX vs COMEX)
   - Correlation heatmap for mining stocks
   - Normalized stock price trends

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- yfinance
- glob (for file handling)

## Usage Notes

The MCX data processing handles:
- Multiple file formats (CSV and Excel)
- Date formatting and sorting
- Missing value forward-fill
- Lot size conversion based on date (pre/post June 2019)
- Zero contract filtering to avoid division errors

## Findings

- The correlation between MCX and COMEX copper futures daily returns is approximately **0.578**, indicating a moderate positive relationship
- Both markets show similar long-term price trends when normalized
- Understanding these correlations can help in hedging strategies and cross-market arbitrage analysis
