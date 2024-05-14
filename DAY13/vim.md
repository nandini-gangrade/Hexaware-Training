# Vim Editor Commands Cheat Sheet

Vim is a highly configurable text editor built to enable efficient text editing. It is an improved version of the Vi editor and comes with powerful features and shortcuts.

## Opening Vim

Vim is typically opened using the `vim` command followed by the name of the file to edit. For example:

```bash
vim filename.txt
```

## Movement

| Command       | Description                             | Usage                                      | When to Use                                |
|---------------|-----------------------------------------|--------------------------------------------|--------------------------------------------|
| `h`           | Move cursor left                        | Press the left arrow key or `h`           | To navigate left in the text              |
| `j`           | Move cursor down                        | Press the down arrow key or `j`           | To navigate downwards in the text         |
| `k`           | Move cursor up                          | Press the up arrow key or `k`             | To navigate upwards in the text           |
| `l`           | Move cursor right                       | Press the right arrow key or `l`          | To navigate right in the text             |
| `w`           | Move cursor forward by a word           | Press `w`                                  | To move forward by a word in the text     |
| `b`           | Move cursor backward by a word          | Press `b`                                  | To move backward by a word in the text    |
| `^`           | Move cursor to the beginning of line    | Press `^`                                  | To move to the beginning of a line        |
| `$`           | Move cursor to the end of line          | Press `$`                                  | To move to the end of a line              |
| `gg`          | Move cursor to the first line           | Type `gg`                                  | To move to the beginning of the document  |
| `G`           | Move cursor to the last line            | Type `G`                                   | To move to the end of the document        |
| `<line_number>`| Move cursor to a specific line number   | Type the line number followed by `G`       | To move to a specific line in the text    |

## Editing

| Command       | Description                             | Usage                                      | When to Use                                |
|---------------|-----------------------------------------|--------------------------------------------|--------------------------------------------|
| `i`           | Enter insert mode                       | Press `i`                                  | To start inserting text at the cursor     |
| `a`           | Enter insert mode after cursor position | Press `a`                                  | To start inserting text after the cursor  |
| `A`           | Enter insert mode at end of line        | Press `A`                                  | To start inserting text at the end of line |
| `o`           | Open new line below and enter insert mode| Press `o`                                  | To start inserting text on a new line     |
| `O`           | Open new line above and enter insert mode| Press `O`                                  | To start inserting text above the current line |
| `x`           | Delete character under cursor           | Press `x`                                  | To delete the character under the cursor  |
| `dd`          | Delete current line                     | Type `dd`                                  | To delete the current line                |
| `yy`          | Copy current line                       | Type `yy`                                  | To copy the current line                  |
| `p`           | Paste copied text                       | Press `p`                                  | To paste copied text                      |
| `u`           | Undo the last change                    | Press `u`                                  | To undo the last change                   |
| `Ctrl + r`    | Redo the last undone change             | Press `Ctrl + r`                           | To redo the last undone change            |

## Searching and Replacing

| Command       | Description                             | Usage                                      | When to Use                                |
|---------------|-----------------------------------------|--------------------------------------------|--------------------------------------------|
| `/`           | Search for a pattern                    | Type `/` followed by the pattern           | To search for a specific pattern in the text |
| `n`           | Move to the next occurrence of the pattern | Press `n`                                | To move to the next occurrence of the search pattern |
| `N`           | Move to the previous occurrence of the pattern | Press `N`                              | To move to the previous occurrence of the search pattern |
| `:s/pattern/replacement/g` | Replace pattern with replacement | Type `:s/pattern/replacement/g`         | To replace a pattern with a replacement    |
| `:s/pattern/replacement/gc` | Replace pattern with replacement with confirmation | Type `:s/pattern/replacement/gc`   | To replace a pattern with a replacement with confirmation |

## Saving and Exiting

| Command       | Description                             | Usage                                      | When to Use                                |
|---------------|-----------------------------------------|--------------------------------------------|--------------------------------------------|
| `:w`          | Save changes                            | Type `:w`                                  | To save changes made to the file          |
| `:wq`         | Save changes and quit                   | Type `:wq`                                 | To save changes and exit the editor       |
| `:q`          | Quit without saving                     | Type `:q`                                  | To quit without saving changes            |
| `:q!`         | Quit without saving and discard changes | Type `:q!`                                 | To quit without saving changes forcefully |

