---
description: Convert Images to SOP Workflow
---

# Convert Images to SOP Workflow

## Goal
To convert draft SOP documents—which typically consist of images and sparsely placed notes separated by dividers (`---`)—into clear, standardized, text-based instructions, while integrating domain-specific notes and cross-references.

## Trigger
Use this workflow when a user tasks you to "inspect pictures and generate SOP steps", "convert images to steps", or write documentation based on draft files with screenshots and notes.

## Formatting Standards
All SOPs must adhere to the following standard format:
1. **Title**: The SOP must begin with a single top-level heading (`#`) representing the title of the document.
2. **Introduction**: Start with a direct introductory sentence explaining the procedure. Avoid using explicit "Objective:" or "Prerequisites:" block labels.
3. **Main Sections**: Group related steps under standard heading levels (e.g., `## Create Shipment`).
4. **Step Headings**: Format step titles as `### Step X: Step Name`.
5. **Dividers**: Use horizontal rules (`---`) only to separate major sections and distinct peer-level concepts/scenarios. Do not use dividers between sequential steps.
6. **Scenarios**: Explicitly label variations as 'Scenario X: [Name]' (e.g., `### Scenario 1: With payment link`) to clarify peer-level distinct paths.
7. **Visual Aids**: Embed the original images directly below the text instructions for the relevant step.
8. **Callouts**: Convert user notes into GitHub-style alerts (`> [!NOTE]`, `> [!IMPORTANT]`, `> [!CAUTION]`, `> [!TIP]`).

## Workflow Steps

### 1. Discovery and Context Gathering
- Read the target draft document to understand the context. It will typically be structured with dividers separating images and notes.
- Identify all linked images within the target section.
- Use the `view_file` tool to inspect the content of each identified image.
- Analyze the images and notes to determine the exact user interface actions being depicted (e.g., clicking menus, selecting dropdown templates, uploading files).

### 2. Drafting the Steps
- Translate the visual UI actions and provided notes into clear, step-by-step text instructions adhering to the **Formatting Standards** defined above.
- Use standard markdown formatting (e.g., bold text for UI buttons, fields, and dropdown options).
- **Cross-Referencing**: Actively explore the repository to identify if any described actions or concepts are already documented elsewhere. If they are, create a relative markdown link to that existing SOP instead of repeating the instructions. Always try to incorporate links into an action item or a specific term (e.g., `Create an [LTL shipping](../ltl/ltl.md) label.`) instead of saying "follow certain instructions" or "refer to something".

### 3. Creating the Implementation Plan (Mandatory)
- **Do not immediately modify the source document.**
- Create an `implementation_plan.md` artifact detailing the proposed textual steps formatted correctly.
- Include a specific "Open Questions" section in the plan. Explicitly ask the user to review the plan and provide any necessary **notes, cautions, tips, or domain knowledge** that isn't visible in the images. Additionally, prompt the user to suggest links to other documents for concepts that may already be available. This helps ensure SOPs are not cluttered and do not have duplicate steps.
- Wait for user approval and feedback before proceeding.

### 4. Execution and Refinement
- Once approved, incorporate the user's feedback into the proper GitHub markdown alerts.
- Replace the draft sections with the finalized, properly formatted SOP text steps. 
- Ensure the original images are retained beneath the newly drafted text steps as visual aids.
- Ensure sequential steps are NOT separated by horizontal rules (`---`), and ensure dividers are placed before major sections and distinct scenarios.

### 5. Finalization
- Verify the markdown formatting of the modified document to ensure consistency with the SOP format.
- **Version Control**: After successfully modifying SOPs, you must update the `changelog.md` file in the root directory to log your changes and bump the version appropriately according to semantic versioning.
- Create a `walkthrough.md` artifact to summarize the changes made for the user.
