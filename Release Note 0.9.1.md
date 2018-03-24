Fixed bugs:

- Issue #238: (uname) on Windows 10 returns version 6.2

New features:

- `change-file-timestamps!` has been added.

Improvements:

- Creating symbolic link on MSYS2 checks 'MSYS' environment variable
- Creating symbolic link on Windows uses `SYMBOLIC_LINK_FLAG_ALLOW_UNPRIVILEGED_CREATE` if possible