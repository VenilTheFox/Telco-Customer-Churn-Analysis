[Wersja polska (Polish version)](./README_PL.md)
# Telco-Customer-Churn-Analysis
Comprehensive Customer Churn Analysis using Python for data engineering and Power BI for business storytelling.

---
## Dataset
The dataset used in this project comes from Kaggle:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data

---

## Tech Stack & Architecture
* **Data Engineering & Preprocessing:** Python (Pandas)
* **BI & Visualization Tool:** Power BI Desktop
* **Data Modeling:** Star Schema (1:N Relationships)
* **Analytics & Metrics:** DAX (Data Analysis Expressions)

### Data Model Architecture
To ensure high query performance and scalable architecture, the raw flat-table structure was refactored into a Star Schema:
* **Fact Table:** `Fact_Churn` (Stores numerical measures: Monthly Charges, Total Charges, Tenure, and Churn status)
* **Dimension Tables:** `Dim_Demographics`, `Dim_Services`, `Dim_Contracts`

---

## Key Business Metrics (DAX)
* **Total Customers:** Unique count of client IDs showing the exact size of the active customer base.
* **Churn Rate:** Percentage of customers who left the company relative to the total customer count.
* **Lost Revenue:** Consolidated monetary value of monthly charges from churned customers, formatted in USD ($) with a thousands separator.

---

## Key Insights & Business Recommendations
1. **The 12-Month Critical Window:** The highest drop-out rate occurs during the first year of tenure (0-12 months). Proactive customer service and onboarding campaigns during this period are vital.
2. **Contract Type Impact:** Short-term (Month-to-month) contracts represent the vast majority of churned users. Introducing incentives to transition these users to 1- or 2-year contracts will significantly stabilize revenue.
3. **Payment Methods Risk:** Customers using *Electronic Check* show a disproportionately high churn rate compared to automated methods (*Credit Card* or *Bank Transfer*). Offering minor discounts for enabling auto-pay can improve retention.

---

## How to Run the Project
1. Clone this repository to your local machine.
2. Review the data clean-up and engineering logic inside the Python scripts/notebooks.
3. Open `Telco_Churn_Dashboard.pbix` using **Power BI Desktop** to explore the interactive dashboard.
