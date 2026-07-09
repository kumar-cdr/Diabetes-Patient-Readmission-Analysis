# Diabetes Patient Readmission Analysis

Analysed 100,100 diabetic patient encounters from the UCI 130-US Hospitals
dataset to identify the key risk factors driving 30-day hospital readmissions.

## Dashboard Preview
<img width="784" height="450" alt="SS" src="https://github.com/user-attachments/assets/09383be9-74ec-40b7-937d-eeeeb780feab" />

## Problem Statement

Hospital readmissions within 30 days are a critical quality indicator and
a significant cost burden. This project identifies which patient segments
are at highest risk so hospitals can prioritise early intervention.

## Dataset
- Source: UCI Machine Learning Repository — Diabetes 130-US Hospitals (1999-2008)
- Size: 100,100 patient encounters across 130 US hospitals
- Key columns: age, num_medications, A1Cresult, time_in_hospital, readmitted

## Tools Used
- MySQL 8.0 — data storage, cleaning, and SQL analysis
- Power BI Desktop — interactive dashboard

## Key Findings
1. Patients aged 20-30 had the highest 30-day readmission rate (14.2%) —
   higher than elderly patients, suggesting uncontrolled juvenile-onset diabetes.
2. Patients on 20+ medications were readmitted at 12.7% vs 7.5% for those
   on 1-5 medications — polypharmacy is a strong early warning signal.
3. 83% of patients received no A1C test during their stay. Those who did
   showed 1.4% lower readmission rates — routine testing could reduce risk.

## SQL Techniques Used
- CASE WHEN aggregations (conditional counting)
- GROUP BY with SUM, COUNT, AVG, ROUND
- CTEs (Common Table Expressions) for risk scoring
- Window functions: SUM() OVER() for percentage of total
- HAVING clause to filter aggregated groups
