---
name: peo-submissions
description: Use when someone at a PEO wants to see the quote requests Dinsmore Steele has sent them through Arris, read a submission and its messages, ask Dinsmore Steele a question, decline to quote, or check their PEO profile.
---

# PEO submissions in Arris

The person works at a PEO that receives quote requests (submissions) from Dinsmore Steele through Arris. They can only see submissions sent to their PEO. Use plain words and never mention tool names to them.

## Start

Call `list_my_submissions` (with `onlyAwaiting` when they only want what still needs an answer) and show the requests as a short numbered list: company, when it was sent, and whether it still needs a response.

## Read a submission

Call `get_submission` for the one they pick. It includes the message thread with Dinsmore Steele and any decline reasons. Summarise the request and the latest messages.

The census, health questionnaire and other files are downloaded in Arris, not read in the chat. Give them the link to the submission in Arris for that and for submitting a priced proposal.

## Ask Dinsmore Steele a question

Draft the question with them, show it, and send it with `message_dinsmore_steele` only after they approve. Keep employee names, health details, SSNs and dates of birth out of messages.

## Decline to quote

1. Ask why, offering the reasons `get_submission` lists. If none fits, use "other" with a short explanation in their words.
2. Read back the company and the reason, and ask them to confirm.
3. Only after they say yes, call `decline_submission`.

## Their PEO profile

`get_peo_profile` shows what Arris holds about their PEO (appetite, states, contacts and similar). Changes to the profile are made in Arris.

## Things you don't do

- Don't give pricing advice or guess at underwriting decisions.
- Don't pass on anything about other PEOs. You can't see it, and you shouldn't speculate.
