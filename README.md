
# Cervical Cancer Analysis

This project analyzes a dataset of demographic, behavioral, and diagnostic risk factors to identify key predictors of cervical cancer and predict biopsy outcomes using Python-based data analysis, visualization, and machine learning techniques.

## Dataset

The dataset (`risk_factors_cervical_cancer.csv`) contains features such as:
- Age, number of sexual partners, age at first intercourse, number of pregnancies
- Smoking habits (years, packs/year), hormonal contraceptive use, IUD use
- History of sexually transmitted diseases (STDs)
- Diagnostic test results (Hinselmann, Schiller, Citology, Biopsy)

Missing values are represented by `?` and are handled during preprocessing.

## Data Processing Pipeline

1. **Load and Clean Data**: Replace `?` with NaN, remove columns with >50% missing values.
2. **Impute Missing Values**: Use KNN imputation for numerical features and mode for categorical features.
3. **Feature Engineering**:
	- Remove highly correlated features to avoid redundancy.
	- Select features most correlated with the target (Biopsy result).
4. **Exploratory Data Analysis**:
	- Visualize missing data, class imbalance, and feature distributions.
	- Analyze relationships between risk factors and biopsy outcomes.

## Machine Learning Workflow

1. **Class Imbalance Handling**: Apply SMOTE to balance positive/negative biopsy classes.
2. **Feature Selection**: Use correlation and permutation importance to select top predictors.
3. **Model Training**: Train a Random Forest classifier with hyperparameter tuning (GridSearchCV).
4. **Evaluation**:
	- Accuracy, classification report, and confusion matrix on the test set
	- Feature importance analysis

## Key Findings

- Smoking, hormonal contraceptive use, IUD use, and certain diagnostic test results are associated with higher risk.
- The model achieves good recall, which is important for medical diagnosis to minimize missed cases.

## Usage

1. Install dependencies (see code.ipynb for required packages such as pandas, numpy, scikit-learn, seaborn, imbalanced-learn, matplotlib).
2. Run the analysis in `code.ipynb` step by step.

## Visualizations

The notebook generates:
- Heatmaps of missing values and feature correlations
- Distribution plots and boxplots for key features
- Confusion matrix and feature importance plots

## References

- [Original dataset](https://archive.ics.uci.edu/ml/datasets/Cervical+cancer+%28Risk+Factors%29)

---
For more details, see the code and comments in `code.ipynb`.
