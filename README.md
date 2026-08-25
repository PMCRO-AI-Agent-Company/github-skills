# ⚙️ PMCRO GitHub Skills

Governed GitHub repository and GitHub Actions operations for the PMCR-O base and domain packs, using the connected GitHub tools as the execution surface.

## Capability pack

- **`github-ops`** — repository/tree inspection, files, branches, commits, pull requests, reviews, CI/workflow runs, Actions logs/artifacts, controlled reruns, and Agent Skills/plugin publication.

## Operating model

```text
INSPECT → PLAN → MUTATE → VERIFY → EVIDENCE
```

All repository mutations are TYPE 1. The skill must inspect current remote state and file SHAs before writes, then verify the resulting commit/PR and relevant Actions status.

## Agent Skills

The pack follows the open Agent Skills model: `SKILL.md` plus optional `scripts/`, `references/`, and `assets/`. Host-specific skill locations remain distinct; do not collapse `.agents/`, `.github/skills`, `.claude/skills`, or `.cursor/skills` into one implicit runtime.

Third-party skills are treated as supply-chain inputs and must be inspected before installation.

## GitHub Actions

Actions are part of the execution harness. The skill distinguishes source correctness from workflow correctness, deployment correctness, and PMCR-O evaluation/governance correctness. A green workflow is evidence only for the checks it actually executes.

## MCP

`assets/github-mcp-tools.json` and `references/github-mcp-catalog.md` describe the expected GitHub MCP surface. The connected GitHub tools remain authoritative; the skill must not invent unsupported tool shapes from the checked-in catalog.

## Related PMCR-O repositories

- `pmcro-runtime` — execution runtime
- `pmcro-skills` — governed marketplace and laws
- `agent-skills` — Agent Skills authoring/template base
- `dotnet-skills` — .NET domain capabilities
- `figma-skills` — Figma domain capabilities
