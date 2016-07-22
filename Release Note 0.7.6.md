Fixed bugs:

- R7RS `syntax-rules` didn't compare bound identifier properly.
- `(text sql)` didn't print `WITH` clause with indent properly.
- `(sagittarius termios)` and `(sagittarius filewatch)` weren't available on Windows installers.

Improvements:

- Printing R7RS character names on R7RS mode.
- `(sagittarius remote-repl)` can now send reader directives.
- Ports created by R7RS procedure now reads as if it's on R7RS mode.
- `(text sql)` prints `VALUES` clause.

New features:

- SRFI-134 has been supported.
- `string->istring` has been added.