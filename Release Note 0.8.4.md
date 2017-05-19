Fixed bugs:

- Issue #226: bitwise-xor inconsistency with other schemes
- `ilist=` in `(srfi :116)` didn't compare correctly if passed lists are more than 2
- `ilist-copy` was not exported
- Argument check of `fxrotate-bit-field` was not executed correctly

Improvements:

- Issue #223: Avoid unnecessary allocation for call-next-method
- Supporting SHA3 and BLAKE2 hash algorithms
- `<simple-server>` in `(net server)` now has `:context` slot to hold user defined server context
- Binary transfer encoding works outside of the ASCII range.

New features:

- `bytevector->escaped-string` has been added to `(util bytevector)`
- Socket select operations for TLS socket have been implemented.
- `http-debug-sender` and `:trace` keyword are introduced to `(rfc http)`
- `http-multipart-sender` has been added to `(rfc http-connections)`
- `oauth-signer-clone` and `oauth-verifier-clone` have been added to `(net oauth)`
- Draft SRFI 143 has been added.