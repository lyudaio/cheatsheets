# Groovy Cheatsheet

Groovy is a dynamic, object-oriented programming language for the Java platform that provides a syntax that is concise and readable, making it easy for developers to write scripts and applications in this language. It supports both functional and object-oriented programming paradigms, making it a versatile language that can be used in a variety of applications.

## Variables

In Groovy, variables are declared using the def keyword.

```groovy
def name = "John Doe"
println(name)
```

## Strings

String concatenation in Groovy can be done using the + operator.

```groovy
def firstName = "John"
def lastName = "Doe"
def fullName = firstName + " " + lastName
println(fullName)
```

## Conditionals

Conditionals in Groovy are similar to those in other programming languages.

```groovy
def x = 5
if (x > 4) {
  println("x is greater than 4")
} else {
  println("x is not greater than 4")
}
```

## Loops

The for loop in Groovy is similar to the for loop in Java.

```groovy
for (int i = 0; i < 5; i++) {
  println(i)
}
```

The while loop in Groovy is also similar to the while loop in other programming languages.

```groovy
def i = 0
while (i < 5) {
  println(i)
  i++
}
```

## Arrays

Arrays in Groovy can be declared using square brackets.

```groovy
def numbers = [1, 2, 3, 4, 5]
println(numbers)
```

## Maps

Maps in Groovy are similar to dictionaries in other programming languages.

```groovy
def map = [firstName: "John", lastName: "Doe"]
println(map)
```

## Functions

Functions in Groovy are declared using the def keyword.

```groovy
def add(a, b) {
  return a + b
}
println(add(2, 3))
```

## Classes and Objects

Classes in Groovy can be declared using the class keyword.

```groovy
class Person {
  String firstName
  String lastName

  String getFullName() {
    return firstName + " " + lastName
  }
}

def person = new Person(firstName: "John", lastName: "Doe")
println(person.fullName)
```

This is a basic cheatsheet for Groovy programming language. There is much more to learn about Groovy, including its advanced features and functionality, and how to use it to build powerful and effective applications.
