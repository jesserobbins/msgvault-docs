# Claude Code Guidelines

## Writing style

- Never use em dashes (—) or en dashes (–) in documentation text. Use commas, periods, semicolons, colons, or parentheses instead. The only exception is table cells where "—" indicates "none" or "not applicable".

## Technical facts

- `msgvault delete-staged` defaults to moving messages to Gmail trash (recoverable for ~30 days); pass `--permanent` for permanent batch deletion. Remote deletion is the final, opt-in rung of the safety ladder, gated behind `MSGVAULT_ENABLE_REMOTE_DELETE=1`.
- msgvault requests full Gmail account access (not narrow/minimal scopes). Do not claim it uses restricted or read-only OAuth scopes.

## Git workflow

- Never commit directly to `main`. Always create a feature branch and open a PR.
- Never switch branches without being asked. Stay on the current branch.
- Never push to remote unless explicitly asked.
- Never force push unless explicitly asked.
