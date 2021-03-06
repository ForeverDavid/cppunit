# CppUnit --- The C++ Unit Test Library 
-------------------------------------
http://www.freedesktop.org/wiki/Software/cppunit

CppUnit is the C++ port of the famous JUnit framework for unit
testing.

For MSWindows installation notes, see INSTALL-WIN32.txt.
For other systems -- including cygwin -- see INSTALL and INSTALL-unix.


Bug reports are welcome. Please open bug reports for Cppunit at
bugs.documentfoundation.org under the component cppunit.

Email to the current maintainers may be sent to
<libreoffice@lists.freedesktop.org>

# CMake Build System
This fork of the original CppUnit project adds CMake build system support to the newest sources found on the mainline. To configure and build the project follow the instructions listed here.

The CMake scripts offer the following options:
   * __BUILD_SHARED_LIBS__      - Enables shared libraries
   * __CPPUNIT_BUILD_APIDOC__   - Enables doxygen documentation build if 'doxygen' can be found
   * __CPPUNIT_BUILD_EXAMPLES__ - Enables the build of the sample applications and libraries
   * __CPPUNIT_BUILD_TESTING__  - Enables test executables that can be run by CTest

Use the following commands to configure with your favorite generator.

```
git clone https://github.com/mschmieder/cppunit

mkdir cppunit_build
cd cppunit_build

cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE:STRING=Debug -DBUILD_SHARED_LIBS:BOOL=ON ../cppunit -DCMAKE_INSTALL_PREFIX:STRING=install

cmake --build . --config Debug --target=install
```

## Continuous Integration
[![Build Status](https://travis-ci.org/mschmieder/cppunit.svg?branch=master)](https://travis-ci.org/mschmieder/cppunit)

This fork of cppunit is build with travis-ci on Linux and OS X using the following compilers
   * Linux (Ubuntu 17.04)
       - gcc-6
       - clang-4.0
    * OS X
       - gcc-6
       - clang-4.0
       - XCode 8.2
