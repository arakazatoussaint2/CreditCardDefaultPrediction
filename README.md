# Credit Card Default Prediction

A machine learning project to predict credit card default risk using exploratory data analysis, principal component analysis (PCA), and classification models.

## Dataset source

This project uses the "Default of Credit Card Clients" dataset provided by the UCI Machine Learning Repository. This dataset contains 30,000 instances with 23 variables and was collected by I-Cheng Yeh in 2009. It comprises historical data from Taiwanese credit card clients, including their demographic information (gender, education, marital status, age), credit limit, as well as their payment history and billing amounts over a six-month period (April to September 2005). The dataset aims to predict the probability of credit default among clients and was used to compare the predictive accuracy of various data mining methods. It is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license, accessible via https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients with the DOI 10.24432/C55S3H.

##  Overview

This project analyzes credit card client data to identify patterns and predictive factors associated with default behavior. Using PCA for dimensionality reduction and multiple classification models, we build a system to assist in credit risk assessment and decision-making.

##  Objectives

- **Exploratory Data Analysis (EDA):** Understand feature distributions, correlations, and client demographics.
- **Principal Component Analysis:** Reduce feature dimensionality and interpret key axes of variation.
- **Clustering Analysis:** Segment clients into profiles (e.g., high-exposure, mature, high-limit profiles).
- **Classification Modeling:** Train and evaluate models (Logistic Regression, others) to predict default risk.
- **Business Insights:** Provide actionable recommendations for credit policy and risk monitoring.

##  Dataset

- **Features:** Credit limit (`LIMIT_BAL`), age (`AGE`), bill amounts (`BILL_AMT1`–`BILL_AMT6`), payment status (`PAY_0`–`PAY_6`), account age (`MONTHS_BALANCE`), and others.
- **Target:** Binary default indicator (`TARGET`: 0 = no default, 1 = default).
- **Size:** Multiple client records with complete feature coverage.
- **Preprocessing:** Feature scaling, missing value handling, and outlier assessment.

##  Methodology

### 1. Exploratory Data Analysis
- Univariate and bivariate analysis of key features.
- Correlation heatmap to identify strong feature relationships.
- Distribution analysis for demographics and financial behavior.

### 2. Principal Component Analysis (PCA)
- Standardized scaling of selected features (`LIMIT_BAL`, `AGE`, `BILL_AMT1`–`BILL_AMT6`).
- Explained variance analysis to determine optimal component count.
- **PC1 (Overall Exposure):** Captures outstanding balance levels and credit usage.
- **PC2 (Demographic Profile):** Reflects customer age and credit limit profiles.
- Interpretation of loadings guides business application and segmentation.

### 3. Clustering
- K-means clustering on PCA-reduced features.
- Profile interpretation: high-exposure, mature/high-limit, young/low-limit segments.
- Business implications for credit policy and monitoring strategies.

### 4. Prediction Modeling
- Train Logistic Regression model.
- Evaluation metrics: accuracy, precision, recall, ROC-AUC.
- Feature importance analysis to identify top predictive factors.
- Recommendations: combine PC1 (exposure) with payment history (`PAY_0`) for effective risk scoring.

##  Project Structure
credit-card-default-prediction/
- README.md # Project documentation
- Exploration_Analysis&Predictions.ipynb # Main analysis and modeling notebook
- default-of-credit-card-clients.xls # csv file
