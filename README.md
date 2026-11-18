# Employee Transfers & Financial Analysis

A Power BI portfolio project exploring employee transfers, travel-related allowances and Fringe Benefits Tax (FBT) exposure through operational and financial reporting.

> **Data notice:** All records in this project are synthetic (mock data) and were created for portfolio demonstration purposes. They do not represent real employees, business transactions, transfer arrangements or financial results.

## Dashboard preview

[Employee Transfers & Financial Analysis dashboard](Screenshots/Employee Tranfer & Financial Analysis.png)

[Employee Transfers & Financial Analysis dashboard_Detailed Report](Screenshots/Employee Tranfer & Financial Analysis_Detailed Report.png)

## Business objective

The report is designed to help finance and business stakeholders explore:

- Employee transfer activity across home depot divisions and locations.
- Total allowances declared in connection with employee transfers.
- Taxable allowances and associated FBT payable.
- Monthly FBT payable trends.
- Financial exposure across temporary transfer locations.
- Individual transfer records and their associated financial details.

## Dashboard contents

1. **Executive overview** – high-level KPIs covering employee transfers, FBT payable, FBT paid over, total allowances declared and taxable allowances.
2. **Transfers by division** – distribution of employee transfers across Home Depot divisions.
3. **Monthly FBT trend** – monthly FBT payable over the reporting period.
4. **Allowances by transfer location** – comparison of allowance expenditure across temporary transfer locations.
5. **Detailed transfer report** – employee-level records, approval dates, trip duration, meal and accommodation allowances, taxable allowances and FBT information.
6. **Interactive filtering** – enables users to explore the data by temporary transfer location, Home Depot division, Home Depot location and approval date.

## Data and model

The accompanying Excel workbook consolidates the synthetic source data and supporting documentation:

`data/Employee_Transfers_Portfolio_Data.xlsx`

The workbook contains the following worksheets:

- `Form` – employee transfer records and related operational information (1,414 rows).
- `FBT Table` – aggregated allowance and FBT information (36 rows).
- `Data Dictionary` – descriptions of the source fields.
- `Data Quality` – summary of basic data quality checks.

The Power BI model includes the following tables:

- `Form` – employee transfer and operational records.
- `FBT Table` – allowance and FBT financial information.
- `Date table` – date dimension used for time-based analysis.
- `Measure Table` – dedicated table for report measures.

The model uses a many-to-many relationship between `Form` and `FBT Table`, with single-direction cross-filtering from `Form` to `FBT Table`. The `Date table` is connected to `Form` through a one-to-many relationship.

See [Data model documentation](documentation/data-model.md) for further details and modelling considerations.

## Example analysis

The report uses Power BI measures to support the analysis of transfer activity, allowances and FBT exposure.

Key reporting metrics include:

- Employee Transfers
- Total Allowances Declared
- Taxable Allowances
- FBT Payable
- FBT Paid Over

## Tools and techniques

- Microsoft Power BI
- DAX
- Power Query
- Data modelling and relationship management
- Many-to-many relationships
- Date dimension and time-based analysis
- Interactive filtering and drill-down analysis
- KPI design and financial reporting
- Excel

## Repository structure

```text
employee-transfers-financial-analysis/
├── README.md
├── report/
│   ├── Employee_Transfers_Financial_Analysis.pbix
│   └── README.md
├── screenshots/
│   └── dashboard-overview.png
├── data/
│   ├── Employee_Transfers_Portfolio_Data.xlsx
│   └── README.md
├── documentation/
│   ├── project-overview.md
│   └── data-model.md  
└── .gitignore
```

## Author

**Augusto Terra**  
Business Intelligence & Data Analytics

- GitHub: [@augusto-terra10](https://github.com/augusto-terra10)
