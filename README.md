# PrimeTrade.ai Internship Assignment

## Bitcoin Market Sentiment x Trader Performance

This repository contains an end-to-end analysis of how Bitcoin market sentiment (Fear & Greed Index) relates to real Hyperliquid trader outcomes, from cleaning and exploratory analysis to behavior mining and ML modeling.

## Final Deliverables

- Analysis report: [outputs/reports/profile_report.html](outputs/reports/profile_report.html)
- Clean merged dataset used across notebooks: [outputs/merged_clean.csv](outputs/merged_clean.csv)
- Generated figures folder: [outputs/figures](outputs/figures)

## Key Insights

- Traders show higher average PnL during Greed phases.
- Extreme Fear is the most volatile regime (high risk, high reward).
- Contrarian behavior (buying fear/selling greed) is associated with stronger outcomes.
- Sentiment transition windows carry meaningful signal for trade performance.
- ML results show sentiment-derived variables remain among top predictive features.

## Project Layout

```text
Primade_ai_internship/
	data/
		fear_greed_index.csv
		historical_data.csv
	notebooks/
		01_data_cleaning.ipynb
		02_eda_analysis.ipynb
		03_sentiment_correlation.ipynb
		04_pattern_mining.ipynb
		05_ml_model (1).ipynb
	outputs/
		merged_clean.csv
		fear_greed_clean.csv
		figures/
		reports/
			profile_report.html
		models/
	requirements.txt
	README.md
```

## Reproducible Run Order

Run notebooks in this exact order so each notebook consumes the previous output:

1. [notebooks/01_data_cleaning.ipynb](notebooks/01_data_cleaning.ipynb)
2. [notebooks/02_eda_analysis.ipynb](notebooks/02_eda_analysis.ipynb)
3. [notebooks/03_sentiment_correlation.ipynb](notebooks/03_sentiment_correlation.ipynb)
4. [notebooks/04_pattern_mining.ipynb](notebooks/04_pattern_mining.ipynb)
5. [notebooks/05_ml_model (1).ipynb](notebooks/05_ml_model%20(1).ipynb)

## Local Setup

```bash
pip install -r requirements.txt
jupyter notebook
```

Then open the notebooks above and run all cells in order.

## Datasets

| Dataset | Approx Rows | Time Window | Notes |
| --- | ---: | --- | --- |
| Fear & Greed Index | 2,644 | 2018-2025 | Daily market sentiment |
| Hyperliquid historical trades | 211,224 | 2024 | Account-level realized trade data |
| Merged analytical table | ~211,200 | 2024 | Trade rows with joined sentiment context |

## Result Snapshot

| Metric | Outcome |
| --- | --- |
| Overall trader win rate | ~83% |
| Best performing sentiment regime | Greed |
| Most volatile regime | Extreme Fear |
| Sentiment vs PnL relationship | Statistically significant |
| XGBoost ROC-AUC (approx.) | 0.75+ |

## Submission Note

This repository is prepared as the final internship submission artifact, including notebooks, generated outputs, and report.
