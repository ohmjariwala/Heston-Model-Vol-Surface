# Heston-Model-Vol-Surface

Heston Model Implementation
This repository contains a Python implementation of the Heston Stochastic Volatility Model, which is widely used in quantitative finance to price options and analyze volatility dynamics. The Heston model assumes that an asset's volatility is random and follows a stochastic process, allowing for a more realistic modeling of market conditions compared to the Black-Scholes model.

# How to Use:

# Set Heston model parameters
kappa = Mean reversion speed
theta = Long-term variance
sigma = Volatility of volatility
rho = Correlation between Brownian motions
S0 = Initial stock price
v0 = Initial variance
T = Time to maturity
N = Number of time steps
M = Number of simulated paths

# Simulate the Heston model
simulate_heston_model(S0, v0, T, N, M, kappa, theta, sigma, rho)

Visualization
The simulation generates plots of the asset price and stochastic variance over time, providing insight into the dynamics modeled by the Heston process.
