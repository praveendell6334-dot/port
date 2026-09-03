# Company Sales Analysis (Excel Dashboard)

An interactive Microsoft Excel dashboard built with Pivot Tables, Pivot Charts, and Slicers to display sales metrics and key performance indicators at a glance.

## Project Overview

This project turns a raw sales export into a single-screen, interactive dashboard that a sales manager can use without touching a formula. It focuses on the parts of Excel built specifically for this kind of reporting: Pivot Tables for aggregation, Pivot Charts for visualization, and Slicers for fast, click-based filtering.

## Data Preparation

Before any Pivot Table is built, the raw data is prepared as a clean table:

- Converted the raw sales range into a proper Excel **Table** (`Ctrl + T`) so it expands automatically with new data
- Standardised column headers (Order Date, Region, Product Category, Quantity, Unit Price, Discount, Revenue)
- Added a calculated **Revenue** column (`Quantity × Unit Price × (1 − Discount)`)
- Removed blank rows, duplicate order IDs, and corrected inconsistent region/category naming
- Added helper columns for **Month** and **Quarter** to support time-based grouping

## Pivot Table Structure

The dashboard is built on a set of linked Pivot Tables, each summarising the sales table from a different angle:

| Pivot Table | Rows | Columns | Values |
|---|---|---|---|
| Revenue by Region | Region | Quarter | Sum of Revenue |
| Revenue by Category | Product Category | — | Sum of Revenue, Count of Orders |
| Monthly Trend | Month | — | Sum of Revenue |
| Top Products | Product Category | — | Sum of Revenue (sorted descending) |

All Pivot Tables are built from the same source Table, keeping them in sync when new data is added.

## Pivot Chart Selection

Each Pivot Table has a matching Pivot Chart, chosen to fit the type of comparison:

- **Line chart** — Monthly revenue trend, to show growth/decline over time
- **Clustered column chart** — Revenue by region per quarter, to compare regions side by side
- **Bar chart** — Top-performing product categories, ranked for easy reading
- **Doughnut chart** — Revenue share by category, to show proportion of total sales

## Slicer Integration

Slicers were added and connected to multiple Pivot Tables via **Report Connections**, so a single click filters every chart at once:

- **Region slicer** — filter the entire dashboard to one or more regions
- **Product Category slicer** — isolate performance for specific categories
- **Quarter/Month slicer** — narrow the view to a specific time period

This lets a user answer questions like *"How did the South region's electronics sales look in Q3?"* with two clicks and no formulas.

## Key Sales Metrics Derived

The dashboard surfaces the following KPIs, calculated via Pivot Table summaries and supporting formulas:

- Total Revenue (overall and filtered by slicer selection)
- Revenue by Region and by Product Category
- Month-over-month revenue growth %
- Average Order Value
- Top 5 performing product categories by revenue
- Discount rate vs. order volume relationship

## File Structure

```
company-sales-analysis-excel/
├── Company_Sales_Dashboard.xlsx
│   ├── Raw Data (sheet)
│   ├── Pivot Tables (sheet)
│   └── Dashboard (sheet — final interactive view)
└── README.md
```

## How to Use

1. Open `Company_Sales_Dashboard.xlsx` in Microsoft Excel (2016 or later recommended for full Slicer support).
2. Go to the **Dashboard** sheet.
3. Use the Region, Product Category, and Quarter/Month slicers at the top to filter all charts simultaneously.
4. To refresh with new data, paste updated rows into the **Raw Data** table, then right-click any Pivot Table → **Refresh All**.

## Key Takeaways

- Revenue is concentrated in a handful of regions and product categories, visible immediately from the dashboard without manual filtering.
- Slicers make it possible for non-technical stakeholders to self-serve their own views of the data.
- The dashboard updates automatically as new sales data is added to the underlying Table.

## Author

**S. Praveen** — Aspiring Data & Financial Analyst
📧 praveen70342@gmail.com · [GitHub](https://github.com/praveendell6334)
