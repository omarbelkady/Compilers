
# Code Generation Introduction

## Theory
**Code generation** translates optimized IR into target machine code. Key tasks:
1. **Instruction Selection**: Map IR operations to CPU instructions.
2. **Register Allocation**: Assign variables to registers (e.g., graph coloring).
3. **Instruction Scheduling**: Reorder operations to avoid pipeline stalls.

## Example: x86 Assembly from LLVM IR
```llvm
; LLVM IR
%sum = add i32 %a, %b