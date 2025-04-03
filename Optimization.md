
# Introduction to Code Optimization

## Theory
**Optimization** improves code efficiency without changing behavior:
1. **Levels**:
   - **O0**: No optimizations (debugging).
   - **O3**: Aggressive optimizations (speed).
2. **Types**:
   - **Local**: Within a basic block (e.g., constant folding).
   - **Global**: Across blocks (e.g., dead code elimination).

## Example: Constant Folding
```c
// Original
int x = 2 + 3 * 4;
// Optimized
int x = 14;
```


