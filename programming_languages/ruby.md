# Ruby Cheatsheet

Ruby is a dynamic, object-oriented, general-purpose programming language. It was created in the mid-1990s by Yukihiro "Matz" Matsumoto in Japan.

## Variables

In Ruby, variables do not need to be declared before they are used. You simply assign a value to a variable with the `=` operator.

```ruby
name = "John Doe"
puts name
```

## Arrays

An array is an ordered collection of objects. In Ruby, you can create an array using square brackets `[]`.

```ruby
names = ["John", "Jane", "Jim"]
puts names[0] # prints "John"
```

## Hashes

A hash is similar to an array, but instead of accessing elements with an index, you access them with a key.

```ruby
person = { "name" => "John Doe", "age" => 30 }
puts person["name"] # prints "John Doe"
```

## Control Flow

### If/Else

```ruby
age = 20
if age >= 18
  puts "You are an adult"
else
  puts "You are a minor"
end
```

### Loops

#### For Loop

```ruby
for i in 0..9
  puts i
end
```

#### While Loop

```ruby
counter = 0
while counter < 10
  puts counter
  counter += 1
end
```

## Methods

Methods are blocks of code that can be called multiple times with different arguments. In Ruby, you define a method using the `def` keyword.

```ruby
def say_hello(name)
  puts "Hello, #{name}!"
end

say_hello("John")
```

## Classes and Objects

In Ruby, everything is an object, and classes are used to create new objects.

```ruby
class Person
  def initialize(name, age)
    @name = name
    @age = age
  end

  def say_hello
    puts "Hello, my name is #{@name} and I am #{@age} years old."
  end
end

person = Person.new("John Doe", 30)
person.say_hello
```
