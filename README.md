# Codex HowTo

Master Codex as an engineering teammate, not just a coding chatbot.

Codex is no longer only a local CLI that edits code. It now spans CLI, the Codex app, IDE integrations, cloud tasks, AGENTS.md, skills, subagents, MCP, hooks, plugins, automations, browser workflows, computer use, GitHub work, and team governance.

This project is a complete learning system for that new Codex world.

## Start Here

### 1. Find Your Level

Take the written assessment in [FIND-YOUR-LEVEL.md](FIND-YOUR-LEVEL.md), or run the bundled Codex skill once this repository is installed in your Codex environment:

```text
codex-self-assessment
```

You will get a personalized roadmap based on what you already know.

### 2. Follow Your Roadmap

Use [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md) to move through five levels:

| Level | Identity | You are ready to learn |
| --- | --- | --- |
| 0 | Curious Starter | What Codex can do and how to stay safe |
| 1 | Solo Operator | Daily coding with CLI, app, IDE, AGENTS.md, approvals, tests |
| 2 | Workflow Builder | Skills, reusable playbooks, browser verification, review loops |
| 3 | Agent Orchestrator | Subagents, custom agents, MCP, hooks, plugins, computer use |
| 4 | Team Systems Designer | Automations, GitHub workflows, governance, team rollout |

### 3. Learn By Doing

Every chapter follows the same structure:

- what you will learn
- when to use it
- when not to use it
- mental model
- step-by-step workflow
- copy-paste template
- hands-on lab
- common mistakes
- success criteria
- quiz
- official references
- last verified date

### 4. Build Your Codex System

The repository includes:

- project instruction templates for `AGENTS.md`
- reusable skills
- subagent definitions
- MCP configuration patterns
- hook and automation examples
- GitHub and PR workflows
- frontend browser verification workflows
- team adoption playbooks
- quizzes and scoring rubrics

### 5. Stay Current

Codex changes quickly. Start with [VERSION_MATRIX.md](VERSION_MATRIX.md) and [CHANGELOG_WATCH.md](CHANGELOG_WATCH.md) before assuming any chapter is current.

Current baseline:

- Last reviewed: 2026-05-02
- Codex CLI baseline: 0.128.0
- Tracked surfaces: CLI, App, IDE, Cloud, GitHub, MCP, Skills, Subagents, Plugins, Automations

## Project Map

| Area | Purpose |
| --- | --- |
| [00-orientation](00-orientation/README.md) | Understand the Codex operating system |
| [01-personal-codex](01-personal-codex/README.md) | Install, run, configure, and control Codex |
| [02-project-instructions](02-project-instructions/README.md) | Teach Codex your project with AGENTS.md |
| [03-safety-and-control](03-safety-and-control/README.md) | Sandbox, approvals, permissions, and risky actions |
| [04-engineering-loop](04-engineering-loop/README.md) | Plan, inspect, edit, test, review, commit |
| [05-skills](05-skills/README.md) | Turn repeated expertise into reusable workflows |
| [06-subagents](06-subagents/README.md) | Parallel exploration, review, verification, and execution |
| [07-mcp-and-connectors](07-mcp-and-connectors/README.md) | Connect Codex to external tools and context |
| [08-hooks-rules-memories](08-hooks-rules-memories/README.md) | Deterministic guardrails and durable preferences |
| [09-plugins](09-plugins/README.md) | Package skills, MCP, and apps for distribution |
| [10-browser-and-computer-use](10-browser-and-computer-use/README.md) | Visual verification and desktop/browser workflows |
| [11-git-github-prs](11-git-github-prs/README.md) | Branches, commits, PRs, reviews, CI fixes |
| [12-automations](12-automations/README.md) | Recurring and background Codex work |
| [13-team-adoption](13-team-adoption/README.md) | Roll Codex out to a team responsibly |
| [14-advanced-patterns](14-advanced-patterns/README.md) | Large repos, long tasks, multi-agent systems |
| [15-case-studies](15-case-studies/README.md) | End-to-end examples |

## Philosophy

Codex is strongest when you give it:

1. clear project instructions
2. bounded authority
3. repeatable workflows
4. verifiable outputs
5. feedback loops
6. team-level conventions

This project teaches those six habits.

## Not A Feature Dump

This repository is intentionally not an awesome list. Feature catalogs age quickly. Workflows, diagnostics, and learning paths age more gracefully when they are kept tied to version checks and official references.

Use [FEATURE_CATALOG.md](FEATURE_CATALOG.md) when you need the map. Use [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md) when you want to become capable.

## Contributing

Contributions are welcome, but every contribution must preserve the learning-system shape:

- include a level target
- include success criteria
- include a template or lab when possible
- include last verified date and official references
- explain when not to use the feature

See [CONTRIBUTING.md](CONTRIBUTING.md) and [STYLE_GUIDE.md](STYLE_GUIDE.md).

