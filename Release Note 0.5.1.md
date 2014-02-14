Fixed bugs;

- Macro visibility problem has been fixed. #1
- `datum->syntax` hid symbols in some cases. #6
- Some port procedure caused SEGV accessing closed port. #8
- `define` didn't raise an error in invalid case. #9
- `(tlv)` miscomputed the length.
- Compiler didn't reject circular list properly.
- `format` caused SEGV with custom textual port.

New features;

- R7RS style SRFI library names have been supported. e.g) `(srfi 1)`
- SRFI-5 has been supported.
- local method form `let-method` has been added to `(clos user)`.
- R6RS record has been integrated to CLOS.

Improvements;

- `quasiquote` now generates constant value if possible.
- Compile time procedure folding.

New platform;

- OpenBSD has been supported

[Download](https://bitbucket.org/ktakashi/sagittarius-scheme/downloads)