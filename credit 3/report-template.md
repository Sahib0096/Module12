# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

## Purpose of the Analysis
* Use a variety of strategies to train and evaluate a loan-risk model. Use a dataset of previous loan activity from a peer-to-peer lending services company to create a model that can determine borrowers' creditworthiness.

## Financial information data

* loan_size: The size of the loan requested by the borrower.
* interest_rate: The interest rate associated with the loan.
* borrower_income: The income of the borrower.
* debt_to_income: The debt-to-income ratio of the borrower, which measures the proportion of debt payments to income.
* num_of_accounts: The number of accounts the borrower has.
* derogatory_marks: The number of derogatory marks on the borrower's credit report.
* total_debt: The total amount of debt owed by the borrower.
* loan_status: The status of the loan, where 0 indicates a healthy loan (low-risk) and 1 indicates a high-risk loan (non-healthy).


  In summary, The dataset contains a variety of borrowers' financial information, such as loan size, interest rate, income, debt-related variables, and loan status. The goal is to create a predictive model that can classify loans as healthy or high-risk based on these financial characteristics. In other words, the goal is to predict a borrower's loan default based on their financial profile.

## Variables we are trying to predict
* value_counts - The function value_counts() counts the number of instances of each class in the loan_status column.
* Precision (pre): This metric measures the proportion of true positive predictions among all positive predictions made by the model. It indicates the model's accuracy in correctly identifying positive instances.
* Recall (rec): This metric measures the proportion of true positive predictions among all actual positive instances in the dataset. It indicates the model's ability to capture all positive instances.
* Specificity (spe): This metric measures the proportion of true negative predictions among all actual negative instances in the dataset. It indicates the model's ability to correctly identify negative instances.
* F1-score (f1): This metric is the harmonic mean of precision and recall. It provides a balanced measure of the model's performance, particularly in scenarios with class imbalance.
* Geometric mean (geo): This metric calculates the geometric mean of sensitivity (recall) and specificity. It is useful for evaluating models in imbalanced datasets.
* Index Balanced Accuracy (iba): This metric assesses the model's balanced accuracy, considering the class imbalance in the dataset.
* Support (sup): This represents the number of samples in each class, providing context for the other metrics.


## Machine learning process
* Problem Definition: It is critical to clearly define the problem statement and the goal of the analysis before proceeding with any other procedures.

* Data Collection: The study is built on a foundation of relevant data from the peer-to-peer lending services company's historical loan activities.

* Data preprocessing involves cleaning the data, dealing with missing values and outliers, and doing feature engineering to ensure the dataset's quality and relevance.

* Exploratory Data Analysis (EDA): Exploring the dataset to understand its structure, uncover trends, and acquire insights into the relationships between variables informs future modeling decisions.

* Model Selection: Selecting a suitable machine learning algorithm, such as logistic regression or resampling method, depending on the problem statement and data type is crucial for developing an effective predictive model.

* Model Training: Training the selected model on the preprocessed dataset with a subset of the data allows it to discover patterns and relationships.

* Model Evaluation: The trained model's performance is evaluated using several measures such as accuracy, precision, recall, and F1-score to ensure its effectiveness in predicting borrowers' creditworthiness.

## Results

<strong>Logistic Regression Model 1:</strong>

* Precision: 99% (an average--the model was 100% precise when predicting low-risk loans, but only 85% precise when predicting high-risk loans).
* Accuracy: 91% (an average--the model had 91% memory in identifying low-risk loans and 90% recall in predicting high-risk loans).
* Recall: 99% (average--the model had 99% recall in predicting low-risk loans and 91% recall in predicting high-risk loans)

<strong>Logistic Regression Model 2:</strong>

* Precision: 99% (an average--the model was 100% precise when predicting low-risk loans, but only 84% precise when predicting high-risk loans).
* Accuracy: 99% 
* Recall: 99%

## Summary
### Model Performance
#### Model 1:
  * Precision (pre): 100% for low-risk loans (class 0) and 85% for high-risk loans (class 1).
  * Recall (rec): 99% for low-risk loans (class 0) and 91% for high-risk loans (class 1).
  * Specificity (spe): 91% for low-risk loans (class 0) and 99% for high-risk loans (class 1).
  * F1-score (f1): 100% for low-risk loans (class 0) and 88% for high-risk loans (class 1).
#### Model 2:
  * Precision (pre): 100% for low-risk loans (class 0) and 84% for high-risk loans (class 1).
  * Recall (rec): 99% for low-risk loans (class 0) and 99% for high-risk loans (class 1).
  * Specificity (spe): 99% for low-risk loans (class 0) and 99% for high-risk loans (class 1).
  * F1-score (f1): 100% for low-risk loans (class 0) and 91% for high-risk loans (class 1).

Both Model 1 and Model 2 have excellent performance measures, including high precision, recall, specificity, and F1 scores in both classes. However, there are significant distinctions to consider.
* Model 1 has somewhat greater precision (85% vs. 84%) and F1-score (88% vs. 91%) for high-risk loans (class 1) than Model 2. This suggests that Model 1 may be more accurate in detecting high-risk loans while retaining a low false positive rate.
* Model 2 has somewhat higher specificity (99% vs. 91%) for low-risk loans (class 0) than Model 1. This shows that Model 2 may be more accurate in selecting low-risk loans while reducing false negatives.

  If the primary goal is to reduce the danger of accepting high-risk loans (class 1), Model 1 may be selected due to its better precision and F1-score for class 1. If the primary goal is to maximize the accuracy of identifying low-risk loans (class 0), Model 2 may be preferable due to its higher specificity for class 0. Finally, the choice between the two models should be based on the company's risk tolerance, business objectives, and the proportional importance of accurately predicting each class. 


