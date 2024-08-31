# Rust Github Action

'Silverbullet' for a quickstart Rust CI based upon [Github Actions](https://developer.github.com/actions/)

[![img](https://img.shields.io/badge/Rust-1.80.1-orange)](https://blog.rust-lang.org/2024/08/08/Rust-1.80.1.html)

*What's inside the "box":*

* Rust 1.80.1
* Rustfmt
* Clippy
* Cargo Release
* Cmake

# Usage

In a file inside `.github/workflows/quickstart.yml`

```yaml
name: Rust Example

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4
      - uses: MachineDynamo/rust-action@master
        with:
          args: cd integration-test && cargo fmt -- --check && cargo clippy -- -Dwarnings && cargo test
```

---

> Thanks to @ [icepuma](https://github.com/icepuma) for handing over the project and @ [bwasty](https://github.com/bwasty) for Cmake
