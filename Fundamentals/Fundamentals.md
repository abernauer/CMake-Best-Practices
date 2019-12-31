# Introduction

CMake is a set of tools covering everything from setting up a build through to producing a package ready for distribution. Supporting a wide range of platforms, tools and languages.


The first stage takes a generic project description and generates platform-specific project files using a developer's standard build tool of choice (e.g. make, Xcode, Visual Studio, etc.). This initial stage can be classified as the setup stage where Project File Generation takes place. Also following under the CMake tools are CTest and CPack for testing and packaging respectively.

# Setting Up a Project

A CMakeLists.txt file is a human readable file that brings order to your project which is a essentially a collection of files. The file defines what should be built and how, what tests to run and what packages(s) to create. It is an agnostic description of the project, which CMake then turns into platform specific build tools.

A fundamental principal of CMake is that your project has both a source directory and a binary directory. The location of your projects'

When building a project the developer can take two different approache: _in-sourcse_ and _out_of_source builds.

