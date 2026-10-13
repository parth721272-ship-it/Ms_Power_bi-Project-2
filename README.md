# Hospital Patient Analytics Dashboard

## Project Overview

This project is a Power BI report built to explore a healthcare dataset
and present patient, hospital, admission, and billing insights through
interactive dashboards.

The report includes three pages:

1.  **Hospital Patient Analytics Dashboard** --- an overview of patient
    volume, revenue, average billing, average length of stay, patient
    counts by medical condition, monthly admissions, and hospital
    billing revenue.
2.  **Patient Detail Table** --- a page for exploring patient-level
    records.
3.  **Billing Analysis** --- a page focused on billing-related analysis.

## Dataset

-   **Dataset:** Healthcare Dataset
-   **Source:** [Kaggle --- Healthcare
    Dataset](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)
-   **Main file:** `healthcare_dataset.csv`
-   **Lookup file:** `Condition_Dept_Lookup.csv`

The lookup file maps medical conditions to departments:

  Medical Condition   Department
  ------------------- ---------------
  Cancer              Oncology
  Diabetes            Endocrinology
  Hypertension        Cardiology
  Obesity             Bariatrics
  Asthma              Pulmonology
  Arthritis           Rheumatology

## Tools Used

-   Microsoft Power BI Desktop
-   Power Query Editor for data preparation and transformation
-   CSV files as data sources

## Data Preparation

The Power Query workflow includes steps such as:

-   Promoting headers and setting data types
-   Creating admission year and month fields
-   Calculating length of stay
-   Creating a patient index
-   Creating age categories
-   Creating billing tiers
-   Creating stay categories
-   Creating risk flags
-   Preparing summary queries for conditions, hospitals, insurance
    providers, and monthly admissions

### Derived fields

  -----------------------------------------------------------------------
  Field                               Purpose
  ----------------------------------- -----------------------------------
  `Admission_Year`                    Year of admission

  `Admission_Month`                   Admission month name

  `Admission_Month_Num`               Numeric month for sorting

  `Length_of_Stay_Days`               Difference between discharge and
                                      admission dates

  `Patient_ID`                        Index-based identifier created in
                                      Power Query

  `Age_Category`                      Groups patients into age categories

  `Billing_Tier`                      Groups billing amounts into tiers

  `Stay_Category`                     Groups length of stay into
                                      categories

  `Risk_Flag`                         Categorizes test results for report
                                      analysis

  `Billing_Amount_Fixed`              Absolute value of billing amount

  `Billing_Rounded`                   Rounded billing amount
  -----------------------------------------------------------------------

## Summary Queries

The report's Power Query model includes summary queries for:

-   **Condition_Summary** --- patient count, average billing, and
    average length of stay by medical condition
-   **Hospital_Summary** --- patient count, total billing revenue, and
    average billing by hospital
-   **Insurance_Summary** --- covered patient count, total claims, and
    average claim by insurance provider
-   **Monthly_Admissions** --- monthly patient count and revenue by
    admission year and month

Additional lookup or analysis queries may be present in the Power BI
file.

## Dashboard Features

The main dashboard currently includes:

-   KPI cards for total patients, total revenue, average billing, and
    average length of stay
-   Patient count by medical condition
-   Patient distribution by insurance provider
-   Monthly patient admissions trend
-   Top 10 hospitals by billing revenue
-   Slicers for admission type, medical condition, and admission year

The report uses filters to support interactive exploration of the
dataset.

## How to Open the Project

1.  Install or open **Microsoft Power BI Desktop**.
2.  Open the `.pbix` project file.
3.  If Power BI asks for data-source locations, browse to the relevant
    CSV files.
4.  Select **Home → Refresh** to update the data.
5.  Use the report tabs at the bottom to move between dashboard pages.
6.  Use the slicers and visual filters to explore the report.

## Suggested Improvements

-   Apply a consistent light theme with teal and navy accents.
-   Keep KPI cards aligned and use consistent number formatting.
-   Add clear titles and descriptive labels to every visual.
-   Check month sorting so months appear in calendar order.
-   Validate totals and calculations against the source data.
-   Add a short insight summary to explain important findings.

## Important Notes

-   KPI values shown in the report depend on the current dataset,
    filters, and visual configuration.
-   The `Patient_ID` field is an index created during data preparation;
    it should not be treated as a verified real-world patient
    identifier.
-   The `Risk_Flag` field is a report categorization based on the
    dataset's test-result values. It is for analytical demonstration and
    should not be interpreted as a clinical diagnosis.
-   Keep the `.pbix` file and its source CSV files together or update
    the data-source paths when moving the project to another computer.

## Author

**Parth Patel**

## Project Purpose

This project demonstrates data preparation in Power Query, creation of
summary tables, and dashboard design in Power BI for healthcare data
analysis.
