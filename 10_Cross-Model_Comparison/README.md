# Cross-Model Comparison
## 1. Performance Metrics
#### In the original paper, Bartram and Grinblatt (2018 & 2021) apply (1) the average monthly return and (2) the fraction of months with positive returns as the primary metrics to examine the effectiveness of the mispricing signal. Besides, they also compare the strategy’s performance across periods to check whether the mispricing signal has weakened over time. <br><br> By contrast, in this work, the main purpose is to compare the performance of the ML augmented strategies, find the best model to boost the mispricing recognition’s precision and explore the strategy’s feasibility in the real world, so the transaction costs and volatility also need considering. Therefore, in addition to the metrics used by Bartram and Grinblatt (2018 & 2021), (3) the annualised standard deviation, (4) the max drawdown, (5) the Sharpe ratio, (6) the average No. of transactions executed per month, and (7) the average market capitalisation of the portfolios are applied as the performance metrics. The 8 ML augmented strategies will be evaluated with the 7 performance metrics and compared with the OLS benchmark. The notations used for the 7 performance metrics are outlined below. 

#### Notation for Performance Metrics
| Performance Metrics                            | Notation |
|------------------------------------------------|----------|
| Average Monthly Return                         | AMR      |
| Percentage of Months with Positive Returns     | M>0      |
| Annualised Standard Deviation (Volatility)     | Vol      |
| Max Drawdown                                   | MDD      |
| Sharpe Ratio                                   | SR       |
| Average No. of Transactions Executed per Month | T/M      |
| Average Market Capitalisation                  | Mkt Cap  |
