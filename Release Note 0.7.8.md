Fixed bugs:

- Issue #193: define-generic and define-method creates global bindings in scope
- Issue #194: Toplevel validation doesn't work properly
- Issue #195: Running with -r7 option doesn't disable keyword reading
- Issue #196: absolute-path procedure on POSIX environment doesn't return path if given file doesn't exist.
- Issue #197: regex-find ignores start position of matcher
- Applied SRFI-113 fixes.


Improvements:

- TLS library should be more stable
- Binding variable names are checked strictly.
- C runtime file on POSIX has version.

New features:

- Experimental C translator `sagittarius-scheme2c` is available (default off)
- `library->path*` procedure has been added.
- `define-inliner` accepts `:origin` keyword to evaluate the expression in the specified library.
- `open-bytevector-input/output-port` has been added to `(binary io)`.
- `->binary-pre-allocated-buffer-input/output-port procedure` has been added to `(util buffer)`.
- SRFI-135 has been supported.
- Logging library `(util logging)` has been added.

Backward incompatible changes:

- `er-rename` is moved to `(core macro)` library.
- Default `unbound-variable` method raises an error.
- Mid level API of `(rfc sftp)` is changed.