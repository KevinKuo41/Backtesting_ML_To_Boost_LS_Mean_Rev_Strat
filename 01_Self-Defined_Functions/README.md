# Self-Defined Functions
### 1. get_price_df()
#### Combine a dataframe containing monthly buying (1), selling (-1), or doing nothing (0) signal with a dataframe containing monthly return data into a dataframe containing an accumulated return NAV time series data with a designated initial NAV.
### 2. get_performance_stats()
#### Generate the performance stats for a time-series price data.
             Tot Return     - total cumulative return over the whole period
             Avg Return     - average annualised return
             Rf Rate        - average annualised risk-free return
             Volatility     - annualised standard deviation
             Sharpe Ratio   - annualised Sharpe Ratio
             Skewness       - skewness (same frequency as prices)
             Kurtosis       - kurtosis (same frequency as prices)
             HWM            - High Water Mark price, i.e. the highest price ever achieved
             HWM date       - date of the HWM
             MDD            - Maximum Drawdown as positive proportional loss from prior peak
             Peak date      - Date of the MDD peak
             Trough date    - Date of the MDD trough
             Recession Date - Date the asset recovered from Drawdown loss
             MDD Duration   - MDD duration in days from peak to recovery date
### 3. get_performance_stats_2()
#### Generate the long/short, long only and short only performance stats for a time-series price data.
             Total Return           - total cumulative return over the whole period
             Avg Monthly Return     - average monthly return over the whole period
             Avg Mkt Cap            - average market cap for the chosen stocks
             Fraction>0             - the fraction among chosen stocks that generates positive returns
             + Return Stocks (Avg)  - average return for the chosen stocks having positive returns
             - Return Stocks (Avg)  - average return for the chosen stocks having negative returns
             Odds Ratio             - the fraction that the portfolio of chosen stocks generating positive return over the whole period
             Odds Ratio 98-10       - the fraction that the portfolio of chosen stocks generating positive return from 1998 to 2010
             Odds Ratio 11-22       - the fraction that the portfolio of chosen stocks generating positive return from 2011 to 2022
             Transactions/Month     - average transactions made per month
