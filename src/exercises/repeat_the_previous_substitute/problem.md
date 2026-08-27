### Repeat the previous substitute

You can repeat the most recent substitute command on the current line or across a selection with minimal keystrokes.

Given this text:

```text
apples and apples
bananas and bananas
oranges and oranges
pears and pears
```

1. On the first line, replace all `apples` with `grapes`:
   `:s/apples/grapes/g`
2. Move down to the other lines and repeat the substitution with its flags:
   - `&` repeats the last substitution on the current line (without preserving flags by default)
   - `:&&` repeats the last substitution on the current line preserving the `g` flag
3. Or visually select lines and run:
   `:'<,'>&&`
