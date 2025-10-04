# Neovim Cheatsheet

## Advanced Text Selection Commands

### Selecting Text Within Parentheses and Braces
- `vi(`: Select all text within a set of parentheses (excluding the parentheses).
- `vi{` or `vi}`: Select everything inside curly braces (excluding the braces).

### Selecting Including Delimiters
- `va{` or `va}`: Select everything within the curly braces, including the braces themselves.  

### Copying (Yanking) Blocks
- `ya{` or `ya}`: Yank (copy) the entire block of text, including the curly braces.

### Word Selection
- `viw`: Select the word the cursor is currently on, regardless of cursor position within the word.
- `viW`: Select the WORD (big word, including surrounding punctuation) the cursor is currently on.