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

## 2. Performance Comparisons Across Strategies
#### Based on the mispricing signals generated by each strategy, the stocks are sorted into 5-quintiles and 10-deciles corresponding to each strategy. The investments are made in the extreme two groups the next month. The long/short portfolios are denoted as Q5 (the most underpriced group) / Q1 (the most overpriced group) for the quintile classified portfolios and D10/D1 for the decile classified portfolios. In each group, the stock holding is equally weighted. The performance statistics for Q5/Q1 and D10/D1 are provided below. <br><br> Our OLS benchmark has very similar properties and performance to the OLS model created by Bartram and Grinblatt (2018 & 2021). The average monthly spread of our OLS benchmark is 0.41%, with 58.9% of months having positive returns. It can be a reasonable benchmark for ML augmented strategies. <br><br> Overall, all ML augmented strategies raise the accuracy of mispricing recognition compared to the OLS benchmark and thus bring higher spreads between the underpriced and the overpriced, a higher percentage of months with positive returns, lower volatility, and a higher Sharpe ratio. The findings are similar to the results derived from Matthias, Marina and Marc (2021), who apply RF and XGB models to detect the mispricing in the Eurozone and train the models with a 4-year term of the fixed rolling training window. <br><br> No matter how precise the ML models’ mispricing recognition can be, the short position in the most overpriced group still generates negative returns like the OLS benchmark does, consistent with the results from Bartram and Grinblatt (2018 & 2021) in the US stock market. Compared to the OLS benchmark, the ML models can further reduce the returns of the overpriced group, raising the spread returns. <br><br> It is worth mentioning that among all the ML strategies, the RF strategy achieves almost the best performance on all metrics and even the lowest holding turnover ratio. Its transaction costs are only 51% and 63% of the OLS benchmark implemented with 5-quintile and 10-decile strategies, respectively. The NN5 model fits the mispricing recognition approach the best in all NN models, and its performance is exceptionally close to that of the RF strategy. However, the NN5 strategy, on average, executes 17% or 28% more transactions per month than the RF model, indicating that the NN5 strategy would have higher transaction costs. <br><br> Besides, compared to the OLS benchmark, all ML strategies are more prone to recognise firms with a smaller market capitalisation as underpriced stocks and firms with a larger market capitalisation as overpriced stocks. As mentioned, firms with a smaller market capitalisation may possess the property of lower liquidity, which may limit the profitability of the strategy’s long position, especially the strategy implemented with the 10-decile classification. Even if the 10-decile classification brings an even higher spread and lower transaction costs to the strategy, it also focuses more on the firms with a smaller market capitalisation. The trade-off between the group size and the trading feasibility can be further discussed. <br><br> Although the LSTM strategy performs a bit better than the OLS benchmark, it still performs worse than other ML strategies. The fair equity value it predicts is relatively closer to each firm’s contemporaneous market capitalisation, primarily because the LSTM model not only learns from the feature variables but the market changing pattern of the 12-month period. Its property of learning the time series evolution shrinks the difference between its predicting fair equity value and market capitalisation, leading to worse performance than other ML strategies.
![Applied Project-18](https://user-images.githubusercontent.com/92542287/206916093-2d8ebe3f-aa0b-47ac-98ab-5d420e47b320.jpg)
![Applied Project-19](https://user-images.githubusercontent.com/92542287/206916099-0ab05110-b7eb-4d9d-8434-6dffc0989664.jpg)

## 2. Backtesting Results For L/S Mean Reversion Strategy
The graph describes the cumulative Q5-Q1 spread returns of the 9 strategies
![Applied Project-26](https://user-images.githubusercontent.com/92542287/206817965-0502fb6a-9b65-4202-ba29-516df81cf083.jpg)
The graph describes the cumulative D10-D1 spread returns of the 9 strategies
![Applied Project-27](https://user-images.githubusercontent.com/92542287/206817969-1452f9d6-2124-4c82-8992-a702b6b7b579.jpg)

## 3. Backtesting Results For Long-only Mean Reversion Strategy
The graph describes the cumulative Q5 returns of the 9 Long-only strategies
![圖片](https://user-images.githubusercontent.com/92542287/209020581-b77442b5-f1cc-4a75-9828-8a3d77440ec7.png)
The graph describes the cumulative D10 returns of the 9 Long-only strategies 
![圖片](https://user-images.githubusercontent.com/92542287/209020633-82750987-2c5e-47a2-b42b-7cbd60e58fda.png)

## 4. Backtesting Results For Short-only Mean Reversion Strategy
The graph describes the cumulative Q1 returns of the 9 Short-only strategies
![圖片](https://user-images.githubusercontent.com/92542287/209020718-8cd385ad-5345-4984-af43-87a81f840247.png)
The graph describes the cumulative D1 returns of the 9 Short-only strategies
![圖片](https://user-images.githubusercontent.com/92542287/209020759-bcfa6722-7d40-4d39-8640-4ddfbb9e6600.png)

