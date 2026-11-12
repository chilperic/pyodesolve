# Repository structure and contribution guide

This guide separates maintained code, inputs, provenance and disposable outputs. It does not move existing files.

| Location | Purpose |
| --- | --- |
| `pyodesolve/` | Package scaffold. Six core and solver implementation files are placeholders. |
| `examples/` | Proposed usage examples; currently blocked by the missing implementations. |
| `tests/` | Existing tests; import currently fails before they can establish numerical correctness. |
| `pyodesolve_v0.1.0.zip` | Historical archive, also containing placeholders. Preserve until a tested release replaces it. |
| `GETTING_STARTED.md` | Recovery steps and acceptance criteria. |

## Outputs and version control

Use root `outputs/` or `tmp/` for disposable local runs. Curated figures, datasets, manuscripts, reference outputs and reproducibility evidence should be committed explicitly in their relevant project directory. Do not hide all PDFs, PNGs, CSVs, notebooks or HTML files with extension-wide ignore rules.

The ignore file prevents accidental additions of local environments, caches and credentials. It does not remove files that are already tracked and it does not erase Git history. Review `git status --short` before committing. Preserve lockfiles and sanitized environment examples when they are introduced.

Keep reusable code in the existing package/module directories and executable workflows in `scripts/` or `tools/`. Preserve original research material and its attribution under the existing provenance directories. A historical folder is not proof that its code is obsolete or safe to delete.
