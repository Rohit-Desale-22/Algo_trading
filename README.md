# MACD Momentum Slowdown Strategy

This repository contains the backtest report and implementation details of the **MACD Momentum Slowdown Strategy**, tested on **15-minute intraday data of top Indian stocks**.  
The strategy leverages the behavior of the **MACD Histogram** to detect weakening bearish momentum and capture potential short-term reversals.

---

## 📌 Strategy Overview
- **Entry (Buy Signal):**
  - MACD Histogram is negative **and** shows significant slowdown (flattening).
- **Exit (Sell Signal):**
  - Take Profit at **5%**, or  
  - Stop Loss at **2.5%**, or  
  - MACD turns positive with price weakness.

🔹 The aim is to catch **early reversals** in bearish intraday trends with dynamic confirmation.

---

## ⚖️ Risk Management Rules
- Fixed **Take Profit**: 5%  
- Fixed **Stop Loss**: 2.5%  
- Only **one position per stock** at a time (no pyramiding).  
- Entry and exit are executed **within the same day** (intraday only).  

---

## 📊 Backtest Results (15-Minute Data)

| Company   | Total Trades | Win Rate (%) | Avg Return/Trade (%) | Total Return (%) |
|-----------|--------------|--------------|----------------------|------------------|
| RELIANCE  | 35           | 80.00        | 0.30                 | 10.45            |
| INFOSYS   | 32           | 68.75        | 0.50                 | 15.92            |
| HDFC      | 34           | 70.59        | 0.17                 | 5.67             |
| TATA      | 32           | 56.25        | 0.16                 | 5.25             |
| TCS       | 35           | 57.14        | 0.27                 | 9.31             |
| SBI       | 38           | 65.79        | 0.77                 | 29.23            |

---

## 🚀 Possible Improvements
- Refine detection of histogram momentum slowdown.  
- Explore additional indicators (e.g., VWAP, RSI, Volume) to improve confirmation **without reducing trades significantly**.  
- Optimize stop loss/take profit thresholds for better risk-reward ratio.
