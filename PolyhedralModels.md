### Polyhedral-Models.md

# Polyhedral Models for Loop Optimization

## Theory
**Polyhedral models** represent loops as mathematical polyhedra to enable transformations:
1. **Data Dependence Analysis**: Determine safe reordering/parallelism.
2. **Loop Transformations**: Tiling, fusion, skewing.
3. **Tools**: ISL (Integer Set Library), Pluto.

## Example: Loop Tiling with ISL
```c
// Original loop
for (i = 0; i < N; i++)
  for (j = 0; j < N; j++)
    A[i][j] = B[i][j] * 2;

// Tiled loop (2x2 tiles)
for (i = 0; i < N; i += 2)
  for (j = 0; j < N; j += 2)
    for (ii = i; ii < i+2; ii++)
      for (jj = j; jj < j+2; jj++)
        A[ii][jj] = B[ii][jj] * 2;
```
