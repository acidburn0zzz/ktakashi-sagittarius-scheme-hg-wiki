This release is minor version update release.

Fixed bugs:

- Archiving zip file with directory caused an error. #83
- Generic hashtable caused SEGV. #84
- `(srfi :106)` didn't export `*msg-*` variables. #86
- `name` and `n` could not be used as `with-args` variables. #88
- `get-mac-address` with position 0 might return loop back address. #90
- GCable symbol and keyword might cause SEGV. #91
- Identifier created by `datum->syntax` could not be referred properly. #89
- Variables converted by `datum->syntax` might referred incorrectly. #92

Improvements:

- Macro expansion is now more copliant with R6RS.
- Sagittarius can be built on Solaris 11.

New features:

- SRFI-60 Integers as Bits is supported.
- SRFI-69 Basic hash table is supported.
- SRFI-113 Sets and Bags is supported.
- SRFI-116 Immutable List Library is supported.
- Draft SRFI-117 Queues based on lists is supported.
