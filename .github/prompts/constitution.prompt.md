---
description: Create or update the project constitution from interactive or provided principle inputs, ensuring all dependent templates stay in sync
---

## User Input

```text
{{user_input}}
```

You **MUST** consider the user input before proceeding (if not empty).

## Agent Constitution

Before taking any action, you **MUST** open and consult the `templates/agent-file.md` file. This document defines your persona, consultation style, and critical assessment frameworks. Adhere to these guidelines at all times.

## Outline

You are creating a new constitution file `02_constitution.md` based on the template at `templates/constitution-template.md`. This template contains placeholder tokens in square brackets (e.g. `[DEPARTMENT_NAME]`, `[CORE_PRINCIPLES]`). Your job is to (a) collect/derive concrete values from the user, (b) fill the template precisely, and (c) create the new constitution file.

Follow this execution flow:

1.  Load the constitution template from `templates/constitution-template.md`.
2.  Identify the department from the user input. If not provided, ask the user for the department name.
3.  Use the user-provided principles as the `[CORE_PRINCIPLES]` or derive them from the organization context and suggest them to the user.
4.  Set `[COMPANY_NAME]` from the organization context if available, otherwise ask the user.
5.  Set `[VERSION]` to `1.0.0`.
6.  Set `[RATIFIED_DATE]` to today's date.
7.  Set `[LAST_AMENDED_DATE]` to today's date.
8.  Create a new file `02_constitution.md` in the root of the workspace with the populated template.
9.  Output a final summary to the user with:
    *   A confirmation that the constitution was created.
    *   The path to the new file.

Formatting & Style Requirements:

- Use Markdown headings exactly as in the template (do not demote/promote levels).
- Wrap long rationale lines to keep readability (<100 chars ideally) but do not hard enforce with awkward breaks.
- Keep a single blank line between sections.
- Avoid trailing whitespace.

