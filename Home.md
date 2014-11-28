R6RS/R7RS Scheme system.

![Build Status](https://drone.io/bitbucket.org/ktakashi/sagittarius-scheme/status.png)

## NEWS
- Sagittarius Scheme 0.5.10 has been released (Nov 24th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.10)
- Sagittarius Scheme 0.5.9 has been released (Oct 17th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.9)
- Sagittarius Scheme 0.5.8 has been released (Sep 19th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.8)
- Sagittarius Scheme 0.5.7 has been released (Aug 15th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.7)
- Sagittarius Scheme 0.5.6 has been released (Jul 18th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.6)
- Sagittarius Scheme 0.5.5 has been released (Jun 20th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.5)
- Sagittarius Scheme 0.5.4 has been released (May 16th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.4)
- Sagittarius Scheme 0.5.3 has been released (Apr 17th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.3)
- Sagittarius Scheme 0.5.2 has been released (Mar 14th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.2)
- Sagittarius Scheme 0.5.1 has been released (Feb 14th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.1)
- Sagittarius Scheme 0.5.0 has been released (Jan 17th, 2014) [Release Notes](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20Note%200.5.0)

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

## Misc

[External Links](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/External%20Links)

## Memos (for developers)

[Release process](https://bitbucket.org/ktakashi/sagittarius-scheme/wiki/Release%20process)
