# Recovering the PyODESolve prototype

The current checkout is incomplete. Installing the package does not supply the missing solver classes, and importing it currently raises an `ImportError` for `ODEResult`.

| Missing class | Destination |
| --- | --- |
| `BaseODESolver` | `pyodesolve/core/base.py` |
| `ODEResult` | `pyodesolve/core/result.py` |
| `SolverStatistics` | `pyodesolve/core/statistics.py` |
| `DormandPrince` | `pyodesolve/explicit/dormand_prince.py` |
| `BDF` | `pyodesolve/implicit/bdf.py` |
| `RadauIIA` | `pyodesolve/implicit/radau.py` |

1. Recover the original implementation and its provenance. The included ZIP also contains placeholders.
2. Confirm method coefficients, solver orders, error estimates and supported problem classes. Resolve the `DOP853` naming mismatch before documenting a numerical method.
3. Restore and review the core classes and relative imports.
4. Run `python -c "import pyodesolve"`, then the existing tests and examples from this repository.
5. Add meaningful convergence, tolerance, failure-mode and reference-solution checks before claiming accuracy or performance. DAE support needs its own formulation and tests.
6. Publish benchmarks only with runnable problem definitions, tolerances, environment and measured results.

If implementation recovery is not planned, keep the repository as an explicitly incomplete historical prototype and archive it after recording that status.
