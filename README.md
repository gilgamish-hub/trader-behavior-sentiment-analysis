# Trader Behavior Analysis using Bitcoin Fear & Greed Index

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-purple)

## Author
Jatin Pal  
Application Role: Junior Data Scientist – Trader Behavior Insights  

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

### 1️⃣ Higher Trading Activity During Greed

Traders are significantly more active during **Greed sentiment**, suggesting higher confidence in bullish markets.

### 2️⃣ Profitability Higher During Greed Markets

Profit distributions show that **Greed periods produce more positive returns**, while Fear markets show larger loss volatility.

### 3️⃣ Strategy Shift During Fear Markets

During Fear periods:

- Short positions increase
- Traders adopt more defensive strategies

### 4️⃣ Trade Size Increases in Greed Markets

Traders take **larger positions during Greed sentiment**, indicating higher risk appetite.

### 5️⃣ Whale Traders Dominate Profits

A small number of traders generate a **large portion of total profits**, highlighting concentration of trading success.

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
trader-behavior-sentiment-analysis
│
├── trader_behavior_analysis.ipynb
├── README.md
└── dataset_links.txt



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

The analysis shows that **market sentiment significantly influences trader behavior**.

Greed markets encourage:

- Higher trading activity
- Larger trade sizes
- Higher profitability

Fear markets lead to:

- Defensive trading strategies
- Increased short positions
- Higher loss volatility

Understanding sentiment-driven behavior can help design **better algorithmic trading systems and risk management strategies**.

---

# Repository

https://github.com/gilgamish-hub/trader-behavior-sentiment-analysis
