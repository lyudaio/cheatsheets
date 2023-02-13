# TypeScript

TypeScript is a statically typed, object-oriented programming language that builds on top of JavaScript. It is designed to provide optional type annotations and increased code maintainability, scalability, and readability.

## Basic Types

TypeScript supports the following basic types:

```typescript
let name: string = 'John Doe';
let age: number = 30;
let isMarried: boolean = true;
let children: string[] = ['Jane', 'John'];
let person: [string, number, boolean] = ['John Doe', 30, true];
```

### Interfaces

Interfaces define the structure of objects and are used to enforce type contracts.

```typescript
interface Person {
  name: string;
  age: number;
}

let john: Person = {
  name: 'John Doe',
  age: 30
};
```

### Classes

Classes are used to create objects and enforce object-oriented programming principles.

```typescript
class Person {
  name: string;
  age: number;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }
}

let john = new Person('John Doe', 30);
```

### Functions

Functions are used to execute blocks of code.

```typescript
function greet(name: string): void {
  console.log(`Hello, ${name}!`);
}

greet('John Doe');
```

### Generics

Generics allow functions, classes, and interfaces to accept a variety of types, rather than being limited to a specific type.

```typescript
function identity<T>(arg: T): T {
  return arg;
}

let output = identity<string>('Hello, world!');
```
