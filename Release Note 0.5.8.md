Fixed bugs:

- Control characters in symbol were printed non hex scalar value. #55
- `#!fold-case` only folded one expression. #56
- Overwriting or redefining didn't raisen an error. #57
- Invalid rename clause in `export` caused SEGV. #58
- `c-struct-set!` didn't accept struct pointer. #60
- Toplevel `(values)` caused exit. #62
- syntax literals was not compared in sense of `free-identifier=?`. #61
- Fixed bunch of unbound variables.
- `cond-expand` in `define-library` was not R7RS compliant.
- `(rfc ssh)` was not using identification string properly.
- `copy-binary-port` didn't copy all port content when src port contains more than 4092 bytes.

Improvements:

- `ldconfig` will be called after `make install`. #59
- exporting unbound variable now either reports  warning or raises an error.
- Slightly better performance of port locking.
- Compiler now folds exported variable when the VM mode does not allow to overwrite.
- RSA and DSA marker is now defined with keyword so that compiler can constant fold.
- `define-method` won't add method to global definition when it's running on child context.
- `(odbc)` can now handle full DSN.
- Bignum and flonum in compiled cache now uses smaller amount of space.
- Compilation time error now has more information.

New features:

- `define-c-union` has been added to `(sagittarius ffi)` to support C union.
- `c-memcpy` has been added to `(sagittarius ffi)` for better performance.
- `(tlv)` now also supports LV structure reading.
- `format` now prints bytevector in hex, octec and binary numbers with `~x`, `~o` and `~b` respectively.

Incompatible changes:

- Bytevectors are written with `#u8()` notation in R7RS mode.

