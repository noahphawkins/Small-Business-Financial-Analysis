# Small Business Financial Analysis

A portfolio project using **Python, Pandas, Matplotlib, Power BI, and DAX** to clean operational data, analyze monthly profitability, investigate expense patterns, and develop recommendations.

The dataset contains **2,150 fictional transactions** for a janitorial-supplies distributor from January 2024 through December 2025. It is training data, not a complete accounting ledger.

## Business Questions

- How do revenue, gross profit, and operating profit change over time?
- Are gross and operating margins improving?
- Which categories contribute most to operating expenses?
- Which data quality issues affect the reliability of the findings?

## Process

1. Inspected missing values, transaction labels, date formats, and currency fields.
2. Standardized transaction types and removed 35 exact duplicate rows.
3. Identified two invalid transaction dates and excluded those records from monthly analysis.
4. Converted currency text into numeric amounts.
5. Validated supplied net sales against gross sales minus discounts and repaired one missing net sales value.
6. Aggregated 2,113 dated transactions into 24 monthly summaries and reconciled totals.
7. Created a Power BI report with financial measures, monthly trends, year filtering, expense categories, and recommendations.

## Key Findings

- Monthly gross margins remained approximately **45–49%**.
- Operating profit was negative in **17 of 24 months**.
- Operating margin improved from approximately **−29.91% in 2024 to −24.54% in 2025**.
- Annual operating losses narrowed by approximately **$4.85K**, as reductions in COGS and operating expenses outweighed lower revenue.
- Rent, payroll, and insurance accounted for approximately **85% of recorded operating expenses** across the full period.
- Rent alone represented approximately **50% of recorded operating expenses**.
- Ten months had no recorded rent expense. February 2024 had three rent entries; October and December 2025 each had two.

## Recommendations and Limitations

Reconcile rent entries against invoices and lease agreements before drawing firm conclusions about monthly profitability. Missing records and multiple entries may affect both expense totals and comparisons.

Prioritize rent, payroll, and insurance for a cost review. Evaluate lease options, insurance quotes with comparable coverage, and staffing efficiency against implementation costs and operational needs. This analysis does not establish achievable savings.

The results reflect available records. Interest, taxes, and non-operating items were not analyzed, so the report presents **operating profit rather than net profit**. Inventory and AR/AP analysis are outside the scope of this version.

## Dashboard

![Financial reporting dashboard](Project%201%20Reporting.png)

![Findings and recommendations](Project%201%20finding%20and%20recs.png)

## Files

| File | Purpose |
|---|---|
| `Analytics Project.ipynb` | Cleaning, validation, analysis, and exports |
| `messy_small_business_financial_operations.csv` | Original fictional dataset |
| `monthly_financial_summary.csv` | Monthly financial totals and margins |
| `monthly_financial_summary_opex.csv` | Individual operating-expense records with categories and dates |
| `Financial Analysis Project.pbix` | Power BI report |

## How to Run

1. Download or clone the repository.
2. Install Python with Pandas, Matplotlib, and Jupyter. Mixed-format date parsing requires Pandas 2.0 or later.
3. Keep the notebook and original CSV in the same folder.
4. Open the notebook in VS Code or Jupyter and run its cells from top to bottom. Running it regenerates the exported CSVs.
5. Open the `.pbix` file in Power BI Desktop. Update the CSV source paths to your downloaded files before refreshing.

Power BI margin measures divide total profit by total revenue, ensuring correct results across selected months rather than averaging monthly percentages.
