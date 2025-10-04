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