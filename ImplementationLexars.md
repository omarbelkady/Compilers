
# Implementing Lexers

## Theory
Lexers are built using:
1. **Handwritten Code**: For full control (e.g., Lua).
2. **Generator Tools**: Flex, ANTLR (e.g., Java).

**Lexer Workflow**:
1. Match regex patterns.
2. Emit tokens for the parser.

## Example: Flex Lexer for Integers
```lex
%%
[0-9]+   { return INTEGER; }
%%
```

```python
if True:
    print("Hello")  // INDENT token inserted
```

