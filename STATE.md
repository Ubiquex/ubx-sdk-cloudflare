# STATE.md -- current state

> Rewritten, not appended, as the LAST act of every session. See `HISTORY.md`
> for the narrative.

## In flight

Nothing in flight as of 2026-09-04. This file's own "just scaffolded"
claim above was stale -- this repo has since published for real
multiple times; don't trust an unrewritten STATE.md's own age claims,
re-check.

## Blocked

Nothing blocked. Zero open PRs.

## Current state

**`translator-watch.yml` is now live (UBI-249).** This repo's own
`hash-watch.yml` already auto-regenerates and correctly commits
`PROVENANCE.json` on real spec drift; `translator-watch.yml` adds the
other, independent trigger (a translator-tag move) that path never
covered -- regenerates holding the schema fixed at this repo's own
pinned version, self-heals (`PROVENANCE.json` only) on an empty diff,
opens a real review PR on a genuine one. Never auto-merges.

This repo's own `--descriptions-dir` fix (a session-wide gap: every
hand regeneration had omitted the flag) and a stale `PROVENANCE.json`
correction (had `source: "explicit-binary"`, no `commit`/`repo_path` at
all, `schema_version` frozen at 1.0.0 while the committed schema had
already moved to 1.0.2) both merged this same arc.

Published: npm/PyPI `1.0.1` (verified directly against the registries).
Committed: `1.0.2` (ahead, not yet published -- no bump needed until a
real publish is dispatched). `PROVENANCE.json` now records a real,
verified `ubx-provider-dynamic` commit (`dba9b68`, tag `v1.0.13`).

`VERSION` at repo root records the real upstream spec this generation was
fetched from.

## Before touching anything

- Never self-merge here. See `CLAUDE.md`.
- Never hand-edit generated bindings -- fix the generator or the upstream
  schema, then regenerate.
