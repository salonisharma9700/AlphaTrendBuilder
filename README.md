# 💹 Alpha Strategy: Trend Detection and Trade Strategy Builder

This project showcases a **trading strategy** designed to **maximize alpha** (excess returns over a benchmark) using historical price data. Leveraging a **dual moving average (SMA) crossover technique**, it optimizes entry and exit points while focusing on **maximizing the Sharpe Ratio** 📊 to balance **risk and reward**.

🏆 **Award-Winning Implementation**: This strategy secured **First Prize** in a hackathon for its exceptional performance and methodology! 🎉

---

## 🌟 Features

- 📈 **Dual Moving Average Crossover Strategy**: 
  - Combines fast (10-period) and slow (50-period) SMAs to generate buy/sell signals.
- ⚠️**Risk Management**: 
  - Implements **stop-loss (2%)** and **take-profit (4%)** mechanisms for trades.
- 📊**Sharpe Ratio Calculation**: 
  - Evaluates the strategy's risk-adjusted returns.
- 🛠️ **Backtesting Framework**: 
  - Simulates historical performance on OHLCV data.
- 🌐 **Generalizable**: 
  - Adapts to any instrument provided in the same data format.

---

## 📥 Input
- **Historical Price Data**: 
  - OHLCV (Open, High, Low, Close, Volume) data for selected instruments from **2019 to 2022**.
  - Includes data for **30 instruments** in CSV format.

---

## 📋  Strategy Overview
1. **📊 Indicators**: 
   - **Fast SMA**: 10-period moving average.
   - **Slow SMA**: 50-period moving average.
2. **🚦 Entry/Exit Logic**:
   - **Buy**: When the fast SMA crosses **above** the slow SMA.
   - **Sell**: When the fast SMA crosses **below** the slow SMA.
3. **⚠️ Risk Management**:
   - **Stop-loss**: Limits losses to **2%** of trade value.
   - **Take-profit**: Secures gains at **4%** of trade value.

---

## 📈 Sharpe Ratio
The **Sharpe Ratio** evaluates the strategy's **risk-adjusted return**.  

🧮 **Formula**:  
\[ \text{Sharpe Ratio} = \frac{\text{Annualized Return} - \text{Risk-Free Rate}}{\text{Annualized Volatility}} \]

---

## 🚀 How to Use
### ✅ Prerequisites
-  **Python 3.7** or above
-  Required libraries: `pandas`, `numpy`, `backtesting`, `os`
