Data Intelligence Dashboard

Project Overview

The Data Intelligence Dashboard is an Excel-based sales analytics project designed to turn transaction-level data into useful business insights. It includes a raw-data table, formula-driven analysis, visualizations, and an interactive dashboard.

> **Dataset note:** The workbook currently contains generated sample data (250 transactions). Replace it with your real project dataset before presenting or submitting the project.

Objectives

• Summarize sales performance using key performance indicators (KPIs).
• Compare revenue across regions, product categories, and customer segments.
• Track monthly revenue trends.
• Identify high-value customers and best-selling products.
• Explore projected revenue using an editable growth assumption.

Workbook Structure

|Worksheet         |Purpose                                                                                              |
|------------------|-----------------------------------------------------------------------------------------------------|
|**Read Me**       |In-workbook guide and notes about the model.                                                         |
|**Raw Data**      |Transaction-level records used by the analysis.                                                      |
|**Analysis**      |KPI calculations, customer/product summaries, revenue projections, and trend/regression calculations.|
|**Visualizations**|Sales charts, including revenue by region, monthly revenue trend, and revenue by category.           |
|**Dashboard**     |Summary view with KPI cards and Region, Category, and Segment filter cells.                          |

Data Fields

The raw data includes transaction, customer, product, and sales attributes, such as:

• Transaction ID and date
• Customer ID and customer name
• Product ID and product name
• Category and quantity
• Unit price and transaction amount
• Payment method
• Region and customer segment

Check the Raw Data sheet for the complete column list.

Key Features

• KPIs: total revenue, transaction count, units sold, average order value, and unique customers.
• Interactive summary: dashboard filter cells for region, category, and customer segment.
• Revenue projection: an editable revenue-growth assumption and projected revenue formula.
• Trend analysis: monthly revenue trend calculations and slope/intercept formulas.
• Charts: revenue by region, monthly revenue trend, and revenue by category.

How to Use

1. Open the workbook in Microsoft Excel.
2. Review the Raw Data sheet and confirm that the data is complete and correctly formatted.
3. Replace the sample records with the intended project dataset, keeping the column structure consistent.
4. Make sure the transaction table is named Transactions, since the formulas refer to that table name.
5. Allow Excel to calculate formulas when prompted.
6. Open Analysis to review KPIs and the what-if growth assumption.
7. Open Dashboard and select values in the Region, Category, and Segment filter cells to explore the summary.
8. Review Visualizations for the sales charts.
9. Validate totals against the source data before using the results in a report or presentation.

Excel Compatibility

• Some formulas, including FILTER and UNIQUE, require Microsoft 365 or Excel 2021 or later.
• NOW() and TODAY() update when Excel recalculates the workbook.
• For the monthly trend/regression exercise, Excel’s Data Analysis ToolPak may be used if desired.

Important Notes / Limitations

• The current records are sample data, not verified business transactions.
• Dashboard filters and formulas should be tested after replacing the sample data.
• Confirm that dates are stored as actual Excel dates, not text, so date-based analysis works correctly.
• If formulas do not update, check Excel calculation settings and recalculate the workbook.
• The workbook’s existing in-sheet guide should be consulted for additional implementation notes.

Suggested Future Improvements

• Add a data-cleaning and validation step.
• Add date-range filtering and additional KPI cards.
• Include a written findings section with evidence-based business recommendations.
• Add a refresh/checklist section for repeatable project updates.
• Replace sample data with a documented, approved dataset.

Project Deliverables

• Excel workbook: Data_Intelligence_Dashboard.xlsx
• Project documentation: README.md

Author

Add your name, course, institution, and submission date here if required

