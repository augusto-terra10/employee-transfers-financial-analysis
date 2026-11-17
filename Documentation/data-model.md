# Data Model

## Relationships confirmed by the report author

The Power BI model has the following relationships:

| From table | To table | Cardinality | Cross-filter direction | Notes |
|---|---|---|---|---|
| `Form` | `FBT Table` | Many-to-many (*:*) | Single: `Form` → `FBT Table` | Both tables contain multiple rows for the matching key. Filters propagate from `Form` to `FBT Table`, not in the reverse direction. |
| `Date table` | `Form` | One-to-many (1:*) | Not confirmed | The Date table is on the one side and filters the Form table on the many side. The exact date column and relationship active status should be checked in Model view. |


## Model entities referenced by report visuals

- `Form`
- `FBT Table`
- `Date table`
- `Measure Table`

## Source tables

| Table | Rows | Columns |
|---|---:|---:|
| Form | 1,414 | 35 |
| FBT Table | 36 | 9 |
