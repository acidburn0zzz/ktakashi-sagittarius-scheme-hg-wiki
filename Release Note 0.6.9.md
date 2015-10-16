Fixed bugs:

- `get-line` didn't accept custom textual input port. #148
- Cached procedure caused an error. #149
- Retrieving timezone offset of Asia/Tokyo failed. #150
- `local-timezone` returned GMT in Japanese timezone on Windows. #152
- Template variable expansion used `free-identifier=?` instead of `bound-identifier=?`. #154
- Comparison of literal from pattern variable was incorrect. #155
- `string->date` didn't consider timezone properly. #156
- Calling `load` in library file outside of library declaration caused SEGV.
- Finding library process was not atomic.
- `-r6` options without script file caused SEGV.
- AES CTR mode (aka RFC 3686) didn't work properly.

New features:

- GCM mode is supported on `(crypto)`. #147
- R7RS `syntax-rules` now signals an error if input forms aren't equal length. #151
- `buffered-port` is introduced.
- User defined custom port class has been introduced.
- `macroexpand-n` has been added to `(sagittarius debug)`.
- Cipher APIs on `(crypto)` now uses parameter classes instead of keyword arguments.
- SMTP library `(rfc smtp)` has been added.
- `process-wait` now can accept `timeout` keyword to stop waiting.

Improvements:

- Pre build process uses less network connect (for developer).