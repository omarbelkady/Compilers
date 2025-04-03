# Formal Verification of Compilers

## Theory
**Formal verification** proves compiler correctness using mathematical models:
1. **Coq/Isabelle**: Proof assistants for verifying transformations.
2. **Translation Validation**: Check equivalence of source/IR after each pass.
3. **Symbolic Execution**: Detect vulnerabilities in generated code.

## Example: Verifying Constant Folding
```coq
Lemma constant_folding_correct:
  forall (a b: Z), eval_expr (fold_constants (Plus (Const a) (Const b)) = a + b.
Proof. (* Coq proof script *) Qed.
```

