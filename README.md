# Heston-Model-Vol-Surface

- This repository provides an implementation of the Heston Stochastic Volatility Model, which is used to simulate financial markets with realistic volatility dynamics. Unlike simpler models like Black-Scholes, the Heston model assumes that volatility changes randomly over time and tends to revert to a long-term average.

Overview of the Heston Model
The Heston model simulates two key processes:

- Asset Prices: These change based on market movements, current volatility, and randomness.
- Volatility: Volatility itself is stochastic (random) and fluctuates over time, reverting to a long-term average.
The model includes a correlation between asset prices and volatility changes, making it more reflective of actual market behavior.

Features of the Code
- Simulates Asset Prices and Volatility: Generates paths for asset prices and volatility using numerical methods.
- Dynamic Volatility: Incorporates randomness and mean reversion in volatility, capturing real-world financial dynamics.

Visualization: 
- Produces plots of simulated asset prices and volatility over time.

Applications
- Option Pricing: Calculate the fair value of options while accounting for changing volatility.
- Risk Management: Analyze the impact of fluctuating volatility on portfolios.
