# Inputs template

Shape your raw input into this format before Gate 1 sign-off. Every role reads it the same way.

```
# Input set

## Context
Group: {{GROUP}}
Question asked: "{{QUESTION}}"
Collection method: {{COLLECTION_METHOD}}
Date collected: {{DATE}}
Total responses: {{N}}
Responses withheld at Gate 1: [count, including 0]
Role attribution: [agreed in advance / merged below {{MIN_GROUP_SIZE}} / not used]

## Responses
R01 | [role or "—"] | [response text, verbatim after de-identification]
R02 | [role or "—"] | [response text]
...

## Evidence pack (optional)
E1 | [citation as you'd write it] | [the passage you vetted] | [vetted by: initials]
...
```

A few notes from real use:

- **Keep responses verbatim.** Fix nothing except identifiers. Typos and fragments are part of the voice.
- **One response per line**, even if a person wrote three paragraphs. If a survey had several questions, run each question as its own input set; combining them hides which question a comment answered.
- **Record what you cut.** If you removed a response entirely (off-topic, identifying beyond repair), note the count: "2 responses withheld at Gate 1." The Synthesizer reports it.
- **Transcripts and notes** work, but mark them: `R07 | notes | "Several people nodded when…"` — a notetaker's summary is already one step from the source, and the Synthesizer will treat it that way.
