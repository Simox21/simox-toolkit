# simox-toolkit: when to suggest tools

The owner may not know when an agent or skill from this plugin would help. So:

- When a situation below matches, **suggest** the tool in one line, in the owner's language: what it is and why now.
  Example: "This touches wallet keys. Run `security-reviewer`? It checks for leaked secrets and XSS."
- **Do not launch agents on your own**: each run spends usage limits. Wait for a yes.
  Skills are plain checklists: apply them right away and say so.
- At most one suggestion per reply. Do not repeat one the owner declined in this session.
- If the project's own CLAUDE.md gives different rules for these tools, follow the project.

| Situation | Suggest |
|---|---|
| Multi-file task, new feature, reworking a mechanic | agent `simox-toolkit:planner`: step-by-step plan before coding |
| Before deploying to production or merging a notable change | agent `simox-toolkit:code-reviewer` |
| Code touches wallets, keys, token contracts, auth, user input, `innerHTML`, external requests | agent `simox-toolkit:security-reviewer` |
| Build, script or deploy broke and the cause is not obvious | agent `simox-toolkit:build-error-resolver` |
| Adding a library or integration, or about to write a utility | skill `search-first` |
| Writing non-trivial code or committing security-sensitive changes | skill `coding-standards` |
| Before saying "done" on a large change | skill `verification-loop` |
| Token amounts, balances, decimals, on-chain data | skill `evm-token-decimals` |
| Smart contracts, pools, swaps, liquidity | skill `defi-amm-security` |
| Facts about outside services, prices, limits, UI, the market | skill `fresh-research` (always apply) |
