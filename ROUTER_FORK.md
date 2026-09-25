# Embedded Codex Router fork

`router/` is the source of the Codex Router runtime used by this project. It is
a regular, versioned directory in this repository — not a submodule, generated
artifact, package-manager indirection, or clone under `~/.local/share`.

## Imported snapshot

- Upstream project: `duolahypercho/codex-router`
- Upstream base: `9c0db45676238d032757370ec4010b66b6759dd8`
- Integrated fork snapshot: `576dba20f02d97822a8170eccf09bb484a6db273`
- Imported: 2026-09-21
- License: MIT, retained at `router/LICENSE`

## GitHub fork and upstream merge

- GitHub fork: `https://github.com/misternay/codex-router`
- Jev integration branch: `jev-integration` (also the fork's `main`)
- Jev integration merge: `65a89a8b` (upstream `main` at `6279f39d`)
- Current fork revision: `bac46b24322cda609abd9aa3202770e1756824b3`
- Merged into this embedded directory: 2026-09-25

The integration branch preserves the original fork ancestry, carries the
committed `router/` changes from this project, and merges upstream `main`.
The embedded directory is a copy of that branch's tree. Continue upstream
work in the GitHub fork and copy reviewed merges into `router/` deliberately.

The snapshot includes the local fork changes that preserve complete canonical
replay for `jev/auto`, keep its prompt-cache identity, carry the routed reasoning
effort, preserve tool traffic across conversation windows, and separate
post-prologue stream stalls from the initial prelude timeout.

## Ownership

Runtime behavior shared with Codex is changed and tested under `router/`.
Jev's typed decision policy and relay are changed and tested under `server/`.
Generated files under `~/.codex/codex-router` remain runtime state and must not
be copied back into the repository.

Future upstream updates are deliberate source merges into `router/`, followed by
the embedded router suite and the Jev end-to-end contract tests. The installed
service never pulls or updates another repository by itself.
