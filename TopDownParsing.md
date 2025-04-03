# Top-Down Parsing

## Theory
**Top-down parsers** build parse trees from the root (start symbol) to leaves. Common approaches:
1. **Recursive Descent**: Handwritten parsers using recursive functions.
2. **LL(k) Parsers**: Use `k` tokens of lookahead to predict rules.

**Key Rules**:
- Eliminate **left recursion** (e.g., rewrite `A → Aα | β` to `A → βA'`, `A' → αA' | ε`).

## Example: Recursive Descent Parser for Arithmetic
```python
def parse_expr():
    parse_term()
    while current_token == '+':
        consume('+')
        parse_term()

def parse_term():
    parse_factor()
    while current_token == '*':
        consume('*')
        parse_factor()