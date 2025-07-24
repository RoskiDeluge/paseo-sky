# AGENTS.md

This file provides basic guidelines for contributors and code assistants
working with the **Sky** repository.

## Repository Overview
- The project is written in C with a traditional `Makefile` build system.
- Source code resides in `src/`.
- Unit tests are in `tests/` and use a small "minunit" style framework.
- Several Ruby utilities can be found in `util/` (e.g., `util/date.rb`).

## Building
- Run `make all` to build the static library (`libsky.a`) and the binaries
  (`skyd`, `sky-gen`, `sky-bench`).
- Use `make install` to install binaries under the `PREFIX` path (default `/usr/local`).
- `make clean` removes build artifacts.

## Testing
- Execute `make test` to run all compiled tests.
  This invokes `tests/runtests.sh`, which iterates over every `tests/*_tests` binary.
- Ensure new features or fixes come with corresponding test cases.

## Coding Style
- Follow C99 conventions.
- Use 4 spaces for indentation (see existing files such as `src/action.c`).
- Keep function names and variable naming consistent with existing code.

## Notes
- The project uses `llvm-config` to obtain compilation flags, so a working
  LLVM toolchain is required.
- The root of the repository currently lacks an official AGENTS file; this
  document serves as a concise set of instructions for future contributions.
