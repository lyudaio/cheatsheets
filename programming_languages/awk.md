# Introduction to AWK

AWK is a scripting language used for processing and manipulating text-based data, either in files or from standard input. AWK scripts contain a sequence of pattern-action statements, where each pattern is tested against each input line, and if a match is found, the corresponding action is executed.

## Basic Usage

The basic structure of an AWK script is as follows:

```bash
pattern { action }
```

Where `pattern` is a regular expression that is tested against each line of input, and `action` is a set of commands to be executed if the pattern is matched.

## Data Types

| Data Type | Description                                                             |
| --------- | ----------------------------------------------------------------------- |
| string    | A sequence of characters                                                |
| numeric   | A number, either integer or floating-point                              |
| boolean   | A logical value, either `true` or `false`                               |
| array     | A collection of values, indexed by integer or string values             |
| field     | A single field in a record, identified by its position number           |
| record    | A complete input record, consisting of one or more fields               |
| regexp    | A regular expression, used for pattern matching                         |
| function  | A named block of code that can be called from other parts of the script |

## Variables

AWK has several built-in variables that provide information about each input line:

- `$0`: The entire input line.
- `$1`, `$2`, `$3`, etc.: The first, second, third, etc. fields in the input line, separated by the field separator (usually a space or a tab).

AWK also allows you to define your own variables.

## Operators

AWK supports several types of operators, including arithmetic, relational, and logical operators. For example:

```bash
awk '{ print $1 + $2 }'
```

## Built-in Functions

AWK provides several built-in functions for performing operations such as string manipulation, arithmetic operations, and more. Some commonly used functions include:

- `length(s)`: Returns the length of string `s`.
- `substr(s, i, n)`: Returns the substring of string `s` starting at position `i` and with a length of `n` characters.
- `sqrt(x)`: Returns the square root of `x`.

## Advanced Features

AWK also provides several advanced features, including:

- User-defined functions: You can define your own functions to perform complex operations in your AWK scripts.
- Conditional statements: You can use `if` statements to perform actions based on conditions.
- Loops: You can use `for` loops to repeat actions.

## Conclusion

AWK is a powerful tool for processing and manipulating text-based data. With its built-in variables, operators, and functions, it can perform complex operations on input data with ease. Whether you're a beginner or an advanced user, this cheatsheet provides a quick reference for the most common operations you'll perform with AWK.
