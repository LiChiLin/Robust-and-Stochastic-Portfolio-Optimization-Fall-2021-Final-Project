# Robust and Stochastic Portfolio Optimization Using the Markowitz and Black-Litterman Models

**Author**: Chi-Lin Li  
**Date**: Fall 2021

## Project Overview

This project explores portfolio optimization through the **Markowitz mean-variance model** and the **Conditional Value-at-Risk (CVaR)** framework. In addition, the **Black-Litterman** model is applied to enhance the portfolio by incorporating market equilibrium and investor views. The primary objective is to construct portfolios that maximize returns while minimizing risk, specifically using the Black-Litterman approach to create more robust portfolios that reflect both market conditions and subjective views.

### Key Features:
- **Markowitz Mean-Variance Model**: Traditional portfolio optimization balancing risk and return.
- **Conditional Value-at-Risk (CVaR)**: A method to minimize risk by focusing on the worst-case scenarios in the tail of the distribution.
- **Black-Litterman Model**: A powerful method to incorporate investor views into the traditional mean-variance framework to adjust for subjective opinions and improve portfolio performance.
- **Empirical Study**: Evaluation of different portfolio strategies using the **Dow Jones Industrial Average (DIJA)** from 2016 to 2020 and forecasting performance for 2021.

## Methodologies

### 1. Markowitz Mean-Variance Model
- **Expected Return**: The average return of an asset over a period of time.
- **Variance and Covariance**: The risk is measured using the variance and covariance between asset returns.
- **Optimization**: The objective is to maximize portfolio return while minimizing risk:
  \[
  \text{max}_w \left( \mu^T w - \rho w^T \Sigma w \right)
  \]
  where \( \mu \) is the vector of expected returns, \( w \) is the portfolio weights, \( \Sigma \) is the covariance matrix, and \( \rho \) is the risk-aversion constant.

### 2. Conditional Value-at-Risk (CVaR)
- CVaR focuses on the tail risk of the distribution, ensuring that the portfolio is optimized against extreme losses. The objective is to minimize risk beyond a certain threshold.

### 3. Black-Litterman Model
- **Market Equilibrium**: Estimates the implied market returns.
- **Investor Views**: Combines market equilibrium with subjective investor views to adjust the return expectations.
- **Merging Views**: The combined model integrates both market and investor views to adjust the portfolio weights.

### 4. Empirical Study and Portfolio Comparison
The empirical study compares five portfolios:
- **Market-Based Portfolio**: A baseline portfolio reflecting market equilibrium.
- **Markowitz Portfolio**: Optimized using the mean-variance framework.
- **CVaR Minimizing Portfolio**: Focused on minimizing the worst-case risk.
- **Markowitz Portfolio with Black-Litterman (BL) Approach**: Incorporates investor views to adjust returns.
- **CVaR Minimizing Portfolio with BL Approach**: Adjusts risk minimization with investor views.

The portfolios are compared based on **return**, **risk**, and the **Sharpe ratio**.

## Empirical Results

### Portfolio Comparison (Without Black-Litterman)
| Portfolio               | Return   | Risk  | Sharpe Ratio |
|-------------------------|----------|-------|--------------|
| Market-Based Portfolio   | 26.04%   | 20.19 | 1.21         |
| Markowitz Portfolio      | 36.14%   | 20.34 | 1.70         |
| CVaR Minimizing Portfolio| 3.60%    | 5.27  | 0.41         |

### Portfolio Comparison (With Black-Litterman)
| Portfolio                             | Return   | Risk  | Sharpe Ratio |
|---------------------------------------|----------|-------|--------------|
| Markowitz Portfolio w/ BL Approach    | 38.06%   | 14.81 | 2.47         |
| CVaR Minimizing Portfolio w/ BL Approach| 27.10% | 27.25 | 0.94         |

### Key Findings:
- **Markowitz Portfolio with Black-Litterman** outperformed all other portfolios, showing the highest return and Sharpe ratio.
- **CVaR Minimizing Portfolio** effectively reduced risk but also significantly lowered returns.
- **Black-Litterman** adjustments improved portfolio performance, especially in reducing risk in the Markowitz framework.

## Conclusion

This project demonstrates that applying the **Black-Litterman** approach to portfolio optimization can enhance returns while managing risk more effectively. The empirical results show that portfolios incorporating subjective investor views generally outperform traditional market-based portfolios in terms of risk-adjusted returns. However, the Black-Litterman approach may not be as suitable for CVaR-minimizing portfolios due to the inherent trade-offs between minimizing risk and incorporating subjective views.

## Installation

To replicate this project, install the following dependencies:

```bash
pip install numpy pandas matplotlib cvxpy
```

## Usage

1. **Preprocess Data**: Load the historical Dow Jones Industrial Average (DIJA) data for analysis.
2. **Run Optimization Models**: Implement the Markowitz, CVaR, and Black-Litterman models to optimize portfolio allocation.
3. **Analyze Results**: Compare the performance of different portfolios based on return, risk, and the Sharpe ratio.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contribution

Chi-Lin Li contributed 100% to this project.
