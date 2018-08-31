Fixed bugs:

- R7RS `syntax-rules` didn't escape ellipsis.
- Issue #242: C Assertion of code builder

New features:

- `(rsa pkcs :12)` supports `pbeWithSHAAnd2-KeyTripleDES-CBC`
- SRFI-152 is supported
- SRFI-156 is supported
- YAML parser/writer library `(text yaml)` has been added.
- JSON Schema (draft 7) library `(text json schema)` has been added.
- JSON validation framework library `(text json validator)` has been added.
- `(text toml)` supports version 0.5.0
- URI resource access library `(util uri)` has been added (not documented)