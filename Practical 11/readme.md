# Sunspot Statistical Analysis — README

## 📌 Project Overview
This project analyzes the **Monthly Mean Total Sunspot Number** dataset from the **SILSO World Data Center (Royal Observatory of Belgium)**. The objective is to study long-term solar activity patterns and model the statistical behavior of sunspot counts.

The analysis includes:
- Time-series visualization
- Modeling using the Gamma distribution
- Splitting data into 12-year solar cycles
- Histogram analysis of sunspot counts
- Manual Metropolis–Hastings MCMC sampling (without PyMC3)
- Posterior estimation and prediction of Gamma parameters `a` and `b`

This project answers **six structured analytical questions**, progressing from exploratory visualization to probabilistic inference.

---

## 📂 Dataset Source
The dataset used is the monthly averaged total sunspot number series:

**URL:** https://www.sidc.be/silso/DATA/SN_m_tot_V2.0.txt

### Dataset Columns
- **year** — calendar year
- **month** — calendar month
- **decimal_date** — year in decimal format
- **sunspot** — mean total sunspot count for the month
- **std** — estimated standard deviation
- **n_obs** — number of observations
- **provisional** — flag (1 = provisional)

---

## ✅ Q1 — Time-Series Exploration
The dataset is indexed by date and visually inspected to observe long-term behavior. This reveals the well-known **solar cycle pattern**, approximately repeating every 11 years.

---

## ✅ Q2 — Gamma Modeling by 12-Year Solar Cycles
To study distributional changes over time, the dataset is divided into 12-year segments. A Gamma distribution is fitted to each block, providing cycle-specific shape (`a`) and scale (`b`) parameters.

Zero sunspot months are excluded because Gamma likelihood estimation requires strictly positive values.

---

## ✅ Q3 — Histogram of Sunspot Counts
A histogram helps assess skewness, spread, and suitability of the Gamma model. Sunspot counts are highly right-skewed, supporting the choice of a Gamma distribution.

---

## ✅ Q4 — Manual MCMC Without PyMC3
Bayesian inference is performed using a **custom Metropolis–Hastings sampler**, not relying on PyMC3 or ArviZ. The prior distribution is:
- shape `a` ~ Gamma(4, 10)
- rate `b` ~ Gamma(4, 10)

Posterior sampling is conducted separately for:
- the first 50 observations
- the full dataset
- the last 50 observations

Each group’s parameter uncertainty and convergence are studied.

---

## ✅ Q5 — Trace & Posterior Visualization
Trace plots show sampler movement across iterations, assessing mixing and convergence.
Posterior histograms display estimated distributions of `a` and `b` after discarding burn-in samples.

---

## ✅ Q6 — Predictive Parameter Estimates
Posterior means and credible intervals for `a` and `b` are computed. These summarize estimates of the underlying solar activity distribution and allow prediction of expected monthly sunspot counts.

---

## ✅ Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- scipy

No Bayesian libraries required.

---

## ✅ Key Insights
🌞 Sunspot behavior is cyclical and non-linear
📈 The distribution is right-skewed — Gamma is appropriate
🔁 Solar cycles differ statistically over time
🎯 Bayesian inference quantifies uncertainty effectively
🧠 Manual MCMC avoids reliance on external probabilistic frameworks

---

## 📜 License
For academic and research purposes.

---

## 🙌 Acknowledgments
Data courtesy of the **SILSO World Data Center**, Royal Observatory of Belgium, Brussels.

---
