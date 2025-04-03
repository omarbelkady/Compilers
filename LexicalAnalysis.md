
# Lexical Analysis

## Theory
The **lexer** (tokenizer) converts raw source code into tokens (keywords, identifiers, literals) using:
1. **Regular Expressions**: Define token patterns (e.g., `[0-9]+` for integers).
2. **Finite Automata**: Efficiently match regex patterns (DFA/NFA).

## Example: Tokenizing Python Code
```python
x = 42  # Tokens:
# IDENTIFIER (x), OPERATOR (=), LITERAL (42)
```
