# Hi, I'm Matthieu 👋

**kdb+/q developer & quant data engineer** — tick data, market microstructure, derivatives pricing.

- 🎓 **Executive Program in Financial Engineering — Sorbonne Université** (Nov 2026 – Jul 2027): stochastic calculus, Monte Carlo methods, high-frequency trading & microstructure, machine learning
- 💼 10 years in data & pricing, 5 of them in financial markets: OTC operational risk at **Société Générale**, gas forward pricing on an **energy trading desk**
- 🏅 **KX certified**: q Developer Level 2 · KDB-X Python Level 2 (+ KDB.AI Vector Database and PyKX courses)
- 🔎 **Open to** an internship / part-time role in capital markets or commodities — Paris, Mon–Thu, from November 2026

---

## Featured projects

| Project | What it does | Key result |
|---|---|---|
| [**Hawkes quote simulator**](https://github.com/matthieu-briche/kdb-hawkes-quote-simulator) · q | End-to-end model of clustered quote arrivals for microstructure analysis: branching simulation, MLE calibration, statistical validation | ~530k quotes/day on 5 symbols, fully vectorised (no loops) · 95% CI coverage of 94/96/92% over 50 fits |
| [**Real-time tick architecture**](https://github.com/matthieu-briche/kdb-q-tick-data-analytics) · q, PyKX | Tickerplant → RDB → HDB with chained TP, real-time engine publishing aggregates, real-time/historical gateway, VWAP & volatility APIs | Compressed HDB of 6.4M rows |
| [**Execution quality & TCA**](https://github.com/matthieu-briche/kdb-execution-quality-tca) · q | Best-ex and slippage via as-of joins, markouts from 1s to 5min, 15-min buckets, anomaly detection | ~157k NBBO updates, 10,000 executions across 5 brokers and 4 venues |
| [**Options pricer**](https://github.com/matthieu-briche/python-options-pricing) · Python | Vanilla options pricer validated against QuantLib and real market data | 94.3% of a real AAPL option chain repriced inside the bid-ask |
| [**Microstructure clustering**](https://github.com/matthieu-briche/python-microclust) · Python | Clusters assets on how their order book works (order-sign memory, impact, tick regime), not on returns, and tests whether the clusters predict strategy transferability; hypotheses fixed before looking at real data | Families recovered on synthetic data (ARI 0.84) · pipeline runs end to end on Binance spot |
| [**Hawkes limit order book**](https://github.com/matthieu-briche/python-lob-modelling) · Python | Order book driven by a bivariate buy/sell Hawkes process (Ogata thinning), recursive-likelihood MLE, analysis dashboard | Bivariate fit removes the μ bias of a univariate fit (2.43 → 2.03, true 2.0) · CI on Python 3.10–3.13 |

### Validation, not just code
The Hawkes simulator is checked with the **time-rescaling theorem** (KS test on compensator residuals), autocorrelation and **Fano factor**; the 10-day HDB is date-partitioned (`.Q.dpft`, `p#` on `sym`) with as-of joins on a 1 ms grid and x60 accelerated replay.

---

## Certifications

<p>
  <a href="assets/certif-q-developer-l2.png"><img src="assets/certif-q-developer-l2.png" alt="KX q Developer Level 2" height="130"></a>
  <a href="assets/certif-kdbx-python-l2.png"><img src="assets/certif-kdbx-python-l2.png" alt="KX KDB-X Python Level 2" height="130"></a>
  <a href="assets/certif-kdbai.png"><img src="assets/certif-kdbai.png" alt="KX KDB.AI Vector Database" height="130"></a>
  <a href="assets/certif-pykx.png"><img src="assets/certif-pykx.png" alt="KX Introduction to PyKX" height="130"></a>
</p>

**q Developer Level 2** (Mar 2026) · **KDB-X Python Level 2** (Mar 2026) · KDB.AI Vector Database (Oct 2024) · Introduction to PyKX (Oct 2024)

---

## Tech stack

**kdb+/q** · qSQL · as-of joins · IPC · tick architecture · attributes & query optimisation · PyKX
**Python** (pandas, NumPy, pytest, scikit-learn, Prophet) · **SQL** · R · BigQuery · ETL pipelines · Git · Linux · Bash

**Quant**: Black–Scholes · SABR · short-rate models (CIR, OU) · Hawkes processes · maximum likelihood · Monte Carlo · stochastic calculus · vanilla derivatives (swaps, options, forwards)

---

## Background

- **M2 Applied Mathematics & Quantitative Finance** — Université de Lille (top 5%), 2016 · thesis: simulation of fractional Brownian motion and Hurst exponent estimation
- **Data engineer**, fuel distribution group (23 subsidiaries, 150 stations) — sales forecasting engine in Python, daily price & volume time series
- **Gas pricing analyst**, energy trading — multi-maturity forward pricing models (month / quarter / semester) with Reuters market data, daily P&L and position reporting

📚 Currently reading: *Q Tips* (Psaris) · *Algorithmic and High-Frequency Trading* (Cartea) · *Trades, Quotes and Prices* (Bouchaud)

---

📫 [LinkedIn](https://linkedin.com/in/matthieu-briche-aa69b441) · matthieu.briche@gmail.com
