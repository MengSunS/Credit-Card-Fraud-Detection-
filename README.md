# Credit-Card-Fraud-Detection

This dataset contains credit card transactions over a two day collection period in September 2013 by European cardholders. Dataset is avaialbe on Kaggle. 

This credit card transaction dataset is highly skewed, with most transactions valid and only a few are fraudulent. In this project, we'll need to identify the minority class (fraudulent transactions). 

The features V1-V28 are the result of a principal components analysis (PCA) transformation. This transformation was applied by the original authors to maintain confidentiality of sensitive information. Additionally the dataset contains 'Time' and 'Amount', which were not transformed by PCA. 

![image](https://github.com/MengSunS/Credit-Card-Fraud-Detection-/raw/master/Amount&Time.jpg)
Dealing with a skewed datset, We'll need to oversample or undersample the dataset to make it more balanced to avoid overfitting. Specifically, we need to oversample or undersample them DURING the cross validation process instead of prior to this process, the reason is the dataset used for validation should not be 'seen' by the model, oversampling or undersampling before cross validation will lead to data leakage. 

In this project, we oversampled original skewed training data using SMOTE in imbalance during cross validation process. And developed several machine learning models (Logistic Regression, Random Forest) with tuned hyperparameters that achieved trade-off between precision and recall to help classify valid and fraudulent transactions.

------------------------------------------------------------
[Logistic Regression:]
              precision    recall  f1-score   support

       Valid       1.00      0.97      0.98     56864
       Fraud       0.05      0.93      0.10        98

   micro avg       0.97      0.97      0.97     56962
   macro avg       0.53      0.95      0.54     56962
weighted avg       1.00      0.97      0.98     56962

------------------------------------------------------------
[Random Forest:]
              precision    recall  f1-score   support

       Valid       1.00      1.00      1.00     56864
       Fraud       0.87      0.84      0.85        98

   micro avg       1.00      1.00      1.00     56962
   macro avg       0.94      0.92      0.93     56962
weighted avg       1.00      1.00      1.00     56962


         Random Forest:
![image](https://github.com/MengSunS/Credit-Card-Fraud-Detection-/raw/master/ConfusionMatrix_rf.jpg)

[Feature Importance:]
![image](https://github.com/MengSunS/Credit-Card-Fraud-Detection-/raw/master/feature_importance.jpg)

------------------------------------------------
Click here https://github.com/MengSunS/Credit-Card-Fraud-Detection-/blob/master/CreditCardFraudDetection.ipynb to see the implementation.
