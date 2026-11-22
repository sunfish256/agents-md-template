# AGENTS.md Template

A general-purpose `AGENTS.md` for projects where AI coding agents (Codex, Claude Code, etc.) do analysis, document, or code work over multiple sessions.

It sets three kinds of ground rules:

| Section | What it covers |
|---|---|
| **Continuity Across Sessions** | Keeping a short, current `SESSION_HANDOFF.md` snapshot instead of a growing log, so the next session can pick up where the last one stopped |
| **File Organization** | Default folders (`deliverables/`, `data/`, `scripts/`, `src/`, `tests/`, `docs/`, `work/`) and what belongs in each, especially what counts as a deliverable |
| **Routine Upkeep** | Reusing existing files before creating new ones, keeping changes consistent, and tidying up only what the task touched |

## Usage

1. Copy [`AGENTS.md`](AGENTS.md) to the root of your project.
2. Adjust anything that doesn't fit your project. Existing project structure and explicit instructions take precedence over these defaults.

For tools that read a different instruction file, point that file at this one. For example, in Claude Code's `CLAUDE.md`:

```markdown
@AGENTS.md
```

Tip: on Windows, you can register a folder containing `AGENTS.md` as a [PowerToys New+](https://learn.microsoft.com/windows/powertoys/newplus) template to drop it into new projects from the context menu.

## License

[MIT](LICENSE)
