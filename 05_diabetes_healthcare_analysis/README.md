# Diabetes Healthcare Analysis & Readmission Prediction

## Project Overview

This project analyses hospital encounters from the Diabetes 130-US Hospitals dataset, covering the period 1999–2008, to investigate factors associated with hospital readmission within 30 days.

The project combines data cleaning, exploratory data analysis, statistical hypothesis testing, feature engineering and predictive modelling. Logistic Regression and Random Forest classifiers are developed and evaluated to compare their ability to identify encounters followed by a readmission within 30 days.

The analysis examines demographic characteristics, clinical information, medication-related variables and previous healthcare utilisation. Model performance is assessed using multiple metrics, including ROC-AUC, precision, recall, F1 score and specificity.

This is an educational healthcare analytics project. The findings describe associations in a historical dataset and should not be interpreted as causal evidence or used to make clinical decisions.

## Objectives

- Clean and inspect a large healthcare dataset.
- Investigate readmission patterns and differences between encounters with and without 30-day readmission.
- Apply statistical tests and effect-size measures to assess observed associations.
- Engineer features for predictive modelling while reducing the risk of target leakage.
- Compare Logistic Regression and Random Forest classifiers.
- Interpret model results and document the limitations of the analysis.

## Dataset

**Dataset:** Diabetes 130-US Hospitals for Years 1999–2008

**Source:** [Kaggle — Diabetes 130-US Hospitals](https://www.kaggle.com/datasets/brandao/diabetes)

The dataset contains 101,766 hospital encounters and 50 original columns. It includes demographic information, admission details, diagnoses, laboratory procedures, medications and previous healthcare utilisation.

The target was defined as a binary indicator of whether an encounter was followed by readmission within 30 days. In the original dataset, 11,357 encounters were labelled `<30`, representing approximately 11.16% of all encounters.

The data represents hospital encounters rather than unique patients. A patient may contribute multiple encounters.

## Tools and Technologies

- Python
- pandas
- NumPy
- Matplotlib and Seaborn
- SciPy
- scikit-learn
- Jupyter Notebook
- Git and GitHub

## Methodology

### 1. Data Inspection and Cleaning

- Inspected dataset dimensions, data types, missing values and duplicate records.
- Converted the dataset's `?` missing-value markers to missing values.
- Removed the highly incomplete weight variable and constant columns.
- Represented missing categorical information using an `Unknown` category where appropriate.
- Converted age bands into numeric midpoint values for analysis.

### 2. Exploratory and Statistical Analysis

- Examined the overall 30-day readmission rate.
- Compared demographic, clinical and healthcare-utilisation variables between encounters with and without 30-day readmission.
- Applied Welch's t-tests to selected continuous variables.
- Used chi-square tests to examine associations between categorical variables and readmission.
- Calculated effect sizes, including Cohen's d and Cramér's V, to distinguish practical differences from statistical significance.
- Examined readmission rates across primary diagnosis categories and glucose-related measurement groups.

### 3. Feature Engineering

- Created a binary 30-day readmission target.
- Grouped diagnosis codes into broader categories.
- Excluded the original target, encounter identifier, patient identifier and discharge disposition from the model features.
- Used a patient-level train/test split to prevent the same patient from appearing in both partitions.
- Applied preprocessing through scikit-learn pipelines, including scaling numerical features and one-hot encoding categorical features.

### 4. Predictive Modelling

Two classification models were developed:

- Logistic Regression
- Random Forest

Both models used class weighting to account for the imbalance between readmitted and non-readmitted encounters.

### 5. Model Evaluation and Interpretation

Models were compared using:

- ROC-AUC
- Precision
- Recall
- F1 score
- Specificity
- Balanced accuracy
- Precision-recall AUC

Model interpretation included Logistic Regression coefficients and Random Forest feature importance.

## Key Findings

### Exploratory Analysis

- The overall 30-day readmission rate was **11.16%**.
- Prior inpatient utilisation showed the strongest association among the continuous variables examined.
- Encounters followed by readmission had an average of 1.22 prior inpatient visits, compared with 0.56 for other encounters.
- The difference in prior inpatient utilisation had a moderate effect size (Cohen's d = 0.532).
- Other statistically significant continuous-variable differences generally had small or negligible effect sizes.

### Model Performance

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| ROC-AUC | 0.6439 | 0.6516 |
| PR-AUC | 0.1922 | 0.1923 |
| Precision | 0.1632 | 0.1738 |
| Recall | 0.5426 | 0.4716 |
| F1 score | 0.2510 | 0.2540 |
| Specificity | 0.6670 | 0.7317 |
| Balanced accuracy | 0.6048 | 0.6017 |

Random Forest achieved a slightly higher ROC-AUC and specificity, while Logistic Regression achieved higher recall at the default classification threshold. PR-AUC and F1 scores were very similar.

Neither model demonstrated strong enough discrimination to support standalone clinical decision-making.

### Model Interpretation

Prior inpatient utilisation was the most important Random Forest feature, accounting for approximately **19.8% of total feature importance**.

Other important features included medical specialty, diagnosis categories, length of stay, medication count, laboratory procedures and prior emergency utilisation.

These are model-based associations and should not be interpreted as causal effects.

## Limitations

- **Historical data:** The dataset covers 1999–2008, so healthcare practices and coding may differ from current settings.
- **Encounter-level records:** Patients can contribute multiple encounters, although a patient-level train/test split was used to reduce leakage between the partitions.
- **Class imbalance:** Approximately 11.16% of encounters resulted in 30-day readmission.
- **Missing information:** Missing information may reflect clinical workflows or measurement decisions rather than random absence.
- **Feature availability:** Discharge disposition was excluded because it may not be available at the intended prediction point.
- **Diagnosis grouping:** Broad diagnostic categories reduce dimensionality but lose some detail.
- **Model performance:** Both models showed modest discrimination and should not be used for clinical decisions.
- **External validation:** The models were evaluated on a held-out subset of the same historical dataset, not an independent hospital system or contemporary population.
- **No causal inference:** Statistical tests and model explanations identify associations, not causes.

## Project Structure

```text
05_diabetes_healthcare_analysis/
├── analysis/
│   └── diabetes_healthcare_analysis.ipynb
├── data/
│   ├── cleaned/
│   │   ├── categorical_chi_square_results.csv
│   │   ├── categorical_effect_sizes.csv
│   │   ├── clinical_readmission_statistics.csv
│   │   ├── continuous_readmission_statistics.csv
│   │   ├── diabetes_cleaned_intermediate.csv
│   │   ├── logistic_regression_coefficients.csv
│   │   ├── model_performance_comparison.csv
│   │   ├── primary_diagnosis_readmission_rates.csv
│   │   ├── random_forest_aggregated_importance.csv
│   │   └── random_forest_feature_importance.csv
│   └── raw/
│       └── diabetic_data.csv
├── .gitignore
└── README.md
```

## How to Run
1. Clone or download the repository.
2. Download the dataset from Kaggle.
3. Place diabetic_data.csv in data/raw/.
4. Install Python and the required libraries.
5. Open analysis/diabetes_healthcare_analysis.ipynb in Jupyter Notebook.
6. Run the notebook cells in order.

The notebook uses relative file paths, so keep the project directory structure intact.

## Conclusion
This project demonstrates an end-to-end healthcare analytics workflow, from data cleaning and statistical analysis to feature engineering, predictive modelling and interpretation.

Prior inpatient utilisation emerged as the strongest continuous-variable association in the exploratory analysis and the most important feature in the Random Forest model. However, both models achieved only modest predictive performance.

The project highlights the importance of patient-level validation, appropriate evaluation metrics, effect-size interpretation and careful consideration of clinical limitations when applying machine learning to healthcare data.