# Implementations

## Compilers

Most of those compilers work for multiple related languages such as C, C++, etc.:

[GCC](gcc/) is arguably the most popular implementation.

### clang

LLVM based.

Made by Apple in 2007 when GCC did not meet it's technical and licensing requirements, later merged into LLVM. It then had contributions by Google, Apple, Intel, etc.

FreeBSD moved to it in 2012: <http://unix.stackexchange.com/questions/49906/why-is-freebsd-deprecating-gcc-in-favor-of-clang-llvm>

Sony PS4 (2013 Q4, FreeBSD based) moved to it while PS3 used GCC.

### CompCert C compiler

<http://compcert.inria.fr/compcert-C.html>

<https://github.com/AbsInt/CompCert>

INRIA formally verified compiler to a very large subset of C99.

Written and verified in Coq.

### Portable C Compiler

<https://en.wikipedia.org/wiki/Portable_C_Compiler>

Very small.

Popular in the 1980s, until GCC killed it.

### Tiny C Compiler

<https://github.com/TinyCC/TinyCC>

By Fabrice Bellard.

Educational only.

### Parsers

Language parsers without built-in assembly output:

- <https://github.com/eliben/pycparser>

### Non-free

#### icc

Intel.

Has intrinsics for every Intel instruction, and optimizes assembly really well for Intel. 

Closed source...

#### IBM XL C

IBM proprietary: <https://en.wikipedia.org/wiki/IBM_XL_C%2B%2B>

The Linux 2014 release uses clang as front-end.

## libc

- glibc: GNU implementation, major on Linux
- Apple's libc is not glibc, but is open source <http://stackoverflow.com/questions/7592069/how-to-build-apples-opensource-libc>
- Microsoft likely has a closed source implementation

Then there are several implementations that target Linux-only embedded systems, and can therefore be smaller or more efficient:

- musl libc. Comparison: <http://www.etalabs.net/compare_libcs.html>. Alpine Linux moved to it, as it is partially binary compatible with glibc.
- Bionic (Android): <https://en.wikipedia.org/wiki/Bionic_%28software%29>
- dietlibc <http://www.fefe.de/dietlibc/>
- newlibc <https://en.wikipedia.org/wiki/Newlib>. GNU.

### ulibc

<http://uclibc.org>

Stands for Micro libc.

Attempts to be very small for embedded systems.

One of the ways in which it is smaller is that it is Linux-only.

Was used in Alpine, but replaced with musl, which is partially binary compatible with glibc.