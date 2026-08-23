---
name: code-review
description: Review a code change against its intent, fix concrete problems, and verify the result.
disable-model-invocation: true
---

# Code Review

Review the change against what was asked, fix real problems, and verify the result.

Use the branch, commit, path, or pull request the user gives. Otherwise review uncommitted work and everything the branch changed from its base. Read the surrounding code, affected callers, and tests, not only the diff.

Recover the intent from the conversation, linked issue, plan, or spec. Ask only when it cannot be established.

Spawn a separate subagent for each review area. Give each the intent, the change, and the relevant surrounding code. Run them in parallel when possible. They review only and return concrete findings with file, line, and impact; the main agent validates, deduplicates, and fixes them.

- Intent: mismatched requirements, missing behavior, and scope creep.
- Correctness: edge cases, error paths, stale state, and broken contracts.
- Security: missing validation or authorization, injection, leaked secrets, and unsafe defaults.
- Performance: unbounded work, repeated I/O or computation, and hot-path regressions.
- Structure: needless duplication, complexity, dead code, and misplaced responsibilities.

Focus on concrete impact, not cosmetic preferences.

Fix in-scope findings at their root cause. Ask before changing intended behavior or deleting code that may still be used. Do not expand the task to unrelated cleanup.

Run the relevant tests, build, and checks. Report what you found and fixed with file and line references, what you skipped and why, verification results, and anything that still fails. State plainly when the change does not match its intent.
