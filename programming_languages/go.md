# Go Cheat Sheet

## Description

Go is a popular open-source programming language developed by Google. It's designed for building modern, efficient, and scalable applications. Go combines the best features of different programming languages, making it a fast, statically-typed, and garbage-collected language that provides memory safety.

## Versions

| Version | Latest Patch Release | Release Date      | End of Support |
| ------- | -------------------- | ----------------- | -------------- |
| 1.21    | 1.21.5               | August 16, 2022   | TBD            |
| 1.20    | 1.20.4               | February 16, 2022 | February 2023  |
| 1.19    | 1.19.14              | August 2, 2021    | August 2022    |
| 1.18    | 1.18.4               | February 16, 2021 | February 2022  |
| 1.17    | 1.17.7               | August 16, 2020   | August 2021    |
| 1.16    | 1.16.13              | February 16, 2020 | February 2022  |
| 1.15    | 1.15.15              | August 11, 2019   | August 2020    |
| 1.14    | 1.14.15              | February 25, 2019 | February 2020  |
| 1.13    | 1.13.15              | September 3, 2018 | September 2019 |
| 1.12    | 1.12.18              | February 16, 2018 | February 2020  |
| 1.11    | 1.11.15              | August 24, 2017   | August 2018    |
| 1.10    | 1.10.8               | February 17, 2017 | February 2018  |
| 1.9     | 1.9.7                | August 24, 2016   | March 2018     |
| 1.8     | 1.8.9                | February 17, 2016 | March 2018     |
| 1.7     | 1.7.6                | March 3, 2015     | December 2016  |
| 1.6     | 1.6.4                | February 19, 2015 | February 2017  |

- Please note that this table includes the latest patch release, release date, and end of support for each version of Go. The end of support date indicates when the Go team will stop providing security patches and updates for that version of Go. It's important to keep your Go version up-to-date to ensure that your projects are secure and stable.

## Data Types

Go has several built-in data types, including:

| Data Type                                     | Description                                                        |
| --------------------------------------------- | ------------------------------------------------------------------ |
| `string`                                      | Represents a sequence of characters.                               |
| `int`, `int8`, `int16`, `int32`, `int64`      | Represents signed integers of various sizes.                       |
| `uint`, `uint8`, `uint16`, `uint32`, `uint64` | Represents unsigned integers of various sizes.                     |
| `float32`, `float64`                          | Represents floating-point numbers.                                 |
| `bool`                                        | Represents a boolean value (`true` or `false`).                    |
| `array`                                       | Represents a fixed-sized array of elements.                        |
| `slice`                                       | Represents a dynamic array that can grow or shrink during runtime. |
| `map`                                         | Represents an unordered collection of key-value pairs.             |

## Variables and Constants

Variables and constants in Go are declared using the `var` and `const` keywords, respectively:

```go
var variableName string = "value"
const constantName string = "value"
```

Go also supports shorthand variable declaration and initialization using the `:=` operator:

```go
variableName := "value"
```

## Control Flow

Go supports several control flow statements, including:

- `if` statements for conditional execution.
- `for` statements for looping.
- `switch` statements for multi-way branching.
- `defer` statements for deferring the execution of a function until the surrounding function returns.

## Functions

Functions in Go are declared using the `func` keyword:

```go
func functionName(parameterName parameterType) returnType {
  // function body
  return value
}
```

## Arrays and Slices

Arrays in Go have a fixed size and are declared as follows:

```go
var arrayName [size]type = [size]type{value1, value2, ...}
```

Slices are dynamic arrays and are declared using the `make` function:

```go
sliceName := make([]type, length, capacity)
```

## Maps

Maps in Go associate keys with values and are declared using the `make` function:

```go
mapName := make(map[keyType]valueType)
```

## Packages and Imports

Go programs are organized into packages, which can be imported by other packages to reuse their functionality. The `import` keyword is used to import packages:

```go
import "packageName"
```

## Additional Resources

- [Go documentation](https://golang.org/doc/)
- [A Tour of Go](https://tour.golang.org/welcome/1)

## Example

Here is a simple example of a Go program that calculates the factorial of a number:

```go
package main

import "fmt"

func factorial(n int) int {
  if n == 0 {
    return 1
  }
  return n * factorial(n - 1)
}

func main() {
  var n int
  fmt.Print("Enter a number: ")
  fmt.Scan(&n)
  fmt.Println("The factorial of", n, "is", factorial(n))
}
```

## Conclusion

This cheat sheet provided an overview of the basic concepts and elements of the Go programming language. To learn more, it is recommended to visit the [Go documentation.](https://golang.org/doc/) With its simplicity, performance, and scalability, Go is a great choice for building modern and efficient applications.
