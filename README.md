# 💹 Alpha Strategy: Trend Detection and Trade Strategy Builder

This project showcases a **trading strategy** designed to **maximize alpha** (excess returns over a benchmark) using historical price data. Leveraging a **dual moving average (SMA) crossover technique**, it optimizes entry and exit points while focusing on **maximizing the Sharpe Ratio** 📊 to balance **risk and reward**.

🏆 Honored Recognition: This strategy was privileged to secure First Prize at the IIT Bombay hackathon, sponsored by Dhan, for its effective performance and clear methodology. 🙏✨

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

---

Output:

📝 Trade details saved in a CSV file (trades.csv).

📊 Sharpe ratio displayed in the console.

---

📊 Results

Sharpe Ratio: Quantifies the strategy's risk-adjusted performance.

Trade Details: Logs entry/exit prices, dates, quantities, and profit/loss for each trade in a CSV file.

---

Example Output

Trade Details (Saved in trades.csv):

| Entry Date   | Exit Date    | Entry Price | Exit Price | Quantity | P/L  |
|--------------|--------------|-------------|------------|----------|------|
| 2021-03-01   | 2021-03-05   | 150.00      | 155.00     | 100      | 500  |
| 2021-03-10   | 2021-03-15   | 200.00      | 208.00     | 50       | 400  |

