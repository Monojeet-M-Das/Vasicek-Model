# Vasicek Model Simulation

This repository contains a Python implementation of the **Vasicek model**, a widely-used one-factor short-rate model in financial mathematics for simulating the evolution of interest rates.

## 📄 Model Overview

The Vasicek model is defined by the following stochastic differential equation (SDE):

\[
dr(t) = kappa * (theta - r(t)) * dt + sigma dW(t)
\]

Where:
- \( r(t) \) is the short-term interest rate at time \( t \),
- \( \kappa \) is the speed of mean reversion,
- \( \theta \) is the long-term mean level,
- \( \sigma \) is the volatility,
- \( dW(t) \) is the increment of a Wiener process.

This SDE is discretized using the Euler–Maruyama method for simulation.

## 📦 Requirements

The script uses the following libraries:

- `numpy`
- `matplotlib`

Install them via pip if not already installed:

```bash
pip install numpy matplotlib

🚀 How to Run

Run the Python script from your terminal or any IDE:

python Vasicek_model_implementation.py

This will simulate the short-term interest rate path and plot the result.
⚙️ Parameters

You can modify the model parameters inside the script:
Parameter	Description	Default
r0	Initial interest rate	1.3
kappa	Speed of mean reversion	0.9
theta	Long-term mean level	1.4
sigma	Volatility	0.05
T	Total time to simulate (in years)	1
N	Number of time steps	1000
📈 Output

The simulation generates a plot of the interest rate over time according to the Vasicek model.