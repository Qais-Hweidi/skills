# Skills

A small collection of focused skills for coding agents, following the [Agent Skills specification](https://agentskills.io/specification).

## Available skills

- `code-review` — Review changes against their intent, fix concrete problems, and verify the result.
- `explain` — Teach a concept through a throwaway interactive visual page.
- `handoff` — Prepare a compact, copy-ready handoff for another agent.
- `implement` — Implement a requested code change from start to finish.
- `interview` — Ask clarifying questions instead of assuming.
- `research` — Research software-engineering questions using current evidence.
- `spec` — Define a simple, implementation-ready specification for a requested change.

## Install

Requires GitHub CLI 2.90.0 or newer.

Install every skill, then choose the target agent(s) and scope when prompted:

```sh
gh skill install Qais-Hweidi/skills --all
```

Install one skill by name:

```sh
gh skill install Qais-Hweidi/skills spec
```

Choose user scope to make skills available across your projects. The installer supports Codex, Claude Code, Cursor, GitHub Copilot, Gemini CLI, and many other agents.

You can also ask your agent to handle installation:

```text
Help me set up agent skills from https://github.com/Qais-Hweidi/skills.

Check which skills the repository provides and which are already installed for the agent you are currently running as. Show me the available options and ask which skills I want to install or update.

After I choose, install or update only those skills at user scope. Do not overwrite skills from another source or discard local modifications without asking. Verify the result and report what changed.
```

## Update

Update installed skills to their latest versions:

```sh
gh skill update --all
```
