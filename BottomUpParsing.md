# Bottom-Up Parsing

## Theory
**Bottom-up parsers** build parse trees from leaves to root. Common methods:
1. **LR Parsers**: Use a state machine with shift/reduce actions.
   - **LR(0)**, **SLR**, **LALR(1)**: Trade-offs between power and table size.
2. **Shift-Reduce Actions**:
   - **Shift**: Move token to stack.
   - **Reduce**: Replace a rule’s RHS with its LHS.

## Example: Bison Grammar for a Calculator
```bison
expr : expr '+' term { $$ = $1 + $3; }
     | term { $$ = $1; }
     ;
term : term '*' factor { $$ = $1 * $3; }
     | factor { $$ = $1; }
     ;
factor : INTEGER { $$ = $1; }
       | '(' expr ')' { $$ = $2; }
       ;
```

