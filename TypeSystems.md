# Type Systems in Compilers

## Theory
**Type systems** enforce correctness by checking operations on data. Key concepts:
1. **Static vs. Dynamic Typing**:
   - Static: Types checked at compile time (e.g., Java).
   - Dynamic: Types checked at runtime (e.g., Python).
2. **Type Inference**: Deduce types without explicit annotations (e.g., Haskell, Rust).
3. **Polymorphism**: Ad-hoc (overloading) vs. parametric (generics).

## Example: Simple Type Checker
```rust
fn add(x: i32, y: i32) -> i32 {
    x + y
}
// Error: add("hello", 5) → type mismatch.

```
Case Study: TypeScript’s Structural Typing
Problem: JavaScript’s dynamic types caused runtime errors.

Solution:

TypeScript uses structural typing: compatibility based on shape, not name.

Example: { name: string } is compatible with { name: string, age?: number }.

Outcome: Safer code with minimal annotations.

Challenges
Complex Types: Handling generics, dependent types.

Performance: Type inference algorithms (e.g., Hindley-Milner) can be slow.

