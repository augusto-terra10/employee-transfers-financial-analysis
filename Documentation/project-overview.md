# Project Overview

## Objective
Build a two-page Power BI report for employee transfer activity, allowance expenditure and FBT analysis.

## Executive overview
- Employee Transfers
- FBT Payable
- FBT Paid Over
- Total Allowances Declared
- Taxable Allowances
- Employee transfers by Home Depot Division
- Monthly FBT payable trend
- Allowances by Temporary Transfer Location

## Detailed report
Filters: Home Depot Division, Home Depot Location, Transfer Location and Approval Date. The table includes employee and approval details, trip duration, allowance components and FBT-related fields.

## Source data
- Form: 1,414 rows × 35 columns
- FBT Table: 36 rows × 9 columns
- 34 distinct Employee IDs overlap between the two sources.

## Design
Navy, blue and gold accents on a light grey canvas, with a summary page and a record-level investigation page.


## Confirmed relationship structure

- `Form` ↔ `FBT Table`: many-to-many (*:*).
- `Date table` → `Form`: one-to-many (1:*).

See `data-model.md` for validation notes. The exact join columns and cross-filter direction should be documented from Model view.
