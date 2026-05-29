# ct-demo

Constraint Theory demos in Rust — proving drift-free arithmetic on Pythagorean manifolds. Shows why constraint theory eliminates accumulated floating-point error.

## What This Gives You

- **Zero-error arithmetic** — integer-based operations on Pythagorean manifolds with no accumulated drift
- **Comparison demos** — side-by-side float vs. constraint theory benchmarks
- **Bitmask benchmarks** — performance testing for constraint operations
- **Integration tests** — comprehensive test suite for solver correctness

## Quick Start

```bash
cargo run --example comparison    # Float vs. constraint theory
cargo run --example solver_demo   # Solver in action
cargo run --example bitmask_benchmark  # Performance benchmarks
cargo test                         # Run integration tests
```

### The Core Idea

IEEE 754 floats accumulate error: `float_error(N) = O(√N · σ)`

Constraint theory snaps to exact integer Pythagorean triples. Once snapped, **no further error accumulates** — the result is an exact `i64`.

## How It Fits

Demo crate for [constraint-theory-core](https://github.com/SuperInstance/constraint-theory-core). Part of the SuperInstance ecosystem.

Related repos:
- [constraint-theory-core](https://github.com/SuperInstance/constraint-theory-core) — core Rust crate
- [ct-api-reference](https://github.com/SuperInstance/ct-api-reference) — API docs
- [constraint-playground](https://github.com/SuperInstance/constraint-playground) — interactive playground

## License

Apache 2.0
