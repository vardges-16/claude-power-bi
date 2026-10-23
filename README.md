# claude-power-bi

A reusable, project-agnostic toolkit that helps Claude work on Power BI projects (semantic models and reports in PBIP/PBIR format).

**Status: batch 1 (scaffold). Nothing here has been tested against a real project yet.**

## What is here
| Path | Purpose |
|---|---|
| `CLAUDE.md` | Safety rules Claude follows in every session |
| `docs/STANDARDS.md` | Naming / DAX defaults (placeholders, edit them) |
| `docs/COVERAGE.md` | What Microsoft's official tooling covers vs what this repo must add |
| `.mcp.json` | Registers Microsoft's local Power BI Authoring MCP server |
| `.claude/skills/pbi-discover/` | Read-only project inspection, run first |

## Requirements
- Windows with Power BI Desktop (for the local MCP server)
- Node.js 18 or later (the server starts through `npx`)
- Projects saved as PBIP, ideally under Git

## Unverified
- The `cmd /c npx` wrapper in `.mcp.json` is the usual Windows form for Claude Code but has not been run here.
- Microsoft's `powerbi-authoring` plugin (skills-for-fabric) may replace parts of this; see `docs/COVERAGE.md`.
