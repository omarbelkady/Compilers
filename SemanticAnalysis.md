
# Semantic Analysis

## Theory
**Semantic analysis** enforces language rules beyond syntax:
1. **Symbol Tables**: Track variables, functions, and types.
2. **Scoping**: Static (lexical) vs. dynamic scoping.
3. **Type Checking**: Verify operand compatibility (e.g., `int + string`).

## Example: Resolving Variable References
```python
x = 10          # Global scope
def foo():
    x = 20      # Local scope
    print(x)     # Refers to local x (20)
foo()
print(x)         # Refers to global x (10)
```