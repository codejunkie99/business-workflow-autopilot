# Business Workflow Autopilot

A Claude skill that turns business operations into AI-powered workflows — sales, support, marketing, ops, finance, admin, content, and reporting — instead of bolting AI onto random tasks.

## Core stance

Most people pick a tool first, then hunt for a use case. This skill does the opposite. It starts with the workflow (input → output sequence) and only recommends tools after the architecture is clear.

- A tool does one thing.
- A workflow handles everything between input and output.
- The value is in the workflow, not the individual tool.

## What it does

Triggers on prompts like "automate my business", "build automations", "AI workflows", or tool names (n8n, Zapier, Make). Walks the user through five phases:

1. **Map the business workflows** — inventory recurring sequences and document trigger, ordered steps, tools and data, output, time cost, failure cost.
2. **Design automation architecture** — for each candidate, define trigger, input processing, AI processing, output routing, and quality check.
3. **Build the first three workflows** — Email Operations Center, Report Factory, Content Engine.
4. **Connect workflows into a system** — central event bus, loosely coupled.
5. **Monitor and improve** — success rate, processing time, quality score.

Every step is labeled:

- **Green / Automate** — predictable, rule-bound, low judgment.
- **Yellow / Assist** — AI drafts, classifies, researches, or summarizes; a human approves.
- **Red / Human** — creativity, relationships, ethics, negotiation, strategy, high-risk judgment.

The goal is not to automate everything. The goal is to automate everything that does not need the owner.

## Install

Copy `SKILL.md` into your agent's skills directory:

- Claude Code: `~/.claude/skills/business-workflow-autopilot/SKILL.md`
- agentic-stack: `.agent/skills/business-workflow-autopilot/SKILL.md`

## Deliverables produced by the skill

1. Workflow inventory table.
2. Green/yellow/red step map.
3. Top-three automation shortlist with impact, risk, and effort.
4. Architecture blueprint for each selected workflow.
5. Build plan with milestones and human approval gates.
6. Quality and monitoring plan.
7. Tooling recommendation — only after the workflow architecture is clear.

## Reference

Full skill spec: [`SKILL.md`](./SKILL.md).
