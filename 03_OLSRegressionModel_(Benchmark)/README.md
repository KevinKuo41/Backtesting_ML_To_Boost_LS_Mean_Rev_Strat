# OLS Regression Applied Strategy (Benchmark)
#### Due to the data source and methodology differences, it is inappropriate to directly compare the performance statistics from Bartram and Grinblatt (2018 & 2021) with those of the ML augmented models in this work. Therefore, an OLS regression model is created as the benchmark. Apart from the differences mentioned, the OLS regression model closely follows the approach proposed by Bartram and Grinblatt (2018 & 2021). <br><br> At the end of each month, a cross-sectional OLS regression of firms’ 21 contemporaneous available accounting items on their market capitalisations is created to calculate the fair equity value and the mispricing signals used to classify stocks. The signal generation starts in April 1998 and ends in May 2022.

#### First, we run a cross-sectional OLS regression of firms’ 21 accounting items $x_{j,1,t},…,x_{j,21,t}$ on their market capitalisations $MV_{j,t}$ to obtain the coefficients $b_{1,t},…,b_{21,t}$ and the intercept $a_t$, i.e.:

$$MV_{j,t}  = a_t+b_{1,t} \times x_{j,1,t}+⋯+b_{21,t} \times x_{j,21,t}$$

#### In which $j$ denotes the firm, $t$ denotes time. Next, we plug each firm’s accounting items into the model with the above coefficients $b_{1,t},…,b_{21,t}$  to calculate its peer-implied fair equity value, $FV_{j,t}$.

$$FV_{j,t}  = a_t+b_{1,t} \times x_{j,1,t}+⋯+b_{21,t} \times x_{j,21,t}$$

#### Firm $j$'s date $t$ mispricing signal, $MS_{j,t}$, can thus be defined as the percentage difference between its date $t$ peer-implied fair equity value, $FV_{j,t}$ and its market capitalisation, $MV_{j,t}$.

$$MS_{j,t}  =  (FV_{j,t}  -MV_{j,t})/MV_{j,t}$$

#### The following month, a long (short) position is implemented for the most underpriced (overpriced) groups based on the corresponding mispricing signals. The holding period is 1 month. The above process is repeated month by month over the whole sample period. Thus, the trading period ranges from May 1998 to June 2022.
