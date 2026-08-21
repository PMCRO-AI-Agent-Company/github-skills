# Contributing

Thanks for contributing to `pmcro-github-skills`. This repo holds the `github` plugin — GitHub
repository operations for the PMCR-O base and packs — kept working across Claude, Cursor, and
other agent runtimes that read the `.claude-plugin/`, `.agents/plugins/`, and `.cursor-plugin/`
marketplace mirrors.

## Adding a skill

1. Scaffold under `plugins/github/skills/<name>/` using `pmcro-skills`' `skill-creator` plugin.
2. Keep the root `plugin.json` (with `version`) mirrored exactly into
   `plugins/github/.codex-plugin/plugin.json`.
3. Bump `plugins/github/version.json` (Nerdbank.GitVersioning) only if the versioning scheme
   changes — the version itself is derived from git history.
4. Update all three root `marketplace.json` files if the plugin's description changes.

## Quality bar

A skill is only worth shipping if it changes a decision the model would otherwise get wrong.
Concretely:

- **Description is the router.** The `description` field is the only text the runtime sees when
  deciding whether to load a skill. Lead with an action verb, name concrete triggers (error
  messages, artifact names, quoted user requests), and exclude the nearest sibling skill.
- **Write for delta over the baseline.** Content the model already produces unaided is worth
  nothing. Encode the decision, give a concrete output contract, and state stop-conditions.
- **Scale to the input.** Don't write a 12-section skill for an 8-line task.
- **Report failures truthfully.** A skill that claims success after a failed step is worse than no
  skill.
- **State what not to do.** Boundaries prevent over-application as much as instructions enable
  correct application.

## Pull requests

- Keep changes scoped to one skill per PR where practical.
- Update all three marketplace mirrors together — a plugin missing from one runtime's catalog is a
  silent regression for that runtime's users.
