Fixed bugs:

- Multipart sender for HTTP/2 didn't send data correctly
- Non blocking server of `(net server)` used only one thread
- Size limited shared priority queue expanded on race condition of removal and addition

Improvements:

- SSE detection on FreeBSD is added (Thanks to Ashish SHUKLA)
- Faster thread creation. (approx. 10 times faster)

New features:

- Sandboxing library `(sagittarius sandbox)` has been added
- Mocking library `(sagittarius mock)` has been added
- Monitoring procedures are added to `(net server)`
- `shared-priority-queue-capacity` has been added to `(util concurrent shared-queue)`
- `shared-queue->list` and `shared-priority-queue->list` have been added to `(util concurrent shared-queue)`
- Actor model library `(util concurrent actor)` has been added
- SRFI-158 has been supported
- Non blocking server now supports socket detaching
- Experimental combinator library `(sagittarius combinators)` has been added
- Experimental PEG library `(peg)` has been added

Backward incompatible change:

- Applied the latest errata of SRFI-115 and implementation