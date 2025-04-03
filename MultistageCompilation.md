# Multi-Stage Compilation

## Theory
**Multi-stage compilation** generates code at runtime for specialization:
1. **Staging Annotations**: Separate compile-time and runtime code (e.g., `%` in MetaOCaml).
2. **Partial Evaluation**: Precompute parts of the program using static inputs.
3. **Templates**: Generate code variants for different data types.

## Example: Terra’s Meta-Programming
```lua
-- Generate specialized C code at runtime
function add_func(T)
  terra add(a : T, b : T) : T
    return a + b
  end
  return add
end
add_int = add_func(int)
```

