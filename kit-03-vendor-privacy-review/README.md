<!-- AUTHOR / LICENSE / ATTRIBUTION: set before distribution -->

# Kit 03 — Vendor Privacy Review

Every district signs contracts with technology providers that will hold student data, and most districts do not have a privacy attorney reading each one. The review usually falls to a technology director with a checklist and forty pages of vendor boilerplate.

This kit does the reading part: it finds the clauses that answer each of your requirements, quotes them, and lays out where the contract meets, misses, conflicts with, or is silent on each one. Then it drafts questions for the vendor and for counsel. It ends there on purpose. Whether a contract is acceptable is a judgment for counsel and the authorized signer, not for a tool.

Three principles run through it:

- **Quote, don't characterize.** Every finding points to the exact contract language, so a reviewer can check it in seconds.
- **"Not found" is not "noncompliant."** Silence in a contract is a question, and the kit treats it that way.
- **The kit never reaches a legal conclusion.** It maps. People decide.

## What's in the kit

```
core/
  01-guardrails.md
  02-inputs-template.md
  03-variables.md
  04-rubric.md
  05-human-gates.md
  requirements-starter-mn.md   starter checklist from Minn. Stat. § 13.32 and FERPA (verify before use)
  roles/
    extractor.md               finds and quotes the clauses for each requirement
    analyst.md                 maps each requirement: met / partial / conflicts / not found
    question-writer.md         drafts vendor questions and flags items for counsel
    auditor.md                 verifies every quote and every status
CLAUDE.md + .claude/           optional Claude Code layer
example/                       synthetic vendor DPA, flawed first analysis, audit
```

## The sequence

1. **Gate 1:** confirm your requirements list with whoever owns it (counsel, business office), and assemble the contract documents.
2. **Extractor** quotes the language relevant to each requirement.
3. **Analyst** assigns a status to each requirement, with the quote as evidence.
4. **Question writer** drafts vendor questions and a counsel list.
5. **Auditor**, in a fresh session, verifies every quote exists verbatim and every status is justified.
6. **Gate 2:** counsel and the authorized signer decide.

## What this kit will not decide

Whether the contract complies with law, whether to sign, or what to negotiate. It will not supply legal requirements from memory — only from the requirements file you give it.

## About the Minnesota starter

`core/requirements-starter-mn.md` is built from the text of Minn. Stat. § 13.32, subd. 13 and 14, and the FERPA school-official conditions. It is a starting point for your own list, not legal advice. Verify it against the current statute and with your district's counsel before relying on it, and add your district's own standards.
