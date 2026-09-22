<!-- AUTHOR / LICENSE / ATTRIBUTION: set before distribution -->

# Kit 04 — Staff Voice Synthesis

A task force meets, a survey closes, a listening session ends, and someone is left holding two hundred comments and a deadline. That synthesis is where trust is quietly won or lost. When staff read the summary, they check one thing first: *did you hear what I actually said?*

This kit turns raw staff input into a theme synthesis and a draft framework, then has a separate reviewer check the synthesis against the original words before any leader sees it. The AI does the sorting and the first draft. A person decides what it means and what happens next.

Four principles run through every file:

- **Staff voice is the translation layer, not the evidence base.** Comments tell you what your people need and how they talk about it. Research tells you what works. The kit keeps those lanes separate and never invents a citation.
- **Attribute at the level the source supports.** One voice stays one voice. Five of sixteen is not "most."
- **Silence is unanswered, not agreement.** What nobody said gets named as an open question.
- **Human judgment leads and finishes.** Three gates, each owned by a person.

## What's in the kit

```
README.md                  ← you are here
core/                      ← works in any AI tool (Gemini, Copilot, Claude, others)
  01-guardrails.md         data handling and the approved-tool lane
  02-inputs-template.md    how to shape your raw input
  03-variables.md          the settings you customize, in one place
  04-rubric.md             how to judge the output
  05-human-gates.md        the three decisions only a person makes
  roles/
    preparer.md            flags identifiers, normalizes input
    synthesizer.md         finds themes, counts honestly, keeps dissent
    drafter.md             turns themes into a draft framework
    auditor.md             checks the synthesis against the source
CLAUDE.md + .claude/       ← optional Claude Code layer (orchestration only)
example/                   ← a fully synthetic worked example, flaws included
facilitator/               ← running this live with a group
input/  output/            ← working folders for the Claude Code layer
```

## The sequence

1. **Gate 1 (person):** confirm the tool lane and de-identify. See `core/01-guardrails.md`.
2. **Preparer** flags anything that could still identify someone.
3. **Synthesizer** produces themes with honest counts, single voices, dissent, and silences.
4. **Gate 2 (person):** would respondents recognize themselves?
5. **Drafter** turns the synthesis into a draft framework, marking what needs outside evidence.
6. **Auditor** — in a separate session, with no view of how the drafts were reasoned — checks every claim against the original input.
7. **Gate 3 (person):** the decision owner accepts, revises, and decides what goes back to staff.

Each role runs in its own fresh chat. That separation is the point: an auditor that watched the synthesis being written is grading its own homework.

## Two ways to run it

**Any AI tool.** Fill in `core/03-variables.md`, then paste each role prompt from `core/roles/` into a new chat in your district's approved tool, in order, carrying the previous output forward. No setup beyond copy and paste.

**Claude Code.** Open this folder in Claude Code, put your de-identified input in `input/`, fill in the variables, and ask Claude to run the synthesis. `CLAUDE.md` orchestrates the same four roles as isolated subagents and stops at each human gate. The subagents read their instructions from `core/roles/`, so a change you make there changes both layers. (The `.claude/` folder is hidden on most systems; show hidden files to see it.)

The two layers do the same work. Claude Code adds orchestration and enforced separation, not a different kind of result.

## What this kit will not decide

It will not tell you what your staff *really* meant, whether a concern is valid, which theme matters most, or what the district should do. It will not supply research. It produces a draft, a set of flags, and a list of decisions — and hands them to you.

## Customizing

Everything local lives in `core/03-variables.md`: your group, your question, your approved tool, your values language, your minimum group size for role labels. Change the variables first; edit role prompts only when you want to change the method itself.

The `example/` folder shows a complete run on invented data, including a first-pass synthesis with deliberate errors and the audit that catches them. Read it before your first real run.
