# Staff Voice Synthesis — Claude Code orchestration

This project turns de-identified staff input into a synthesis, a draft framework, an independent audit, and a decision memo. You coordinate four subagents and stop at three human gates. The method lives in `core/`; this file adds sequencing and enforcement only.

## Hard rules — read first, apply throughout

- NEVER modify anything in `input/` or `core/`. Write only to `output/`.
- NEVER proceed past a human gate without the user's explicit go-ahead in chat.
- NEVER use web search or fetch. Nothing in this project leaves the machine through you, and no outside claims come in.
- NEVER supply research or citations. Only items in the evidence pack may be cited.
- If `input/` contains student names or student-specific details, STOP and tell the user before doing anything else.
- The auditor subagent receives only file paths to the input, the synthesis, the draft, and the evidence pack. Do not pass it your reasoning, the other subagents' reasoning, or a summary of what they intended.

## Starting state

- `config.md` in the project root: a filled copy of `core/03-variables.md`. If it is missing or still contains `{{` placeholders, stop and ask the user to complete it.
- `input/input-set.md`: shaped to `core/02-inputs-template.md`, de-identified by a person.
- `input/evidence-pack.md`: optional.

## Workflow

**Step 0 — Gate 1 check.** Ask the user to confirm: "I've de-identified this input and I'm working in the lane described in core/01-guardrails.md." Wait for yes.

**Step 1 — Preparer.** Delegate to the `preparer` subagent. Output: `output/01-preparer-flags.md`.
→ STOP. Show the flag summary. The user resolves flags by editing `input/` themselves. Continue only when they say so. If they edited the input, re-run Step 1 once.

**Step 2 — Synthesizer.** Delegate to the `synthesizer` subagent. Output: `output/02-synthesis.md`.
→ STOP for Gate 2. Point the user to the single-voices and dissent sections first. Ask: "Would respondents recognize themselves?" Continue only on go-ahead. If they request changes, re-run the synthesizer with their notes; do not hand-edit the synthesis yourself.

**Step 3 — Drafter.** Delegate to the `drafter` subagent. Output: `output/03-draft-framework.md`. No gate; proceed.

**Step 4 — Auditor.** Delegate to the `auditor` subagent with file paths only. Output: `output/04-audit.md`.

**Step 5 — Decision memo.** Fill the top half of the memo template in `core/05-human-gates.md` from outputs 02–04. List every audit flag with "resolution: pending owner." Leave the Decisions section blank. Output: `output/05-decision-memo.md`.
→ STOP for Gate 3. Summarize: number of flags by severity, the auditor's verdict, and the open questions. Hand off to the user.

After each step, report in one line: ✅ [step] — [output file] — [one-sentence status].

## Stop conditions

- A subagent's output is missing required sections → re-run that subagent once, then stop and tell the user.
- The auditor's verdict is "Re-run synthesis" → stop; do not re-run automatically. The user decides.
- Any subagent reports it could not follow a hard rule → stop and report.

## Hard rules — again, because they matter most at the end

Write only to `output/`. Stop at every gate. No web access. No outside citations. The auditor sees files, never reasoning. People decide.
