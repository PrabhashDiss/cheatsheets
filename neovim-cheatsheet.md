# Neovim Cheatsheet

## Text Selection

| Command | Description |
|---------|-------------|
| `vi` + delimiter | Select text within delimiters (excluding them). Delimiters: `(`, `{`, `[`, `"`, `'` |
| `va` + delimiter | Select text including delimiters. Delimiters: `(`, `{`, `[`, `"`, `'` |
| `ya` + delimiter | Yank (copy) text including delimiters. Delimiters: `(`, `{`, `[`, `"`, `'` |

## Word Selection
- `viw`: Select current word
- `viW`: Select current WORD (including punctuation)

## Text Change

| Command | Description |
|---------|-------------|
| `ci` + delimiter | Change text within delimiters (excluding them). Delimiters: `(`, `{`, `[`, `"`, `'` |
| `ca` + delimiter | Change text including delimiters. Delimiters: `(`, `{`, `[`, `"`, `'` |

## Word Change
- `cw`: Change current word (from cursor to end of word)
- `ciw`: Change inner word
- `caw`: Change a word (including surrounding spaces)
- `cW`: Change current WORD (including punctuation)