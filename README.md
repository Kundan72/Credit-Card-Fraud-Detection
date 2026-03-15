# Credit Card Fraud Detection using Machine Learning

* Two separate datasets (train & test)
* SMOTE applied
* Logistic Regression, Random Forest, XGBoost
* Evaluation using Accuracy, Precision, Recall, F1-score

# Project Overview

Credit card fraud detection is an important problem in the financial industry. Fraudulent transactions are rare compared to legitimate transactions, making this a highly imbalanced classification problem.

The goal of this project is to build machine learning models capable of identifying fraudulent transactions by analyzing transaction data. Multiple machine learning algorithms were trained and compared to determine which model performs best for fraud detection.

# Project Workflow

The project follows a structured machine learning pipeline consisting of five main stages.
# 1️⃣ Import Libraries and Load Dataset
The first step involved importing the necessary Python libraries required for data manipulation, preprocessing, model building, and evaluation.
# Libraries Used
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Imbalanced-learn (SMOTE)

Two separate datasets were used:

* **Training Dataset** → Used to train the machine learning models
* **Testing Dataset** → Used to evaluate the model on unseen transactions

Using separate datasets ensures a more realistic evaluation of model performance.
# 2️⃣ Data Preprocessing

The dataset contained several columns such as transaction identifiers, timestamps, and personal information that were not useful for prediction.

These columns were removed to improve model efficiency and prevent data leakage.
After cleaning the dataset:

* **Features (X)** were separated
* **Target variable (y)** representing fraud or non-fraud transactions was extracted

Target values:

* **1 → Fraudulent transaction**
* **0 → Legitimate transaction**
# 3️⃣ Handling Class Imbalance

Fraud detection datasets are typically **highly imbalanced**, where fraudulent transactions are much fewer than legitimate ones.

To address this issue, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to the training dataset.

SMOTE generates synthetic samples for the minority class (fraud transactions), helping the model learn patterns more effectively.

This step improves the model's ability to detect fraudulent transactions.
# 4️⃣ Feature Scaling

Feature scaling was applied to normalize the input variables so that all features contribute equally during model training.

Scaling helps improve the performance and convergence of machine learning algorithms.

**StandardScaler** was used to transform the features so that they have:

* Mean = 0
* Standard deviation = 1
# 5️⃣ Model Training and Evaluation

Three machine learning models were trained and evaluated for fraud detection.

### Models Implemented

* Logistic Regression
* Random Forest
* XGBoost
* Isolation Forest

These models were selected because they are widely used for classification problems and fraud detection tasks.
# Evaluation Metrics

To measure model performance, the following metrics were used:

* Accuracy – Overall correctness of predictions
* Precision – Percentage of predicted fraud transactions that were actually fraud
* Recall – Ability of the model to detect actual fraud cases
* F1 Score – Balance between precision and recall

# Insights
# Logistic Regression achieved the best overall performance, with the highest accuracy and F1-score.
# Random Forest provided balanced performance across precision and recall.
# XGBoost achieved strong precision, indicating fewer false positive predictions.

This comparison highlights how different algorithms behave when applied to fraud detection problems.

# Conclusion

This project demonstrates how machine learning techniques can be used to detect fraudulent credit card transactions. By handling class imbalance using SMOTE and comparing multiple models, it is possible to build predictive systems capable of identifying suspicious financial activity.
