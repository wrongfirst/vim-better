### Delete matching lines

The `:global` (or `:g`) command executes an Ex command on all lines that match a regular expression.

General syntax:
`:[range]g/{pattern}/[cmd]`

Given this file with interspersed debug statements:

```javascript
function calculateTotal(items) {
  console.log("Starting calculation...");
  let total = 0;
  for (const item of items) {
    console.log("Processing item:", item);
    total += item.price;
  }
  console.log("Finished:", total);
  return total;
}
```

Delete all `console.log` lines across the file in a single command:

```vim
:g/console\.log/d
```

Notice:
- `g` runs across the entire file.
- `/console\.log/` is the search pattern.
- `d` is the delete command executed on each matching line.

You can also delete all empty lines in a file with:
`:g/^$/d`
