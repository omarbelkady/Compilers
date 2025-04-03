# LLVM Deep Dive

## Theory
**LLVM** is a modular compiler infrastructure with three pillars:
1. **Frontend**: Clang (C/C++), Rustc, etc., generating LLVM IR.
2. **Middle-end**: Optimizations (e.g., loop unrolling, SROA).
3. **Backend**: Target codegen (x86, ARM, etc.).

**LLVM IR**:
- Typed, SSA-form intermediate representation.
- Supports metadata for debugging and optimization.

## Example: LLVM IR for a Function
```llvm
define i32 @add(i32 %a, i32 %b) {
  %result = add i32 %a, %b
  ret i32 %result
}
```
