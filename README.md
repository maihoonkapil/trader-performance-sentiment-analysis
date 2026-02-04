# trader-performance-sentiment-analysis

# Trader Performance vs Market Sentiment (Fear vs Greed)

**Assignment for Data Science Intern – Primetrade.ai**  
Analysis of how Bitcoin Fear & Greed Index relates to trader behavior and performance on Hyperliquid.

## Objective
Investigate whether trader PnL, win rate, trade frequency, position sizing and long/short bias differ between **Fear** and **Greed** market sentiment days, identify behavioral segments, and propose actionable trading rules.

## Datasets
- **Bitcoin Fear & Greed Index** → daily sentiment classification (Fear / Extreme Fear / Greed / Extreme Greed / Neutral)
- **Hyperliquid historical trader data** → per-trade records (211,224 rows) including Account, Closed PnL, Size USD, Side, Timestamp, etc.

Both datasets were provided via Google Drive links in the assignment email.

## Files in this repository
- `Trader_Performance_vs_Market_Sentiment.ipynb`    ← main analysis notebook
- `requirements.txt`                                 ← Python dependencies
- `output/`                                          ← saved charts & tables

## Setup & How to Run
1. Create & activate virtual environment
   python -m venv .venv
   source .venv/bin/activate    # Windows: .venv\Scripts\activate
2. Install dependencies
   pip install -r requirements.txt

3. Download the two CSV files from the assignment links and place them in the root folder (or in data/):
 - fear_greed_index.csv
 - historical_data.csv

4. Open and run the notebook
 jupyter notebook

→ Open Trader_Performance_vs_Market_Sentiment.ipynb and run all cells

Requirements
- Python 3.9–3.11 
- pandas>=2.0
- numpy>=1.24
- matplotlib>=3.7
- seaborn>=0.12
- jupyter

Methodology

Aligned both datasets to daily level using timestamps
Grouped sentiment into Fear / Greed / Neutral
Computed daily trader-level metrics: PnL, # trades, win rate, avg position size, long/short ratio
Segmented traders by frequency (trades/day) and consistency (PnL volatility)
Compared behavior and performance across sentiment regimes.

Main Insights

Traders earn significantly higher average & median PnL during Fear days compared to Greed days.
Trade frequency increases during Fear, but average position size tends to be larger during Greed (overconfidence?).
Frequent traders dominate volume but inconsistent (high PnL variance) traders capture most of the upside during Fear periods.
Long/short ratio is slightly more balanced during Fear → possible hedging behavior.

Actionable Strategy Recommendations

Fear days → selectively increase trade frequency and/or position sizing for inconsistent / high-variance traders (they show strongest PnL in pessimistic regimes).
Greed days → reduce leverage (if available), tighten position sizing, and consider short bias — especially for frequent traders — to protect against euphoria-driven reversals.
