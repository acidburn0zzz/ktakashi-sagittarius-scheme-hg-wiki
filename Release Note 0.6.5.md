Fixed bugs:

- `uinteger->pointer` doesn't work properly on 32bit environment. #117
- `define-record-type` with custom protocol on parent doesn't raise an error. #118
- `input-port-open?` and `output-port-open?` should not raise an error when port is given. #119
- inconsistency between `char-numeric?` and `digit-value`. #120
- `quotient` return incorrect result. #121
- `(log -0.0)` should return -inf.0+pi. #122
- promise is evaluated twice. #123
- `(exact +nan.0)` causes C assertion error. #124
- calling `display` with socket port raises an error. #125
- `letrec`, `letrec*` and internal definition should raise an error if init part contains undefined variable. #127
- `write-shtml-as-html` doesn't handle `*TOP*`. #128
- `json-read` goes infinite loop if string terminates without delimiter. #129
- RSA encryption with PKCS v1.5 padding sometimes generates incorrect padding. #130
- Passing closed socket to fdset caused SEGV.
- TLS server socket calculated signature wrongly.
- Fixing `set-xor!`, `set-xor`, `bag-xor!` and `bag-xor`.
- `heap-search` might go infinite loop.

Improvements:

- Parameters' initial values is now initialised even it's created on different threads. #126
- Missing SRFI-116 comparators has been added.
- `sxml:attr-list` is now exported from `(text sxml tools)` as well.
- `(sagittarius remote-repl)` now handles I/O (stdout and stderr) separately.
- Exporting auxiliary syntax defined in SRFI-86.
- `-r6` and `-r7` options affect reader/writer better.

New features:

- `thread-interrupt!` procedure has been added.
- `socket-select` related procedures are now interruptible by above procedure.
- `(net server)` now also supports non blocking server.
- `(util timer)` is now resumable

New documents:

- Concurrency library `(util concurrent)` has been documented.
- Low level socket APIs are documented.