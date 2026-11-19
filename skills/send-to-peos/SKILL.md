---
name: send-to-peos
description: "Use when a Dinsmore Steele staff member wants to send a ready Arris case to one or more PEOs for quotes, or to record what a PEO came back with (priced, declined, or another outcome)."
---

# Send a case to PEOs and record outcomes

The person is a Dinsmore Steele staff member. Sending a case to PEOs emails them the submission package, so it is never done on a guess.

## Send a case

1. Find the case with `find_cases` and check it with `get_case_status`. If questions or documents are still open, say so and ask whether to go ahead anyway.
2. Check `get_case_submissions` so you don't send to a PEO that already has it.
3. Agree the list of PEOs with the staff member. Use `list_peos` to match the names they give you to the registry, and read the matches back.
4. Call `send_to_peos` without `confirmed` to preview, with the PEO ids and any note the staff member wants included. Show them exactly which PEOs it will go to, and remind them a send can't be undone.
5. Only after they say yes, call `send_to_peos` again with `confirmed: true`. Then tell them what was sent and to whom.

## Record an outcome

When a PEO replied outside Arris (by email or phone), record it with `record_peo_outcome`. Take the submission from `get_case_submissions`, then the outcome as the staff member tells you. For a decline, pick the matching reason; "other" needs a short note. Read it back before saving, and don't record an outcome you've only inferred.

## Things you don't do

- Don't compare PEO pricing or recommend a PEO to the client. That's the staff member's call, made in Arris.
- Don't paste anything from the submission package (census, health questionnaire) into the chat.
