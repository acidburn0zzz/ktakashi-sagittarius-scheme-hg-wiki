Fixed bugs:

- SRFI-112 `rx` required underlying `(test sre)`.
- Compiler computed pre-frame size wrongly. #46
- `syntax-rules` could not refer template variable properly. #7
- R6RS placeholder `_` was compared without considering binding. #47
- Reading huge cache file took more time than compiling library. #35
- CMakeLists.txt contained EQUAL instead of using STREQUAL.
- Macro expansion did not slice ellipsis properly. #48
- With certain value bignum subtraction was done incorrectly. #49
- Custom hash function did not accept bignum as hash value. #50
- Identifier renamed by R7RS `syntax-rules` was not resolved properly. #51
- `let-syntax` made invalid scope. #52
- R7RS style escaped symbol was not read/write invariance. #53
- `#!r6rs` did not change writer mode in REPL. #54

Improvements:

- `sagittarius` supports handling pipe input.
- `(rfc http)` do not convert socket binary port to transcoded port.
- `(rfc ssh)` supports counter mode.
- `include` and `include-ci` include files more like C's include.

New features:

- `(packrat)` supports `*`, `+` and `?` as quantifier.
- Binary I/O utility library `(binary io)` has been added.
- `(util bytevector)` supports SRFI-13 like APIs.
- Binary data parsing library `(binary parse)` has been added.
- Gauche like char-set reading reader macro has been added. `#!read-macro=char-set`.

New documents:

- `(rfc http)` has been documented.