# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.5] - 2026-08-17

### Changed
- Bumped version to force a new upload to the Conan remote; no functional changes.

## [1.0.4] - 2026-08-14

### Added
- Added `docker/Dockerfile.rhel10.build` for building, testing, and uploading the package on RHEL 10 (builds both Debug and Release, runs the Release tests, then uploads all package binaries).
- Added `.dockerignore` to reduce the Docker build context size.

## [1.0.3] - 2026-01-21

### Changed
- Fixed missed file rename on macos.

## [1.0.2] - 2026-01-11

### Changed
- Fixing missed file rename on macos.
- Fixed unit-test linker errors on Aarch64 Linux.
- Updating `terminus_cmake` to version 1.0.10

## [1.0.1] - 2025-12-22

### Changed
- Updated to use `terminus_cmake` version 1.0.9
- Updated package test.

## [1.0.0] - 2025-12-21

### Added
- Making boost static by default

## [0.0.12] - 2025-11-21

### Changed
- Updated to use `terminus_cmake` version 1.0.8

## [0.0.11] - 2025-11-20

### Changed
- Migrating to new TERMINUS CMake helpers
- Updated CMake minimum required version to 4.0.0
- Moving headers to `library/include`

## [0.0.10] - 2025-11-20

### Changed
- Updated dependencies

## [0.0.9] - 2025-05-18

### Changed

- Updating headers in error namespace
- Creating base-level `error.hpp` file.

## [0.0.8]

### Changed

- Better support for Emscripten
- Fixed errors in primary conan build method caused by emsdk updates.

## [0.0.7]

### Added

- This changelog now supported
- Migrated error codes from `terminus_core`.
- Adding support for Emscripten

