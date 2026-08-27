### Sort lines

The `:sort` Ex command sorts lines within a range or visual selection.

Given this unordered list of fruits:

```text
Orange
Apple
Banana
Mango
Apple
Grape
Banana
```

Sort all lines alphabetically:

```vim
:%sort
```

Useful variations:
- Unique/Deduplicate while sorting:
  `:%sort u`
- Numeric sort:
  `:%sort n`
- Reverse sort:
  `:%sort!`
- Sort only a highlighted visual selection:
  `:'<,'>sort`
