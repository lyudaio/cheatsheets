# Rust (1.57.0)

Rust is a systems programming language that runs blazingly fast, prevents segfaults, and guarantees thread safety. It is used for low-level system programming, game development, and web assembly.

## Variables

Variables in Rust are declared with the `let` keyword and are either immutable (cannot be changed) or mutable (can be changed).

```rust
// Declare an immutable variable
let x = 5;

// Declare a mutable variable
let mut y = 10;
y = 20;
```

### Data Types

Rust has a rich set of built-in data types, including integers, floating-point numbers, booleans, and characters.

```rust
// Integer types
let i8: i8 = -128;
let i16: i16 = -32768;
let i32: i32 = -2147483648;
let i64: i64 = -9223372036854775808;
let i128: i128 = -170141183460469231731687303715884105728;
let u8: u8 = 255;
let u16: u16 = 65535;
let u32: u32 = 4294967295;
let u64: u64 = 18446744073709551615;
let u128: u128 = 340282366920938463463374607431768211455;

// Floating-point types
let f32: f32 = 3.14;
let f64: f64 = 3.14159265358979323846;

// Boolean type
let b: bool = true;

// Character type
let c: char = 'A';
```

### Arrays and Tuples

Arrays in Rust have a fixed size and are stored on the stack, while tuples are ordered, heterogeneous collections that can be stored on the stack or the heap.

```rust
// Array
let a = [1, 2, 3];

// Tuple
let t = (1, "Hello");
```

### Functions

Functions in Rust are declared with the `fn` keyword and can return values or be declared as void.

```rust
// Function that returns a value
fn sum(a: i32, b: i32) -> i32 {
    a + b
}

// Void function
fn print_hello() {
    println!("Hello");
}
```

### Ownership and Borrowing

Rust has a unique ownership model that ensures safety and eliminates data races. When a variable goes out of scope, its value is dropped and its memory is freed.

```rust
fn main() {
    let s = String::from("Hello");
    let t = s;
    // s can no longer be used here

    let x = 5;
    let y = &x;
    // Both x and y can be used here
}
```

### Concurrency

Rust provides multiple tools to handle concurrency.

#### Threads

Rust supports multi-threading through the `std::thread` module. You can create a new thread using the `spawn` method.

```rust
use std::thread;

fn main() {
    let handle = thread::spawn(|| {
        println!("Running in a new thread");
    });

    handle.join().unwrap();
}
```

#### Channels

Channels allow you to safely send values between threads. A `Sender` instance can send values to a `Receiver` instance, creating a one-way communication channel.

```rust
use std::sync::mpsc;
use std::thread;

fn main() {
    let (tx, rx) = mpsc::channel();

    let handle = thread::spawn(move || {
        let val = String::from("Hello from the thread");
        tx.send(val).unwrap();
    });

    let received = rx.recv().unwrap();
    println!("Received: {}", received);

    handle.join().unwrap();
}
```
