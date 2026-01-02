# Project 03 — Sales Performance Dashboard

## Goal
Create a sales performance dashboard that answers:
- Total Revenue, Profit, Orders, Avg Order Value (AOV)
- Revenue/Profit trends over time (date slicer)
- Performance by Region, Sales Rep, Product Category, and Channel
- Actual vs Target (monthly)

## Data (in /data)
- Sales.csv (Fact): one row per order line
- Customers.csv (Dim)
- Products.csv (Dim)
- Regions.csv (Dim)
- SalesReps.csv (Dim)
- SalesTargets.csv (Fact-like): monthly revenue targets by rep + region

## Suggested Model
- Sales[CustomerID] -> Customers[CustomerID]
- Sales[ProductID] -> Products[ProductID]
- Sales[RegionID] -> Regions[RegionID]
- Sales[RepID] -> SalesReps[RepID]
- Create a Date table and relate Date[Date] -> Sales[OrderDate]
- Optional: relate Date[Month] -> SalesTargets[TargetMonth] (or create a MonthKey)

## Suggested Pages
### Page 1 — Executive Overview
- KPI cards: Revenue, Profit, Orders, AOV
- Line chart: Revenue trend by Date
- Bar: Revenue by Region
- Bar: Revenue by Category
- Slicers: Date, Region, Rep, Category, Channel

### Page 2 — Rep & Target Performance
- Clustered column: Actual Revenue vs Target by Month
- Table: Rep performance (Revenue, Profit, Orders, AOV, Target, % to Target)
- Bar: Top 10 Customers by Revenue

### Page 3 — Product & Channel Drilldowns
- Matrix: Category -> Product (Revenue, Profit, Margin%)
- Bar: Revenue by Channel
- Scatter: Profit vs Revenue by Customer (size = Orders)

## Deliverables to commit
- /pbix/Sales-Performance.pbix
- /images/page-1.png, /images/page-2.png, /images/page-3.png
- README notes + insights

## Key Features
- Executive overview with revenue, profit, orders, and average order value KPIs
- Revenue trend analysis with interactive date and region filters
- Sales performance vs monthly targets by sales representative
- Percent-to-target and variance analysis with conditional formatting
- Product and channel drilldowns to identify revenue and profitability drivers
- Customer-level profitability analysis
