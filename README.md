# IEEE Fraud Detection with XGBoost, Isolation Forests, and Deep Learning

This repository presents a solution for the [IEEE-CIS Fraud Detection (Kaggle competition)](https://www.kaggle.com/competitions/ieee-fraud-detection/overview). The objective is to detect fraudulent transactions in a highly imbalanced dataset, using real-world data provided by Vesta Corporation. This project utilizes an XGBoost classifier, an isolation forest for anomaly detection, and a deep learning model, comparing their performance and addressing class imbalance through oversampling techniques.

## Project Overview

The dataset is heavily imbalanced, with a predominance of non-fraudulent transactions. This project applies three distinct models to approach this binary classification problem:

1. **XGBoost Classifier**: Achieved the highest ROC AUC of 0.9671, establishing itself as the top-performing model.
2. **Isolation Forest**: Used for anomaly detection with an ROC AUC of 0.7229, leveraging unsupervised learning to identify outliers.
3. **Deep Learning Model**: Achieved an ROC AUC of 0.9012, demonstrating the potential of neural networks in large-scale classification tasks.
   
Given the exceptional performance of XGBoost and the dataset size, additional hyperparameter tuning was deemed unnecessary at this stage.

## Approach

1. **Data Preprocessing**:
* Missing values were handled, and categorical variables were encoded.
* Numerical features were scaled to standardize the data in the deep learning and isolation forest models.
2. **Handling Class Imbalance**:
* The Synthetic Minority Oversampling Technique (SMOTE) was applied to the training data in the deep learning model, but it was deemed not necessary in the isolation forest and XGBoost models. 
* Both techniques were evaluated to determine which offered better model performance and alignment with the test distribution.
3. **Modeling**:
* Three distinct models—XGBoost, Isolation Forest, and a deep learning neural network—were implemented to address the classification task from different perspectives.
* Model performance was evaluated primarily through the ROC AUC metric.
4. **Evaluation**:
* The XGBoost classifier showed superior performance, followed by the deep learning model.

## Requirements

* Python 3.8+
* Jupyter Notebook
* Libraries: ```pandas```, ```numpy```, ```scikit-learn```, ```xgboost```, ```imbalanced-learn```, ```tensorflow```, ```keras```
To install all requirements:

```
pip install -r requirements.txt
```

## Getting Started

1. **Clone the repository**:
```
git clone https://github.com/hypercohomology/IEEE_fraud_detection.git
cd IEEE_fraud_detection
```
2. **Extract the Data Files**: Due to file size constraints on GitHub, they could not be uploaded here. Instead, access the train and test data directly from [Kaggle](https://www.kaggle.com/competitions/ieee-fraud-detection/data).
3. **Run the Jupyter Notebook**: Open ```XGBoost_fraud.ipynb``` in Jupyter to explore the data analysis, model training, and evaluation processes.

