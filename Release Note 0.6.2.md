Fixed bugs:

- Passing non string value to `sys-process-call` caused SEGV. #100
- Cache of macro generating macro which used `generate-temopraries` causes unbound variable. #101
- Building on Clang 3.6 failed. #102
- Stopping server of `(net server)` caused SEGV on Windows.
- SRE with `w/ascii` raised an error.
- SRFI-115 procedure `regexp-partition`.was missing.
- Internal condition variable was not initialised.

Improvements:

- `hash-process!` and `hash-done!` now can take optional argument to specify the range of passing bytevector.
- Macro expander for `syntax-case` is more compliant with R6RS.
- `time` macro now accepts multiple values return.

New features:

- SHA-512/224 and SHA-512/256 have been supported on `(math)`.
- Bytevector conversion reader macro library `(sagittarius bv-string)` has been added (not documented).
- `->size-limit-binary-input-port` has been added to `(binary io)`.
- Simple LRU cache library `(cache lru)`has been added.
- `.sld` files can be recognised as libraries.
- Keystore library `(security keystore)` has been added.

New documents:

- PKCS#12 library `(rsa pkcs :12)` has been documented.