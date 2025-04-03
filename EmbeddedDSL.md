# Embedded Domain-Specific Languages (DSLs)

## Theory
**Embedded DSLs** extend host languages for domain-specific tasks:
1. **Syntax Abstraction**: Use macros or operator overloading.
2. **Optimization**: Generate efficient code via compiler hooks.
3. **Examples**: Halide (image processing), SQLAlchemy (database queries).

## Example: Halide for Image Processing
```python
# Halide DSL in Python
blur_x = Func("blur_x")
blur_x[x, y] = (input[x-1, y] + input[x, y] + input[x+1, y]) / 3
blur_x.compile_to_gpu()
```

