# Quantum Compilers

## Theory
**Quantum compilers** translate high-level quantum algorithms to hardware-specific instructions:
1. **QIR (Quantum Intermediate Representation)**: Language-agnostic IR.
2. **Circuit Optimization**: Reduce gate count (e.g., merging Hadamards).
3. **Qubit Mapping**: Assign logical qubits to physical hardware.

## Example: Quantum Circuit Optimization
Original: H → CNOT → H → T
Optimized: CNOT → T (H gates cancel out)



## Example: Q# Resource Estimator
```qsharp
operation EstimateShor() : Unit {
  use qubits = Qubit[2048];
  // ... Shor's algorithm ...
  let resources = EstimateResources(qubits);
}
```