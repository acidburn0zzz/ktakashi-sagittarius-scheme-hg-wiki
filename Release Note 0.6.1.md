Fixes bugs:

- REPL showed cache warning. #94
- `sint-list->bytevector` raised an error if given list contained 0. #97
- RSA decryption didn't restore original value. #98

Improvements:

- Bundled libffi can be used on x64 environment. #93
- Better cooperation of `syntax-case` and `er-macro-transformer`. #96
- Performance improvement of JSON parser.
- `timer-schedule!` and `timer-reschedule!` procedures can now accept time duration object as _period_ argument.

New features:

- `(text json)` has been added.
- OAEP padding is supported for RSA encryption/decryption by `rsa-oaep-padding` procedure.

New documents:

- SRFI-13 convention procedures of `(util bytevector)` is documented.
- `(sagittarius threads)` is documented.
- `(text sxml html-parser)` is documented.

Incompatible changes:

- `(scheme base)` now doesn't export `import`. #95