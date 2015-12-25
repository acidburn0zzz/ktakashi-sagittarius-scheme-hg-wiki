Fixed bugs:

- Issue #164: file buffered port isn't flushed when GCed. 
- Issue #165: syntax-case returns identifier even it's not macro expansion phase
- `fxior`, `fxand` and `fxxor` returned invalid value when more than 2 arguments have passed and one of them wasn't a fixnum
- `lucas-lehmer?` test returned `#f` even the given argument is prime number.

New improvements:

- VM dispatch is 5% faster.
- `(asin 0)` and `(acos 1)` return exact integer.
- Reduced stack overflow during compilation
- Improved performance of `free-identifier=?`.
- Compiler removes  `when` expression like this : `(lambda () (when #f #t) 'ok)`.
- Removed `exists` and `lset-union` procedure from compiler for better performance.
- Pointer object can be passed for FFI type `wchar_t*`.
- Referring callback type of FFI structure now returns callback object even if it's not created on Scheme world.

New freatures:

- Generator library `(sagittarius generators)` and draft SRFI-121 have been added.
- `fold2` and `fold3` procedures have been added to `(util list)`.
- Base64 port operations procedures `open-base64-encode-output-port`, `open-base64-encode-input-port`, `open-base64-decode-output-port`, and `open-base64-decode-input-port` have been added.
- `delete-file` procedure show better error message when it failed to delete the given file.
- SQL parser and serializer have been added to `(text sql)` (not documented and still experimental).
- Added bunch of Windows message constants.
- `vector-sort` and `vector-sort!` now accepts optional arguments `start` and `end` according to draft SRFI 132.
