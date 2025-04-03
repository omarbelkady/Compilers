
# Syntax Analysis: Parsing Code Structure

## Theory
**Syntax analysis** (parsing) validates code structure against a **context-free grammar (CFG)**. Key concepts:
1. **Parse Tree**: Hierarchical representation of grammar rules.
2. **Abstract Syntax Tree (AST)**: Simplified tree omitting syntactic details (e.g., parentheses).
3. **Ambiguity**: Grammars with multiple valid parse trees (e.g., `if-if-else` dangling else).

## Example: Parsing Arithmetic Expressions
**Grammar**:
Expr → Expr + Term | Term
Term → Term * Factor | Factor
Factor → (Expr) | Integer

Copy

**Input**: `2 + 3 * 4`  
**Parse Tree**:

Expr
├─ Expr (Term → 2)
├─ +
└─ Term
├─ Term (Factor → 3)
├─ *
└─ Factor → 4

/
2 *
/
3 4


## Case Study: Lua’s Lightweight Recursive Descent Parser
- **Problem**: Lua needed a fast, portable parser for embedded systems.
- **Solution**:
  - Handwritten **recursive descent parser** with minimal memory usage.
  - Directly constructs AST without intermediate representations.
- **Outcome**: Lua’s parser is one of the fastest among scripting languages.

## Challenges
- **Ambiguity**: Resolving conflicts in grammars (e.g., operator precedence).
- **Error Handling**: Detecting and recovering from syntax errors.

