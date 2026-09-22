<!-- AUTHOR / LICENSE / ATTRIBUTION: set before distribution -->

# Kit 02 — Reading Your Adoption

Most districts that turned on an AI tool can now export who used it and how much. The export is honest data, and it is easy to misread. A single semester gets described as a trend. Conversation counts get described as time saved. A building with thirteen users gets described as "less engaged." None of those claims is in the data.

This kit reads a usage export the way a careful analyst would: what the data can show, what it can't, where use is concentrated, who tried and stalled — and then designs learning responses aimed at what the data actually supports. The most useful finding is usually not the power users. It's the people who opened the tool once or twice and stopped, because they are telling you something about the conditions, not about themselves.

Three principles run through it:

- **Say only what the data measures.** Counts of conversations are not time saved, quality, or impact. A snapshot is not a trend.
- **Attribute at the level the data supports.** Small groups are reported with their counts, or not reported at all.
- **The numbers are computed, not generated.** Language models are unreliable at arithmetic. Every figure comes from a spreadsheet or code, and the auditor recomputes.

## What's in the kit

```
core/
  01-guardrails.md       privacy, small cells, and the arithmetic rule
  02-inputs-template.md  export format and a summary table with spreadsheet formulas
  03-variables.md
  04-rubric.md
  05-human-gates.md
  roles/
    profiler.md          describes the data and its limits before anyone analyzes it
    analyst.md           concentration, stalls, categories — claims at the right level
    designer.md          learning responses tied to specific findings
    auditor.md           recomputes and checks every claim
CLAUDE.md + .claude/     optional Claude Code layer (can run the arithmetic in code)
example/                 30 synthetic users, flawed first analysis, audit
```

## The sequence

1. **Gate 1:** export, de-identify (hashed or sequential user IDs), and suppress small groups.
2. **Profiler** describes what the fields are, what they can and can't show, and what's missing.
3. **Analyst** reports concentration, stalls, and patterns, using computed figures only.
4. **Gate 2:** does this match what you know from the buildings?
5. **Designer** proposes learning responses tied to specific findings.
6. **Auditor**, in a fresh session, recomputes figures and checks every claim.
7. **Gate 3:** the decision owner chooses what to act on.

## What this kit will not decide

It will not tell you whether usage is "good," rank people or buildings, or identify individuals. It will not claim the tool saved time or improved learning — this data cannot show either.

## Two ways to run it

In any tool: compute the summary table in a spreadsheet using the formulas in `core/02-inputs-template.md`, then paste the role prompts into fresh chats. In Claude Code: the analyst and auditor compute directly from the de-identified export in `input/`, so the arithmetic is reproducible.
