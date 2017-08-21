Fixed bugs:

- Issue #229: Passing NaN to flfinite? returns #t
- Issue #231: (fl/ 0.0) raises an error
- Issue #230: Inexacting 100000000000000000000001 and 99999999999999999999999 end up the same results

New features:

- SRFI-142 has been supported
- SRFI-144 has been supported
- SRFI-151 has been supported
- `(rfc uuid)` now has UUID version check procedures
- `(sagittarius generators)`: `circular-generator` has been added

Improvements

- `(text json object-builder)`: JSON serializer can be reused in other serializer
- `(text sql)` can parse/serialize 'BEGIN', 'CREATE SCHEMA', 'INTERVAL' and more
- Nagle's algorithm is disabled by default on socket creation