# Hospital Readmission Analysis

## Project Overview

This project analyses hospital encounter data to investigate patterns associated with hospital readmission. The aim is to explore patient and encounter characteristics, identify variables associated with readmission, and communicate findings through a structured data analysis workflow.

The analysis uses Python to inspect, clean and explore the data, with an emphasis on descriptive statistics and interpreting relationships between variables.

## Objectives

- Inspect and prepare hospital encounter data for analysis.
- Explore the distribution of readmissions.
- Investigate how readmission relates to patient and encounter characteristics.
- Summarise key patterns using descriptive statistics and visualisations.
- Identify data-quality issues and limitations that affect interpretation.

## Dataset

**Source:** [Hospital Readmissions — Kaggle](https://www.kaggle.com/datasets/dubradave/hospital-readmissions)

The dataset contains 25,000 hospital encounters. These records should not automatically be interpreted as 25,000 unique patients, because the available analysis does not establish that each encounter belongs to a different individual.

## Tools and Technologies

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Methodology

### 1. Data Inspection and Cleaning

The dataset was inspected to understand its structure, data types, missing values and category distributions. Data-quality limitations were considered before interpreting the results.

### 2. Exploratory Data Analysis

The analysis examined the overall readmission rate and explored how readmission related to encounter characteristics, including previous inpatient utilisation, age, length of stay and other available variables.

### 3. Interpretation

The findings were interpreted as descriptive relationships rather than evidence of causation. Particular attention was paid to the distinction between encounter-level records and unique patients, as well as missing data and category imbalances.

## Key Findings

- The dataset contained **25,000 hospital encounters**.
- Approximately **47.0% of encounters** were recorded as readmissions in the analysis.
- Previous inpatient utilisation showed the strongest descriptive relationship with readmission among the variables examined.
- Age, length of stay and medication changes were also statistically associated with readmission.
- These relationships do not establish that any individual factor caused a readmission.

## Limitations

- **Encounter versus patient records:** The 25,000 observations represent encounters; they should not be assumed to represent 25,000 unique patients.
- **Missing data:** Missing data in fields such as medical specialty may affect comparisons and interpretation.
- **Category imbalance:** Uneven category sizes can make some comparisons less reliable.
- **Association versus causation:** Statistical relationships do not establish causal effects.
- **Scope:** This project focuses on descriptive and statistical analysis rather than developing a predictive machine-learning model.

## How to Run

1. Clone or download the repository.
2. Ensure the dataset files are available in the project's data directory.
3. Install Python and the required libraries.
4. Open hospital_readmission_analysis.ipynb in Jupyter Notebook.
5. Run the notebook cells in order.

Keep the project directory structure intact so that the notebook can locate its input files.

## Conclusion

This analysis explored hospital readmission patterns across 25,000 encounters. Previous inpatient utilisation showed the strongest descriptive relationship with readmission, while age, length of stay and medication changes were also associated with the outcome.

The project demonstrates a structured approach to healthcare data analysis, including data inspection, exploratory analysis and cautious interpretation. The findings should be understood in the context of the dataset's limitations and should not be interpreted as causal evidence.

## Project Structure

```text
01_hospital_readmission/
├── data/
├── hospital_readmission_analysis.ipynb
└── README.md