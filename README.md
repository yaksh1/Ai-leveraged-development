# UI/UX Project Workflow: Agile Design & Development with AI Assistance

This `README.md` outlines a structured, agile workflow for UI/UX design and development projects, leveraging AI assistance to streamline research, design generation, and documentation. The process emphasizes iterative development, clear documentation, and isolated experimentation using Git worktrees.

-----

## 0\. Setting Up Your Gemini UI/UX Expert Gem

Before diving into the workflow, ensure your "Gemini UI/UX Expert Gem" (which is me\!) is properly set up to provide optimal assistance:

**Instructions:** Take the content from your `Ui/Ux-gem-prompt.md` file and paste it into the "Instructions" section when configuring your Gemini Gem. This will provide me with the necessary context and guidelines for our project.

**Knowledge Base:** Paste all relevant books and resources from your `books-for-context` folder into the "Knowledge" section of your Gemini Gem. This will equip me with the foundational knowledge required for product research, design principles, and user understanding.

*Once these steps are complete, your Gemini UI/UX Expert Gem will be ready to assist you throughout the project.*

-----

## 1\. Workflow Overview

Our workflow is designed to move from high-level understanding to detailed implementation, with AI support at each stage.

1.  **Product Research & Brainstorming:** Define core problem, context, and user needs.
2.  **Sitemap Generation:** Structure the application's navigation.
3.  **Wireframe Generation & Customization:** Visualize layouts and user flows.
4.  **UI Preferences Setup:** Define the visual language and component libraries.
5.  **Detailed Page & Story Documentation:** Break down each page into user stories and tasks.
6.  **Iterative Development & Task Completion:** Build and refine in an agile manner.
7.  **Git Worktree for Isolation:** Manage parallel design iterations or feature branches.

-----

## 2\. The Role of the Gemini UI/UX Expert Gem (AI)

As your dedicated "Gemini UI/UX Expert Gem," I will assist throughout this workflow by:

  * **Conducting Product Research:** Analyzing requirements, brainstorming concepts, and identifying key user needs.
  * **Creating Context Scenarios & User Journeys:** Developing detailed narratives of how users will interact with the product.
  * **Generating Sitemap:** Proposing logical navigation structures based on product scope.
  * **Generating Wireframes:** Translating sitemap into low-fidelity visual layouts.
  * **Assisting with Customization:** Providing suggestions and modifications to wireframes and UI elements.
  * **Extracting Design Systems:** Analyzing provided images or descriptions to define design system parameters.
  * **Generating Documentation:** Creating initial drafts and structures for all required `.md` files.
  * **Supporting Agile Iteration:** Responding to task completion updates and assisting with next steps.

-----

## 3\. Detailed Workflow Steps

-----

### Step 1: Product Research & Brainstorming (AI-Assisted)

  * **Action:** Initiate a discussion with the "Gemini UI/UX Expert Gem" (me) to define the product's core purpose, target users, and key functionalities.
  * **AI Output:**
      * `Docs/user-journey.md`: Detailed user journey(s) derived from context scenarios and user research. This document will outline user goals, pain points, and interaction flows.

-----

### Step 2: Sitemap Generation (AI-Assisted)

  * **Action:** Based on the product research and user journey, instruct the AI to generate a comprehensive sitemap.
  * **AI Output:** A clear, hierarchical representation of all pages and their relationships within the application. This will be integrated into the `user-journey.md` or a separate `sitemap.md` if complex.

-----

### Step 3: Wireframe Generation & Customization (AI-Assisted & User-Driven)

  * **Action:** Request the AI to generate initial wireframes for key pages based on the sitemap.
  * **User Action:** Review and provide feedback to the AI for customization and refinement of the wireframes. This is an iterative process.
  * **AI Output:** Visual representations of page layouts, content blocks, and basic interactions.

-----

### Step 4: Set Up UI Preferences (User-Defined)

  * **Action:** Clearly define your UI preferences.
      * **Design System:** tweakcn (or provide an image/description for AI to analyze).
      * **Components Libraries:** Specify your preferred libraries (e.g., OriginUI, SkipperUI, KiboUI, AccernityUI, ReactBits).
      * **Animations:** Specify desired animation styles (e.g., jitter animations).
  * **AI Action:** The AI will acknowledge these preferences and incorporate them into subsequent design suggestions and documentation.

-----

### Step 5: Create Required Documentation Files

The following file structure will be maintained within the `Docs/` directory:

```
Docs/
├── design-system.json
├── user-journey.md
├── tech_stack.md
├── [page_name_1]/
│   ├── [page_name_1]_details.md
│   ├── [page_name_1]_animations.md
│   ├── [page_name_1]_story_1.md
│   └── [page_name_1]_story_2.md
├── [page_name_2]/
│   ├── [page_name_2]_details.md
│   ├── [page_name_2]_animations.md
│   ├── [page_name_2]_story_1.md
│   └── [page_name_2]_story_2.md
└── ...
```

  * **`Docs/design-system.json`**:
      * **Content:** Detailed specifications of the design system (e.g., colors, typography, spacing, components). If tweakcn is used, this might contain its configuration or a representation of its key elements. If an image is provided, the AI will extract and document the design system from it.
  * **`Docs/user-journey.md`**:
      * **Content:** Comprehensive user journey(s) including context scenarios, user goals, steps, emotions, and potential pain points.
  * **`Docs/tech_stack.md`**:
      * **Content:** Overview of the chosen technologies for front-end and back-end (if applicable), including the specified UI component libraries.
  * **`Docs/[page_name]/[page_name]_details.md`**:
      * **Content:** For each primary page (e.g., `home_page_details.md`, `dashboard_details.md`):
          * What the page represents and its primary purpose.
          * List of main components on the page.
          * Key interactions and user flows specific to this page.
  * **`Docs/[page_name]/[page_name]_animations.md`**:
      * **Content:** Specific animation details for elements on that page, adhering to the jitter animations preference or other defined styles.
  * **`Docs/[page_name]/[page_name]_story_X.md`**:
      * **Content:** Multiple user stories for each page (e.g., `home_page_story_1.md`, `home_page_story_2.md`). Each story will contain granular sub-tasks.
      * **Agile Task Tracking:** The "Gemini UI/UX Expert Gem" (me) will mark tasks as `[x]` (completed) within these files as they are addressed.

-----

### Step 6: Agile Iteration & Task Completion

  * **Action:** Work through the `_story_X.md` files. As tasks are completed (either by you or through AI-generated code/design), inform the AI.
  * **AI Action:** The AI will update the task status (`[ ]` to `[x]`) in the relevant `_story_X.md` file and assist with the next logical steps or generate necessary assets/code.

-----

### Step 7: Git Worktree for Iteration

  * **Action:** For significant design iterations or feature explorations, utilize Git worktrees.
      * Create a new worktree for a specific design variant or feature.
      * `git worktree add -b <branch-name> ./trees/<branch-name>`
      * Work on the design within this isolated environment.
  * **Benefit:** This allows for parallel experimentation without affecting the main branch, enabling easy comparison and merging of the best solutions.

-----

## 4\. Getting Started / How to Use

1.  **Initialize your project:** Create your main project directory.
2.  **Create the `Docs/` folder:** Inside your project root.
3.  **Start a chat with the "Gemini UI/UX Expert Gem" (me):** Provide an initial prompt describing your project idea.
4.  **Follow the workflow:** I will guide you through the steps, generating the required `.md` files and content as we progress. You will provide feedback and make decisions.
5.  **Maintain documentation:** Ensure all `.md` files are kept up-to-date as the project evolves.
6.  **Utilize Git worktrees:** For any significant design divergence or feature development.

This structured approach ensures clarity, efficiency, and a collaborative environment for your UI/UX projects.
