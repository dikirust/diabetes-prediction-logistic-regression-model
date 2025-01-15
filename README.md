# Diabetes Prediction Model

This repository contains a machine learning model that predicts the likelihood of a patient having diabetes based on their glucose levels and diastolic blood pressure readings. The model is built using the Orange data mining software and a dataset from Kaggle.

## Dataset

The dataset used for this model is sourced from Kaggle: [Naive Bayes Classification Data](https://www.kaggle.com/datasets/himanshunakrani/naive-bayes-classification-data)

It contains 995 rows of data with 2 features (glucose and blood pressure) and a target variable (diabetes).

## Orange Workflow

The Orange workflow consists of the following steps:

1. **Select Columns**: The 'diabetes' variable is set as the target, while 'glucose' and 'bloodpressure' are used as predictive features.

2. **Data Table**: Confirms the data has been processed correctly, with 995 rows and no missing values.

3. **Rank**: Determines the correlation of features to the target. The 'bloodpressure' variable is found to be the most influential.

4. **Test and Score**: Evaluates the linear regression model using 10-fold cross-validation. Key metrics:
   - MSE (Mean Squared Error): 4.976
   - RMSE (Root Mean Squared Error): 2.231
   - MAE (Mean Absolute Error): 1.615
   - MAPE (Mean Absolute Percentage Error): 16.3%
   - R² (Coefficient of Determination): 0.517

5. **Predictions**: Compares the predicted vs actual diabetes status for all data points, including the margin of error for each prediction.

## Linear Regression Equation

The linear regression equation coefficients are as follows:

- Intercept: 0.0894
- Glucose: 0.0017
- Blood Pressure: 0.0069

To predict the likelihood of diabetes, input the patient's glucose and blood pressure values into the equation:

Diabetes Likelihood = 0.0894 + (0.0017 * Glucose) + (0.0069 * Blood Pressure)

## Conclusion

The evaluation metrics indicate a reasonably good accuracy for a biological dataset, with a MAPE below 20% and R² above 0.5. This model is effective for predicting diabetes likelihood and can be used for similar predictive applications.

The linear regression equation coefficients are provided to enable diabetes prediction by inputting glucose and blood pressure values.
