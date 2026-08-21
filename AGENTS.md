# Repository Instructions

This repository contains a single PMCR-O plugin under `plugins/github`: GitHub repository
operations (create/update repos, push files, branches, PRs, tree inspection, pack overlay
publish) via connected GitHub MCP tools.

## Working on this plugin

Use `pmcro-skills`' `skill-creator` plugin for scaffolding new skills, agents, or MCP specs in
this repo rather than improvising a layout.

## Marketplace mirrors

Three root marketplace catalogs point at the same `plugins/github`: `.claude-plugin/marketplace.json`,
`.agents/plugins/marketplace.json`, and `.cursor-plugin/marketplace.json`. Keep the `plugins` array
in sync across all three when the plugin's description changes. The plugin mirrors its root
`plugin.json` into `.codex-plugin/plugin.json` only — it does not get its own `.claude-plugin/`
folder.
