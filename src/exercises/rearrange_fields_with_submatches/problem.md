### Rearrange fields with submatches

You can capture parts of a match using parentheses `\(` and `\)` and reference them in the replacement string using `\1`, `\2`, etc.

Given this list of names in `Last, First` format:

```text
Hopper, Grace
Lovelace, Ada
Knuth, Donald
Turing, Alan
```

Transform all names to `First Last` format using capture groups:

```vim
:%s/\(\w\+\),\s*\(\w\+\)/\2 \1/g
```

Explanation:
- `\(\w\+\)` captures the first word (Last Name) into `\1`.
- `,\s*` matches the comma and following spaces.
- `\(\w\+\)` captures the second word (First Name) into `\2`.
- `\2 \1` outputs First Name followed by a space and Last Name.
