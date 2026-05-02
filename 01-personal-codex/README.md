# Personal Codex

Verified with:
- Codex CLI: 0.128.0 baseline in this repository
- Codex App: current as of 2026-05-02
- Official docs checked: needs re-check before publishing externally

Target level: 0 to 1
Prerequisites: a GitHub account, a repository you are allowed to edit, and a basic understanding of Git commits and pull requests.

## What You Will Learn

You will learn how to use Codex as your personal engineering teammate across three practical surfaces:

1. local CLI work in a repository
2. web or cloud work when you do not want to keep your computer open
3. IDE or app work when you want a more visual review loop

The goal is not to memorize every button. The goal is to build a repeatable operating loop: give Codex enough context, bound its authority, inspect its plan, let it edit, verify the result, and review the diff before merging.

## When To Use This

Use personal Codex when you are working on a concrete repository and need help with:

- understanding an unfamiliar codebase
- turning a spec into implementation steps
- making small to medium code changes
- writing tests or fixing failing tests
- preparing a clean pull request
- continuing work from another device through a cloud or GitHub workflow

It is especially useful when the task can be judged by files changed, tests passing, screenshots, logs, or a pull request diff.

## When Not To Use This

Do not use personal Codex as an unsupervised replacement for engineering judgment.

Avoid giving it broad authority when:

- production credentials, patient data, customer data, or private keys are present
- the repository has no tests and the change affects critical behavior
- the task requires legal, clinical, financial, or security sign-off
- you cannot clearly describe the success criteria
- you are not willing to review the diff line by line

For risky work, first ask Codex to inspect and propose a plan only. Then decide whether to proceed.

## Mental Model

Treat Codex as a capable junior-to-mid engineering teammate with unusually high speed and unusually imperfect situational awareness.

It becomes strong when you provide four things:

- goal: what should change
- context: which files, errors, docs, examples, and constraints matter
- constraints: what must not change, what style to follow, and what safety boundaries apply
- completion criteria: how you will know the work is done

This is the basic personal Codex prompt shape:

```text
Goal:
Change or build ...

Context:
Relevant files: ...
Relevant error/log/spec: ...
Current behavior: ...
Desired behavior: ...

Constraints:
Do not touch ...
Follow ...
Ask before ...

Completion criteria:
Tests ... pass.
Behavior ... is visible.
Diff is focused.
Summarize what changed and what remains.
```

## Step By Step

### 1. Start with repository orientation

Before asking for edits, ask Codex to inspect the project.

```text
Inspect this repository first. Explain the project structure, likely tech stack, main entry points, test commands, and risks. Do not edit files yet.
```

This prevents a common failure mode: Codex starts editing before it understands where the real implementation lives.

### 2. Add or read project instructions

Look for `AGENTS.md`, README files, contribution docs, package scripts, test setup, and existing style conventions.

If no project instructions exist, create a minimal `AGENTS.md` before serious work:

```md
# AGENTS.md

## Project purpose

Describe what this project does.

## How to work

- Inspect before editing.
- Keep diffs focused.
- Prefer existing patterns over new architecture.
- Run relevant tests before reporting completion.

## Safety

- Do not commit secrets.
- Do not rewrite history unless explicitly asked.
- Ask before deleting files or changing public APIs.

## Completion

- Summarize changed files.
- Include tests run and results.
- List any remaining risks.
```

### 3. Choose the right surface

Use the CLI when you want tight local control, direct terminal feedback, and fast iteration.

Use the app or cloud task flow when your computer does not need to stay open, or when you want Codex to work from a GitHub repository and return a branch or pull request.

Use IDE integration when you want to keep your normal editor open and review changes visually while Codex assists.

The decision rule is simple: if the task needs local-only services or sensitive files, prefer local CLI. If the task can be fully represented by a GitHub repo, issue, branch, tests, and PR, cloud work is often cleaner.

### 4. Use plan-first prompts for nontrivial work

For anything larger than a tiny edit, split the work into plan, execution, and verification.

```text
Goal:
Implement the feature described in SPEC.md.

Context:
Read SPEC.md, README.md, package scripts, and the existing app structure.

Constraints:
Do not change unrelated formatting.
Do not introduce new dependencies unless necessary.
Ask before changing data models or public APIs.

First:
Inspect the repository and propose a short implementation plan.
Do not edit files until the plan is clear.
```

After reviewing the plan, continue:

```text
Proceed with the smallest implementation slice that satisfies the core user path. Keep the diff focused. Run the most relevant tests or build command. If tests cannot run, explain exactly why.
```

### 5. Keep authority bounded

Codex can read, edit, run commands, and sometimes access connected tools depending on the surface and permissions. Do not give broad permission by default.

A safe default for serious work:

- allow reading and planning freely
- allow edits inside the target repository
- require approval for dependency installation, destructive commands, migrations, publishing, deployment, or credential changes
- require a final diff summary

### 6. Verify before trust

A Codex task is not done when it says it is done. It is done when the result is checked.

Use this verification checklist:

- Did it change only relevant files?
- Did it preserve the existing architecture?
- Did it run the right tests or explain why not?
- Did it create or update tests for changed behavior?
- Did it avoid secrets and private data?
- Can you explain the diff yourself?

### 7. Finish with a reviewable handoff

Ask Codex to end every task with:

```text
Summarize:
1. What changed
2. Files changed
3. Tests run and results
4. Risks or follow-up work
5. Suggested commit message
```

This creates a clean review habit and makes the work easier to continue later.

## Copy-Paste Template

Use this for your first serious Codex task in any repo:

```text
Goal:
[Describe the feature, bugfix, refactor, or documentation change.]

Context:
- Repo purpose: [short description]
- Relevant files: [paths]
- Spec or issue: [paste or link]
- Current behavior: [what happens now]
- Desired behavior: [what should happen]

Constraints:
- Inspect before editing.
- Keep the diff focused.
- Follow existing project style.
- Do not add dependencies unless necessary.
- Do not touch secrets, deployment config, or unrelated files.
- Ask before destructive or irreversible changes.

Completion criteria:
- [Test/build/lint command] passes, or explain why it cannot run.
- The core behavior works as described.
- Final answer includes changed files, tests run, remaining risks, and suggested commit message.

First step:
Read the relevant files and propose a short plan before editing.
```

## Hands-On Lab

### Lab: make one safe documentation improvement

Choose a small repository. Ask Codex to inspect it and improve one README section.

Prompt:

```text
Inspect this repo and find one README section that could be clearer for a first-time contributor. Propose a focused edit first. After I approve, update only that section and summarize the diff.
```

Success looks like this:

- Codex reads before editing
- the proposed change is narrow
- only the README or one related doc changes
- the final summary names the changed file and the reason for the edit

### Lab: turn a spec into a first implementation slice

Use a repository with a `SPEC.md` or issue.

Prompt:

```text
Read SPEC.md and the project structure. Identify the smallest end-to-end slice that creates user-visible value. Do not implement the whole spec at once. Propose the slice, files likely affected, tests to run, and risks.
```

Then ask Codex to implement only that slice.

## Common Mistakes

The most common mistake is asking Codex to “build the whole thing” before the project has a clear instruction file, test command, and completion criteria.

Other common mistakes:

- giving vague goals without file context
- skipping the plan step for large changes
- allowing dependency installation too early
- accepting a final answer without reading the diff
- treating cloud tasks as safe just because they are not on your computer
- mixing refactor, feature work, and formatting in the same task
- not preserving your own uncommitted work before starting

## Success Criteria

You are ready to move on when you can:

- explain when to use CLI, app/cloud, or IDE workflows
- write a prompt with goal, context, constraints, and completion criteria
- ask Codex to inspect before editing
- bound permissions for risky operations
- review a Codex-generated diff before merging
- continue a task through a branch or pull request

## Quiz

1. Why should Codex inspect a repository before editing?
2. What are the four parts of a strong task prompt?
3. When should you prefer local CLI over cloud work?
4. What commands or actions should usually require approval?
5. Why is “tests passed” not the same as “safe to merge”?

## Official References

Check the current official Codex documentation before publishing or teaching exact UI steps. Codex surfaces change quickly, especially app, cloud, automations, permissions, and integrations.

For this project, update `VERSION_MATRIX.md` when behavior changes and avoid brittle UI instructions unless recently verified.
