# Learning Roadmap

This roadmap teaches Codex as an engineering operating system.

Principles:

- project instructions before advanced automation
- safety before autonomy
- repeatable workflows before clever prompting
- verification before trust
- team conventions before team scale

## Level 0: Curious Starter

Best for:

- you have heard of Codex but have not used it seriously in a repository
- you mostly ask one-off prompts
- you are unsure what Codex can read, edit, and run

Study:

1. [00-orientation](00-orientation/README.md)
2. [01-personal-codex](01-personal-codex/README.md)
3. [02-project-instructions](02-project-instructions/README.md)

Practice:

- `labs/lab-01-first-codex-session`
- create your first `AGENTS.md`
- ask Codex to inspect a repo before editing

Success criteria:

- you can explain the main Codex surfaces
- you can start Codex in a repo
- you can identify active project instructions
- you can make a small edit and review the diff

## Level 1: Solo Operator

Best for:

- you use Codex for daily coding
- you need safer edits, testing, review, and Git hygiene

Study:

1. [03-safety-and-control](03-safety-and-control/README.md)
2. [04-engineering-loop](04-engineering-loop/README.md)
3. [11-git-github-prs](11-git-github-prs/README.md)

Practice:

- `labs/lab-03-bugfix-with-tests`
- `templates/workflows/bugfix.md`
- `templates/workflows/code-review.md`

Success criteria:

- you choose the right approval mode for a task
- you can ask Codex to plan, inspect, edit, test, and review
- you can separate your edits from unrelated dirty worktree changes
- you can produce a clean commit or PR summary

## Level 2: Workflow Builder

Best for:

- you repeat the same Codex instructions often
- you want reliable workflows, not one-off prompts
- you work on docs, tests, frontend, reviews, or refactors repeatedly

Study:

1. [05-skills](05-skills/README.md)
2. [10-browser-and-computer-use](10-browser-and-computer-use/README.md)
3. [15-case-studies](15-case-studies/README.md)

Practice:

- `labs/lab-05-skill-authoring`
- `labs/lab-08-frontend-browser-verification`
- create a skill for one repeated task in your own repo

Success criteria:

- you can decide when a skill is worth writing
- you can write a `SKILL.md`
- you can use a lab to verify real output
- you can turn a repeated prompt into a reusable workflow

## Level 3: Agent Orchestrator

Best for:

- your tasks require parallel exploration, review, or verification
- you need external context through MCP/connectors
- you want deterministic guardrails through hooks

Study:

1. [06-subagents](06-subagents/README.md)
2. [07-mcp-and-connectors](07-mcp-and-connectors/README.md)
3. [08-hooks-rules-memories](08-hooks-rules-memories/README.md)
4. [09-plugins](09-plugins/README.md)

Practice:

- `labs/lab-06-subagent-investigation`
- `labs/lab-07-mcp-connected-workflow`
- package one workflow as a plugin

Success criteria:

- you can split work between explorer, worker, reviewer, and verifier agents
- you can connect Codex to needed context without overexposing data
- you can design a hook that enforces a deterministic rule
- you can explain the difference between a skill and a plugin

## Level 4: Team Systems Designer

Best for:

- you want Codex to work consistently across a team
- you need recurring tasks, repository briefings, PR review workflows, or governance
- you care about onboarding, auditability, and safety

Study:

1. [12-automations](12-automations/README.md)
2. [13-team-adoption](13-team-adoption/README.md)
3. [14-advanced-patterns](14-advanced-patterns/README.md)

Practice:

- `labs/lab-09-automation-review-loop`
- `labs/lab-10-team-codex-rollout`
- create a team `AGENTS.md` and rollout checklist

Success criteria:

- you can define team-level instruction hierarchy
- you can create recurring Codex tasks with clear outputs
- you can define permissions and review gates
- you can maintain a Codex workflow library over time

