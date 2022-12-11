# Self-Defined Functions
### get_price_df()
#### Combine a dataframe containing monthly buying (1), selling (-1), or doing nothing (0) signal with a dataframe containing monthly return data into a dataframe containing an accumulated return NAV time series data with a designated initial NAV.
### get_performance_stats
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
