# Running it live

The kit works as a room activity: a group answers a question, the synthesis runs in front of them, and the audit checks the synthesis against their own words. People watch a tool handle what they said with precision — or catch it when it doesn't. That is a more persuasive case for careful AI use than any slide.

Plan for 15–20 minutes. It works with a staff meeting, a leadership team, or a conference room.

## Before

- Choose one question. Open-ended, about something the group has real views on, answerable in two or three sentences. Examples:
  - "What would you need to see before trusting an AI-drafted summary of your staff's feedback?"
  - "What is one thing your staff has asked for about AI that you haven't been able to answer yet?"
  - "Where should AI stay out of your schools' work, and why?"
- Set up collection in an approved, anonymous tool. Ask for no names. If you collect a role field, make sure every role will have at least `{{MIN_GROUP_SIZE}}` people, or skip it.
- Fill in `core/03-variables.md` for the session and open two fresh chats in your approved AI tool: one for the Synthesizer, one for the Auditor. Paste the role prompts in advance.
- Pre-run the `example/` folder so you have finished outputs ready if the live run stalls or the network fails.

## During

1. **Declare the intent (1 min).** Tell the room what will happen: their words will be sorted by a tool, and then a second, separate session will check whether the sort was faithful. Invite them to argue with both — and mean it.
2. **Collect (4 min).** Put up the question. Give quiet time to write.
3. **Gate 1, out loud (1 min).** Scroll the raw responses, check for names or identifying details, and say what you're checking for. The room sees the human step happen.
4. **Synthesize (3 min).** Paste the responses into the Synthesizer chat and run it. While it works, ask the room to predict: what will the biggest theme be? What might get lost?
5. **Gate 2 with the room (3 min).** Read the single voices and dissent sections first. Ask: "Does anyone not see their response reflected?" If someone doesn't, that is the most valuable moment of the session — note it, don't smooth it over.
6. **Audit (3 min).** Paste the input and the synthesis into the separate Auditor chat. (Skip the Drafter live; it adds time without adding to the point.) Read the flags aloud.
7. **Close (2 min).** Ask: "What did the auditor catch that you would have missed? What did you catch that it missed?" Whatever the answer, the lesson is the same — the tool made the first draft faster, and people made it trustworthy.

## If the live run misbehaves

That is useful too, and worth saying so. If the synthesis overclaims, the audit should catch it; if the audit misses something the room caught, that is the case for Gate 2 made by the room itself. Switch to the pre-run example only if the tool fails outright.

## Taking it home

Participants leave with the whole kit. Suggest they start with a low-stakes input set they already have — last spring's survey, a PLC exit ticket — so the first real run is practice, not a decision.
