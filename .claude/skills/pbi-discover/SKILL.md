---
name: pbi-discover
description: Read-only inspection of a Power BI project (PBIP folder) before any change. Use at the start of every Power BI task to report format, sources, Git status, incremental refresh feasibility, and what the toolkit can safely do.
---

# pbi-discover (read-only)

Never modify files in this skill. Output is a capability report.

## Steps
1. Locate the project: look for a `*.pbip` file and sibling folders `*.SemanticModel` and `*.Report`. If only a `.pbix` exists, report that it must be saved as a PBIP project first (File > Save as in Power BI Desktop) and stop.
2. Semantic model format: `definition/` with `.tmdl` files = TMDL (good); `model.bim` = legacy TMSL (report it).
3. Report format: `*.Report/definition/` with `pages/` = PBIR (good); a single `report.json` = legacy format (report it; visual/bookmark edits are riskier).
4. Sources and parameters: read `expressions.tmdl` and table partitions. List each source (type, server/path), which are hard-coded vs parameterized, and any `RangeStart` / `RangeEnd`.
5. Incremental refresh feasibility, per table: size if known, date/datetime column present, source type, and whether query folding is likely. Mark "needs confirmation" when unknown; never assume.
6. Git: is the project in a repo, current branch, uncommitted changes?
7. Theme and branding: is a custom theme JSON referenced?
8. Report counts: pages, visuals, bookmarks.

## Output
A short table: Item | Finding | Evidence (file path) | What this enables / blocks.
End with "Suggested next steps" (max 3) and ask which to run. Mark anything not verified as "unverified".
