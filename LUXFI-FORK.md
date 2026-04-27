# LUXFI-FORK

This is a luxfi-maintained fork of [PQClean/PQClean](https://github.com/PQClean/PQClean).

## Pin

- Upstream master HEAD mirror: `3730b32aa50ba9e712592c1476bdd048f5f6ed7e`
- License: per-implementation (CC0-1.0 for most, Apache-2.0 / MIT for some;
  see each scheme's `LICENSE` file under `crypto_kem/<scheme>/<impl>/LICENSE`
  and `crypto_sign/<scheme>/<impl>/LICENSE`)

## Why this fork exists

luxcpp/crypto's `mldsa/`, `mlkem/`, and `slhdsa/` cpp bodies consume the
clean reference implementations from PQClean to drive KAT tests and ensure
specification conformance. Pinning to a luxfi-controlled mirror guarantees
deterministic builds and protects against upstream history rewrites or
removals.

## Sync policy

- Track upstream master at tagged release boundaries. Never auto-bump.
- Pull upstream into `sync/<date>` branches.
- Re-run mldsa, mlkem, slhdsa KAT suites before merging to `master`.
- Do not modify clean implementations in this fork. Patches go upstream.

## Maintainer

luxfi crypto team. Contact via the `luxfi/crypto` repo.
