# Swift Cheatsheet

This cheatsheet contains the essential syntax and concepts of Swift programming language.

`Latest LTS: Swift 5.5`

## Basics

### Variables and Constants

```swift
// Declaring variables
var variableName: DataType = value

// Declaring constants
let constantName: DataType = value
```

### Optional Values

```swift
// Optional variable
var optionalValue: DataType? = nil

// Unwrap optional variable
if let value = optionalValue {
    // use value
}

// Force unwrap optional variable (can cause runtime error if value is nil)
let value = optionalValue!
```

### Optionals Chaining

```swift
// Optional chaining
var value = optionalVariable?.property
```

### Typealias

```swift
typealias NewName = ExistingType
```

### Tuples

```swift
let tupleName = (value1, value2, value3)

// Access tuple values
tupleName.0
tupleName.1
tupleName.2

// Named tuple values
let namedTuple = (value1: 10, value2: "text")
namedTuple.value1
namedTuple.value2
```

### Loops

```swift
// for loop
for item in collection {
    // code block
}

// while loop
while condition {
    // code block
}

// repeat-while loop
repeat {
    // code block
} while condition
```

### Conditionals

```swift
if condition {
    // code block
} else if condition2 {
    // code block
} else {
    // code block
}
```

### Functions

```swift
func functionName(parameterName: DataType) -> ReturnType {
    // code block
    return value
}

// Function call
functionName(parameterName: value)
```

### Closures

```swift
{ (parameters) -> ReturnType in
    // code block
    return value
}
```

## Advanced

### Enumerations

```swift
enum EnumerationName {
    case case1
    case case2
}

// Accessing enum values
let variable = EnumerationName.case1
```

### Structs

```swift
struct StructName {
    var property1: DataType
    var property2: DataType

    // Methods
    func methodName() -> ReturnType {
        // code block
        return value
    }
}

// Struct initialization
let variable = StructName(property1: value1, property2: value2)

// Accessing struct properties
variable.property1
variable.property2

// Calling struct methods
variable.methodName()
```

### Classes

```swift
class ClassName: SuperclassName, ProtocolName {
    var property: DataType
    var computedProperty: DataType {
        // get set
    }

    // Methods
    func methodName() -> ReturnType {
        // code block
        return value
    }

    // Class initialization
    init(property: DataType) {
        self.property = property
    }
}

// Object creation
let object = ClassName(property: value)

// Accessing object properties
object.property

// Calling object methods
object.methodName()
```

### Extensions

```swift
extension ExistingType {
    // New properties and methods
}

// Extension usage
existingObject.newMethod()
```

### Protocols

```swift
protocol ProtocolName {
    // Properties and methods
}

// Class/Struct/Enum adoption
class ClassName: ProtocolName {
    // Implement protocol properties and methods
}
```

## Official Documentation

- [The Swift Programming Language](https://docs.swift.org/swift-book/)
- [Swift Standard Library](https://developer.apple.com/documentation/swift)
- [Apple Developer](https://developer.apple.com/documentation/)
