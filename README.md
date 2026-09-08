# AI Career Counsellor - Persona-Based Web Application

## Problem Statement & Objective
Students often get one-dimensional career advice. This project provides multi-perspective guidance using an AI Career Counsellor web app powered by the Google Gemini API (`gemini-2.5-flash`). Users can query single or multiple advisor personas simultaneously to receive customized, domain-specific insights.

## Features
- **4 Custom Personas:** Technical, HR & Placement, Academic, and Entrepreneurship Counsellors.
- **Single Request Batching:** Sends all selected persona instructions in a single structured Gemini API request using JSON schema outputs.
- **Prompt Card Architecture:** Built using standard 6-element Prompt Cards (Role, Audience, Context, Format, Constraints, Language).
- **Comparative Analysis Matrix:** Dynamically generates a summary comparison table when multiple personas are queried.
- **Zero API Key Exposure:** API Key is entered via a client UI input field and never hardcoded or committed to git.

## Prompt Card Architecture (Example)
| Element | Description |
| :--- | :--- |
| **Role** | Senior Technical Career Counsellor |
| **Audience** | ICT / Computer Science Undergraduate Students |
| **Context** | Evaluating technical tools, skills, projects, and career choices |
| **Format** | Bulleted Technical Focus, Required Projects, Immediate Action |
| **Constraints** | Realistic advice, no job guarantees, return "I don't know" if out-of-scope |
| **Language** | Clear, simple English |

## How to Run
1. Clone the repository.
2. Open `index.html` directly in any modern Web Browser (Chrome, Edge, Firefox).
3. Enter your Google Gemini API key into the input field.
4. Select one or more personas, type a career question, and click **Get Career Advice**.

## Sample Test Questions
1. *Should I prepare for campus placements or pursue higher studies?*
2. *I know Python and basic Machine Learning. What projects should I build to stand out?*
3. *Should I become an AI Engineer, Data Scientist, or Software Developer?*