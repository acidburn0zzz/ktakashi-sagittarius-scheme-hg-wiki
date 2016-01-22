Fixed bugs:

- Modifying string returned from symbol->string shouldn't affect original symbol. (Issue #168)
- Internal process of `time-usage` converted micro second to second incorrectly.
- Return value of `uintptr_t` was not handled correctly on 64 bit environment.
- `intptr_t` and `uintptr_t` arguments were treated 32 bit integer on 64 bit environment.

New features:

- Bit field for FFI c structure. (Issue  #169)
- Following the final SRFI-121.
- Supporting SRFI-127.
- Adding new format specifier `~!` which flushes the port.
- More support of SQL on `(text sql)`.
- New style of FFI argument type.
- Null pointer can be passed as callback in FFI.

Improvements:

- SRFI-114 uses builtin symbol comparator.