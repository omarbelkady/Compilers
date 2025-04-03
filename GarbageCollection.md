
# Garbage Collection

## Theory
**Garbage Collection (GC)** automates memory management by reclaiming unused objects. Common algorithms:
1. **Mark-and-Sweep**: Traverse reachable objects, then free unreachable ones.
2. **Generational GC**: Focus on short-lived objects (young generation).
3. **Reference Counting**: Track object references (used in Python/C++ smart pointers).

## Example: Mark-and-Sweep in Python
```python
a = [1, 2, 3]
a = None  # Object [1,2,3] becomes unreachable → collected.
```

