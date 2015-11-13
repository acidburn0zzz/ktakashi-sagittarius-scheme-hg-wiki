Fixed bugs:

- Importing an error containing library in library causeed dead lock on multithread environment. #159
- `get-bytevector-all` with buffered port ignored buffered values. #160
- Subtract negative rational number from zero returned positive number. #161
- Loading FFI library from child thread raised an error. #163
- `(expt 5 10000000)` caused SEGV. #162
- compare procedure passed to `er-macro-transformer` returned #t even the given 2 arguments are not the same.
- `syntax-case` expander contained incorrect use of `free-identifier=?`.
- Reading more than one byte from standard input port on Windows returned incorrect number of values.

Improvements:

- TLS socket port is now bidirectional port.
- Windows file port can also read from COM now.
- Displaying big integers of radix 2, 8 and 16 takes O(n) order. (n = size of bignum)
- Displaying big integers of other radixes is now much faster than before.

New features:

- `(sagittarius termios)` has been added. Not documented.
- ``smtp-login-authentication` for `LOGIN` method has been added to `(rfc smtp)`.
