# V (0.2.2)

V is a statically-typed, interpreted language designed to improve the developer experience and make programming more accessible and enjoyable. It aims to provide a clean, efficient, and fast syntax, while still being simple to understand.

## Variables

In V, variables are declared using the `let` keyword, followed by the variable name and value. The type of the variable can be explicitly specified using a colon `:` and the type name. If no type is specified, V will infer the type from the value assigned to the variable.

```go
let x = 10
let y: f64 = 3.14
let name = "John"
```

## Functions

Functions in V are declared using the `fn` keyword, followed by the function name, arguments, and the code block. Arguments are specified within parenthesis `()`, and the code block is enclosed within curly braces `{}`. The return type of a function can be specified using an arrow `->` and the type name.

```go
fn add(x: i32, y: i32) -> i32 {
  return x + y
}

let result = add(10, 20)
```

## Control Flow

V provides several control flow constructs for making decisions and repeating actions in code.

### If/Else

The `if` statement is used to evaluate a boolean expression and execute a block of code if the expression is true. An optional `else` clause can be used to specify alternative code to be executed if the expression is false.

```go
let x = 10

if x > 5 {
  println("x is greater than 5")
} else {
  println("x is less than or equal to 5")
}
```

### Loop

V provides two types of loops: `for` and `while`. The `for` loop is used to repeat a block of code a specific number of times, while the `while` loop is used to repeat a block of code as long as a condition is true.

```go
for i in 0..10 {
  println(i)
}

let x = 10
while x > 0 {
  println(x)
  x -= 1
}
```

## Modules

Modules in V are used to group related functions and data together. A module is defined in a separate file with the `.v` extension, and can be imported into other files using the `import` keyword.

```go
// my_module.v

fn add(x: i32, y: i32) -> i32 {
  return x + y
}

// main.v

import my_module

let result = my_module.add(10, 20)
```