# Project 03 — Sales Performance Dashboard

## Overview
This project simulates a sales performance and revenue tracking solution designed to support business and operational decision-making. The dashboard provides visibility into revenue, profitability, sales trends, and target attainment across regions, sales representatives, product categories, and sales channels.

The goal is to demonstrate real-world Power BI modeling, DAX, and dashboard design skills applied to commercial and revenue-focused analytics use cases.

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
- Sales — transaction-level sales data including revenue, profit, order status, and channel
- Customers — customer segmentation and regional assignment
- Products — product catalog with category, pricing, and cost information
- Regions — geographic dimension for regional performance analysis
- SalesReps — sales representative and team assignments
- SalesTargets — monthly revenue targets by sales rep and region
- Date — centralized date table

**Relationships:**
- Customers (1) → Sales (*)
- Products (1) → Sales (*)
- Regions (1) → Sales (*)
- SalesReps (1) → Sales (*)
- Date (1) → Sales (*) via Order Date
- Date (1) → SalesTargets (*) via Year-Month key

---

## Dashboard Pages

### Page 1 — Executive Overview

Provides a high-level snapshot of overall sales performance.

**Key Metrics:**
- Total Completed Revenue
- Total Completed Profit
- Total Completed Orders
- Average Order Value (AOV)
**Visuals Include:**
- Revenue trend over time
- Revenue by region
- Revenue by product category
- Interactive slicers for date, region, sales rep, category, and channel
**Purpose:**
Quickly assess overall sales health, trends, and primary revenue drivers.

---

### Page 2 — Rep & Target Performance

Focuses on sales accountability and target attainment.

**Key Metrics:**
- Actual Revenue
- Revenue Target
- Revenue Variance
- Percent to Target
**Visuals Include:**
- Actual revenue vs monthly target comparison
- Revenue by sales representative
- Percent-to-target analysis with conditional formatting
- Rep-level performance summary table
**Purpose:**
Identify high and low performers, track progress toward goals, and support coaching and performance management.

---

### Page 3 — Product & Channel Analysis

Provides deeper insight into revenue and profitability drivers.

**Visuals Include:**
- Revenue by product category
- Top products by revenue
- Revenue by sales channel
- Customer-level profitability analysis
**Purpose:**
- Understand which products, channels, and customers contribute most to revenue and profit.

---
## Key Skills Demonstrated
- Star-schema style data modeling
- Centralized date table and time-based filtering
- DAX measures for revenue, profit, targets, and performance ratios
- Target vs actual performance analysis
- Interactive, slicer-driven dashboards
- Business-focused dashboard design and storytelling
- GitHub documentation and portfolio presentation

---

## Screenshots
Screenshots of all dashboard pages are included in the `/images` folder.

---

## Notes
This project uses synthetic data to simulate realistic sales, revenue, and performance management scenarios. It is intended for portfolio and demonstration purposes only.
