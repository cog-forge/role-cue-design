# RoleCue design workspace

Canonical design-contract repository for RoleCue's approved OpenDesign-derived visual language and its current Candidate, Recruiter, Administrator, public, and interview-runtime UX scope.

## Repository entrypoints

1. [`DESIGN.md`](./DESIGN.md) — authority hierarchy, product boundaries, shells, density, runtime, accessibility, and historical-artifact policy.
2. [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md) — canonical manifest of **70** retained user-facing screens/subviews: 48 `DRAW`, 22 `DOC-ONLY`; also identifies preserved historical artifacts.
3. [`SCREEN-NOTES.md`](./SCREEN-NOTES.md) — product-only notes for every current canonical screen target.
4. [`flows/NOTES.md`](./flows/NOTES.md) — current public/account, Candidate, Personal 3D Avatar, Recruiter/Application, and Administrator flow contracts; preserved flow PNGs are labelled where stale.
5. [`references/open-design/source-system/`](./references/open-design/source-system/) — read-only visual authority. Do not modify it.
6. [`brand/`](./brand/) — approved RoleCue Split Halo vector assets. Do not modify during product-contract sync.

## Artifact policy

- `screens/` and `flows/` contain preserved visual artifacts, not an automatically current product manifest. Consult the inventory status before using one.
- `references/open-design/*.webp`, `brand/*`, and `references/open-design/source-system/*` are frozen for this workstream.
- This repository does not authorize screen generation, image replacement, Figma/Stitch work, HTML/CSS prototypes, or implementation code during a documentation/contract sync.
