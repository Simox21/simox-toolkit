# simox-toolkit

Personal Claude Code plugin marketplace.

The `simox-toolkit` plugin has 4 agents (planner, code-reviewer, security-reviewer, build-error-resolver),
6 skills (search-first, coding-standards, verification-loop, fresh-research, evm-token-decimals, defi-amm-security)
and a SessionStart hook that only prints `ADVISOR.md`, so Claude suggests these tools when they fit
instead of running them unasked.

## Install on your computer (all local projects)

In Claude Code:

```
/plugin marketplace add Simox21/simox-toolkit
/plugin install simox-toolkit@simox-tools
```

Updates: `/plugin marketplace update simox-tools`, or turn on auto-update under Marketplaces in `/plugin`.

## Use in a repository (cloud sessions too)

Commit this to the repository's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "simox-tools": {
      "source": { "source": "github", "repo": "Simox21/simox-toolkit" }
    }
  },
  "enabledPlugins": {
    "simox-toolkit@simox-tools": true
  }
}
```

Third-party notice: `plugins/simox-toolkit/NOTICE.md`.
