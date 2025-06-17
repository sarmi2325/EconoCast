# EconoCast v1 — Univariate forecasting for Tesla Stock by Linear Regression


Forecast the **next day’s closing price** of Tesla using past values and time-based features. This is a **univariate, single-step, supervised forecasting** task.

---

##  Pipeline Overview

1. **Data Preparation**
   - Parse dates, set `Date` as index
   - Sort chronologically
   - Create lag features (1, 2, 3, 7 days)
   - Create rolling window features (mean & std)
   - Add time-based features: `day_of_week`, `month`, `is_weekend`

2. **Train-Test Split**
   - Time-based split (e.g., last 30 days as test)

3. **Modeling**
   - Linear Regression from `sklearn`
   - Evaluation metrics: **RMSE** and **MAE**

---

##  Feature Engineering

| Feature             | Description                                 |
|---------------------|---------------------------------------------|
| `lag_1`, `lag_7`    | Previous stock prices                       |
| `rolling_mean_3`    | Moving average over 3 days                  |
| `rolling_std_3`     | Rolling std deviation over 3 days           |
| `dayofweek`, `month`| Time-based seasonality indicators           |
| `is_weekend`        | Binary weekend flag                         |

---

##  Model Evaluation (Baseline)

- **Model**: Linear Regression
- **RMSE**: 6.24
- **MAE**: 4.41

---

##  Feature Importance

Feature importance is visualized using the absolute value of coefficients from the linear model.
