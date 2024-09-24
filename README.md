# Credit Scoring Model Using Machine Learning

## Project Overview
This repository contains a machine learning project aimed at predicting customer credit scores. The model classifies customers as either good or bad credit risks 
based on features such as income, age, loan amount, and credit history. Multiple machine learning algorithms, including Logistic Regression, Decision Tree, and Random Forest,
are used to build the classification models. The project evaluates model performance using metrics like accuracy, AUC score, and classification reports, and also ranks feature 
importance using Random Forest.

## Key Features
- **Preprocessing Pipeline:** Handles missing values, encodes categorical variables, scales features, and splits data into training and testing sets.
- **Multiple Models:** Trains and evaluates three different models (Logistic Regression, Decision Tree, and Random Forest).
- **Model Evaluation:** Evaluates each model using metrics such as accuracy, AUC score, classification report, and confusion matrix.
- **Feature Importance:** Identifies the most important features contributing to the Random Forest model’s predictions.
- **Model Saving:** Saves the best-performing model (Random Forest) using `joblib` for future use.

## Steps

### 1. Data Collection
The dataset (`credit_data.csv`) includes customer attributes such as:
- **age**
- **income**
- **loan amount**
- **credit history** 
- **credit score** (target variable: 1 for good credit, 0 for bad credit)

### 2. Data Preprocessing
- **Handling Missing Values:** Removes missing values for simplicity, but imputation techniques can also be used.
- **Feature and Target Separation:** The dataset is split into feature variables (`X`) and target variable (`y` - the credit score).
- **One-Hot Encoding:** Categorical features are encoded into numerical format using one-hot encoding.
- **Feature Scaling:** Standardizes numerical features using `StandardScaler` to ensure that the models perform optimally.

### 3. Model Building
The following machine learning models are implemented:
- **Logistic Regression:** A linear model for binary classification.
- **Decision Tree:** A non-linear, tree-based model.
- **Random Forest:** An ensemble model that aggregates the predictions of multiple decision trees.

Each model is trained on the training data and evaluated on the testing data.

### 4. Model Evaluation
The models are evaluated based on:
- **Accuracy:** The percentage of correctly classified instances.
- **AUC Score:** Area Under the ROC Curve, which measures the model's ability to distinguish between classes.
- **Classification Report:** Includes precision, recall, and F1-score.
- **Confusion Matrix:** Shows the number of true positives, true negatives, false positives, and false negatives.

### 5. Feature Importance (Random Forest)
For the Random Forest model, the feature importance is calculated to identify which features contribute most to the predictions.
This helps in understanding what drives creditworthiness.

### 6. Model Saving
The trained Random Forest model is saved as a `.pkl` file using `joblib`, allowing for easy reuse in future predictions.


