Fixed bugs:

- Issue #177: Detached process should not have pipe as its current ports.
- Issue #178: (rfc pem) does not confirm RFC 1421 section 4.4
- Issue #179: Chunked input/output port without any content raises an error by set-port-position!
- Issue #180: unbound variable check on R6RS is done incorrectly.
- R7RS `syntax-rules` raised unbound variable warning

Improvements:

- Safe read/write library cache file
- Performance of bignum multiplication on Linux has been improved.


New features:

- SRFI-133 has been supported
- File monitoring library `(sagittarius filewatch)` has been added
- `http-gzip-receiver` procedure for handling gzip encoded HTTP response has been added to `(rfc http)`