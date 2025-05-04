# 📊 Sector-Neutral Pairs Trading Strategy (2020–2025)

A **personally developed**, market-neutral, long/short strategy that systematically exploits short-term mispricings between correlated stock pairs. 
Built to demonstrate core statistical arbitrage and risk hedging principles using clean, readable Python code — no external backtesting libraries.

---

## 📌 Strategy Overview

This model forms **long/short positions** on sector-aligned stock pairs when their price ratio diverges by more than **3%** from their historical mean. It then **rebalances** the positions toward the mean, assuming convergence.

| **Component**       | **Description**                                    |
| ------------------- | -------------------------------------------------- |
| Tickers Used        | 11 stock pairs (e.g., JPM vs BAC, XOM vs CVX)      |
| Selection Method    | Sector alignment + visual correlation              |
| Entry Condition     | Pair spread exceeds ±3%                            |
| Rebalance Frequency | Daily check, rebalance when condition met          |
| Sizing Method       | Dollar-neutral (equal capital long/short per pair) |
| Weighting           | Equal-weight across all 11 pairs                   |

---

## 🧪 Strategy Logic

* 📈 **Historical Mean Spread**: Track price ratio of each pair over a lookback window.
* ⚡ **Divergence Trigger**: Enter position when current spread deviates ≥ 3% from the mean.
* ⟳ **Mean Reversion Bet**: Go long undervalued and short overvalued side of the pair.
* ⚖️ **Neutral Exposure**: Pairs are structured to have minimal directional market risk.
* 🌐 **Portfolio Aggregation**: Pairs return streams are combined into a unified equity curve.

---

## 📊 Backtest Summary (2020–2025)

| **Metric**   | **Value** |
| ------------ | --------- |
| CAGR         | 18.6%     |
| Sharpe Ratio | 0.86      |
| Max Drawdown | 32%       |
| Pairs Used   | 11        |

📊 Portfolio Equity Curve vs SPY

> \[Insert `Sector_Pairs_Equity_Curve.jpg` here]

---

## 🛠️ Tech Stack

* `pandas` — pairwise spread tracking
* `numpy` — statistical divergence
* `matplotlib` — plotting equity curves
* `yfinance` — stock data
* All logic fully implemented using native Python (no QuantConnect / Zipline / bt)

---

## 🎯 Key Learnings & Skills Demonstrated

| Skill Area              | Evidence                                                          |
| ----------------------- | ----------------------------------------------------------------- |
| Mean Reversion Strategy | Developed full reversion-based entry/exit logic                   |
| Statistical Arbitrage   | Defined pairwise divergence and convergence signals               |
| Market Neutrality       | Constructed beta-minimized portfolios via equal-dollar offsetting |
| Dynamic Positioning     | Capital is deployed per spread condition in real-time             |
| Risk Management         | Evaluated with Max Drawdown, Sharpe, CAGR; controlled exposure    |

---

## 🏦 Why It Matters for Recruiters & PMs

| Target Signal           | Value Delivered                                                       |
| ----------------------- | --------------------------------------------------------------------- |
| Quant / Statistical PMs | Real alpha-generation logic rooted in spreads and reversion           |
| Buy-side Analysts       | Strategy scalability, sector insights, pair dependency mapping        |
| Recruiters              | Python fluency + risk/return thinking + cleaner-than-most codebase    |
| Interview Storytelling  | Can walk through end-to-end: asset selection, logic, results, lessons |

---

## 💡 Project Highlights

> Engineered and tested **11 sector-aligned stock pairs** with a 3% reversion trigger.
>
> Portfolio delivered **18.66% CAGR** with **0.86 Sharpe Ratio** and **32.3% Max Drawdown**, outperforming SPY in **risk-adjusted terms** while maintaining beta neutrality.

---

## 📖 Run It Yourself

1. Clone the repo:

   ```bash
   git clone https://github.com/your-username/Sector-Neutral-Pairs-Trading.git
   ```
2. Navigate inside:

   ```bash
   cd Sector-Neutral-Pairs-Trading
   ```
3. Install dependencies:

   ```bash
   pip install pandas numpy yfinance matplotlib
   ```
4. Run Jupyter Notebook:

   ```bash
   jupyter notebook Sector_Pairs_Strategy.ipynb
   ```

---

## 📷 Files to Include on GitHub

* `Sector_Pairs_Strategy.ipynb`
* `Sector_Pairs_Equity_Curve.jpg` (equity chart)
* `README.md` (this file)

---

## ✉️ Disclaimer

This repository is for **educational and demonstration purposes only**. This does **not constitute financial advice** or a recommendation to trade. Please consult a financial advisor before making any investment decisions.

---

