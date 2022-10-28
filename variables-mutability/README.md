# Variables and Mutability

Take aways:
- variables are mutable by default
- mutability can be opted into with
```rust
let mut x = 5; 
```
- alternative to mutable variables is shadowing
```rust
let x = 5;
let x = 6;
```
- constants can't be made mutable
```rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
```