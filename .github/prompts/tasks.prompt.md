---
description: "Generate a detailed task plan for a chosen solution, creating a `05_<solution_name>.md` file."
---

## Agent Constitution

Before taking any action, you **MUST** open and consult the `templates/agent-file.md` file. This document defines your persona, consultation style, and critical assessment frameworks. Adhere to these guidelines at all times.

## User Input

```text
{{user_input}}
```

The user may provide the name of the solution they have chosen.

## Outline

1.  **Identify Context Files**:
    *   Locate the `03_...md` file (Objective) and the `04_plan.md` file in the workspace. These are essential inputs.
    *   If either file is missing, you MUST stop and inform the user that the `objective` and `plan` commands must be run first.

2.  **Solution Selection Workflow**:
    *   **Step 2a: Parse Solutions**: Read `04_plan.md` and identify the ranked solutions presented. Extract the title/name of each solution.
    *   **Step 2b: Prompt User for Selection**:
        *   If the user has NOT already specified a solution in their input, you MUST present the list of solutions from `04_plan.md` and ask the user to choose one to proceed with.
        *   If the user HAS specified a solution, confirm that it matches one of the options in `04_plan.md`. If it doesn't match, list the available options and ask for clarification.

3.  **Task Plan Generation**:
    *   Once a valid solution is chosen, proceed with generating the detailed task plan.
    *   **Step 3a: Create New File**: Create a new file named `05_<solution_name>.md`. Sanitize the chosen solution name to be filesystem-friendly (e.g., replace spaces with hyphens, lowercase).
    *   **Step 3b: Load Template**: Use the content of `templates/tasks-template.md` as the foundational structure for the new file.
    *   **Step 3c: Populate the Template**: You will now fill in the placeholders in the template with extreme detail and professionalism.
        *   **[SOLUTION_NAME]**: The name of the chosen solution.
        *   **[DATE]**: The current date.
        *   **[Link to 03_objective_name.md]**: Add a relative link to the objective file.
        *   **[Link to 04_plan.md]**: Add a relative link to the plan file.
        *   **Solution Recap**: Find the chosen solution in `04_plan.md` and copy its `Description` and `Acceptance Criteria` into this section. This provides essential context.
        *   **Task Breakdown**: This is the most critical part. You must generate a comprehensive list of tasks that would be required to implement the chosen solution.
            *   **Adhere to the Phases**: Generate tasks that logically fit within the predefined phases: `Planning & Discovery`, `Design & Prototyping`, `Implementation & Testing`, `Rollout & Change Management`, and `Measurement & Closure`.
            *   **Generate Realistic Tasks**: The tasks should be specific, actionable, and relevant to the solution. Think about what a real project manager would need to track. Include tasks for project management, stakeholder communication, requirements gathering, design, development/configuration, testing, training, deployment, and post-launch support.
            *   **CRITICAL: Include These Essential Tasks**:
                *   **Baseline Measurement Task** (Phase 1): Must include task to measure baseline BEFORE any implementation starts
                *   **Risk Mitigation Tasks** (appropriate phases): For each high-risk item (score ≥6) from plan, create specific mitigation task
                *   **Dependency Management Tasks** (Phase 1): Tasks to secure commitments from dependency owners, validate timelines
                *   **Critical Path Buffer** (all phases): Add 20-30% time buffer to tasks on critical path
                *   **Resource Validation Task** (Phase 1): Confirm team member availability and % allocation
                *   **Knowledge Transfer Tasks** (Phase 5): Create documentation, train BAU owner, conduct handoff session
                *   **Sustainability Tasks** (Phase 5): Establish continuous improvement process, schedule 30/60/90 day reviews
            *   **Populate All Columns**: For each task you generate, you must also fill in the other columns of the table with realistic, placeholder information:
                *   **Owner**: Assign a plausible role (e.g., `[Project Manager]`, `[Business Analyst]`, `[Lead Developer]`, `[QA Lead]`, `[Training Lead]`).
                *   **Effort (Days)**: Provide a reasonable estimate in days (e.g., `1`, `3`, `5`, `10`). Add buffer time for critical path tasks.
                *   **Definition of Done (Acceptance Criteria)**: Write 1-2 clear, concise acceptance criteria for each task. This is crucial for demonstrating your consulting acumen.
                *   **Dependencies**: Note if task depends on completion of other tasks or external parties.

4.  **Report to User**:
    *   Once the `05_<solution_name>.md` file has been created and saved, inform the user of the success.
    *   Provide the full path to the newly created file.
    *   Briefly summarize the plan, mentioning the chosen solution and the number of tasks generated across the five phases.
    - Suggest the next step, which is to review the plan and secure stakeholder buy-in.
