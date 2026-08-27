### Eyeball each substitution

When you want to inspect each match before replacing it, use the `c` (confirm) flag.

Given this text:

```javascript
let count = 0;
let totalCount = 100;
let counter = "not this";
let countLimit = count * 2;
```

Run interactive substitution:

```vim
:%s/count/tally/gc
```

For each match, Vim prompts you with choices:
- `y` – substitute this match
- `n` – skip this match
- `a` – substitute this match and all remaining matches
- `q` – quit substitution immediately
- `l` – substitute this match and quit (last)

Try substituting only the first and last `count` using `y` and `n`!
