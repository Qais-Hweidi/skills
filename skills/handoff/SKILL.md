---
name: handoff
description: Create a compact, copy-ready context handoff for another AI agent to continue the current task without re-discovery.
disable-model-invocation: true
---

# Handoff

Prepare a self-contained, copy-ready handoff that another agent can use to continue the current task without the original conversation.

Capture the objective, relevant context, work already completed, important decisions and constraints, current state, verification results, unresolved issues, and next steps. Include exact paths, identifiers, commands, or errors when they will help the next agent.

Use clear paragraphs and light structure where helpful. Do not reproduce irrelevant conversation, repeat facts, expose secrets, invent missing state, or claim work was verified when it was not.

Return the handoff in a single fenced Markdown block with no commentary outside it.
