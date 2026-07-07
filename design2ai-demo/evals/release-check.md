# Release Check

Date: 2026-07-07

## Validation

- `quick_validate.py`: passed
- Placeholder scan: passed
- Frontmatter: name and description only
- Public language: English
- Default route: Next.js + Vercel AI SDK + Claude API + JSON/CSV + Vercel

## Manual Forward Check

Prompt:

> Use $design2ai-demo to create a six-week plan for me. I studied architecture, know Figma and a little HTML/CSS, and want a portfolio AI demo related to spatial design. I can spend 6 hours a week.

Expected output shape:

- Assumptions: architecture background, beginner coding level, 6 hours/week, portfolio goal
- Recommended demo: one scoped spatial-design workflow, such as a precedent-to-design-constraint assistant
- Stack: Next.js, Vercel AI SDK, Claude API, JSON/CSV precedent dataset, Vercel deployment
- Week 1: demo brief, 5 sample inputs, single-screen flow
- Week 2: clickable frontend shell with fake outputs
- Week 3: one live model call
- Week 4: structured output for constraints, risks, and next design moves
- Week 5: 20-50 real precedent/source records and deployment
- Week 6: 3 realistic tasks, 2 failure samples, portfolio case-study outline
- Pushback: no full CS curriculum, no RAG until real retrieval need exists

Pass criteria:

- The skill should narrow scope rather than offering many unrelated ideas.
- The plan should create a visible artifact every week.
- The plan should include deployment and failure testing.
- The plan should avoid career guarantees.
