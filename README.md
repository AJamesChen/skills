# Technical Skills

This repository is a hands-on portfolio of systems, C++, CUDA, Python, Rust,
and embedded Linux practice projects. The focus is practical engineering:
build systems, automated tests, CI/CD, benchmarking, static analysis, and
readable examples that explain the underlying tradeoffs.

## Clone the Repository

Clone the repository and initialize all submodules:

```sh
git clone --recurse-submodules git@github.com:AJamesChen/skills.git
```

For an existing clone:

```sh
git submodule update --init --recursive
```

## Project Map

| Area | Project | What it demonstrates |
| --- | --- | --- |
| Embedded Linux and Yocto | [yocto-platforms](https://github.com/AJamesChen/yocto-platforms/tree/f161f465919c129a75d8bc381764621aa0f62191) | Reproducible Raspberry Pi 4B Yocto builds with signed RAUC A/B updates, visible OTA progress, U-Boot rollback, GPIO peripherals including a ULN2003A stepper driver and direction/speed test harness, and V4L2/GStreamer camera support with a configurable text OSD. |
| Embedded device management | [device-web](https://github.com/AJamesChen/device-web/tree/48d63747ea04485115a27fb10eba5d7df9c2ea73) | Authenticated Go dashboard and REST API for system information, RAUC updates, controlled reboot, live camera playback, snapshots, and persistent top-right OSD settings. |
| Linux systems programming | [systems](https://github.com/AJamesChen/systems/tree/b2c61ec151dfd77848212030cf86b0d6a81243c2) | CMake-based C examples for Linux APIs, unit testing, sanitizer-enabled CI, and embedded/custom kernel considerations. |
| Modern C++ | [cpp](https://github.com/AJamesChen/cpp/tree/892646b85664d5a1af4065bf92f0f1fdddc8ac26) | CMake, GoogleTest, clang-format, clang-tidy, benchmarks, algorithm implementation, and GitHub Actions workflows. |
| Rust | [rust](https://github.com/AJamesChen/rust/tree/42a45966d02ebb5c08d9806d91d3af41106018f7) | Cargo workspace layout, Rust 2024, unit tests, formatting, Clippy, and CI for library-style exercises. |
| Python | [python/codility](https://github.com/AJamesChen/codility/tree/346c0579742d2375fd03b9e07dd5b01a86507a65) | Algorithm practice across arrays, sorting, stacks, prefix sums, leaders, slices, and related Codility exercises. |
| CUDA | [cuda](https://github.com/AJamesChen/cuda/tree/570ecf0a2a16764ea04503463196f27493625205) | CUDA/GPU programming practice area. |

## Highlighted Skills

- **Embedded Linux and Yocto:** reproducible Raspberry Pi platform builds,
  Kas manifests, BitBake, custom layers, WIC partitioning, and RAUC A/B updates
  with health checks and automatic rollback, device-tree overlays, native C
  SPI/GPIO tooling for MFRC522 RFID, and a debounced 4x4 matrix keypad/HD44780
  display service built on libgpiod, plus legacy `bcm2835-v4l2` and GStreamer
  camera bring-up. The ULN2003A addition provides a device-tree-bound kernel
  driver, a terminal direction/speed harness, and a verified RAUC deployment;
  see the [stepper documentation](https://github.com/AJamesChen/yocto-platforms/blob/f161f465919c129a75d8bc381764621aa0f62191/docs/uln2003a.md).
- **Embedded device management:** Go HTTP services, authenticated browser
  sessions, system information, streamed drag-and-drop firmware updates, and
  orderly device reboot, with authenticated REST endpoints for MJPEG playback,
  stopping capture, JPEG snapshots, and persistent GStreamer `textoverlay`
  settings, with visible OTA upload/install progress and selectable
  V4L2/GStreamer capture.
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
[inotify file watcher](https://github.com/AJamesChen/systems/tree/b2c61ec151dfd77848212030cf86b0d6a81243c2/linux/inotify). It includes:

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
- Kas, BitBake, RAUC, U-Boot, libgpiod, Linux SPI/GPIO interfaces, and
  device-tree overlays for reproducible images, OTA workflows, and hardware
  bring-up

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
