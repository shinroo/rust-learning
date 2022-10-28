# Functions

- function declaration in Rust is very similar to Go
```rust
fn main() {
    println!("Hello, world!");

    another_function();
}

fn another_function() {
    println!("Another function.");
}
```

- parameters can be specified

```rust
fn main() {
    another_function(5);
}

fn another_function(x: i32) {
    println!("The value of x is: {x}");
}
```

- distinction between statements and expressions: expressions return values

```rust
// not allowed, can't assign a statment
fn main() {
    let x = (let y = 6);
}

// allowed, can assign expressions
fn main() {
    let y = {
        let x = 3;
        x + 1
    };

    println!("The value of y is: {y}");
}
```

- return values in rust are statements

```rust
fn five() -> i32 {
    5
}
```
