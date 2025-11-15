Credit Card Approval Prediction

This project predicts whether a credit card application will be approved based on various applicant features. It uses machine learning algorithms to classify applications into approved (0) or denied (1) categories.

Project Overview

This project uses machine learning to predict whether a credit card application will be approved or denied based on various applicant features. The dataset contains information like the applicant's income, age, occupation, family status, and more.

The primary goal is to implement a model that can help financial institutions screen applicants by predicting whether they are a risky applicant based on the features provided.

Technologies Used

Programming Language: Python

Libraries:

pandas

numpy

scikit-learn

matplotlib

seaborn

Tools: Jupyter Notebook

Dataset

This project uses a credit card approval dataset with features like:

AMT_INCOME_TOTAL: Total income of the applicant.

DAYS_BIRTH: Age of the applicant (calculated as the negative number of days since birth).

OCCUPATION_TYPE: Occupation of the applicant.

FLAG_MOBIL: Whether the applicant has a mobile phone.

CODE_GENDER: Gender of the applicant.

NAME_FAMILY_STATUS: Family status (e.g., single, married).

And more...

The target variable (TARGET) is binary, indicating whether the credit card application is approved (0) or denied (1).

Usage

To run the project, open the Jupyter notebook (CreditApproval.ipynb) and follow the steps outlined below:

Data Preprocessing:

The dataset is loaded, and missing values are handled.

Label encoding is applied to categorical features like gender, car ownership, and real estate ownership.

Target Variable:

A binary target variable (TARGET) is created based on the worst_status column, which indicates whether the application is approved (0) or denied (1).

Model Comparison:

Three machine learning models were trained and compared:

Logistic Regression

Decision Tree

Random Forest

Random Forest performed the best, achieving an ROC AUC score of 0.97, indicating excellent model performance.

Threshold Adjustment:

Threshold Adjustment (0.2) was applied to increase recall for risky customers (Class 1).

Effect: Recall for Class 1 significantly increased, but precision dropped as more positives were predicted. This is a trade-off between precision and recall.

SMOTE (Synthetic Minority Oversampling Technique) and class_weight adjustments did not significantly improve performance over threshold adjustment. While these techniques had some effect, the threshold adjustment technique appeared to dominate and provided the most significant performance improvements in this dataset.

Final Model:

The final model, Random Forest with threshold adjustment, can effectively be used to screen potentially risky applicants.
Results and Evaluation

The model's performance was evaluated using classification metrics like:

ROC AUC: Random Forest achieved an impressive ROC AUC score of 0.97, indicating a strong model performance in distinguishing between approved and denied applications.

Precision and Recall Trade-off: The threshold adjustment (0.2) led to an increase in recall for risky applicants (Class 1), but precision dropped as more positives were predicted.

Class Imbalance Handling: SMOTE and class weight adjustments did not improve model performance significantly. The threshold adjustment technique was more effective in improving recall.
