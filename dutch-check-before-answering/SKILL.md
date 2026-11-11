---
name: dutch-check-before-answering
description: >-
  Use whenever the user writes to you in Dutch (any bot, any chat, even one
  Dutch sentence): first correct their Dutch, then judge how authentic it sounds
  and suggest a more idiomatic Dutch version, log both to the Dutch Coach bot,
  then answer their actual request in Dutch.
---
# Dutch check before answering

Applies to every bot whenever the user's own message is (partly) in Dutch. Not for Dutch text they quote from someone else (a teacher, an email) unless they ask for it to be checked.

## Steps (always in this order, in one reply, at the top)

1. **Correctie**: Give the corrected, natural sentence(s). Under it, list each real error briefly, verbs first (conjugation, tense, word order), then word choice, articles, spelling, capitals and punctuation. Give a short reason per point. Never invent errors; acceptable style alternatives are not errors. If the Dutch is fully correct, say so in one line.
2. **Hoe Nederlands klinkt het?**: Give a one-line verdict: *natuurlijk Nederlands*, *begrijpelijk maar Engels-achtig*, or *letterlijk vertaald uit het Engels*. If it is not natural, give a more authentic Dutch way to say it, preferably with a common Dutch idiom, fixed expression or collocation (e.g. *rekening houden met*, *het lukt me niet*, *daar staat tegenover dat*), and name the expression in one short clause. Keep it to 1 or 2 suggestions.
3. **Log to Dutch Coach** (silently, see below).
4. **Antwoord**: Then handle the user's actual request as you normally would, written in Dutch (clear B2/C1 level, short sentences). If the request belongs to another bot, route it there as usual and reply in Dutch.

## Logging to the Dutch Coach bot (required)

Every correction AND every authenticity suggestion goes to the Dutch Coach bot (id b61a2c19-cb98-4b3e-9cea-4880e9c54f8a), which owns the user's Dutch error register (DutchLearningOS).

Append one JSON line per item to `/workspace/DutchLearningOS/inbox/error-reports.jsonl` with these fields:
- report_id (unique, e.g. `<botname>-<YYYYMMDDHHMMSS>-<n>`)
- timestamp
- source_bot
- source_type: "chat"
- record_type: "error" for a real mistake, or "authenticity" for an "English-like" suggestion
- original
- correction (for authenticity: the more authentic Dutch version)
- category (e.g. VERB-AGR, VERB-TENSE, VERB-PERF, WO-SUB, LEX-CHOICE, EN-INTERFERENCE, PREP-FIXED, IDIOM)
- explanation
- idiom (the expression suggested, if any)
- context (minimal, with no private, patient, financial or account data)

Then verify the line was written. If you cannot write to that file, send the same items to the Dutch Coach bot as a short message (SendToAgent) instead. Never store passwords, patient, financial or account details.

## Rules

- The correction always comes FIRST, before any other content.
- Keep the check short (max ~4 points) so the answer is not buried; give full detail only if the user asks.
- Do not ask the user to repeat sentences or do drills; that only happens in the Dutch Coach's own chat.
- If the user writes in another language, this skill does not apply.
