<!-- AUTHOR / LICENSE / ATTRIBUTION: set before distribution -->

# Kit 05 — Curriculum Mapping with an Adversarial Reviewer

Most talk about AI in curriculum starts from the tool: here is what it can do, where can we use it? This kit starts from the standard: here is the thinking students are supposed to learn, so where — if anywhere — does AI belong in learning it?

Subject mappers read your standards and propose AI-integration moments, including "none here" when the thinking should stay unassisted. A separate pedagogy reviewer then tries to break every proposal against a rubric built on what we know about how learning works: whether students feel safe enough to learn, whether the thinking the standard names stays with the student, whether every learner can get in, whether it fits the age, and whether it is safe. Only what survives reaches a curriculum lead, and only what the lead approves becomes a teacher-ready moment.

This is the kit where agents earn their keep. Parallel mappers can cover a grade's worth of standards across subjects; an independent reviewer with a sharp rubric catches what an enthusiastic designer misses.

Three principles run through it:

- **The standard leads; the tool follows.** A moment exists only if it serves the thinking the standard names.
- **"No AI here" is a valid and often correct answer.**
- **The reviewer is adversarial by design.** Its job is to find the problem before a student does.

## What's in the kit

```
core/
  01-guardrails.md
  02-inputs-template.md
  03-variables.md
  04-rubric.md             the pedagogy reviewer's lenses
  05-human-gates.md
  roles/
    mapper.md              proposes moments (or none) for each standard
    pedagogy-reviewer.md   tries to break every proposal
    moment-writer.md       turns approved moments into teacher-ready cards
CLAUDE.md + .claude/       optional Claude Code layer: parallel mappers by subject
example/                   two grade 7 ELA standards, flawed first mapping, review
```

## The sequence

1. **Gate 1:** standards pasted verbatim from the official source; your AI use scale, approved tools, and grade-level progression filled in.
2. **Mapper(s)** propose moments per standard — one mapper per subject.
3. **Pedagogy reviewer**, in a separate session, reviews every proposal against the rubric.
4. **Gate 2:** a curriculum lead and a teacher of that subject approve, revise, or cut.
5. **Moment writer** drafts teacher-ready cards for approved moments.
6. **Gate 3:** pilot with a small group of teachers before scaling.

## What this kit will not decide

What your curriculum should be, which tools to approve, or whether a moment works. Whether it works is something only a classroom pilot can show.

## Two ways to run it

In any tool: run the mapper once per subject in fresh chats, then the reviewer in its own chat. In Claude Code: put one standards file per subject in `input/standards/`, and the orchestrator runs mappers in parallel, then the reviewer across all of them.

Use your district's own AI use scale and progression in the variables. The example uses a generic four-level scale for illustration.
