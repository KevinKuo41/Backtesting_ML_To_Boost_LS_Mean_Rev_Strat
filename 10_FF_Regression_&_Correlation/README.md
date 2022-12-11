#	6 Factor Time-Series Regressions
#### The time-series regressions of 6 known market anomalies, i.e. Mkt_RF, SMB, HML, Mom, ST_Rev and LT_Rev on 4 representative strategies are performed to examine whether these factors can explain the strategies. The results are reported below. <br><br> The Q1, Q5, and Q5-Q1 portfolios of the OLS Benchmark, RF, NN5, and LSTM strategies generate significant positive alpha, meaning that the mispricing signal indeed captures some positive returns that the known anomalies cannot explain. Besides, most of their returns come from SMB and HML factors, consistent with our expectations and the statistics of the average market capitalisation. Interestingly, compared to most of the strategies that lightly but statistical-significantly rely on the ST_Rev factor, the RF strategy has an insignificant relationship with the factor, and the RF possess the highest alpha. Considering the length of the holding window is only 1 month, it is pretty reasonable that the relationships between most strategies and LT_Rev are statistically insignificant. <br><br> Furthermore, it is worth mentioning that the Q5-Q1 returns for all strategies have a significant negative relationship with the market risk factor, which is an excellent selling point for institutional clients that especially favour counter-cyclical investments, such as insurance companies and pension funds.

##### The table describes the intercept, slope coefficients, t-statistics, R^2, and the number of observations from time-series regression of the Q1, Q5 and Q5-Q1 positions’ monthly return on 6 factors for OLS, RF, NN5, and LSTM strategy separately. The numbers in parentheses are t-statistics. *, **, *** represent the statistical significance at the 10%, 5%,and 1% levels, respectively.
|            |            | **OLS**   |            |            | **RF**    |            |           | **NN5**   |            |            | **LSTM**   ||
|------------|------------|-----------|------------|------------|-----------|------------|-----------|-----------|------------|------------|------------||
|            | Q1         | Q5        | Q5-Q1      | Q1         | Q5        | Q5-Q1      | Q1        | Q5        | Q5-Q1      | Q1         | Q5         | Q5-Q1      |
| **Alpha**  | 0.0074***  | 0.0151*** | 0.0039***  | 0.0024***  | 0.0203*** | 0.0090***  | 0.0030*** | 0.0203*** | 0.0087***  | 0.0028***  | 0.0113***  |0.0043***  |
|            | (6.703)    | (12.622)  | (4.089)    | (3.546)    | (20.500)  | (15.660)   | (4.474)   | (20.398)  | (15.053)   | (3.699)    | (10.302)   | (6.759)    |
| **Mkt_RF** | 0.9699***  | 0.7824*** | -0.0941*** | 0.9862***  | 0.7224*** | -0.1322*** | 0.9957*** | 0.7218*** | -0.1372*** | 1.0197***  | 0.7703***  | -0.1248*** |
|            | (35.796)   | (26.515)  | (-4.033)   | (59.445)   | (29.111)  | (-9.203)   | (59.481)  | (28.948)  | (-9.526)   | (54.550)   | (27.878)   | (-7.846)   |
| **SMB**    | 0.4914***  | 0.4416*** | -0.0251    | 0.1789***  | 0.6781*** | 0.2495***  | 0.1808*** | 0.7251*** | 0.2720***  | 0.1918***  | 0.5188***  | 0.1632***  |
|            | (12.247)   | (10.106)  | (-0.726)   | (7.317)    | (18.545)  | (11.792)   | (7.332)   | (19.735)  | (12.816)   | (6.943)    | (12.705)   | (6.943)    |
| **HML**    | -0.1461*** | 0.3112*** | 0.2284***  | -0.0842*** | 0.2002*** | 0.1421***  | -0.0582** | 0.1673*** | 0.1126***  | -0.1259*** | 0.3301***  | 0.2280***  |
|            | (-3.478)   | (6.800)   | (6.316)    | (-3.330)   | (5.293)   | (6.489)    | (-2.281)  | (4.402)   | (5.128)     | (-4.427)   | (7.851)   | (9.419)    |
| **Mom**    | 0.0136     | -0.0604** | -0.0370*   | 0.0197     | -0.027    | -0.0234*   | 0.0156    | -0.0095   | -0.0125    | 0.0474***  | -0.1389*** | -0.0929*** |
|            | (0.574)    | (-2.340)  | (-1.815)   | (1.387)    | (-1.270)  | (-1.899)   | (1.088)   | (-0.444)  | (-1.016)   | (2.964)    | (-5.875)   | (-6.823)   |
| **ST_Rev** | -0.0581*   | 0.0882*** | 0.0732***  | -0.0233    | 0.0218    | 0.0226     | -0.0569** | 0.0344    | 0.0457**   | -0.0315    | 0.1010***  | 0.0662***  |
|            | (-1.923)   | (2.682)   | (2.814)    | (-1.285)   | (0.801)   | (1.435)    | (-3.103)  | (1.262)   | (2.896)    | (-1.554)   | (3.374)    | (3.843)    |
| **LT_Rev** | 0.1028**   | -0.0267   | -0.0646    | -0.0405    | 0.0175    | 0.0291     | -0.0477   | 0.0421    | 0.045      | -0.0679*   | -0.0812    | -0.0066    |
|            | (2.036)    | (-0.485)  | (-1.487)   | (-1.321)   | (0.382)   | (1.096)    | (-1.541)  | (0.914)   | (1.690)    | (-1.971)   | (-1.596)   | (-0.226)   |
| **R^2**    | 0.892      | 0.836     | 0.28       | 0.948      | 0.883     | 0.521      | 0.947     | 0.887     | 0.544      | 0.94       | 0.872      | 
0.539      |
| **Obs**    | 290        | 290       | 290        | 284        | 284       | 284        | 284       | 284       | 284        | 278        | 278        | 
278        |

#	Correlations Between 9 Strategies
#### Finally, a correlation matrix between strategies is provided below to help understand the interactions between strategies. Due to the difference in mispricing signal recognition where OLS only capture linear relationship, but ML models consider the nonlinearity, the correlations between the OLS benchmark and each ML strategy are significantly lower than those between the ML strategies.
##### The table describes the correlation analysis of the Q5-Q1 spread returns of the 9 strategies

|      | OLS    | RF     | XGB    | NN2    | NN3    | NN4    | NN5    | NN6    | LSTM   |
|------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| OLS  | 1      | 0.3653 | 0.5443 | 0.1403 | 0.4005 | 0.3966 | 0.3319 | 0.4388 | 0.5377 |
| RF   | 0.3653 | 1      | 0.858  | 0.8398 | 0.9249 | 0.96   | 0.9643 | 0.9537 | 0.7639 |
| XGB  | 0.5443 | 0.858  | 1      | 0.6314 | 0.8247 | 0.8314 | 0.7738 | 0.864  | 0.8725 |
| NN2  | 0.1403 | 0.8398 | 0.6314 | 1      | 0.8567 | 0.8849 | 0.8965 | 0.8651 | 0.533  |
| NN3  | 0.4005 | 0.9249 | 0.8247 | 0.8567 | 1      | 0.9262 | 0.9248 | 0.9418 | 0.7065 |
| NN4  | 0.3966 | 0.96   | 0.8314 | 0.8849 | 0.9262 | 1      | 0.9675 | 0.9782 | 0.7382 |
| NN5  | 0.3319 | 0.9643 | 0.7738 | 0.8965 | 0.9248 | 0.9675 | 1      | 0.9496 | 0.6899 |
| NN6  | 0.4388 | 0.9537 | 0.864  | 0.8651 | 0.9418 | 0.9782 | 0.9496 | 1      | 0.7701 |
| LSTM | 0.5377 | 0.7639 | 0.8725 | 0.533  | 0.7065 | 0.7382 | 0.6899 | 0.7701 | 1      |
