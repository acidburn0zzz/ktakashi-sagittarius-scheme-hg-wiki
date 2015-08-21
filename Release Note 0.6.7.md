Fixed bugs:

- Internal bignum to int64_t convertion doesn't consider signness. #138
- `(archive)` with tar doesn't create proper tar ball. #139
- `delete-directory*` doesn't delete hidden directory. #140
- terminate-oldest-handler sometimes causes `&abandoned-mutex-exception`. #141
- `socket-select` causes SEGV. #142
- Identifier created by datum->syntax is refered incorrectly. #105

Improvements:

- `thread-terminate!` on Windows is now a bit safer.
- Supporting Unicode 8.0.0
- Better timezone handling.

New features:

- Timer SRFI is supported.
- `(sagittarius timezone)` has been added.
- `with-syntax*` has been added to `(sagittarius control)`