# Vasicek Model using Monte Carlo Simulation

This repository provides a Monte Carlo simulation of the **Vasicek interest rate model** for pricing zero-coupon bonds. It uses repeated simulations of interest rate paths to compute the expected present value of a future cash flow.

## 📄 Model Overview

The Vasicek model is a one-factor short rate model described by the stochastic differential equation:

\[
dr(t) = kappa * (theta - r(t)) * dt + sigma dW(t)
\]

Where:
- \( r(t) \): short-term interest rate at time \( t \)
- \( \kappa \): mean reversion speed
- \( \theta \): long-term mean interest rate
- \( \sigma \): interest rate volatility
- \( dW(t) \): Wiener process increment

In this implementation, Monte Carlo simulations generate multiple paths of \( r(t) \), which are then used to estimate the price of a zero-coupon bond.

## 📦 Requirements

Make sure the following Python libraries are installed:

- `numpy`
- `matplotlib`
- `pandas`

You can install them with:

```bash
pip install numpy matplotlib pandas

🚀 How to Run

Execute the script:

python Vasicek_model_using_Monte_Carlo.py

This will:

    Simulate 1000 paths of the short-term interest rate.

    Use the simulations to estimate the present value of a cash flow.

    Print the bond price based on the Vasicek model and Monte Carlo simulation.

⚙️ Parameters

Key parameters used in the simulation:
Parameter	Description	Default
x	Future cash flow value (e.g., bond face value)	1000
r0	Initial interest rate	0.1
kappa	Speed of mean reversion	0.3
theta	Long-term average interest rate	0.3
sigma	Volatility of the interest rate	0.03
T	Maturity time in years	1
NUM_OF_SIMULATIONS	Number of Monte Carlo simulations	1000
NUM_OF_POINTS	Number of time steps per simulation	200

You can change these values directly in the script as needed.
📈 Output

Example output:

Bond price based on Monte-Carlo simulation: $973.45

This value is computed as the average discounted cash flow across all simulated paths.