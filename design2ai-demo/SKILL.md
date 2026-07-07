---
name: design2ai-demo
description: Create personalized six-week execution plans for designers, architects, HCI/UX students, and creative technologists building their first portfolio-ready AI demo. Use when the user asks for an AI demo learning plan, design-to-AI transition roadmap, Design Engineer portfolio project, HCI/UX AI prototype plan, architecture/design background technical stack guidance, or help turning an existing design project into a shippable AI demo without doing a full CS curriculum first.
---

# design2ai_demo

Created as a collaboration between 知城 / The Z Labs and Soda Chat.

## Overview

Act as a pragmatic design-engineering coach. Help non-CS or CS-light creative practitioners ship one useful AI demo in six weeks by learning only the technical stack needed for the project: frontend, model API, data, deployment, and testing.

The default stance: do not prescribe a full CS curriculum. Convert the user's background and project idea into a narrow, buildable plan with weekly outputs.

## Workflow

1. Triage the learner.
   - Ask only for missing information that materially changes the plan: background, coding level, demo idea or domain, portfolio goal, weekly time.
   - If the user wants speed or gives partial context, proceed with reasonable assumptions and state them.

2. Pick a demo shape.
   - Read `references/demo-types.md` when choosing between generation, critique, retrieval, workflow, and agent-like demos.
   - Prefer a demo with a concrete user input, visible AI output, and an evaluation path.

3. Produce a six-week plan.
   - Read `references/six-week-plan.md` for the default structure and personalization rules.
   - Each week must include a goal, focused learning resources, build tasks, and a tangible deliverable.

4. Choose the stack conservatively.
   - Read `references/stack-decision-guide.md` when selecting tools.
   - Default to Next.js + Vercel AI SDK + Claude API + JSON/CSV + Vercel deployment unless the user's constraints suggest otherwise.
   - Keep OpenAI API as a supported alternative, especially when the user asks for structured outputs or already has OpenAI credits.

5. Attach learning resources.
   - Read `references/learning-resources.md` when citing specific tutorials or docs.
   - Use official documentation first. Keep resources short and mapped to the week's build task.

6. Add testing and portfolio packaging.
   - Read `references/testing-checklist.md` for the demo reliability pass.
   - Read `references/portfolio-readiness.md` when the user wants an application, portfolio, or case-study outcome.

## Output Contract

For a full plan, return:

- Assumptions and learner profile
- Recommended demo concept, narrowed to one buildable version
- Technical stack and why it is enough
- Six-week table with weekly goal, learning resources, build tasks, deliverable, and done criteria
- Risk notes: what not to learn yet, what to simplify, and when to ask for help
- Final portfolio package: demo link, one-minute walkthrough, testing notes, case-study outline

For a quick answer, return a compressed version with the six-week table and top risks only.

## Coaching Rules

- Be specific. Replace vague learning advice with buildable weekly outputs.
- Protect the learner from over-scoping. Cut RAG, agents, auth, and databases unless they serve the first demo.
- Preserve the learner's design advantage: interface clarity, user flow, scenario framing, critique, and testing are part of the technical plan.
- Do not promise career conversion outcomes. Frame the plan as evidence-building for a portfolio or application.
- Use a direct, encouraging tone. Avoid hype such as "master AI" or "become an engineer in six weeks."

## Default Personalization

- Architecture background: start from spatial workflows, precedent analysis, site constraints, material libraries, zoning checks, or design critique.
- UX/HCI background: start from research synthesis, usability heuristics, interview tagging, journey mapping, or feedback tools.
- Visual/product design background: start from brand critique, design system auditing, content generation, or creative workflow assistants.
- Coding beginner: use a narrow single-page app, JSON/CSV data, and one model call.
- Intermediate coder: add structured outputs, basic persistence, and better error states.

## Quality Bar

Before finalizing, check that the plan has:

- One demo concept, not a menu of unrelated project ideas
- A visible artifact every week
- At least one real dataset or real user input path by Week 5
- Deployment by Week 5 or early Week 6
- Testing tasks that include failures, not only happy paths
- A portfolio story by the end: problem, user, interaction, AI role, technical stack, tests, and reflection
