# Java Programming Language Cheatsheet

Java is a popular general-purpose programming language that is widely used for developing enterprise-scale applications, mobile applications, and games. It was first released by Sun Microsystems in 1995 and has since become one of the most widely used programming languages in the world. Java is known for its robustness, platform independence, and security features, making it a popular choice for building applications that require high performance and reliability.

## Supported Versions

| Java Version | Initial Release Date | Latest Patch Release | Release Date      | End of Support |
| ------------ | -------------------- | -------------------- | ----------------- | -------------- |
| Java 17 LTS  | September 14, 2021   | 17.0.2               | December 14, 2021 | September 2029 |
| Java 16 LTS  | March 16, 2021       | 16.0.2               | July 20, 2021     | March 2026     |
| Java 11 LTS  | September 25, 2018   | 11.0.13              | January 19, 2021  | September 2026 |
| Java 8 LTS   | March 18, 2014       | 8u302                | July 20, 2021     | December 2030  |

## Basic Syntax

When writing Java code, it's important to follow the language's syntax rules to ensure that your code is readable and easy to understand. Here are some basic syntax rules to keep in mind:

- Java is a case-sensitive language, so make sure to use the correct casing in your code.
- Class names should always start with a capital letter, while method names should start with a lowercase letter.
- Remember to use a semicolon (`;`) at the end of every statement to denote the end of the line of code.
- Code is written inside classes and methods, so be sure to define your code within the appropriate scope.
- The `main` method is the entry point of the program and is where the program starts execution.

## Variables

Variables must be declared with a data type before use (See [Primitive Data Types](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html))

- **Primitive Data types and limitations:**
  | Data Type | Size | Value | Default Value (for fields) | Description |
  | --------- | ---- | ----------------------------------------------- | --------------------------- | ----------- |
  | `boolean` | 1 bit | `true` or `false` | `false` | Represents a true/false value |
  | `int` | 4 bytes | -2^31 to 2^31-1 | `0` | Represents a 32-bit integer |
  | `float` | 4 bytes | up to 6-7 digits; must suffix 'f' to the number | `0.0f` | Represents a single-precision floating point number |
  | `double` | 8 bytes | up to 15 digits | `0.0d` | Represents a double-precision floating point number |
  | `char` | 2 bytes | single character/letter/Unicode | `'\u0000'` | Represents a Unicode character |
  | `String` | varies | sequence of characters | `null` | Represents a string of text though differs from the other types in that [`Strings`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/String.html) are [Object](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/Object.html) data types. |
  | `byte` | 1 byte | -128 to 127 | `0` | Represents an 8-bit integer |
  | `short` | 2 bytes | -2^15 to 2^15-1 | `0` | Represents a 16-bit integer |
  | `long` | 8 bytes | -2^63 to 2^63-1 | `0L` | Represents a 64-bit integer |

### Strings are immutable

[`Strings`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/String.html) in Java are immutable; their values cannot be changed after they are created. String literals have to be encompassed in double quotes.

To support mutable strings, Java provides both [StringBuilders](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/lang/StringBuilder.html) and [StringBuffers](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/StringBuffer.html), though it is worth mentioning that single-threated Java application [StringBuilders](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/lang/StringBuilder.html) are preferred.

Here are some examples of how strings can be used:

```java
System.out.println("abc"); // prints "abc"
String cde = "cde";
System.out.println("abc" + cde); // prints "abccde"
String c = "abc".substring(2, 3); // c is now "c"
String d = cde.substring(1, 2); // d is now "d"
```

Since Java's String class is immutable, we can create a new String object from an existing one, with some modifications.

For instance, the following code replaces all occurrences of the character 'a' with 'b' in a given string:

```java
String original = "banana";
String modified = original.replace('a', 'b');
System.out.println(original); // prints "banana"
System.out.println(modified); // prints "bbnbnb"
```

In this example, we create a new String object called modified from the original string by replacing all occurrences of the character `'a'` with `'b'`. Since the String class is immutable, the original string remains unchanged.

#### Fields

In Java, fields don't always require an initial value when they are declared. If a field is declared but not initialized, the compiler will set it to a default value that is typically zero or null, depending on the data type. It's generally considered poor programming practice to rely on these default values.

#### Final Declarations

Use `final` keyword to declare immutable constants

- Examples:

```java
  String name = "John";
  int age = 30;
  float salary = 25000.50f;
  double tax = 10.00;
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

- A blueprint for creating objects, defining their structure and behavior
- Fields (structure) and methods (behavior) can be found inside classes
- A class can also have a constructor, which a special method that initializes the state of an object
- An instance is an object that is created from a class
- Methods can operate on instances of classes (instance methods) or operate on the class as whole (static methods, which are declared with the `static` keyword)
- Examples:

```java
  class Student {
      // Fields
      int rollNo;
      String name;

      // Constructor
      public Student(int rollNo, String name) {
          this.rollNo = rollNo;
          this.name = name;
      }

      // Instance method
      void displayDetails() {
          System.out.println("Roll No: " + rollNo);
          System.out.println("Name: " + name);
      }

      // Static method
      static void displayJavaMessage() {
          System.out.println("I like java.");
      }
  }

  class Main {
      public static void main(String[] args) {
          // Creating an instance of Student class
          Student javaLearner = new Student(1, "John");

          // Calling instance method
          javaLearner.displayDetails();

          // Calling static method
          Student.displayJavaMessage();
      }
  }
```

## Object-Oriented Programming (OOP)

- A programming paradigm that relies on the concept of classes and objects
- Helps to structure and organize code into reusable, modular components, making it easier to maintain and extend the code over time
- The main principles promoted by OOP are abstraction, encapsulation, inheritance and polymorphism

## Abstract Classes

- A special type of class that cannot be instantiated and is intended to be extended by other classes (subclasses)
- Can be extended through the keyword `extends`, and all methods and properties are inherited in this process
- Provides a common structure and behavior for its subclasses
- Can contain abstract methods, which are methods that are declared but not implemented, apart from concrete methods
- Examples:

```java
abstract class Vehicle {
    abstract void startEngine();
}

class Car extends Vehicle {
    void startEngine() {
        System.out.println("Turning on the car engine");
    }
}

class Truck extends Vehicle {
    void startEngine() {
        System.out.println("Turning on the truck engine");
    }
}
```

## Interfaces

- An interface can be thought of as a set of rules (a contract)
- Can be implemented by other classes or extended by other interfaces through the keywords `implements` and `extends`, respectively
- When an interface is implemented by a class, the class must provide an implementation for each of the abstract methods defined in the interface
- Interfaces allow objects of different types to be used interchangeably as long as they implement the same interface, making it easier to write code that works with objects of different types
- Apart from abstract methods to be implemented, an interface can also contain default methods (methods with a default implementation) and constant fields
- Examples:

```java
interface Printable {
    void print();
}

class Book implements Printable {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public void print() {
        System.out.println(title + " by " + author);
    }
}

class Document implements Printable {
    private String name;
    private String format;

    public Document(String name, String format) {
        this.name = name;
        this.format = format;
    }

    public void print() {
        System.out.println(name + "." + format);
    }
}
```

## Keywords 'this' and 'super'

- The `this` keyword in Java is a reference to the current object, while `super` is a reference to the parent class of the current object
- Examples:

```java
class Animal {
    public void eat() {
        System.out.println("The animal is eating.");
    }
}

class Dog extends Animal {
    public void eat() {
        System.out.println("The dog is eating.");
    }
    public void eatWithSuper() {
        super.eat();
    }
    public void eatWithThis() {
        this.eat();
    }
}

class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eatWithSuper(); // Prints "The animal is eating."
        dog.eatWithThis(); // Prints "The dog is eating."
    }
}
```

## Overloading and overriding

- Method overloading is a feature where you can define multiple methods with the same name but with different parameters
- Examples:

```java
class Calculator {
    public int add(int x, int y) {
        return x + y;
    }

    public double add(double x, double y) {
        return x + y;
    }

    public int add(int x, int y, int z) {
        return x + y + z;
    }
}
```

- Method overriding is a feature where a subclass provides a specific implementation of a method that is already provided by its parent class
- Examples:

```java
class Animal {
    public void makeSound() {
        System.out.println("The animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("The dog barks");
    }
}
```

## Abstraction

- Abstraction refers to the act of creating a simplified representation of a more complex object or system
- Examples:

```java
interface Vehicle {
    void start();
}
class Car implements Vehicle {
    // Some sort of complex implementation for start() method, but we don't need to worry about it when using Vehicle interface
}
```

## Encapsulation

- Hides internal data and exposes the necessary functionalities through public methods
- The main purpose of encapsulation is to help you (or others) safely make changes to one part of your program without damaging other parts
- Examples:

```java
public class Car {
    // Private fields are encapsulated and cannot be accessed directly from outside Car
    // The methods, on the other hand, provide a public interface for interacting with a Car object
    private int speed;
    private boolean engineRunning;

    public void startEngine() {
        engineRunning = true;
    }

    public void stopEngine() {
        engineRunning = false;
    }

    public void setSpeed(int newSpeed) {
        if (engineRunning) {
            speed = newSpeed;
        } else {
            System.out.println("Cannot set speed - engine is not running");
        }
    }
}
```

## Inheritance

- Allows a new class to be based on an existing class, inheriting its fields and methods
- Examples:

```java
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Dog inherits eat() method
        dog.bark();
    }
}
```

## Polymorphism

- Refers to the ability of an object to take on many forms
- Polymorphism is usually achieved through method overriding and overloading
- Examples:

```java
class Animal {
    public void makeSound() {
        System.out.println("The animal makes a sound");
    }
}

class Cat extends Animal {
    public void makeSound() {
        System.out.println("Cat sound");
    }
}

class Dog extends Animal {
    public void makeSound() {
        System.out.println("Dog sound");
    }
}

class Main {
    public static void main(String[] args) {
        // Animal can take on different forms
        Animal animal1 = new Cat();
        Animal animal2 = new Dog();
        animal1.makeSound();
        animal2.makeSound();
    }
}
```

## Access Modifiers

- Access modifiers are keywords that determine the level of access to a variable, method or class
- In Java, there are four access modifiers: `public`, `private`, `protected` and `default` (no modifier, also known as package private)

| Access modifier | Within the same class | Within the same package | Subclasses | Global |
| --------------- | --------------------- | ----------------------- | ---------- | ------ |
| `public`        | Yes                   | Yes                     | Yes        | Yes    |
| `protected`     | Yes                   | Yes                     | Yes        | No     |
| `default`       | Yes                   | Yes                     | No         | No     |
| `private`       | Yes                   | No                      | No         | No     |

## Exceptions

- Exceptions are events which occur during the execution of a program and disrupt the normal flow of the program's instructions
- Exceptions can be _checked_ (checked at compile-time) or _unchecked_ (runtime event)
- Handling exceptions is important as it enables the program to recover from errors and provides a better user experience
- Exceptions can be handled by try-catch blocks (or be declared on a method signature to pass its handling to the caller)
- The `try` block contains the code that might throw an exception
- The `catch` block contains the code that handles the potential exception
- Also, the `finally` block contains code that will always be executed regardless of whether an exception is thrown or not
- Examples:

```java
public class DivideByZeroExample {
    public static void main(String[] args) {
        int a = 10,
        int b = 0;
        try {
            int c = a / b; // Dividing by zero will throw an ArithmeticException
            System.out.println("Result: " + c);
        } catch (ArithmeticException ae) {
            // Exception is handled here
        } finally {
            System.out.println("Finally block is being executed.");
        }
    }
}
```

```java
public class CallerExample {
    public static void main(String[] args) {
        try {
            runDangerousMethod();
        } catch (Exception e) {
            // Exception is handled here
        }
    }

    public static void runDangerousMethod() throws Exception {
        // Code that may throw an exception
    }
}
```

## Additional Resources

- [Official Java Documentation](https://docs.oracle.com/en/java/)
- [Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [Java Language Specification](https://docs.oracle.com/javase/specs/)
- [Java SE Downloads](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Java API Specification](https://docs.oracle.com/en/java/javase/16/docs/api/index.html)
- [/r/learnjava](https://reddit.com/r/learnjava)

These resources provide comprehensive and detailed information about the Java programming language, its syntax, libraries, and best practices for writing efficient and maintainable code. They also provide a wealth of examples, tutorials, and code samples to help you get started with Java programming and to deepen your understanding of the language. Whether you're a beginner or an experienced Java developer, these resources are essential references for your Java development projects.
