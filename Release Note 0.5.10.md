Fixed bugs:

- Installation directory was not configurable. #75
- `make-parameter` did not accept transcoder and codec as its initial value. #76
- `vector-map` was not run in the same dynamic environment. #77
- `real-part` always returned 0 for non complex number. #78
- Applying `=` with complex number raised an error. #79
- `vector-reverse!` did not respect optional start and end arguments. #80
- `make-temporary-file` didn't make unique enough file under multithreading environment. #81
- Calling `get-string-n` with length 0 raised an error. #82
- `get-bytevector-n!` returned EOF when reading length is 0.

Improvements:

- Custome binary port now uses less memory.
- Adapt `U+180E` to be treated as 'Cf' (This is since Unicode 6.3.0)
- Lightweight port locking.
- Reading huge string from textual port consumes less memory.
- `min` and `max` now always returns `+nan.0` if the given arguments contain NaN.
- Symbols and keywords are now GC target.
- Socket error prints proper error message.
- crypto and hash operation now won't create C continuation boundary.

New features:

- Bytevector comparison procedures `bytevector>?`, `bytevector<?`, `bytevector>=?` and `bytevector<=?` have been added to `(util bytevector)`.
- Regular expression now accepts bytevectors as well.
- `bytevector->hex-string` now accepts `upper?` keyword.
- `create-entry` in `(archive)` now also accepts 3 arguments for different archive name.
- Timer library `(util timer)` has been added.

Incompatible change:

- Returning from C continuation now always raises an error.