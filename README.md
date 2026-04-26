## Overview
This project is a C/C++ application designed to demonstrate the use of custom language components and libraries. It includes a main entry point `Main.c` and several header files that define various functionalities.

## Features
- Custom Language Components: The project uses custom language components defined in the `code/` directory, such as `.alxml` files.
- Multi-platform Support: The project supports building for Linux, Windows, Wine (Linux cross-compile for Windows), and WebAssembly using Emscripten.
- Modular Architecture: The codebase is organized into source (`src/`) and header (`*.h`) files, promoting modularity.

## Project Structure
### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects:
  - Wine Build configuration: `libwinpthread-1.dll` for Windows support.
  - Webassembly Build configuration: Emscripten SDK.

## Build & Run
### Linux
To build and run the application on Linux, follow these steps:

1. **Build**:
   ```sh
   cd <Project>
   make -f Makefile.linux all
   ```

2. **Clean Rebuild**:
   ```sh
   make -f Makefile.linux clean
   make -f Makefile.linux all
   ```

3. **Execute**:
   ```sh
   make -f Makefile.linux exe
   ```

### Windows
To build and run the application on Windows, follow these steps:

1. **Build**:
   ```sh
   cd <Project>
   make -f Makefile.windows all
   ```

2. **Clean Rebuild**:
   ```sh
   make -f Makefile.windows clean
   make -f Makefile.windows all
   ```

3. **Execute**:
   ```sh
   make -f Makefile.windows exe
   ```

### Wine (Linux Cross-Compile for Windows)
To build the application on Linux using Wine, follow these steps:

1. **Build**:
   ```sh
   cd <Project>
   make -f Makefile.wine all
   ```

2. **Clean Rebuild**:
   ```sh
   make -f Makefile.wine clean
   make -f Makefile.wine all
   ```

3. **Execute**:
   ```sh
   make -f Makefile.wine exe
   ```

### Webassembly (Emscripten)
To build the application for the web using Emscripten, follow these steps:

1. **Build**:
   ```sh
   cd <Project>
   emmake make -f Makefile.web all
   ```

2. **Clean Rebuild**:
   ```sh
   make -f Makefile.web clean
   emmake make -f Makefile.web all
   ```

3. **Execute**:
   Open the generated HTML file in a web browser to run the application.

---

This README provides a comprehensive overview of the project, its features, and instructions on how to build and execute it across different platforms.