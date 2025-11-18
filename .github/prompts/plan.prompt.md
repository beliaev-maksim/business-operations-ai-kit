---
description: Brainstorm and evaluate potential solutions for a defined business problem.
---

## User Input

```text
{{user_input}}
```

You **MUST** consider the user input before proceeding (if not empty).

## Agent Constitution

Before taking any action, you **MUST** open and consult the `templates/agent-file.md` file. This document defines your persona, consultation style, and critical assessment frameworks. Adhere to these guidelines at all times.

## Outline

1.  **Load Context**:
    *   Find and read the latest `03_<objective_name>.md` file in the workspace. This file contains the root problem analysis.
    *   If no such file exists, inform the user and stop.
    *   Extract the "Refined Problem Statement" and "Problem-Oriented KPIs" to use as the foundation for your work.
    *   Load the `templates/plan-template.md`.

2.  **Execute Solution Brainstorming Workflow**:

    1.  **Generate Solutions**:
        *   Based on the root problem, brainstorm at least **three distinct solutions**.
        *   These solutions should represent different approaches (e.g., a people/process change, a technology change, a minimal "quick win" vs. a comprehensive "strategic fix").

    2.  **Evaluate Each Solution**: For each of the three solutions, you must fill out the following in the template:
        *   **Description**: Clearly explain what the solution is and how it would work at a high level.
        *   **How it Addresses the Root Cause**: Directly link the solution back to the root cause identified in the `03_<objective_name>.md` file.
        *   **Impact vs. Effort Analysis**: Provide a high-level assessment (High, Medium, Low) for both the potential impact on the KPIs and the estimated effort to implement.
        *   **Pros and Cons**: List at least two advantages and two disadvantages for each solution.
        *   **Acceptance Criteria**: Write clear, testable acceptance criteria in the "Given/When/Then" format. These criteria must prove that the solution, if implemented, successfully solves the problem.
        *   **CRITICAL ASSESSMENTS** (Add these to each solution evaluation):
            *   **Risk Assessment**: Identify 3-5 key risks using probability/impact matrix (Low/Medium/High). Calculate risk score. List mitigation strategies for high risks (score ≥6).
            *   **Resource Capacity**: Estimate team % allocation required. Flag if >60% of team capacity. Identify skill gaps or competing priorities.
            *   **Dependency Analysis**: List critical dependencies (teams, vendors, approvals). Identify critical path items that could delay timeline by >2 weeks.
            *   **Change Magnitude**: Assess change scale (Minor/Moderate/Transformational). Recommend change readiness activities for Moderate+ changes.
            *   **Sustainability Planning**: Identify BAU owner post-launch. Note knowledge transfer needs and long-term support model.

    3.  **Rank the Solutions**:
        *   Rank the solutions from #1 (most recommended) to #3.
        *   The ranking should be based on a balanced assessment of impact, effort, and alignment with general business best practices. The #1 solution should typically offer the best value proposition.

3.  **File Creation**:
    *   Create a new file named `04_plan.md` in the root of the workspace.
    *   Populate this file with the brainstormed and evaluated solutions, following the structure of `templates/plan-template.md`.

4.  **Report Completion**:
    *   Inform the user that the `04_plan.md` file has been created.
    *   Provide a brief summary of the recommended solution (#1) and why it was chosen.
    *   Advise the user to review the options with stakeholders and then use the `/tasks` prompt to create a detailed implementation plan for the selected solution.

## Key Rules

-   **No Implementation**: This is strictly a planning and brainstorming phase. Do not create any implementation artifacts (e.g., no scripts, no configuration files, no detailed project plans).
-   **Focus on Options**: The primary goal is to present and compare options, not to create a single, detailed execution plan.
-   **Reference the Problem**: Constantly tie your solutions back to the root problem and KPIs defined in the `03_<objective_name>.md` file.
-   **Be Objective**: Present the pros and cons of each solution fairly. Your recommendation should be backed by a clear rationale.
