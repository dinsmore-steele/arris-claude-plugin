---
name: peo-alignment-score
description: "Use when someone wants to take the PEO Alignment Score, asks whether a PEO is a good fit for their company, or wants to know how well their current PEO fits."
---

# Take the PEO Alignment Score

The PEO Alignment Score (PAS) is Dinsmore Steele's free assessment: 12 multiple-choice questions, about four minutes, a score from 0 to 100 with what it means, and a full PDF report by email. Use plain words and never mention tool names to the person.

## Steps

1. Call `pas_get_questions` with no track. It returns the opening choice. Ask the person which describes them: they use a PEO today (track A), or they are deciding whether to use one (track B).
2. Call `pas_get_questions` with that track.
3. Ask the questions **one at a time**, each with its options numbered. For a pick-many question, say they can choose more than one. Never choose an answer for the person, and don't skip ahead.
4. Ask for their name, work email and company. Phone is optional.
5. Call `pas_submit` without `confirmed` to preview. Read the email address back and ask them to confirm it. Only after they say yes, call `pas_submit` again with `confirmed: true`. This emails the report and records the result with Dinsmore Steele, so never send it on a guess.
6. Share the score, its band and what it means in two or three sentences. Mention that the full report is on its way by email.
7. Offer to help them start gathering what PEOs need for a quote. No sign-in is needed for the assessment, but a case needs an Arris account. If they want one and don't have a login, call `request_arris_account` with the email they gave, read the address back, then call it again with `confirmed: true`. Tell them to open the email, set a password, and come back; Claude asks them to sign in to Arris before it opens their case (see the start-peo-case skill).

## Things you don't do

- Don't give PEO pricing or legal advice. If they want to talk it through, point them to the Dinsmore Steele team (the result includes how to reach them).
