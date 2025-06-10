# EconoCast v2: Multivariate LSTM for Time Series Forecasting

EconoCast v2 is a deep learning model built using Keras that predicts future stock prices (e.g., Tesla - TSLA) using historical multivariate time series data. This project demonstrates advanced time series forecasting using LSTM (Long Short-Term Memory) neural networks, incorporating multiple financial indicators to enhance prediction accuracy.

---

## Project Highlights

- **Multivariate LSTM Model**: Uses historical prices and technical indicators like RSI, MACD, Moving Averages, etc.
- **Low Forecasting Error**: Achieves strong accuracy with low MAE and RMSE.
- **Built with Deep Learning**: Trained using Keras + TensorFlow backend.
- **Real-world Dataset**: Yahoo Finance stock data (TSLA) with full preprocessing pipeline.
- **Visualized Performance**: Includes training/validation loss curves and predicted vs actual stock price charts.

---

---

## 🔢 Model Details

| Feature | Description |
|--------|-------------|
| Model  | Multivariate LSTM |
| Layers | 2 LSTM layers (64 → 32) + Dropout + Dense(1) |
| Input Features | `Close`, `MA20`, `RSI`, etc. |
| Output | Next-day `Close` price |
| Sequence Length | 30 days |
| Epochs | 15 |
| Loss | MSE |
| Optimizer | Adam |

---

## 📈 Performance

| Metric | Value |
|--------|-------|
| MAE (Mean Absolute Error) | **11.47** |
| RMSE (Root Mean Squared Error) | **15.76** |
| Best val_loss | **0.0011** |

---

