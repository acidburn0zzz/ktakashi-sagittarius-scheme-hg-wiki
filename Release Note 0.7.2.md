Fixed bugs:

- Issue #175: (define a 'b 'c) isn't valid form
- Issue #176: thread-pool-wait-all! hangs if one of the threads is terminated.
- Nested ellipsis was not resolved properly on R7RS `syntax-rules`
- `thread-pool-task-running?` raised an error.

Improvements:

- Building on FreeBSD uses `gc-threaded` if both `gc` and `gc-threaded` are found.
- Testing script detects timeout.
- Following the latest version of `match`.