# Heston-Model-Vol-Surface

Heston Model Implementation
This repository contains a Python implementation of the Heston Stochastic Volatility Model, which is widely used in quantitative finance to price options and analyze volatility dynamics. The Heston model assumes that an asset's volatility is random and follows a stochastic process, allowing for a more realistic modeling of market conditions compared to the Black-Scholes model.

Overview of the Heston Model
The Heston model is defined by the following system of stochastic differential equations (SDEs):

The asset price 
𝑆
𝑡
S 
t
​
  evolves as:

𝑑
𝑆
𝑡
=
𝜇
𝑆
𝑡
𝑑
𝑡
+
𝑣
𝑡
𝑆
𝑡
𝑑
𝑊
𝑡
1
dS 
t
​
 =μS 
t
​
 dt+ 
v 
t
​
 
​
 S 
t
​
 dW 
t
1
​
 
where:

𝜇
μ: Drift of the asset price.
𝑣
𝑡
v 
t
​
 : Stochastic variance.
𝑊
𝑡
1
W 
t
1
​
 : Standard Brownian motion for the asset price.
The variance 
𝑣
𝑡
v 
t
​
  follows:

𝑑
𝑣
𝑡
=
𝜅
(
𝜃
−
𝑣
𝑡
)
𝑑
𝑡
+
𝜎
𝑣
𝑡
𝑑
𝑊
𝑡
2
dv 
t
​
 =κ(θ−v 
t
​
 )dt+σ 
v 
t
​
 
​
 dW 
t
2
​
 
where:

𝜅
κ: Rate at which 
𝑣
𝑡
v 
t
​
  reverts to the long-term mean 
𝜃
θ.
𝜃
θ: Long-term mean variance.
𝜎
σ: Volatility of volatility.
𝑊
𝑡
2
W 
t
2
​
 : Standard Brownian motion for variance, correlated with 
𝑊
𝑡
1
W 
t
1
​
 .
The correlation between 
𝑊
𝑡
1
W 
t
1
​
  and 
𝑊
𝑡
2
W 
t
2
​
  is denoted by 
𝜌
ρ.

Features of the Implementation
Simulates paths of the asset price and stochastic variance using Euler-Maruyama discretization for numerical solutions to the SDEs.
Calculates option prices based on the generated paths.
Customizable parameters including 
𝜇
μ, 
𝜅
κ, 
𝜃
θ, 
𝜎
σ, 
𝜌
ρ, initial price 
𝑆
0
S 
0
​
 , and initial variance 
𝑣
0
v 
0
​
 .
How to Use
Prerequisites
Ensure you have Python installed along with the required libraries. Install dependencies using:

bash
Copy code
pip install numpy matplotlib
Code Explanation
Model Parameters: The code allows users to define key Heston model parameters, such as:

𝜅
κ: Mean reversion speed.
𝜃
θ: Long-term variance.
𝜎
σ: Volatility of volatility.
𝜌
ρ: Correlation between asset and variance.
Initial values for 
𝑆
0
S 
0
​
  and 
𝑣
0
v 
0
​
 .
Simulation: The Heston model's SDEs are simulated using the Euler-Maruyama method:

Asset price and variance evolve over small time steps 
𝑑
𝑡
dt.
Correlation between the Brownian motions is introduced using Cholesky decomposition.
Outputs:

Simulated paths for the asset price and variance.
Visualizations of the stochastic variance and the asset price over time.
Computation of option prices based on these paths.
Example Usage
Below is an example of how to run the model:

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

Output Example
A line chart of the simulated asset price paths over time.
A line chart of the stochastic variance paths over time.
Applications
The Heston model is commonly used for:

Option pricing: Calculating the fair value of options by accounting for stochastic volatility.
Risk management: Understanding the impact of changing volatility on portfolio values.
Volatility modeling: Capturing market behavior more accurately than constant volatility models like Black-Scholes.
