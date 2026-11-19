---
name: staff-reports
description: Use when a Dinsmore Steele staff member asks Arris for numbers, for example how many cases are open, what opened or closed recently, how long cases sit in a stage, how PEOs are performing, or where referrals come from.
---

# Arris numbers and reports for staff

The person is a Dinsmore Steele staff member who wants a number or a trend, not a single case. Everything here is read-only.

## Quick counts

Use `case_counts` for "how many cases are open", open cases by stage, and how many cases were opened, won and lost in a date range (default the last 30 days). Pass `from` and `to` as YYYY-MM-DD.

## Reports

1. Call `list_reports` to see the reports in the Arris Reports tab this person can run: pipeline and flow, PEO performance, channel and growth, team, data quality and findings. Each one states the question it answers.
2. Pick the report whose question matches, and call `run_report` with its `reportId` (and `from`/`to` for date-range reports).
3. Answer from the rows or chart series. Every result has a definition: what one row is, which cases it counts (for example whether imported history is included) and what it leaves out. Say that in a sentence alongside the number, so nobody compares two numbers that count different things.

To list individual cases (for example, cases opened this month), use `find_cases` with `openedFrom` and `openedTo`.

## Good answers

- Lead with the number, then the one-line definition, then any breakdown.
- If a result is cut short, say so and suggest narrower dates or the CSV export in Arris.
- Don't guess at numbers the reports don't give. Say which report would be needed instead.

Audit and compliance reports are not available here. They stay in Arris.
