## 1. Packages Used
             import numpy as np
             import pandas as pd
             import os
             import seaborn as sns
             import matplotlib.pyplot as plt
             import xgboost as xgb
             from sklearn.model_selection import GridSearchCV
             from sklearn.linear_model import LinearRegression
             from sklearn.ensemble import RandomForestRegressor
             from sklearn.metrics import mean_squared_error
             from tensorflow.keras.models import Sequential
             from tensorflow.keras.layers import LSTM, Dense, Dropout
             from tensorflow.keras import regularizers
             import keras_tuner as kt
             import tensorflow as tf
             from IPython.display import display
             from eli5.sklearn import PermutationImportance
             from hyperopt import STATUS_OK, Trials, fmin, hp, tpe
             from statsmodels.api import OLS

## 2. Random State & Random Seed
             random_state = 123
             np.random.seed(123)
