
# Loop Optimizations

## Theory
Loop optimizations improve performance by restructuring loops:
1. **Loop Unrolling**: Execute multiple iterations per cycle (reduces overhead).
2. **Invariant Code Motion**: Move computations outside loops.
3. **Vectorization**: Use SIMD instructions for parallel execution.

## Example: Loop Unrolling
```c
// Original
for (int i = 0; i < 4; i++) {
    sum += arr[i];
}

// Unrolled
sum += arr[0] + arr[1] + arr[2] + arr[3];
```


