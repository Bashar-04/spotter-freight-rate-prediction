# Spotter Freight Rate Prediction Model

This repository contains the end-to-end implementation for predicting spot freight rates for Spotter.

## 📌 Project Overview
The goal of this project is to build a high-precision LightGBM regression model to predict spot market rates while preventing temporal data leakage.

## 📊 Key Results
- **Validation MAE:** ~$142.73
- **Validation RMSE:** ~$643.34
- **Validation Dataset Size:** 12,000 predictions
- **December Forecasts:** 31 daily predictions for Lexington -> Fort Wayne lane

## 🛠️ Tech Stack & Methodology
- **Libraries:** Python, LightGBM, Pandas, Scikit-Learn
- **Validation Strategy:** Strict time-based split (Train: pre-Sept 2025, Validation: post-Sept 2025)
- **Features Engineered:** Temporal features (day of week, seasonality), lane encodings (`pickup -> delivery`), and `weight_per_mile`.

## 📁 Submission Files
- `freight_rate_prediction.ipynb`: Main model training & prediction notebook.
- `validation_predictions.csv`: Model predictions for the validation set.
- `december_chart_inputs.csv`: Daily December rate forecasts.
- `candidate_december.png`: Generated chart output from `score.py`.
- `Spotter_Freight_Rate_Prediction_Report.pdf`: Final technical report.
