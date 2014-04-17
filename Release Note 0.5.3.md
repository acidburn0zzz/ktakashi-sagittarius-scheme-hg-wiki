Fixed bugs;

- Merged `(sagittarius debug)` libraries in one file.
- Local macro expansion caused compilcation error. (#15)
- Extended lambda syntax didn't work if the result was from macro expansion. (#16)
- `shutdown-port` raised an error even it's passed proper socket port. (#17)
- `bytevector-slices` crushed if the argument `k` was 0. (#18)

Improvements;

- `filter-map` is now in `(core base)`.
- `<date>` is now defined in Scheme world for future extension.
- `(rfc tls)` now ignores warning level alert.

New Features;

- SRFI-114 `(srfi :114 comparator)` has been supported.

New platform support;

- Cygwin64 has been supported.