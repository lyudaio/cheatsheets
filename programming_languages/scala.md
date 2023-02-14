# Scala Cheatsheet (2.13.4 LTS)

## Basic Data Types

- Integer: `val x: Int = 5`
- Long: `val x: Long = 5L`
- Double: `val x: Double = 5.0`
- Float: `val x: Float = 5.0f`
- String: `val x: String = "Hello, Scala!"`
- Boolean: `val x: Boolean = true`
- Char: `val x: Char = 'a'`

## Variables

- Immutable variable: `val x = 5`
- Mutable variable: `var x = 5`

## Functions

- Define function:

  ```java
  def add(x: Int, y: Int): Int = {
    x + y
  }
  ```
  
- Call function: `add(5, 6)`
- Anonymous function (lambda): `(x: Int, y: Int) => x + y`

## Control Structures

- If-else statement:

  ```java
  if (x > 5) {
    println("x is greater than 5")
  } else {
    println("x is less than or equal to 5")
  }
  ```

- For loop:

  ```java
  for (i <- 1 to 5) {
    println(i)
  }
  ```
  
- While loop:

  ```java
  var i = 1
  while (i <= 5) {
    println(i)
    i = i + 1
  }
  ```

## Arrays

- Define array: `val x = Array(1, 2, 3, 4, 5)`
- Access array elements: `x(0)`

## Collections

- List: `val x = List(1, 2, 3, 4, 5)`
- Set: `val x = Set(1, 2, 3, 4, 5)`
- Map: `val x = Map("one" -> 1, "two" -> 2, "three" -> 3)`

## Classes

- Define class:

  ```java
  class Person {
    val name: String = "John Doe"
    var age: Int = 30
  }
  ```

- Create object: `val p = new Person`
- Access object properties: `p.name`
- Define constructor:

  ```java
  class Person(val name: String, var age: Int)
  ```

## Traits

- Define trait:

  ```java
  trait Greeter {
    def greet(name: String): Unit = {
      println(s"Hello, $name")
    }
  }
  ```

- Use trait:

  ```java
  class Person extends Greeter
  ```

## Official Documentation

- [Scala Language Specification](https://www.scala-lang.org/files/archive/spec/2.13/)
- [Scala Standard Library](https://www.scala-lang.org/api/2.13.4/)
