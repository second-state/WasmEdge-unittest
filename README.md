# Introduction

**ssvm-unittest** is a repository of unit test data by extracting WebAssembly (WASM) test suites.

* Test data is from [WebAssembly Core Tests](https://github.com/WebAssembly/spec/tree/master/test/core).

* [S-Expression script](https://github.com/WebAssembly/spec/blob/master/interpreter/README.md#s-expression-syntax) of tests are extracted into `json` and `wasm` files by [wast2json](https://webassembly.github.io/wabt/doc/wast2json.1.html) tool in [wabt](https://github.com/WebAssembly/wabt).
