# claude-code-dev-rules

A global `CLAUDE.md` with general software development rules for [Claude Code](https://claude.com/claude-code): how to ask questions, research sources, use subagents, handle Git safely, document work and build UI/UX that does not look AI-generated.

## What it covers

| Area | Examples |
|------|----------|
| Communication | confidence levels for claims, never invent facts |
| Before starting | open questions, proportional research, engineering standards, plan approval |
| Documentation | Markdown only, Mermaid diagrams, one `docs/` folder, handoff notes |
| Subagents | when to use them, model choice by cost/benefit, branches and worktrees, review of their work |
| Git and safety | no push or destructive commands without consent, consent for installs |
| Quality | verification with evidence, tests, Definition of Done, Conventional Commits |
| UI/UX | at least 3 mockups, design system, accessibility, design critique, anti-generic-UI standards |
| Proportionality | every rule scales with the project's size, complexity and risk |

The full text is in [`CLAUDE.md`](CLAUDE.md).

## Install

Copy it to your global Claude Code instructions file:

```bash
# new file
cp CLAUDE.md ~/.claude/CLAUDE.md

# you already have one: back it up and merge by hand
cp ~/.claude/CLAUDE.md ~/.claude/CLAUDE.md.bak-$(date +%Y%m%d)
```

Claude Code reads `~/.claude/CLAUDE.md` at the start of every session. A project's own `CLAUDE.md` takes precedence where it is stricter (see the "Precedence" line at the top of the file).

## Adapt before using

These rules reflect the author's preferences. Check at least:

- **Rule 1, language**: it tells Claude to talk to the user in Italian. Change it to your language.
- **Rule 9, documentation folder**: the rules use `docs/`. Change it if your projects use another name.
- **Rule 15 and 21, branching**: the rules follow the project's own branching strategy and name `develop` only as an example.
- **Rules 12 to 14, subagents and models**: the model names (Haiku, Sonnet, Opus, Fable) and the cost/benefit policy depend on the plan you have.
- **Rule 30, mockups**: requiring at least 3 mockups is a deliberate choice for UI work; remove it if it does not fit your workflow.

## License

[MIT](LICENSE)
