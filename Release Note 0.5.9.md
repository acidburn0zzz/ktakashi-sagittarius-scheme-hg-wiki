Fixed bugs:

- `(rfc tls)` did not caclculate MAC properly. #63
- R7RS `syntax-rules` did not allow dot after ellipsis. #64
- Compiler raised an error when macro expression was not proper list. #65
- SRFI-9 `define-record-type` did not work in a library. #66
- R7RS `let-syntax` and `letrec-syntax` did not allow more than one bindings. #67
- R6RS/R7RS tests hung on BSD OS. #70
- `process-wait` did not return proper value on BSD OS. #71
- `define-library` without `export` clause raised an error.
- Library `(sagittarius)` was loaded with `-t` option. #74

Improvements: 

- `:allow-other-keys` now keeps argument order. #68
- `(scheme r5rs)` now exports all auxiliary syntaxes, `=>`, `else`, `unquote`, `unquote-splicing` and `syntax-rules`. #73
- Socket input/output port is now bidirectional.
- Sagittarius now can be build on Microsoft Visual C++ Compiler for Python 2.7.

New features:

- MQTT client library `(net mq mqtt)` has been added.
- AMQP client library `(net mq amqp)` has been added.
- Concurrency library `(util concurrent)` has been added. (not documented yet)
- Simple socket server framework library `(net server)` has been added.
- `align-bytevectors` procedure has been added to `(util bytevector)`
- Chunked buffer input and input/output port have been added to `(binary io)`.
- Racket's `htmlprag` compatible library `(text sxml htmlprag)` has been added.
