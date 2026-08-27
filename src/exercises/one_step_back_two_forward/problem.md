### One step back, two forward

Change this text:

```javascript
var foo = "method(" + argument1 + "," + argument2 + ")";
```

to this:

```javascript
var foo = "method(" + argument1 + "," + argument2 + ")";
```

Steps:

1. find "+" with `f+` (NOTE: For this to work you will have to be on the line to be changed)
2. delete and switch to insert mode with `s`
3. Type ` + `
4. Leave insert mode
5. find the next "+" with `;`
6. Repeat with `.`

### Bonus
- Similar to `s` for deleting one character and switching to Insert mode, in viusal mode, you can use `c` to delete a block and enter Insert mode
- Since `f` only searches on a given line, to search the entire file use `/` in command mode, followed by the term to search (eg `/foo` will search for `foo` in the file) and hit `Enter`. Once the term is term is found, you can navigate to the next instance using `n` or the previous instance using `N`
