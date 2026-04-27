# LUXFI-FORK

This is a luxfi-maintained fork of [PQClean/PQClean](https://github.com/PQClean/PQClean).

## Pin

* Upstream branch: `master`
* Commit SHA: `3730b32aa50ba9e712592c1476bdd048f5f6ed7e` (2026-01-09)
* License: per-implementation (CC0 / public-domain / MIT / Apache-2.0). See
  each `crypto_*/.../LICENSE` and `LICENSE` files in the tree.

## Why this fork exists

PQClean ships clean reference implementations of NIST PQC finalists (ML-DSA,
ML-KEM, SLH-DSA). luxcpp/crypto vendors these for `mldsa/`, `mlkem/`, and
`slhdsa/` (LP-137 sibling #102). Owning the fork pins the reference impls so
upstream churn (refactors, NIST round-update reshuffles) never silently breaks
KAT vectors in luxcpp/crypto.

## Sync policy

* Track upstream `master` snapshots, NOT HEAD.
* Pull upstream into `sync/<yyyy-mm-dd>` branches. Re-run all luxcpp/crypto
  KAT suites for `mldsa`, `mlkem`, `slhdsa`. Merge to `master` only when KATs
  match.
* NIST round changes: update the pin, re-run KATs, tag as `pqclean-luxfi.<n>`.

## Maintainer

luxfi crypto team. Contact via the `luxfi/crypto` repo.
