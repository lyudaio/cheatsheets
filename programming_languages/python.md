## Basic Syntax

- Python is case-sensitive
- Use `#` for single-line comments and `'''` for multi-line comments
- Indentation is used to define blocks (no curly braces)
- Use `'''` or `"""` to define multiline strings
- Use `\` for line continuation

## Variables

- No need to declare variable data types
- Variables can be assigned using `=`
- Examples:
```python
  age = 30
  salary = 25000.50
  gender = 'M'
  is_married = True
```

## Operators

- Arithmetic operators: `+`, `-`, `*`, `/`, `%`, `//`, `**`
- Relational operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Logical operators: `and`, `or`, `not`
- Assignment operators: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=`

## Conditional Statements

- `if` statement
- `if-elif-else` statement

## Loops

- `for` loop
- `while` loop

## Lists

- Collection of ordered and changeable elements
- Elements can be of different data types
- Lists are defined using square brackets `[]`
- Examples:
```python
  marks = [85, 90, 80]
  names = ['John', 'Jane', 'Jim']
```

## Tuples

- Collection of ordered and unchangeable elements
- Elements can be of different data types
- Tuples are defined using parentheses `()`
- Examples:
```python
  marks = (85, 90, 80)
  names = ('John', 'Jane', 'Jim')
```

## Dictionaries

- Collection of unordered, changeable and indexed elements
- Elements are stored in key-value pairs
- Dictionaries are defined using curly braces `{}`
- Examples:
```python
  details = {'name': 'John', 'age': 30, 'gender': 'M'}
```

## Functions

- Reusable blocks of code
- Can accept parameters and return values
- Use `def` keyword to define a function
- Examples:
```python
  def add_numbers(a, b):
      return a + b
  def say_hello():
      print("Hello")
```

## Classes

- Blueprint for creating objects
- Variables and methods inside a class
- Use `class` keyword to define a class
- Examples:
```python
  class Student:
      def __init__(self, roll_no, name):
          self.roll_no = roll_no
          self.name = name
      def display_details(self):
          print("Roll No:", self.roll_no)
          print("Name:", self.name)
```
