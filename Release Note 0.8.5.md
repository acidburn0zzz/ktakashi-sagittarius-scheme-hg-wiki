Fixed bugs:

- `(srfi :143)` exported incorrect name
- Issue #228: srfi 134 errors

New features:

- `&dbi-sql-error` condition has been added to `(dbi)`
- `string->smtp-address` and `smtp-valid-address?` have been added to `(rfc smtp)`
- Client cookie parsing procedures `parse-cookies` and `parse-cookies-string` have been added to `(rfc cookie)`
- Pseudo random number generator ChaCha20 has been supported.