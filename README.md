# PyODESolve - incomplete solver prototype

**Status: scaffold, not a working numerical solver.** The checked-in package cannot currently be imported because `ODEResult` is not implemented. `BaseODESolver`, `SolverStatistics`, `DormandPrince`, `BDF` and `RadauIIA` are also placeholders.

This repository contains a proposed ODE-solver API, packaging files, example usage and tests. The bundled `pyodesolve_v0.1.0.zip` contains the same placeholder implementations; it is not a working release.

## Current contents

| Path | Current status |
| --- | --- |
| `pyodesolve/api.py` | Proposed method-dispatch interface |
| `pyodesolve/core/` | Missing core class implementations |
| `pyodesolve/explicit/` | Dormand-Prince placeholder |
| `pyodesolve/implicit/` | BDF and Radau placeholders |
| `examples/` | Usage examples awaiting a working implementation |
| `tests/` | Existing tests blocked by package import |

## Recovery and validation

Restore the actual implementations from a verified source before claiming solver support, stability, accuracy or performance. See [GETTING_STARTED.md](GETTING_STARTED.md) for the missing-file map and acceptance criteria.

The previous README's solver orders, DAE support, step counts and speed comparisons have not been established by the checked-in code. The API name `DOP853` also needs review against the actual method coefficients once recovered. Do not infer numerical capabilities from class or method names.

This repository is a candidate for archival if no implementation is recoverable and development is no longer planned. Preserve the source history and link to any maintained successor before archiving.

## License

See [LICENSE](LICENSE). Retain attribution when restoring code from another source.

## Maintaining this repository

See [CONTRIBUTING.md](CONTRIBUTING.md) for the directory map, output conventions, provenance and cleanup boundaries.
