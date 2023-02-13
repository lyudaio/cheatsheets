
# Julia Cheatsheet

## Variables

In Julia, variables are created and assigned a value using the `=` operator.

```julia
x = 3
y = "Hello, world!"
```

## Data Types

Julia supports a variety of data types, including integers, floating-point numbers, strings, and booleans.

```julia
# integers
x = 3

# floating-point numbers
y = 3.14

# strings
z = "Hello, world!"

# booleans
a = true
b = false
```

## Operators

Julia supports a variety of operators, including arithmetic, comparison, and logical operators.

```julia
# arithmetic operators
x = 3 + 4 # 7
y = 3 - 4 # -1
z = 3 * 4 # 12
w = 3 / 4 # 0.75

# comparison operators
a = 3 == 4 # false
b = 3 != 4 # true
c = 3 < 4 # true
d = 3 > 4 # false

# logical operators
e = true && false # false
f = true || false # true
```

## Control Flow

Julia supports a variety of control flow statements, including `if`-`else` and `for` loops.

```julia
# if-else statement
x = 3
if x > 0
    println("x is positive")
else
    println("x is non-positive")

# for loop
for i in 1:5
    println(i)
```

## Functions

In Julia, functions are defined using the `function` keyword.

```julia
function add(x, y)
    x + y
end

add(3, 4) # 7
```

## Types

Julia is a dynamically-typed language, but it also supports user-defined types.

```julia
# defining a type
type Person
    name::String
    age::Int
end

# creating an instance of a type
p = Person("John Doe", 30)
```

## Arrays

In Julia, arrays are created using the `[]` syntax.

```julia
a = [1, 2, 3, 4]
a[1] # 1
```

## Dictionaries

In Julia, dictionaries are created using the `Dict` type.

```julia
d = Dict("a" => 1, "b" => 2)
d["a"] # 1
```

