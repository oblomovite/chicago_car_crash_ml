# Injury Severity Classification in Traffic Crashes

## Objective

Predict injury severity in Chicago traffic crashes by analyzing environment, road conditions, crash dynamics, human factors, and location data.

## Data

- Sourced from Chicago's open data portal, merging the following records using CRASH_RECORD_ID:
  - [Crash](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/about_data)
  - [Vehicle](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3/about_data)
  - [People](https://data.cityofchicago.org/Transportation/Traffic-Crashes-People/u6pd-qa9d/about_data)
- Cleaned, transformed, and enhanced with feature engineering to improve predictive power.

## Approach

1. Data Preparation:
   - Impute missing values
   - Drop irrelevant features
   - Feature engineering
     - Reduce dimensionality of categorical variables using rare value grouping
     - Bin continuous variables into ranges
   - Feature Selection
     - Spearman correlation for numerical variables
     - Cramer's V for association strength
     - Chi-squared test for association
     - ANOVA for continuous variables
   - Encode categorical variables using one-hot encoding
   - Scale numerical data using StandardScaler
2. Modeling:
   - Logistic Regression
3. Evaluation:
   - Classification metrics (accuracy, precision, recall, F1-score)
   - Confusion matrix
   - AUC-ROC for robust model assessment.

## Usage

1. Install dependencies and place all CSV data in the /data folder.
2. Run the supplied notebook to preprocess data, train models, and view performance metrics.
3. Experiment with hyperparameter tuning, additional feature engineering, or alternate models to enhance accuracy.

## Next Steps

- Fine-tune sampling techniques (SMOTE) to balance classes effectively.
- Expand or refine feature engineering to capture domain-specific insights.
