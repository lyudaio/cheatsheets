# Python Cheatsheet

Python is a popular high-level programming language known for its simplicity, readability, and versatility. It is widely used for web development, data analysis, artificial intelligence, and more.

## Versions

| Version | Initial Release    | End of Life    | Latest Patch Release | Release Date      |
| ------- | ------------------ | -------------- | -------------------- | ----------------- |
| 3.10    | October 4, 2021    | October 2026   | 3.10.2               | February 18, 2022 |
| 3.9     | October 5, 2020    | October 2025   | 3.9.10               | October 4, 2021   |
| 3.8     | October 14, 2019   | October 2024   | 3.8.12               | July 19, 2021     |
| 3.7     | June 27, 2018      | June 2023      | 3.7.12               | June 28, 2021     |
| 3.6     | December 23, 2016  | December 2021  | 3.6.15               | December 23, 2020 |
| 3.5     | September 13, 2015 | September 2020 | 3.5.10               | March 13, 2017    |
| 2.7     | April 4, 2010      | January 2020   | 2.7.18               | April 20, 2020    |

## Basic Syntax

### Variables and Data Types

```python
# Variable assignment
x = 10
y = "hello"

# Data types
string = "hello"
integer = 42
float_num = 3.14
boolean = True
list = [1, 2, 3]
tuple = (1, 2, 3)
dictionary = {"key": "value"}
```

Here is a table that summarizes the basic data types and their sizes in Python:

| Data Type | Description           | Size (bytes)             |
| --------- | --------------------- | ------------------------ |
| int       | Integer               | 4 or 8                   |
| float     | Floating-point number | 8                        |
| bool      | Boolean               | 1                        |
| str       | String                | 1 per character          |
| list      | List                  | 4 + (4 or 8) per element |
| tuple     | Tuple                 | 4 + (4 or 8) per element |
| dict      | Dictionary            | Varies                   |

### Control Flow

```python
# If statement
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")

# For loop
for i in range(5):
    print(i)

# While loop
while x < 20:
    x += 1

# Break and continue
for i in range(10):
    if i == 5:
        continue
    if i == 8:
        break
    print(i)
```

### Functions

```python
# Define a function
def greet(name):
    print("Hello, " + name)

# Call a function
greet("Alice")

# Return a value from a function
def square(x):
    return x * x

result = square(5)
print(result)
```

## Built-in Functions

### Type Conversion

```python
# Convert to integer
x = int("42")

# Convert to float
y = float("3.14")

# Convert to string
z = str(42)
```

### String Manipulation

```python
# Concatenate strings
greeting = "Hello"
name = "Alice"
message = greeting + ", " + name

# Replace a substring
text = "The quick brown fox"
new_text = text.replace("quick", "slow")

# Split a string into a list
sentence = "This is a sentence"
words = sentence.split(" ")
```

### Lists and Tuples

```python
# Access an element by index
my_list = [1, 2, 3]
first_element = my_list[0]

# Add an element to a list
my_list.append(4)

# Create a tuple
my_tuple = (1, 2, 3)

# Unpack a tuple
a, b, c = my_tuple
```

### Dictionaries

```python
# Create a dictionary
my_dict = {"name": "Alice", "age": 30}

# Access a value by key
name = my_dict["name"]

# Add a key-value pair to a dictionary
my_dict["location"] = "New York"

# Loop through a dictionary
for key, value in my_dict.items():
    print(key + ": " + str(value))
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

## Additional Resources

- [Python Documentation](https://docs.python.org/3/)
- [Python Tips and Tricks](https://realpython.com/tutorials/best-practices/)
- [Python Package Index (PyPI)](https://pypi.org/)
