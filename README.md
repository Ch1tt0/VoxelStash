# VoxelStash

Voxel Game, you've heard it a million times before!

## Prerequisites

- CMake `v4.1` or higher
- MSVC/GCC/Clang C++ compiler
  - On Linux, I recommend Clang
- Ninja

## Building

### With VSCode

1. Open the project folder in VSCode
2. Install the recommended extensions (clangd, CMake Tools, Clang-Format, EditorConfig for VS Code)
3. Make sure in the CMake tab your chosen preset is the same as `CompilationDatabase` in `.clangd`
4. Open the terminal and run `./vcpkg/bootstrap-vcpkg.sh` or `./vcpkg/bootstrap-vcpkg.bat`
5. Press `Ctrl+Shift+P` and run "CMake: Configure"
6. Press `F7` or use "CMake: Build" to build the project or press `Ctrl+Shift+F5`

## Project Structure

```sh
Project-Directory/
├── src/                        # Source files
├── build/                      # Build output (generated)
├── vcpkg/                      # Git submodule of the vcpkg repo
├── CMakeLists.txt              # CMake configuration
├── CMakePresets.json           # CMake configuration
├── vcpkg.json                  # vcpkg dependencies and general information
├── vcpkg-configuration.json    # vcpkg registries
├── .clang-format               # Code formatting rules
├── .clangd                     # Points clang to compile_commands.json
├── .editorconfig               # Editor configuration
├── .gitignore                  # Git ignore rules
├── .gitattributes              # Git attributes
├── .gitmodules                 # Git submodules
├── LICENSE                     # License file
├── CONTRIBUTING.md             # Contribution guidelines
└── README.md                   # This file
```

## Adding Dependencies

```pwsh
> vcpkg add port <dependency>
```

Then reconfigure CMake to install the dependencies.
