# Jump Diffusion Models for Option Pricing with emphasis on Stochastic Calculus

This repository showcases my MS Thesis work, jointly done at IIT Ropar and IISER Mohali. The work is organized into Theory, Approach, and Experiments sections for this repository.
## Theory

1. **Foundations**:
   - A review of option pricing theory primer.
   - Introduction to **stochastic processes**, including Brownian motion and Poisson processes, as fundamental building blocks for financial modeling.
   - A review of probability theory and stochastic calculus, including Itô's lemma and stochastic differential equations.

3. **Black-Scholes Model**:
   - Detailed derivation of the Black-Scholes option pricing formula using the **Equivalent Martingale Measure (EMM)** approach and Girsanov's theorem.
   - Discussion of the model’s limitations, such as its inability to incorporate jumps or capture return asymmetries.

4. **Jump Diffusion Models**:
   - **Merton’s Jump Diffusion Model (MJD)**: Enhances the Black-Scholes model by incorporating a compound Poisson process with normally distributed jumps.
   - **Kou’s Jump Diffusion Model (KJD)**: Improves MJD by using a double-exponential distribution for jump sizes, addressing the volatility smile and leptokurtic return features.

5. **Volatility Modeling**:
   - Analytical discussions on implied volatility and its role in option pricing.
   - Overview of **GARCH(1,1)** models for time-varying volatility.
   - Comparison of Gaussian and Student’s t-distribution innovations to capture heavy-tailed returns effectively.

## Approach
- **Statistical Verification**:
  - **Normality Tests**: Used to verify the assumptions of normally distributed log-returns (e.g., Kolmogorov-Smirnov and Shapiro-Wilk tests).
  - **Stationarity Tests**: Augmented Dickey-Fuller (ADF) tests performed to confirm the stationarity of return series.
  - **Autocorrelation Analysis**: Ljung-Box test applied to examine autocorrelation in squared returns for GARCH modeling.
  - **Goodness-of-Fit Tests**: Kernel density estimates compared simulated returns from Black-Scholes, MJD, and KJD models against empirical data.

- **Parameter Estimation**:
  - **Maximum Likelihood Estimation (MLE)**: Applied for calibrating model parameters using historical stock price data.

- **Computational Simulations**:
  - Simulations of stochastic processes (Brownian motion, Poisson processes, geometric Brownian motion, and jump diffusion paths).
  - Numerical methods implemented to compute option prices and volatility.

## Experiments

1. **Model Comparison**:
   - **Data**: Infosys stock prices.
   - **Objective**: Estimate parameters and verify model assumptions using statistical tests.
   - **Results**: KJD outperformed MJD and Black-Scholes in fitting empirical return distributions.

2. **Option Pricing**:
   - Infosys call options priced under Black-Scholes, MJD, and KJD models.
   - KJD exhibited superior accuracy in replicating real market prices.

3. **Implied Volatility Analysis**:
   - Generated implied volatility surfaces for **TATA Motors** stock and **NIFTY50** index.
   - Provided insights into volatility patterns and their practical implications.

4. **Volatility Modeling with GARCH**:
   - **Data**: Reliance stock daily returns.
   - **Objective**: Model time-varying volatility and assess innovations.
   - **Results**: GARCH(1,1) with Student’s t-distribution provided a better fit for heavy-tailed returns compared to Gaussian innovation.

5. **Assumption Verification**:
   - Normality tests confirmed leptokurtic nature of returns.
   - ADF test validated stationarity of return series.
   - Ljung-Box test demonstrated significant autocorrelation in squared returns, justifying the use of GARCH models.
