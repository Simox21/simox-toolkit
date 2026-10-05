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

## Cloud sessions (claude.ai/code)

Cloud sessions do not install plugins, neither from your computer nor from a repository's
`.claude/settings.json`. They do load `.claude/agents/`, `.claude/skills/` and `CLAUDE.md`
committed in the repository. For a repo you work on in the cloud, copy
`plugins/simox-toolkit/agents` and `skills` into its `.claude/` and paste the table from
`ADVISOR.md` into its `CLAUDE.md` (drop the `simox-toolkit:` prefixes). Skills enabled on
your claude.ai account also load in cloud sessions.

Third-party notice: `plugins/simox-toolkit/NOTICE.md`.
