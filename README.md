# RoleCue design workspace

Canonical design-contract repository for RoleCue's current brand contract, frozen OpenDesign structural/editorial reference, and Candidate, Recruiter, Administrator, public, and interview-runtime UX scope.

## Repository entrypoints

1. [`DESIGN.md`](./DESIGN.md) — current RoleCue design contract: visual authority model, brand direction, product boundaries, shells, density, runtime, accessibility, and historical-artifact policy.
2. [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md) — canonical manifest of **70** retained user-facing screens/subviews: 48 `DRAW`, 22 `DOC-ONLY`; also identifies preserved historical artifacts.
3. [`SCREEN-NOTES.md`](./SCREEN-NOTES.md) — product-only notes for every current canonical screen target.
4. [`flows/NOTES.md`](./flows/NOTES.md) — current public/account, Candidate, Personal 3D Avatar, Recruiter/Application, and Administrator flow contracts; preserved flow PNGs are labelled where stale.
5. [`references/open-design/source-system/`](./references/open-design/source-system/) — frozen structural, interaction, and editorial reference material. Its source branding is not RoleCue branding; do not modify it.
6. [`brand/`](./brand/) — canonical RoleCue brand assets. Historical approved assets are preserved, and this directory must be synchronized with the current blue identity defined in `DESIGN.md`.

## Artifact policy

- `screens/` and `flows/` may contain historical visual artifacts, not an automatically current product manifest. Consult the inventory status before using one.
- `references/open-design/*.webp` and `references/open-design/source-system/*` are frozen source/reference material.
- This repository does not authorize screen generation, image replacement, Figma/Stitch work, HTML/CSS prototypes, or implementation code during a documentation/contract sync.
