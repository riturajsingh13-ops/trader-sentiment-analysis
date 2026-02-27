📊 Trader Performance vs Market Sentiment Analysis
--
Data Science Intern Assignment – Primetrade.ai
--
📌 Project Overview
--
This project analyzes how Bitcoin market sentiment (Fear & Greed Index) influences trader behavior and performance on Hyperliquid.
Using over 211,000 trade records, the study evaluates how profitability, win rate, trade frequency, position sizing, and directional bias vary across sentiment regimes such as Extreme Fear, Fear, Neutral, Greed, and Extreme Greed.

The objective is to identify behavioral patterns and derive actionable, sentiment-aware trading insights.
--
📂 Dataset Description
--
1️⃣ Fear & Greed Index (fear_greed_index.csv)
--
Date

Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

2️⃣ Historical Trade Data (historical_data.csv)
--
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
--
Cleaned column names and removed duplicates

Corrected timestamp parsing (used Timestamp IST due to corrupted Unix column)

Converted both datasets to daily granularity

Performed inner join on Date

Final merged dataset size: 211,218 rows
--
⚙️ Feature Engineering
--
The following metrics were created:
--
1. Daily PnL per trader

2. Win rate per trader

3. Average trade size

4. Trades per day

5. Long/Short (BUY/SELL) distribution

6. Drawdown proxy (cumulative PnL vs running max)

📊 Key Findings
--
🔹 1. Profitability Peaks During Extreme Greed
--
1. Highest average PnL: 67.89

2. Highest win rate: 46.5%

3. Strong alignment with bullish momentum environments

🔹 2. Fear Regimes Drive Aggressive Trading Behavior
--
1. Highest trade activity: 61,837 trades

2. Largest average position size: 7,816 USD

3. Suggests volatility-driven participation rather than pure optimism

🔹 3. Profitability Driven by Asymmetric Payoffs
--
1. Win rates below 50% across all regimes

2. Positive average PnL indicates larger winning trades outweigh losses

🔹 4. Sell-Side Dominance Across Regimes
--
1. SELL trades slightly exceed BUY trades in most sentiment states

2. Suggests profit-taking or contrarian behavior

🧠 Behavioral Interpretation
--
Traders appear more volatility-responsive than momentum-biased.
While Extreme Greed delivers the strongest performance, Fear regimes show the highest risk-taking intensity. Neutral conditions provide the weakest edge.

The findings suggest that regime-aware strategy design may significantly improve risk-adjusted returns.

📈 Strategy Recommendations
--
1️⃣ Volatility-Controlled Exposure in Fear Regimes
--
1. Reduce position size caps

2. Implement tighter risk management rules

2️⃣ Structured Momentum Participation in Extreme Greed
--
1. Gradual position scaling

2. Avoid excessive leverage expansion

3️⃣ Capital Preservation in Neutral Regimes
--
1. Reduce trade frequency

2. Focus on high-conviction setups only

🔮 Optional Extension
--
A simple classification model was implemented to predict trade profitability using:

1. Sentiment regime

2. Position size

3. Trade characteristics

This demonstrates potential for sentiment-aware predictive modeling.

🛠️ Tech Stack
--
1. Python

2. Pandas

3. NumPy

4. Matplotlib / Seaborn 

📁 Project Structure
--
```
Trader-Sentiment-Analysis/
│
├── README.md
|
|── fear_greed_index.csv
|── historical_data.csv
│
├── notebooks.ipynb
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
--

Market sentiment materially influences trader behavior and profitability on Hyperliquid.
Extreme Greed environments maximize performance, while Fear regimes amplify risk-taking intensity.

Incorporating sentiment-aware rules into strategy design can improve capital efficiency and reduce volatility exposure.

🚀 How to Run
--
1. Clone the repository

2. Install dependencies

3. Open notebook.ipynb

4. Run all cells

👤 Author
--
Rituraj Singh

Aspiring Data Analyst

📧 Open to Data Analyst & Business Analyst roles







