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

## Motion Commands

| Command | Description |
|---------|-------------|
| `f` + char | Find next occurrence of char on the current line |
| `F` + char | Find previous occurrence of char on the current line |
| `t` + char | Find next occurrence of char on the current line, stopping before it |
| `T` + char | Find previous occurrence of char on the current line, stopping before it |
| `r` + char | Replace the character under the cursor with char |

## Searching
- `/foo` : Search for the word "foo"
- `n` : Next occurrence
- `N` : Previous occurrence

## Substitution
Basic `%s` syntax: `:[range]s/pattern/replacement/[flags]`

- **range**: Where to apply the substitution
  - `%` : Whole file
  - `.` : Current line
  - `1,10` : Lines 1–10
- **pattern**: The word or regex to match
- **replacement**: What to replace it with
- **flags**:
  - `g` : Replace all matches on a line (global per line)
  - `c` : Confirm each replacement
