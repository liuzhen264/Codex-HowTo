# Quick Reference

## Default Personal Workflow

```text
1. Ask Codex to inspect.
2. Ask for a short plan.
3. Approve the plan or refine it.
4. Let Codex edit.
5. Run targeted tests.
6. Review the diff.
7. Ask for risks and follow-ups.
```

## Strong Task Prompt

```text
Inspect the code first. Then propose a short plan.
Keep the change scoped to the smallest safe surface.
Preserve unrelated user changes.
After editing, run the relevant tests and summarize the diff.
```

## Good AGENTS.md Sections

- project overview
- commands
- architecture
- coding style
- testing expectations
- safety constraints
- review expectations
- forbidden changes

## When To Use A Skill

Use a skill when:

- the workflow repeats
- there is a checklist
- the task has domain-specific rules
- the instructions are too long for a prompt

Avoid a skill when:

- the task is one-off
- the workflow is still unstable
- the instruction would become outdated quickly

## When To Use Subagents

Use subagents when:

- independent investigation can run in parallel
- review can happen while implementation continues
- large repositories require separate exploration paths

Avoid subagents when:

- the next step is blocked on a single answer
- the work is tightly coupled
- the task is small enough to do directly

