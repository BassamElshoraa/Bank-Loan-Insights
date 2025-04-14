# Advanced Loan Data Analysis Dashboard

## Overview

Effective loan management requires a deep understanding of borrower behavior, lending trends, and financial metrics. Traditional reporting methods often fail to provide the necessary level of insight, making informed decision-making challenging. 
This project delivers a suite of **interactive Power BI dashboards** designed to **unlock the full potential of loan data**. By leveraging dynamic visualizations and powerful analytical metrics, stakeholders gain a **comprehensive** and **actionable** view of lending operations, borrower demographics, and loan performance.

[**Access the Dashboard here**](https://app.powerbi.com/view?r=eyJrIjoiZWE0YmE5ZWItYWEwYy00ODQ2LTk5MzQtZDdlZDE5NWZlNGEyIiwidCI6IjBkODkwMmEzLTE1OGYtNGM3MC04MTI4LTFlM2JiNGFiMzk3ZCIsImMiOjh9&pageName=d58eb427d81af13a5503)

![Dashboard Image](https://github.com/BassamElshoraa/Bank-Loan-Insights/blob/main/Bank%20Loan%20Insights.png)

---

## Tools & Technologies Used

- **Power BI Desktop**: For designing interactive dashboards and visualizations.
- **DAX (Data Analysis Expressions)**: To create custom KPIs like Month-over-Month (MoM) growth and interest rate trends.
- **Power Query**: For data cleaning, transformation, and preparation.

---

## Dashboards Overview

### 1. **Executive Summary Dashboard**
**Purpose:** Provides an overview of **Key Performance Indicators (KPIs)** to evaluate lending efficiency.

- **Total Loan Applications:** `total_loan_appl = COUNT(financial_loan[id])`
- **Total Funded Amount:** `total_funded_amt = SUM(financial_loan[loan_amount])`
- **Total Amount Received:** `total_received_amt = SUM(financial_loan[total_payment])`
- **Average Debt-to-Income Ratio (DTI):** `avg_DTI = AVERAGE(financial_loan[dti])`
- **Average Interest Rate:** `avg_interest_rate = AVERAGE(financial_loan[int_rate])`
- **Loan Performance Classification:** 
  - **Bad Loans:** `bad_loan_appl`, `bad_loan_funded_amt`, `bad_loan_received_amt`
  - **Good Loans:** `good_loan_appl`, `good_loan_funded_amt`, `good_loan_received_amt`
- **Percentage Analysis:**
  - **Bad Loan Percentage:** `bad_loan_per = [bad_loan_appl] / [total_loan_appl]`
  - **Good Loan Percentage:** `good_loan_per = [good_loan_appl] / [total_loan_appl]`

---

### 2. **Trends & Overview Dashboard**
**Purpose:** Provides interactive visualizations to highlight lending trends, borrower demographics, and loan purposes.

📌 **Monthly Lending Trends (Line Chart)**  
📌 **Regional Lending Analysis (Filled Map)**  
📌 **Loan Term Distribution (Donut Chart)**  
📌 **Employment Length Impact (Bar Chart)**  
📌 **Loan Purpose Breakdown (Bar Chart)**  
📌 **Home Ownership Impact (Tree Map)**  

Includes **Month-to-Date (MTD) Calculations** and **Previous Month (PMTD) Comparisons**:
- `MTD_avg_DTI`, `PMTD_avg_DTI`
- `MTD_funded_amt`, `PMTD_funded_amt`
- `MTD_interest_rate`, `PMTD_Interest_rate`
- `MTD_loan_appl`, `PMTD_loan_appl`
- `MTD_received_amt`, `PMTD_received_amt`

---

### 3. **Detailed Insights Dashboard**
**Purpose:** Provides granular analysis with **Month-over-Month (MoM) Comparisons**:

- `MOM_avg_DTI = ([MTD_avg_DTI] - [PMTD_avg_DTI]) / [PMTD_avg_DTI]`
- `MOM_funded_amt = ([MTD_funded_amt] - [PMTD_funded_amt]) / [PMTD_funded_amt]`
- `MOM_interest_rate = ([MTD_interest_rate] - [PMTD_Interest_rate]) / [PMTD_Interest_rate]`
- `MOM_loan_appl = ([MTD_loan_appl] - [PMTD_loan_appl]) / [PMTD_loan_appl]`
- `MOM_received_amt = ([MTD_received_amt] - [PMTD_received_amt]) / [PMTD_received_amt]`

---

## Sample Metrics

| Metric | Value |
| :----- | :---- |
| **Total Loan Applications** | 38.58K |
| **Total Funded Amount** | $435.76M |
| **Total Amount Received** | $473.07M |
| **Average Interest Rate** | 12.05% |
| **Average Debt-to-Income Ratio (DTI)** | 13.33% |
