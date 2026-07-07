# design2ai_demo

`design2ai_demo` is a public Claude/Codex skill for designers, architects, HCI/UX students, and creative technologists who want to build their first portfolio-ready AI demo without starting from a full CS curriculum.

Created as a collaboration between **知城 / The Z Labs** and **Soda Chat**.

It turns a learner's background, coding level, project idea, portfolio goal, and weekly time budget into a focused six-week execution plan around one shippable AI demo.

## What It Helps With

- Narrowing a broad design-to-AI ambition into one buildable demo
- Choosing the right first demo type: critique, workflow, generation, retrieval, or agent-like
- Planning a six-week learning and build path
- Avoiding early over-scope such as full RAG, auth, multi-agent systems, or a complete CS curriculum
- Packaging the final demo as credible portfolio evidence

## Who It Is For

- Designers moving toward AI product or design engineering
- Architecture or spatial design students building AI-adjacent portfolio work
- HCI/UX students preparing application or job portfolio projects
- Creative technologists who want a practical first AI web demo

## Default Stack

The skill defaults to a conservative first-demo stack:

- Frontend: Next.js
- AI app layer: Vercel AI SDK
- Model provider: Claude API by default
- Alternative provider: OpenAI API
- Data: JSON/CSV before databases or RAG
- Deployment: Vercel
- Version control: GitHub

## Skill Name

The installable skill folder is `design2ai-demo` because skill metadata requires lowercase letters, digits, and hyphens. The public display name is `design2ai_demo`.

Invoke it as:

```text
Use $design2ai-demo to create a personalized six-week plan for my first portfolio-ready AI demo.
```

## Example Prompt

```text
Use $design2ai-demo to create a personalized six-week plan for my first portfolio-ready AI demo. I studied architecture, know Figma and a little HTML/CSS, and can spend 6 hours per week.
```

## Example Output Shape

The skill is designed to return:

- Assumptions and learner profile
- Recommended demo concept
- Technical stack and why it is enough
- Six-week table with weekly goals, learning resources, build tasks, deliverables, and done criteria
- What not to learn yet
- Final portfolio package checklist

## Repository Structure

```text
.
  README.md
  .gitignore
  design2ai-demo.zip
  design2ai-demo/
    SKILL.md
    agents/
      openai.yaml
    references/
      six-week-plan.md
      demo-types.md
      stack-decision-guide.md
      learning-resources.md
      testing-checklist.md
      portfolio-readiness.md
    examples/
      architecture-background.md
      ux-background.md
      hci-application.md
    evals/
      test-prompts.md
      release-check.md
```

## Installation

Use the `design2ai-demo/` folder as the installable skill package.

For local Codex-style skill usage, copy the folder into your skills directory:

```bash
cp -R design2ai-demo ~/.codex/skills/
```

Then invoke:

```text
Use $design2ai-demo to create a six-week AI demo plan for a UX designer with interview notes and basic JavaScript.
```

## Validation

This skill has passed the official `quick_validate.py` structure check:

```text
Skill is valid!
```

The package also includes `evals/test-prompts.md` for manual forward testing.

## Release Notes

Current release target:

- Public language: English
- Default audience: designers, architects, HCI/UX students, and creative technologists
- Default planning horizon: six weeks
- Default output: one portfolio-ready AI demo plan

## License

Add a license before final public release. MIT is a reasonable default if the goal is permissive reuse.
