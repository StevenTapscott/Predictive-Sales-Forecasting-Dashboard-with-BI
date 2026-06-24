# Predictive Sales Forecasting Dashboard | Power BI

## Project Overview

This project focuses on building an interactive sales forecasting and business intelligence dashboard using Power BI. The objective was to transform historical sales transaction data into a structured analytical model capable of supporting KPI monitoring, trend analysis, and predictive sales forecasting.

The dashboard was designed to simulate a real-world business reporting environment where stakeholders require both high-level executive summaries and deeper analytical forecasting capabilities to support operational and strategic decision-making.

---

<h2>Dashboard Preview</h2>

<h3>Data Model / Schema</h3>
<img src="images/01_schema.png" width="100%">

<h3>Dashboard 1</h3>
<img src="images/02_dashboard1.png" width="100%">

<h3>Dashboard 2</h3>
<img src="images/03_dashboard2.png" width="100%">

<h3>Executive Summary</h3>
<img src="images/04_summary.png" width="100%">

---

## Business Problem

Sales teams and business managers require visibility not only into historical performance, but also into where revenue trends are heading. Traditional reporting often focuses only on past sales activity without providing predictive insight into future performance.

This project addresses that challenge by combining:

- KPI monitoring
- Time intelligence analysis
- Regional and product performance analysis
- Power BI forecasting capabilities

into a centralized reporting solution.

---

## Objectives

- Build a structured star schema data model
- Create reusable DAX measures for KPI reporting
- Implement time intelligence calculations
- Develop interactive executive dashboards
- Apply Power BI forecasting with confidence intervals
- Deliver multi-page analytical reporting with synced filtering

---

# Dataset

Dataset used:

- Superstore Sales Analysis Dataset (Kaggle)

### Key Fields

| Category | Fields |
|---|---|
| Orders | Order ID, Order Date, Ship Date |
| Customers | Customer ID, Customer Name, Segment |
| Geography | Country, City, State, Region, Postal Code |
| Products | Product ID, Category, Sub-Category, Product Name |
| Metrics | Sales, Quantity, Discount, Profit |

---

# Tools & Technologies

| Tool | Purpose |
|---|---|
| Power BI Desktop | Dashboard development |
| Power Query | Data transformation & modelling |
| DAX | KPI & time intelligence calculations |
| Forecast Analytics | Predictive trend forecasting |

---

# Data Model

A star schema model was implemented to improve performance, maintainability, and analytical flexibility.

## Fact Table

### Sales

Contains transactional sales records and quantitative business metrics.

---

## Dimension Tables

### Customer

- Customer ID
- Customer Name
- Segment

### Product

- Product ID
- Category
- Sub-Category
- Product Name

### Geography

- Postal Code
- Country
- City
- State
- Region

### Date

- Date Key
- Date
- Year
- Quarter
- Month
- Week
- Day

---

# Key DAX Measures

## Core KPIs

```DAX
Total Sales = SUM(Sales[Sales])
```

```DAX
Total Profit = SUM(Sales[Profit])
```

```DAX
Profit Margin % =
DIVIDE([Total Profit], [Total Sales], 0)
```

```DAX
Order Count =
DISTINCTCOUNT(Sales[Order ID])
```

```DAX
Average Order Value =
DIVIDE([Total Sales], [Order Count], 0)
```

---

## Time Intelligence

```DAX
Previous Year Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Date'[Date])
)
```

```DAX
YoY Sales Growth % =
DIVIDE(
    [Total Sales] - [Previous Year Sales],
    [Previous Year Sales],
    0
)
```

---

## Forecast KPIs

```DAX
Sales Target =
[Previous Year Sales] * 1.10
```

```DAX
Sales Target Achievement % =
DIVIDE([Total Sales], [Sales Target], 0)
```

---

# Dashboard Pages

## 1. Executive Overview Dashboard

### Features

- KPI cards
- Historical sales trend visualization
- 6-month forecast projection
- Regional sales analysis
- Product category contribution analysis
- Top-performing products
- Interactive slicers

### KPIs Included

- Total Sales
- Total Profit
- Profit Margin %
- Order Count
- Average Order Value
- YoY Sales Growth %

---

## 2. Forecast Analysis Dashboard

### Features

- Forecast-focused KPI reporting
- Revenue forecast projections
- Regional trend comparisons
- Monthly sales vs prior year analysis
- Sales target gauge visualization
- Category revenue contribution analysis
- Synced slicers across report pages

### KPIs Included

- Latest Year Sales
- Previous Year Sales
- Sales Target
- Sales Target Achievement %

---

# Key Findings

## Overall Performance

- Total sales reached approximately **$2.3M**
- Total profit exceeded **$286K**
- Overall profit margin reached **12.5%**

---

## Forecasting Insights

- Forecast projections indicate continued revenue stability
- Historical trends show long-term positive sales growth
- Forecast confidence intervals suggest moderate variability without major decline risk

---

## Regional Insights

- The West region generated the highest sales performance
- The South region remained the lowest-performing region
- Regional sales trajectories showed differing growth volatility patterns

---

## Product Insights

- Technology generated the highest revenue contribution
- Revenue concentration was driven by a relatively small group of top-performing products
- Product trends revealed opportunities for targeted sales and inventory strategies

---

## Target Performance

- The business achieved approximately **90.9%** of projected sales targets
- Forecast trends suggest targets remain achievable with sustained growth momentum

---

# Skills Demonstrated

- Power BI dashboard development
- Star schema modelling
- Data transformation using Power Query
- DAX calculations
- Time intelligence analysis
- Forecasting & predictive analytics
- KPI reporting
- Interactive dashboard design
- Business storytelling with data
- Multi-page report architecture
- Synced slicer implementation

---

# Project Outcome

This project demonstrates the end-to-end development of an intermediate-level Power BI business intelligence solution capable of supporting:

- Executive KPI reporting
- Predictive forecasting
- Regional performance analysis
- Interactive business decision-making

The final dashboard provides a scalable analytical foundation that could be extended further using:

- Power Apps
- Power Automate
- Azure services
- Machine learning integration

---

# Dashboard Screenshots

Shown in the screenshots folder

# Future Improvements

Potential future enhancements include:

- SQL Server integration
- Incremental refresh
- Row-level security (RLS)
- Power BI Service deployment
- Power Apps integration
- Power Automate workflows
- Azure Machine Learning forecasting
- Scenario modelling with What-If parameters

---




