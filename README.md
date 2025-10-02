# F1 Finish Predictor  

*A machine learning pipeline for pre-race prediction of Formula 1 driver results using historical data, feature engineering, and probabilistic simulation.*  

---

## Overview  
This project builds an end-to-end predictive modeling workflow to forecast Formula 1 race outcomes **before the race begins**.  
We focus on predicting **driver points** and **finish probabilities** based only on pre-race information such as grid order, driver/team form, and season progress.  

---

## Features  
- **Data preprocessing**: categorical encoding, scaling, leakage control.  
- **Feature engineering**: exponentially decaying form for drivers and teams, grid advantage, season progress.  
- **Modeling**: LightGBM and XGBoost gradient boosting regressors.  
- **Backtesting**: rolling time-series validation to mimic real-world forecasting.  
- **Simulation**: Monte Carlo runs to estimate probabilities for win, podium, and top-10 finishes.  

---

## Results  
- **Baseline (driver historical average)**: R² ≈ 0.46  
- **LightGBM**: R² ≈ 0.57, MAE ≈ 3.125 points  
- **XGBoost**: R² ≈ 0.59, MAE ≈ 2.983 points  
- Captures expected pre-race performance but not unpredictable events (DNFs, crashes, safety cars).  

---

## Limitations  
- Predictions rely only on **pre-race data**.  
- Cannot account for **unpredictable race-day events** (crashes, safety cars, DNFs).  
- Forecast accuracy ceiling of around **R² ≈ 0.60**.  

---

## Future Work  
- Integrate **qualifying sector times** and **track-specific performance**.  
- Model the **probability of DNFs** explicitly.  
- Add **betting odds** or other external signals for more realistic uncertainty.  
- Extend to **live race simulations**.  
