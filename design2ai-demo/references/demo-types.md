# Demo Types

Use this guide to choose one buildable AI demo type. Pick the smallest version that creates portfolio evidence.

## Generation Demo

Use when the learner wants to create copy, concepts, layouts, prompts, visual directions, or design variants.

Good first demos:
- Brand voice draft assistant
- Moodboard caption generator
- Design concept option generator
- UX microcopy helper

Stack:
- Form input
- Model call
- Structured output
- Optional JSON examples

Risk:
- Output can feel like generic prompting. Add constraints, examples, and before/after framing.

## Critique Demo

Use when the learner has design judgment and wants the AI to evaluate an artifact, brief, user flow, or portfolio page.

Good first demos:
- Portfolio case-study critique
- Landing page UX heuristic review
- Architecture concept review against constraints
- Research-plan feedback tool

Stack:
- Text or screenshot input
- Rubric prompt
- Structured scores and comments
- Optional model vision if images are central

Risk:
- Critique can become vague. Require specific evidence, severity, and next action.

## Retrieval Demo

Use when the project needs to answer from a small curated body of material.

Good first demos:
- Precedent finder over 30 architecture examples
- Research insight finder over interview notes
- Policy or program FAQ assistant

Stack:
- Start with JSON/CSV and simple search/filter
- Add embeddings/RAG only when keyword search fails
- Render citations or source snippets

Risk:
- Beginners overbuild RAG. For the first demo, a curated JSON search is often enough.

## Workflow Demo

Use when the demo transforms a real design workflow step by step.

Good first demos:
- Interview notes to insight clusters
- Project brief to feature checklist
- Site constraints to design prompts
- Design system audit to prioritized fixes

Stack:
- Multi-step UI
- One or two model calls
- Structured intermediate outputs
- Review/edit step before final result

Risk:
- Scope creep. Keep to one workflow and one primary user.

## Agent-Like Demo

Use only for intermediate learners or when tool use is essential.

Good first demos:
- Checks a brief, asks one follow-up, then creates a task list
- Reads a small dataset and recommends next steps
- Runs a simple tool call such as date, calculator, or source lookup

Stack:
- Model API
- Tool/function calling
- Strict output schema
- Clear stop condition

Risk:
- Agent demos can hide weak product thinking. Make the UI, state, and fallback path explicit.

## Selection Rule

If the user is a beginner, prefer:
1. Critique demo
2. Workflow demo
3. Generation demo with strong constraints
4. Retrieval demo with JSON/CSV
5. Agent-like demo only after the basics work
