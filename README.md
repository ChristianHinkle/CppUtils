# CppUtils

CppUtils is a collection of general purpose C++ libraries with no external dependencies. This repository is a superproject providing all the libraries CppUtils has to offer. Each one is individually usable, although some may depend on others.

## Project Structure 📂

CppUtils
- [CppUtils_Core](https://github.com/ChristianHinkle/CppUtils_Core) (library)
- [CppUtils_Misc](https://github.com/ChristianHinkle/CppUtils_Misc) (library)
- [CppUtils_StdReimpl](https://github.com/ChristianHinkle/CppUtils_StdReimpl) (library)

These projects are built together using `FetchContent` in CMake. This means they configure together (all from the same invocation of CMake), which makes debugging and development easier with the subprojects.

## Build System ⌨

Built with CMake - cross-platform, standardized, and IDE-friendly.

We provide CMake presets, which handle feeding arguments to CMake for you.

### IDE Support

Most IDEs provide built-in CMake integration.

#### VS Code

Has the "CMake Tools" and "C/C++" extensions, both developed by Microsoft.

#### Visual Studio

Has very nice integration, but they seem behind when it comes to supporting the latest CMake features. I've had experiences where I have to switch to VS Code because of this.

## Build Instructions 🔨

### 1. Invoke CMake on the Project (the Configure Step)

Command line: `cmake --preset="win-debug-default"`.

IDE: Choose the `win-debug-default` configure preset, and "configure" the CMake project.

### 2. Invoke a Build Command

Command line: `cmake --build --preset="win-debug"`.

IDE: Choose the `win-debug` build preset, and "build" it.

## Test Instructions 🧪

Here's how to run automated tests, to verify that our code behaves as intended.

### 1. Build the Project

See "Build Instructions" above.

### 2. Invoke CTest

Command line: `ctest --preset="cpputils-win-debug"`.

IDE: Choose the `cpputils-win-debug` test preset, and "run tests".
