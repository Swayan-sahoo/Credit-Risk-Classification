# Credit-Risk-Classification
## Credit Risk Analysis Report

## Overview

This analysis aims to assess the credit risk of loan applicants using a logistic regression model. The model is trained to classify loans as either healthy (0) or high-risk (1) based on historical lending data. By evaluating the performance of the model, we determine whether it is suitable for predicting credit risk and making informed lending decisions.
## Sumary:
## Step 1: Data Preparation
A. We need to import some important libreries such as numpy,pandas,pathlib and from sklearn.metrics import confusion_metrix , classification_report.

B. Load lending_data.csv into a Pandas DataFrame.

C. Define:
   Features (X): All columns except loan_status.
    Target variable (y): The loan_status column (0 = healthy loan, 1 = high-risk loan).
    
D. Split the dataset into training and testing sets using train_test_split().

## Step 2. Create a logistic regression  model with the original data.
   A. Fit a logistic regression model by using the training data (x_train and y_train)
   
   B. Import the LogisticRegression from sklearn.
   
   C. Instantiate the Logistic Regression Model , assign a random_state parameter of 1 to the model .
   
   D. Fit the model using training data.
   
## Step 3.Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.
  A. Make a prediction using (.credit) on the testing data.
  
## Step 4: Evaluate the model’s performance by doing the following:
  A. Generate a confusion matrix for the model.
  
  B. Print the classification report for the model.
  
## Result:
  After Analyisis we got this result
  
  precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

## Step 5: Answer the following question.
### Question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Answer: 

A. The logistic regression model performed very well in predicting loan statuses, with an overall accuracy of 99%. However, a closer look at the precision, recall, and F1-score for high-risk loans (loan_status = 1) reveals some important insights:

B. Healthy Loans (0): The model achieved a precision of 1.00 and a recall of 0.99, meaning it is nearly perfect in identifying and correctly classifying healthy loans.

C. High-Risk Loans (1): The model had a precision of 0.84, meaning 16% of predicted high-risk loans were actually healthy. However, its recall was 0.94, indicating that it correctly identified 94% of actual high-risk loans.

## Recommendation:
A.The high recall (0.94) for high-risk loans means the model is good at catching risky loans, which is critical in credit risk assessment.

B.The overall accuracy (99%) and weighted scores indicate strong performance.

C.The precision for high-risk loans (0.84) suggests that some healthy loans might be misclassified as high-risk.

D.There is a class imbalance, with far fewer high-risk loans (619) compared to healthy loans (18,765), which could affect model fairness.

E.The model is highly effective and can be used for initial risk assessment.

F.The model performs exceptionally well in predicting healthy loans (0) with precision = 1.00 and recall = 0.99 , f1-score = 1.00.
