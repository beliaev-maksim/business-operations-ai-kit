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

3.  **Ask Clarifying Questions:**
    *   Based on your research, ask the user clarifying questions to fill in any gaps. For example:
        *   "I found that your mission is 'X'. Could you elaborate on what that means in practice for your team?"
        *   "Your website mentions a value of 'innovation'. How does your organization encourage and measure innovation?"
        *   "Are there any internal goals or priorities for the upcoming year that are not publicly mentioned?"

4.  **Synthesize and Create the File:**
    *   Synthesize all the gathered information into a structured markdown document.
    *   Use the `templates/organization-template.md` as a template for the output file.
    *   Create a new file named `01_organization.md` in the root of the workspace.
    *   Populate the file with the synthesized information.
    *   Inform the user that the file has been created and is ready for their review.
