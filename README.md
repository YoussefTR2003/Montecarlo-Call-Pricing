# Monte Carlo Option Pricing

This project implements a Monte Carlo approach to price a European call option
under the Black–Scholes framework using Python.

The goal is to illustrate how Monte Carlo simulation can be used for derivative
pricing and to compare the simulated price with the analytical Black–Scholes
formula.

---

##  Model Overview

The underlying asset price follows a Geometric Brownian Motion (GBM) under the
risk-neutral measure:

S_T = S_0 · exp[(r − q − ½σ²)T + σ√T · Z]

where:
- r is the risk-free rate  
- q is the continuous dividend yield  
- σ is the volatility  
- Z ~ N(0,1)

The European call price is obtained as the discounted expected payoff:

C₀ = e^(−rT) · E[(S_T − K)⁺]

---

## ⚙️ Methodology

1. Simulate terminal stock prices using Monte Carlo
2. Compute the call payoff at maturity
3. Discount payoffs back to present value
4. Estimate:
   - Monte Carlo price
   - Standard error
   - 95% confidence interval
5. Compare the result with the Black–Scholes closed-form solution
6. Analyze convergence as the number of simulations increases

---

##  Outputs

- Monte Carlo call price
- Standard error and 95% confidence interval
- Distribution of simulated terminal prices
- Convergence of Monte Carlo price toward Black–Scholes value

---

##  Technologies Used

- Python
- NumPy
- SciPy
- Matplotlib

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
python src/monte_carlo_call.py
