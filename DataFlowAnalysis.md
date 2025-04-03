### Data Flow Analysis

## Theory
**Data flow analysis** tracks how data values propagate:
1. **Reaching Definitions**: Where a variable’s value was last assigned.
2. **Live Variables**: Variables that may be read before being overwritten.
3. **Iterative Algorithms**: Solve data flow equations (e.g., worklist algorithm).

## Example: Live Variable Analysis
```c
// Block 1
a = 5;       // a is live here
b = a + 1;   // a is live, b becomes live
// Block 2
c = b * 2;   // b is live
print(c);    // c is live
```
