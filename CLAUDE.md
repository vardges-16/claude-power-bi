# Power BI toolkit: working rules

This repo is a generic, project-agnostic toolkit for Power BI work (semantic models, reports in PBIP/PBIR).
It is not tied to one report. Always inspect the project first (skill: `pbi-discover`).

## Safety rules (always apply)
1. Work on a copy or Git branch of the project, never on the only copy.
2. Propose, then wait. For any change, show the plan (what, where, why, risk) and get explicit approval before editing.
3. Publishing, deploying, or triggering a refresh is a separate step with its own confirmation. Never bundle it into another approval.
4. Never delete tables, columns, measures, pages, or visuals without naming them and getting approval.
5. Keep real data, credentials, and connection strings out of this repo and out of commits.
6. If a tool call fails or returns partial output: stop, report it, and ask. Do not retry automatically.
7. Say "unverified" when something has not been tested against a real project. Do not guess file formats.

## Defaults
- Standards: see `docs/STANDARDS.md` (placeholders until the owner edits them).
- Prefer Microsoft's official Power BI Authoring MCP server for model changes, and PBIR/TMDL file edits for the report layer.
- Cite the file and object (table, measure, page) for every finding.

## Skills
- `pbi-discover`: read-only project inspection. Run first.
- More are planned; see `docs/COVERAGE.md`.
