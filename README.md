# Skills

Portable personal skills following the [Agent Skills specification](https://agentskills.io/specification).

## Install

Requires GitHub CLI 2.90.0 or newer. Install every skill, then choose the target agent(s) and scope when prompted:

```sh
gh skill install Qais-Hweidi/skills --all
```

Or copy this prompt into your agent:

```text
Help me set up agent skills from https://github.com/Qais-Hweidi/skills.

Check which skills the repository provides and which are already installed for the agent you are currently running as. Show me the available options and ask which skills I want to install or update.

After I choose, install or update only those skills at user scope. Do not overwrite skills from another source or discard local modifications without asking. Verify the result and report what changed.
```

Update every installed skill after new versions are pushed:

```sh
gh skill update --all
```

Validate every skill without publishing:

```sh
gh skill publish --dry-run
```
