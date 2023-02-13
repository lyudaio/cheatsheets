# Javascript Cheatsheet

Javascript is a high-level, dynamically typed programming language commonly used for client-side web development and server-side programming with Node.js.

## Variables

Javascript has dynamic typing, meaning that a variable's type can change at runtime. Variables can be declared using the keywords `var`, `let`, or `const`.

```javascript
var x;
let y;
const z = 10;
```

`var` is function scoped, while `let` and `const` are block scoped. `const` is used to declare a constant value that cannot be re-assigned.

## Data Types

Javascript has the following primitive data types:

- String: a sequence of characters, denoted with quotes `''` or `""`.
- Number: numeric values, including integers and floating point numbers.
- Boolean: either `true` or `false`.
- Undefined: a variable that has been declared, but has no value.
- Null: explicitly represents the absence of any object value.

## Arrays

Arrays are ordered collections of values that can hold any data type. They are declared with square brackets `[]`.

```javascript
let numbers = [1, 2, 3];
let mixed = [1, 'two', false];
```

## Objects

Objects are collections of key-value pairs. They are declared with curly braces `{}`.

```javascript
let person = {
  name: 'John Doe',
  age: 30,
  occupation: 'developer'
};
```

## Operators

Javascript has various operators for performing arithmetic, assignment, comparison, and logical operations.

### Arithmetic Operators

- `+`: addition
- `-`: subtraction
- `*`: multiplication
- `/`: division
- `%`: modulus (remainder after division)

### Assignment Operators

- `=`: assignment
- `+=`: addition and assignment
- `-=`: subtraction and assignment
- `*=`: multiplication and assignment
- `/=`: division and assignment

### Comparison Operators

- `==`: equality
- `===`: strict equality (value and type)
- `!=`: inequality
- `!==`: strict inequality (value and type)
- `>`: greater than
- `<`: less than
- `>=`: greater than or equal to
- `<=`: less than or equal to
- `?`: ternary operator

### Logical Operators

- `&&`: logical AND
- `||`: logical OR
- `!`: logical NOT

### Type Operators

- `typeof`: returns the type of a variable
- `instanceof`: returns true if object is an instance of an object type

## Conditional Statements

Conditional statements are used to make decisions in code based on whether a condition is true or false.

```javascript
if (condition) {
  // code to be executed if condition is true
} else if (condition) {
  // code to be executed if condition is true
} else {
  // code to be executed if all conditions are false
}
```

## Loops

Loops are used to repeatedly execute a block of code.

### For Loop

A for loop is used to execute a block of code a specified number of times.

```javascript
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

### For-In Loop

A for-in loop is used to iterate over the properties of an object.

```javascript
let person = {
  name: 'John Doe',
  age: 30
};

for (let prop in person) {
  console.log(prop + ': ' + person[prop]);
}
```

### For-Of Loop

A for-of loop is used to iterate over the values of an iterable object, such as an array.

```javascript
let colors = ['red', 'green', 'blue'];

for (let color of colors) {
  console.log(color);
}
```

### While Loop

A while loop is used to execute a block of code as long as a specified condition is true.

```javascript
let i = 0;

while (i < 10) {
  console.log(i);
  i++;
}
```

### Do-While Loop

A do-while loop is similar to a while loop, but the block of code will always be executed at least once.

```javascript
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 10);
```
