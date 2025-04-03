# Peephole Optimization

## Theory
**Peephole optimization** improves code by examining small instruction sequences ("peepholes") and replacing them with faster or shorter equivalents. Common techniques include:
1. **Redundant Instruction Elimination**: Remove unused loads/stores.
2. **Strength Reduction**: Replace expensive operations (e.g., `x * 2` → `x << 1`).
3. **Constant Propagation**: Replace variables with known constant values.

## Example
```llvm
; Before optimization
%1 = add i32 5, 3
%2 = mul i32 %1, 2

; After optimization
%2 = mul i32 8, 2  → %2 = 16
```
