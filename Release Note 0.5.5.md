Fixed bugs:

- `(math mt-random)` sometimes raised an error. #31
- `random-source-state-set! didn't restore the prng state. #32
- `read-line` didn't compliant what R7RS requires. #33
- SRFI-42 implementation was not up to date. #36

Improvements:

- `sash` now accepts `-A`, `-Y` and `-F` option to append load path, dynamic load path or library suffix.
- `uri-encode` now encodes with capital letter by default.

New features:

- Treemap library `(util treemap)` has been added.
- Queue library `(util queue)` has been added.
- Deque library `(util deque)` has been added.
- `subtype?` has been added to `(clos user)` and `(clos core)`.

New documents:
- `(util hashtables)` has been documented.