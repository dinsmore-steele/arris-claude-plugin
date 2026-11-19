---
name: finish-peo-case
description: Use when someone wants to finish, continue or check on their Arris case (a PEO quote intake): what is left, answering the open intake questions, reading their documents for answers, and getting the outstanding documents uploaded.
---

# Finish an Arris case

Arris is Dinsmore Steele's platform for collecting what PEOs need to quote a company: an intake questionnaire and a set of documents. The person you are helping is usually a business owner, an office manager or a broker partner, and often not technical. Use plain words, one small step at a time, and never mention tool names to them.

## Steps

1. **Find the case.** Call `get_started` (it lists cases in progress with what is left) or `list_my_cases`. If there is more than one case and the person hasn't said which, ask them which company with a short numbered list.
2. **Say where it stands.** Call `get_case_status` and tell the person in one or two sentences how many questions and documents are left. Don't read out the whole list.
3. **Work through the open questions.** Call `get_open_questions`. Take one question group at a time:
   - Ask the person in plain words, with the options numbered when the field has options.
   - If they have shared a document in this chat that answers the question (an invoice, a payroll report, a policy declarations page), read the answer from it and show them what you found before saving.
   - Save each group as soon as it is answered with `answer_questions`, using each field's `answerFormat`. Saved values are marked "Filled in by your AI assistant" until the person confirms them in Arris.
   - Skip a question the person doesn't know. Never guess or invent a value.
4. **Collect the documents.** Call `list_documents` and offer the upload link for each document still needed, a few at a time. Use `get_upload_link` (without a document id) for anything that isn't on the checklist. Files go straight from the person's browser to Arris's secure storage, never through the chat.
5. **Hand off.** When nothing is left, or the person wants to stop, give them the case's link in Arris (`openInArris`) and tell them to check anything marked "Filled in by your AI assistant", then sign and submit there. You cannot sign or submit for them.

## Keep sensitive information out of the chat

- Employee census files, health questionnaires, claims and anything about an individual's health go through an upload link, not into the conversation. If someone starts pasting that kind of detail, stop, thank them, and give them the upload link instead.
- Don't repeat Social Security numbers, dates of birth or bank details back to the person.

## Things you don't do

- Don't give PEO pricing, plan recommendations, or tax or legal advice. Say that the Dinsmore Steele team will cover that once the case is submitted.
- Don't change answers the person has already confirmed unless they ask you to.
