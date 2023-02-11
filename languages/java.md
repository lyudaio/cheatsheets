## Basic Syntax

- Java is case-sensitive
- Class names start with a capital letter
- Method names start with a lowercase letter
- Use `;` at the end of every statement
- Code is written inside class and methods
- `main` method is the entry point of the program

## Variables

- Use `int`, `float`, `double`, `char`, `boolean` to declare variables
- Variables must be declared before use
- `final` keyword is used for constants
- Examples:
```java
  int age = 30;
  float salary = 25000.50f;
  char gender = 'M';
  boolean isMarried = true;
```

## Operators

- Arithmetic operators: `+`, `-`, `*`, `/`, `%`
- Relational operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Logical operators: `&&`, `||`, `!`
- Assignment operators: `=`, `+=`, `-=`, `*=`, `/=`, `%=`

## Conditional Statements

- `if` statement
- `if-else` statement
- `switch` statement

## Loops

- `for` loop
- `while` loop
- `do-while` loop

## Arrays

- Array is a collection of similar data types
- Array index starts from `0`
- Examples:
```java
  int[] marks = new int[5];
  marks[0] = 85;
  marks[1] = 90;
  marks[2] = 80;
```

## Methods

- Reusable blocks of code
- Can accept parameters and return values
- Examples:
```java
  public int addNumbers(int a, int b) {
      return a + b;
  }
  public void sayHello() {
      System.out.println("Hello");
  }
```

## Classes

- Blueprint for creating objects
- Variables and methods inside a class
- Examples:
```java
  class Student {
      int rollNo;
      String name;
      void displayDetails() {
          System.out.println("Roll No: " + rollNo);
          System.out.println("Name: " + name);
      }
  }
```
