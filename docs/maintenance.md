# Source maintenance

The upstream base is [PropEr v1.5.0](https://github.com/proper-testing/proper/tree/v1.5.0)
from `proper-testing/proper` at commit
`5640d0715d4b346676267504d8e84398e2a29f75`. UPSTREAM_COMMIT contains exactly
that 40-character SHA and a newline. Use the exact committed tree when comparing
or reproducing the import.

The repository's root commit contains the complete, unmodified upstream file
tree, including its original modes. The BEAM scaffold retains `src/*.erl`, all
four `include/*.hrl` files, `examples/`, COPYING and THANKS unchanged. The original
`test/` directory maps to `tests/upstream/` without source or assertion changes.

The scaffold omits the upstream Rebar and Make recipes, application descriptor,
scripts, PLT directory, documentation and GitHub Actions workflows. Their
original content remains in the root import commit. The provisional manifest
replaces the build inventory; it is not a working recipe or dependency closure.

Preserve the upstream license text and individual source notices. Keep future
BEAM adaptations distinct from upstream updates. Review a new exact revision's
source and license changes before updating the pin; do not silently overwrite
adaptations or original test assertions. Imports and structural checks establish
no runtime or source-compatibility qualification.

Future builds must use a selected installed public BEAM SDK and these owned
source files, without reading an upstream checkout or reference tree.
