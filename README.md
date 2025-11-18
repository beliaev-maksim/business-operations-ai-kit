# Business Operations AI Kit

Welcome to the Business Operations AI Kit! This framework is designed to help non-technical users in business operations define and execute their annual Objectives and Key Results (OKRs) and other initiatives. It uses an AI agent powered by GitHub Copilot to guide you through a structured process, from clarifying context to implementing tasks.

## Prerequisites

To use this kit, you will need the following:

1.  **Visual Studio Code**: This is the editor where you will interact with the AI agent. You can download it from [here](https://code.visualstudio.com/).
2.  **GitHub Copilot Extension**: This VS Code extension provides the AI capabilities. You can install it from the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot).
3.  **GitHub Copilot Subscription** or **Valid API key to LLM**: You need an active subscription to get access to major LLMs.

## How It Works

This kit is a collection of prompts and templates that guide the AI agent. You interact with the agent in the VS Code chat, and it will help you create a series of documents that build upon each other, leading to a well-defined and executable plan.

The core philosophy is defined in the `constitution.prompt.md`, which sets the rules for how the AI agent should behave.

## The Workflow

The process is broken down into a sequence of steps. You should follow them in order to get the best results. Each step corresponds to a prompt that you will use to instruct the AI agent.

### Step 1: Define Your Organizational Context
-   **Prompt**: `/organization`
-   **Goal**: To create a foundational document with key information about your organization.
-   **Action**: The agent will ask you questions, do some research, and create a file named `01_organization.md`. You should review this file for accuracy.
-   **Example**: `/organization My company is called Canonical, publisher of Ubuntu OS`

### Step 2: Set the Constitution
-   **Prompt**: `/constitution`
-   **Goal**: To establish the rules and principles for the AI agent's behavior for a specific department.
-   **Action**: The agent will use a template to create a `02_constitution.md` file with the core principles for a specific department.
-   **Example**: `/constitution for the HR department`

### Step 3: Specify Your Initiative
-   **Prompt**: `/specify`
-   **Goal**: To clearly define a new initiative or OKR.
-   **Action**: The agent will guide you in creating a detailed specification document.
-   **Example**: `/specify I want to create an OKR to improve our customer onboarding process.`

### Step 4: Clarify and Refine
-   **Prompt**: `/clarify`
-   **Goal**: To have the agent review a document and ask you clarifying questions to help improve it.
-   **Action**: The agent will analyze a specification or plan and identify areas that need more detail or clarity.
-   **Example**: `/clarify Can you review the specification for the new onboarding process and ask me some questions to make it better?`

### Step 5: Create a Plan
-   **Prompt**: `/plan`
-   **Goal**: To develop a high-level plan for executing the initiative.
-   **Action**: The agent will generate a plan based on the specification.
-   **Example**: `/plan Let's create a plan for the customer onboarding initiative.`

### Step 6: Break Down into Tasks
-   **Prompt**: `/tasks`
-   **Goal**: To break the high-level plan into smaller, actionable tasks.
-   **Action**: The agent will create a detailed task list.
-   **Example**: `/tasks Break down the onboarding plan into smaller tasks.`

### Step 7: Implement the Work
-   **Prompt**: `/implement`
-   **Goal**: To get assistance in executing the defined tasks.
-   **Action**: The agent can help you draft documents, write scripts, or perform other work as needed.
-   **Example**: `/implement Help me draft an email to announce the new onboarding process.`

### Step 8: Analyze and Review
-   **Prompt**: `/analyze`
-   **Goal**: To analyze the progress or outcome of your initiative.
-   **Action**: The agent can help you review data, summarize results, and prepare reports.
-   **Example**: `/analyze Let's analyze the feedback from the first week of the new onboarding process.`

### Step 9: Final Checklist
-   **Prompt**: `/checklist`
-   **Goal**: To ensure all aspects of the initiative have been addressed.
-   **Action**: The agent will run through a checklist to validate the completeness of the work.
-   **Example**: `/checklist Run the final checklist for the customer onboarding project.`



