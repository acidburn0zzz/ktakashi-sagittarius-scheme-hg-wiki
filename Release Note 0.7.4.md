Fixed bugs:

- Issue #181: #e1@1 returns inexact number. (now it raises `&implementation-restriction`)
- Issue #182: Problem with equal-hash? -- Segmentation fault: 11
- Issue #183: default-hash on SRFI-128 raises an error when passing a pair
- Issue #184: Lookahead-* procedures mutate port position.
- Issue #143: Bundled libffi can't be compiled on clang (OS X)
- SRFI-113 set/bag depended on the order of hashtable

Improvements:

- Builtin hash procedures now follows SRFI-125 (accepts second argument and ignores)
- Applying SRFI-41 performance improvements
- `(sagittarius filewatch)` now works also on OS X
- Thread termination of thread pool is more stable.

New features:

- SRFI-132 - Sort Libraries has been supported.
- Draft SRFI, SRFI-125 - Intermediate hash tables has been supported.
- `shared-queue-remove!` has been added to `(util concurrent)`.