# RNN LSTM Model Based Strategy
#### The detailed setup for the model is outlined in section "0407_Summary_for_ML_Models" (A standardisation process is executed on each feature variable individually within the training and testing windows before being fed into the models. In contrast, this step is not done for Random Forest and XGBoost models.)

### 1. Training & Testing Windows
| Model | Fixed Sliding Training Window | Fixed Testing Window |
|-------|-------------------------------|----------------------|
| LSTM  | 12 months                     | 12 months            |

### 2. Fixed Sliding Window Scheme

![圖片2](https://user-images.githubusercontent.com/92542287/206920267-1cfa2e62-444e-41e2-a0b0-dfd265d7a949.png)
