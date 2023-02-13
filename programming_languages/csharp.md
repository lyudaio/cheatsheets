# C# Cheatsheet

C# is a modern, object-oriented programming language developed by Microsoft. It is used to develop a wide range of applications, including desktop applications, mobile applications, and web applications.

## Variables

Variables are containers for storing data values. In C#, variables must be declared before they can be used and they have a specific data type that determines what kind of data they can store.

```C#
int x = 10;
float y = 20.5f;
string name = "John Doe";
```

## Conditional Statements

Conditional statements allow you to make decisions based on certain conditions. The `if` statement is used to execute a block of code only if a specified condition is true.

```C#
int x = 10;
if (x > 5) {
  Console.WriteLine("x is greater than 5");
}
```

## Loops

Loops are used to repeat a block of code multiple times. The `for` loop is used to execute a block of code a specified number of times.

```C#
for (int i = 0; i < 10; i++) {
  Console.WriteLine(i);
}
```

## Arrays

Arrays are data structures that store multiple values in a single variable.

```C#
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
foreach (int number in numbers) {
  Console.WriteLine(number);
}
```

## Methods

Methods are blocks of code that perform a specific task. They can be called multiple times in a program.

```C#
static void PrintHello() {
  Console.WriteLine("Hello World!");
}
```

## Classes and Objects

Classes are blueprint for creating objects, a blueprint defines a set of attributes and behaviors. Objects are instances of classes.

```C#
class Car {
  public string Brand;
  public string Model;
  public int Year;

  public void StartEngine() {
    Console.WriteLine("Engine started!");
  }
}
```

## Exception Handling

Exception handling is a mechanism for handling errors and exceptional conditions that may occur in a program.

```C#
try {
  int x = 10;
  int y = 0;
  if (y == 0) {
    throw new DivideByZeroException();
  }
  int z = x / y;
} catch (DivideByZeroException ex) {
  Console.WriteLine("Error: division by zero.");
}
```
