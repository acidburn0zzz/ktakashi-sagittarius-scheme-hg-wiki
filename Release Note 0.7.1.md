Fixed bugs:

- Issue #171: Infinite system call error on Windows 10
- Issue #172: Expanding ellipsis template raises an error if variables contains the same pattern variable
- Issue #173: read-sys-random reads doubled size of specified bits
- Issue #174: Build failure on FreeBSD
- Parsing `CREATE TABLE` statement with multiple constraints on column specification raised an error in `(text sql)`

New features:

- SRFI-99, ERR5RS records, has been supported.
- SRFI-57, Records, has been supported.
- SRFI-100, define-lambda-object, has been supported.
- SRFI-126, R6RS-based hashtables, has been supported.
- SRFI-128, Comparators (reduced), has been supported.
- SRFI-131, ERR5RS Record Syntax (reduced), has been supported.

Improvements:

- Thread pool of `(util concurrent thread-pool)` now pushes task best case O(1).
- `(net server)` is more stable.
- Improved RFC 5322 library `(rfc :5322)` performance.
- Improved failure case of `string-ci` related procedures' performance.
