# Skills

Portable personal skills following the [Agent Skills specification](https://agentskills.io/specification).

## Install

Requires GitHub CLI 2.90.0 or newer. Choose the agent you use:

```sh
gh skill install Qais-Hweidi/skills research --agent codex --scope user
gh skill install Qais-Hweidi/skills research --agent claude-code --scope user
```

Update installed skills after new versions are pushed:

```sh
gh skill update research
```

Validate every skill without publishing:

```sh
gh skill publish --dry-run
```
