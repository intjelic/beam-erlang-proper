# Current dependency boundary

The imported framework has no resolved BEAM/Erlang dependency closure. Its
provisional manifest records the source and header inventory only. Upstream
module names and calls to ordinary OTP support remain unadapted.

Framework compilation itself uses a parse transform: `proper_gen.erl` selects
`vararg`, which the upstream recipe compiles first. Client headers also select
`proper_unused_imports_remover`, `proper_transformer` or `proper_prop_remover`.
Current package builds disable transforms and do not support nonempty build
dependencies. Compiler-side tool selection and compilation order remain
unimplemented; runtime dependencies alone cannot provide this integration.

`proper.hrl` includes `proper/include/proper_common.hrl`. Exporting the header
files does not by itself preserve this library-root spelling. Header resolution
needs explicit source inputs, without OTP application discovery or startup.

Random generation, shrinking, state-machine testing and type/specification
inspection use ordinary library, I/O, compiler and code-inspection facilities.
Their modern providers and host capabilities have not been selected. Requirements
must be assessed by feature, including abstract-code metadata and any runtime
compilation or filesystem operations. Compiler-private helper availability does
not establish a public runtime dependency.

The original tests and examples include EUnit and property-testing inputs.
Development dependency selection, a test runner and reproducible seed and
counterexample handling are not integrated. No fallback to external Erlang/OTP,
implicit native loading or automatic dependency acquisition is supplied.
