---
name: github-mcp
description: >-
  Configure and govern the GitHub MCP server for IDEs, Copilot, or agent
  runtimes. Use when selecting remote/local transport, toolsets, authentication,
  and least-privilege access.
---

# GitHub MCP

The current remote GitHub MCP endpoint is `https://api.githubcopilot.com/mcp/`. OAuth is preferred where the host supports it; PAT-based configurations must keep credentials in secret storage.

## Tool governance

- Prefer explicit tool allowlists for autonomous environments.
- For repository Copilot MCP configuration, GitHub requires an `mcpServers` object and supports `tools`, `type`, `url`, and headers/environment substitutions.
- Repository-level MCP access can be autonomous; do not assume user approval will appear at invocation time.
- Keep write-capable toolsets disabled unless the workflow explicitly needs them.

## PMCRO

MCP connectivity is capability, not authorization. `github-ops` and PMCRO policies determine when a GitHub mutation is allowed and what evidence is retained.
