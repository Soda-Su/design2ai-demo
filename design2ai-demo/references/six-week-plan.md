# Six-Week Plan Guide

Use this reference to generate the core plan. The plan is for a first portfolio-ready AI demo, not a comprehensive technical education.

## Intake Fields

Capture or infer:

- Background: architecture, product/visual design, UX, HCI, creative technology, other
- Coding level: none, HTML/CSS, basic JavaScript, React/Next.js, shipped web app
- Demo idea: if absent, propose one based on the user's background
- Goal: application portfolio, job portfolio, Design Engineer transition, class project, personal project
- Weekly time: 3 hours, 6-8 hours, 10+ hours
- Model/provider constraints: Claude default, OpenAI alternative, local/no-code preference if stated

## Default Six-Week Arc

### Week 1: Demo brief and scope cut

Goal: turn an interest or old design project into one AI workflow.

Learning resources:
- React Quick Start, only the concepts of components, props, state, and events
- Next.js Learn, only getting started and pages/layout basics

Build tasks:
- Define target user, concrete input, AI job, visible output, and failure mode
- Sketch the single-screen flow
- Write 5 realistic sample inputs
- Decide whether the demo is generation, critique, retrieval, workflow, or agent-like

Deliverable:
- One-page demo brief with problem, user, input, AI behavior, output, and success criteria

Done criteria:
- A stranger can understand what the demo does in 30 seconds
- The demo can be built as a single-page app
- The first version does not require login, payments, complex RAG, or multi-agent orchestration

### Week 2: Clickable frontend shell

Goal: make the workflow visible before making it smart.

Learning resources:
- React Quick Start: events and state
- Next.js Learn: routing, styling, forms, and basic project structure
- GitHub Git basics if the learner has not used version control

Build tasks:
- Create a Next.js project
- Build the input form, action button, loading state, result area, and error state
- Add 3-5 hardcoded example outputs
- Commit to GitHub

Deliverable:
- A clickable local prototype with fake AI output

Done criteria:
- The learner can run the app locally
- The interface shows what is happening before, during, and after generation
- The UI is usable enough for a first test

### Week 3: Model API connection

Goal: replace fake output with one model call.

Learning resources:
- Claude API overview and Messages API, or OpenAI API quickstart if the user chooses OpenAI
- Vercel AI SDK getting started for app integration

Build tasks:
- Add a server route or server action for the model call
- Send user input to the model
- Display the response in the UI
- Add basic loading and failure messages
- Store the API key in `.env.local`

Deliverable:
- A working AI demo that returns live model output

Done criteria:
- No API key is exposed in client code
- The app handles empty input and API failure
- The output is useful for at least 2 sample inputs

### Week 4: Structured output and guardrails

Goal: make the AI result stable enough to design around.

Learning resources:
- Claude tool use or OpenAI structured outputs/function calling
- Vercel AI SDK structured data documentation if using AI SDK

Build tasks:
- Define the output schema
- Ask the model for structured fields instead of a free-form paragraph
- Add fallback handling for malformed or incomplete output
- Add lightweight rubric or confidence notes where relevant

Deliverable:
- A stable output format that the UI can render consistently

Done criteria:
- The same input type produces the same output structure
- The UI does not break on weak output
- The learner can explain what the model is expected to produce

### Week 5: Real data and deployment

Goal: move from local prototype to shareable demo.

Learning resources:
- Vercel deployment docs
- Vercel environment variables docs
- Supabase database docs only if persistence is actually needed

Build tasks:
- Add 20-50 real source items, examples, or constraints as JSON/CSV
- Use a database only when the demo needs accounts, saved history, or editable records
- Deploy to Vercel
- Configure environment variables
- Check logs after a failed and successful run

Deliverable:
- Public demo link with real-ish data

Done criteria:
- Another person can open the demo
- Secrets are configured through environment variables
- The learner has tested at least one successful and one failed request in production

### Week 6: Testing and portfolio packaging

Goal: turn the project into credible evidence.

Learning resources:
- Review deployment logs and testing notes
- No new major technical topic unless required to fix a blocker

Build tasks:
- Run 3 realistic tasks, 2 failure samples, and 1 manual takeover scenario
- Record before/after screenshots or a one-minute walkthrough
- Fix the top 3 usability or reliability problems
- Draft the portfolio case study

Deliverable:
- Portfolio-ready package: demo link, walkthrough, testing notes, and case-study outline

Done criteria:
- The demo has a working link
- The project story explains the AI role and technical stack honestly
- Testing includes failure behavior and human override

## Time Variants

### 3 hours per week

Cut scope aggressively:
- One page
- One model call
- No database
- JSON file only
- Deployment by Week 6
- Portfolio case study can be a short write-up

### 6-8 hours per week

Use the default plan:
- One page or two pages
- Structured output
- JSON/CSV or simple database
- Deployment by Week 5
- Real testing in Week 6

### 10+ hours per week

Add only one advanced feature:
- Saved history, or
- User-editable dataset, or
- Retrieval over a small curated source set, or
- Better evaluation dashboard

Do not add all of them.

## Response Template

Use this structure:

```markdown
## Assumptions

## Recommended Demo

## Stack

## Six-Week Plan

| Week | Goal | Learning | Build Tasks | Deliverable | Done Criteria |
|---|---|---|---|---|---|

## What Not To Learn Yet

## Final Portfolio Package
```
