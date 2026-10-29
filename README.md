# Audi Sales Dashboard Project (2023–2024)

## Project overview
This project uses a sample Audi-themed sales dataset to explore sales performance, profit, customer reach, monthly trends, state-level sales, and customer-satisfaction metrics. The source workbook includes a dashboard layout and supporting chart data.

> **Data disclaimer:** The transaction records are synthetic sample data created for learning, spreadsheet practice, and dashboard development. They are **not official Audi sales figures**. Some dashboard/chart figures are approximations or reference-image matching values.

## Project files
- `audi_sales_data.csv` — main transaction-level dataset exported from the workbook's **Source Data** sheet.
- `dashboard_chart_data.csv` — supporting summary values exported from the workbook's **Chart Data** sheet.
- `README.md` — project overview, data dictionary, and suggested analysis steps.

## Dataset snapshot
- **Records:** 1,008 transactions
- **Period:** 1 January 2023 – 28 December 2024
- **Years:** 504 records for 2023 and 504 for 2024
- **Unique customer IDs:** 100
- **Units recorded:** 1,426
- **Total sales in transaction data:** $201,215.21
- **Total profit in transaction data:** $79,967.37
- **Missing values in the exported transaction data:** none

Totals are calculated from `audi_sales_data.csv`; they may not match every dashboard element because some visual KPI/chart values were set to match a reference design.

## Main CSV columns
| Column | Description |
|---|---|
| `Date` | Transaction date in `YYYY-MM-DD` format |
| `Year` | Calendar year |
| `Month` | Abbreviated month name |
| `Month No` | Numeric month (1–12), useful for sorting months |
| `Country` | Country recorded for the transaction |
| `State` | State/region recorded for the transaction |
| `Customer ID` | Sample customer identifier |
| `Product` | Audi model/product category |
| `Sales Channel` | Channel such as Online, Dealer, or Corporate |
| `Sales Rep` | Sample sales representative |
| `Units` | Units recorded in the transaction |
| `Sales ($)` | Sales amount in US dollars |
| `Profit ($)` | Profit amount in US dollars |

## Suggested project questions
1. How did total sales and profit change between 2023 and 2024?
2. Which months had the highest and lowest sales?
3. Which Audi product generated the most sales and profit?
4. Which states and sales channels contributed the most revenue?
5. How do units sold relate to sales and profit?

## How to use
### Excel / Google Sheets
1. Open `audi_sales_data.csv` in Excel or import it into Google Sheets.
2. Check that `Date` is recognized as a date and the sales/profit columns as numbers.
3. Create PivotTables:
   - **Monthly sales:** Rows = `Month No` and `Month`; Columns = `Year`; Values = Sum of `Sales ($)`.
   - **Product performance:** Rows = `Product`; Values = Sum of `Sales ($)`, Sum of `Profit ($)`, Sum of `Units`.
   - **State performance:** Rows = `State`; Values = Sum of `Sales ($)`.
   - **Channel performance:** Rows = `Sales Channel`; Values = Sum of `Sales ($)` and Sum of `Profit ($)`.
4. Add charts and optional slicers for `Year`, `State`, `Product`, and `Sales Channel`.

### Python (optional)
```python
import pandas as pd

df = pd.read_csv("audi_sales_data.csv", parse_dates=["Date"])

sales_by_year = df.groupby("Year", as_index=False)["Sales ($)"].sum()
profit_by_product = (
    df.groupby("Product", as_index=False)["Profit ($)"]
      .sum()
      .sort_values("Profit ($)", ascending=False)
)

print(sales_by_year)
print(profit_by_product)
```

## Data quality notes
- `Month No` is included to keep months in calendar order when sorting or charting.
- Customer IDs and employee names are sample identifiers.
- The chart-helper CSV contains pre-aggregated values for the dashboard and should not be appended to the transaction data; doing so would double-count values.
- Currency columns are numeric values in USD, despite the dashboard's display formatting.

## Possible deliverables / next steps
- A polished dashboard with KPI cards and monthly sales charts.
- A short insights report comparing 2023 and 2024.
- Product, state, and channel PivotTables.
- Data validation and reconciliation between dashboard KPIs and transaction-level totals.

