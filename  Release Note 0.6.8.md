Fixed bugs:

- `"2.225073858507201e-308"` can't be converted to number. #144
- `(regex "a/b")` returns unreadable regex literal. #145
- `(security keystore)` with JKS or JCEKS has unbound variables.
- `pid->process` didn't work on Windows.
-  Incorrect calculation of `add-duration` and `subtract-duration` has been fixed.

Improvements:

- Windows environment got stabler.
- Generating TZ database can be done with local files.
- Building OS X can be done without specifying libffi
- Calling outer loop inside of `guard` consumes less stack.
- Stabilised `(net server)`.
- Thread specific value is available on threads created by `(util concurent thread-pool)`.
- Native stack trace can be shown on Windows when Sagittarius is crashed.
- Native stack trace can be shown on POSIX environment when SEGV or other critical signal is raised.

New features:

- `thread-pool-thread-task-running?` has been added.
- Weak box has been added.
- Draft SRFI 123 has been added.
- Draft SRFI 124 has been added. The implementation does not comply the whole requirement.
- `process-active?` has been added.

New platform:

- OS X environment has been supported. Some of POSIX functionalities are not usable due to the limitation of OS X.