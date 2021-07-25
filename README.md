# maersk_data_challenge

## Organization of the directory

The directory has been structured in the following way :
- At the ```/``` level, ```eda_outlier_removal.ipynb``` is present which contains all the EDA and Outlier Removal Logic
- At the ```/data``` level, the training and testing data along with intermediate data created for training on Google Colab is present
- At the ```/model``` level, all the 9 models developed on Google Colab with their prediction on the test dataset is present

## Summary

Since the data does not belong to one particular time-series, one single model can't solve the forecasting problem.

The idea was to club similar time-series data together and build models in way which is scalable even if the ***Area Code*** being served increases.

Descriptive Statistics has been used to club similar data together. The way the entire data set has been split and clubbed is shown in the image below:

![Data Splitting Schema](https://github.com/AnishDelft/maersk_data_challenge/blob/main/model_data_split.png)

The outlier removal has been done to find and remove outlier in a month's data for the subset of the data set that has been created as the quantum of time here is a month

The time-series modeling on the grouped data has been done using the Prophet Forecasting model developed by Facebook for forecasting on scale

## Results 

It is observed where the grouping has been accurately done, a mean absolute error of ~10 has been acheived

## Future Improvements

The grouping of the data set if done in a better way will result in better models and better forecast on test data where the current model isn't performing well

