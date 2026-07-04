# Trader Performance vs Market Sentiment Analysis

## Overview

The objective of this analysis is to investigate how **Bitcoin market sentiment (Fear & Greed Index)** relates to **trader behaviour and trading performance** on the Hyperliquid exchange. By combining market sentiment data with historical trading records, the analysis identifies behavioural patterns and proposes practical trading recommendations.

---

## Datasets

### 1. Bitcoin Fear & Greed Index
Contains daily market sentiment information including:
- Date
- Fear & Greed Index Value
- Sentiment Classification
  - Extreme Fear
  - Fear
  - Neutral
  - Greed
  - Extreme Greed

### 2. Hyperliquid Historical Trading Data
Contains historical trade-level information including:
- Account
- Coin
- Direction
- Trade Size (USD)
- Closed PnL
- Execution Price
- Timestamp
- Additional trading metadata

---

## Project Workflow

### 1. Data Preparation
- Loaded both datasets using Pandas
- Checked for missing values and duplicate records
- Converted timestamps to a common daily format
- Merged the datasets using the trading date

### 2. Performance Analysis
The following performance metrics were analysed across different market sentiment categories:

- Average Closed PnL
- Median Closed PnL
- Total Closed PnL
- Win Rate
- Drawdown Proxy

### 3. Behaviour Analysis

Trader behaviour was analysed using:

- Trading Frequency
- Position Size (Mean & Median)
- Long vs Short Direction Bias

### 4. Trader Segmentation

Two trader segments were created:

- Frequent vs Infrequent Traders
- Consistent vs Inconsistent Traders

These segments were compared using profitability, win rate and trading behaviour.

---

## Key Insights

- Trader performance varies across different market sentiment conditions.
- Position size distributions are highly skewed, making the median a more representative measure than the mean.
- Frequent traders achieved a higher win rate than infrequent traders in this dataset.
- Consistent traders demonstrated higher win rates, while inconsistent traders generated larger average profits with greater variability.

---

## Strategy Recommendations

Based on the analysis, the following recommendations were proposed:

1. Adapt position sizing according to prevailing market sentiment while maintaining disciplined risk management.

2. Focus on consistent execution and controlled risk rather than relying on occasional high-risk trades for large profits.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Repository Structure

```
├── trader_sentiment_analysis.ipynb
├── historical_data.csv
├── fear_greed_index.csv
├── README.md
```

---

## How to Run

1. Clone the repository.

```bash
git clone <repository-link>
```

2. Install the required dependencies.

```bash
pip install pandas numpy matplotlib seaborn
```

3. Open the notebook.

```bash
jupyter notebook trader_sentiment_analysis.ipynb
```

4. Run all cells in sequence.

---

## Note

This analysis identifies historical relationships between market sentiment and trader behaviour. The findings should be interpreted as analytical observations rather than causal conclusions or guaranteed trading strategies.
