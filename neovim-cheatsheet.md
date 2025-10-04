# Neovim Cheatsheet

## Advanced Text Selection Commands

### Selecting Text Within Delimiters
- `vi` followed by an opening delimiter (e.g., `(`, `{`, `[`, `"`, `'`) selects all text within the matching delimiters (excluding the delimiters).
  - Examples: `vi(`, `vi{`, `vi[`, `vi"`, `vi'`

### Selecting Including Delimiters
- `va` followed by an opening delimiter (e.g., `(`, `{`, `[`, `"`, `'`) selects everything within the delimiters, including the delimiters themselves.
  - Examples: `va(`, `va{`, `va[`, `va"`, `va'`

### Copying (Yanking) Blocks
- `ya` followed by an opening delimiter (e.g., `(`, `{`, `[`, `"`, `'`) yanks (copies) the entire block of text, including the delimiters.
  - Examples: `ya(`, `ya{`, `ya[`, `ya"`, `ya'`

### Word Selection
- `viw`: Select the word the cursor is currently on, regardless of cursor position within the word.
- `viW`: Select the WORD (big word, including surrounding punctuation) the cursor is currently on.