# prodmoh-mcp
Bring your PRDs &amp; User Stories directly into your IDE — via MCP  Prodmoh MCP is a **Model Context Protocol (MCP)** server that connects your Prodmoh workspace to any MCP-compatible AI client (ChatGPT, Claude Desktop, VS Code agents, custom IDE tools).

# ProdMoh MCP Server 🚀

> **Your PRDs & User Stories, delivered directly into your IDE.**

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-purple)](https://modelcontextprotocol.io)
[![Powered By ProdMoh](https://img.shields.io/badge/Powered%20By-ProdMoh-blue)](https://prodmoh.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**ProdMoh MCP** is a **Model Context Protocol (MCP)** server that connects your [ProdMoh](https://prodmoh.com) workspace to any MCP-compatible AI client (Cursor, VS Code, Claude Desktop, Windsurf).

It acts as your **Product Context Layer**, delivering PRDs, User Stories, and Acceptance Criteria directly into your coding environment so developers can build, test, and ship with perfect alignment.

---

## ⚡ Why ProdMoh MCP?

Today’s development workflow is broken. Developers constantly context-switch between:
* IDE (Code)
* Jira / Linear (Tasks)
* Confluence / Notion (Docs)
* Slack (Clarifications)

**ProdMoh MCP fixes this.** It makes product requirements instantly accessible inside AI-powered coding workflows.

* **No context switching.**
* **No outdated docs.**
* **No hallucinations.**

## 🧑‍💻 Developer Workflows & Prompt Library

Maximize your productivity by using these prompt patterns in Cursor, VS Code, or Claude Desktop.

### 1. 🏗️ Scaffold Implementation Code (Backend)
Stop guessing field names. Generate services that match the spec exactly.
> **Prompt:** "Using `get_prd`, fetch the 'Checkout Flow' requirements. Generate the Node.js service for this feature. Include validation logic for all edge cases listed in the doc."

### 2. 🧪 Auto-Generate Unit Tests (TDD)
Achieve 100% coverage of Acceptance Criteria before writing logic.
> **Prompt:** "Fetch the User Story for 'Login'. Generate a Jest test suite that covers every bullet point in the Acceptance Criteria. Ensure you include test cases for the 'Negative Scenarios' (e.g., locked account, timeout)."

### 3. 🎨 Frontend Component Construction
Build UI components that respect design constraints and accessibility rules.
> **Prompt:** "Read the 'User Profile' User Story. Scaffold a React/Tailwind component for the profile card. Ensure the 'Bio' field enforces the character limit defined in the requirements and includes the specific aria-labels mentioned."

### 4. 🗄️ Database Schema Modeling
Translate data requirements directly into SQL or ORM definitions.
> **Prompt:** "Reference the 'Order Management' PRD. Generate the Prisma schema `model` for Orders and OrderItems. Ensure all relationship constraints (1-to-1 vs 1-to-many) match the Data Requirements section."

### 5. 📜 API Contract Generation
Prevent frontend/backend drift by generating specs from the source of truth.
> **Prompt:** "Look at the 'Search API' requirements. Generate an OpenAPI (Swagger) YAML definition for this endpoint, including all the specific error codes (400, 403, 429) defined in the 'Error Handling' section."

### 6. 🕵️ Code Review & Validation
Use the AI as a 'QA Buddy' to check your work against the spec.
> **Prompt:** "I have highlighted my current implementation of the `calculateTax` function. Compare this code against the 'Taxation Rules' PRD. Did I miss any specific state exemptions or rounding rules mentioned in the doc?"

### 7. 💡 Clarify Requirements Instantly
Don't wait for a Zoom call to get an answer.
> **Prompt:** "@ProdMoh What are the specific password complexity rules defined in the Security PRD? Do we require special characters?"

<img width="1024" height="1024" alt="ChatGPT Image Nov 25, 2025, 10_38_12 PM" src="https://github.com/user-attachments/assets/0e49e14f-e658-4c19-bb2b-b2c462edf48d" />

<img width="937" height="697" alt="Screenshot 2025-11-25 at 10 41 49 PM" src="https://github.com/user-attachments/assets/03a31235-c228-4380-b40e-d12841ea128b" />

<img width="846" height="681" alt="Screenshot 2025-11-25 at 10 46 59 PM" src="https://github.com/user-attachments/assets/af5562cc-16af-4c44-a29f-7ce6a986e95e" />


## 🛠️ Installation & Setup

You do not need to run a local server. ProdMoh provides a hosted MCP endpoint via **Server-Sent Events (SSE)**.

### Prerequisite
1.  Log in to your [ProdMoh Dashboard](https://prodmoh.com/login).
2.  Click **"Share with Developers"** to generate your secure `x-prodmoh-token`.

### Option 1: Configure Cursor / VS Code (Recommended)
Add this to your `mcp.json` config file (usually found in `~/.cursor/mcp.json` or `%APPDATA%/Cursor/User/globalStorage/mcp.json`).

```json
{
  "mcpServers": {
    "prodmoh": {
      "type": "sse",
      "url": "[https://api.prodmoh.com/mcp/sse](https://api.prodmoh.com/mcp/sse)",
      "headers": {
        "x-prodmoh-token": "YOUR_TOKEN_HERE"
      }
    }
  }
}

{
  "mcpServers": {
    "prodmoh": {
      "type": "sse",
      "url": "[https://api.prodmoh.com/mcp/sse](https://api.prodmoh.com/mcp/sse)",
      "headers": {
        "x-prodmoh-token": "YOUR_TOKEN_HERE"
      }
    }
  }
}
```

# What Prodmoh MCP Does

### Direct PRD Retrieval  
Fetch any PRD by:
- Name  
- ID  
- Feature keyword  
- Tags  
- Semantic search  

### User Story Access  
Pull complete user stories for features or epics:
- Story text  
- Acceptance criteria  
- Status & priority  

### Requirements & Acceptance Criteria Extraction  
LLMs use this for:
- Code generation  
- Test generation  
- API scaffolding  
- Validation logic  

### Documentation Search  
Search all Prodmoh workspace docs:
- PRDs  
- Stories  
- Requirements  
- Insights  
- Edge cases  

### Context for Coding, Testing & Refactoring  
Zero assumptions.  
Only accurate product truth.

---

# How Developers Use Prodmoh MCP for Coding & Testing  
### *Code & tests generated with real product context — without leaving the IDE.*

Prodmoh MCP enables a new AI-native developer workflow:



## 1. Pull PRDs & stories directly inside ChatGPT / IDE

Use Prodmoh MCP to get_prd "Checkout Flow"

Instantly retrieves:
- Requirements  
- Acceptance criteria  
- Edge cases  
- Metrics  
- Dependencies  

Developers don’t search. They just continue coding.



## 2. Generate implementation code using the real PRD

Ask: Using this PRD, generate the Node.js service.
Include validation, routing, and all edge cases.


LLMs now write code based on:
- Actual requirements  
- Real edge cases  
- Defined constraints  

No hallucination.  
No misinterpretation.  


## 3. Auto-generate unit tests from acceptance criteria

Generate Jest unit tests using the acceptance criteria from this PRD or user story.


AI produces:
- Meaningful test cases  
- Proper coverage  
- Expected edge cases  
- Failure conditions  

This drastically improves correctness & reduces bugs.


## 4. Ask clarifying questions instantly

No Slack messages. No waiting.

- What happens if the user cancels during onboarding?
- What error states are defined in the PRD?
- What are the password rules mentioned in the Login PRD?


MCP responds using the authoritative product documentation.



## 5. Continue coding with perfect alignment  
Developers build exactly what product intended.  
Testing aligns to real acceptance criteria.  
No surprises later.  



Available MCP Actions
-get_prd

## Fetches a complete PRD.

Input:

{
  "query": "checkout flow"
}


Output includes:

-Product overview

-Problem statement

-Requirements

-Acceptance criteria

-Edge cases

-Technical notes

-Metrics / success criteria

## get_userstories

Retrieve user stories for a feature or epic.

Input:

{
  "feature": "Login"
}


Output:

-Story ID

-Story text

-Acceptance criteria

-Priority & status



License

MIT License — free to use, modify, and integrate commercially.

Support the Project

If Prodmoh MCP improves your workflow:

⭐ Star the repo

Share it with your team

Contribute improvements

Build IDE plugins using it







