# Curriculum Mapping — Claude Code orchestration

Runs one mapper per subject in parallel, then an independent pedagogy reviewer across all proposals, then stops for the curriculum lead. Method lives in `core/`.

## Hard rules
- NEVER modify `input/` or `core/`. Write only to `output/`.
- NEVER pass a gate without the user's explicit go-ahead.
- NEVER use web search or fetch. Standards come only from `input/standards/`.
- The reviewer receives file paths to standards, context, and proposals — never mapper reasoning.
- No subagent may recommend a tool outside the approved list in `input/context.md`.

## Starting state
- `config.md` (filled `core/03-variables.md`; stop if missing or contains `{{`)
- `input/context.md` (scale, approved tools, progression, optional evidence pack)
- `input/standards/<subject>.md`, one per subject

## Workflow
**Step 0 — Gate 1.** Confirm standards are verbatim from the official source and tool age terms have been checked. Wait.
**Step 1 — Mappers, in parallel.** Launch one `mapper` subagent per file in `input/standards/`, each told its subject. Outputs: `output/01-map-<subject>.md`.
**Step 2 — Pedagogy reviewer.** One `pedagogy-reviewer` subagent reviews all mapper outputs → `output/02-review.md`.
→ STOP for Gate 2. Summarize PASS / FIX / CUT counts per subject and the cross-set patterns. Ask the user to record decisions in `input/approvals.md` (approve / revise with notes / cut, per moment).
**Step 3 — Moment writer** → `output/03-cards-<subject>.md`, approved moments only.
→ STOP for Gate 3. Remind the user to pilot before scaling.

After each step: ✅ [step] — [file(s)] — [one-sentence status].

## Stop conditions
A mapper output is missing required fields → re-run that mapper once, then stop. Reviewer CUTs more than half of a subject's moments → stop and flag before Gate 2.

## Hard rules, again
Write only to `output/`. No web. Approved tools only. The reviewer sees files, not reasoning. People approve; classrooms decide.
