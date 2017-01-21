Fixed bugs:

- `(rfc http2 client)` didn't send GOAWAY frame properly.
- `(text sql)` couldn't parse window functions
- `(text sql)` emitted `;` after comments
- `_` was considered as a pattern variable on R7RS `syntax-rules`

New features:

- R7RS-large RedEdition has been supported
- Closing procedure for HTTP2 connection has been added to `(rfc http2 client)`
- GZIP receiver has been added to `(rfc http2 client)`
- SRFI-101 has been supported

Improvements:

- `(text sql)` now emits better indented SQL