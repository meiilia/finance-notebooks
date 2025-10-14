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

## Run Locally

### 1) Quick start
```bash
# Python 3.10+ recommended
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
jupyter lab  # or jupyter notebook
