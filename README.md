📊 Trader Performance vs Market Sentiment Analysis
--
Data Science Intern Assignment – Primetrade.ai
--
📌 Project Overview
--
This project analyzes how Bitcoin market sentiment (Fear & Greed Index) influences trader behavior and performance on Hyperliquid.
Using over 211,000 trade records, the study evaluates how profitability, win rate, trade frequency, position sizing, and directional bias vary across sentiment regimes such as Extreme Fear, Fear, Neutral, Greed, and Extreme Greed.
--
The objective is to identify behavioral patterns and derive actionable, sentiment-aware trading insights.

📂 Dataset Description

1️⃣ Fear & Greed Index (fear_greed_index.csv)

Date

Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

2️⃣ Historical Trade Data (historical_data.csv)

Account

Coin

Execution Price

Size USD

Side (BUY/SELL)

Timestamp

Closed PnL

Fee

Trade ID

Other trade metadata

🧹 Data Preparation

Cleaned column names and removed duplicates

Corrected timestamp parsing (used Timestamp IST due to corrupted Unix column)

Converted both datasets to daily granularity

Performed inner join on Date

Final merged dataset size: 211,218 rows

⚙️ Feature Engineering

The following metrics were created:

Daily PnL per trader

Win rate per trader

Average trade size

Trades per day

Long/Short (BUY/SELL) distribution

Drawdown proxy (cumulative PnL vs running max)

📊 Key Findings
🔹 1. Profitability Peaks During Extreme Greed

Highest average PnL: 67.89

Highest win rate: 46.5%

Strong alignment with bullish momentum environments

🔹 2. Fear Regimes Drive Aggressive Trading Behavior

Highest trade activity: 61,837 trades

Largest average position size: 7,816 USD

Suggests volatility-driven participation rather than pure optimism

🔹 3. Profitability Driven by Asymmetric Payoffs

Win rates below 50% across all regimes

Positive average PnL indicates larger winning trades outweigh losses

🔹 4. Sell-Side Dominance Across Regimes

SELL trades slightly exceed BUY trades in most sentiment states

Suggests profit-taking or contrarian behavior

🧠 Behavioral Interpretation

Traders appear more volatility-responsive than momentum-biased.
While Extreme Greed delivers the strongest performance, Fear regimes show the highest risk-taking intensity. Neutral conditions provide the weakest edge.

The findings suggest that regime-aware strategy design may significantly improve risk-adjusted returns.

📈 Strategy Recommendations
1️⃣ Volatility-Controlled Exposure in Fear Regimes

Reduce position size caps

Implement tighter risk management rules

2️⃣ Structured Momentum Participation in Extreme Greed

Gradual position scaling

Avoid excessive leverage expansion

3️⃣ Capital Preservation in Neutral Regimes

Reduce trade frequency

Focus on high-conviction setups only

🔮 Optional Extension

A simple classification model was implemented to predict trade profitability using:

Sentiment regime

Position size

Trade characteristics

This demonstrates potential for sentiment-aware predictive modeling.

🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib / Seaborn

Scikit-learn (optional model)

📁 Project Structure
```
Trader-Sentiment-Analysis/
│
├── README.md
|
|── fear_greed_index.csv
|── historical_data.csv
│
├── notebooks/
│   └── sentiment_trader_analysis.ipynb
│
├── output_charts/
│   ├── avg_pnl_by_sentiment.png
│   ├── win_rate_by_sentiment.png
│   ├── trade_count_by_sentiment.png
│   ├── position_size_by_sentiment.png
│   ├── long_short_distribution.png
│   └── drawdown_by_sentiment.png
│
└── summary/
    └── executive_summary.pdf  

  ```   
🎯 Conclusion


Market sentiment materially influences trader behavior and profitability on Hyperliquid.
Extreme Greed environments maximize performance, while Fear regimes amplify risk-taking intensity.

Incorporating sentiment-aware rules into strategy design can improve capital efficiency and reduce volatility exposure.

🚀 How to Run

Clone the repository

Install dependencies

Open notebook.ipynb

Run all cells

👤 Author
Rituraj Singh
Aspiring Data Analyst
📧 Open to Data Analyst & Business Analyst roles


