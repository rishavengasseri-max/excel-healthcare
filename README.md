# Healthcare Analysis Workbook — README

## Overview
This workbook (`healthcare2_0.xlsx`) contains customer, hospitalization, and medical
examination records for **2,335 patients**, along with a pivot table, charts, and a
dashboard summarizing the data.

## Sheets

| Sheet | Rows (data) | Description |
|---|---|---|
| **Customer Names** | 2,335 | Customer ID, Title, First Name, Last Name |
| **Hospitalisation Details** | 2,343 | Customer ID, Date of Birth, Children, Charges, Hospital Tier, City Tier, State ID, Age |
| **Medical Examinations** | 2,335 | Customer ID, BMI, HBA1C, Heart Issues, Any Transplants, Cancer History, Number of Major Surgeries, Smoker, Weight Status, Diabetes Status |
| **Medical_Examinations** | 2,335 | Duplicate of "Medical Examinations" (same columns; note the "Diabetes Status" spelling differs — "Daibetes" vs "Diabetes" — between the two copies) |
| **Healthcare** | 2,335 | Master/combined table joining Customer Names, Hospitalisation Details, and Medical Examinations into one row per customer (17 data columns + blank columns) |
| **Detail1** | 2,337 | Pivot-table drill-through detail ("Details for Count of Customer ID"), same 17 columns as Healthcare |
| **Pivot Table** | — | Summary pivot: "Major Surgeries and Average HbA1C by Transplant History" — breaks out Sum of NumberOfMajorSurgeries and Average HBA1C by transplant history (Yes/No) |
| **Column,Bar Chart** | — | Underlying data for the dashboard's column/bar chart |
| **Dashboard** | — | "Healthcare Analysis Dashboard" — visual summary combining charts, pivot table, and slicers |

## Key Fields
- **Customer ID** — primary key linking all sheets (format: `Id1`, `Id2`, …)
- **Demographics** — Title, First/Last Name, Date of Birth, Age
- **Health indicators** — BMI, HBA1C, Heart Issues, Cancer History, Any Transplants, Smoker status, Weight Status, Diabetes Status, Number of Major Surgeries
- **Hospitalization/cost** — Children, Charges, Hospital Tier, City Tier, State ID

## Known Data Notes
- **Medical Examinations** and **Medical_Examinations** appear to be duplicate sheets; the "Diabetes Status" field is spelled inconsistently ("Daibetes" vs "Diabetes") across the two.
- The **Healthcare** sheet has several trailing blank columns (through column V) with no headers.
- The **Pivot Table** sheet's summary shows: of 1,579 total major surgeries, 1,417 occurred in patients with no transplant history (avg HBA1C 6.67) vs. 162 in patients with a transplant history (avg HBA1C 5.19).

## Suggested Uses
- Cross-reference customer demographics with health risk factors and hospitalization charges
- Use the Pivot Table / Dashboard sheets for a quick visual summary
- De-duplicate the two Medical Examinations sheets and standardize the "Diabetes"/"Daibetes" spelling before further analysis
