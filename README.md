# Vol Surfaces

- This repository provides an implementation of the Heston Stochastic Volatility Model, which is used to simulate financial markets with realistic volatility dynamics. Unlike simpler models like Black-Scholes, the Heston model assumes that volatility changes randomly over time and tends to revert to a long-term average.

# Overview of the Heston Model
The Heston model simulates two key processes:

- Asset Prices: These change based on market movements, current volatility, and randomness.
- Volatility: Volatility itself is stochastic (random) and fluctuates over time, reverting to a long-term average.
The model includes a correlation between asset prices and volatility changes, making it more reflective of actual market behavior.

# Features of the Code
- Simulates Asset Prices and Volatility: Generates paths for asset prices and volatility using numerical methods.
- Dynamic Volatility: Incorporates randomness and mean reversion in volatility, capturing real-world financial dynamics.

# Visualization: 
- Produces plots of simulated asset prices and volatility over time.

# Applications
- Option Pricing: Calculate the fair value of options while accounting for changing volatility.
- Risk Management: Analyze the impact of fluctuating volatility on portfolios.

# Overview of Vol_Surface Notebook

- The vol_surface notebook implements implied volatility surface construction using data from options chains, combining Gaussian Process Regression, polynomial transformations, and smoothing techniques to model the relationship between moneyness, time to expiry, and implied volatility.
    - Implied volatility is calculated using a brentq optimizer, but over time, this calculation will be improved and far more rigorous

- 3D Visualizations: Utilized plotly to create interactive 3D plots of implied volatility surfaces across multiple stocks and expiry dates

- Creates implied volatility surfaces using machine learning techniques and enhances accuracy with smoothing and optimization.
