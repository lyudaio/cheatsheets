# CoffeeScript (2.3.3)

CoffeeScript is a high-level, dynamic, and interpreted programming language that compiles to JavaScript.

## Variables

You can declare variables in CoffeeScript with the `=` operator.

```javascript
x = 10
y = 20
z = x + y
```

## Loops

CoffeeScript has several ways to write loops.

### For Loop

A for loop can be written using the `for` keyword.

```javascript
for i in [0...10]
  console.log i
```

### While Loop

A while loop can be written using the `while` keyword.

```javascript
i = 0
while i < 10
  console.log i
  i++
```

## Functions

Functions in CoffeeScript are declared using the `->` operator.

```javascript
square = (x) -> x * x
console.log square(10)
```
