# Reading Your Adoption — Claude Code orchestration

Coordinates four subagents to read a de-identified usage export. In this layer the analyst and auditor compute figures with code, so the arithmetic is reproducible. Method lives in `core/`.

## Hard rules
- NEVER modify `input/` or `core/`. Write only to `output/`.
- NEVER pass a gate without the user's explicit go-ahead.
- NEVER use web search, fetch, or any network command. Bash is for local computation only.
- If `input/` contains emails, names, or conversation text, STOP before any step and tell the user.
- The auditor receives file paths only and computes independently. Never pass it the analyst's code or reasoning.

## Starting state
- `config.md` (filled `core/03-variables.md`; stop if missing or contains `{{`)
- `input/usage-export.md` (de-identified, format in `core/02-inputs-template.md`)

## Workflow
**Step 0 — Gate 1.** Confirm with the user: IDs replaced, content removed, small groups merged. Wait.
**Step 1 — Profiler** → `output/01-profile.md`.
**Step 2 — Analyst** → `output/02-analysis.md` (computes with Python via Bash; includes code in an appendix).
→ STOP for Gate 2. Ask whether the patterns match what the user knows from the buildings.
**Step 3 — Designer** → `output/03-learning-responses.md`.
**Step 4 — Auditor** (file paths to export, analysis, responses) → `output/04-audit.md`, with its own recomputation.
→ STOP for Gate 3.

After each step: ✅ [step] — [file] — [one-sentence status].

## Stop conditions
Figures disagree between analyst and auditor → stop and show both. Verdict "Re-run analysis" → stop.

## Hard rules, again
Write only to `output/`. Local computation only, no network. Stop at every gate. The auditor computes independently.
