# Skills

Portable personal skills following the [Agent Skills specification](https://agentskills.io/specification).

## Sync locally

Requires GitHub CLI 2.90.0 or newer:

```sh
./sync
```

The default targets are Claude Code and Codex. Override them when needed:

```sh
SKILLS_AGENTS="claude-code codex cursor gemini-cli" ./sync
```

Validate every skill without publishing:

```sh
gh skill publish --dry-run
```
