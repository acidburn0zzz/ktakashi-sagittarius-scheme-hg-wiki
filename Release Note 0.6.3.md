Fixed bugs:

- `er-macro-transformer`'s `rename` procedure didn't rename given identifiers properly. #103, #110
- Internal definition didn't behave as `letrec*`. #106
- Creating record constructor overwrote previous one. #107
- Compilation error with certain vector. #108
- Using `get-bytevector-n` and `get-bytevector-n!` on socket port hanged. #109
- Passing empty port to `json-read` hanged. #111
- Subtraction of real number and complex number returned incorrect value. #112
- `sin`, `cos`, `tan`, `asin`, `acos` and `atan` didn't accept complex number. #113
- Importing cached `(sagittarius debug)` on REPL caused SEGV.

Improvements:

- R6RS/R7RS strict mode. This fixes #104
- Macro expander is now more R6RS compliant.
- R6RS/R7RS macros can co-operate better.
- `json-read` now can return EOF if nothing to read.
- `string->utf8` and `utf8->string` are now as twice as faster.
- OAEP padding is now bouncy castle compatible as well.

New features:

- Shared queue library `(util concurrent shared-queue)` has been added. Not documented.
- Pointer conversion procedure `bytevector->pointer` has been added to `(sagittarius ffi)`.
- `address` macro can now take offset argument to specify from where to pass.
- `pointer->bytevector` can now take offset argument to specify from where to convert to a bytevector.
- `allocate-pointer` procedure can now take fill optional argument.