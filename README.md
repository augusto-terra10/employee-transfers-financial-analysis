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
```

## Public-sharing checklist
Before making this repository public, verify that IDs, free-text answers, locations, financial values and embedded report assets are synthetic or explicitly approved for public release. Inspect hidden pages, tooltips, filters and metadata. Do not include real employee or company confidential information.

## Technical documentation
See `documentation/data-model.md` and `documentation/measures-catalog.md`. The model includes a many-to-many relationship between `Form` and `FBT Table`, with single-direction filtering from `Form` to `FBT Table`, plus a one-to-many relationship from `Date table` to `Form`. The current recommendation is to retain the single-direction filter unless a tested report requirement calls for reverse filtering. See `documentation/data-model.md` for the rationale and remaining validation items.
