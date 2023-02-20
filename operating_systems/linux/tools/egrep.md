# egrep Command Cheatsheet

The "egrep" command in Linux is used to search for text patterns in one or more files, using extended regular expressions. It is similar to the "grep" command, but with support for more complex pattern matching.

## Syntax

The syntax for the "egrep" command is as follows:

```bash
egrep [options] pattern [file(s)]
```

## Options

The following options are available for the "egrep" command:

| Option  | Description                                                                                                                  |
| ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| -i      | Ignore case when matching patterns.                                                                                          |
| -r      | Recursively search subdirectories.                                                                                           |
| -v      | Invert the match: display all lines that do NOT match the pattern.                                                           |
| -w      | Match whole words only.                                                                                                      |
| -n      | Display line numbers for matched lines.                                                                                      |
| -H      | Display the filename along with the matched lines.                                                                           |
| -h      | Do NOT display the filename along with the matched lines.                                                                    |
| -E      | Interpret the pattern as an extended regular expression. (This option is enabled by default, but can be disabled with "-G".) |
| -G      | Interpret the pattern as a basic regular expression.                                                                         |
| -f FILE | Read patterns from FILE, one per line.                                                                                       |

## Pattern Syntax

The pattern syntax for "egrep" is an extension of basic regular expressions, with support for additional metacharacters and quantifiers. Here are some examples:

| Pattern  | Matches                                                  |
| -------- | -------------------------------------------------------- |
| foo      | Lines containing the string "foo".                       |
| ^foo     | Lines starting with "foo".                               |
| foo$     | Lines ending with "foo".                                 |
| [abc]    | Lines containing any of the characters "a", "b", or "c". |
| [a-z]    | Lines containing any lowercase letter.                   |
| [0-9]    | Lines containing any digit.                              |
| .        | Lines containing any single character.                   |
| foo\|bar | Lines containing either "foo" or "bar".                  |
| (abc)    | Lines containing the string "abc".                       |
| a{2,3}   | Lines containing 2 or 3 consecutive "a" characters.      |
| a\*      | Lines containing 0 or more "a" characters.               |
| a+       | Lines containing 1 or more "a" characters.               |

## Examples

Here are some examples of how to use the "egrep" command:

```bash
egrep 'hello' myfile.txt
```

This command will search for the string "hello" in the file "myfile.txt".

```bash
egrep -i 'hello' myfile.txt
```

This command will search for the string "hello" in a case-insensitive manner.

```bash
egrep -r 'hello' /myfolder/
```

This command will search for the string "hello" in all files within the directory "/myfolder/" and its subdirectories.

```bash
egrep -v 'hello' myfile.txt
```

This command will display all lines in "myfile.txt" that do NOT contain the string "hello".

```bash
egrep -w 'hello' myfile.txt
```

This command will search for the word "hello" (i.e. surrounded by whitespace) in "myfile.txt".

```bash
egrep -n 'hello' myfile.txt
```

This command will display the line numbers of all lines in "myfile.txt" that contain the string
