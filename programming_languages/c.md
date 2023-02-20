# Introduction to C

C is a general-purpose programming language that was developed in the 1970s by Dennis Ritchie at Bell Labs. It is a compiled language, meaning that the source code is translated into machine code before being executed. C is a powerful language that is widely used for system programming, embedded systems, and high-performance applications.

C has a concise syntax that allows for efficient and powerful code. It is a low-level language that provides direct access to memory and hardware, making it a popular choice for developing operating systems, device drivers, and other system-level software.

The latest LTS (Long Term Support) version of C is C17, released in 2018. It introduced several new features, including improvements to the standard library and support for Unicode characters.

## Basic Syntax

The basic syntax of C is similar to many other programming languages. A C program consists of a series of functions, each of which contains a sequence of statements. The main function is the entry point of the program and is called when the program starts.

```c
#include <stdio.h>

int main() {
    printf("Hello, world!\n");
    return 0;
}
```

- This program uses the `printf` function to print the message "Hello, world!" to the console.

## Data Types

| Data Type            | Description                                   | Format Specifier        | Size (bytes) | Range                           |
| -------------------- | --------------------------------------------- | ----------------------- | ------------ | ------------------------------- |
| `char`               | A single character                            | `%c`                    | 1            | -128 to 127 or 0 to 255         |
| `signed char`        | A signed character                            | `%c`                    | 1            | -128 to 127                     |
| `unsigned char`      | An unsigned character                         | `%c`                    | 1            | 0 to 255                        |
| `short`              | A short integer                               | `%hd` or `%hi`          | 2            | -32,768 to 32,767               |
| `unsigned short`     | An unsigned short integer                     | `%hu`                   | 2            | 0 to 65,535                     |
| `int`                | An integer                                    | `%d` or `%i`            | 4            | -2,147,483,648 to 2,147,483,647 |
| `unsigned int`       | An unsigned integer                           | `%u`                    | 4            | 0 to 4,294,967,295              |
| `long`               | A long integer                                | `%ld` or `%li`          | 4 or 8\*     | -2,147,483,648 to 2,147,483,647 |
| `unsigned long`      | An unsigned long integer                      | `%lu`                   | 4 or 8\*     | 0 to 4,294,967,295              |
| `long long`          | A long long integer                           | `%lld` or `%lli`        | 8            | -(2^63) to (2^63)-1             |
| `unsigned long long` | An unsigned long long integer                 | `%llu`                  | 8            | 0 to (2^64)-1                   |
| `float`              | A single-precision floating-point number      | `%f` or `%e` or `%g`    | 4            | 3.4E-38 to 3.4E+38              |
| `double`             | A double-precision floating-point number      | `%lf` or `%le` or `%lg` | 8            | 1.7E-308 to 1.7E+308            |
| `long double`        | A long double-precision floating-point number | `%Lf` or `%Le` or `%Lg` | 12 or 16\*   | 3.4E-4932 to 1.1E+4932          |
| `void`               | A generic pointer                             | N/A                     | N/A          | N/A                             |

- The size of long and long double may vary depending on the compiler and platform.

## Variables

Variables in C are declared with a type and a name, and can be assigned a value. The following are some of the basic data types in C:

```c
    int a = 10;
    float b = 20.5;
    char c = 'a';
```

## Operators

C supports a wide range of operators, including arithmetic, comparison, and logical operators.

```c
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

C supports a number of control structures, including `if` statements, `for` loops, and `while` loops.

```c
    int i;
    // If statement
    if (i > 10) {
        printf("i is greater than 10");
    } else if (i < 10) {
        printf("i is less than 10");
    } else {
        printf("i is equal to 10");
    }

    // For loop
    for (i = 0; i < 10; i++) {
        printf("%d\n", i);
    }

    // While loop
    while (i < 20) {
        printf("%d\n", i);
        i++;
    }
```

## Functions

Functions in C are declared with a return type, a name, and a list of parameters. Functions can be called from other parts of the code.

```c
    int add(int a, int b) {
        return a + b;
    }

    int result = add(10, 20);
    printf("%d\n", result);
```

## Pointers

Pointer in C is a variable that stores memory address of another variable.

```c
    // Simple example of creating a pointer and using it
    int number = 128;
    int *intPointer = &number;
    int numberCopied = *intPointer;
```

Syntax regarding pointers simply put is as follows:

- '&' Sign before variable name means access to memory adress of that variable.
- '\*' Before variable name can mean either:
  1. On definition, specyfying variable being a pointer (int \*intPointer).
  2. On assignment, accessing data of variable on that memory adress (int numberCopied = \*intPointer).

Note that every pointer should have an assigned data type it points to (int*, char* ...), with exception of void\* that can have assigned any data type.

## Structs

Structs are data containers used to store several variables together (struct variables are called members).

Struct definition:

```c
    struct Entity {
        int positionX;
        int positionY;
    };
```

Struct usage:

```c
// Creating an "Entity" struct with members positionX and positionY equal to 0
struct Entity e1 = {0,0};

// Accessing and changing members of a struct
e1.positionX += 10;
e1.positionY += 5;
```
