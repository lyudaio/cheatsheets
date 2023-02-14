# Basic Syntax

- Java is case-sensitive
- Class names start with a capital letter
- Method names start with a lowercase letter
- Use `;` at the end of every statement
- Code is written inside class and methods
- `main` method is the entry point of the program

## Variables

- Variables must be declared with a data type before use
- Data types and limitations:
  | Data Type | Size   | Yes/Reference | Value                                           |
  | --------- | ------ | :-----------: | ----------------------------------------------- |
  | `boolean` | 1 bit  |      Yes      | `true` or `false`                               |
  | `int`     | Yes    |      Yes      | -2 billion to 2 billion                         |
  | `float`   | Yes    |      Yes      | up to 6-7 digits; must suffix 'f' to the number |
  | `double`  | Yes    |      Yes      | up to 15 digits                                 |
  | `char`    | Yes    |      Yes      | single character/letter/ASCII                   |
  | `String`  | varies |   reference   | sequence of characters                          |
  | `byte`    | 1 byte |      Yes      | -128 to 127                                     |
  | `short`   | Yes    |      Yes      | -32,768 to 32,767                               |
  | `long`    | Yes    |      Yes      | -9 quintillion to 9 quintillion                 |
- Use `final` keyword to declare immutable constants
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

## This and super keywords

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
        dog.eatWithSuper(); // prints "The animal is eating."
        dog.eatWithThis(); // prints "The dog is eating."
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
  void stop();
}
```


## Encapsulation

- Hides data and exposes necessary functionality via methods
- Examples:
```java
class BankAccount {
  private double balance;

  public void deposit(double amount) {
    balance += amount;
  }

  public void withdraw(double amount) {
    balance -= amount;
  }

  public double getBalance() {
    return balance;
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
        dog.eat(); // prints "Animal is eating"
        dog.bark(); // prints "Dog is barking"
    }
}
```


## Polymorphism

- The ability of an object to take on many forms
- Examples:
```java 
class Math {
  int add(int a, int b) {
    return a + b;
  }

  double add(double a, double b) {
    return a + b;
  }
}
```


## Access Modifiers

- Access modifiers are keywords that determine the level of access to a variable, method or class.
- In Java, there are four access modifiers: `public`, `private`, `protected` and `default`.
  
| Access modifier | Within the same class | Within the same package | Subclasses | Global |
| --------------- | --------------------- | ----------------------- | ---------- | ------ |
| `public`        | Yes                   | Yes                     | Yes        | Yes    |
| `protected`     | Yes                   | Yes                     | Yes        | No     |
| `default`       | Yes                   | Yes                     | No         | No     |
| `private`       | Yes                   | No                      | No         | No     |