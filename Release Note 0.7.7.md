Fixed bugs:

- Issue #189: nested guard causes infinite loop
- Issue #190: non continuable condition should not return
- Issue #191: Cannot build on Cygwin
- `(net server)` didn't stop on a platform which merges IPv6 and IPv4 sockets, having the same port, into one
- Fixing build process on FreeBSD. (`FindGC` added `-L` option globally)
- Passing `time-process` and `time-thread` to `current-time` didn't return proper values

Improvements:

- Build process can find `clock_gettime` on Linux properly.
- `<process>` object now initialises all ports to #f.
- `(sagittarius socket)` defines and raises socket specific conditions.
- `socket-accept` can be interrupted by `thread-interrupt!`.

New features:

- WebSocket library `(rfc websocket)` has been added.
- `get-process-times` and `get-thread-times` have been added to retrieve CPU time of process and thread.

Incompatible changes:

- `(core syntax-case)` is renamed to `(core macro)`.

Miscellaneous

- size of `SgVM` was reduced.