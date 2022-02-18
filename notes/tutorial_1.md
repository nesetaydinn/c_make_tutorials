# Tutorial 1, Understanding CMake tool and concept:
- In the basic and small prpjects you can use a basic gcc or g++ command, as like;

```bash
gcc main.c -o main
```
or

```bash
g++ main.cpp -o main
```
But when your project grows and be a complex structure then these commands will be grow and may be a complicated structure. Hence we need to have a standard and basic project management concept. **_ CMAKE TOOL IS A PROJECT MANAGER, AND IS NOT A COMPILER. _** this defination so important because CMake tool not be create a executable object file, but CMake generate some control files for any other make tools. So each environment use different a compiler therefore to easy compile in a complex project, using more easy a standart as like buildsystem files written in the CMake language instead of multiple such buildsystems.

## To generate a build system on CMake 3 parts (given by <https://cmake.org/cmake/help/latest/manual/cmake.1.html#manual:cmake(1)> introduction to CMake Buildsystems):
- Source Tree: The top-level directory containing source files provided by the project. The project specifies its buildsystem using files, starting with a top-level file named CMakeLists.txt. These files specify build targets and their dependencies.
- Build Tree: The top-level directory in which buildsystem files and build output artifacts (e.g. executables and libraries) are to be stored. CMake will write a CMakeCache.txt file to identify the directory as a build tree and store persistent information such as buildsystem configuration options. The top-level directory in which buildsystem files and build output artifacts (e.g. executables and libraries) are to be stored. CMake will write a CMakeCache.txt file to identify the directory as a build tree and store persistent information such as buildsystem configuration options.
- Generator: This chooses the kind of buildsystem to generate. (Run cmake **_--help_** to see a list of generators available locally.) Optionally use the **_-G_** option below to specify a generator, or simply accept the default CMake chooses for the current platform. 
