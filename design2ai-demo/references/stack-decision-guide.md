# Stack Decision Guide

Default stack:

- Frontend: Next.js
- AI integration: Vercel AI SDK when building a web app
- Default model provider: Claude API
- Alternative provider: OpenAI API
- Data: JSON/CSV first
- Database: Supabase only when persistence is needed
- Deployment: Vercel
- Versioning: GitHub

## Why This Stack

The first demo needs a visible interface, a model call, some real data, deployment, and testing. It does not need a complete CS curriculum, complex infrastructure, or production-grade auth.

## Frontend

Use Next.js when:
- The learner wants a portfolio-ready web demo
- The demo needs API routes or server actions
- The final artifact should deploy easily

Use plain HTML/CSS/JavaScript only when:
- The learner has almost no coding background
- The Week 2 goal is just a clickable shell
- The model API will be added later by another collaborator

Do not start with mobile apps, desktop apps, or browser extensions unless the user's idea truly requires that form.

## Model Provider

Use Claude API by default when:
- The user did not specify a provider
- The demo is critique, workflow, research synthesis, or long-context reasoning
- The plan is intended as a Claude Skill-adjacent public resource

Use OpenAI API when:
- The user already has OpenAI credits or project infrastructure
- Structured outputs/function calling are the central learning target
- The learner wants to compare provider behavior

Use Vercel AI SDK when:
- The app is Next.js-based
- The learner needs a practical integration layer
- Streaming, structured output, or provider switching may matter

## Data

Start with JSON/CSV when:
- There are fewer than 100 source items
- The dataset can be edited manually
- The demo does not need user accounts or saved history

Use Supabase or another database when:
- The user needs saved projects, edit history, or user-submitted records
- The data changes often
- The portfolio story benefits from showing data modeling

Use embeddings/RAG only when:
- The demo needs semantic search over source materials
- The learner can explain why keyword search is insufficient
- The source set has enough content to justify retrieval

## Deployment

Deploy by Week 5 whenever possible. A demo that only runs locally is weaker portfolio evidence.

Minimum deployment hygiene:
- API keys in environment variables
- No secrets committed to GitHub
- Basic production error message
- At least one successful and one failed request checked in logs

## Anti-Scope Rules

Avoid these in the first six weeks unless essential:
- Multi-user auth
- Payments
- Full RAG pipeline
- Vector database before real source material exists
- Multi-agent orchestration
- Complex design system work
- Model fine-tuning
- Native mobile app
- Custom backend infrastructure
