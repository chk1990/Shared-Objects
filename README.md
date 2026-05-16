# Shared-Objects

A modern C++ project demonstrating the design and usage of shared objects, dynamic libraries, and modular software components.

This repository focuses on:
- shared library development,
- dynamic linking concepts,
- modular software architectures,
- reusable runtime components,
- interface-driven design,
- and modern C++ build structures.

The project is intended for educational, experimental, and reference purposes.

---

## Features

Possible functionality includes:

- creation of shared libraries,
- dynamic runtime loading,
- interface-based module systems,
- reusable software components,
- plugin-style architectures,
- platform abstraction,
- modular dependency separation,
- CMake integration for shared objects.

---

## Project Goals

The primary goals of this repository are:

- demonstrate shared object usage in C++,
- provide clean modular examples,
- simplify experimentation with dynamic linking,
- improve understanding of runtime-loaded components,
- create reusable library structures,
- support educational learning.

---

## Concepts Covered

This repository may demonstrate:

- `.so` shared objects on Linux,
- `.dll` libraries on Windows,
- symbol visibility,
- dynamic linking,
- runtime module loading,
- ABI considerations,
- interface separation,
- plugin architectures,
- dependency management.

---

## Requirements

### Compiler

Recommended:
- GCC 13+
- Clang 17+

### Language Standard

- C++20

### Build System

- CMake 3.16 or newer

---

## Build Instructions

### Clone Repository

```bash
git clone https://github.com/chk1990/Shared-Objects.git
cd Shared-Objects
```

### Configure

```bash
cmake -B build
```

### Build

```bash
cmake --build build
```

---

## Running

Example:

```bash
./build/SharedObjectsExample
```

Depending on platform and configuration, runtime library paths may need to be configured.

---

## Linux Shared Object Notes

Example shared object output:

```text
libexample.so
```

Inspect linked libraries:

```bash
ldd ./build/SharedObjectsExample
```

Inspect exported symbols:

```bash
nm -D libexample.so
```

Example runtime path setup:

```bash
export LD_LIBRARY_PATH=./build:$LD_LIBRARY_PATH
```

---

## Windows Notes

Example shared library output:

```text
example.dll
```

Depending on the compiler and runtime environment, DLL search paths may require configuration.

---

## Example Architecture

```text
Application
    │
    ├── Shared Interface Library
    │
    ├── Shared Object / DLL
    │
    └── Runtime-loaded Modules
```

---

## Project Structure

```text
Shared-Objects/
├── include/        # Public interfaces
├── src/            # Source files
├── shared/         # Shared library implementations
├── examples/       # Example applications
├── tests/          # Unit tests
├── docs/           # Documentation
├── build/          # Generated build files
└── CMakeLists.txt
```

---

## Documentation

API documentation may be generated using Doxygen.

Generate documentation:

```bash
doxygen Doxyfile
```

Generated documentation is typically located in:

```text
docs/html/
```

---

## Design Principles

This project aims to follow:

- modular software architecture,
- interface-based design,
- low coupling,
- reusable software components,
- clean dependency boundaries,
- RAII,
- const correctness,
- modern C++ practices.

---

## Intended Use

This project is intended for:
- educational purposes,
- experimentation,
- prototyping,
- learning dynamic linking concepts,
- reusable software architecture demonstrations.

It is not intended for safety-critical environments without proper validation.

---

## Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT.

IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY ARISING FROM THE USE
OF THE SOFTWARE.

Use at your own risk.

---

## License

This project is licensed under the MIT License.

See the LICENSE file for details.

---

## Contributing

Contributions are welcome.

Please ensure:
- readable and maintainable code,
- clean modular interfaces,
- successful compilation,
- reasonable documentation,
- platform compatibility where possible.

---

## Author

Created and maintained by Christoph Kolhoff.

GitHub:
https://github.com/chk1990
