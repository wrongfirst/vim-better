### Filter and keep matching lines

The `:vglobal` (or `:v` / `:g!`) command executes an Ex command on all lines that do NOT match the given pattern.

General syntax:
`:[range]v/{pattern}/[cmd]`

Given this mixed log output:

```text
[INFO] Application starting...
[DEBUG] Initializing cache
[ERROR] Database connection failed
[INFO] Retrying connection...
[ERROR] Timeout reached on port 5432
[DEBUG] Releasing pool resources
```

Keep only the `[ERROR]` lines and remove everything else:

```vim
:v/\[ERROR\]/d
```

Notice:
- `:v/pattern/d` deletes every line that does *not* contain `[ERROR]`.
- Alternatively, `:g!/\[ERROR\]/d` accomplishes the exact same result.
