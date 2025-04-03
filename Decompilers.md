
### Decompilers

## Theory
**Decompilers** reverse-engineer machine code/bytecode into high-level source code. Steps:
1. **Control Flow Recovery**: Reconstruct loops and conditionals.
2. **Type Inference**: Guess variable types from usage patterns.
3. **Pattern Matching**: Replace assembly idioms with high-level constructs.

## Example: Ghidra’s Decompilation
```c
// Original C code
int add(int a, int b) {
    return a + b;
}

// Decompiled output (simplified)
int add(int param1, int param2) {
    return param1 + param2;
}
```