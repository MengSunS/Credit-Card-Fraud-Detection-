# Credit-Card-Fraud-Detection

This dataset contains credit card transactions over a two day collection period in September 2013 by European cardholders. Dataset is avaialbe on Kaggle. 

This credit card transaction dataset is highly skewed, with most transactions valid and only a few are fraudulent. In this project, we'll need to identify the minority class (fraudulent transactions). 

The features V1-V28 are the result of a principal components analysis (PCA) transformation. This transformation was applied by the original authors to maintain confidentiality of sensitive information. Additionally the dataset contains 'Time' and 'Amount', which were not transformed by PCA. 

![image](https://github.com/MengSunS/Credit-Card-Fraud-Detection-/raw/master/Time&Amount.jpg)

Dealing with a skewed datset, We'll need to oversample or undersample the dataset to make it more balanced to avoid overfitting. Specifically, we need to oversample or undersample them DURING the cross validation process instead of prior to this process, the reason is the dataset used for validation should not be 'seen' by the model, oversampling or undersampling before cross validation will lead to data leakage. 

In this project, we oversampled original skewed training data using SMOTE in imbalance during cross validation process. And developed several machine learning models (Logistic Regression, Random Forest) with tuned hyperparameters that achieved trade-off between precision and recall to help classify valid and fraudulent transactions.

![image](https://github.com/MengSunS/Credit-Card-Fraud-Detection-/raw/master/ConfusionMatrix_rf.jpg)

