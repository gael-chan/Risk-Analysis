# Risk-Analysis
# 📉 SMM272 – Risk Analysis Coursework (2024/25)

**Abstract**  
This project investigates financial risk modelling through Value-at-Risk (VaR) forecasting, portfolio construction techniques, and bond risk estimation using both analytical and simulation-based methods. We address Questions 1, 2, and 3 from the Risk Analysis coursework, implementing parametric, non-parametric, and Monte Carlo frameworks using Python. Key outputs include VaR backtesting using Christoffersen tests, comparative performance of Risk Parity vs Diversification strategies, and delta-gamma based bond risk measures. The work critically evaluates the limitations of model assumptions and the robustness of alternative risk estimation approaches.

---

## ✅ Covered Questions

### 📊 Question 1 – Portfolio VaR Modelling
- **Assets**: AAPL, MSFT, IBM, NVDA, GOOGL, AMZN (2014–2024)
- **Tasks**:
  - Return statistics and distributional tests (skewness, kurtosis, Jarque-Bera)
  - VaR forecasts using:
    - Parametric (Normal)
    - Parametric (t-Distribution)
    - Delta-Gamma Approximation
    - Non-Parametric Bootstrap
    - Bottom-Up Monte Carlo (RiskMetrics)
  - **Backtesting**:
    - VaR Violations Count
    - Unconditional & Conditional Coverage Tests
    - Distributional Test (transformed probability histogram)
- **Insights**:
  - Normal distribution underestimates tail risk
  - Bootstrap VaR captures leptokurtic behaviour but lags recent volatility
  - Monte Carlo with EWMA provides adaptive risk estimation

---

### 📈 Question 2 – Risk Parity and Portfolio Construction
- **Portfolios**:
  - Risk Parity Portfolio (RPP)
  - Maximum Diversification Portfolio (MDP)
  - Equally-Weighted Portfolio (EWP)
- **Steps**:
  - Component VaR and Conditional VaR using parametric and non-parametric methods
  - Out-of-sample backtesting using:
    - Sharpe Ratio
    - Maximum Drawdown
    - VaR Violations
    - Skewness & Excess Kurtosis
- **Insights**:
  - MDP has highest Sharpe ratio but largest drawdowns
  - RPP shows more balanced risk allocation
  - EWP has high simplicity but suboptimal tail risk control

---

### 💵 Question 3 – Bond VaR Estimation
- **Bond Parameters**:
  - Face Value: 100 | Maturity: 10 years | Coupon: 5% | Current Price: 99
  - YTM volatility: σ = 0.006 (daily, i.i.d. normal)
- **VaR Methods Compared**:
  1. Exact (Full Revaluation)
  2. Delta Approximation
  3. Delta-Gamma Approximation
  4. Monte Carlo (Delta / Delta-Gamma / Full)
- **Expected Shortfall**: Estimated via Monte Carlo Full Revaluation
- **Insights**:
  - Delta-Gamma improves curvature estimation but underestimates tail losses over long horizons
  - Full revaluation captures convexity effects more accurately

---

## 📁 Repository Structure

```bash
risk-analysis-cw/
├── Question1.ipynb             # Portfolio VaR modelling & backtesting
├── Question2.ipynb             # Portfolio construction and performance evaluation
├── Question3.ipynb             # Bond VaR and ES via analytical and simulation methods
├── DataQ2.xlsx                 # Data used in portfolio optimisation (Q2)
├── Risk_Analysis_CW-6_merged.pdf # Final coursework report
├── CourseWork_QF_MTF_FM_QF_2024_25-3.pdf # Official coursework instructions
├── README.md                   # Coursework overview (this file)
```

---


## 👨‍👩‍👦‍👦 Authors

- Gael Chen  
- Theo Cadier  
- Lorenzo Rossi  
- Stéphane Leboyer  

*City, University of London – MSc Quantitative Finance*

---

## 📚 Key References

- Jorion, P. (2012). *Value at Risk: The New Benchmark for Managing Financial Risk*
- Ballotta & Fusai (2017). *A Gentle Introduction to Value at Risk*
- Glasserman, P. (2003). *Monte Carlo Methods in Financial Engineering*
- Christoffersen, P. (2003). *Elements of Financial Risk Management*

---
