# Project Overview
This project repository is created to classify if a breast cancer tumour is benign or malignant. 

## Key Question
Breast Cancer is the top rated type of cancer amongst women; which takes away thousands of lives every year. This high mortality rate due to breast cancer does need attention, for early detection so that prevention can be done in time. In this project, out goal is to predict if the tumour is benign or malignant, based on 10 physical features of a breast tumour such as radius, texture, asymmentry, concave points, etc.

## Dataset
The dataset is from UCI machine learning repository. All feature values are recoded with four significant digits. There are no missing values in the dataset.
Class distribution: 357 benign, 212 malignant.

Data Source Link: https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/wdbc.data 
Description: https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancerwisconsin/wdbc.names 


## Uber level approach
- Some initital EDA and anomaly detection checks are performed
- Data is standardized using min max scaler, regularization was also performed
- Several classification models are tried with and without grid search and their results are noted. A holistic comparison is done to assess which models performed better
- The following models were tried: KNN, Decision Tree, Logistic Regression
![Alt text](/ProcessFlow.png)

## Results
The modelling process involved exploration of dataset to check nulls, outliers and other erroneous details but none were found, the distributions were also checked.
The data was then standardized for usage in the KNN and logistic regression models because in KNN distance has to be calculated and Logistic is using regularization

The models were built using both normal hyperparameter tuning and grid search CV to identify best set of parameters and the performance was measured in terms of Accuracy, Precision, recall, AUC score and confusuion matrix

Using above specifications, both overfitting and underfitting was assessed and relevantsteps were taken to avoid the issue. The best metrics and their performances have been summarised and suitable models have been recommended based on evidence.

Best results are obtained from Logistic regression model because they are able to generalize well and it not overfitting on train data.
Also, recall is highest along with AUC for this model, which is a suitable fit for the problem at hand, where identification of
M(positive outcome) holds higher importance than B(negative outcome).
