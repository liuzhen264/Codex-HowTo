# Contributing

Codex HowTo is a learning system, not a loose collection of tips.

## Contribution Requirements

Every new chapter or major section should include:

- target level
- prerequisite knowledge
- when to use it
- when not to use it
- step-by-step workflow
- template or lab when possible
- success criteria
- common mistakes
- official references
- last verified date

## Version Hygiene

If you update content for a Codex feature change:

1. update [VERSION_MATRIX.md](VERSION_MATRIX.md)
2. update affected chapter metadata
3. update examples and templates
4. update quiz questions
5. record the change in [CHANGELOG_WATCH.md](CHANGELOG_WATCH.md)

## Style

Prefer concrete workflows over abstract advice.

Bad:

```text
Use Codex to improve productivity.
```

Good:

```text
Ask Codex to inspect the failing test, identify the smallest behavioral fix, edit only the relevant module, run the targeted test, then summarize the diff and residual risk.
```

