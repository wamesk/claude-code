# WAME Claude Code Plugins

A marketplace of Claude Code plugins by [WAME](https://wame.sk) — developer productivity tools for teams.

## Installation

Add the WAME marketplace:

```
/plugin marketplace add wamesk/claude-code
```

Then install any plugin:

```
/plugin install git-commits@wamesk
```

## Available Plugins

| Plugin | Description | Repo |
|--------|-------------|------|
| **git-commits** | Fetch and summarize git commits across all repositories for a date range. AI-powered summaries, file changes, project breakdown. | [wamesk/claude-code-plugin-git-commits](https://github.com/wamesk/claude-code-plugin-git-commits) |
| **laravel-docs** | Generate Laravel project documentation (technical, business, admin navigation) for individual models or modules. Auto-detects modular (`wamesk/*`, `Modules/*`) vs flat (`app/Models`) layout. Per-project config with replaceable prompts per type. | [wamesk/claude-code-plugin-laravel-docs](https://github.com/wamesk/claude-code-plugin-laravel-docs) |

## Adding a New Plugin

1. Create a new repo with your plugin (must have `.claude-plugin/plugin.json`)
2. Add an entry to `.claude-plugin/marketplace.json` in this repo
3. Push — users run `/plugin marketplace add wamesk/claude-code` to get the update

## License

MIT
