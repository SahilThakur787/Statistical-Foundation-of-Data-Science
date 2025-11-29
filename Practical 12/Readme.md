# Modified Metropolis Sampler & Deterministic Evolution Model  
### Python-Based Computational Methods  
---

## 📌 Introduction

This repository presents an alternative implementation of:

1. A **Metropolis MCMC sampler**, rewritten with different function names, variables, and structural choices.
2. A **deterministic evolution model**, demonstrating rule-based state updates.

The aim of this code is to sample effectively from the standard normal distribution and illustrate a deterministic system’s predictable behavior.

---

## 🧠 Part A – Metropolis Sampler (Modified Version)

This version implements a flexible Metropolis sampler using:

- A custom `log_density_normal()` function  
- A rewritten sampling routine `run_metropolis()`  
- New variable and parameter names  
- A redesigned output format  

Despite structural differences, the algorithm maintains full accuracy and produces results consistent with the theoretical properties of **N(0,1)**.

### ✔ Outputs Generated

The sampler computes:

- **Metropolis acceptance ratio**  
- **Estimated mean of samples** (expected ≈ 0)  
- **Estimated variance** (expected ≈ 1)  
- **Approximate deterministic value of E[X²]** (expected ≈ 1)  

These metrics confirm that the Markov chain mixes well and converges to the desired distribution.

---

## ⚙️ Part B – Deterministic Evolution Function

This section implements a deterministic recurrence:


The function generates a sequence that evolves purely based on the growth factor.  
No randomness is involved — identical input always yields identical output.

This model serves as a clear contrast to the stochastic Metropolis sampler.

---

## 🧪 Technologies Used

- **Programming Language:** Python  
- **Library:** NumPy  
- **Execution Platform:** Google Colab / Jupyter Notebook  

---

## ▶️ Running the Program

1. Open the notebook in any Python environment.  
2. Ensure NumPy is installed.  
3. Run all cells sequentially.  
4. Review printed results for both the MCMC sampler and deterministic sequence.

---
