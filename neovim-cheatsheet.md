# Neovim Cheatsheet

## Text Selection

| Command | Description |
|---------|-------------|
| `vi(` | Select text within parentheses (excluding delimiters) |
| `vi{` | Select text within braces (excluding delimiters) |
| `vi[` | Select text within brackets (excluding delimiters) |
| `vi"` | Select text within double quotes (excluding delimiters) |
| `vi'` | Select text within single quotes (excluding delimiters) |
| `va(` | Select text including parentheses |
| `va{` | Select text including braces |
| `va[` | Select text including brackets |
| `va"` | Select text including double quotes |
| `va'` | Select text including single quotes |
| `ya(` | Yank (copy) text including parentheses |
| `ya{` | Yank text including braces |
| `ya[` | Yank text including brackets |
| `ya"` | Yank text including double quotes |
| `ya'` | Yank text including single quotes |

## Word Selection
- `viw`: Select current word
- `viW`: Select current WORD (including punctuation)