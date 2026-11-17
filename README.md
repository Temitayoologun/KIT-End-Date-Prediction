# KIT-End-Date-Prediction
Predicting KIT completion dates using historical sales order data and machine learning.

## Project Overview

This case study explores how accurately KIT completion dates can be predicted using historical sales order data. The objective was to estimate the number of days between KIT start and completion and assess whether machine learning could improve on a simple one-day prediction baseline.

The analysis includes data cleaning, exploratory data analysis, feature engineering, model development, chronological validation, and error analysis.

## Approach

- Cleaned historical KIT records and investigated inconsistent completion dates.
- Aggregated family-level records into order-level features.
- Established a one-day baseline for comparison.
- Trained and evaluated Decision Tree and Random Forest models.
- Tested additional features, including expected processing minutes, capacity, and product-family information.
- Evaluated predictions on later orders to assess performance over time.

## Key Results

| Model | Validation ±1 Day | Test ±1 Day |
|---|---:|---:|
| One-day baseline | 81.76% | 78.33% |
| Original Random Forest | 85.16% | 78.68% |
| Random Forest V4 | 86.10% | 78.99% |

Although the machine learning models improved within-one-day accuracy slightly, the one-day baseline achieved the lowest test mean absolute error.

The analysis also identified challenges related to unusually long KIT durations, changes in completion times over time, and data-quality issues.

## Repository Files

- **TemitayoOlogun_DS_Case_JupyterNotebook_2026.ipynb** — Main notebook containing the complete analysis, model development, evaluation, and prediction generation.
- **TemitayoOlogun_DS_Case_Summary_2026.pdf** — Two-page summary of findings, limitations, and recommendations.
- **TemitayoOlogun_DS_Case_Predictions_2026.npy** — Final predicted KIT completion dates in the original inference-row order.
- **TemitayoOlogun_DS_Case_Supporting_2026.csv** — Predicted KIT completion dates alongside sales order IDs for easier inspection.

## Reproducibility

The original datasets are not included in this public repository because they were provided for the case study.

The notebook requires the supplied input files and a Python environment with the relevant libraries. Local file paths must be updated before running the analysis on another computer.

## Conclusion

The results suggest that additional operational information and better handling of long-running orders may be more valuable than simply increasing model complexity. The predictions should be treated as planning estimates rather than guaranteed completion dates.
