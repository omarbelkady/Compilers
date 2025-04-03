# Operational Semantics

## Theory
**Operational semantics** define program behavior via execution steps:
1. **Small-Step**: Detailed step-by-step reduction (e.g., `3 + 4 → 7`).
2. **Big-Step**: High-level evaluation (e.g., `while` loops → final state).

## Example: Small-Step Semantics for Arithmetic

⟨2 + 3 * 4, σ⟩ → ⟨2 + 12, σ⟩ → ⟨14, σ⟩

- `σ` represents the program state (e.g., variable values).

## Case Study: CompCert’s Formally Verified Semantics
- **Problem**: Bugs in compilers can introduce security vulnerabilities.
- **Solution**:
  - CompCert (C compiler) uses Coq-based proofs to match source and assembly semantics.
  - Example: Proven absence of miscompilation for pointer arithmetic.
- **Outcome**: Critical systems (avionics, nuclear) use CompCert for safety.

## Challenges
- **Complexity**: Modeling low-level behaviors (e.g., concurrency).
- **Tooling**: Steep learning curve for proof assistants like Coq.