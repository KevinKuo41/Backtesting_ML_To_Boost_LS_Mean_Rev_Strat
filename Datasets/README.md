# Source
#### Overall, equity stock is the only asset class involved in this work. Three primary datasets, which range 291 months, from April 1998 to June 2022, are utilised. All currently active firms and delisted firms once listed in the US stock market are included. <br> 
Download Link: https://drive.google.com/drive/folders/10TP7iOiUej9Y8RwLQY-RUU4a-VYY_CHb?usp=share_link <br> <br> 

#### The sources of the three primary datasets are from:

## 1. S&P Compustat Fundamentals Dataset
Link: https://www.marketplace.spglobal.com/en/datasets/compustat-fundamentals-(8)
#### 21 accounting items, share prices, shares outstanding, and total returns for all companies listed from 1998 to 2022 are downloaded from the S&P Compustat Fundamentals Dataset. Among them, 21 accounting items are most on a quarterly basis, since they were only updated at the end of every quarter. By contrast, share prices and shares outstanding are on a monthly basis.

## 2. Fred Economic Data
Link: https://fred.stlouisfed.org/
#### Monthly Federal Funds Effective Rate is downloaded from Fred Economic Data to serve as the risk-free rate.

## 3. Ken French Data Library
Link: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html
#### 6 known risk premium factors (including Mkt-Rf, SMB, HML, Momentum, ST_Rev, LT_Rev) proposed by Kenneth R. French are downloaded from Ken French Data Library. <br> <br> <br> The detailed information on all used variables is outlined in the belo table:

| **Variable** | **Definition**                                                                 | **Source**                         |
|--------------|--------------------------------------------------------------------------------|------------------------------------|
| ACOQ         | Current Assets - Other - Total - Quarterly                                     | S&P Compustat Fundamentals Dataset |
| AOQ          | Assets - Other - Total - Quarterly                                             | S&P Compustat Fundamentals Dataset |
| ATQ          | Assets - Total - Quarterly                                                     | S&P Compustat Fundamentals Dataset |
| CEQQ         | Common/Ordinary Equity - Total - Quarterly                                     | S&P Compustat Fundamentals Dataset |
| CHEQ         | Cash and Short-Term Investments - Quarterly                                    | S&P Compustat Fundamentals Dataset |
| DLTTQ        | Long-Term Debt - Total - Quarterly                                             | S&P Compustat Fundamentals Dataset |
| DVPQ         | Dividends - Preferred/Preference - Quarterly                                   | S&P Compustat Fundamentals Dataset |
| IBADJQ       | Income Before Extraordinary Items - Adjusted for Stock Equivalents - Quarterly | S&P Compustat Fundamentals Dataset |
| IBQ          | Before Extraordinary Items - Quarterly                                         | S&P Compustat Fundamentals Dataset |
| LCOQ         | Current Liabilities - Other - Total - Quarterly                                | S&P Compustat Fundamentals Dataset |
| LOQ          | Liabilities - Other - Total - Quarterly                                        | S&P Compustat Fundamentals Dataset |
| LTQ          | Liabilities - Total - Quarterly                                                | S&P Compustat Fundamentals Dataset |
| NIQ          | Net Income (Loss) - Quarterly                                                  | S&P Compustat Fundamentals Dataset |
| NOPIQ        | Non-operating Income (Expense) - Quarterly                                     | S&P Compustat Fundamentals Dataset |
| PIQ          | Pretax Income - Quarterly                                                      | S&P Compustat Fundamentals Dataset |
| PPENTQ       | Property Plant and Equipment - Total (Net) - Quarterly                         | S&P Compustat Fundamentals Dataset |
| PSTKQ        | Preferred/Preference Stock (Capital) - Total - Quarterly                       | S&P Compustat Fundamentals Dataset |
| SALEQ        | Sales/Turnover (Net) - Quarterly                                               | S&P Compustat Fundamentals Dataset |
| TXTQ         | Income Taxes - Total - Quarterly                                               | S&P Compustat Fundamentals Dataset |
| XIDOQ        | Extraordinary Items and Discontinued Operations - Quarterly                    | S&P Compustat Fundamentals Dataset |
| DVY          | Cash Dividends (Cash Flow) - Yearly                                            | S&P Compustat Fundamentals Dataset |
| PRCCM        | Price - Close - Monthly                                                        | S&P Compustat Fundamentals Dataset |
| TRT1M        | Total Return - Monthly                                                         | S&P Compustat Fundamentals Dataset |
| CSHOM        | Shares Outstanding – Issue - Monthly                                           | S&P Compustat Fundamentals Dataset |
| Fed Rate     | Federal Funds Effective Rate - Monthly                                         | Fred Economic Data                 |
| Mkt_RF       | Monthly market index excess return                                             | Ken French Data Library            |
| SMB          | Monthly Small Minus Big (SMB) portfolio return                                 | Ken French Data Library            |
| HML          | Monthly High Minus Low (HML) portfolio return                                  | Ken French Data Library            |
| Mom          | Monthly Momentum portfolio return                                              | Ken French Data Library            |
| ST_Rev       | Monthly Short-term reversal portfolio return                                   | Ken French Data Library            |
| LT_Rev       | Monthly long-term reversal portfolio return                                    | Ken French Data Library            |
