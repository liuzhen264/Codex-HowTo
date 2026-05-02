# Find Your Level

Do not start at chapter one by default. Start where your current capability actually is.

This assessment gives you:

- current level
- strongest areas
- weakest areas
- chapters to skip
- chapters to study next
- labs to complete

## Quick Assessment

Answer yes/no.

1. I can explain the difference between Codex CLI, Codex App, IDE integration, and cloud tasks.
2. I have used Codex inside a real repository, not only in chat.
3. I know where Codex reads `AGENTS.md` from.
4. I have written or edited an `AGENTS.md` for a project.
5. I understand approval modes, sandboxing, and when commands require confirmation.
6. I can ask Codex to inspect before editing.
7. I can make Codex run tests and summarize failures.
8. I can review Codex's diff before accepting work.
9. I have created a reusable Codex skill.
10. I have used subagents for parallel exploration or review.
11. I have configured MCP or a connector for Codex.
12. I have used browser or computer use to verify a UI.
13. I have configured hooks, rules, or memories.
14. I have packaged or installed a plugin.
15. I have set up an automation or CI-style Codex workflow.

Score:

- 0-3 yes: Level 0, Curious Starter
- 4-7 yes: Level 1, Solo Operator
- 8-10 yes: Level 2, Workflow Builder
- 11-13 yes: Level 3, Agent Orchestrator
- 14-15 yes: Level 4, Team Systems Designer

## Deep Assessment

Score each area:

- 0: I do not know this yet.
- 1: I understand the concept.
- 2: I have used it once.
- 3: I can teach or standardize it.

| Area | Score | Evidence |
| --- | --- | --- |
| CLI, App, IDE, Cloud surfaces |  |  |
| AGENTS.md and project instructions |  |  |
| config, sandbox, approvals |  |  |
| prompting, planning, inspection |  |  |
| engineering loop: edit, test, review |  |  |
| skills |  |  |
| subagents |  |  |
| MCP and connectors |  |  |
| hooks, rules, memories |  |  |
| plugins |  |  |
| browser and computer use |  |  |
| automations and team governance |  |  |

## Roadmap Rules

Use the first rule that applies.

### If AGENTS.md is below 2

Start with:

1. [02-project-instructions](02-project-instructions/README.md)
2. [03-safety-and-control](03-safety-and-control/README.md)
3. [04-engineering-loop](04-engineering-loop/README.md)

Why: Codex without project instructions is improvising.

### If safety is below 2

Start with:

1. [03-safety-and-control](03-safety-and-control/README.md)
2. `templates/config`
3. `labs/lab-03-bugfix-with-tests`

Why: autonomy without controls is not engineering.

### If engineering loop is below 2

Start with:

1. [04-engineering-loop](04-engineering-loop/README.md)
2. [11-git-github-prs](11-git-github-prs/README.md)
3. `templates/workflows/bugfix.md`

Why: the core loop is plan, inspect, edit, test, review.

### If skills and subagents are below 2

Start with:

1. [05-skills](05-skills/README.md)
2. [06-subagents](06-subagents/README.md)
3. `labs/lab-05-skill-authoring`
4. `labs/lab-06-subagent-investigation`

Why: reusable workflows and parallel work are the main productivity jump.

### If MCP, hooks, and plugins are below 2

Start with:

1. [07-mcp-and-connectors](07-mcp-and-connectors/README.md)
2. [08-hooks-rules-memories](08-hooks-rules-memories/README.md)
3. [09-plugins](09-plugins/README.md)

Why: these convert Codex from an assistant into an integrated system.

### If automations and team governance are below 2

Start with:

1. [12-automations](12-automations/README.md)
2. [13-team-adoption](13-team-adoption/README.md)
3. [14-advanced-patterns](14-advanced-patterns/README.md)

Why: team Codex requires repeatability, auditability, and ownership.

## Personalized Roadmap Template

```text
Current level:
Strongest areas:
Weakest areas:
Skip for now:
Study next:
Labs to complete:
Templates to install:
Success criteria:
Review date:
```

