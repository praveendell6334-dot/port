# Company Sales Analysis (Python)

Sales performance analytics built in Python — cleaning raw transactional data, analysing regional revenue trends, and evaluating product-category performance to support business decisions.

## Project Overview

This project analyses a company's historical sales records to answer questions a sales or finance team actually asks: *Which regions are growing? Which product categories are underperforming? Where is revenue concentrated?* The focus is on turning a raw, inconsistent sales export into a clean dataset and a set of clear, decision-ready visualizations.

## Data Cleaning

Raw sales data is rarely analysis-ready. This project handles:

- Removing duplicate and cancelled/void transactions
- Standardising inconsistent region and product-category labels
- Converting date fields to proper datetime format for time-based analysis
- Handling missing values in quantity, unit price, and discount fields
- Deriving calculated fields: `revenue = quantity × unit_price × (1 − discount)`

## Exploratory Data Analysis

The EDA phase profiles the cleaned dataset before deeper analysis:

- Summary statistics for revenue, order volume, and average order value
- Distribution checks for outlier orders (unusually large or small transactions)
- Correlation checks between discount levels and order volume
- Monthly and quarterly aggregation to prepare for trend analysis

## Regional Sales Trends

- Revenue is broken down by region and plotted over time to identify **growth, decline, and seasonal patterns**.
- Regions are ranked by total revenue contribution and by revenue growth rate, distinguishing large-but-flat markets from smaller-but-fast-growing ones.
- Month-over-month and year-over-year comparisons highlight seasonal peaks (e.g. festive or quarter-end spikes).

## Product Performance

- Revenue and order volume are aggregated by product category to identify top and bottom performers.
- A category-level contribution analysis shows which categories drive the majority of revenue (Pareto-style 80/20 view).
- Discount impact is analysed per category to check whether heavy discounting is actually driving volume or eroding margin.

## Revenue Growth Visualizations

Charts produced in this project include:

- Monthly revenue trend line (overall and by region)
- Regional revenue comparison bar chart
- Product category contribution breakdown
- Discount-vs-volume scatter plot

## Tools & Libraries

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis language |
| Pandas | Data cleaning and aggregation |
| NumPy | Numerical calculations |
| Matplotlib | Trend and comparison visualizations |
| Jupyter Notebook | Interactive analysis workflow |

## Project Structure

```
company-sales-analysis-python/
├── data/
│   └── sales_raw.csv
├── notebooks/
│   └── sales_analysis.ipynb
├── outputs/
│   └── charts/
├── requirements.txt
└── README.md
```

## Code Execution Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/praveendell6334/company-sales-analysis-python.git
   cd company-sales-analysis-python
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook**
   ```bash
   jupyter notebook notebooks/sales_analysis.ipynb
   ```
   Execute cells top to bottom — the notebook loads raw data, applies cleaning, then generates every regional and product-level chart.

4. **Review outputs**
   All generated charts are saved to `outputs/charts/`.

## Key Takeaways

- A small set of regions and product categories account for the majority of revenue.
- Some high-discount categories show limited volume benefit, suggesting room to tighten discount policy.
- Clear seasonal peaks exist and can inform inventory and staffing decisions ahead of time.

## Author

**S. Praveen** — Aspiring Data & Financial Analyst
📧 praveen70342@gmail.com · [GitHub](https://github.com/praveendell6334)
