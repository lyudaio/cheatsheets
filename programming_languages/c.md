# Variables

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
