# How to Add to this SOP

This documentation repository is maintained by human domain experts and AI agents. Agentic workflows are used to ensure Standard Operating Procedures (SOPs) are consistent, well-formatted, and easy to read.

## For Human Contributors

You do not need to manually format complex markdown tables or structure step-by-step guides. You can leverage AI coding tools to assist with this process.

### The Toolkit Workflow

1. **Provide Raw Materials**: Start by creating a draft markdown (`.md`) file. Insert screenshots of the process you want to document and add bulleted notes explaining what is happening. Separate different steps with horizontal dividers (`---`).

   **How Image Links Work**:
   In Markdown, you aren't actually pasting the image itself into the text. Instead, you are placing a text link that points to an image file saved in the same directory.
   > [!TIP]
   > Most modern IDEs and Markdown editors make this effortless. When you copy an image and paste it directly into your document, the editor will automatically save the image file to your directory and generate the correct link for you (e.g., `![caption](image.png)`).

   **Example of raw input:**

   ```markdown
   Click on the Sales Order link in the sidebar to open the module.
   ![menu navigation](image.png) <-- this is the link to the image file

   ---

   Fill out the customer information and click save.
   ![customer form](image-1.png)
   ```

2. **Invoke the AI Agent**: Instruct your AI agent to review the `.agents/workflows/convert-images-to-sop.md` workflow file. Tell the agent to convert the draft images and notes into a formal SOP based on those instructions.
3. **Review**: The agent will generate a plan. Review it and provide feedback if any crucial domain knowledge, tips, or cautions were missed.
4. **Approve**: Once approved, the agent will format the document, embed the images, and update the `changelog.md` and `index.md`.

**Useful Resources for Getting Started**:

- [The Convert Images to SOP Workflow](.agents/workflows/convert-images-to-sop.md): Read the instructions the AI follows when generating documentation.

## For AI Agents

When tasked with adding to or modifying SOPs in this repository, you must adhere to the following rules:

1. **Follow established workflows**: If converting images and notes to text, you must strictly follow the `.agents/workflows/convert-images-to-sop.md` workflow.
2. **Review the Structure**: Always check the `index.md` to understand where new documentation belongs in the broader repository structure.
3. **Avoid Duplication**: Explore the repository for other documents that could be linked in the procedures being worked on. If you have the ability to plan and ask questions, prompt the user to suggest links to existing documents for shared concepts. This prevents clutter and duplicate steps across multiple documents.
4. **Maintain Consistency**: Use standard Markdown and GitHub-style alerts (`> [!NOTE]`, `> [!IMPORTANT]`, etc.) for callouts, warnings, and tips. Do not use generic block labels.
5. **Version Control**: Every time an SOP is successfully modified, you must update the `changelog.md` file using semantic versioning to track the revision.
