# Variables

In PHP, variables are declared using the "$" symbol. The data type of the variable is determined automatically based on its value.

```php
    $name = "John Doe";
    $age = 30;
    $is_student = false;
```

## Data Types

PHP supports the following data types:

- String
- Integer
- Float
- Boolean
- Array
- Object
- Null

```php
    $name = "John Doe";    // String
    $age = 30;            // Integer
    $price = 19.99;       // Float
    $is_student = false;  // Boolean
    $colors = array("red", "green", "blue");  // Array
    $person = new Person();  // Object
    $value = null;        // Null
```

## Arithmetic Operations

PHP supports the following arithmetic operations:

- Addition (+)
- Subtraction (-)
- Multiplication (\*)
- Division (/)
- Modulus (%)
- Exponentiation (\*\*)

```php
    $a = 10;
    $b = 20;
    $c = $a + $b;
    $d = $a - $b;
    $e = $a * $b;
    $f = $a / $b;
    $g = $a % $b;
    $h = $a ** $b;
```

## Conditional Statements

PHP supports the following conditional statements:

- If statement
- If...else statement
- If...elseif...else statement
- Switch statement

```php
    // If statement
    if ($a > $b) {
        echo "a is greater than b";
    }

    // If...else statement
    if ($a > $b) {
        echo "a is greater than b";
    } else {
        echo "a is not greater than b";
    }

    // If...elseif...else statement
    if ($a > $b) {
        echo "a is greater than b";
    } elseif ($a == $b) {
        echo "a is equal to b";
    } else {
        echo "a is less than b";
    }

    // Switch statement
    switch ($a) {
        case 10:
            echo "a is 10";
            break;
        case 20:
            echo "a is 20";
            break;
        default:
            echo "a is not 10 or 20";
            break;
    }
```

## Looping Constructs

PHP supports the following looping constructs:

- For loop
- Foreach loop
- While loop
- Do...while loop

```php
    // For loop
    for ($i = 0; $i < 10; $i++) {
        echo $i;
    }

    // Foreach loop
    $colors = array("red", "green", "blue");
    foreach ($colors as $color) {
        echo $color;
    }

    // While loop
    $i = 0;
    while ($i < 10) {
        echo $i;
        $i++;
    }

    // Do...while loop
    $i = 0;
    do {
        echo $i;
        $i++;
    } while ($i < 10);
```

## Functions

PHP supports the creation of custom functions. Functions are declared using the "function" keyword and can accept parameters.

```php
    function greet($name) {
        return "Hello, " . $name;
    }

    echo greet("John Doe");
```

## Classes and Objects

PHP supports object-oriented programming through classes and objects. A class is a blueprint for creating objects, and an object is an instance of a class.

```php
    class Person {
        public $name;
        public $age;

        public function __construct($name, $age) {
            $this->name = $name;
            $this->age = $age;
        }

        public function greet() {
            return "Hello, my name is " . $this->name . " and I am " . $this->age . " years old.";
        }
    }

    $person = new Person("John Doe", 30);
    echo $person->greet();
```

## File Input/Output

PHP supports reading from and writing to files on the server. The following example demonstrates how to write a string to a file.

```php
    $file = fopen("test.txt", "w");
    fwrite($file, "Hello World!");
    fclose($file);
```

And the following example demonstrates how to read from a file.

```php
    $file = fopen("test.txt", "r");
    $content = fread($file, filesize("test.txt"));
    fclose($file);
    echo $content;
```
