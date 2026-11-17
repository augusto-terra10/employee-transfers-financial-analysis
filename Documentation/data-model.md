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

The two Excel source tables share 34 distinct Employee IDs. This overlap does not, by itself, establish the correct relationship grain. The exact matching column(s) should be recorded from Model view.

6. Whether the date relationship is active and how date filters affect report measures.

Cardinality and filter direction above reflect the report author's description of the model. The exact join column(s), date relationship details and measure behaviour still need validation in the PBIX semantic model.
