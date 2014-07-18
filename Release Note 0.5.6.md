Fixed bugs:

- SRFI-42 implementation was out dated. #36
- `letrec*`evaluated init values incorrect order. #38
- `char-set-map` raised an error when passing empty map. #39
- `thread-sleep!` stopped in millisecond instead of second. #40
- `thread-sleep!` only accepted exact integer. #41
- Thread related procedures timeout value didn't accept time object. #42
- `string-split` caused SEGV when empty match was given. #43
- `digit-value` returned truncated value for half valued numbers. #44
- Predefined charset name of regular expression resolved incorrectly.
- `interaction-enviromnent` in `(scheme repl)` was defined as a variable instead of a procedure.

Improvements:

- Compiler eliminates no side effect expression more eagerly.
- Improved compiled code of `filter`, `remp`, `remove`, `remv` and `remq`.
- `hashtable-update!` searches only once.
- `regex-group` can accept named match.
- Improved performance of `vector-map`, `vector-for-each` and `string-for-each`.
- Unicode 7.0.0 has been supported.
- `regex-replace` has been added.
- Regular expression replace procedure can understand $p and $P as pre-match and post-match placeholder.

New features:

- Heap data structure library `(util heap)` has been added.
- SRE conversion library `(text sre)` has been added.
- SRFI-115 has been supported.

Incompatible change:

- `sash` is now a symbolic link, the binary name is `sagittarius`. #37
- Handling empty match of regular expression has been changed to Perl compatible.
- Character sets are not only ASCII but Unicode.