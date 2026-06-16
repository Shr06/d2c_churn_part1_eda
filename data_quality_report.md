# Data Quality Report

## Project

Customer Churn Prediction – Data Audit & Exploratory Data Analysis
---

# 1. Dataset Summary

| Dataset              |   Rows |
| -------------------- | -----: |
| Customers            |  2,400 |
| Orders (Raw)         | 10,009 |
| Orders (Clean)       |  9,997 |
| Support Tickets      |  1,921 |
| Web Events Snapshot  |  2,400 |
| Churn Labels         |  2,400 |
| Intervention History |  2,400 |

---

# 2. Duplicate Record Assessment

A duplicate audit identified records in the orders dataset containing the `_DUP` suffix.

### Findings

| Metric                    |  Value |
| ------------------------- | -----: |
| Raw Orders                | 10,009 |
| Clean Orders              |  9,997 |
| Duplicate Records Removed |     12 |

### Action Taken

12 duplicate records were removed to prevent inflated transaction counts and revenue calculations.

---

# 3. Missing Value Assessment

### Findings

| Column       | Missing Count |
| ------------ | ------------: |
| loyalty_tier |         1,386 |
| skin_type    |           401 |
| rating       |            58 |

### Treatment

* Missing `loyalty_tier` values were filled with **"Not Enrolled"**.
* Missing `skin_type` values were retained.
* Missing `rating` values were retained for future feature engineering.

---

# 4. Data Type Validation

Date columns were converted to appropriate datetime formats prior to analysis.

Validated date fields included:

* signup_date
* order_date
* snapshot_date
* support ticket dates

This ensured accurate recency calculations and temporal analysis.

---

# 5. Leakage Assessment

A leakage review was performed before EDA.

### Snapshot Logic

Orders were split into:

| Dataset Portion      | Records |
| -------------------- | ------: |
| Pre-Snapshot Orders  |   8,128 |
| Post-Snapshot Orders |   1,872 |

Only pre-snapshot information was used for feature generation.

### Conclusion

Future information was isolated from the feature window to prevent target leakage.

---

# 6. Join Validation

Customer-level joins were validated across all datasets using `customer_id`.

### Result

* No unmatched customer records were identified.
* Customer coverage remained consistent across datasets.

This confirms referential integrity between source tables.

---

# 7. Business Rule Validation

Numerical fields were checked for invalid values.

### Result

No invalid values were detected.

Key numerical variables satisfied expected business constraints, reducing the risk of downstream analytical errors.

---

# 8. Outlier Analysis

Outliers were evaluated for `gross_amount`.

### Treatment Decision

* Values above the 99th percentile (₹2,343.24) were capped using winsorization.
* Lower values were retained because they represent valid customer purchases.

### Action Taken

Only extreme high-end values were capped to reduce skewness while preserving customer purchasing behaviour.

---

# 9. Data Cleaning Summary

| Issue                | Action                          |
| -------------------- | ------------------------------- |
| Duplicate Orders     | Removed 12 records              |
| Missing Loyalty Tier | Filled with "Not Enrolled"      |
| Missing Skin Type    | Retained                        |
| Missing Ratings      | Retained                        |
| High-End Outliers    | Winsorized at 99th percentile   |
| Leakage Risk         | Controlled using snapshot split |

---

# Conclusion

The datasets were found to be suitable for churn analysis after cleaning.

Key quality improvements included:

* Removal of duplicate transactions
* Treatment of missing loyalty membership
* Outlier capping for monetary variables
* Validation of dataset joins
* Prevention of target leakage through snapshot-based filtering

The cleaned data was subsequently used for exploratory analysis and churn-risk assessment.
