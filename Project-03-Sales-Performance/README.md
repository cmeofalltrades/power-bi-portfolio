Project 03 — Sales Performance Dashboard
Overview

This project is a Sales Performance Dashboard built in Power BI to analyze revenue, profitability, and target attainment across regions, sales representatives, products, and channels. The dashboard is designed to mirror real-world sales reporting used by leadership and operations teams to track performance and identify opportunities for improvement.

All data used in this project is synthetic and created for demonstration purposes.

Objectives

The dashboard is designed to answer the following business questions:

How much revenue and profit are we generating?

How is sales performance trending over time?

Which regions and product categories drive the most revenue?

How are sales representatives performing against monthly targets?

Which products, channels, and customers are most profitable?

Data Sources

All datasets are located in the /data directory.

Sales.csv (Fact table)
Transaction-level sales data including revenue, profit, order status, and channel.

Customers.csv (Dimension)
Customer details including segment and region.

Products.csv (Dimension)
Product catalog with categories, pricing, and cost information.

Regions.csv (Dimension)
Geographic hierarchy used for regional analysis.

SalesReps.csv (Dimension)
Sales representative details including team assignments.

SalesTargets.csv (Targets table)
Monthly revenue targets by sales representative and region.

Data Model

The dashboard uses a star-schema style model with the Sales table as the central fact table.

Key relationships:

Sales[CustomerID] → Customers[CustomerID]

Sales[ProductID] → Products[ProductID]

Sales[RegionID] → Regions[RegionID]

Sales[RepID] → SalesReps[RepID]

A dedicated Date table related to Sales[OrderDate]

Monthly target alignment using a Year-Month key between the Date table and SalesTargets

Dashboard Pages
Page 1 — Executive Overview

Provides a high-level snapshot of sales performance.

KPI cards for Revenue, Profit, Orders, and Average Order Value (AOV)

Revenue trend over time with date filtering

Revenue by region

Revenue by product category

Interactive slicers for date, region, sales rep, category, and channel

Page 2 — Rep & Target Performance

Focuses on accountability and target tracking.

Actual revenue vs monthly targets

Percent-to-target and revenue variance analysis

Sales performance by representative

Conditional formatting to highlight underperformance

Summary table for rep-level comparison

Page 3 — Product & Channel Analysis

Supports deeper performance exploration.

Revenue by product category and top products

Revenue by sales channel

Customer-level profitability analysis

Identification of high-impact products and channels

Key Features

Executive-friendly KPI design with consistent business logic

Time-based trend analysis using a centralized Date table

Target vs actual performance modeling with correct filter granularity

Conditional formatting to surface performance gaps

Product, channel, and customer drilldowns for deeper insights

Clean, realistic dataset structure aligned with enterprise reporting patterns

Deliverables

Power BI report file:
/pbix/Sales-Performance.pbix

Dashboard screenshots:
/images/page-1-executive-overview.png
/images/page-2-rep-target-performance.png
/images/page-3-product-channel-analysis.png

Notes

This project was built as part of a broader Power BI portfolio to demonstrate practical data modeling, DAX, and dashboard design skills using realistic business scenarios.
