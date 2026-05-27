# Technical Skills

This repository is a hands-on portfolio of systems, C++, CUDA, Python, and Rust
practice projects. The focus is practical engineering: build systems, automated
tests, CI/CD, benchmarking, static analysis, and readable examples that explain
the underlying tradeoffs.

## Project Map

| Area | Project | What it demonstrates |
| --- | --- | --- |
| Linux systems programming | [systems](systems) | CMake-based C examples for Linux APIs, unit testing, sanitizer-enabled CI, and embedded/custom kernel considerations. |
| Modern C++ | [cpp](cpp) | CMake, GoogleTest, clang-format, clang-tidy, benchmarks, algorithm implementation, and GitHub Actions workflows. |
| Rust | [rust](rust) | Cargo workspace layout, Rust 2024, unit tests, formatting, Clippy, and CI for library-style exercises. |
| Python | [python/codility](python/codility) | Algorithm practice across arrays, sorting, stacks, prefix sums, leaders, slices, and related Codility exercises. |
| CUDA | [cuda](cuda) | CUDA/GPU programming practice area. |

## Highlighted Skills

- **Linux systems programming:** `inotify`, file-descriptor based APIs, `poll`,
  POSIX process/runtime behavior, and custom/embedded Linux kernel requirements.
- **C/C++ engineering:** CMake project structure, compiler warnings, sanitizers,
  GoogleTest, CTest, clang-format, clang-tidy, and benchmark targets.
- **Concurrency and performance foundations:** low-level API design,
  event-driven I/O, benchmark separation from correctness tests, and attention
  to runtime behavior.
- **CI/CD:** GitHub Actions workflows for build, test, format, lint, and
  sanitizer checks.
- **Rust development:** Cargo workspaces, idiomatic module organization,
  `cargo test`, `cargo fmt`, and `cargo clippy`.
- **Algorithmic problem solving:** Codility-style exercises implemented across
  Python, C++, and Rust.

## Featured Example

The first Linux systems example is an
[inotify file watcher](systems/linux/inotify). It includes:

- A small reusable C wrapper around `inotify_init1`, `inotify_add_watch`, and
  batched event dispatch
- A CLI watcher using `poll`
- A self-contained unit/integration test that observes a real `IN_CREATE` event
- CMake and CTest integration
- GitHub Actions CI with sanitizer-enabled builds
- Documentation for the required Linux kernel option `CONFIG_INOTIFY_USER`

## Common Tooling

The projects use a deliberately small, standard toolchain:

- CMake and CTest for C/C++ and C examples
- GoogleTest for C++ unit tests
- clang-format and clang-tidy for C++ style and static analysis
- Cargo, rustfmt, and Clippy for Rust
- GitHub Actions for CI

## Repository Goals

This repository is intended to grow into a collection of focused examples for:

- Linux systems programming
- Networking
- Concurrency
- Embedded Linux
- RTOS concepts
- Unit testing
- Benchmarking
- CI/CD
- C/C++, CUDA, Python, and Rust practice
