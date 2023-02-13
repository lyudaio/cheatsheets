# D Programming Language Cheatsheet

D is a statically-typed, multi-paradigm system programming language created by Walter Bright of Digital Mars. It is known for its high performance, modern features and its interoperability with C code.

## Variables

In D, variables are declared with a specific type and can be mutable or immutable:

```D
// Mutable variable
int x = 10;
x = 20;

// Immutable variable
const int y = 10;
y = 20; // Error: cannot modify a const
```

## Functions

Functions are declared using the `void` return type, or with a specific return type:

```D
void printHello()
{
    writeln("Hello");
}

int add(int a, int b)
{
    return a + b;
}
```

## Conditional Statements

Conditional statements in D use the `if` and `switch` keywords:

```D
int x = 10;

if (x < 20)
{
    writeln("x is less than 20");
}
else if (x == 20)
{
    writeln("x is equal to 20");
}
else
{
    writeln("x is greater than 20");
}

switch (x)
{
    case 10:
        writeln("x is 10");
        break;
    case 20:
        writeln("x is 20");
        break;
    default:
        writeln("x is not 10 or 20");
        break;
}
```

## Arrays

Arrays in D are declared with a specific type and size:

```D
int[] arr = [1, 2, 3, 4, 5];

foreach (int element; arr)
{
    writeln(element);
}
```

## Classes and Objects

D supports object-oriented programming, with classes and objects:

```D
class Person
{
    string name;
    int age;

    void printInfo()
    {
        writeln("Name: ", name);
        writeln("Age: ", age);
    }
}

auto person = new Person();
person.name = "John Doe";
person.age = 30;
person.printInfo();
```

## Conclusion

This cheatsheet has covered some of the basic elements of the D programming language. There are many more features and advanced concepts in D that are not covered here. To learn more about D, refer to the official D documentation and resources.
