# Using-RNN_LSTM-for-pollution-prediction
In this project value of air pollution is predicted using  RNN LSTM. The dataset has various attributes like pressure, dew, wind speed etc. Hence the type of RNN LSTM is multivariate. The data is loaded from csv file, scaled and then trained in a defined RNN LSTM model.  The model used has very low mean absolute error.

# Why RNN LSTM for pollution prediction?
In case of pollution the attributes like wind speed, pressure, dew etc. may have some interdependancy because one attribute can affect all attributes. Some attributes affect others more than the rest of attributes and such attributes become more important. RNN LSTM takes this into account by using LSTM cell to remember important attributes.

# How parameters change with time
![image](https://github.com/DevShah011/Using-RNN_LSTM-for-pollution-prediction/assets/115929900/eae9a493-9e15-4e1a-ad3b-1f1e549fce14)

# Scaling the input and output 
Inputs and outputs are scaled using MinMaxScaler this is done so that computation is faster.

# Description of RNN model used
Sequential API is used for the model. The model has two LSTM layers with 128 nodes each. The window size for LSTM is taken as 300 and Dropout is 0.3 to increase randomness and prevent overfitting. The last layer is a Dense layer giving one ouput for predicting pollution.

# Training and Results 
As seen in the code the training stops after just 3 epochs because EarlyStopping is used. Since there are a total of 5 parameters Mean Squared Error is used as loss function and as a metric but Mean Absolute error may also be used. The value of mean squared error and loss is low since the first epoch because the dataset used is consistent.
![image](https://github.com/DevShah011/Using-RNN_LSTM-for-pollution-prediction/assets/115929900/e97afeb0-8429-42c5-8548-5993a7f4195d)
