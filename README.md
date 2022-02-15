# Introduction

**WasmEdge-unittest** is a repository of unit test data by extracting WebAssembly (WASM) test suites.

* Test data is from [WebAssembly Core Tests](https://github.com/WebAssembly/spec/tree/master/test/core).

* [S-Expression script](https://github.com/WebAssembly/spec/blob/master/interpreter/README.md#s-expression-syntax) of tests are extracted into `json` and `wasm` files by [wast2json](https://webassembly.github.io/wabt/doc/wast2json.1.html) tool in [wabt](https://github.com/WebAssembly/wabt).

## Whats Difference

* `core/select/select.wast` line 368: `invalid result arity` -> `type mismatch`
  * This error message is for the WAT format, WASM format cannot detect this error by the bytecode.
* Temporary not update the `core/binary` tests for `wasm-dev` branch and related tags.
  * These tests should be covered after the file manager refactored in the WasmEdge project.

## Branches And Tags

### Active Branches

* `master`: The newest test suite from the [WebAssembly Spec](https://github.com/WebAssembly/spec/).
* `wasm-dev`: The developing branch for the newest [WasmEdge](https://github.com/WasmEdge/WasmEdge).

### Newest Tags

* `wasm-dev-0.9.1`: The test suite for [WasmEdge 0.9.1](https://github.com/WasmEdge/WasmEdge/releases/tag/0.9.1).
* `wasm-core-20211214`: The test suite in the date 2021/12/14 from the WASM spec.

### Inactive Branches

* `wasm-core`: The older test suite for the [SSVM 0.7.2](https://github.com/second-state/SSVM/releases/tag/0.7.2) and [SSVM 0.7.3](https://github.com/second-state/SSVM/releases/tag/0.7.3). Deprecated and will not update.

### Older Tags

* `wasm-dev-0.9.0`: The test suite for [WasmEdge 0.9.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.9.0).
* `wasm-dev-0.8.0`: The test suite for [WasmEdge 0.8.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.8.0).
* `wasm-core-20211119`: The test suite in the date 2021/11/19 from the WASM spec.
* `wasm-core-20210414`: The test suite in the date 2021/04/14 from the WASM spec.
* `wasm-ref-types`: The test suite for the bulk-memory-operations and reference-types proposals.
* `wasm-1.1`: The test suite for the WASM 1.1.
* `wasm-1.0`: The test suite for the WASM 1.0.
