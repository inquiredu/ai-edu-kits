# Guardrails

## Tool lane
Usage exports identify staff by email. Before any AI tool sees the data, replace emails with sequential or hashed IDs (U01, U02…) and keep the key offline, with a person. Role and building labels stay only if they pass the small-group rule. In an approved tool with a data agreement, keep the same practice anyway — the analysis never needs names.

**Conversation content never goes into this kit.** It is built for usage metadata (counts, dates, categories). If your export includes prompt text or conversation content, strip it before anything else. That content can contain student information.

## Small-group rule
Any group smaller than `{{MIN_CELL}}` — a role at a building, a department — is merged into a larger group or not reported. "The one counselor at Building B didn't use it" identifies a person.

## The arithmetic rule
Language models are unreliable at counting, summing, and percentages, especially across dozens of rows. So:
- **Any tool:** a person computes the summary table in a spreadsheet, or reviews a table computed by deterministic application code, using the definitions and formulas in `02-inputs-template.md`. The AI roles interpret the table; they do not compute from raw rows. If a role needs a number that isn't in the table, it asks for it.
- **Claude Code:** the analyst and auditor compute with code from the de-identified export and show the code.

## What the data can and can't show

| Can show | Cannot show |
|---|---|
| Who used the tool, how often, over what span | Whether use was good, effective, or appropriate |
| Concentration of use | Time saved |
| Tried-and-stalled patterns | Why someone stalled |
| Self-reported or auto-classified categories, as classified | What the conversations were actually about |
| One period's picture | A trend, unless you have multiple periods |

## Tone
Stalls describe conditions, not people. No "resistant," "laggards," or ranking of staff. Land on what the district can change.
