# AI Career Counsellor Web Application

An interactive, single-page web application that leverages the Google Gemini API (`gemini-3.6-flash`) to deliver structured, multi-perspective career guidance. The system allows users to query single or multiple career advisor personas simultaneously, returning tailored domain-specific advice alongside an automated comparative analysis matrix.



## Technical Architecture & Design Principles

The application relies on key frontend and prompt design concepts:

* **Single Request Batching:** Sends all selected persona definitions in a single structured Gemini API request to minimize network latency and prevent rate-limit exhaustion.
* **Structured Output Schema:** Utilizes the `@google/genai` Web SDK with JSON Schema enforcement (`responseMimeType: "application/json"`) to guarantee consistent output parsing.
* **Six-Element Prompt Engineering Framework:** Each persona prompt is constructed strictly using the 6 Prompt Card elements: *Role*, *Audience*, *Context*, *Format*, *Constraints*, and *Language*.
* **Zero External Dependencies / Single-File Build:** HTML, CSS, and modular ES JavaScript are contained inside `index.html` without external bundling tools.
* **Out-of-Scope Rule Enforcement:** Personas enforce guardrails using strict fallback logic ("I don't know") for non-career or non-technical queries.



## Defined Advisor Personas

The system provides 4 specialized advisor personas, each engineered via distinct Prompt Cards:

1. **Technical Career Counsellor:** Focuses on programming stacks, AI/ML tools, software architecture, DSA, and project portfolios.
2. **HR & Placement Counsellor:** Focuses on resume optimization, corporate hiring expectations, soft skills, and behavioral interview readiness.
3. **Academic & Research Counsellor:** Focuses on post-graduate studies (MS/M.Tech/PhD), academic research methodologies, and competitive examinations (GRE/GATE).
4. **Entrepreneurship Counsellor:** Focuses on product validation, startup incubation, commercialization, MVPs, and freelancing.



## Repository Structure

```text
.
├── index.html          # Main single-file source code (HTML, CSS, JS)
├── prompt_card.html    # Printable single-page Prompt Card specification sheet
└── README.md           # Technical documentation and execution guide