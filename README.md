# Pairs-Trading-Project\
The main objective of the project is to explore and implement Pairs Trading, a statistical arbitrage strategy, to profit from the relative mispricing between co-integrated stocks. Specifically, the project aims to:

Identify pairs of stocks from major economic sectors whose prices are co-integrated, meaning they move together in the long run.
Develop a trading strategy that exploits short-term divergences in the price relationship of these stock pairs using a mean reversion technique.
Optimize the parameters for the trading strategy, such as moving average windows and threshold values, to maximize profit while minimizing risk.
Test the strategy's effectiveness in terms of profit generation and market neutrality, assessing its viability using historical data from multiple sectors.
This repository contains the code files for the project on Pairs Trading.

1) Terms and Terminology:
   
Stationarity: A time series is stationary if its statistical properties (mean, variance, covariance) do not change over time.

Integrated Processes and Order of Integration: A time series that becomes stationary after differencing is called integrated, and the number of differences needed to achieve stationarity defines its order of integration.

Co-integration: A set of non-stationary time series are co-integrated if a linear combination of them is stationary, indicating a long-term equilibrium relationship.
Mean Reversion Strategy: Assumes that prices of assets return to their historical averages, forming the foundation of pairs trading.

Pairs Trading: A statistical arbitrage technique that exploits the relative mispricing of two co-integrated stocks by taking long and short positions.

Augmented Dickey-Fuller (ADF) Test: A statistical test used to determine whether a time series is stationary.

Engle-Granger Test: A method for testing co-integration between two time series.



3) Steps:
Step 1: Test for Stationarity
Applied the ADF test to the time series data to confirm non-stationarity (I(1)) and after differencing, stationarity (I(0)) was achieved.
Step 2: Test for Co-integration
Engle-Granger test was used to test whether two stock prices are co-integrated.
Linear regression was used to estimate the co-integration vector.
Step 3: Pairs Trading Strategy
Stocks are selected based on co-integration, and moving averages (short-term and long-term) are used to detect price divergences.
A Z-score is calculated to quantify deviations from the historical average.
Trading signals are generated based on Z-scores:
Buy the spread when the Z-score is below -1.
Sell the spread when the Z-score is above +1.
Step 4: Trading Strategy Execution
A function was created to automate the process of buying and selling based on thresholds for opening and closing trades.
Parameters such as moving average windows, Z-score thresholds, and trade costs were optimized to maximize profit.
Step 5: Results and Conclusion
The co-integrated stock pairs from different sectors were identified, and optimized parameters were used for generating profitable trades.
The strategy showed a profit in most sectors, but there were risks, such as spreads not returning to zero or changes in co-integration due to market events like mergers or acquisitions.

<!-- The file named Time_Series_Project_(to_be_submitted) contains the collaboratory codes for the porject.   --> 
