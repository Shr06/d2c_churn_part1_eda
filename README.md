# d2c_churn_part1_eda

# Part 1: Data Audit, EDA & Business Understanding

## Project Overview
This repository contains the exploratory data analysis (EDA) and data audit for a D2C 
(Direct-to-Consumer) personal care brand's customer churn prediction project.
The goal is to understand the data, identify data quality issues, explore customer behaviour and generate business hypotheses before building any churn prediction model.
## Dataset
Source: [D2C Churn Dataset]
https://drive.google.com/drive/folders/1PmLapJI1VSDgvl_AxARNKwM1MCd3WFX0?usp=sharing 
| File | Description |
|---|---|
| `customers.csv` | Customer profile and demographics |
| `orders.csv` | Order transaction history |
| `support_tickets.csv` | Customer support interactions |
| `web_events_snapshot.csv` | Web and app activity |
| `churn_labels.csv` | Churn target variable |
| `rfm_modeling_snapshot.csv` | Pre-built RFM and behavioural features |
| `intervention_history.csv` | Campaign and retention history |
---
## How to Run
1. Open `eda_audit.ipynb` in Google Colab or Jupyter Notebook
2. Mount your Google Drive and update `BASE_PATH` to your dataset location
3. Run all cells in order (`Runtime → Run all`)
---
## Key Findings
- **47% overall churn rate** — nearly half the customer base is at risk
- **100% churn for single-order customers** — first repeat purchase is the most critical retention event
- **Recency is the strongest churn predictor** — churned customers last ordered 135 days ago vs 45 days for retained
- **Digital inactivity precedes churn** — 0 sessions = 66.3% churn vs 20.9% for 10+ sessions
- **Category diversity protects against churn** — single-category customers churn at 50.5%
---
## Tasks Completed
- [x] Task 1: Load and inspect all raw datasets
- [x] Task 2: Data quality report
- [x] Task 3: Exploratory data analysis
- [x] Task 4: Six churn-risk hypotheses
- [x] Task 5: Business memo
---
## Dependencies
See `requirements.txt`
