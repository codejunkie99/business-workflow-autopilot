---
name: business-workflow-autopilot
version: 2026-04-25
triggers: ["AI workflows", "business autopilot", "automate my business", "workflow automation", "AI operations", "build automations", "n8n", "Zapier", "Make", "automate sales", "automate support", "automate reports", "automate content"]
tools: [bash, memory_reflect]
preconditions: []
constraints: ["start with workflows, not tools", "separate automate/assist/human steps", "include quality checks before customer-facing or financial actions", "design before building", "prefer loosely coupled workflows"]
---

# Business Workflow Autopilot — turn operations into AI workflows

Use this when a business owner wants an agent to help build an AI-powered
operations system: sales, support, marketing, operations, admin, finance,
reporting, or content. The goal is not a chatbot or one-off automation; the goal
is interconnected workflows that handle execution while humans keep strategy,
relationships, judgment, and growth.

## Core stance

Most people start backwards: they pick a tool, then hunt for a use case. Do the
opposite. Start with the workflow: a repeatable sequence that transforms an
input into an output.

- A tool does one thing.
- A workflow handles everything between input and output.
- The value is in the workflow, not the individual tool.

Never recommend Claude, n8n, Zapier, Make, CRM changes, or code until the
workflow has been mapped.

## Phase 1 — Map the business workflows

Ask the owner for their recurring workflows across sales, marketing, support,
operations, finance, admin, and content. If they are vague, interview them area
by area.

For each workflow, document:

1. Trigger: what starts it.
2. Ordered steps: what happens from input to output.
3. Tools and data: inboxes, CRM, docs, files, spreadsheets, databases, Slack,
   calendars, billing systems, knowledge bases.
4. Output: what the finished work looks like.
5. Time cost: how long the step or workflow takes.
6. Failure cost: what breaks if this is wrong.

Label every step:

- Green / Automate: predictable, rule-bound, low judgment.
- Yellow / Assist: AI can draft, classify, research, summarize, or prepare, but
  a human approves.
- Red / Human: creativity, relationship awareness, ethics, negotiation,
  emotional intelligence, strategy, or high-risk judgment.

The goal is not to automate everything. The goal is to automate everything that
does not need the owner.

## Phase 2 — Design automation architecture

For every candidate workflow, design these five components before building:

1. Trigger: email, form, schedule, file, webhook, CRM event, support ticket.
2. Input processing: parse, clean, enrich, fetch context, extract text, structure
   data.
3. AI processing: classify, analyze, decide, extract, draft, summarize, generate
   documents, or route. Specify the prompt, tools, source data, and output
   schema.
4. Output routing: CRM, email draft, Slack, spreadsheet, folder, ticket system,
   accounting system, calendar, or database.
5. Quality check: validation rules, confidence thresholds, human review queues,
   escalation paths, and audit logs.

Always identify likely error points and define what happens when they occur.

## Phase 3 — Build the first three workflows

Recommend starting with the workflows that save the most time and have the
clearest input-output pattern.

### Workflow 1: Email Operations Center

Trigger: new email.

Classify and route:

- Sales inquiry: extract company, need, urgency; score against ICP; enrich; add
  to CRM; draft holding response.
- Support request: categorize, set severity, search knowledge base, draft
  response; escalate with context if no answer exists.
- Invoice or billing: extract vendor, amount, date, terms; add to payable
  tracker; flag approval thresholds.
- Internal communication: summarize, extract action items, route to owner or
  team.
- Newsletter or promo: archive or summarize only if relevant.

Quality gate: customer-facing replies queue for approval; financial extractions
above threshold require manual verification.

### Workflow 2: Report Factory

Trigger: scheduled weekly, monthly, or quarterly.

Pull data from CRM, analytics, finance, and project tools. Calculate metrics,
compare against targets and prior periods, identify trends, flag anomalies, and
write the narrative using the owner's template.

Quality gate: validate totals, percentages, and internal consistency; flag any
metric moving more than 20 percent from the prior period; require review for the
executive summary.

### Workflow 3: Content Engine

Trigger: weekly content cycle.

Generate ideas from industry trends, existing calendar, and owner notes. Let the
owner pick the best ideas. Research, outline, draft in the owner's voice, run a
self-critique pass, then repurpose into social posts, threads, newsletter
sections, and short-form video scripts.

Quality gate: human review for voice, factual accuracy, and strategic alignment.

## Phase 4 — Connect workflows into a system

After individual workflows work, connect them. Example:

Email classifies a sales inquiry -> CRM creates lead -> qualification workflow
runs -> meeting prep brief is generated -> meeting notes become action items ->
action items appear in the weekly report.

Use a central event system where workflows emit events and other workflows
listen. Visual orchestrators like n8n, Zapier, and Make are acceptable. Code,
webhooks, and queues are acceptable when more control is needed.

Design principle: keep workflows loosely coupled. Each workflow must still work
if another workflow is down. Prevent cascading failures.

## Phase 5 — Monitor and improve

Define three metrics for each workflow:

- Success rate: target 95 percent or higher.
- Processing time: trigger to completion; rising times suggest problems.
- Quality score: sample 10 percent of outputs weekly and rate correctness,
  usefulness, and edit distance.

Monthly: review the lowest-quality workflow, identify whether the issue is
prompting, tool connection, missing context, or edge cases, then fix and re-score.

Quarterly: reassess new AI capabilities, MCP servers, tools, and model features
that could improve existing workflows or unlock new ones.

## Required deliverables

When using this skill, produce:

1. Workflow inventory table.
2. Green/yellow/red step map.
3. Top-three automation shortlist with impact, risk, and effort.
4. Architecture blueprint for each selected workflow.
5. Build plan with milestones and human approval gates.
6. Quality and monitoring plan.
7. Tooling recommendation only after the workflow architecture is clear.

## Good behavior examples

If the user says, "I want AI in my business," ask about recurring workflows
before suggesting tools.

If the user asks, "Can this all be automated?", mark green/yellow/red steps and
protect human judgment steps.

If the workflow touches customers, money, legal, or reputation, include human
review or confidence thresholds before external action.

## Failure mode to avoid

Do not produce a generic list of automations. Generic automation ideas do not
help a business owner build. Always convert the owner's real operations into
workflow maps, architecture, build steps, and quality checks.

## Self-rewrite hook

After every 5 business workflow plans, or after any workflow causes bad output,
missed routing, customer-facing error, or financial mistake:
1. Review the last 5 uses of this skill.
2. Add the smallest missing checklist item that would have caught the failure.
3. Do not add new tools unless the workflow pattern requires them.
