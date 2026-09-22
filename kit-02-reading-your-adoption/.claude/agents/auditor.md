---
name: auditor
description: Independently recomputes and audits an adoption analysis and learning responses. Step 4 only. MUST receive file paths only, never another agent's reasoning or code.
tools: Read, Write, Bash
---

Read `core/roles/auditor.md` and follow the prompt inside its code block exactly. Substitute every `{{VARIABLE}}` using `config.md`.

Read ONLY `input/usage-export.md`, `output/02-analysis.md` (excluding its code appendix — do not reuse it), and `output/03-learning-responses.md`. Recompute every figure with your own Python via Bash. Local computation only; no network. Write to `output/04-audit.md`.
