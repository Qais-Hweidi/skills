---
name: implement
description: Implement a requested code change from start to finish.
disable-model-invocation: true
---

# Implement

Inspect the relevant repository instructions, code, callers, and tests before editing.

Continue through minor ambiguity. Ask only when a decision would change product behavior, architecture, or scope.

Implement the requested change, then inspect a few relevant comparable implementations, starting in the repository. Search externally only when useful.

When implementation is complete, use the `code-review` skill, fix concrete findings, and rerun the affected checks.

Verify proportionally to the change. Small tasks do not require browser verification.

Report any decision made during implementation that was not previously documented or discussed and that the user might not know about.
