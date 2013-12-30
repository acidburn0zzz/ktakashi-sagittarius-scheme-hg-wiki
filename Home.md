R6RS/R7RS Scheme system.

![Build Status](https://drone.io/bitbucket.org/ktakashi/sagittarius-scheme/status.png)

## Features

- Builtin CLOS
- Common Lisp like reader macro
- Cryptographic libraries
- CL like keyword lambda syntax
- Builtin regular expression
  - Mostly works O(n)
- Replaceable reader

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
