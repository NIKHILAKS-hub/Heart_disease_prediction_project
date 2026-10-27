# Heart Disease Prediction – Data Preprocessing and Exploratory Data Analysis

## Project Overview

This project focuses on understanding, cleaning, and preparing the Heart Failure Prediction dataset for machine learning. The objective is to explore patient-related features and prepare the data to classify whether a patient record indicates the presence or absence of heart disease.

The project covers data cleaning, exploratory data analysis (EDA), outlier detection, feature engineering, categorical encoding, and correlation analysis.

## Business Objective

Heart disease is a major public health concern. Analysing patient data can help identify patterns associated with heart disease and support the development of data-driven research and decision-support systems.

The goal of this project is to prepare a reliable, machine-learning-ready dataset for a future classification model.


## Dataset

- **Dataset:** Heart Failure Prediction
- **Source:** [Kaggle – Heart Failure Prediction](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- **Target variable:** `heart_disease`
- **Target values:** `0` – No heart disease; `1` – Heart disease

The dataset contains features such as age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting ECG, maximum heart rate, exercise-induced angina, oldpeak, and ST slope.

## Project Workflow

1. **Data Loading and Inspection**
   - Loaded the original dataset using Pandas.
   - Examined dataset dimensions, column names, data types, and summary statistics.
   - Checked for missing values and duplicate records.

2. **Data Cleaning**
   - Standardized column names using lowercase snake_case.
   - Investigated suspicious zero values in resting blood pressure and cholesterol.
   - Replaced the identified zero values with missing values and applied median imputation.

3. **Outlier Detection**
   - Investigated numerical features using the Interquartile Range (IQR) method and Z-scores.
   - Visualized outliers using box plots.
   - Retained remaining flagged values where there was insufficient evidence to classify them as errors.

4. **Feature Engineering**
   - Created an `age_group` feature for exploratory analysis.

5. **Categorical Encoding**
   - Encoded binary categorical variables.
   - Applied one-hot encoding to categorical features such as chest pain type, resting ECG, and ST slope.

6. **Exploratory Data Analysis**
   - Examined feature distributions and the target variable.
   - Created visualizations to investigate patterns in the data.
   - Used a correlation matrix and heatmap to explore relationships between features.

7. **Machine-Learning Data Preparation**
   - Prepared a cleaned dataset and a machine-learning-ready dataset.
   - Reviewed feature relationships and potential redundancy.

## Key Observations

- The original dataset contains zero values in resting blood pressure and cholesterol that were treated as potentially invalid measurements.
- Median imputation was selected because it is less sensitive to extreme values than mean imputation.
- Several numerical features contained values flagged as potential outliers.
- Some encoded features showed notable associations with the target variable.
- Strong correlations between certain one-hot encoded columns reflect their mutually exclusive categories.
- Correlation does not establish causation or, by itself, determine a feature's predictive importance.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Files

The repository should contain the following files and folders:

```text
WEEK2_DATASCIENCE/
├── README.md
├── heart.csv
├── cleaned_dataset.csv
├── machine_learning_ready_dataset.csv
├── WEEK2_DS.ipynb
├── Business_Understanding_Report.docx
├── Data_Preprocessing_Report.docx
└── visualizations/
```


## Limitations

- Median imputation introduces estimated values rather than recovering true measurements.
- Outlier detection methods flag unusual values but do not prove that the values are errors.
- Correlation analysis alone cannot establish causal relationships or conclusively identify the best predictors.
- The prepared data has not, by itself, demonstrated the performance of a trained predictive model.
- Any future model would require appropriate evaluation, validation, and safeguards before real-world use.

## Future Work

- Build and evaluate classification models.
- Compare model performance using suitable metrics such as precision, recall, F1-score, and ROC-AUC.
- Use a proper train-test split and fit preprocessing steps on training data to avoid data leakage.
- Investigate feature importance and model interpretability.

## Author

NIKHILA K. S.
