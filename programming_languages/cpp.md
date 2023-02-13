# C++ Cheatsheet

C++ is an object-oriented, high-level programming language that is widely used for developing a wide range of applications, including system software, video games, and business applications.

## Variables

Variables in C++ are declared with a type and a name, and can be assigned a value. The following are some of the basic data types in C++:

```c++
    int a = 10;
    float b = 20.5;
    char c = 'a';
    string d = "hello";
```

## Operators

C++ supports a wide range of operators, including arithmetic, comparison, and logical operators.

```c++
    int a = 10;
    int b = 20;

    // Arithmetic operators
    int sum = a + b;
    int difference = a - b;
    int product = a * b;
    int quotient = a / b;

    // Comparison operators
    int equal = (a == b);
    int not_equal = (a != b);
    int greater_than = (a > b);
    int less_than = (a < b);

    // Logical operators
    int and_result = (a == 10) && (b == 20);
    int or_result = (a == 10) || (b == 20);
    int not_result = !(a == 10);
```

## Control Structures

C++ supports a number of control structures, including `if` statements, `for` loops, `while` loops, and `switch` statements.

```c++
    int i;
    // If statement
    if (i > 10) {
        cout << "i is greater than 10" << endl;
    } else if (i < 10) {
        cout << "i is less than 10" << endl;
    } else {
        cout << "i is equal to 10" << endl;
    }

    // For loop
    for (i = 0; i < 10; i++) {
        cout << i << endl;
    }

    // While loop
    while (i < 20) {
        cout << i << endl;
        i++;
    }

    // Switch statement
    switch (i) {
        case 10:
            cout << "i is 10" << endl;
            break;
        case 20:
            cout << "i is 20" << endl;
            break;
        default:
            cout << "i is not 10 or 20" << endl;
    }
```

## Functions

Functions in C++ are declared with a return type, a name, and a list of parameters. Functions can be called from other parts of the code.

```c++
    int add(int a, int b) {
        return a + b;
    }

    int result = add(10, 20);
    cout << result << endl;
```

## Classes and Objects

C++ allows the creation of classes, which are essentially custom data types that can be used to represent real-world objects. A class defines the structure and behavior of objects, and objects are instances of classes.

```
class Car {
  public:
    string brand;
    string model;
    int year;

    void startEngine() {
      cout << "Engine started!" << endl;
    }
};
```

To create an object of a class, we use the following syntax:

```
Car myCar;
myCar.brand = "Toyota";
myCar.model = "Camry";
myCar.year = 2020;
```

### Functions

Functions in C++ allow you to encapsulate a block of code that performs a specific task. Functions can be defined inside classes as well as outside of classes.

```
void printHello() {
  cout << "Hello World!" << endl;
}

int addNumbers(int a, int b) {
  return a + b;
}
```

### Pointers

Pointers are variables that hold the memory address of another variable. They allow for dynamic memory allocation and can be used for more efficient memory usage.

```
int x = 10;
int *ptr = &x;
cout << "The value of x is: " << x << endl;
cout << "The address of x is: " << ptr << endl;
```

### Standard Template Library (STL)

The Standard Template Library (STL) is a collection of templates and algorithms that provide common data structures and operations. Some of the most commonly used STL components are `vector`, `map`, and `string`.

```
#include <vector>
#include <string>

vector<int> numbers;
numbers.push_back(1);
numbers.push_back(2);
numbers.push_back(3);

string name = "John Doe";
```

### Exception Handling

Exception handling is a mechanism for handling errors and exceptional conditions that may occur in a program.

```
try {
  int x = 10;
  int y = 0;
  if (y == 0) {
    throw string("division by zero");
  }
  int z = x / y;
} catch (string &e) {
  cout << "Error: " << e << endl;
}
```
