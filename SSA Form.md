# Static Single Assignment (SSA) Form

## Theory
**SSA form** ensures each variable is assigned once, simplifying optimizations:
1. **Phi (φ) Functions**: Resolve variable versions at control flow merges.
2. **Dominance Frontiers**: Identify where φ nodes are needed.
3. **Benefits**: Simplifies data flow analysis and dead code elimination.

## Example: SSA Conversion
```llvm
; Original
%x = add i32 1, 2
%x = add i32 %x, 3

; SSA
%x.1 = add i32 1, 2
%x.2 = add i32 %x.1, 3
```