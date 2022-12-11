#	Performance Comparisons Across Periods (1998-2012 vs 2013-2022)
#### To help inspect whether the effectiveness of the mispricing recognition factor has declined in recent years, the whole sample period is split into two periods: the first period ranges from April 1998 to December 2012, and the second period is from January 2013 to June 2022. The performance statistics for each strategy implemented with the 5-quintile portfolio in the 2 periods are calculated respectively and listed below. Each strategy’s Q5-Q1 spread lessens by around 50% in unison after switching from the 1998-2012 to 2013-2022 period, primarily because the long position’s returns reduce by 20% to 30%. <br><br>On the other hand, it is worth noticing that the OLS benchmark’s Q1 return decreases after switching from the 1998-2012 to 2013-2022 period. In contrast, all ML models’ Q1 return increases, decreasing their Q5-Q1 spread. The difference may result from the fact that the ML models’ optimal hyper-parameters are grid searched with the samples in 1998 and remain the same for all windows. Since the market regime may change a lot after such a long time, these hyper-parameters may not be optimal anymore. Thus, if hyper-parameters are tuned using the samples within the 2013-2022 period, ML models’ Q1 return would decrease a bit, and their Q5-Q1 spread returns would be higher than the returns shown. <br><br>In summary, the mispricing recognition factor still works so far, and its effectiveness has weakened in recent years compared to the performance from 1998 to 2012. However, the degree of decline in its effectiveness may be smaller than shown in the tables.

#### Performance Statistics for Quintile Sorted Portfolios (from 1998 to 2012)
| ’98 – ‘12 | AMR   | M>0   | Vol    | MDD   | SR   | T/M | Mkt Cap (bn) |
|-----------|-------|-------|--------|-------|------|-----|--------------|
| OLS       |
| Q5        | 2.08% | 65.9% | 17.39% | 19.1% | 1.50 | 208 | 3.9          |
| Q1        | 1.57% | 61.4% | 21.11% | 37.4% | 0.64 | 205 | 38.8         |
| Q5 - Q1   | 0.51% | 60.2% | 7.59%  | 13.8% | 0.38 | 413 | 22.0         |
| RF        |
| Q5        | 2.84% | 68.8% | 16.49% | 17.8% | 2.31 | 145 | 0.6          |
| Q1        | 0.90% | 59.1% | 17.92% | 46.7% | 0.33 | 74  | 63.9         |
| Q5 - Q1   | 1.94% | 77.8% | 4.80%  | 2.7%  | 2.48 | 218 | 33.7         |
| XGB       |
| Q5        | 2.71% | 68.8% | 16.47% | 17.8% | 2.18 | 201 | 1.7          |
| Q1        | 1.01% | 58.5% | 18.91% | 49.1% | 0.37 | 143 | 55.4         |
| Q5 - Q1   | 1.70% | 77.3% | 5.00%  | 3.0%  | 2.08 | 344 | 29.7         |
| NN2       |
| Q5        | 2.81% | 67.6% | 18.00% | 18.7% | 2.08 | 218 | 1.4          |
| Q1        | 0.99% | 61.4% | 17.80% | 47.9% | 0.40 | 224 | 56.0         |
| Q5 - Q1   | 1.82% | 73.3% | 5.34%  | 1.6%  | 2.09 | 442 | 29.9         |
| NN3       |
| Q5        | 2.89% | 68.2% | 17.35% | 17.3% | 2.24 | 200 | 1.1          |
| Q1        | 0.90% | 57.4% | 18.13% | 47.4% | 0.33 | 208 | 58.6         |
| Q5 - Q1   | 1.99% | 77.8% | 5.02%  | 2.9%  | 2.45 | 408 | 31.1         |
| NN4       |
| Q5        | 2.89% | 68.2% | 17.17% | 17.6% | 2.26 | 150 | 0.6          |
| Q1        | 0.93% | 58.5% | 18.57% | 47.4% | 0.33 | 149 | 62.5         |
| Q5 - Q1   | 1.96% | 76.1% | 5.35%  | 3.4%  | 2.25 | 299 | 32.9         |
| NN5       |
| Q5        | 2.84% | 67.6% | 17.14% | 17.2% | 2.22 | 142 | 0.5          |
| Q1        | 0.92% | 59.7% | 17.66% | 49.3% | 0.36 | 113 | 66.4         |
| Q5 - Q1   | 1.92% | 76.1% | 5.01%  | 2.7%  | 2.35 | 255 | 35.0         |
| NN6       |
| Q5        | 2.85% | 67.0% | 17.15% | 17.0% | 2.23 | 157 | 0.8          |
| Q1        | 0.99% | 57.4% | 18.96% | 47.5% | 0.36 | 125 | 60.3         |
| Q5 - Q1   | 1.86% | 75.6% | 5.10%  | 3.4%  | 2.25 | 282 | 31.9         |
| LSTM      |
| Q5        | 1.56% | 57.1% | 16.82% | 19.5% | 1.11 | 135 | 1.6          |
| Q1        | 0.82% | 62.1% | 17.95% | 46.5% | 0.28 | 179 | 37.1         |
| Q5 - Q1   | 0.74% | 54.9% | 5.50%  | 18.3% | 0.74 | 306 | 19.6         |

#### Performance Statistics for Quintile Sorted Portfolios (from 2013 to 2022)
| ’13 – ‘22 | AMR   | M>0   | Vol    | MDD   | SR   | T/M | Mkt Cap (bn) |
|-----------|-------|-------|--------|-------|------|-----|--------------|
| OLS       |
| Q5        | 1.66% | 71.1% | 16.34% | 11.8% | 1.23 | 211 | 4.2          |
| Q1        | 1.41% | 71.9% | 16.00% | 24.8% | 0.84 | 210 | 49.5         |
| Q5 - Q1   | 0.25% | 57.0% | 3.95%  | 11.6% | 0.23 | 421 | 27.4         |
| RF        |
| Q5        | 2.03% | 73.7% | 16.28% | 12.4% | 1.56 | 130 | 0.6          |
| Q1        | 1.04% | 65.8% | 14.20% | 21.9% | 0.64 | 81  | 80.0         |
| Q5 - Q1   | 0.99% | 65.8% | 4.38%  | 2.1%  | 1.22 | 211 | 41.7         |
| XGB       |
| Q5        | 2.05% | 74.6% | 16.07% | 10.1% | 1.60 | 169 | 1.8          |
| Q1        | 1.09% | 66.7% | 15.14% | 28.9% | 0.63 | 144 | 62.9         |
| Q5 - Q1   | 0.96% | 68.4% | 4.46%  | 3.0%  | 1.17 | 313 | 33.4         |
| NN2       |
| Q5        | 1.94% | 73.7% | 15.96% | 12.8% | 1.51 | 234 | 1.9          |
| Q1        | 1.18% | 66.7% | 15.24% | 24.6% | 0.70 | 289 | 65.8         |
| Q5 - Q1   | 0.76% | 64.0% | 4.13%  | 3.2%  | 0.95 | 523 | 35.0         |
| NN3       |
| Q5        | 2.04% | 72.8% | 16.02% | 10.5% | 1.59 | 180 | 1.3          |
| Q1        | 1.05% | 64.0% | 14.97% | 26.0% | 0.60 | 252 | 68.5         |
| Q5 - Q1   | 0.99% | 67.5% | 4.45%  | 2.6%  | 1.20 | 432 | 36.1         |
| NN4       |
| Q5        | 2.02% | 73.7% | 16.32% | 12.1% | 1.55 | 150 | 0.9          |
| Q1        | 1.09% | 64.0% | 14.70% | 25.0% | 0.65 | 194 | 76.3         |
| Q5 - Q1   | 0.93% | 67.5% | 4.37%  | 2.7%  | 1.15 | 344 | 39.9         |
| NN5       |
| Q5        | 2.05% | 72.8% | 16.28% | 12.1% | 1.57 | 136 | 0.7          |
| Q1        | 1.07% | 66.7% | 14.26% | 22.2% | 0.67 | 143 | 84.8         |
| Q5 - Q1   | 0.98% | 65.8% | 4.37%  | 2.6%  | 1.20 | 279 | 44.2         |
| NN6       |
| Q5        | 2.02% | 72.8% | 16.24% | 10.8% | 1.55 | 161 | 1.1          |
| Q1        | 1.13% | 65.8% | 15.17% | 28.2% | 0.66 | 160 | 72.6         |
| Q5 - Q1   | 0.89% | 64.0% | 4.48%  | 2.8%  | 1.06 | 321 | 38.1         |
| LSTM      |
| Q5        | 1.39% | 66.7% | 17.91% | 23.6% | 0.90 | 171 | 2.2          |
| Q1        | 1.08% | 66.7% | 15.45% | 25.9% | 0.60 | 259 | 72.3         |
| Q5 - Q1   | 0.31% | 53.5% | 4.73%  | 9.3%  | 0.27 | 430 | 37.6         |
