# VIM 8.2 (Latest LTS Version as of 2021-09)

Vim is a highly configurable text editor built to enable efficient text editing. It is an improved version of the vi editor distributed with most UNIX systems. Vim is often called a "programmer's editor," and so useful for programming that many consider it an entire IDE. It's not just for programmers, though. Vim is perfect for all kinds of text editing, from composing email to editing configuration files.

## Getting Started

Starting Vim:

```vim
vim filename
```

Where `filename` is the name of the file you want to open/create.

## Modes

Vim has two modes:

- Command mode: Where you can execute commands like save, close, copy, paste, etc.
- Insert mode: Where you can type and edit text.

## Basic Navigation

- h: move cursor left
- j: move cursor down
- k: move cursor up
- l: move cursor right
- w: move cursor to the beginning of the next word
- b: move cursor to the beginning of the previous word
- 0 (zero): move cursor to the beginning of the line
- $: move cursor to the end of the line
- gg: move cursor to the beginning of the file
- G: move cursor to the end of the file

## Basic Editing

- i: switch to insert mode at the current cursor position
- I: switch to insert mode at the beginning of the line
- a: switch to insert mode after the current cursor position
- A: switch to insert mode at the end of the line
- o: create a new line below the current line and switch to insert mode
- O: create a new line above the current line and switch to insert mode
- x: delete the character under the cursor
- dd: delete the current line
- d$: delete from the cursor to the end of the line
- dw: delete from the cursor to the end of the current word
- u: undo the last change
- Ctrl + r: redo the last undone change
- yy: copy the current line
- p: paste the copied text after the cursor
- P: paste the copied text before the cursor
- :w: save the current file
- :q: quit the editor
- :wq: save and quit the editor

## Advanced Editing

- /{pattern}: search for the given pattern in the file
- n: move to the next instance of the pattern
- N: move to the previous instance of the pattern
- :%s/old/new/g: replace all instances of "old" with "new" in the entire file
- :%s/old/new/gc: replace all instances of "old" with "new" in the entire file with a confirmation for each change
- . (dot): repeat the last change
- Ctrl + v: enter visual block mode, where you can select and edit multiple lines at once
- v: enter visual mode, where you can select and edit a range of text
- r: replace a single character under the cursor
- R: enter replace mode, where you can replace multiple characters at once
- :help {topic}: open the Vim help documentation for the given topic

## Configuration

Vim configuration is done using a file called `.vimrc` located in your home directory. You can use the `.vimrc` file to customize Vim's settings and mapping keys to perform tasks.

## Conclusion

That's it! You now have a comprehensive overview of Vim and its commands, including basic movements and editing, visual mode, ex mode, Vim's insert mode, searching and replacing, commands for working with multiple files, and customizing Vim. Remember, Vim is all about efficiency, and the more you use it, the more natural it becomes.

Vim is a powerful tool and can be overwhelming at first, but with time and practice, you'll be a Vim ninja in no time!
