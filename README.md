# Arris by Dinsmore Steele

![Arris](./assets/icon.png)

Arris is Dinsmore Steele's platform for getting a company quoted by professional employer organizations (PEOs). This plugin lets you work on your Arris case from Claude: see what is left, answer the intake questions from what you know or from your own documents, get secure links to upload the documents Arris still needs, start a new case, or take the free PEO Alignment Score.

You need an Arris account to use it. Dinsmore Steele invites clients, broker partners and PEOs to Arris, and what you can do depends on your account; if you don't have an account yet, visit [dinsmoresteele.com](https://www.dinsmoresteele.com).

## What's included

| Component | What it does |
|---|---|
| Arris connector | Connects Claude to Arris at `https://arris.dinsmoresteele.com/api/mcp`. You sign in to Arris the first time you use it. |
| `finish-peo-case` skill | Walks through a case in progress: status, open questions, documents, and the hand-off to sign in Arris. |
| `start-peo-case` skill | Opens a new case after you confirm the company name. Broker partners can then invite their client by email. |
| `peo-alignment-score` skill | Takes you through the 12-question PEO Alignment Score and emails you the report. |
| `staff-case-work` skill | For Dinsmore Steele staff: your queue, finding a case, what's missing, messaging the client or partner, waiving a document, returning or reopening a case. |
| `send-to-peos` skill | For Dinsmore Steele staff: send a ready case to PEOs (after you confirm the list) and record what each PEO came back with. |
| `staff-reports` skill | For Dinsmore Steele staff: open case counts, what opened and closed recently, and any report from the Arris Reports tab. |
| `peo-submissions` skill | For PEOs: the quote requests sent to you, their messages, asking Dinsmore Steele a question, declining to quote, and your PEO profile. |

## Getting started

In claude.ai or the Claude desktop app, add Arris from the directory. In Claude Code, run:

```
/plugin install arris-peo --marketplace dinsmore-steele/arris-claude-plugin
```

After installing, say "Hi Arris" or "help me finish my Arris case". Claude will ask you to sign in to Arris, then show you what you can do.

## What it sends, and where

- **Everything goes to Arris only.** The plugin's single connection is the Arris server above, run by Dinsmore Steele. It does not run any code on your computer, fetch anything else, or send data to any other service.
- **Sign-in.** Claude connects with OAuth. Arris sees which Claude app connected; you can revoke the connection at any time under Profile, then AI connections, in Arris.
- **What Claude reads from Arris:** your cases, which questions and documents are still open, and the answers already saved. It only sees the cases your account can see.
- **What Claude writes to Arris:** the intake answers you give it, each marked "Filled in by your AI assistant" until you confirm it in Arris; a new case, only after you confirm the company name; for partners, a client invitation email, only after you confirm the address; for Dinsmore Steele staff, case messages, waivers, returns, reopens, sends to PEOs and recorded outcomes, each after you confirm it; for PEOs, a message to Dinsmore Steele or a decline, after you confirm it. Claude asks before each change unless you set that tool to "Always allow".
- **Documents never pass through the chat.** Claude gives you an upload link, and the file goes from your browser straight to Arris's secure storage.
- **PEO Alignment Score.** Your answers, name, work email and company are sent to Dinsmore Steele to score the assessment and email you the report.
- **Claude cannot sign or submit your case.** You review, sign and submit in Arris yourself.

Please don't paste employee health information, census files or Social Security numbers into the chat. Use the upload links instead.

## Support and policies

- Help connecting: [arris.dinsmoresteele.com/connect](https://arris.dinsmoresteele.com/connect)
- Privacy policy: [arris.dinsmoresteele.com/privacy](https://arris.dinsmoresteele.com/privacy)
- Terms: [arris.dinsmoresteele.com/terms](https://arris.dinsmoresteele.com/terms)
- Support: [arris@dinsmoresteele.com](mailto:arris@dinsmoresteele.com)
- Dinsmore Steele: [dinsmoresteele.com](https://www.dinsmoresteele.com)
