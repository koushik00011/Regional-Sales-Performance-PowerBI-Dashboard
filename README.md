# 📊 Regional Sales Performance & Target Achievement Dashboard

## Overview

This project presents an end-to-end Business Intelligence solution built using Power BI to analyze regional sales performance, profitability, target achievement, returns, delivery efficiency, and regional manager performance.

The dashboard helps business stakeholders monitor key performance indicators, identify operational risks, and evaluate the effectiveness of regional managers across different product categories.

---

## Business Objectives

- Analyze sales and profit performance across regions and categories.
- Track year-over-year growth trends.
- Compare actual sales against targets.
- Monitor return rates and delivery delays.
- Evaluate regional manager performance.
- Support data-driven business decisions.

---

## Tools & Technologies

- **Power BI**
- **Python**
- **Pandas**
- **Power Query**
- **DAX**
- **Excel/CSV**

---

## Data Preparation

The raw datasets were cleaned and transformed using Python and Pandas before importing into Power BI.

### Data Cleaning Activities

- Removed missing and inconsistent values
- Standardized date formats
- Converted delivery duration into numeric format
- Handled data type mismatches
- Exported cleaned datasets for dashboard development

---

## Data Model

The solution uses the following tables:

| Table | Description |
|---------|-------------|
| Orders | Sales transactions |
| Returns | Returned orders |
| People | Regional manager information |
| Targets | Category-wise yearly sales targets |
| Calendar | Date dimension for time intelligence |

---

## Key KPIs

- Total Sales
- Total Profit
- YoY Sales Growth %
- YoY Profit Growth %
- Target Achievement %
- Return Rate %
- Delay Rate %
- Average Delivery Days

---

# Dashboard 1: Regional Sales Performance

### KPI Summary

- Total Sales
- Total Profit
- YoY Sales Growth %
- YoY Profit Growth %
- Target Achievement %
- Return Rate %
- Delay Rate %
- Average Delivery Days

### Visualizations

### 1. Sales vs Target by Category
Compare actual sales against target values across product categories.

### 2. Sales Growth Trend
Year-over-Year sales trend analysis.

### 3. Profit Growth Trend
Year-over-Year profit trend analysis.

### 4. Regional Sales Performance
Compare sales contribution by region.

### 5. Target Achievement by Category
Evaluate category-wise target performance.

### 6. Delayed Orders Analysis
Monitor operational delivery delays.

---

# Dashboard 2: Regional Manager Performance

### Visualizations

### 1. Sales by Regional Manager
Analyze manager-wise sales contribution.

### 2. Profit by Regional Manager
Compare profitability across managers.

### 3. Manager vs Category Sales Performance
Evaluate manager performance across product categories.

### 4. Target Achievement by Manager
Track manager contribution toward business targets.

### 5. Manager Operational Risk Summary
Monitor:

- Return Rate %
- Delay Rate %
- Average Delivery Days

Conditional formatting highlights high-risk areas for quick decision-making.

---

## DAX Measures Used

```DAX
Total Sales =
SUM(orders_cleaned[sales])

Total Profit =
SUM(orders_cleaned[profit])

Total Orders =
DISTINCTCOUNT(orders_cleaned[order_id])

Previous Year Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(Calendar[Date])
)

YoY Sales Growth % =
DIVIDE(
    [Total Sales] - [Previous Year Sales],
    [Previous Year Sales]
)

Target Achievement % =
DIVIDE(
    [Total Sales],
    [Total Target]
)
```

## Key Business Insights

- Sales exceeded **2.9 Million**.
- Profit crossed **372K**.
- Sales and profit demonstrated strong year-over-year growth.
- Overall target achievement exceeded 100%.
- Regional performance differences were identified.
- Return and delay rates highlighted operational improvement opportunities.
- Manager-level analysis enabled performance comparison and accountability.

---

## Features

- Interactive slicers
  - Year
  - Category
  - Region
  - Ship Mode

- Drill-through navigation between dashboards

- Dynamic KPI cards

- Time Intelligence using Calendar Table

- Conditional formatting for operational risk analysis

---

## Project Structure

```text
├── Regional_Sales_Dashboard.pbix
├── README.md
├── dashboard_page1.png
├── dashboard_page2.png
└── presentation_video_link.txt
```

## Dashboard Preview

### Regional Sales Performance Dashboard

(Add Screenshot Here)

### Regional Manager Performance Dashboard

(Add Screenshot Here)

---

## Author

### Koushik Naidu

Aspiring Data Analyst

Skills:
- Power BI
- Python
- SQL
- Excel
- Data Visualization
- Business Analytics

LinkedIn: (Add Your LinkedIn Profile)

GitHub: (Add Your GitHub Profile)

---
⭐ If you found this project interesting, feel free to star the repository.
