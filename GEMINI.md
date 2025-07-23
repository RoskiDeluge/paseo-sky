# Gemini Code Assistant Documentation for the Sky Repository

This document provides guidance for the Gemini Code Assistant on how to interact with the Sky source code.

## About the Project

Sky is an open-source behavioral database management system (BDBMS) written in C. It is designed for analyzing and segmenting behavioral data for objects. The core concepts are:

*   **Events:** An action and/or state change for an object at a specific time.
*   **Paths:** A sequence of events for a single object.
*   **Objects:** The entities being tracked, identified by a 64-bit integer.

The project is still in its early stages, with a roadmap that includes features like a multi-threaded server, a write-ahead log, and real-time queries.

## Key Files

*   `README.md`: Provides a high-level overview of the project.
*   `ARCHITECTURE.md`: Describes the data types, physical file format, and network protocol.
*   `Makefile`: Contains the build and test automation.
*   `src/`: The main source code directory.
*   `tests/`: The test suite.

## Development Environment

The project uses a `Makefile` for building and testing. The following are the main targets:

*   `make all`: Builds the `libsky.a` library and the `skyd`, `sky-gen`, and `sky-bench` binaries.
*   `make test`: Runs the test suite using the `tests/runtests.sh` script.
*   `make install`: Installs the Sky binaries and data files.
*   `make clean`: Removes all build artifacts.

The compiler flags are set in the `CFLAGS` and `CXXFLAGS` variables in the `Makefile`. The project uses `llvm-config` to determine the correct flags for the system.

## Coding Style

The coding style is standard C99. Please adhere to the following conventions:

*   Use 4-space indentation.
*   Follow the existing naming conventions for variables and functions.
*   Write clear and concise code.
*   Add comments to explain complex logic.

## Testing

The project has a test suite in the `tests/` directory. The tests are written in C and use the `minunit.h` framework. To run the tests, use the `make test` command.

When adding new features, please add corresponding tests to the test suite.

## How to Get Help

If you have any questions, please refer to the `README.md` and `ARCHITECTURE.md` files. You can also ask for help on the project's mailing list.
