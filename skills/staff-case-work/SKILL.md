---
name: staff-case-work
description: "Use when a Dinsmore Steele staff member wants to work Arris cases from Claude, for example to see their queue, find a case, check what's missing, message the client or partner, waive a document, return a case to the client or reopen one."
---

# Staff case work in Arris

The person is a Dinsmore Steele staff member (operations or admin). Every change you make is recorded in the case history under their name, so say exactly what you will change before you do it, and make each change only after they agree.

## Start

Call `staff_overview` at the start of a conversation. It gives case counts by stage and the cases assigned to this person. Offer a short numbered list of what they can do next.

## Find and read a case

- Use `find_cases` to search by company name, by stage, or for only the cases assigned to them.
- To see what's left on a case, use `get_case_status`, `get_open_questions` and `list_documents`.
- To see where a case stands with PEOs, use `get_case_submissions`: who it went to, whether they downloaded it, and each PEO's outcome.
- Use `list_peos` to look up a PEO in the registry.

Summarise; don't paste raw lists. Lead with what needs attention.

## Make changes (confirm each one first)

- **Answer intake questions** with `answer_questions`, only from what the staff member tells you or from documents they shared with you.
- **Message the client or partner** with `send_case_message`. Draft the message, show it, and send it only after they approve. Arris refuses messages that look like they contain health or personal identifiers, and so should you: never put health information, SSNs or dates of birth in a message.
- **Waive a document** with `waive_document`, with a reason the staff member gives you. The document id comes from `list_documents`.
- **Return a case to the client** with `return_case_to_client`, with a note that says plainly what the client needs to do. The client is notified.
- **Reopen a closed case** with `reopen_case`, with the reason.
- **Invite the client** (when a partner case needs it) with `invite_client`, previewing first.

Sending a case to PEOs and recording their outcomes are covered by the `send-to-peos` skill.

## What stays in Arris

Signing and anything an admin-only screen does stay in Arris. Give the staff member the case link (`openInArris`) for those.
