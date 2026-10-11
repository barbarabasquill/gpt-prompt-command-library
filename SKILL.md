---
name: gpt-prompt-command-library
description: Interpret reusable slash-style prompt shortcuts to produce well-structured visuals, marketing plans, executive documents, AI agent workflows, coding guidance, and research. Use when a user invokes a command such as /cheatsheet, /blueprint, /schematic, /campaignbrief, /agentblueprint, or requests a reusable prompt command.
---

# GPT Prompt Command Library

## Purpose
Translate slash-style shorthand into a clear, actionable output instruction. These are **custom prompt conventions**, not claims of built-in ChatGPT slash commands. Follow the user's actual intent and applicable tool capabilities.

## Usage
The user can enter `/command <topic and constraints>`. Identify the command in `references/commands.md`, infer a sensible output structure, and fulfill the request. When a command is ambiguous, apply the closest documented meaning; ask only if a required choice cannot be inferred.

## Workflow
1. Parse the leading `/command` (case-insensitive) and the remaining topic/constraints.
2. Look up the command in `references/commands.md`. If it is unknown, infer a likely meaning and state the interpretation only when helpful.
3. Respect audience, format, brand, scope, sources, and constraints in the request. Never override the explicit request with a default.
4. Produce the actual artifact or answer, not merely a prompt template, unless the user explicitly asks for a prompt.
5. For factual claims, distinguish verified facts from assumptions. For up-to-date claims, research when available.
6. For diagrams, use an appropriate supported representation (e.g., Mermaid, SVG, slides, or image generation where available and requested). Do not pretend a generated illustration is an editable engineering drawing.
7. For code and automation, describe access, inputs, outputs, validation, error handling, and any human approval gates as relevant.
8. Favor crisp, practical outputs with clear sections and directly usable materials.

## Default style
Professional, concise, and practical. For executive and marketing requests, prioritize goal, audience, strategy, execution, measurement, dependencies, and next actions. For technical diagrams prioritize components, connections, data flows, safeguards, and legends.

## Combining commands
Support `/onepager /campaignbrief ...` or `/schematic + /agentworkflow ...` by satisfying both where possible. If outputs conflict, prefer the more specific user instruction.

## Templates
- Executive brief: objective, business context, audience, strategy, workstreams, measures, risks, decisions.
- Campaign brief: objectives, ICP, buying committee, message, 1:1/1:few/1:many plays, channel mix, sequence, owners, KPIs, budget, governance.
- AI workflow: trigger, source systems, inputs, transformations, decision gates, human approval, output destinations, auditability, exceptions.
- Blueprint/schematic: scope, labeled components, directional connections, assumptions, legend, constraints.
- Cheatsheet: essential concepts, quick steps, examples, common pitfalls, compact reference.

## Catalog
See `references/commands.md` for the full inventory and concise definitions.
