# Trader Behavior Analysis using Bitcoin Fear & Greed Index

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-purple)

## Author
Jatin Pal · [Portfolio](https://gilgamish-hub.github.io)

---

# Project Overview

This project analyzes how **Bitcoin market sentiment** influences **trader behavior and profitability**.

By combining **Hyperliquid historical trading data** with the **Bitcoin Fear & Greed Index**, the analysis uncovers patterns in trading direction, trade size, and profit distribution across different market conditions.

The goal is to extract insights that could help design **smarter trading strategies and risk management systems**.

---

# Problem Statement

Does market sentiment influence trader behavior?

Specifically we investigate:

- Do traders perform better during **Fear or Greed markets**?
- Does sentiment affect **trade direction (long vs short)**?
- Do traders take **larger positions during Greed markets**?
- Are a few **whale traders responsible for most profits**?

---

# Datasets

## 1️⃣ Historical Trader Data
Contains trade-level data including:

- Account
- Coin
- Execution Price
- Trade Size (USD & Tokens)
- Trade Direction
- Buy / Sell Side
- Closed Profit & Loss (PnL)
- Fees
- Transaction IDs

## 2️⃣ Bitcoin Fear & Greed Index

Daily sentiment indicator representing overall market psychology:

| Value | Market Sentiment |
|------|----------------|
| 0-25 | Extreme Fear |
| 25-50 | Fear |
| 50 | Neutral |
| 50-75 | Greed |
| 75-100 | Extreme Greed |

---

# Project Workflow
Data Collection
↓
Data Cleaning
↓
Data Integration
↓
Exploratory Data Analysis
↓
Trader Behavior Analysis
↓
Market Sentiment Analysis
↓
Machine Learning Model
↓
Insights & Conclusions



---

# Methodology

The analysis follows a standard **data science pipeline**:

### 1. Data Preprocessing
- Timestamp conversion
- Feature extraction
- Handling missing values

### 2. Data Integration
- Merge trader dataset with sentiment dataset by date

### 3. Exploratory Data Analysis
- Market sentiment distribution
- Profit distribution
- Trade frequency analysis

### 4. Behavioral Analysis
- Trade direction vs sentiment
- Trade size vs sentiment
- Profitability patterns

### 5. Advanced Insights
- Profit heatmap (Sentiment vs Direction)
- Whale trader detection
- Profit distribution analysis

### 6. Machine Learning Model
A **Random Forest Regressor** is used to predict trade profitability using:

Features:
- Market Sentiment
- Trade Direction
- Trade Size
- Fees

Target:
- Closed PnL

---

# Key Insights

Measured on the 211,218 trade records (32 accounts, May 2023 to May 2025) that match a day in the Fear & Greed Index. "Closing trades" are the records with a non-zero Closed PnL.

| Sentiment | Trades | Days | Trades per day | Median trade size (USD) | Avg PnL per closing trade (USD) | Win rate of closing trades | Buy share |
|---|---|---|---|---|---|---|---|
| Extreme Fear | 21,400 | 14 | 1,529 | 766 | 71.0 | 76.2% | 51.1% |
| Fear | 61,837 | 91 | 680 | 736 | 112.6 | 87.3% | 49.0% |
| Neutral | 37,686 | 67 | 562 | 548 | 71.2 | 82.4% | 50.3% |
| Greed | 50,303 | 193 | 261 | 555 | 85.4 | 76.9% | 48.9% |
| Extreme Greed | 39,992 | 114 | 351 | 500 | 130.2 | 89.2% | 44.9% |

### 1️⃣ Traders are busiest when the market is afraid
Extreme Fear days average **1,529 trades a day**, almost 6× the 261 of Greed days. Panic brings activity, not caution.

### 2️⃣ Positions are larger in Fear, not in Greed
The median trade is **$766 in Extreme Fear and $736 in Fear**, against $555 in Greed and $500 in Extreme Greed.

### 3️⃣ Extreme Greed is the most profitable regime
Closing trades in Extreme Greed average **$130** with an **89.2% win rate**, the best of any regime. Plain Greed ($85, 76.9%) does worse than Fear ($113, 87.3%), so the relationship is not a simple "greed means profit".

### 4️⃣ Selling rises at the euphoric top
The share of buys stays near 49–51% in every regime except Extreme Greed, where it drops to **44.9%**. That fits traders taking profit when sentiment peaks.

### 5️⃣ A few accounts make most of the money
The **top 3 of 32 accounts earned 44.5%** of all profit made by profitable accounts.

**Caveat:** the dataset covers only 32 accounts, and regimes have very different numbers of days (14 Extreme Fear days against 193 Greed days), so these are patterns in this sample, not general market laws.

---

# Technologies Used

Python  
Pandas  
NumPy  
Matplotlib  
Seaborn  
Scikit-Learn  
Jupyter Notebook  

---

# Project Structure

```text
trader-behavior-sentiment-analysis/
├── trader_behavior_analysis.ipynb   # the full analysis
├── historical_data.csv              # Hyperliquid trade records
├── fear_greed_index.csv             # daily Bitcoin Fear & Greed Index
├── dataset_links.txt                # where the data came from
└── README.md
```

---

# How to Run the Project

### 1️⃣ Clone Repository
git clone https://github.com/gilgamish-hub/trader-behavior-sentiment-analysis.git

### 2️⃣ Install Dependencies
pip install pandas numpy matplotlib seaborn scikit-learn


### 3️⃣ Run Notebook

Open Jupyter Notebook and run:
trader_behavior_analysis.ipynb


---

# Conclusion

In this data, sentiment does change how traders behave, but not always in the expected direction:

- **Fear** brings the most activity and the largest positions.
- **Extreme Greed** brings the best results and more selling, consistent with profit-taking at the top.
- **Profits are concentrated** in a handful of accounts.

A risk system built on this data should watch position size most closely in fearful markets, when traders are most active and trade the largest amounts.

---

# Repository

https://github.com/gilgamish-hub/trader-behavior-sentiment-analysis
