# Healthcare-KPI-Dashboards
# Healthcare Encounter Analytics Dashboard

## Project Overview

This project analyzes synthetic healthcare encounter data using **Databricks SQL** and **Databricks Dashboards**.

The goal of the project is to understand patient utilization patterns, encounter types, changes in encounter volume over time, and organization-level activity using healthcare data.

This project uses **synthetic Synthea healthcare data**, so no real patient information or protected health information (PHI) is included.

---

## Objectives

The dashboard was designed to answer business and operational questions such as:

- How many patients are represented in the dataset?
- How many healthcare encounters occurred?
- What types of encounters are most common?
- How have encounter volumes changed over time?
- Which organizations have the highest encounter volume?
- What is the average duration of a healthcare encounter?

---

## Dataset

The project uses synthetic healthcare data generated using **Synthea**.

The dataset includes healthcare-related information such as:

- Patients
- Encounters
- Encounter class
- Encounter start and stop timestamps
- Providers
- Organizations

The encounter dataset was used as the primary source for healthcare utilization analysis.

---

## Tools and Technologies

- Databricks
- Databricks SQL
- Databricks Dashboards
- SQL
- Synthea Synthetic Healthcare Data

---

## Dashboard KPIs and Visualizations

### 1. Total Patients

Measures the number of unique patients represented in the dataset.

```sql
SELECT
    COUNT(DISTINCT Id) AS total_patients
FROM patients;
