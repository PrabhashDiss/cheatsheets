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

## Registers

Quick reference for registers and common workflows:

- View registers: `:registers` or `:reg`
- Yank (copy) into a specific register: `"ay` (yank into register a)
- Paste from a register: `"ap` (put contents of register a after cursor)
- Append to a register: `"Ay` (uppercase appends to register A)
- Use the yank buffer (register `0`): `"0y` (yank into register 0), useful to access the last yank even after a delete
- Delete into the black hole register (discard): `"_d` (prevents overwriting the unnamed register)
- System clipboard (X11/Wayland): `"+y` / `"+p` or `"*y` / `"*p` (use `+` for clipboard, `*` for primary selection)
- Read/write registers from command-line:
  - `:let @a = "some text"` — set register `a`
  - `:echo @a` — print register `a`

Macros
- Start/stop recording: `q{register}` (e.g., `qa` starts recording into `a`, `q` stops)
- Run a macro: `@a` (execute macro in register `a`), `@@` repeats the last executed macro

Examples
- Yank a line into register `b` and paste it below: `"byy` then move and `"bp`
- Record a simple macro that deletes a word and moves right: `qaxdwq` then run it with `@a`
