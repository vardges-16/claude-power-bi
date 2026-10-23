# Standards (PLACEHOLDERS: edit to match your own conventions)

Status: defaults only. The owner has no conventions yet. Nothing here is enforced until confirmed.

## Naming (proposed defaults)
- Tables: singular business nouns, `Title Case` (e.g. `Customer`, `Sales`). Dimensions and facts are not prefixed.
- Columns: `Title Case` with spaces; no technical prefixes in the model.
- Measures: `Title Case`, no table prefix, stored in a dedicated `_Measures` table.
- Parameters: `p` + purpose (e.g. `pServerName`, `pDatabaseName`), plus `RangeStart` / `RangeEnd` for incremental refresh.
- Hide keys and technical columns from report view.

## DAX style (proposed defaults)
- Use variables (`VAR`/`RETURN`); one logical step per line.
- Fully qualify columns (`Table[Column]`); never qualify measures with a table name.
- Use `DIVIDE` instead of `/`.
- Add a description to every measure.

## Model hygiene (proposed defaults)
- Star schema where practical; no bidirectional relationships unless justified.
- Set data types and summarization explicitly; mark one date table.

## Branding
- No brand guide yet. Add colors / theme JSON path here when available.
