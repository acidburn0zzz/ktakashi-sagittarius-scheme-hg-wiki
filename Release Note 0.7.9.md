Fixed bugs:

- Issue #198: SRFI 46 ellipsis renaming not supported on R7RS REPL
- Issue #199: Incorrect result in gcd procedure
- `(sagittarius ffi)` created invalid string when returning value `char*` contains negative value.
- `macroexpand-n` expended `n+1` times.

New features:

- SRFI-139, `compile-r7rs` has been supported on POSIX environment.
- SXML to object builder `(text sxml object-builder)` has been added (not documented yet).
- Simple RSS 2.0 library `(net rss)` has been added (not documented yet).
- `(text sql)` now supports LIMIT and OFFSET non standard SQL clauses.
