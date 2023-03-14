# Introduction

**WasmEdge-unittest** is a repository of unit test data by extracting WebAssembly (WASM) test suites.

* Test data is from [WebAssembly Core Tests](https://github.com/WebAssembly/spec/tree/master/test/core).

* [S-Expression script](https://github.com/WebAssembly/spec/blob/master/interpreter/README.md#s-expression-syntax) of tests are extracted into `json` and `wasm` files by [wast2json](https://webassembly.github.io/wabt/doc/wast2json.1.html) tool in [wabt](https://github.com/WebAssembly/wabt).

## Whats Difference

* `core/select/select.wast` line 325: `invalid result arity` -> `type mismatch`
  * This error message is for the WAT format, WASM format cannot detect this error by the bytecode.
* `core/comments/comments.wast` line 81: remove the WAT tests.
  * The tests are for comment tests in WAT and cannot be parsed by wabt, therefore remove them.
* `threads/atomic/atomic.wast`: divergence behavior
  * Please check [this issue](https://github.com/WebAssembly/threads/issues/195).
  * Modified the `wast` file for fitting the `compare_exchange_strong` behavior in C++.
* `threads/atomic_wait_notify/atomic_wait_notify.wast`: line 73: remove the thread tests.
  * The S-Expression of threads cannot be parsed by wabt, therefore remove them.
* `function-references/select/select.wast` line 369: `invalid result arity` -> `type mismatch`
  * This error message is for the WAT format, WASM format cannot detect this error by the bytecode.

## Branches And Tags

### Active Branches

* `master`: The newest test suite from the [WebAssembly Spec](https://github.com/WebAssembly/spec/).
* `wasm-dev`: The developing branch for the newest [WasmEdge](https://github.com/WasmEdge/WasmEdge).

### Newest Tags

* `wasm-dev-0.14.0`: The test suite for [WasmEdge 0.14.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.14.0).
* `wasm-core-20240217`: The test suite in the date 2024/02/17 from the WASM spec.

### Older Tags

* `wasm-dev-0.13.0`: The test suite for [WasmEdge 0.13.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.13.0).
* `wasm-dev-0.12.0`: The test suite for [WasmEdge 0.12.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.12.0).
* `wasm-dev-0.11.0`: The test suite for [WasmEdge 0.11.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.11.0).
* `wasm-dev-0.10.1`: The test suite for [WasmEdge 0.10.1](https://github.com/WasmEdge/WasmEdge/releases/tag/0.10.1).
* `wasm-dev-0.10.0`: The test suite for [WasmEdge 0.10.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.10.0).
* `wasm-dev-0.9.1`: The test suite for [WasmEdge 0.9.1](https://github.com/WasmEdge/WasmEdge/releases/tag/0.9.1).
* `wasm-dev-0.9.0`: The test suite for [WasmEdge 0.9.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.9.0).
* `wasm-dev-0.8.0`: The test suite for [WasmEdge 0.8.0](https://github.com/WasmEdge/WasmEdge/releases/tag/0.8.0).
* `wasm-core-20231026`: The test suite in the date 2023/10/26 from the WASM spec.
* `wasm-core-20230511`: The test suite in the date 2023/05/11 from the WASM spec.
* `wasm-core-20221215`: The test suite in the date 2022/12/15 from the WASM spec.
* `wasm-core-20221026`: The test suite in the date 2022/10/26 from the WASM spec.
* `wasm-core-20220712`: The test suite in the date 2022/07/12 from the WASM spec.
* `wasm-core-20220504`: The test suite in the date 2022/05/04 from the WASM spec.
* `wasm-core-20220223`: The test suite in the date 2022/02/23 from the WASM spec.
* `wasm-core-20211214`: The test suite in the date 2021/12/14 from the WASM spec.
* `wasm-core-20211119`: The test suite in the date 2021/11/19 from the WASM spec.
* `wasm-core-20210414`: The test suite in the date 2021/04/14 from the WASM spec.

### Deprecated

* `wasm-core`: The older test suite for the [SSVM 0.7.2](https://github.com/second-state/SSVM/releases/tag/0.7.2) and [SSVM 0.7.3](https://github.com/second-state/SSVM/releases/tag/0.7.3). Deprecated and will not update.
* `wasm-ref-types`: The test suite for the bulk-memory-operations and reference-types proposals.
* `wasm-1.1`: The test suite for the WASM 1.1.
* `wasm-1.0`: The test suite for the WASM 1.0.
