# Chronic Kidney Disease Clinical Analysis

## Project Overview

This project analyses clinical data to investigate differences between patients classified as having chronic kidney disease (CKD) and those classified as not having CKD.

Using Python and statistical analysis, the project explores clinical measurements, demographic characteristics and categorical indicators to identify variables associated with CKD status.

The focus is on data cleaning, exploratory data analysis, hypothesis testing and effect-size interpretation rather than predictive machine learning.

## Objectives

- Inspect and clean clinical data containing missing values.
- Compare clinical measurements between CKD and non-CKD groups.
- Apply appropriate statistical tests to assess observed differences.
- Use effect sizes and confidence intervals to interpret the magnitude of differences.
- Examine associations between categorical clinical variables and CKD status.
- Document data-quality issues and limitations.

## Dataset

**Source:** [Chronic Kidney Disease Dataset — Kaggle](https://www.kaggle.com/mansoordaku/ckdisease)

The dataset contains 400 records and 25 clinical features in the cleaned analytical dataset, covering demographic information, clinical measurements and categorical indicators associated with kidney disease.

The analysis distinguishes between records classified as CKD and those classified as not CKD.

## Tools and Technologies

- Python
- pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Methodology

### 1. Data Inspection and Cleaning

- Inspected dataset dimensions, data types and missing values.
- Prepared the clinical variables for statistical analysis.
- Examined the distribution of CKD and non-CKD records.
- Considered missingness when interpreting the results.

### 2. Continuous Variable Analysis

Welch's independent-samples t-tests were used to compare selected clinical measurements between the CKD and non-CKD groups.

Cohen's d was calculated to assess the standardised magnitude of group differences, and 95% confidence intervals were used to quantify uncertainty around the estimated mean differences.

### 3. Categorical Variable Analysis

Chi-square tests were used to examine associations between selected categorical variables and CKD status.

Results were interpreted cautiously where category distributions showed strong separation between the groups.

## Key Findings

The cleaned dataset contained **400 records**:
- **250** classified as CKD
- **150** classified as not CKD

Several continuous clinical measurements differed statistically between the two groups:

| Variable | Cohen's d |
|---|---:|
| Age | 0.479 |
| Blood pressure | 0.632 |
| Blood glucose | 0.939 |
| Blood urea | 0.847 |
| Serum creatinine | 0.647 |
| Haemoglobin | -2.435 |

Haemoglobin showed the largest standardised difference in magnitude among these variables. Blood glucose and blood urea also showed relatively large group differences.

Categorical analyses identified associations between CKD status and variables including hypertension and diabetes. These findings describe the observed dataset and do not establish that these characteristics caused CKD.

## Limitations

- **Sample size:** The dataset contains 400 records, limiting the scope of generalisation.
- **Missing values:** Clinical variables have missing observations, which can affect comparisons and statistical power.
- **Group separation:** Some categorical variables show strong separation between CKD and non-CKD records, which should be interpreted in the context of the dataset.
- **Association versus causation:** Statistical differences do not establish causal relationships.
- **External validity:** Findings from this dataset may not generalise to other patient populations or clinical settings.
- **Scope:** This project focuses on statistical analysis rather than developing or validating a clinical prediction model.

## Project Structure

```text
02_chronic_kidney_disease/
├── data/
├── chronic_kidney_disease_analysis.ipynb
└── README.md
```

## How to Run

1. Clone or download the repository.
2. Ensure the dataset files are available in the project's data directory.
3. Install Python and the required libraries.
4. Open chronic_kidney_disease_analysis.ipynb in Jupyter Notebook.
5. Run the notebook cells in order.

Keep the project directory structure intact so the notebook can locate its input files.

## Conclusion

This project used statistical analysis to examine clinical differences between CKD and non-CKD records.

Haemoglobin, blood glucose and blood urea showed relatively large standardised differences between the groups, while categorical analyses identified associations involving hypertension and diabetes.

The project demonstrates a structured clinical data analysis workflow, combining data cleaning, hypothesis testing, effect-size estimation and cautious interpretation. The results should be understood within the limitations of the dataset and should not be interpreted as causal evidence or a substitute for clinical assessment.