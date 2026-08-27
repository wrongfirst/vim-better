### Run normal commands on matches

You can use `:g/{pattern}/normal {commands}` to execute normal mode keystrokes exclusively on lines matching a pattern.

Given this HTML list:

```html
<ul>
<li>Alpha</li>
<li>Beta</li>
<li>Gamma</li>
<li>Delta</li>
</ul>
```

Indent all `<li>` items by running normal mode `>>` on each matching line:

```vim
:g/<li>/normal >>
```

Or comment out all `return` lines in a code block:

```vim
:g/return/normal I// 
```

Notice:
- `:normal` (or `:norm`) runs the keystrokes as if typed in Normal mode.
- `:normal!` can be used if you want to bypass custom keymappings.
