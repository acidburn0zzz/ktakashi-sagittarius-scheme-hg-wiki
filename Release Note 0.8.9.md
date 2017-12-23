Fixed bugs:

- Issue #232: R7RS mode syntax-rules literal problem
- `(peg)` had unbound variable
- `$or` in `(peg)` caused infinite loop

Improvements:

- Compiler checks arguments count of calling procedure if possible.

New features:

- JSON pointer library `(rfc json-pointer)` has been added
- `make-hashtable-serializer` has been added to `(text json object-builder)`

Backward incompatible change:

- `valid-sre?` in `(srfi :155)` now return boolean value instead of SRE