# WebAssembly Compilation

## Theory
**WebAssembly (WASM)** is a portable binary format for browsers/servers. Key features:
1. **Stack-Based VM**: Compact bytecode with linear memory.
2. **WASI**: System interface for non-browser environments.
3. **Compilation**: Source languages (C, Rust) → WASM via LLVM.

## Example: Rust to WASM
```bash
rustup target add wasm32-unknown-unknown
cargo build --target wasm32-unknown-unknown
```