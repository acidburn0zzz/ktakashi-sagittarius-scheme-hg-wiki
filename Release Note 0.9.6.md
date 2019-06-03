Fixed bugs:

- Issue: #247: macro does not work if i import scheme base
- Issue: #248: every and any from SRFI-1 aren't compliant of the specification
- Issue: #254: raise and raise-continuable don't attach stack trace
- Issue: #256: ÿ can't be printed properly
- Issue: #257: flexible-vector-delete! raises an error when removing the last element
- Fixing the build process (retrieving windows time zone)

New features:

- Mutable JSON library `(text json mutable)` has been added
- URI PEG parser library `(rfc uri parser)` has been added
- SRFI-146 mappings is supported.
- Some of R7RS-large Tangerine editions are supported
- `define-c-struct` now accepts `alignment` keyword as its base alignment

Improvements:

- `(text json pointer)` supports mutable JSON as well
- Minor performance improvement of `(util logging)`
- `(rfc tls)` now verify certificates

New documentation:

- `(text json patch)` has been documented