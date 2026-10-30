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
| [**Real-time tick platform & dashboard**](https://github.com/matthieu-briche/kdb-realtime-tick-dashboard) · q | kdb+tick written from scratch (feed, TP, RDB, RTE, HDB, gateway) with a live trading dashboard; incremental RTE analytics (OHLC, VWAP, notional, top of book); one gateway port serving q IPC (KX Dashboards, PyKX), HTTP and WebSocket | No data loss: daily TP log replayed on restart · automatic EOD to a date-partitioned HDB · dashboard queries cost O(symbols), not O(ticks) |
| [**fi-algo: TorQ framework**](https://github.com/matthieu-briche/fi-algo) · q, TorQ | TorQ pipeline (segmented and chained TPs, RDB, WDB, HDB, gateway) fed by simulated government bonds on Ornstein–Uhlenbeck yield curves; fixed-income library in q (cash flows, accrued interest, price/yield, Newton–Raphson); rolling VWAP/TWAP | 12 government bonds (UST, Bunds, OATs) · qspec CI |
| [**Day-ahead power price forecasting**](https://github.com/matthieu-briche/power-price-forecasting) · Python | Hourly day-ahead price forecasts for the German power market (DE-LU): residual load, merit-order features, D-1/D-7 price lags; naive EPF benchmark, LEAR-style ridge and gradient boosting; walk-forward back-test with weekly retraining; forecasts valued economically through a 1 MW / 2 MWh battery strategy settled at realised prices; MongoDB, Docker, CI with leakage tests | Gradient boosting cuts MAE by 71% vs the naive benchmark and captures 97.6% of perfect-foresight battery PnL (synthetic data; real-market run via `make real`) |
| [**Tick-data analytics platform**](https://github.com/matthieu-briche/kdb-q-tick-data-analytics) · q, PyKX | Full tick stack driven from Python (feed handler, TP, RDB, chained TP, RTE, HDB, gateway) fed by Hawkes-simulated quotes (vectorised NumPy); throttled real-time analytics (VWAP, spread in bps, live quote rate); gateway APIs for OHLC bars (`xbar`), slippage to mid (`aj`) and realised volatility | Compressed HDB of 6.4M rows · query-tuning benchmarks · CI on q and pytest suites |
| [**Hawkes quote simulator**](https://github.com/matthieu-briche/kdb-hawkes-quote-simulator) · q | End-to-end modelling of clustered quote arrivals: branching-representation simulation fully vectorised in q (no explicit loops); MLE calibration with an O(n) log-likelihood and Nelder–Mead; goodness of fit via time-rescaling (KS test), autocorrelation and Fano factor | ~530k quotes/day across 5 symbols · 10-day date-partitioned HDB (`.Q.dpft`, `p#` on sym), `aj` on a 1 ms grid, x60 replay · 50 fits, 95% CI coverage of 94% / 96% / 92% for (μ, α, β) |
| [**Options pricer**](https://github.com/matthieu-briche/python-options-pricing) · Python | Vanilla options pricing engine with Greeks, validated against QuantLib | 94.3% of a real AAPL option chain repriced within the bid–ask spread |
| [**Execution quality & TCA**](https://github.com/matthieu-briche/kdb-execution-quality-tca) · q · KX Academy capstone | Best-execution and slippage analysis via `aj`; markouts from 1 s to 5 min; 15-min buckets (`xbar`); anomaly detection (`fby`), `lj`, correlations and IPC to a reference service | ~157k simulated NBBO updates · 10,000 executions (5 brokers, 4 venues) |

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

**kdb+/q** · qSQL · as-of joins · IPC · tick architecture · attributes & query optimisation · TorQ · PyKX
**Python** (pandas, NumPy, pytest, scikit-learn, Prophet) · **SQL** · R · BigQuery · ETL pipelines · Git · Linux · Bash · MongoDB · Docker

**Quant**: Black–Scholes · SABR · short-rate models (CIR, OU) · Hawkes processes · maximum likelihood · Monte Carlo · stochastic calculus · vanilla derivatives (swaps, options, forwards)

---

## Background

- **M2 Applied Mathematics & Quantitative Finance** — Université de Lille, 2016 · thesis: simulation of fractional Brownian motion and Hurst exponent estimation
- **Data engineer**, fuel distribution group (23 subsidiaries, 150 stations) — sales forecasting engine in Python, daily price & volume time series
- **Gas pricing analyst**, energy trading — multi-maturity forward pricing models (month / quarter / semester) with Reuters market data, daily P&L and position reporting

📚 Currently reading: *Q Tips* (Psaris) · *Algorithmic and High-Frequency Trading* (Cartea) · *Trades, Quotes and Prices* (Bouchaud)

---

📫 [LinkedIn](https://linkedin.com/in/matthieu-briche-aa69b441)
