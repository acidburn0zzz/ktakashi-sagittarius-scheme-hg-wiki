Fixed bugs:

- Issue: #243: yaml-write raises an error with valid YAML
- Issue: #244: Null value of YAML object can't be written
- Issue: #245: Invalid cache on (test r6rs hashtables)
- Issue: #246: Sliced definition of let-syntax inside of let raises an error

New features:

- URI template library `(rfc uri-template)` has been added.
- Vector utilities library `(util vector)` has been added.
- JMESPath library `(text json jmespath)` has been added.
- Character specialised PEG utility library `(peg chars)` has been added.
- JSON patch library `(rfc json-patch)` has been added.
- Extensible vector like data structure library `(util flexible-vector)` has been added.
- Multiple HTTP header value reference procedure `rfc5322-header-ref*` has been added to `(rfc :5322)`
- JSON structure comparison library `(text json compare)` has been added.

Improvements:

- `(text yaml)` writes multi-lined string prettier
- Errata of SRFI-115 is applied.

Backward incompatible changes:

- Post finalisation of SRFI-144 has been applied. `flonum` procedure returns `+nan.0` if it's not a flonum.