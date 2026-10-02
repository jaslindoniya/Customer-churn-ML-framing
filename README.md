# Customer Churn - ML Framing & Baseline

## Project Overview
This project frames customer churn as a supervised ML problem and establishes a non-ML baseline before building any ML model.

**Business Decision:** Should we give a retention offer (discount/support) to prevent churn?
**Prediction Task:** Will customer churn in next 30 days? (1 = Yes, 0 = No)
**Unit of Analysis:** One row = One customer
**Action:** Predict daily at 9 AM, retention team calls within 2 days.

## Dataset
- **Source:** CRM + Billing + Support (Jan 2024 - June 2025)
- **Sample:** 12 rows (Original 7000 rows)
- **Features:** `tenure_months`, `support_tickets`, `monthly_spend_inr`, `last_login_days`, `plan_type`
- **Target:** `churned`
- **Note:** `customer_id` is dropped to avoid data leakage. Missing values = 0%.

## Key Findings (from Notebook)

**EDA:**
- Retain (0): 7 customers, Avg Tenure 17.8 months
- Churn (1): 5 customers, Avg Tenure 4.2 months
- Basic plan shows 100% churn in this small sample (bias risk)

**Non-ML Baseline Rule:**# Customer-churn-ML-framing
