---
name: code-review
description: Review the change against the spec, fix what's wrong, verify.
disable-model-invocation: true
---

# Code Review

Run after implementing. Find the problems, fix them, prove the change still does what was asked.

1. Scope it. Take everything this branch changed since it left its base, including work not yet committed. An argument, such as a branch, commit, path, or pull request, replaces that base. Read the whole function around each change, not only the changed lines.

2. Recover the intent. The request in this conversation, the linked issue, the plan or spec file. State it in one line. Ask if you cannot find it.

3. Send one agent per area below, all in a single message so they run in parallel. Give each the change, the intent, and its area. Each returns findings as file, line, a one-line summary, and the concrete cost. Keep the areas apart, because a clean result in one does not excuse a failure in another.
   - Intent: missing requirements, silent scope creep, behavior that drifted from the request, invariants that were deleted and never re-established.
   - Correctness: edge cases, empty and boundary values, error paths, every caller and callee of a changed signature, state that can go stale, swallowed errors.
   - Security: untrusted input crossing a boundary unvalidated, injection through concatenated queries or commands, secrets in code or logs, missing authentication and authorization checks, unescaped output, unsafe deserialization, permissive defaults.
   - Performance: N+1 queries, unbounded loops or fetches, repeated I/O and recomputation, independent work run sequentially, blocking work added to startup or a hot path, large objects kept alive by closures.
   - Structure: logic an existing helper already covers, near-duplicates, new conditionals bolted onto unrelated flows, feature logic in shared modules, deep nesting, dead code left behind.

4. Wait for all of them, merge findings that point at the same line or mechanism, then fix each one at the right depth. Generalize the mechanism instead of special-casing it, delete the near-duplicate instead of polishing it. Skip a finding only when the fix would change intended behavior, reach well outside the change, or you judge it a false positive, and say which and why. Ask before deleting anything you are not certain is unused.

5. Verify. Run the tests and the build. Report the intent, what you fixed, what you skipped, and whether the change now matches. Say plainly when something still fails.
