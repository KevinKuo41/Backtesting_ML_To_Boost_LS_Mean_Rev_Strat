# 5 Vanilla Neural Network Models Based Strategies
#### The detailed setup for the model is outlined in section "0407_Summary_for_ML_Models" <br> (A standardisation process is executed on each feature variable individually within the training and testing windows before being fed into the models. In contrast, this step is not done for Random Forest and XGBoost models.)

### 1. Training & Testing Windows
| Model | Fixed Rolling Training Window | Fixed Testing Window |
|-------|-------------------------------|----------------------|
| NN2   | 6 months                      | 1 month              |
| NN3   | 6 months                      | 1 month              |
| NN4   | 6 months                      | 1 month              |
| NN5   | 6 months                      | 1 month              |
| NN6   | 6 months                      | 1 month              |

### 2. Fixed Window Rolling Scheme
![圖片1](https://user-images.githubusercontent.com/92542287/206919871-005f5fde-5e25-4539-9986-921953441fcd.png)
