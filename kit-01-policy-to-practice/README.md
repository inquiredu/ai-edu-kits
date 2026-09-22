<!-- AUTHOR / LICENSE / ATTRIBUTION: set before distribution -->

# Kit 01 — Policy to Practice

A board adopts a policy, and the real work starts the next morning. Principals have to explain it to staff. Staff have to act on it by Friday. Somewhere between the policy's legal language and a teacher's question, meaning drifts — a "may" becomes a "must," an ambiguity gets quietly resolved one way in one building and another way down the hall.

This kit translates a policy into an administrator guide and a staff one-pager, and keeps every sentence tied to the section it came from. Where the policy is clear, the translation says so. Where it is silent or ambiguous, the translation says that too, and routes the question to the person who owns interpretation, instead of guessing.

Three principles run through it:

- **Precision in language is a trust behavior.** A plain-language version that says more than the policy does erodes trust the first time someone checks.
- **Text, interpretation, and guidance stay visibly separate.** Every statement is tagged: what the policy literally says, what the district interprets it to mean, or what comes from supporting guidance.
- **Peer-to-peer, never pedantic.** Principals are the experts on their buildings. The translation offers clarity as a trade, not a lecture.

## What's in the kit

```
core/
  01-guardrails.md       what the tools may and may not do with policy text
  02-inputs-template.md  how to package the policy and supporting documents
  03-variables.md        the settings you customize
  04-rubric.md           how to judge the output
  05-human-gates.md      the decisions only a person makes
  roles/
    reader.md            extracts what the policy requires, permits, prohibits, and leaves open
    translator.md        writes the admin guide and staff one-pager, every line tagged
    auditor.md           checks the translation against the policy text
CLAUDE.md + .claude/     optional Claude Code layer
example/                 synthetic policy, flawed first translation, audit
```

## The sequence

1. **Gate 1:** assemble the adopted policy text verbatim, plus any guidelines it references.
2. **Reader** produces a clause map: requires / permits / prohibits / silent / ambiguous, each with its section reference.
3. **Gate 2:** the policy owner rules on each ambiguity. Their rulings become the district interpretation.
4. **Translator** writes the admin guide and staff one-pager from the clause map and rulings.
5. **Auditor**, in a fresh session, checks every translated statement against the policy text.
6. **Gate 3:** the policy owner approves before anything is distributed.

## What this kit will not decide

It will not interpret ambiguous policy language on its own authority, give legal advice, or decide whether the policy is good. It shows you exactly where interpretation is required and who has to make it.

## Two ways to run it

Paste the role prompts from `core/roles/` into fresh chats in your approved tool, in order. Or open the folder in Claude Code, put the policy in `input/`, and ask Claude to run the translation; `CLAUDE.md` runs the same roles and stops at each gate.
