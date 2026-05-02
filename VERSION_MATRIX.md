# Version Matrix

Codex changes quickly. This matrix records what the project currently teaches and when each surface was last checked.

Last reviewed: 2026-05-02

| Surface | Baseline | Maturity | Covered In | Notes |
| --- | --- | --- | --- | --- |
| Codex CLI | 0.128.0 | stable, fast-moving | 01, 03, 04, 06, 07, 11 | Check GitHub releases before updating commands |
| Codex App | current as of 2026-05-02 | fast-moving | 01, 10, 12 | Includes app threads, worktrees, browser, terminal, automations |
| IDE integration | current as of 2026-05-02 | fast-moving | 01, 04 | Teach workflow concepts, not brittle UI details |
| AGENTS.md | current as of 2026-05-02 | stable concept, evolving details | 02 | Includes global, project, nested, override, fallback patterns |
| Skills | current as of 2026-05-02 | evolving | 05 | Reusable workflow authoring format |
| Subagents | current as of 2026-05-02 | evolving | 06 | Built-in and custom agents |
| MCP | current as of 2026-05-02 | ecosystem-dependent | 07 | Treat as integration layer with permission risk |
| Hooks | current as of 2026-05-02 | evolving | 08 | Deterministic guardrails |
| Plugins | current as of 2026-05-02 | evolving | 09 | Distribution unit for skills, MCP, apps |
| Browser workflows | current as of 2026-05-02 | evolving | 10 | Local dev server and visual verification |
| Computer Use | current as of 2026-05-02 | experimental/fast-moving | 10 | Desktop operation; requires extra caution |
| Automations | current as of 2026-05-02 | fast-moving | 12 | Thread and project recurring tasks |
| GitHub workflows | current as of 2026-05-02 | stable patterns, tool-dependent | 11, 12 | Use connector and local Git carefully |

## Update Rules

When Codex changes:

1. update this file first
2. update affected chapter frontmatter
3. update templates only after verifying behavior
4. add a note to [CHANGELOG_WATCH.md](CHANGELOG_WATCH.md)
5. update quiz questions if behavior changed

