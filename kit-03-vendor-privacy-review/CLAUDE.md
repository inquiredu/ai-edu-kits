# Vendor Privacy Review — Claude Code orchestration

Coordinates four subagents to map contract language against a requirements file, then stops for counsel. Method lives in `core/`.

## Hard rules
- NEVER modify `input/` or `core/`. Write only to `output/`.
- NEVER pass a gate without the user's explicit go-ahead.
- NEVER use web search or fetch. Requirements come only from `input/requirements.md`. If the user asks you to check the current statute, tell them to verify it at the Revisor's site and update the file themselves.
- NEVER state that a vendor is compliant or in violation, or recommend signing.
- The auditor receives file paths to requirements, documents, and outputs — never reasoning.

## Starting state
- `config.md` (filled `core/03-variables.md`; stop if missing or contains `{{`)
- `input/requirements.md` (adapted from `core/requirements-starter-mn.md` or your own)
- `input/documents.md` (all contract documents, verbatim)

## Workflow
**Step 0 — Gate 1.** Confirm with the user: requirements approved by the owner, all incorporated documents included, confidentiality terms checked. Wait.
**Step 1 — Extractor** → `output/01-extraction.md`.
**Step 2 — Analyst** → `output/02-gap-map.md`.
**Step 3 — Question writer** → `output/03-questions.md`.
**Step 4 — Auditor** (file paths only) → `output/04-audit.md`.
→ STOP for Gate 2. Report flags by severity and the verdict. Remind the user the output is working material for counsel and the signer.

After each step: ✅ [step] — [file] — [one-sentence status].

## Hard rules, again
Write only to `output/`. No web. No legal conclusions. Requirements only from the file. The auditor sees files, not reasoning.
