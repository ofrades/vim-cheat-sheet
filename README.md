<h2 align="center"><img src="https://raw.githubusercontent.com/VSCodeVim/Vim/master/images/icon.png" height="128"><br>VSCodeVim</h2>
<p align="center"><strong>Vim Cheat Sheet for Visual Studio Code</strong></p>

<strong>Table of Contents</strong>

- [Getting Started](#GettingStarted)
  - [Navigating](#Navigating)
  - [Words](#Words)
  - [Line](#Line)
  - [Character](#Character) 
  - [Document](#Document)
  - [Window](#Window)
  - [Tab Pages](#TabPages)
  - [Editing](#Editing)
  - [Exiting Insert Mode](#ExitingInsertMode)
  - [Clipboard](#Clipboard)
- [Visual Mode](#VisualMode)
  - [In Visual Mode](#InVisualMode)
  - [Operators](#Operators)
  - [Operators List](#OperatorsList)
  - [Operators Examples](#OperatorsExamples)
  - [Text Objects](#TextObjects)
  - [TextObjectsUsageExamples](#TextObjectsExamples)
- [Folds](#Folds)
- [Advanced Navigation](#AdvancedNavigation)
- [Jumping](#Jumping)
- [Counters](#Counters)
- [Windows](#Windows)
- [Tags](#Tags)
- [Case](#Case)
- [Marks](#Marks)
- [Command Line](#CommandLine)
- [Commenting](#Commenting)
- [Surround](#Surround)
- [Working with multiple files](#MultipleFiles)
- [VSCodeVim Tricks](#VSCodeVimTricks)

## GettingStarted

| Shortcut       | Description                      |
| -------------- | -------------------------------- |
| `:qa`          | Close all files                  |
| `:qa!`         | Close all files, abandon changes |
| `:w`           | Save                             |
| `:wq` _/_ `:x` | Save and close file              |
| `:q`           | Close file                       |
| `:q!`          | Close file, abandon changes      |
| `.`            | Repeat last command              |

### Navigating

| Shortcut            | Description              |
| ------------------- | ------------------------ |
| `<C-F>` _/_ `<C-B>` | Scrool Down/Up page      |
| `<C-D>` _/_ `<C-U>` | Scrool Down/Up half page |
| `<C-Y>` _/_ `<C-E>` | Scrool Down/Up line      |
| `{` _/_ `}`         | Previous/Next paragraph  |
| `h` `j` `k` `l`     | Arrow keys               |


#### Words

| Shortcut     | Description                      |
| ------------ | -------------------------------- |
| `b` _/_ `w`  | Previous/Next word               |
| `ge` _/_ `e` | Previous//Next end of word       |
| `leader` before above shortcut | P/N Camel case |

#### Semantically

| Shortcut | Description      |
| -------- | ---------------- |
| `gd`     | Go to definition |
| `gf`     | Go to file       |

#### Line

| Shortcut     | Description                        |
| ------------ | ---------------------------------- |
| `0` _(zero)_ | Start of line                      |
| `^`          | Start of line _(after whitespace)_ |
| `$`          | End of line                        |
| `}`          | Jumps entire paragraphs downwards  |
| `{`          | similarly but upwards              |

#### Character

| Shortcut | Description                      |
| -------- | -------------------------------- |
| `fc`     | Go forward to character `c`      |
| `Fc`     | Go backward to character `c`     |
| `tc`     | Go forward till character `c`    |
| `Tc`     | Go backward till character `c`   |
| `;c`     | Go to next occurrence of `c`     |
| `,c`     | Go to previous occurrence of `c` |

#### Document

| Shortcut | Description    |
| -------- | -------------- |
| `gg`     | First line     |
| `G`      | Last line      |
| `:n`     | Go to line `n` |
| `nG`     | Go to line `n` |

#### Window

| Shortcut | Description              |
| -------- | ------------------------ |
| `zz`     | Center this line         |
| `zt`     | Top this line            |
| `zb`     | Bottom this line         |
| `H`      | Move to top of screen    |
| `M`      | Move to middle of screen |
| `L`      | Move to bottom of screen |

#### Tab Pages

| Shortcut        | Description                   |
| --------------- | ----------------------------- |
| `:tabnew:`      | New tab                       |
| `:tabc`         | Close current tab             |
| `:tabo`         | Close all tabs except current |
| `gt` or `:tabn` | Go to next tab                |
| `gT`or `:tabp`  | Go to previous tab            |
| `2gt`           | Move to second tab            |

### Editing

| Shortcut | Description                         |
| -------- | ----------------------------------- |
| `a`      | Append                              |
| `i`      | Insert                              |
| `o`      | Next line                           |
| `O`      | Previous line                       |
| ---      | ---                                 |
| `s`      | Delete char and insert              |
| `S`      | Delete line and insert              |
| `C`      | Delete until end of line and insert |
| ---      | ---                                 |
| `r`      | Replace one character               |
| `R`      | Enter Replace mode                  |
| ---      | ---                                 |
| `u`      | Undo changes                        |
| `<C-R>`  | Redo changes                        |

### ExitingInsertMode

| Shortcut          | Description                                 |
| ----------------- | ------------------------------------------- |
| `Esc` _/_ `<C-[>` | Exit insert mode                            |
| `<C-C>`           | Exit insert mode, and abort current command |

### Clipboard

| Shortcut | Description         |
| -------- | ------------------- |
| `x`      | Delete character    |
| ---      | ---                 |
| `dd`     | Delete line _(Cut)_ |
| `yy`     | Yank line _(Copy)_  |
| ---      | ---                 |
| `p`      | Paste               |
| `P`      | Paste before        |

### VisualMode

| Shortcut | Description             |
| -------- | ----------------------- |
| `v`      | Enter visual mode       |
| `V`      | Enter visual line mode  |
| `<C-V>`  | Enter visual block mode |

#### InVisualMode

| Shortcut    | Description             |
| ----------- | ----------------------- |
| `d` _/_ `x` | Delete selection        |
| `s`         | Replace selection       |
| `y`         | Yank selection _(Copy)_ |

## Operators

Operators let you operate in a range of text (defined by _motion_). These are performed in normal mode.

|          |        |
| -------- | ------ |
| `d`      | `w`    |
| Operator | Motion |

### OperatorsList

| Shortcut | Description                     |
| -------- | ------------------------------- |
| `d`      | Delete                          |
| `y`      | Yank _(copy)_                   |
| `c`      | Change _(delete then insert)_   |
| ---      | ---                             |
| `>`      | Indent right                    |
| `<`      | Indent left                     |
| ---      | ---                             |
| `g~`     | Swap case                       |
| `gU`     | Uppercase                       |
| `gu`     | Lowercase                       |
| ---      | ---                             |
| `!`      | Filter through external program |

See `:help operator`

### OperatorsExamples

Combine operators with _motions_ to use them.

| Shortcut               | Description                               |
| ---------------------- | ----------------------------------------- |
| `d`_d_                 | _(repeat the letter)_ Delete current line |
| `d`_w_                 | Delete to next word                       |
| `d`_b_                 | Delete to beginning of word               |
| _2_`dd`                | Delete 2 lines                            |
| `d`_ip_                | Delete a text object _(inside paragraph)_ |
| _(in visual mode)_ `d` | Delete selection                          |

See: `:help motion.txt`

## TextObjects

Text objects let you operate (with an _operator_) in or around text blocks (_objects_).

|          |                      |             |
| -------- | -------------------- | ----------- |
| `v`      | `i`                  | `p`         |
| Operator | [i]nside or [a]round | Text object |

| Shortcut                                 | Description           |
| ---------------------------------------- | --------------------- |
| `p`                                      | Paragraph             |
| `w`                                      | Word                  |
| `s`                                      | Sentence              |
| ---                                      | ---                   |
| `[` `(` `{` `<`                          | A [], (), or {} block |
| `'` `"` <code>`</code> | A quoted string |
| ---                                      | ---                   |
| `b`                                      | A block [(            |
| `B`                                      | A block in [{         |
| `t`                                      | A XML tag block       |

### TextObjectsExamples

| Shortcut    | Description                        |
| ----------- | ---------------------------------- |
| `vip`       | Select paragraph                   |
| `vipipipip` | Select more                        |
| ---         | ---                                |
| `yip`       | Yank inner paragraph               |
| `yap`       | Yank paragraph (including newline) |
| ---         | ---                                |
| `dip`       | Delete inner paragraph             |
| `cip`       | Change inner paragraph             |

### Folds

| Shortcut      | Description                  |
| ------------- | ---------------------------- |
| `zo` _/_ `zO` | Open                         |
| `zc` _/_ `zC` | Close                        |
| `za` _/_ `zA` | Toggle                       |
| ---           | ---                          |
| `zv`          | Open folds for this line     |
| ---           | ---                          |
| `zM`          | Close all                    |
| `zR`          | Open all                     |
| ---           | ---                          |
| `zm`          | Fold more _(foldlevel += 1)_ |
| `zr`          | Fold less _(foldlevel -= 1)_ |
| ---           | ---                          |
| `zx`          | Update folds                 |

Uppercase ones are recursive (eg, `zO` is open recursively).

### AdvancedNavigation

| Shortcut       | Description                |
| -------------- | -------------------------- |
| `[(` `[{` `[<` | Previous `(` or `{` or `<` |
| `])`           | Next                       |
| ---            | ---                        |
| `[m`           | Previous method start      |
| `[M`           | Previous method end        |

### Jumping

| Shortcut | Description                  |
| -------- | ---------------------------- |
| `<C-O>`  | Go back to previous location |
| `<C-I>`  | Go forward                   |
| ---      | ---                          |
| `gf`     | Go to file in cursor         |

### Counters

| Shortcut | Description      |
| -------- | ---------------- |
| `<C-A>`  | Increment number |
| `<C-X>`  | Decrement        |

### Windows

| `z{height}<Cr>` | Resize pane to `{height}` lines tall |

### Tags

| Shortcut             | Description                                     |
| -------------------- | ----------------------------------------------- |
| `:tag Classname`     | Jump to first definition of Classname           |
| ---                  | ---                                             |
| `<C-]>`              | Jump to definition                              |
| `g]`                 | See all definitions                             |
| `<C-T>`              | Go back to last tag                             |
| `<C-O> <C-I>`        | Back/forward                                    |
| ---                  | ---                                             |
| `:tselect Classname` | Find definitions of Classname                   |
| `:tjump Classname`   | Find definitions of Classname (auto-select 1st) |

### Case

| Shortcut | Description                          |
| -------- | ------------------------------------ |
| `~`      | Toggle case (Case => cASE)           |
| `gU`     | Uppercase                            |
| `gu`     | Lowercase                            |
| ---      | ---                                  |
| `gUU`    | Uppercase current line (also `gUgU`) |
| `guu`    | Lowercase current line (also `gugu`) |

Do these in visual or normal mode.

### Marks

| Shortcut                                                 | Description                                         |
| -------------------------------------------------------- | --------------------------------------------------- |
| <code>`^</code> | Last position of cursor in insert mode |
| <code>`.</code> | Last change                            |
| <code>``</code> | Last jump                              |
| ---                                                      | ---                                                 |
| `ma`                                                     | Mark this cursor position as `a`                    |
| <code>`a</code> | Jump to the cursor position`a`         |
| `'a`                                                     | Jump to the beginning of the line with position `a` |

### CommandLine

| Shortcut     | Description                               |
| ------------ | ----------------------------------------- |
| `<C-R><C-W>` | Insert current word into the command line |
| `<C-R>"`     | Paste from " register                     |
| `<C-X><C-F>` | Auto-completion of path in insert mode    |

### Commenting

| Shortcut | Description                                    |
| -------- | ---------------------------------------------- |
| `gc`     | Toggle Line Comment                            |
| `gcc`    | Toggle Comment Current Line                    |
| `gc2j`   | Toggle Comment Current Line and Next Two Lines |
| `gC`     | Toggle Block Comment                           |

### Surround

| Shortcut                             | Description                                                           |
| ------------------------------------ | --------------------------------------------------------------------- |
| `d s <existing char>`                | Delete existing surround                                              |
| `c s <existing char> <desired char>` | Change surround existing to desired                                   |
| `y s <motion> <desired char>`        | Add surround   |
| `S <desired char>`                   | Surround when in visual modes (surrounds full selection)              |

With cursor inside quotes `"test"` type `cs"'` to end up with `'test'`
With cursor in word `test` type `ysw"` to end up with `"test"`

## MultipleFiles

| Shortcut           | Description             |
| ------------------ | ----------------------- |
| `<C-w> s` or `:sp` | split window            |
| `<C-w> v` or `:vs` | split window vertically |
| `<C-w> w`          | switch windows          |
| `<C-w> q`          | quit a window           |
| `<C-w> h`          | move to left window     |
| `<C-w> j`          | move to below window    |
| `<C-w> k`          | move to top window      |
| `<C-w> l`          | move to right window    |

## 🎩 VSCodeVimTricks!

VS Code has a lot of nifty tricks and we try to preserve some of them:

- `gd` - jump to definition.
- `gq` - on a visual selection reflow and wordwrap blocks of text, preserving commenting style. Great for formatting documentation comments.
- `gb` - adds another cursor on the next word it finds which is the same as the word under the cursor.
- `af` - visual mode command which selects increasingly large blocks of text. For example, if you had "blah (foo [bar 'ba|z'])" then it would select 'baz' first. If you pressed `af` again, it'd then select [bar 'baz'], and if you did it a third time it would select "(foo [bar 'baz'])".
- `gh` - equivalent to hovering your mouse over wherever the cursor is. Handy for seeing types and error messages without reaching for the mouse!
