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
| **git-commit** | Turn the current working tree into one or more **logical** git commits using the `TYPE(scope): Message` convention from your global `~/.claude/CLAUDE.md`. Title and body always in English; `TYPE` and `scope` inferred from the changes. When the run is tied to a task, the task ID is appended in square brackets — `TYPE(scope)[<task-id>]: Message` — detected from `$ARGUMENTS`, `--task=<id>`, or current branch name (`feature/teamwork-task-<id>`, `task/<id>`, …). When no task ID is detected, the brackets are omitted entirely (never empty `[]`). Groups related changes into one commit each; pass `--all-in-one` to skip grouping. Never adds `Co-Authored-By` lines, never pushes, never amends. Singular `git-commit` — distinct from `git-commits` (plural) which **summarises** historical commits. | [wamesk/claude-code-plugin-git-commit](https://github.com/wamesk/claude-code-plugin-git-commit) |
| **git-commits** | Fetch and summarize git commits across all repositories for a date range. AI-powered summaries, file changes, project breakdown. | [wamesk/claude-code-plugin-git-commits](https://github.com/wamesk/claude-code-plugin-git-commits) |
| **laravel-docs** | Generate Laravel project documentation (technical, business, admin navigation) for individual models or modules. Auto-detects modular (`wamesk/*`, `Modules/*`) vs flat (`app/Models`) layout. Per-project config with replaceable prompts per type. | [wamesk/claude-code-plugin-laravel-docs](https://github.com/wamesk/claude-code-plugin-laravel-docs) |
| **teamwork-tasks-from-dnr** | Generate a Teamwork.com import-ready XLSX plus a companion Markdown plan from a "Detailný návrh riešenia" (DNR) document. LLM extraction of task lists, business-friendly task names, acceptance criteria (checkbox list), goal, and technical plan. Multi-language (`sk`/`en`/`cs`), DOCX/PDF/MD input, stdlib-only XLSX writer. Single repo serves both Claude Code (plugin) and Claude.ai (skill). | [wamesk/claude-code-plugin-teamwork-tasks-from-dnr](https://github.com/wamesk/claude-code-plugin-teamwork-tasks-from-dnr) |
| **teamwork-task** | Fetch a Teamwork.com tasklist or single task by URL (including all task comments), render a plan for approval, then implement each task in the current repository, commit per task using `TYPE(scope)[<task-id>]: Message`, and log spent time back to Teamwork via REST API v3. Parses task descriptions on the first HR into acceptance criteria + final summary. Configurable plan mode (`overview` / `per_task` / `none`), time tracking (real time rounded to 5 min, or ask) and branching (current branch or new feature branch). Persistent config — API token survives plugin updates. Push is left to the user. | [wamesk/claude-code-plugin-teamwork-task](https://github.com/wamesk/claude-code-plugin-teamwork-task) |

## Adding a New Plugin

1. Create a new repo with your plugin (must have `.claude-plugin/plugin.json`)
2. Add an entry to `.claude-plugin/marketplace.json` in this repo
3. Push — users run `/plugin marketplace add wamesk/claude-code` to get the update

## License

MIT
