### Files

[Budget Starter Notebook](Starter_Code/account_summary.ipynb)

[Retirement Planner Starter Notebook](Starter_Code/portfolio_planner.ipynb)

- - -

### Instructions

#### Budget Analysis

In this section, you will use the Plaid API to obtain transaction and account data for the budget analysis section of the report.

Follow the steps outlined in the budget starter notebook to complete the following:

1. Generate a Plaid access token to access the Developer Sandbox.

2. Use the Access token to fetch account transactions from the sandbox. You should fetch the last 90 days of transactions from the sandbox using the following institution:

    ```python
    INSITUTION_ID = "ins_109508"
    ```

3. Perform basic budget analysis on the sandbox transaction and generate the following plots:

* Spending Categories Pie Chart

* Spending Per Month Bar Chart

4. Use the API to fetch income data from the sandbox and print the following:

* Last Year's Income Before Tax

* Current Monthly Income

* Projected Year's Income Before Tax

#### Retirement Planner

In this section, you will use the IEX API to fetch historical closing prices for a retirement portfolio and then run Monte Carlo simulations to project the portfolio performance at 20 years. You will then use the Monte Carlo data to answer questions about the portfolio.

Follow the steps outline in the budget starter notebook to complete the following:

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
5. (Optional Challenge) Use the Monte Carlo data and calculate the cumulative returns at the 5%, 50%, and 95% quartiles and plot this data as a line chart to see how the cumulative returns change over the life of the investment.

#### Financial Report

In this section, you will compile a financial report to demo your calculations to the consumer app team. The report should be written as a markdown file and include the following sections:

1. Budget Analysis: Summarize the transaction data from the budget analysis and include images for each chart and table produced.
2. Retirement Planning: Summarize the retirement portfolio analysis and include the charts for the Monte Carlo simulation.

***

# Banking and Investing Reporting

The consumer division of Harold's company has decided to offer budgeting and financial planning services to customers. They want to build a report for customers that links to their banking and investment accounts and automatically refreshes the data and charts on login. However, some of the calculations are tricky, and Harold could really use some help connecting the accounts and simulating the retirement investment projections. Luckily, there are APIs available to obtain account transactions and fetch retirement portfolio prices.

In this homework assignment, you will help Harold complete the following tasks:

1. Budget Analysis with Plaid
2. Retirement Planner
3. Financial Report

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Roberto Cantu**  - [GitHub](https://github.com/RCantu92)