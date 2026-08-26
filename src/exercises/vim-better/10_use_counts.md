### Use count

Change this text:

```css
.blog, .news { background-image: url(/sprite.png); }
.blog { background-position: 0px 0px }
.news { background-position: 0px 0px }
```

to this:

```css
.blog, .news { background-image: url(/sprite.png); }
.blog { background-position: 0px 0px }
.news { background-position: -180px 0px }
```

Moves:

1. `yyp` to duplicate the last line
2. `cW.news<Esc>` to replace the word 'blog' with 'news'
3. `180<C-x>`

### Bonus
- `yy` and `Y` are interchangable
- `p` pastes just below and `P` pastes just above
- `w` goes to the next word respecting punctaution, `W` skips to the next words after whitespace
- `<C-x>` is a contectual completion
