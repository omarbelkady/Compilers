### **2. `02-Compiler-Architecture.md`**

# Compiler Architecture

## Theory
Modern compilers are structured into modular components:
1. **Frontend**: Language-specific parsing and semantic checks.
2. **Middle-end**: Language-agnostic optimizations (e.g., LLVM IR).
3. **Backend**: Target-specific code generation (e.g., x86, ARM).

**Single-pass vs. Multi-pass**:
- **Single-pass**: Fast but limited optimizations (e.g., early Pascal).
- **Multi-pass**: Enables complex optimizations (e.g., GCC, Clang).

## Example: LLVM Architecture
```llvm
; LLVM IR example
define i32 @main() {
  ret i32 42
}
```

Case Study: LLVM’s Modular Design

- Problem: Compilers historically coupled to languages/targets.
- Solution: LLVM splits frontend, middle-end, and backend.

- Impact:
- Reuse optimizations across languages (C, Rust, Swift).
- Simplify porting to new architectures (e.g., RISC-V).
- Example: Apple’s Swift uses LLVM for ARM and x86.

Challenges