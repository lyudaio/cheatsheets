# Kotlin Cheatsheet

Kotlin is a statically-typed, cross-platform programming language that is concise, expressive, and interoperable with Java. It was developed by JetBrains and has become one of the most popular programming languages for Android app development.

## Variables

In Kotlin, you can declare variables using the `var` or `val` keywords. The `var` keyword is used for mutable variables, while the `val` keyword is used for read-only (immutable) variables.

```java
// Declare a mutable variable
var name: String = "John Doe"

// Declare an immutable variable
val age: Int = 30
```

## Functions

Kotlin provides a simple and concise syntax for defining functions. Functions can be defined inside a class or outside of a class as a top-level function.

```java
// Define a top-level function
fun greet(name: String): String {
    return "Hello, $name"
}

// Call the function
println(greet("John Doe")) // Output: Hello, John Doe
```

## Classes and Objects

In Kotlin, classes are defined using the `class` keyword. Classes can have properties, methods, and constructors. To create an instance of a class, you use the `new` keyword in Java, but in Kotlin you can simply call the class name as a function.

```java
// Define a class
class Person(val name: String, var age: Int)

// Create an instance of the class
val person = Person("John Doe", 30)
```

## Control Flow

Kotlin provides a rich set of control flow constructs, including `if` expressions, `when` expressions, `for` loops, and `while` loops.

```java
// If expression example
val age = 30
val isAdult = if (age >= 18) true else false

// When expression example
val message = when (age) {
    in 0..17 -> "Too young"
    in 18..29 -> "Young adult"
    else -> "Adult"
}

// For loop example
for (i in 1..10) {
    println(i)
}

// While loop example
var i = 1
while (i <= 10) {
    println(i)
    i++
}
```

## Null Safety

Kotlin provides null safety features to avoid NullPointerException in the code. By default, variables in Kotlin cannot be null, but you can make them nullable by adding a `?` after the type declaration.

Here is an example of nullable variable declaration:

```java
var name: String? = null
```

## Lambdas

Lambdas are anonymous functions that can be assigned to variables or passed as arguments. Here is an example of a lambda expression in Kotlin:

```java
val sum = {a: Int, b: Int -> a + b}
```

## Extension Functions

Kotlin allows you to add new functionality to an existing class without having to inherit from the class. This is achieved through extension functions.

Here is an example of an extension function:

```java
fun String.toTitleCase(): String {
    return this.split(" ").joinToString(" ") { it.capitalize() }
}
```

## Coroutines

Coroutines are a powerful tool for asynchronous programming in Kotlin. They allow you to write asynchronous code that is readable and easy to understand. Here is an example of coroutines in Kotlin:

```java
suspend fun fetchData(): String {
    delay(1000)
    return "Data fetched"
}
```

## Conclusion

This cheatsheet provides an overview of some of the most important features of Kotlin. To learn more about Kotlin, you can refer to the official documentation or other resources available online.
