# Healthcare Clinic Business Intelligence Dashboard

## Project Overview

This project analyses a synthetic healthcare clinic dataset using Python, Excel and Tableau Public to investigate operational activity, clinical services, patient utilisation and recorded payment values.

The project demonstrates an end-to-end business intelligence workflow, from data validation and preparation through to KPI analysis and interactive dashboard development.

### Business Question

> How are patient activity, clinical services and healthcare payment activity distributed over time and across clinics, doctors and specialties?

## Tools

- Python — data inspection, cleaning and validation
- Excel — analytical summaries and KPI validation
- Tableau Public — interactive business intelligence dashboard

## Dataset

The project uses the **Healthcare Clinic Dataset** from Kaggle.

The dataset contains synthetic records covering:

- Patients
- Appointments
- Doctors
- Clinics
- Payments
- Treatments
- Prescriptions
- Staff
- Patient insurance

The data is synthetic and should not be interpreted as representative of real-world healthcare activity.

## Data Preparation

The raw CSV files were preserved unchanged.

Python was used to:

- Inspect the source tables
- Check missing values and duplicate records
- Validate primary keys
- Validate relationships between tables
- Check date ranges and categorical distributions
- Create cleaned CSV files for analysis and Tableau

Excel was then used to produce analytical summaries and validate the main KPIs used in the dashboard.

## Key Metrics

The analysis contains:

- 100,000 appointments
- 33,409 completed appointments
- 33,152 cancelled appointments
- 33,439 pending appointments
- 19,861 unique patients with appointments
- 33.41% completion rate
- 33.15% cancellation rate
- £80,138,137.64 total recorded treatment/payment value
- £801.38 average treatment/payment value

Payment values are described as recorded payment values rather than revenue because the dataset does not provide sufficient accounting information to establish recognised revenue.

## Dashboard

The Tableau Public workbook contains three interactive dashboards.

### Executive Overview

Provides a high-level view of:

- Appointment KPIs
- Monthly appointment activity
- Clinic activity
- Appointment status
- Interactive clinic filtering

### Clinical Operations

Examines:

- Activity by specialty
- Appointment status
- Treatment types
- Treatment status
- Top doctor appointment activity
- Interactive appointment-status filtering

### Financial & Patient Profile

Examines:

- Treatment costs
- Recorded payment values
- Payment methods
- Insurance coverage
- Patient gender profile
- Interactive payment-method filtering

### Tableau Public

[View the interactive Tableau dashboard](https://public.tableau.com/app/profile/shaun.agbaje/viz/HealthcareClinicBusinessIntelligenceDashboard/FinancialandPatientProfile?publish=yes)

## Key Observations

- Appointment activity is broadly consistent across the full months in the dataset, while March 2025 and March 2026 represent partial months.
- Appointment statuses are distributed relatively evenly across pending, completed and cancelled appointments.
- Appointment activity is distributed across the 50 clinics and 500 doctors represented in the synthetic dataset.
- The three treatment types have very similar appointment volumes and recorded treatment costs.
- Recorded payment values are similar across cash, card and insurance payment methods.
- Insurance coverage is approximately evenly split among patients with appointments.
- The observed distributions are characteristics of this synthetic dataset and should not be interpreted as evidence of real-world healthcare utilisation, clinical outcomes or financial behaviour.

## Skills Demonstrated

- Data cleaning and validation
- Relational data analysis
- KPI development
- Healthcare operations analysis
- Exploratory data analysis
- Excel-based analytical validation
- Tableau dashboard development
- Interactive business intelligence
- Data storytelling
- Analytical documentation

## Limitations

- The dataset is synthetic and not representative of real-world healthcare activity.
- Payment values should not be interpreted as recognised revenue.
- The analysis is descriptive and does not establish causal relationships.
- Some source records contain synthetic edge cases, such as implausible dates of birth.
- The dashboard is intended to demonstrate healthcare analytics and business intelligence skills rather than provide clinical or financial decision support.