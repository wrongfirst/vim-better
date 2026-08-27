### Reuse the last search pattern

Leaving the search pattern empty in a substitute command tells Vim to automatically reuse the most recent search pattern.

Given this text:

```text
The pragmatic programmer practices pragmatic thinking to build pragmatic software.
```

Instead of retyping a search pattern into `:s`, follow this workflow:

1. Search for the target word using `/`:
   `/pragmatic<CR>`
2. Test and navigate through the matches using `n` and `N`.
3. Once satisfied with the search matches, execute substitute with an empty pattern:
   `:%s//practical/g`

Vim will substitute all occurrences of `pragmatic` with `practical`.
