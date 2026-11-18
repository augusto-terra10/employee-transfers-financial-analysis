# Employee Transfers & Financial Analysis

A two-page Power BI portfolio project analysing employee transfer activity, allowances and Fringe Benefits Tax (FBT).

## Report pages
1. **Employee Transfer & Financial Analysis** – executive overview with employee transfer count by Home Depot Division, monthly FBT payable, allowances by temporary transfer location and headline KPIs.
2. **Extended Detailed Report** – filters for Home Depot Division, Home Depot Location, Transfer Location and Approval Date, plus a transfer-level detail table.

## Data
`data/Employee_Transfers_Portfolio_Data.xlsx` consolidates the two supplied dummy-data sources:
- `Form`: 1,414 rows, 35 columns
- `FBT Table`: 36 rows, 9 columns
- `Data Dictionary` and `Data Quality` worksheets

The sources share 34 distinct Employee IDs. This overlap does not by itself establish the correct relationship or data grain.

**Data Disclaimer:** All data contained in this dataset is entirely synthetic (mock data) and has been created solely for demonstration, testing, and analytical purposes. It does not represent real employees, employee records, or actual business transactions. No real personal or organisational information is included.

## Tools
- Microsoft Power BI
- Microsoft Excel
- DAX (document exact expressions from the PBIX before describing formulas)

## Repository structure
```text
employee-transfers-financial-analysis/
├── README.md
├── report/
├── data/
├── screenshots/
└── documentation/

