# Data Types

## Scalars

### Integers

- Rust has the expected range of integer types

|Length|Signed|Unsigned|
|--|--|--|
|8-bit|	i8|	u8|
|16-bit|	i16|	u16|
|32-bit|	i32|	u32|
|64-bit|	i64|	u64|
|128-bit|	i128|	u128|
|arch|	isize|	usize|

- Integer types can be defined with suffixes to literals
```rust
57u8
```

- `_` can be used as a separator to break up large numbers for readability
- Hex, binary and octal can be used by suffixing literals

```rust
0xff // hex
0o77 // octal
0b1111_0000 // binary
```

### Floating Points

- Rust implements [IEEE-754](https://en.wikipedia.org/wiki/IEEE_754)

### Bools

```rust
let t = true;
let f: bool = false; // with explicit type annotation
```

### Characters

- Rust characters are unicode by default
```rust
let c = 'z';
let z: char = 'ℤ'; // with explicit type annotation
let heart_eyed_cat = '😻';
```

## Compound Types

- used to group multiple scalar types together
- two native compound types, tuples and arrays

### Tuples

- types of tuple vars can be explicit, or implicit
```rust
let tup: (i32, f64, u8) = (500, 6.4, 1);
let tup = (500, 6.4, 1);
```
- we can destructure tuples into vars similar to JS
```rust
let tup = (500, 6.4, 1);
let (x, y, z) = tup;
```
- tuple vars can be accessed by their index
```rust
let x: (i32, f64, u8) = (500, 6.4, 1);

let five_hundred = x.0;
let six_point_four = x.1;
let one = x.2;
```

### Arrays

- arrays are declared similarly to Python or JS
```rust
let a = [1, 2, 3, 4, 5];
```
- we can specify the length and type of an array
```rust
let a: [i32; 5] = [1, 2, 3, 4, 5];
```
- array access is also similar to Python or JS
```rust
let a = [1, 2, 3, 4, 5];

let first = a[0];
let second = a[1];
```
- accessing elements outside the bounds of the array result in a runtime error, rather than letting you access bad memory like in C