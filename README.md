# WAME Claude Code Plugins

A marketplace of Claude Code plugins by [WAME](https://wame.sk) — developer productivity tools for teams.

## Installation

Add the WAME marketplace:

```
/plugin marketplace add wamesk/claude-code
```

Then install any plugin:

```
/plugin install git-commits-history@wame
```

## Available Plugins

| Plugin | Description | Repo |
|--------|-------------|------|
| **git-commit** | Turns your uncommitted changes into one or more logical git commits in the `TYPE(scope): Message` format, with the task ID in brackets when one is known. Never pushes, never amends. | [wamesk/claude-code-plugin-git-commit](https://github.com/wamesk/claude-code-plugin-git-commit) |
| **git-commits-history** | Summarizes the git commit history of all your repositories (GitHub, GitLab, Bitbucket) for a date range: a timeline, AI summaries and a per-project breakdown. Renamed from `git-commits` in 2.0.0. | [wamesk/claude-code-plugin-git-commits-history](https://github.com/wamesk/claude-code-plugin-git-commits-history) |
| ~~**git-commits**~~ | **[DEPRECATED]** Renamed to `git-commits-history`. Run `/plugin uninstall git-commits@wame && /plugin install git-commits-history@wame`. Your config is kept. | [wamesk/claude-code-plugin-git-commits](https://github.com/wamesk/claude-code-plugin-git-commits) |
| **laravel-docs** | Generates technical, business and admin-navigation documentation for a Laravel model or module. Works with modular (`wamesk/*`, `Modules/*`) and flat (`app/Models`) projects. | [wamesk/claude-code-plugin-laravel-docs](https://github.com/wamesk/claude-code-plugin-laravel-docs) |
| **dnr-business** | Writes a WAME **Detailný návrh riešenia (DNR)**, the binding pre-development project document, as a branded `.docx` in sk, cs or en. Input is a folder, files, a description or the current repository. Missing client data is marked `[DOPLNIŤ]`, never invented. | [wamesk/claude-code-plugin-dnr-business](https://github.com/wamesk/claude-code-plugin-dnr-business) |
| **work-mode** | **Build fast, check once.** Fast mode builds without tests, reviews or browser checks, makes visual changes live in Chrome so you can watch and comment, and notes what it skipped; `/work-mode full` runs all the skipped checks at the end. Switch with `/work-mode` or set a default in `/config`. | [wamesk/claude-code-plugin-work-mode](https://github.com/wamesk/claude-code-plugin-work-mode) |
| **teamwork-tasks-from-dnr** | Turns a DNR document into a Teamwork.com import-ready task plan (XLSX + Markdown): tasklists and tasks with acceptance criteria, a goal, a technical plan and an estimate. | [wamesk/claude-code-plugin-teamwork-tasks-from-dnr](https://github.com/wamesk/claude-code-plugin-teamwork-tasks-from-dnr) |
| **teamwork-tasks-from-desk** | Turns a Teamwork **Desk** ticket into a Teamwork **Projects** task with subtasks, attachments and an estimate, links it to the ticket and leaves an internal note there. Never replies to the customer. | [wamesk/claude-code-plugin-teamwork-tasks-from-desk](https://github.com/wamesk/claude-code-plugin-teamwork-tasks-from-desk) |
| **teamwork-tasks-from-session** | Creates a Teamwork.com task from work you already did in a Claude Code session (its commits, diff and conversation) and logs the real session time to it. Each write needs your confirmation. | [wamesk/claude-code-plugin-teamwork-tasks-from-session](https://github.com/wamesk/claude-code-plugin-teamwork-tasks-from-session) |
| **teamwork-task-analyze** | Prepares a Teamwork.com task for development: reads everything attached to it, scans the repository, asks the open questions and rewrites the description into the WAME format with acceptance criteria, a goal, a technical plan and an estimate. Each write needs your confirmation. | [wamesk/claude-code-plugin-teamwork-task-analyze](https://github.com/wamesk/claude-code-plugin-teamwork-task-analyze) |
| **teamwork-task** | Implements a Teamwork.com task or tasklist from its URL: reads the description, comments and attachments, plans and builds each task, commits it, moves the card on the board and logs the time back to Teamwork. You push. | [wamesk/claude-code-plugin-teamwork-task](https://github.com/wamesk/claude-code-plugin-teamwork-task) |
| **teamwork-task-test** | Checks a Teamwork.com task against the code: verifies each acceptance criterion with the existing tests, a real browser or a manual scenario, reviews UI/UX, performance, security and reachability, and reports the result per criterion. Always runs full, whatever the work mode. | [wamesk/claude-code-plugin-teamwork-task-test](https://github.com/wamesk/claude-code-plugin-teamwork-task-test) |
| **laravel-agents** | Seven Laravel subagents (backend, database, API design, Pest tests, code review, security audit, performance) with the WAME coding standards as companion skills. For Nova, install `laravel-nova-agents` too. | [wamesk/claude-code-plugin-laravel-agents](https://github.com/wamesk/claude-code-plugin-laravel-agents) |
| **laravel-nova-agents** | The `laravel-nova` subagent for Laravel Nova admin panels: resources, fields, actions, lenses, filters, metrics, exports and Dusk tests, written for the installed Nova version. Install it with `laravel-agents`. | [wamesk/claude-code-plugin-laravel-nova-agents](https://github.com/wamesk/claude-code-plugin-laravel-nova-agents) |
| ~~**laravel-filament-agents**~~ | **[PLACEHOLDER]** Reserved for WAME's Filament agents and skills. Ships nothing yet. | [wamesk/claude-code-plugin-laravel-filament-agents](https://github.com/wamesk/claude-code-plugin-laravel-filament-agents) |

## Adding a New Plugin

1. Create a new repo with your plugin (must have `.claude-plugin/plugin.json`)
2. Add an entry to `.claude-plugin/marketplace.json` in this repo
3. Push — users run `/plugin marketplace add wamesk/claude-code` to get the update

## License

MIT
