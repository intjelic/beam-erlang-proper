# BEAM PropEr package guidance

Read ../AGENTS.md. This repository owns the experimental ordinary
`erlangsters/proper` development package, its imported framework sources,
headers, examples and original tests. Read README.md and docs/maintenance.md
before changing imported files. The scaffold is unfinished; buildability and
runtime compatibility are unestablished.

The root import commit preserves the exact upstream PropEr tree. UPSTREAM_COMMIT
identifies its source revision. Preserve source bytes, module names, generators,
shrinking behavior, test assertions and upstream GPL notices until a scoped
adaptation deliberately changes them. Keep unresolved requirements explicit in
docs/dependencies.md; the provisional manifest supplies no dependency closure.

Future builds and tests must use explicitly selected installed public BEAM SDKs.
Do not use private VM headers, sibling source/build dependencies, external Erlang
execution, Rebar, automatic fetching or OTP application startup as a fallback.
Compiler transforms and their dependencies need explicit compiler-side selection;
compiler-private helpers are not public runtime dependencies.

Build and install only under ignored build/ and install/. Keep temporary plans,
investigations and run logs outside tracked product source. Future runners own
their inputs, resources and cleanup. Preserve unrelated changes and work in
this checkout. No further commits, remotes, pushes, publication or system
installation are implied.
