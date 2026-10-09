# Healthcare Clinic Business Intelligence Dashboard

## Project Overview

This project explores a synthetic healthcare clinic dataset using Python, Excel and Tableau Public to analyse appointment activity, clinical operations, patient utilisation and recorded payment values.

The project demonstrates an end-to-end business intelligence workflow, from data inspection and validation to key performance indicator (KPI) development and interactive dashboard creation.

The aim is to transform structured healthcare data into accessible visual insights that demonstrate how data analytics and business intelligence techniques can support operational monitoring and reporting.

### Business Question

> How are patient activity, clinical services and healthcare payment activity distributed over time and across clinics, doctors and specialties?

## Project Objectives

The main objectives were to:

- Inspect and validate healthcare-related datasets.
- Assess data quality, missing values, duplicate records and relationships between tables.
- Prepare cleaned datasets for analysis and visualisation.
- Calculate key operational and financial indicators.
- Use Excel to review analytical summaries and validate KPIs.
- Develop interactive Tableau dashboards to explore appointment activity, clinical operations and patient profiles.
- Communicate findings clearly while acknowledging the limitations of synthetic data.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Data inspection, cleaning, validation and analysis |
| Pandas | Data manipulation and structured data analysis |
| Jupyter Notebook | Documenting and running the analytical workflow |
| Microsoft Excel | Analytical summaries and KPI validation |
| Tableau Public | Interactive dashboards and data visualisation |
| Git and GitHub | Version control and project documentation |

## Dataset

The project uses the [Healthcare Clinic Dataset from Kaggle](https://www.kaggle.com/datasets/ottiliewinterbourne/healthcare-clinic-dataset).

The dataset contains synthetic records relating to:

- Patients
- Appointments
- Doctors
- Clinics
- Payments
- Treatments
- Prescriptions
- Staff
- Patient insurance

The data represents a simulated healthcare environment rather than real patient activity.

**Important:** The dataset is synthetic and should not be treated as representative of actual healthcare utilisation, clinical outcomes or financial performance.

## Data Preparation and Methodology

The project followed a structured analytical workflow.

### 1. Data Inspection

Python was used to inspect the source tables and understand their structure, including the available fields, record counts, date ranges and categorical variables.

### 2. Data Quality and Validation

The source data was assessed for:

- Missing values
- Duplicate records
- Primary key validity
- Relationships between tables
- Date consistency and ranges
- Categorical distributions
- Potential data quality issues

The raw CSV files were preserved unchanged to maintain the original source data.

### 3. Data Cleaning

Cleaned CSV files were prepared for subsequent analysis and Tableau visualisation.

This step helped establish a consistent foundation for calculating KPIs and developing the dashboards.

### 4. KPI Development and Validation

Excel was used to produce analytical summaries and validate the principal KPIs used in the dashboard.

This provided an additional check on the reported metrics and helped maintain consistency between the supporting analysis and the visualisations.

### 5. Dashboard Development

Tableau Public was used to create three interactive dashboards, each designed to address a different aspect of the business question.

The dashboards combine summary indicators, charts and interactive filters to support exploration of appointment activity, clinical operations and patient and payment profiles.

## Key Metrics

The analysis identified the following headline metrics:

| Metric | Result |
|---|---:|
| Total appointments | 100,000 |
| Completed appointments | 33,409 |
| Cancelled appointments | 33,152 |
| Pending appointments | 33,439 |
| Unique patients with appointments | 19,861 |
| Appointment completion rate | 33.41% |
| Appointment cancellation rate | 33.15% |
| Total recorded treatment/payment value | £80,138,137.64 |
| Average recorded treatment/payment value | £801.38 |

The appointment status counts account for all 100,000 appointment records.

The completion and cancellation rates are calculated as the respective appointment counts divided by the total number of appointments.

**Financial interpretation:** The monetary figures are described as recorded treatment/payment values rather than recognised revenue. The dataset does not provide sufficient accounting information to establish that these values represent recognised revenue.

## Interactive Tableau Dashboard

The Tableau Public workbook contains three dashboards.

### 1. Executive Overview

The Executive Overview provides a high-level summary of appointment activity and operational performance.

It includes:

- Appointment KPIs
- Monthly appointment activity
- Clinic-level activity
- Appointment status distribution
- Interactive clinic filtering

This dashboard is intended to provide a quick overview of the dataset and allow users to explore differences in appointment activity across clinics and time periods.

### 2. Clinical Operations

The Clinical Operations dashboard focuses on the distribution of healthcare services and appointment activity.

It includes:

- Activity by medical specialty
- Appointment status distribution
- Treatment types
- Treatment status
- Top doctors by appointment activity
- Interactive appointment-status filtering

This view allows users to explore how recorded activity is distributed across specialties, treatments and doctors.

### 3. Financial & Patient Profile

The Financial & Patient Profile dashboard examines recorded payment activity alongside selected patient characteristics.

It includes:

- Treatment costs
- Recorded payment values
- Payment methods
- Insurance coverage
- Patient gender profile
- Interactive payment-method filtering

This dashboard brings together financial and demographic summaries to support exploration of the synthetic dataset.

### View the Published Dashboard

**[Explore the Healthcare Clinic Business Intelligence Dashboard on Tableau Public](https://public.tableau.com/app/profile/shaun.agbaje/viz/HealthcareClinicBusinessIntelligenceDashboard/FinancialandPatientProfile?publish=yes)**

The published dashboard can be explored in a web browser.

## Key Observations

The analysis identified several patterns within the synthetic dataset:

- **Appointment activity over time:** Activity is broadly consistent across the full months represented in the dataset. March 2025 and March 2026 represent partial months and should be interpreted accordingly.
- **Appointment status:** Pending, completed and cancelled appointments are distributed relatively evenly across the dataset.
- **Clinic and doctor activity:** Appointment activity is distributed across the 50 clinics and 500 doctors represented in the synthetic data.
- **Treatment activity:** The three treatment types have similar appointment volumes and recorded treatment costs.
- **Payment methods:** Recorded payment values are similar across cash, card and insurance payment methods.
- **Insurance coverage:** Insurance coverage is approximately evenly split among patients with appointments.

These observations describe patterns in the available synthetic records. They should not be interpreted as evidence of real-world healthcare utilisation, clinical effectiveness, patient behaviour or financial performance.

## Skills Demonstrated

This project demonstrates practical skills in healthcare data analytics and business intelligence, including:

### Data Analytics
- Data inspection and cleaning
- Missing-value and duplicate checks
- Data quality validation
- Relational data analysis
- Exploratory data analysis
- KPI calculation and validation

### Business Intelligence
- Translating business questions into analytical metrics
- Developing operational and financial summaries
- Designing interactive dashboards
- Using filters to support data exploration
- Presenting findings through data visualisation

### Technical and Professional Skills
- Python and Pandas
- Jupyter Notebook
- Excel-based analytical validation
- Tableau Public dashboard development
- Git and GitHub project organisation
- Analytical documentation
- Communicating findings and limitations clearly

## Project Structure

The project is organised into separate folders for analysis, dashboards and data.

```text
04_healthcare_dashboard/
├── analysis/
│   ├── healthcare_dashboard_analysis.ipynb
│   └── healthcare_dashboard_analysis.xlsx
├── dashboard/
│   ├── Healthcare Clinic Business Intelligence Dashboard.twb
│   ├── Healthcare Clinic Business Intelligence Dashboard.twbx
│   └── healthcare_dashboard_analysis.hyper
├── data/
│   ├── cleaned/
│   └── raw/
├── .gitignore
└── README.md
```

- `analysis/` contains the Jupyter Notebook and Excel workbook used for analysis and KPI validation.
- `dashboard/` contains the Tableau workbook files and Hyper extract.
- `data/raw/` is intended for the original source data.
- `data/cleaned/` is intended for the prepared datasets used in analysis and visualisation.
- `README.md` documents the project, methodology, findings and limitations.

The presence of a folder in the project structure does not necessarily mean that it contains committed files. Raw data availability depends on the repository contents and the dataset's download requirements.

## How to Run

### Option 1: Explore the Published Dashboard

The simplest way to explore the project is to open the published dashboard:

[Open the interactive Tableau dashboard](https://public.tableau.com/app/profile/shaun.agbaje/viz/HealthcareClinicBusinessIntelligenceDashboard/FinancialandPatientProfile?publish=yes)

No local installation is required to view the published dashboard in a web browser.

### Option 2: Review the Supporting Analysis

To inspect the analytical work:

1. Clone or download this GitHub repository.
2. Navigate to the `04_healthcare_dashboard` folder.
3. Open `analysis/healthcare_dashboard_analysis.ipynb` in Jupyter Notebook or JupyterLab.
4. Review the data inspection, cleaning, validation and KPI calculations.
5. Open `analysis/healthcare_dashboard_analysis.xlsx` in Microsoft Excel or a compatible spreadsheet application to examine the supporting summaries and KPI checks.

To rerun the analysis, ensure that Python, Jupyter Notebook and the required Python libraries are installed. The original dataset may also need to be downloaded from Kaggle, and file paths may need to be adjusted to match your local environment.

### Option 3: Inspect the Tableau Workbooks

If Tableau Desktop is available:

1. Navigate to the `dashboard/` folder.
2. Open the Tableau workbook.
3. Review the dashboard layouts, charts, filters and data connections.
4. If prompted, update the data connections to point to the relevant local data files.

The `.twb` file contains the workbook definitions, while the `.twbx` file is a packaged Tableau workbook intended to make sharing easier. The exact availability of supporting data depends on how the workbook was packaged.

## Limitations

Several limitations should be considered when interpreting the results:

- **Synthetic data:** The dataset does not represent actual healthcare activity and cannot support conclusions about real-world healthcare services.
- **Financial interpretation:** Recorded treatment and payment values should not be interpreted as recognised revenue or audited financial results.
- **Descriptive analysis:** The project describes patterns in the available data and does not establish causal relationships.
- **Data quality:** Some source records contain synthetic edge cases, including implausible dates of birth.
- **Generalisability:** The observed distributions may reflect how the synthetic dataset was constructed rather than realistic patient or operational behaviour.
- **Decision support:** The dashboards are intended to demonstrate analytical and business intelligence skills, not to provide clinical, operational or financial decision support for a real healthcare organisation.

## Conclusion

This project demonstrates an end-to-end healthcare business intelligence workflow, combining Python-based data preparation and validation, Excel-based KPI checks, and interactive Tableau dashboard development.

The three dashboards provide complementary views of appointment activity, clinical operations, recorded payment values and patient profiles. Together, they demonstrate how structured data can be transformed into interactive visualisations that make operational patterns easier to explore and communicate.

The project also highlights the importance of data quality checks, consistent KPI definitions and transparent reporting of analytical limitations.

Although the dataset is synthetic and the findings cannot be generalised to real healthcare settings, the project demonstrates practical skills in data analytics, KPI development, dashboard design and business intelligence communication.