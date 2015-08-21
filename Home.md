R6RS/R7RS Scheme system.

[![Build Status](https://drone.io/bitbucket.org/ktakashi/sagittarius-scheme/status.png)](https://drone.io/bitbucket.org/ktakashi/sagittarius-scheme)
[![Build status](https://ci.appveyor.com/api/projects/status/8axfxf8dvr8pdtjk/branch/default?svg=true)](https://ci.appveyor.com/project/ktakashi/sagittarius-scheme/branch/default)


## NEWS

- Sagittarius Scheme 0.6.7 has been released (Aug 21th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.7)
- Sagittarius Scheme 0.6.6 has been released (Jul 17th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.6)
- Sagittarius Scheme 0.6.5 has been released (Jun 19th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.5)
- Sagittarius Scheme 0.6.4 has been released (May 15th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.4)
- Sagittarius Scheme 0.6.3 has been released (Apr 17th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.3)
- Sagittarius Scheme 0.6.2 has been released (Mar 13th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.2)
- Sagittarius Scheme 0.6.1 has been released (Feb 13th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.1)
- Sagittarius Scheme 0.6.0 has been released (Jan 16th, 2015) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.6.0)

[Old NEWS](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Old%20NEWS)

## Features

- Builtin CLOS
- Common Lisp like reader macro
- Cryptographic libraries
- CL like keyword lambda syntax
- Builtin regular expression
    - Mostly works O(n)
- Replaceable reader

## Document

- [Sagittarius Users' Reference](http://ktakashi.github.io/sagittarius-online-ref.html)
- [Sagittarius Users' Reference(One file)](http://ktakashi.github.io/sagittarius-ref.html)

## Build tips
If you are using Ubuntu 11.10 (which I tested from scratch), you need to install these packages.

`cmake`, `libgc-dev`, `zlib1g-dev` and `libffi-dev`.

`cmake` must be installed the other can be installed during building, however it is not managed by package manager so it might cause problems.

On Debian Linux, default `cmake` version is 2.8.2 and Sagittarius requires 2.8.4 so it might complain. If you got the problem, please change the version number to 2.8.2 in the `CMakeLists.txt`.

### For QNX environment
QNX environment has been supported (only x86 has been tested). To build Sagittarius on it, you need to use CMake tool chain like this;

```
#!shell
cmake -DCMAKE_TOOLCHAIN_FILE=cmake/Toolchain-QNX-8.0.0.cmake .
```

Then patch Boehm GC with following command before build;


```
#!shell
patch -p < cmake/patches/gc.qnx.patch
```

If you are building with out of tree, then adjust above commands.

## Building from repository

You may want to build the developing version of Sagittarius retrieved from the developing repository. It requires the latest release version of Sagittarius. Following steps describe how to do it:

1. Download the latest Sagittarius from download page and install it (if you already have installed the latest version this is not required).
2. Clone the repository.
3. Run `./dist.sh gen` in the cloned source directory.
4. Execute CMake described above section.

If you don't do this steps, you will get an error during CMake process something like the following:

```
CMake Error at src/CMakeLists.txt:102 (ADD_LIBRARY):
  Cannot find source file:

    regex_stub.c

  Tried extensions .c .C .c++ .cc .cpp .cxx .m .M .mm .h .hh .h++ .hm .hpp
  .hxx .in .txx
```

## Misc

[External Links](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/External%20Links)

## Memos (for developers)

[Release process](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20process)
