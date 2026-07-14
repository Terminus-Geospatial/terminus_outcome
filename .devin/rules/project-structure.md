---
trigger: always_on
---

# Terminus Outcome Project Structure

## Purpose

`terminus_outcome` is a header-only C++ library that provides modern error- and result-handling primitives built on `std::error_code` semantics. Public headers live under `terminus/error/` and `terminus/outcome/`.

## Repository Layout

| Path | Purpose |
|------|---------|
| `library/include/terminus` | Public headers (`error.hpp`, `outcome.hpp`, `error/`, `outcome/`) |
| `templates/` | CMake template files used during the build (e.g., `exports.hpp.in`) |
| `test/unit/` | Unit tests for the Outcome library |
| `test/package/` | Conan package verification example |
| `docs/` | Additional developer documentation |
| `build/` | Generated build tree (not tracked) |
| `conanfile.py` | Conan 2.x recipe |
| `CMakeLists.txt` | CMake build definition |

## Key Dependencies

- `boost` (Boost headers)
- `terminus_cmake` (Terminus CMake helpers, build requirement)

## Build & Test

Activate the Conan environment created by `terminus_setup` (the venv lives at `~/conan` and is activated with `go-conan`), then:

```bash
conan-build.sh -r -c -B

# Or manually
go-conan
conan install . -b missing
conan build .
```

Run tests with `ctest --output-on-failure` inside the `build/` directory.

## Conan / Environment Notes

- The `terminus_setup` repository creates a Python virtual environment at `~/conan` and wires a `go-conan` shell function. Activate it with `go-conan` before running any Conan commands.
- This package is header-only, so `conanfile.py` clears `libdirs` and `bindirs` in `package_info()`.
- The `terminus/error.hpp` header is owned by this repository and is the canonical source for `Error_Code`, `Error_Category`, `Result`, and `Optional` primitives.
