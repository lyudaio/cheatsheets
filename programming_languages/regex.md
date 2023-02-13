# Regular Expressions (Regex) Cheatsheet

A regular expression, or regex for short, is a pattern that describes a set of strings. Regular expressions are a powerful tool for searching, manipulating, and validating text.

## Basic Syntax

Here are the basic elements of a regular expression:

- `.`: Matches any single character except for a newline.
- `*`: Matches zero or more occurrences of the preceding element.
- `+`: Matches one or more occurrences of the preceding element.
- `?`: Matches zero or one occurrence of the preceding element.
- `{n}`: Matches exactly n occurrences of the preceding element.
- `{n,}`: Matches n or more occurrences of the preceding element.
- `{m,n}`: Matches between m and n (inclusive) occurrences of the preceding element.
- `[ ]`: Matches any single character within the brackets.
- `^`: Matches the start of a line.
- `$`: Matches the end of a line.
- `( )`: Grouping elements and capturing submatches.
- `|`: Alternation, matches either the expression before or the expression after the `|`.

## Common Character Classes

Here are some common character classes:

- `\d`: Matches any digit (equivalent to `[0-9]`).
- `\D`: Matches any non-digit (equivalent to `[^0-9]`).
- `\w`: Matches any word character (equivalent to `[a-zA-Z0-9_]`).
- `\W`: Matches any non-word character (equivalent to `[^a-zA-Z0-9_]`).
- `\s`: Matches any whitespace character (equivalent to `[ \t\r\n\f]`).
- `\S`: Matches any non-whitespace character (equivalent to `[^ \t\r\n\f]`).

## Flags

Here are some common flags that can be added to the end of a regular expression:

- `g`: Global, matches multiple occurrences throughout the entire input string.
- `i`: Case-insensitive, performs a case-insensitive match.
- `m`: Multi-line, matches across multiple lines.

## Examples

Here are some examples of regular expressions in action:

- `/\d+/g`: Matches one or more digits globally.
- `/^[a-z]+$/i`: Matches lowercase letters only, case-insensitively.
- `/^#[a-f0-9]{6}$/`: Matches a hexadecimal color code, case-sensitively.

For more information on regular expressions, see the [official documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).

## Advanced Regex Topics

### Grouping and Capturing

Regex provides the ability to group multiple subpatterns together and capture the matched text as a whole. This allows for more complex pattern matching and manipulation of matched text.

To group subpatterns, use parentheses `( )` in your pattern. The matched text for the group can then be referred to later in the pattern using backreferences, such as `\1`, `\2`, etc.

Here's an example to match a repeating word:

```javascript
(\b\w+\b)\s+\1
```

This pattern matches a word followed by a space and the same word again. The grouped subpattern `(\b\w+\b)` captures the first word and the backreference `\1` references the same text matched by the group.

### Non-Capturing Groups

Sometimes, you may want to group subpatterns without capturing the matched text. This can be done using non-capturing groups, denoted by `(?: )`.

Here's an example to match a repeating word, without capturing the matched word:

```javascript
(?:\b\w+\b)\s+(\b\w+\b)
```

In this example, the first grouped subpattern `(?:\b\w+\b)` is a non-capturing group and will not be included in the final matched text. The second group `(\b\w+\b)` captures the second word.

### Lookarounds

Lookarounds allow you to assert a condition about the text surrounding a match, without including the surrounding text in the final matched text.

There are two types of lookarounds: positive lookahead (`(?= )`) and negative lookahead (`(?! )`).

A positive lookahead asserts that the text following the current position matches the pattern within the lookahead. For example, to match a word followed by a digit:

```javascript
\b\w+\b(?=\d)
```

A negative lookahead asserts that the text following the current position does not match the pattern within the lookahead. For example, to match a word not followed by a digit:

```javascript
\b\w+\b(?!\d)
```

There are also positive lookbehind (`(?<= )`) and negative lookbehind (`(?<! )`) that assert conditions about the text preceding a match.

### Named Groups and References

Named groups and references allow you to assign a name to a capturing group, making it easier to refer to the matched text later in your pattern or code.

Named groups are denoted by `(?<name> )`. For example:

```javascript
(?<word>\b\w+\b)\s+(\k<word>)
```

In this example, the first capturing group `(?<word>\b\w+\b)` is assigned the name "word". The second group references the same matched text as the first group using the syntax `\k<word>`.
