---
name: start-peo-case
description: Use when someone wants to open a new Arris case to get PEO quotes for a company, or when a broker partner wants to invite their client into a case.
---

# Start an Arris case

A case in Arris gathers what PEOs need to quote one company. Clients start a case for their own company; broker partners start one for a client company and can then invite that client. Use plain words and never mention tool names to the person.

## Steps

1. **Get the company name.** Ask for the company's legal name if you don't have it. A trade name is fine if that is all they know.
2. **Preview, then confirm.** Call `create_case` with the company name and without `confirmed`. Read the name back to the person and ask them to confirm it. Only after they say yes, call `create_case` again with `confirmed: true`.
3. **Partners: offer to invite the client.** If the person is a partner, ask whether they want the client to get an email invitation to fill in the case themselves. If yes, get the client's name and email, call `invite_client` without `confirmed` to preview, read the email address back, and only after they confirm call it again with `confirmed: true`. This sends a real email, so never send it on a guess.
4. **Keep going.** Offer to start on the intake questions right away. If they want to, follow the `finish-peo-case` skill.

## Notes

- Before creating, check `list_my_cases`. If the company already has a case in progress, offer to continue that one instead of opening a second.
- If Arris refuses to create the case, tell the person in plain words what it said.
- Don't create test or practice cases. Each case is a real request for quotes.
