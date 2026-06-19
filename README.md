# Dengue Risk Classification: Logistic Regression vs Random Forest

## Overview

This project explores the use of machine learning techniques to classify dengue cases using clinical patient data. The primary objective is to compare the performance of two widely used classification algorithms—Logistic Regression and Random Forest—and evaluate their ability to identify patterns associated with dengue-positive cases.

Using a structured healthcare dataset, the project follows a complete machine learning workflow including exploratory data analysis, data preprocessing, feature engineering, model training, and performance evaluation.

## Business Problem

Early identification of dengue cases is important for patient management and healthcare resource allocation. Clinical indicators such as platelet count and white blood cell count are often associated with dengue infections and may provide valuable information for predictive modeling.

The goal of this project is not to create a clinical diagnostic tool, but rather to investigate whether machine learning models can successfully learn patterns associated with dengue cases from structured clinical data.

## Dataset

The dataset was obtained from Kaggle and contains clinical information from patients, including laboratory measurements and demographic characteristics.

Features include:

* Age
* Gender
* White Blood Cell Count (WBC)
* Platelet Count
* Additional clinical indicators

Target Variable:

* Dengue Diagnosis (Positive / Negative)

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

The analysis began by exploring the relationships between clinical variables and the dengue diagnosis.

Key activities included:

* Correlation analysis
* Scatter plot visualization
* Missing value assessment
* Feature distribution analysis

### 2. Data Preparation

To prepare the dataset for machine learning:

* Missing numerical values were imputed
* Categorical variables were encoded
* Features were cleaned and transformed
* The dataset was split into training and testing subsets using stratified sampling

### 3. Model Development

Two machine learning models were trained and compared:

#### Logistic Regression

A linear classification algorithm commonly used as a baseline model for binary classification problems.

#### Random Forest Classifier

An ensemble learning method that combines multiple decision trees to capture more complex relationships within the data.

## Model Comparison

| Metric    | Logistic Regression | Random Forest |
| --------- | ------------------- | ------------- |
| Accuracy  | 89%                 | 90%           |
| Precision | Strong              | Strong        |
| Recall    | High                | Higher        |
| F1-Score  | Strong              | Strongest     |

The Random Forest model achieved the highest overall performance, suggesting that non-linear relationships exist within the dataset that are not fully captured by Logistic Regression.

## Key Findings

* Platelet count and white blood cell count exhibited strong associations with dengue diagnosis.
* Dengue-positive cases tended to cluster around lower platelet and WBC values.
* Both models performed well on the classification task.
* Random Forest slightly outperformed Logistic Regression across most evaluation metrics.
* Ensemble methods appear better suited for capturing the complexity of the clinical data.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
├── data/
├── notebooks/
├── images/
├── README.md
└── requirements.txt
```

## Future Improvements

Potential enhancements include:

* Hyperparameter tuning
* Feature importance analysis
* ROC-AUC comparison
* Confusion matrix visualization
* Additional models such as XGBoost or Gradient Boosting
* Deployment as a Streamlit application

## Conclusion

This project demonstrates how machine learning can be applied to healthcare-related datasets to identify patterns associated with dengue cases. Through the comparison of Logistic Regression and Random Forest classifiers, the analysis highlights the importance of model selection and evaluation when building predictive systems. While not intended for clinical use, the project provides a practical example of an end-to-end machine learning workflow using real-world structured data.

