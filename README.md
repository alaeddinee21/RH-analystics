---

# RH Analytics

![Human Resources Promotion](https://events.ceu.edu/sites/default/files/styles/crop_promo_image/public/human-resources-101-intro-to-human-resources186458large.jpg?itok=8x6z1C-E)

## Overview

The RH Analytics project aims to streamline the employee promotion process for a large multinational corporation (MNC) by predicting eligible candidates for promotion to manager positions and below. The goal is to identify potential candidates at a checkpoint to expedite promotions and reduce delays.

## Problem Statement

The client faces delays in the promotion cycle as the final promotions are only announced after training and evaluations. This project uses predictive analytics to identify candidates for promotion earlier in the process, based on various performance metrics and employee data.

## Data

- **Training Data**: `train.csv`
- **Test Data**: `test.csv`

## Evaluation Metric

The model's performance is evaluated using the F1 Score, which balances precision and recall.

## Data Inspection

1. **Data Loading**: Read the CSV files using pandas.
2. **Exploration**: Conduct exploratory data analysis (EDA) to understand the distribution of data, missing values, and correlations.
3. **Categorization**: Classify variables into categories such as employee information, demographics, and performance metrics.

## Data Preprocessing

1. **Handling Missing Values**: Fill missing values in categorical columns with the mode.
2. **Feature Encoding**:
   - **Numerical Features**: Scale numerical features using `StandardScaler`.
   - **Categorical Features**: One-hot encode categorical features.
   - **Target Encoding**: Apply target encoding to the `region` column.
3. **Handling Imbalance**: Use SMOTE to address class imbalance.

## Model Pipeline

1. **Preprocessing**:
   - Numerical features: StandardScaler
   - Categorical features: OneHotEncoder
   - Target encoding: TargetEncoder
2. **Model**: CatBoostClassifier
3. **Integration**: Combine preprocessing and modeling using imbalanced pipeline.

## Model Tuning

- **Grid Search**: Optimize hyperparameters using GridSearchCV.
- **Metrics**: Evaluate model performance using F1 Score.

## Results

- **Best Parameters**: Parameters identified through GridSearchCV.
- **Test F1 Score**: F1 Score of the best model on the test set.
- **Accuracy**: Accuracy score of the final model.

## Installation

```bash
pip install category_encoders xgboost ydata_profiling imblearn catboost
```

## Code

The code performs the following steps:
1. Load and inspect the data.
2. Preprocess the data.
3. Define and tune the model pipeline.
4. Evaluate and report the results.

## Usage

1. **Load Data**: Read the `train.csv` and `test.csv` files.
2. **Preprocess Data**: Handle missing values and encode features.
3. **Train Model**: Fit the model pipeline on training data.
4. **Evaluate Model**: Assess performance using F1 Score and other metrics.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---
