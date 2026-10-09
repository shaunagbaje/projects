# COVID-19 Gene Expression Analysis

## Project Overview

This project analyses gene-expression data to investigate differences between lung tissue samples from fatal COVID-19 cases and normal samples.

Using Python, the project follows a gene-expression analysis workflow involving sample metadata processing, count-data inspection, normalisation, exploratory analysis, differential-expression testing and sensitivity analysis.

The analysis focuses on identifying genes with different expression levels between the two groups, while considering the limitations of bulk tissue data and the statistical methods used.

## Objectives

- Inspect and prepare gene-expression count data and sample metadata.
- Identify lung tissue samples and distinguish COVID-19 from normal samples.
- Filter genes with low expression.
- Explore sample-level patterns using principal component analysis (PCA).
- Identify genes differentially expressed between the two groups.
- Assess the sensitivity of the results to an unusual sample.
- Document the methodological and biological limitations of the analysis.

## Dataset

**Source:** [Fatal COVID-19 Gene Data — Kaggle](https://www.kaggle.com/datasets/vijayveersingh/fatal-covid-19-gene-data)

The project uses gene-expression count data and associated sample metadata. The original count matrix contained 58,735 genes and 38 sample columns. The analysis focused on 19 lung tissue samples:

- **9 COVID-19 samples**
- **10 normal samples**

The analysis concerns fatal COVID-19 cases represented in the dataset and should not be assumed to represent all COVID-19 infections or disease severities.

## Tools and Technologies

- Python
- pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

## Methodology

### 1. Data Inspection and Sample Selection

The raw gene-expression count matrix and sample metadata were inspected and linked to identify the samples relevant to the analysis.

The primary comparison was restricted to lung tissue samples classified as COVID-19 or normal.

### 2. Expression Filtering and Normalisation

Expression counts were converted to counts per million (CPM). Genes were retained if they had CPM of at least 1 in at least three samples.

This filtering step reduced the influence of genes with very low expression across the selected samples.

### 3. Exploratory Analysis

Principal component analysis (PCA) was applied to the transformed expression data to explore variation between samples.

The first principal component explained approximately **34.85%** of the variance, and the second explained approximately **12.56%**.

### 4. Differential Expression Analysis

Expression values were transformed using log2(CPM + 1). Welch's t-tests were used to compare expression between COVID-19 and normal samples.

P-values were adjusted for multiple testing using the Benjamini–Hochberg false discovery rate procedure.

Genes were classified as differentially expressed using both:
- Adjusted p-value below 0.05
- Absolute log2 fold change of at least 1

This approach is an educational statistical workflow. It is not a replacement for specialised RNA-seq differential-expression methods such as DESeq2, edgeR or limma-voom.

### 5. Sensitivity Analysis

An unusual sample, SRR12816735, was examined in a sensitivity analysis.

The analysis was repeated without that sample to assess how its inclusion affected the number of genes meeting the differential-expression criteria.

## Key Findings

### Differential Expression

Using the selected statistical thresholds, **3,047 genes** met the differential-expression criteria:

- **136 upregulated genes**
- **2,911 downregulated genes**

Examples among the most highly ranked upregulated genes included `PI15`, `PTX3`, `KRT6A`, `SPP1` and `COL3A1`.

Examples among the most highly ranked downregulated genes included `FOSB`, `RTKN2`, `SFTPC`, `NCKAP5` and `AGER`.

These results describe differences in expression in the selected samples. They do not establish that individual genes cause COVID-19 outcomes.

### Sensitivity Analysis

When the unusual sample was excluded, the number of genes meeting the differential-expression criteria decreased from 3,047 to 2,631, a reduction of approximately **13.7%**.

This indicates that the results were sensitive to the composition of the sample set and reinforces the importance of sample-level quality checks.

## Limitations

- **Small sample size:** The primary comparison included only 19 lung tissue samples.
- **Fatal cases:** The findings may not generalise to mild, moderate or non-fatal COVID-19.
- **Bulk tissue composition:** Observed expression differences may reflect changes in cell-type composition as well as changes in gene expression within individual cells.
- **Statistical method:** Welch's t-tests on log2(CPM + 1) are an educational approach and do not model RNA-seq count distributions as specialised differential-expression methods do.
- **Sensitivity to samples:** Excluding one unusual sample changed the number of genes passing the selected thresholds.
- **Association versus causation:** Differential expression does not demonstrate that a gene causes disease or determines clinical outcomes.
- **External validation:** The results were not independently validated in a separate dataset.

## How to Run

1. Clone or download the repository.
2. Obtain the dataset from Kaggle.
3. Place the required raw data files in the project's expected data location.
4. Install Python and the required libraries.
5. Open gene_expression_analysis.ipynb in Jupyter Notebook.
6. Run the notebook cells in order.

Keep the project directory structure intact so the notebook can locate the required input files.

## Conclusion

This project examined gene-expression differences between lung tissue samples from fatal COVID-19 cases and normal samples. The analysis identified 3,047 genes meeting the selected statistical and fold-change thresholds, including 136 upregulated and 2,911 downregulated genes.

The sensitivity analysis showed that excluding one unusual sample reduced the number of genes meeting those thresholds by approximately 13.7%. This highlights the importance of sample quality and robust validation in gene-expression analysis.

Overall, the project demonstrates a gene-expression analysis workflow covering metadata processing, expression filtering, exploratory analysis, differential-expression testing and sensitivity analysis. The findings should be interpreted cautiously because of the small sample size, bulk tissue composition, historical context and limitations of the statistical method.

## Project Structure

```text
03_covid_gene_expression/
├── data/
├── gene_expression_analysis.ipynb
└── README.md