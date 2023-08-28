# Rust Github Action

'Silverbullet' for a quickstart Rust CI based upon [Github Actions](https://developer.github.com/actions/)

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org) [![](https://img.shields.io/badge/Rust-1.72.0-orange)](https://blog.rust-lang.org/2023/08/24/Rust-1.72.0.html)

*What's inside the "box":*

* Rust 1.72.0
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
      - uses: actions/checkout@v1
      - uses: mirlahiji/rust-action@master
        with:
          args: cd integration-test && cargo fmt -- --check && cargo clippy -- -Dwarnings && cargo test
```

---

> Thanks to @ [icepuma](https://github.com/icepuma) for handing over the project and @ [bwasty](https://github.com/bwasty) for Cmake
