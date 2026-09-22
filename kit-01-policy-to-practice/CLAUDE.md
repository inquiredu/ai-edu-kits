# Policy to Practice — Claude Code orchestration

Coordinates three subagents to translate a board policy, stopping at three human gates. Method lives in `core/`; this file adds sequencing and enforcement only.

## Hard rules
- NEVER modify `input/` or `core/`. Write only to `output/`.
- NEVER pass a gate without the user's explicit go-ahead.
- NEVER use web search or fetch. Referenced documents not in `input/` are reported as not provided.
- NEVER resolve policy ambiguity yourself. Only rulings in `input/rulings.md` may be used.
- The auditor receives file paths to the policy, rulings, and translation only — never reasoning.

## Starting state
- `config.md`: filled copy of `core/03-variables.md` (stop if missing or contains `{{`)
- `input/policy-input-set.md`

## Workflow
**Step 0 — Gate 1.** Ask the user to confirm the policy text is the adopted version, verbatim. Wait.
**Step 1 — Reader** → `output/01-clause-map.md`.
→ STOP for Gate 2. List every ambiguity and silence. Ask the user to record the policy owner's rulings in `input/rulings.md` (ruling / defer / guidance for each). Continue only when they say so.
**Step 2 — Translator** → `output/02-translation.md`.
**Step 3 — Auditor** (file paths only) → `output/03-audit.md`.
→ STOP for Gate 3. Report flags by severity, the coverage table's gaps, and the verdict.

After each step: ✅ [step] — [file] — [one-sentence status].

## Stop conditions
Missing sections → re-run once, then stop. Verdict "Re-translate" → stop; the user decides.

## Hard rules, again
Write only to `output/`. Stop at every gate. No web. No interpretation without a ruling. The auditor sees files, not reasoning.
