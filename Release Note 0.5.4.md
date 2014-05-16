Fixed bugs;

- `(write '\x7c;)` wrote `|` instead of `|\||`. #19
- Reading `#!r6rs` from string changed writer's behaviour. #20
- Passing negative value to hashtable constructor procedure caused C level assert. #21
- `pointer->integer` didn't consider the result values bit length. #22
- Passing big exponent to `expt` returned incorrect value. #23
- `(expt 1.0 0)` returned exact number. #25
- `sash` didn't accept non ASCII options. #26
- Passing overflowed value to bytevector input-port with `set-port-position!` causes SEGV. #27
- Passing overflowed value to bytevector output-port with `set-port-position!` didn't expand buffer. #28
- `randome-source-pseudo-randomize!` raised an error. #29

Improvements;

- Bignum multiplication now uses karatsuba algorithm if the given valus is big enough.
- `pointer->integer` now accepts optional argument bit to specify retrieving value of bits.
- `file-options` now accepts `append` option to open append mode.
- `set-port-position!` now accepts `whence` optional argument.
- `promise?` procedure now compromise R7RS tests.

New Features;

- `pointer->uinteger` has been added to `(sagittarius ffi)`
- SFTP library `(rfc sftp)` has been added.

