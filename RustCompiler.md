# Rust Compiler Internals

## Theory
The **Rust compiler** (rustc) enforces memory safety via:
1. **Ownership**: Each value has a single owner.
2. **Borrow Checker**: Tracks references at compile time.
3. **MIR (Mid-Level IR)**: Simplified IR for borrow checking and optimizations.

## Example: MIR for a Function
```rust
fn add(a: i32, b: i32) -> i32 {
    a + b
}

// MIR:
// _0 = CheckedAdd(a, b)
// return _0
```