# A Whale off the Port(folio)

This project focuses on evaluating the performance of algorithmic, hedge, mutual fund portfolios, and a custom portfolio against the S&P TSX 60 Index. Here's a breakdown of key steps:

## Data Cleaning and Preparation

Read and clean whale portfolio returns, algorithmic returns, and S&P TSX 60 historical data.
Convert date formats, clean the values (e.g., removing symbols), calculate daily returns, and merge all datasets into a consolidated DataFrame.

## Performance Analysis

The cumulative returns for each portfolio are computed using (1 + returns).cumprod() and visualized using a line plot.
This helps in visualizing the overall growth of each portfolio over the entire time period.

## Risk Analysis

The risk analysis involves calculating standard deviations of daily returns, which measures the volatility of each portfolio.
A boxplot is used to visually represent the spread and identify which portfolios are riskier than the S&P TSX 60.
The rolling standard deviation is also calculated with a 21-day window, showing how the risk fluctuates over time for all portfolios.

## Correlation and Rolling Beta

A correlation matrix of the portfolios is computed and displayed via a heatmap, which helps identify any strong positive or negative correlations between portfolios and the benchmark (S&P TSX 60).
The 60-day rolling beta is calculated for each portfolio to examine how closely each portfolio moves in relation to the S&P TSX 60, offering insights into the sensitivity of portfolios relative to market movements.

## Sharpe Ratios

The Sharpe ratio is calculated to measure the risk-adjusted return of each portfolio. A higher Sharpe ratio indicates that the portfolio offers a better return per unit of risk.
A bar plot is used to visualize these ratios across all portfolios.

## Custom Portfolio Creation

Three new stocks are selected (L, OTEX, and SHOP), and their returns are calculated and combined to form a custom portfolio.
The custom portfolio is weighted equally across all three stocks and its performance is compared to the other portfolios.
The custom portfolio’s daily returns are then joined with the consolidated returns of all portfolios, allowing for performance comparisons with established whale portfolios and the S&P TSX 60.