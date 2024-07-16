# Credit Risk Classification Challenge

In this Challenge, various techniques are used to train and evaluate a model based on loan risk.

A dataset of historical lending activity from a peer-to-peer lending services company is used to build a model that can identify the creditworthiness of borrowers.


## 1. Split the Data into Training and Testing Sets

**Dataset**

![](Pics/Dataset.png)


**Data Split**
![](Pics/Splitdata.png)


## 2. Create a Logistic Regression Model with the Original Data

**Model**

![](Pics/Model.png)

**Predictions**

![](Pics/Predictions.png)

**Confusion Matrix**

![](Pics/Confusion.png)


**Classification Report**

![](Pics/Classification.png)

- How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

**99.54% of the Healthy loans were correctly predicted as Healthy by the model**

**94.88% of the High-risk loans were correctly predicted as High-risk by the model**


## 3. Write a Credit Risk Analysis Report

### Overview of the Analysis

* The purpose of this analysis is to determine if a logistic regression model can predict the quality of a loan based on a series of features.

* The dataset includes features such as: loan size, interest rate, borrower income, debt to income ration, number of accounts, derogatory marks, total debt.

* The variable being predicted is Loan Status which has 0 values for Healthy loans and 1 values for High-risk loans.

* The following steps were follow to create the model:
    - After importing the data the 'x' and 'y' variables where separated.
    - Then the data set was split between training and testing datasets, using train_test_split function.
    - Using the LogisticRegression algorithm a Logistic Regression Model was created using the training data.
    - Using the predict function with the model, predictions were created for the 'x' testing data.
    - The predictions were compared to the 'y' testing data
    - Finaly, based on the confusion_matrix and the classification_report, conclusions about the quality of the model were made.

### Results

- Accuracy score *(TP + TN) / (TP + TN + FP + FN)*:

**(19,266 / 19,384) = 99.39%**

**99.39% of the loans were correctly predicted as Healthy or High-risk.**

- Precision score *TP / (TP + FP)*:

**(593 / 679) = 87.33%**

**87.33% of the Predicted High-risk loans are actually High-risk loans.**

- Recall score *TP / (TP + FN)*:

**(593 / 625) = 94.88%**

**94.88% of the High-risk loans were correctly predicted as High-risk loans.**

### Summary

- **I would recommend the used of this model. It has a good level of accuracy, precision and recall.**
- **In terms of credit risk, a financial institution will benefit of this model as 94.88% of the High-level loans were correctly predicted.**
- **However, there should be considerations regarding reputational risk because of the False Positive results.**
- **From the High-risk loans predicted by the model, 12.67% are actually Healthy. So, if the Financial Institution makes a decision based on the model, customers with healthy loans may be affected and become detractors or take legal actions.**