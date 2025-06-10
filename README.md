# EconoCast v1 — Univariate LSTM for Tesla Stock Forecasting

EconoCast is a deep learning-based time series forecasting project focused on predicting the next-day **Tesla (TSLA)** stock closing price using an LSTM model.

This version uses only the **historical closing price** (Univariate LSTM) to establish a strong foundational model, showcasing both technical understanding and model interpretability.

---

## Problem Statement

> Can we forecast the next day's Tesla stock closing price using only its past price history?

Traditional models like ARIMA and moving averages rely on stationarity or limited memory. LSTM (Long Short-Term Memory) networks, on the other hand, **learn patterns from sequential data** by maintaining long-term dependencies, making them ideal for stock forecasting.

---

## Data Source

- Source: [Yahoo Finance](https://finance.yahoo.com/)
- Ticker: `TSLA`
- Duration: 2018–2024 (daily data)
- Features used in this version: only `Close`

---

## Workflow Summary
## Data Collection

Download historical stock data (Close price of TSLA) using yfinance.

## Preprocessing

Normalize the close prices using MinMaxScaler.

Create sequences: Use past 60 days to predict the next day.

## Train-Test Split

Split the time series into 80% training and 20% testing (no shuffling!).

## Model Building (Keras)

Layers:

LSTM(50 units)

Dropout(0.2)

Dense(1 output)

Loss: MSE, Optimizer: Adam

## Model Training

Train for 10 epochs with batch size 32.

## Evaluation

Predict on test set.

Inverse scale predictions.

Calculate MAE & RMSE.

## Visualization

Plot training/validation loss.

Plot actual vs predicted prices.

## Results

MAE: ~13.82

RMSE: ~18.17

---
