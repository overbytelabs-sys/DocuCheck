# DocuCheck
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](#license)
[![Status](https://img.shields.io/badge/status-pre--release-orange.svg)]()

> Private, portable ML inference via **WebAssembly**.  
> Status: **pre-init** (no code yet).

## What this will be
A lean ONNX-compatible inference runtime that runs **entirely in WASM/WASI** (browser, Node, CLI), with optional Python bindings.

## Why it matters
- Keep user data **on-device** (privacy by default)
- Same core runs everywhere (browser/Node/WASI)
- Minimal dependencies, permissive license

## Initial scope (v0.1 MVP)
- ONNX loader + tiny executor
- Core ops: `Conv`, `MatMul/Gemm`, `Relu`, `Softmax`, `Add`, pooling
- One browser demo + a CLI example
- Packages: npm + PyPI

## Tech direction (tentative)
- **Core:** Rust → `wasm32-unknown-unknown` / `wasm32-wasi`
- **JS:** `wasm-bindgen`/`wasm-pack` (ESM)
- **Py:** PyO3/maturin wrapper (optional)
- **License:** Apache-2.0 (code), CC BY 4.0 (docs)

## Roadmap (high level)
- [ ] Project skeleton (workspace, crates, CI)
- [ ] ONNX parser stub + model loader
- [ ] Executor + first ops
- [ ] Demo (browser) + CLI tool
- [ ] Packaging (npm / PyPI)
- [ ] Docs page & examples

## Getting involved
We’re just starting. Open an issue to discuss design or claim a TODO.
Good first labels will appear once code lands.

## License
Apache-2.0 for code; docs under CC BY 4.0. See `LICENSE` when added.
