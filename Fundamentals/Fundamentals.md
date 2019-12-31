# Introduction

CMake is a set of tools covering everything from setting up a build through to producing a package ready for distribution. Supporting a wide range of platforms, tools and languages.


The first stage takes a generic project description and generates platform-specific project files using a developer's standard build tool of choice (e.g. make, Xcode, Visual Studio, etc.). This initial stage can be classified as the setup stage where Project File Generation takes place. Also following under the CMake tools are CTest and CPack for testing and packaging respectively.

# Setting Up a Project

A CMakeLists.txt file is a human readable file that brings order to your project which is a essentially a collection of files. The file defines what should be built and how, what tests to run and what packages(s) to create. It is an agnostic description of the project, which CMake then turns into platform specific build tools.

A fundamental principal of CMake is that your project has both a source directory and a binary directory. The source directory is the location of your CMakesLists.txt file and the project's source files as well as other files needed to build your project.

The binary or build directory is where everything created by the build ends up. 

When building a project the developer can take two different approaches:  *in-source*  and *out-of-source* builds.

## In-source builds or Out-of-source Builds

The preferable organization of your project is for the source and build directories to be different, which is an *out-of-source* build. This avoids intermixing problems created by an *in-source* approach and makes version control easier. An added advantage is it allows multiple builds with different configurations.


## Generating Project Files

After selecting your directory structure discussed above the developer runs CMake, which in turn reads in the CMakeLists.txt file and creates the project in the build directory. You select a type of *generator* which determines your project files. The following list is available:

+ Visual Studio
  + Visual Studio 15 2017
  + Visual Studio 14 2015

+ Xcode
  + Xcode

+ Makefiles
  + Unix Makefiles
  + MSYS Makefiles
  + MinGW Makefiles
  + NMake Makefiles



The simplest make to invoke/run CMakke is via the *cmake* command line utility. Demonstrated below. 


```bash
mkdir build
cd build
cmake -G "Unix Makefiles" ../source
```

If you leave out the ```-G``` option, CMake will determine a default generator type on the host platform. The build process is a two part proccess consisting of a *configuring* and *generating* phase. In the *configuring* phase, CMake reads in the CMakeLists.txt file and builds an interpretation of the whole project. After completing this, the *generation* phase creates the project files.

After finishing a run CMake, will save a CMakeCache.txt fil in the build directory.

