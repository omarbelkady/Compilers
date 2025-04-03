### Control Flow Analysis

## Theory
**Control flow analysis** models program execution paths:
1. **Basic Blocks**: Sequences of instructions with no branches.
2. **Control Flow Graph (CFG)**: Nodes = blocks, edges = branches.
3. **Dominators**: Block `A` dominates `B` if all paths to `B` pass through `A`.

## Example: CFG for a Simple Function
```c
void foo(int x) {
    if (x > 0) {
        printf("positive");
    } else {
        printf("non-positive");
    }
}
```