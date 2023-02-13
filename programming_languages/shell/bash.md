# Bash Cheat Sheet

## Basic commands

- `ls`: List the files in the current directory.
- `pwd`: Print the current working directory.
- `cd`: Change the current working directory.
- `mkdir`: Create a new directory.
- `rm`: Remove a file or directory.
- `rmdir`: Remove an empty directory.
- `touch`: Create an empty file.

## File operations

- `cp`: Copy a file.
- `mv`: Move or rename a file.
- `cat`: Display the contents of a file.
- `less`: Display the contents of a file one page at a time.
- `head`: Display the first few lines of a file.
- `tail`: Display the last few lines of a file.
- `grep`: Search for a pattern in a file.

## Environment variables

- `echo`: Display the value of a variable or text.
- `export`: Export a variable to the environment.
- `unset`: Unset a variable.
- `$PATH`: A list of directories where the shell will search for commands.
- `$HOME`: The path to the user's home directory.

## Input/Output Redirection

- `>`: Redirect standard output to a file, overwriting its contents.
- `>>`: Redirect standard output to a file, appending to its contents.
- `<`: Redirect standard input from a file.
- `2>`: Redirect standard error to a file, overwriting its contents.
- `2>>`: Redirect standard error to a file, appending to its contents.
- `&>`: Redirect both standard output and standard error to a file, overwriting its contents.

## Pipes

- `|`: Pipe the output of one command as the input to another command.

## Scripts

- `#!`: Shebang line specifying the interpreter for the script.
- `chmod`: Change the permissions of a file to make it executable.
- `./`: Run a script in the current directory.

## Loops

- `for`: Loop through a list of items.
- `while`: Repeat a block of commands as long as a condition is true.
- `until`: Repeat a block of commands until a condition is true.

## Conditional statements

- `if`: Execute a block of commands if a condition is true.
- `elif`: Execute a block of commands if the previous `if` condition is false and this condition is true.
- `else`: Execute a block of commands if all previous conditions are false.

## Functions

- `function`: Declare a function.
- `return`: Return a value from a function.
- `$1`, `$2`, etc.: Positional parameters passed to a function.
- `$@`: All positional parameters passed to a function.
- `$#`: The number of positional parameters passed to a function.

## Miscellaneous

- `&&`: Run the following command only if the previous command succeeded.
- `||`: Run the following command only if the previous command failed.
- `!`: Negate the return value of a command.
- `$?`: The return value of the last command.
- `$0`: The name of the script or shell.
- `$_`: The last argument of the previous command.
- `ctrl + c`: Interrupt the current command.
- `ctrl + z`: Suspend the current command.
- `bg`: Resume a suspended command in the background.
- `fg`: Resume a suspended command in the foreground.
