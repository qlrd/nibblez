# CLAUDE.md

Instructions for Claude Code when working in this repository.

## Project summary

**nibblez** is a terminal-based ASCII snake game — a modern homage
to the classic Nibbles game, rendered entirely in ASCII art.

The project is in early development. The language and toolchain
have not been decided yet. This file will be updated as the stack
is chosen.

---

## Build

> To be filled in once the language and toolchain are decided.

---

## Test

> To be filled in once the test framework is decided.

All tests must pass before committing.

---

## Project layout

```
nibblez/
├── README.md            project overview and gameplay instructions
├── CHANGELOG.md         keep-a-changelog format
├── CONTRIBUTING.md      contribution guidelines
├── CODE_OF_CONDUCT.md   contributor covenant v2.1
├── SECURITY.md          vulnerability reporting policy
├── CLAUDE.md            this file
├── LICENSE              MIT
└── .github/
    └── copilot-instructions.md   Copilot agent instructions
```

Source directories and their structure will be added here once
the implementation begins.

---

## Conventions

- Commit messages follow **Conventional Commits 1.0.0**
- Subject line must not exceed 72 characters
- Prose (comments, docs, Markdown) wraps at 72 characters
- No unnecessary dependencies — prefer stdlib where possible

## Commit message format

```
<type>[(<scope>)][!]: <description>
```

Types: `feat` `fix` `docs` `style` `refactor` `perf` `test`
`build` `ci` `chore` `revert` `init` `lore`

`lore` is for in-world narrative commits (mascot artwork, game
lore, ASCII art). It is not standard CC 1.0.0 — only use it in
project-level repositories.

---

## Key design decisions

> To be documented as implementation begins.

Candidate language: **Rust** (fits the author's other terminal
tooling in this org).

Candidate rendering approach: raw terminal escape codes via a
minimal crate (e.g. `crossterm`) — no heavy TUI framework unless
needed.
