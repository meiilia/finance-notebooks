# Finance Notebooks — Tutorials

**Who is this for?**  
- **Track A (Finance → Code):** finance students who want a practical Python toolkit (pandas, numpy, matplotlib) to analyze returns and risk.  
- **Track B (Code → Finance):** developers/data learners who want the essential finance concepts (returns, compounding, annualization, volatility, Sharpe, drawdowns).

---

## Notebook 01 — How to Analyze Financial Returns in Python

**TL;DR.** Use `pct_change()` for returns, compound with `(1+R).prod()-1`, annualize consistently (**returns** by compounding, **volatility** by √N), and always report **risk** (volatility, Sharpe, **max drawdown**) next to performance.

### What you’ll learn
- From **prices to returns**: simple vs **log** returns, `shift(1)` vs `DataFrame.pct_change()`  
- **Compounding** & **annualizing** returns (daily/monthly/quarterly; `periods_per_year` param)  
- **Exploratory risk**: summary stats, histograms, **rolling mean/volatility**  
- **Sharpe ratio** (annualized) with a clear convention (√N)  
- **Drawdown** & **max drawdown** to capture depth of losses  
- A **one-page metrics table**: Mean, Vol, Sharpe (annualized), Total Return, Ann. Return, Ann. Vol, Max DD

### Screenshots / Outputs
- Price levels and bar charts of period returns  
- Histograms for BLUE/ORANGE  
- Rolling 21-period mean and volatility  
- Drawdown plots per asset  
- Metrics table (rounded)

---

## Notebook 02 — Deviations from Normality: Skewness, Kurtosis & Tail Risk

**TL;DR.** Real-world returns are *not normal*. This notebook explores **asymmetry (skewness)**, **fat tails (kurtosis)**, and **non-parametric risk measures** (VaR, CVaR, semideviation) using the **EDHEC Risk Institute hedge-fund dataset**.

### What you’ll learn
- Why Gaussian assumptions fail in finance (2008, Black Monday, etc.)  
- **Skewness & Median–Mean gap** to detect asymmetric loss profiles  
- **Kurtosis** and fat-tail effects → frequency of extreme events  
- **Jarque–Bera test** for normality (and how to interpret p-values)  
- **VaR models**: historical, Gaussian, Cornish–Fisher (adjusted for skew/kurtosis)  
- **CVaR (Expected Shortfall)** & **semideviation** for true downside risk  
- **Rolling analysis**: time-varying skewness, kurtosis & volatility (24-month window)  
- **Portfolio dashboards**: correlation heatmaps, risk–return scatterplots, higher-moment mapping  

### Financial takeaways
- Traditional mean-variance models underestimate tail risk  
- High negative skew → exposure to “crash” risk  
- Leptokurtic distributions demand CVaR-based risk budgeting  
- Basel III → shift from VaR to Expected Shortfall (ES)  
- Combining strategies with opposite skews improves portfolio stability  

### Screenshots / Outputs
- QQ plots (empirical vs. normal quantiles)  
- Rolling skew/kurtosis charts for top strategies  
- VaR comparison bars (Historical vs Gaussian vs Cornish–Fisher vs CVaR)  
- 2D risk–return scatter colored by skewness (bubble size = kurtosis)  
- Summary table of all statistical moments + Jarque–Bera results  

---

## Run Locally

### 1) Quick start
```bash
# Python 3.10+ recommended
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
jupyter lab  # or jupyter notebook
