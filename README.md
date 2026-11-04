# BEAM PropEr package scaffold

`erlangsters/proper` 0.0.1 is a provisional ordinary BEAM/Erlang development
package for property-based testing. Its framework sources, headers, tests and
examples are unchanged copies of [PropEr v1.5.0](https://github.com/proper-testing/proper/releases/tag/v1.5.0).
**The package is unfinished: compilation, execution and compatibility are unestablished.**

The provisional `beam.toml` inventories the framework sources and headers.
It declares no application startup, native build, entry point or test task.
The original `proper` APIs, generators and compiler transforms retain their
upstream names. Their BEAM/Erlang integration remains unresolved.

`tests/upstream/` preserves the original test modules; `examples/` preserves the
original examples and include fixture. Neither directory is part of the
production source inventory. There is no runnable acceptance harness or workflow.

See [dependencies](docs/dependencies.md) for unresolved requirements and
[maintenance](docs/maintenance.md) for source ownership and the original import.
The package version is independent of the upstream PropEr release version.

The upstream [license text](COPYING), [acknowledgements](THANKS), copyright and
GPL-3.0-or-later source notices are preserved.

Project website: [BEAM/Erlang](https://beam.erlangsters.org/).
