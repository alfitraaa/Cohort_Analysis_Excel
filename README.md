# Cohort Retention Analysis Using Excel

## Overview
This project performs a cohort retention analysis on a subset of online retail data for customers in Germany and Ireland. The analysis uses Excel to track customer cohorts over time and compare retention behavior between the two countries.

## Business Question
The primary objective of this project is to evaluate customer retention over time and compare the retention behavior of customers in Germany with those in Ireland.

## Dataset Scope
The analysis is based on the following verified dataset characteristics:
- 15,433 transaction rows
- 96 unique customers
- Geographic scope: Germany and Ireland
- Approximately 11 months of observed activity (January 2011 to November 2011)

## Methodology
The cohort retention analysis was conducted entirely within Excel using the following workflow:
- **Identifying First Invoices:** Used the `MINIFS` function to identify the earliest invoice date for each unique customer.
- **Mapping Cohorts:** Used the `VLOOKUP` function to append the first invoice date to the main transaction dataset.
- **Calculating Cohort Age:** Calculated the approximate cohort age for each transaction by taking the date difference between the invoice date and the first invoice date, dividing by 30, and rounding the result. *Note: This is a 30-day approximation rather than an exact calendar-month boundary calculation.*
- **Data Aggregation:** Used PivotTables to aggregate unique customers grouped by their initial cohort month and subsequent cohort age.
- **Retention Calculation:** Calculated retention rates by comparing the remaining active customers in a given cohort age against the original cohort size.
- **Visualization:** Applied conditional formatting color scales to produce cohort retention heatmaps and used line charts to compare retention trends over time.

## Key Findings
Based on the observed dataset and timeframe:
- **Ireland:** Customers from Ireland showed higher and more stable retention across the observed period.
- **Germany:** Customers from Germany exhibited a steeper retention decline compared to Ireland.

## Skills Demonstrated
- Cohort Analysis
- Customer Retention Analysis
- Excel Formulas (`MINIFS`, `VLOOKUP`, rounding/date math)
- Data Aggregation (PivotTables)
- Data Visualization (Line Charts, Conditional Formatting)
- Business Interpretation

## Limitations
- **Small Population:** The analysis is based on a small sample size of 96 unique customers.
- **Limited Scope:** The geographic scope is strictly limited to Germany and Ireland.
- **Age Approximation:** The cohort age is approximated using 30-day periods rather than exact calendar months.
- **Dataset Provenance:** The original source URL for the dataset and the specific sampling context (e.g., whether this is a random sample or a specific subset) cannot currently be verified.

## Repository Files
- `online_retail_II_germany_and_ireland_cohort_analysis.xlsx`: The main Excel workbook containing the raw data, intermediate calculations, PivotTables, and final cohort matrices.
- `Cohort Analysis Using Excel Pacmann.pdf`: A presentation summarizing the business background, methodology, step-by-step Excel execution, and insights.
- `README.md`: This project summary.

## How to Review the Project
- Read this `README.md` for a high-level overview and summary of the methodology and findings.
- Open the PDF (`Cohort Analysis Using Excel Pacmann.pdf`) for a presentation-style walkthrough of the project.
- Inspect the Excel workbook (`online_retail_II_germany_and_ireland_cohort_analysis.xlsx`) to review the formulas, data transformations, PivotTables, and cohort retention tables directly.
