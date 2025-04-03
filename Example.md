## Theory
A **compiler** is a program that translates source code written in a high-level language (e.g., C++, Python) into a lower-level representation (e.g., machine code, bytecode). Key phases include:
1. **Frontend**: Lexical analysis, parsing, and semantic analysis.
2. **Middle-end**: Code optimizations (e.g., loop unrolling).
3. **Backend**: Target-specific code generation.

**Compiler vs. Interpreter**:
- **Compiler**: Translates the entire program upfront (e.g., GCC).
- **Interpreter**: Executes code line-by-line (e.g., Python).

## Example
```c
// Simple C program
int main() {
    return 42;
}
```

- Compiler Workflow:
- Lexer: Tokens int, main, {, return, 42, }.
- Parser: Builds AST for function structure.
- Codegen: Generates x86 assembly like mov eax, 42.
- Case Study: The First Fortran Compiler (1957)
- Problem: Early programmers wrote error-prone machine code.
- Solution: Fortran’s compiler automated translation of math-heavy code.
- Impact:
    - Reduced development time by 20x.
- Introduced optimizations like register allocation.
- Legacy: Established compilers as essential tools.