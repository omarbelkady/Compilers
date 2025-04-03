# Just-In-Time (JIT) Compilation

## Theory
**JIT compilation** dynamically translates bytecode or IR to machine code during runtime. Key features:
1. **Adaptive Optimization**: Profile hot code paths and recompile for speed.
2. **Inline Caching**: Cache method/type lookups for dynamic languages.
3. **Tiered Compilation**: Start with quick bytecode interpretation, then optimize hot code.

## Example: Java’s HotSpot JVM
```java
// Repeated method calls trigger JIT compilation
for (int i = 0; i < 1_000_000; i++) {
    processData(); // Compiled to native code after 10k iterations
}
```

