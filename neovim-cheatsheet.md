# Neovim Cheatsheet

This cheatsheet is organized into three categories: Command, Count, and Motion.

## Command

| Command | Description |
|---------|-------------|
| `vi` + delimiter | Select text within delimiters (excluding them). Delimiters: `(`, `{`, `[`, `"`, `'` |
| `va` + delimiter | Select text including delimiters. Delimiters: `(`, `{`, `[`, `"`, `'` |
| `ya` + delimiter | Yank (copy) text including delimiters. Delimiters: `(`, `{`, `[`, `"`, `'` |
| `ci` + delimiter | Change text within delimiters (excluding them). |
| `ca` + delimiter | Change text including delimiters. |
| `cw` | Change current word (from cursor to end of word) |
| `ciw` | Change inner word |
| `caw` | Change a word (including surrounding spaces) |
| `cW` | Change current WORD (including punctuation) |
| `f` + char | Find next occurrence of char on the current line |
| `F` + char | Find previous occurrence of char on the current line |
| `t` + char | Find next occurrence of char on the current line, stopping before it |
| `T` + char | Find previous occurrence of char on the current line, stopping before it |
| `r` + char | Replace the character under the cursor with char |
| `/pattern` | Search forward for pattern |
| `n` | Jump to next search match |
| `N` | Jump to previous search match |
| `:%s/pat/repl/gc` | Substitute with confirmation (example) |
| `:reg` | Show registers |
| `"ay` | Yank into register a |
| `"ap` | Paste from register a |
| `"_d` | Delete into black hole register (discard) |
| `"+y` / `"+p` | Use system clipboard |
| `q{reg}` / `q` | Start/stop macro recording |
| `@{reg}` | Execute macro in register |
| `zz` | Center the current line in the window |
| `C-o` | Jump to previous cursor position |
| `==` | Auto-indent the current line |
| `=ap` | Re-indent a paragraph/object |
| `dap` | Delete a paragraph (a paragraph object) |
| `*` | Search forward for word under cursor |
| `o` (in Visual mode) | Move cursor to other end of visual selection (useful with v and V selections) |
| `o` | Open a new line below and enter insert mode |
| `O` | Open a new line above and enter insert mode |
| `i` | Insert before cursor |
| `I` | Insert at first non-blank of the line |
| `a` | Append after cursor |
| `A` | Append at end of line |
| `%` | Jump to matching bracket/parenthesis |
| `,` and `;` | Repeat f/t search backwards/forwards respectively (`,` repeats in opposite direction; `;` repeats in same direction) |

## Count

| Count form | Description |
|------------|-------------|
| `N{cmd}` | Repeat command `{cmd}` N times. Example: `3dw` deletes 3 words. |
| `.` | Repeat last change (dot command) |

## Motion

| Motion | Description |
|--------|-------------|
| `w`, `e`, `b` | Word motions (forward to start/end, backward) |
| `W` | WORD motion (moves forward to start of next WORD, treats punctuation as part of word) |
| `iw`, `aw` | inner/around word text objects |
| `ip`, `ap` | inner/around paragraph text objects |
| `%` | Move to matching delimiter (also listed in Command) |
| `_` | Move to first non-blank of line (line motion) |
| `$` | Move to end of line |
| `C-d` | Scroll half-page down (Ctrl-d) |
| `C-u` | Scroll half-page up (Ctrl-u) |
| `,` and `;` | Repeat f/t motions (see Command) |

## Examples and quick tips

- Yank a line into register `b` and paste it below: `"byy` then move and `"bp`
- Record a simple macro that deletes a word and moves right: `qaxdwq` then run it with `@a`


```

## LSP key mappings

| Key | LSP action |
|-----|------------|
| `g r a` | LSP: [G]loto Code [A]ction |
| `g r d` | LSP: [G]oto [D]efinition |
| `g r D` | LSP: [G]oto [D]eclaration |
| `g r i` | LSP: [G]oto [I]mplementation |
| `g r r` | LSP: [G]oto [R]eferences |
| `g r n` | LSP: [R]e[n]ame |
| `g r t` | LSP: [G]oto [T]ype Definition |

```

