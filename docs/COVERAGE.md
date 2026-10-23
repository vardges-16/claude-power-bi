# Coverage: official tooling vs this repo

Source: Microsoft Learn (Power BI MCP overview, agentic overview) and the skills-for-fabric CHANGELOG. Not yet tested on a real project.

| Need | Official coverage | Gap for this repo |
|---|---|---|
| Model: measures, tables, relationships, best-practice evaluation | Power BI Authoring MCP server (local GA, hosted preview); `semantic-model-authoring` skill | None expected; add our standards |
| Field parameters | `semantic-model-authoring` (0.3.17) | None |
| Source parameters (server, database, path) | Not found | Own skill: `pbi-parameterize-sources` |
| Incremental refresh | Not found for Power BI | Own skill: `pbi-incremental-refresh` (assess, propose, apply on approval) |
| Report pages, visuals, filters, slicers, themes | `powerbi-report-authoring` / `powerbi-report-cli` | Duplication across pages: check, then own skill if missing |
| Bookmarks (create) | `powerbi-report-cli` (0.3.18) | Sorting and grouping: unverified, check |
| Page background image from layout + brand colors | Not mentioned | Own skill + script |

Open decision: install Microsoft's `powerbi-authoring` plugin as the foundation (its install steps for Claude Code are not fully documented), or reference its skills and write only the gaps.
