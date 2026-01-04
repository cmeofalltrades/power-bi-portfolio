# Project 04 — Financial Overview Dashboard

## Overview
This project simulates a financial performance and budget management reporting solution designed to support executive and operational decision-making. The dashboard provides visibility into revenue, expenses, net profit, and budget variance across departments and time. 

The goal is to demonstrate real-world Power BI modeling, DAX, and dashboard design skills applied to financial and operational analytics use cases.


---
## Tools & Technologies
- Power BI Desktop
- Power Query
- DAX
- CSV-based relational dataset
- GitHub (documentation & version control)

---

## Data Model
**Tables Used:**
- Financial_Transactions — transaction-level revenue and expense data
- Departments — department and manager information
- Categories — revenue and expense classification
- Budget — monthly departmental budgets
- Date — centralized date table
- Month — month-level table to support budget alignment

**Relationships:**
- Departments (1) → Financial_Transactions (*)
-Categories (1) → Financial_Transactions (*)
- Date (1) → Financial_Transactions (*) via Date
- Month (1) → Date (*) via MonthStart
- Month (1) → Budget (*) via Year-Month key

---

## Dashboard Pages
### Page 1 — Financial Overview

Provides a high-level snapshot of overall financial performance.

**Key Metrics:**
- Total Revenue
- Total Expenses
- Net Profit
- Profit Margin %
**Visuals Include:**
- Revenue vs expenses over time
- Net profit trend
- Revenue by category
- Expenses by category
- Interactive slicers for month, department, and expense category
**Purpose:**
Quickly assess financial health, profitability trends, and primary revenue and expense drivers.

---

### Page 2 — Expense Analysis

Focuses on cost distribution and expense behavior across the organization.

**Key Metrics:**
- Total Expenses
- Average Monthly Expenses
**Visuals Include:**
- Expenses by department
- Expenses by category
- Monthly expense trend
- Expense detail table by department and category
**Purpose:**
Identify cost drivers, monitor expense trends, and support expense control and optimization efforts.

---

### Page 3 — Budget vs Actual

Provides insight into budget performance and financial discipline.

**Key Metrics:**
- Total Budget
- Actual Expenses
- Budget Variance
- Budget Variance %
**Visuals Include:**
- Budget vs actual expenses over time
- Budget variance by department
- Budget variance percentage by department
- Department-level budget vs actual summary table with conditional formatting
**Purpose:**
Evaluate budget adherence, identify departments over or under budget, and support financial planning and accountability.

---

## Key Skills Demonstrated
- Star-schema style data modeling
- Month-level and date-level time intelligence
- DAX measures for financial KPIs and variance analysis
- Budget vs actual modeling
- Conditional formatting for financial performance indicators
- Interactive, slicer-driven dashboards
- Executive-focused financial dashboard design
- GitHub documentation and portfolio presentation

---

## Screenshots
Screenshots of all dashboard pages are included in the /images folder.

---

## Notes
This project uses synthetic data to simulate realistic financial reporting, expense management, and budgeting scenarios. It is intended for portfolio and demonstration purposes only.
