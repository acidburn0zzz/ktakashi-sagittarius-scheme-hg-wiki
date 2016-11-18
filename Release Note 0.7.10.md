Fixed bugs:

- Issue #200: -Ewarn doesn't show any warning
- Issue #201: read-directory returns invalid string if the directory contains Japanese filename.
- `(text sql)` didn't handle `DISTINCT` SQL keyword correctly
- Experimental C translator emitted incorrect dependency
- `(net rss)` raised an error if empty tag was given for simple values
- `(text sql)` couldn't serialise chain identifier in `order-by` and `group-by`

New feature:

- `force` accepts non promise object.
- `change-file-mode` is now actual implementation on Windows environment
   It can only set readonly flag for now

Improvements:

- `hashtable-entities` is now implemented in C

Incompatible change:

- Issue #202: File operation failure should raise &i/o instead of &assersion