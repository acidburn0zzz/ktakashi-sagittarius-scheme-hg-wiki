Fixed bugs;

- `import` in `cond-expand` clause did not work as R7RS requires. #4.
- process `run` procedure crushed on Linux. #6.

New features;

- `change-class` has been supported.

Improvements;

- `-S` option has been added to handle other library suffixes.
- Class object now has 'direct-subclasses' slot.
- R7RS style srfi library names are supported.
- Compiler now eliminate some of referencial transparent expressions if it can.

Internal changes;

- Build process has been changed.

[Download](https://bitbucket.org/ktakashi/sagittarius-scheme/downloads)