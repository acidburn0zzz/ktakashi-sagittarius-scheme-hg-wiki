- Move macro related VM register to Scheme world.
    1. `boot/lib/macro.scm` should have all of them (c.f. `usage-env` and so)
    2. `make-macro-transformer` should be implemented in Scheme for simplicity.
    3. `Sg_MacroExpand` should be placed in Scheme.
- Remove cache related VM register from VM.
- (Should we?) Remove load path releated VM register form VM.