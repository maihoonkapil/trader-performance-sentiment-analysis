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
