# Crystal (0.35.1)

Crystal is a statically-typed, object-oriented programming language that aims to have the syntax and performance of Ruby. It is designed to be fast and efficient, allowing developers to write high-performance code that is easy to read and maintain.

## Hello World

A classic "Hello World" program in Crystal:

```ruby
puts "Hello World"
```

## Variables

Variables in Crystal are declared with the `var` keyword. The type of the variable can be explicitly set or inferred from the value assigned to it:

```ruby
var name = "Alice"      # Inferred type is String
var age : Int32 = 30    # Explicitly set as Int32
```

## Arrays

Arrays in Crystal are declared using square brackets:

```ruby
array = [1, 2, 3]
puts array[0]   # Outputs 1
```

## Hashes

Hashes (also known as dictionaries or associative arrays) in Crystal are declared using curly braces:

```ruby
hash = { "name" => "Alice", "age" => 30 }
puts hash["name"]   # Outputs "Alice"
```

## Functions

Functions in Crystal are declared using the `def` keyword. They can take parameters and return a value:

```ruby
def greet(name : String) : String
  return "Hello, #{name}"
end

puts greet("Alice")   # Outputs "Hello, Alice"
```

## Classes

Classes in Crystal are declared using the `class` keyword. They can have properties and methods:

```ruby
class Person
  property name : String
  property age : Int32

  def initialize(@name, @age)
  end

  def greet
    return "Hello, I am #{@name} and I am #{@age} years old."
  end
end

person = Person.new("Alice", 30)
puts person.greet   # Outputs "Hello, I am Alice and I am 30 years old."
```
