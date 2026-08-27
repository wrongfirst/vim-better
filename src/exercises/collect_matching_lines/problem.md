### Collect matching lines

Combining `:g` with `:t` (copy/transfer) or `:m` (move) allows you to aggregate lines matching a pattern to a target location.

Given this text with tasks scattered across notes:

```markdown
# Project Notes

TODO: Refactor authentication flow
Meeting notes from Tuesday...
Discussed API rate limiting.

TODO: Add unit tests for payment webhook
Architecture review notes...
Decided on Postgres index strategies.

TODO: Update documentation for API v2

---
## Summary of Action Items
```

Copy all `TODO` lines to the end of the file (`$`):

```vim
:g/TODO:/t$
```

Notice:
- `:t$` copies each matching line to the last line of the buffer.
- To move them instead of copying, use `:g/TODO:/m$`.
