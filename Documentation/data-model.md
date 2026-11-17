# Data Model

## Relationships confirmed by the report author

The Power BI model has the following relationships:

| From table | To table | Cardinality | Cross-filter direction | Notes |
|---|---|---|---|---|
| `Form` | `FBT Table` | Many-to-many (*:*) | Single: `Form` → `FBT Table` | Both tables contain multiple rows for the matching key. Filters propagate from `Form` to `FBT Table`, not in the reverse direction. |
| `Date table` | `Form` | One-to-many (1:*) | Not confirmed | The Date table is on the one side and filters the Form table on the many side. The exact date column and relationship active status should be checked in Model view. |

## Recommended filter-direction approach

Keep the `Form` → `FBT Table` relationship single-direction for the current report.

This is the simpler and more controlled configuration, and it avoids introducing reverse filter propagation that may create ambiguous paths or unexpected results. Use **Both** only if a specific report requirement has been identified and tested—for example, if a filter originating in `FBT Table` genuinely needs to filter `Form`.

If that reverse filtering becomes necessary, review the model design before changing the relationship. A shared employee or transfer dimension/bridge may be a better solution than enabling bidirectional filtering directly between two fact-like tables. Any redesign should be based on the actual join columns, row grain and measure behaviour.

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

## Validation notes

Before publishing the PBIX, verify:

1. The exact join column(s) between `Form` and `FBT Table`.
2. That the implemented cross-filter direction remains single (`Form` → `FBT Table`).
3. That the many-to-many relationship does not produce ambiguous filter paths or unexpected totals.
4. Whether a separate employee or transfer bridge/dimension is appropriate for the actual business grain. Do not change the model solely to force a one-to-many relationship without checking the data grain and measures.
5. The exact date column used by the `Date table` relationship.
6. Whether the date relationship is active and how date filters affect report measures.

Cardinality and filter direction above reflect the report author's description of the model. The exact join column(s), date relationship details and measure behaviour still need validation in the PBIX semantic model.
