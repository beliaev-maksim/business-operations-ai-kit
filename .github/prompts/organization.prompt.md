---
name: Business Ops AI Kit - Organization Context
---
# Organization Context

## Agent Constitution

Before taking any action, you **MUST** open and consult the `templates/agent-file.md` file. This document defines your persona, consultation style, and critical assessment frameworks. Adhere to these guidelines at all times.

This prompt is designed to gather and synthesize information about the user's organization. The goal is to create a comprehensive document that will serve as a foundation for defining Objectives and Key Results (OKRs).

## Instructions

1.  **Gather Initial Information:**
    *   Ask the user to provide the name of their organization.
    *   Ask the user for any publicly available information or links that describe their organization's mission, vision, and values.

2.  **Conduct Research:**
    *   Perform a web search using the organization's name to find their official website, news articles, and other relevant public information.
    *   Extract key information about the organization's to fill a doc based on `templates/organization-template.md`
    *   Research and answer the following questions using publicly available info, like reviews on glassdoor, linkedin, reddit, etc:
        *   **Key Leadership**: Who are the key executive and functional leaders relevant to your business operations initiatives?
        *   **Organizational Culture**: How would you describe the culture regarding:
            *   **Decision-making**: Is it top-down, consensus-driven, or decentralized?
            *   **Change**: How readily do teams adapt to new processes or tools?
            *   **Communication**: What are the preferred channels for internal communication (e.g., email, chat, formal meetings)?

3.  **Fill Gaps with User Input (One Question at a Time):**
    *   After your research, review the `templates/organization-template.md` structure.
    *   If you identify any missing information, ask the user a **single, specific question** to get the data you need for the first gap.
    *   **Wait for the user's response** before proceeding.
    *   Once you receive an answer, move to the next piece of missing information and repeat the process: ask one question and wait for the answer.
    *   **IMPORTANT**: Do not ask multiple questions at once. The interaction must be sequential.
    *   For example, if you can't find the key leadership and the decision-making process:
        1.  First, ask: "I couldn't find details on the key leadership. Who are the key executive and functional leaders relevant to your business operations initiatives?"
        2.  *Wait for the user to reply.*
        3.  Then, ask: "Thank you. Now, regarding organizational culture, how would you describe the decision-making process? Is it top-down, consensus-driven, or decentralized?"

4.  **Synthesize and Create the File:**
    *   Synthesize all the gathered information into a structured markdown document.
    *   Use the `templates/organization-template.md` as a template for the output file.
    *   Create a new file named `01_organization.md` in the root of the workspace.
    *   Populate the file with the synthesized information.
    *   Inform the user that the file has been created and is ready for their review.
