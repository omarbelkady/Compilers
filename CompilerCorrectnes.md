# Compiler Correctness

## Theory
**Compiler correctness** ensures compiled code preserves source program behavior:
1. **Translation Validation**: Verify individual compiler passes.
2. **Verified Compilers**: Formally prove correctness (e.g., CompCert).
3. **Equivalence Checking**: Compare source and target behaviors.

## Example: Translation Validation in LLVM
```llvm
; Source IR: %x = add i32 2, 3
; Target IR: %x = 5
```