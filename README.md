# Banking and Investing Reporting

This project builds a report that links to banking and investment accounts and automatically refreshes the data and charts on login. 

In the end, this project aims to do the following:

1. Budget Analysis with Plaid
2. Retirement Planner
3. Financial Report

## Getting Started

#### Budget Analysis

For the budget analysis, this project uses the Plaid API to obtain transaction and account data for the budget analysis section of the report.

The follow are the steps in doing so:

1. Generate a Plaid access token to access the Developer Sandbox.

2. Use the Access token to fetch account transactions from the sandbox.

3. Perform basic budget analysis on the sandbox transaction and generate the following plots:

* Spending Categories Pie Chart

* Spending Per Month Bar Chart

4. Use the API to fetch income data from the sandbox and print the following:

* Last Year's Income Before Tax

* Current Monthly Income

* Projected Year's Income Before Tax

#### Retirement Planner

Next, the project will use the IEX API to fetch historical closing prices for a retirement portfolio and then run Monte Carlo simulations to project the portfolio performance at 20 years. The results will then used to answer questions about the portfolio.

##### Monte Carlo Simulation

Create a Monte Carlo simulation for the retirement portfolio:

1. Use the IEX API to fetch historical closing prices for a traditional 60/40 portfolio using the `SPY` and `AGG` tickers to represent the 60% stocks (SPY) and 40% bonds (AGG).
2. Run a Monte Carlo Simulation of 500 runs and 30 years for the 60/40 portfolio and plot the results.

3. Select the ending cumulative returns from the Monte Carlo simulation and calculate the interval values for a 90% confidence interval.
4. Using the ending cumulative returns, plot a histogram of the results and plot the 90% confidence interval as vertical lines on the histogram.

##### Retirement Analysis

Use the Monte Carlo simulation data to answer the following questions:

1. What are the expected cumulative returns at 20 years for the 10th, 50th, and 90th percentiles?
2. Given an initial investment of $50,000, what is the expected return in dollars at the 10th, 50th, and 90th percentiles?
3. Given the current projected annual income from the Plaid analysis, will a 4% withdrawal rate meet or exceed that value at the 10th percentile? Note: This is basically determining if retirement income is equivalent to current income.
4. How would a 50% increase in the initial investment amount affect the 4% retirement withdrawal? In other words, what happens if the initial investment had been bigger?
5. Use the Monte Carlo data and calculate the cumulative returns at the 5%, 50%, and 95% quartiles and plot this data as a line chart to see how the cumulative returns change over the life of the investment.

#### Financial Report

In this last section, the project will compile a financial report to demo calculations. The report is written as a markdown file and includes the following sections:

1. Budget Analysis: Summarizes the transaction data from the budget analysis and include images for each chart and table produced.
2. Retirement Planning: Summarizes the retirement portfolio analysis and include the charts for the Monte Carlo simulation.

## Built With

* [Python](https://www.python.org/) - Programming language.
* [Pandas](https://pandas.pydata.org/) - Data analysis and manipulation tool.
* [Plaid](https://plaid.com/) - API used to access financial data.
* [IEX Cloud](https://iexcloud.io/docs/api/) - Another API used to access financial data.

## Authors

* **Roberto Cantu**  - [GitHub](https://github.com/RCantu92)