# NYC Yellow Taxi Trips: Exploratory Data Analysis & Statistical Testing

**Course:** CMSC 320 – Introduction to Data Science (Spring 2025)  
**Instructor:** Dr. Fardina Alam  
**Dataset:** NYC Yellow Taxi Trip Records (January 2024)

## Overview
This project presents an end-to-end exploratory data analysis of New York City Yellow Taxi trips using a large, real-world dataset (~3 million records). The goal of the analysis is to understand how taxi usage patterns, trip distances, and fares vary by **time of day** and **day of week**, using statistical testing and data visualization to support conclusions.

The final deliverable is a **public, self-contained tutorial** that walks readers through the full data science pipeline, from data acquisition and preprocessing to hypothesis testing and interpretation.

---

## Research Questions
This project investigates the following questions:

- How does taxi trip volume vary across days and hours?
- Do trip distances differ significantly by day of the week?
- Does the time of day influence average taxi fares?
- Is there a statistically significant difference in fares based on payment type (cash vs. credit)?

---

## Dataset
The analysis uses the **NYC Yellow Taxi Trip Data** for January 2024, published by the NYC Taxi & Limousine Commission (TLC).

- **Initial size:** ~2.96 million trips, 19 features  
- **Key attributes:** pickup/dropoff timestamps, trip distance, fare amount, payment type, location IDs  
- **Data source:** https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

---

## Data Preprocessing
- Loaded parquet-formatted trip data into pandas DataFrames
- Inspected schema, data types, and memory usage
- Identified missing values across several columns
- Dropped rows with missing values (≈4.7% of data), retaining a large, clean dataset
- Filtered trips to January 2024 and derived additional features (weekday, hour)

---

## Exploratory Data Analysis
Exploration focused on identifying temporal and behavioral trends:

- **Trip volume trends**
  - Trips per day and per hour
  - Comparison of weekday vs. weekend patterns
- **Trip distance**
  - Distribution of distances by day of week
  - Identification and filtering of distance outliers using IQR
- **Fare behavior**
  - Average fare by hour of day
  - Fare distributions by payment type

All findings are supported by clearly labeled, publication-quality visualizations.

---

## Statistical Analysis
The project applies multiple statistical methods to test hypotheses:

- **One-way ANOVA** to test whether average trip distance differs by day of week
- **Tukey HSD post-hoc analysis** to identify which weekday pairs differ significantly
- **Two-sample t-test** to evaluate fare differences between cash and credit card payments
- **Correlation analysis** to examine the relationship between trip distance and fare amount

Statistical results are interpreted alongside visual evidence to ensure clarity and rigor.

---

## Key Findings
- Taxi trip volume exhibits strong hourly patterns, with peaks during commuting and evening hours.
- Average trip distance varies significantly by day of the week, confirmed by ANOVA and post-hoc testing.
- Average fares tend to increase during evening hours, suggesting higher demand or longer trips.
- Credit card fares are significantly higher than cash fares, based on two-sample t-test results.

These findings demonstrate how temporal factors influence taxi usage and pricing behavior.

---

## Repository Structure
