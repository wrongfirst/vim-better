### Meet the substitute command

The substitute command allows us to find and replace text across a range of lines or throughout the entire file.

General syntax:
`:[range]s[ubstitute]/{pattern}/{string}/[flags]`

Given this text:

```text
The fruit of an apple tree is an apple.
Apple trees are cultivated worldwide as a fruit tree.
We love fresh apple pie and apple cider.
```

Change every occurrence of `apple` to `orange` throughout the file:

```vim
:%s/apple/orange/g
```

Notice:
- `%` specifies the entire buffer as the range.
- `s` stands for substitute.
- `g` flag makes it substitute every match on each line, rather than just the first.
