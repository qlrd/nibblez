# Copilot Instructions for nibblez

These instructions apply to all Copilot interactions in this
repository: code review, chat, agent tasks, and PR generation.

---

## Project summary

**nibblez** is a terminal-based ASCII snake game — a modern homage
to the classic Nibbles game, rendered entirely in ASCII art.

The project is in early development. Implementation has not begun
yet. When writing code, favour **Rust** with `crossterm` for
terminal rendering unless the maintainer specifies otherwise.

---

## Stack (planned)

| Layer | Candidate |
|-------|-----------|
| Language | Rust |
| Terminal rendering | `crossterm` |
| Build | `cargo` |
| Tests | `cargo test` |

Update this table and `CLAUDE.md` once the stack is confirmed.

---

## Commit discipline

- Follow **Conventional Commits 1.0.0**:
  `<type>[(<scope>)][!]: <description>`
- Subject line ≤ 72 characters
- Types: `feat` `fix` `docs` `style` `refactor` `perf` `test`
  `build` `ci` `chore` `revert` `init` `lore`
- `lore` is for in-world narrative commits (mascot artwork, game
  ASCII art, character descriptions) — only use in project-level
  repos, not in submissions
- Once the PR number is known, append `(#N)` to the subject line
  or add `Closes #N` / `Refs #N` in the commit body footer
- When force-pushing, always use `--force-with-lease`

---

## Code style

- Prose (comments, docs, Markdown) wraps at 72 characters
- No unnecessary dependencies — prefer stdlib where possible
- Rust: run `cargo fmt` and `cargo clippy` before every commit,
  zero warnings allowed

---

## Pull request discipline

- Open an issue before writing code for non-trivial changes
- PR description must state: what, why, how tested
- CI must be green before merging
- Merge method: **Rebase and merge**

---

## Feedback loop with @copilot

Every review comment, NACK, tACK, or concern posted in response
to a Copilot-opened PR or Copilot comment **must** address
`@copilot` directly. This notifies the agent and keeps the
review thread active.

Examples:

```
@copilot NACK — fix the off-by-one in collision detection.

@copilot tACK abc1234 — all tests pass, clippy clean.

@copilot the food spawn overlaps the snake body; fix it.
```

Do not leave review concerns as unaddressed prose. If the
concern is actionable, mention `@copilot` so the agent can
act on it.
