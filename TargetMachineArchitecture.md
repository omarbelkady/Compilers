# Target Machine Architecture

## Theory
Code generation depends on the target architecture:
1. **Stack Machines**: Operations push/pop a stack (e.g., JVM).
2. **Register Machines**: Operations use explicit registers (e.g., x86).
3. **SIMD Architectures**: Parallel vector units (e.g., AVX, NEON).

## Example: JVM Stack-Based Bytecode
```jvm
iload_1   ; Push local variable 1 onto stack
iload_2   ; Push local variable 2
iadd      ; Pop two values, add, push result
istore_3  ; Pop result into local variable 3
```