# AI Leadership Kits

Five small systems for work school leaders already do: translating policy, reading adoption data, reviewing vendor contracts, synthesizing staff voice, and mapping curriculum. Each one uses AI for what it does well — reading, sorting, drafting at speed — and keeps people in charge of what it cannot do: judging, deciding, and being accountable.

A single prompt asks one model to do everything at once and grade its own work. These kits split the work into roles, give each role a narrow job and hard rules, put a separate reviewer on every output, and stop at the points where a person has to decide. That structure is the difference between a faster draft and a trustworthy one.

| Kit | For | The reviewer catches |
|---|---|---|
| **01 — Policy to Practice** | Turning a board policy into an admin guide and staff one-pager | "may" becoming "must"; interpretation presented as policy text |
| **02 — Reading Your Adoption** | Reading an AI usage export to plan professional learning | Trends from one semester; time saved from counts; small groups that identify people |
| **03 — Vendor Privacy Review** | Mapping a vendor contract against your privacy requirements | Misquoted clauses; deadlines from memory; legal conclusions |
| **04 — Staff Voice Synthesis** | Turning survey or task-force input into themes and a draft framework | Five of sixteen called "most"; dissent dropped; one voice turned into a group |
| **05 — Curriculum Mapping** | Finding where AI belongs, or doesn't, in learning a standard | AI doing the thinking the standard names; students producing harmful media |

## What every kit shares

- **A tool-agnostic core.** Role prompts you paste into your district's approved AI tool, one fresh chat per role.
- **An optional Claude Code layer.** `CLAUDE.md` and `.claude/agents/` run the same roles as isolated subagents and stop at each gate. The subagents read their instructions from the core files, so a change you make in one place changes both.
- **Human gates.** Named decisions that belong to a named person.
- **An independent reviewer.** It sees the source and the output, never the reasoning that produced it.
- **Evidence lanes.** Roles cite only what you provide. Anything else becomes a question for a person to answer.
- **A synthetic worked example** with deliberate errors and the review that catches them. Read it before your first real run.

## Where to start

Pick the kit closest to a task already on your desk, and run it first on something low-stakes you have already done by hand — last spring's survey, a policy you've already explained, a contract you've already signed. Comparing the kit's output to your own is the fastest way to learn where it helps and where you still need to look closely.

Each kit's settings live in `core/03-variables.md`. Change those first; change the role prompts only when you want to change the method.

## License and attribution

Copyright (c) 2026 Sean Beaverson.

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/) (CC BY-NC-SA 4.0). The full legal text is in [LICENSE](LICENSE).

In plain terms, you may copy, adapt, and share these kits for non-commercial purposes as long as you:

- **Give credit.** Name the author, link to this repository, and note any changes you made.
- **Share alike.** Distribute anything you build from these kits under this same license.
- **Do not sell it.** You may not use these kits, or works derived from them, for commercial purposes.

Suggested attribution: "AI Leadership Kits by Sean Beaverson, https://github.com/inquiredu/ai-edu-kits, licensed CC BY-NC-SA 4.0."
