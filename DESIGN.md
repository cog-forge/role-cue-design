# RoleCue Design System & Product Contract

This is the current RoleCue design contract for people designing, reviewing, or implementing RoleCue. It synchronizes product and UX scope and defines the current visual authority model. Where older assets or references conflict with this contract, this contract governs RoleCue's visual direction.

## 1. Canonical authority hierarchy

Product and visual authority are deliberately separate.

### Product / UX truth

When sources conflict, use the following order:

1. The latest canonical RoleCue Brain/contracts in `/home/dorriss/Documents/SEP490/`.
2. [`2026-09-27-navigation-screen-contract-pruned.md`](/home/dorriss/Documents/SEP490/99_Inbox/2026-09-27-navigation-screen-contract-pruned.md), the finalized screen and navigation staging contract.
3. [`Report7_Final_Project_Report.pdf`](/home/dorriss/Documents/SEP490/production_report/Report7_Final_Project_Report.pdf), read as a lower-priority report source.
4. Finalized main business flows in the canonical vault.
5. This repository's Markdown documents, which record the synchronized design contract rather than superseding the sources above.

The finalized formal use-case count is **57**. [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md) is the repository's current manifest of the **70 retained user-facing screens and subviews**: 48 `DRAW` and 22 `DOC-ONLY`. Internal automation is not a screen deliverable.

### Visual authority

Visual authority has two complementary layers. OpenDesign is the structural, interaction, and editorial reference for how an interface is constructed. RoleCue's approved brand assets and this current brand contract define whose interface it is and how RoleCue is visually expressed. OpenDesign's own branding and source colors are not RoleCue brand tokens.

#### Structural / interaction / editorial authority

The frozen [`references/open-design/source-system/`](./references/open-design/source-system/) material is the primary reference for:

- composition and layout geometry
- typography hierarchy and spacing rhythm
- surface treatment, border/elevation discipline, and information density
- responsive behavior and interaction patterns
- motion restraint and editorial presentation grammar

The source files are read-only reference evidence. Their original green/lime branding and tokens are intentionally preserved there, but do not define RoleCue's brand color.

- [`SOURCE-DESIGN.md`](./references/open-design/source-system/SOURCE-DESIGN.md) — design-construction thesis, layout, surface, and interaction grammar.
- [`SOURCE-TOKENS.md`](./references/open-design/source-system/SOURCE-TOKENS.md) — source colors, typography, spacing, radii, elevation, and borders.
- [`SOURCE-PATTERNS.md`](./references/open-design/source-system/SOURCE-PATTERNS.md) — architectural layout and presentation patterns.
- [`SOURCE-COMPONENTS.md`](./references/open-design/source-system/SOURCE-COMPONENTS.md) — component appearance, interaction physics, controls, and states.

#### RoleCue brand authority

RoleCue's canonical approved brand assets and this current brand contract define product identity, logo/mark, wordmark, brand color, brand accent usage, and product-specific visual expression. The approved team RoleCue logo/mark is authoritative. OpenDesign branding itself is not RoleCue branding, and RoleCue is not required to preserve OpenDesign's Signal Lime.

### Provenance and frozen references

- [`SOURCE-AUDIT.md`](./references/open-design/source-system/SOURCE-AUDIT.md) records the source extraction audit.
- [`references/open-design/*.webp`](./references/open-design/) are frozen visual-memory references.
- [`brand/`](./brand/) contains historical approved RoleCue vector assets; its blue identity assets still require synchronization with the current direction below.
- Existing PNGs in [`screens/`](./screens/) and [`flows/`](./flows/) are preserved visual artifacts. Their current product status is explicitly classified in [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md) and [`flows/NOTES.md`](./flows/NOTES.md).

> [!important]
> Product wording and navigation may change as canonical RoleCue scope changes. RoleCue's brand layer is applied to the construction grammar in the frozen OpenDesign reference. This contract supersedes older RoleCue color direction in historical assets; canonical blue brand assets must be synchronized. OpenDesign source files remain frozen and must not be recolored.

## 2. Product definition and boundaries

### What RoleCue is

RoleCue is an AI-supported technical interview practice platform with a lightweight, moderated recruitment board.

- A **Candidate** privately manages Target Job Descriptions for practice, reviews AI-extracted technical information, adds natural-language refinement notes, configures a session, completes an interview, and reviews results.
- A **Recruiter** owns Job Postings, which are the company's Job Descriptions in the recruitment context. The Recruiter configures the company interviewer and Voice Profile, submits the posting for moderation, receives completed applications, and records an Approve or Reject decision.
- An **Administrator** governs accounts, Job Posting moderation, interview operations, AI/evaluation settings, provider-sourced Voice Profiles, and membership financial operations.
- A **Guest** has the restricted public entry scope defined by the canonical contract: landing and account registration. Login remains the authentication entry point for registered users; public pricing and anonymous product demos are not canonical guest destinations.
- **Better Auth** is the selected authentication library. This contract specifies only user-facing behaviors (registration, login, Forgot Password/Set New Password, Change Password, and eligible 2FA), not library internals.

### What RoleCue is not

- Not an AI chatbot, surveillance tool, or punitive proctoring experience.
- Not a full ATS: no shortlist Kanban, multi-stage pipeline, ranking, interview scheduling, offers, or onboarding.
- Not a multi-tenant company-workspace system: no organizations, tenant switching, membership administration, or company tenancy.
- Not a credit-wallet product: no practice-credit ledger, packs, per-interview deductions, or public credit-package pricing.
- Not a 3D marketplace or community-publishing product.

### Core domain distinctions

- **Target JD for Practice:** private Candidate-owned practice input. Raw JD → AI extraction → Candidate review/refinement → confirmation. Refinement notes influence the internal preparation plan.
- **Job Posting:** Recruiter-owned company Job Description and public vacancy after Administrator approval. Do not introduce a separate Corporate JD entity.
- **Interview Blueprint:** internal only. It is generated from confirmed inputs, remains hidden from Candidates, and is never previewed, edited, or confirmed by them.
- **Question:** the generic runtime unit. The LLM determines subsequent Questions from the Answer and immutable Interview Context; the UX does not expose separate Core Question or Follow-up Question paths.
- **Membership:** Candidate subscription status gates access where required. Payment transactions are recorded; credits are not.

## 3. Brand identity and visual thesis

The canonical RoleCue identity is BLUE. The approved team RoleCue logo/mark is authoritative. Blue is a restrained, intentional product identity/accent color, not a mandate for a blue-heavy interface. Near-black remains the primary action and text authority. Neutral near-white/white surfaces remain the primary canvas and material system. Rich imagery and media may carry more chroma than interface chrome.

> Blue identifies RoleCue. Black drives action. Media carries emotion.

Keep the interface bright, editorial, professional, modern, restrained, and high-craft. Use blue purposefully for brand recognition and selected accents; preserve clear action hierarchy through near-black. Maintain generous neutral surfaces, disciplined borders/elevation, and readable typography.

Explicitly reject blue-purple AI gradients, neon blue glow, cyberpunk styling, glassmorphism, generic AI blobs, excessive pill UI, dense card soup, and arbitrary decorative blue everywhere. Do not recolor third-party provider brands into RoleCue blue.

Canonical approved brand assets belong in [`brand/`](./brand/). The current directory still contains the historical Split Halo assets [`rolecue-logo.svg`](./brand/rolecue-logo.svg), [`rolecue-icon.svg`](./brand/rolecue-icon.svg), and [`rolecue-wordmark.svg`](./brand/rolecue-wordmark.svg); they are preserved, but their green accent does not supersede this contract. Canonical blue brand assets must be synchronized by the team. Do not fabricate or recolor those assets, and do not typeset a custom wordmark with a substitute font.

### OpenDesign adaptation rule

OpenDesign implementation and reference material may be studied and decomposed for design intent. Production RoleCue UI must be re-authored through the RoleCue brand layer. Reuse construction grammar such as navbar geometry, hero composition, spacing, typography hierarchy, motion behavior, interaction physics, and responsive logic. Do not literally copy OpenDesign branding, its green/lime accent, logos, product wording, or proprietary identity.

**Reuse the grammar, not the branding.**

## 4. Core product shells

```text
RoleCue application suite
├── Public / authentication shell
├── Candidate workspace
├── Recruiter workspace
├── Interview runtime room
└── Administrator operations workspace
```

1. **Public / authentication shell:** landing, registration, login, Forgot Password journey, profile, and security account paths. It does not require a public pricing destination.
2. **Candidate workspace:** lower-density practice, Target JD, personal avatar, evaluation, job-board/application, membership, and account work. Do not present Blueprint controls here.
3. **Recruiter workspace:** operational Job Posting and Application work, with clear list/detail relationships. It is more operational than Candidate work but less governance-heavy than Administrator work.
4. **Interview runtime room:** a focused spoken-interview environment for both Candidate practice and Job Posting interviews.
5. **Administrator operations workspace:** high-density governance for accounts, Job Posting moderation, sessions, AI/evaluation configuration, Voice Profiles, and financial reporting. It has no avatar-catalog or environment-catalog area.

## 5. Density and runtime principles

| Dimension | Candidate workspace | Recruiter workspace | Administrator workspace |
|---|---|---|---|
| Primary mode | Guided individual practice | Posting/application operations | Platform governance |
| Density | Low to medium | Medium | Medium to high |
| Information shape | Clear next action and progress | Lists, filters, detail dossiers | Dense records, controls, and audit context |
| Scope guardrail | Supportive, non-proctoring | No ATS pipeline | No 3D avatar/background catalog |

The live interview room is a confidence-building rehearsal space:

- Clearly communicate turn ownership: interviewer speaking, candidate response, and processing.
- Use a supportive, non-proctoring tone; never add surveillance framing or artificial progress percentages.
- Present the 3D interviewer stage without distracting workspace chrome.
- When WebGL cannot be used, preserve the spoken interaction with the canonical 2D animated waveform fallback.
- Require explicit confirmation before an early exit. Do not describe a credit consequence.
- For a Target JD session, the Candidate chooses an allowed system or personal 3D interviewer option and an allowed Voice Profile as part of **Configure Interview Session**. For a Job Posting session, the Recruiter's company interviewer and Voice Profile are fixed and cannot be overridden.

## 6. Personal 3D Avatar boundary

Personal 3D Avatar generation is in scope, with a strict integration boundary:

1. Candidate opens **Personal 3D Avatar Studio**.
2. The embedded **free Avaturn** experience owns photo capture, validation/retakes, generation/preview, accessories/customization, and final GLB generation.
3. Avaturn hands the final GLB to RoleCue.
4. RoleCue handles GLB-to-VRM conversion and persistence of the Candidate-owned avatar.

Do not describe Avaturn Pro API orchestration, a paid API, or RoleCue-controlled photo capture. Administrators curate provider-sourced Voice Profiles, not 3D avatars or environment presets.

## 7. Accessibility and responsive constraints

Keep the established WCAG-oriented contract:

- Do not use color alone for status; pair status with text and a visible cue.
- Keep accessible focus treatment, explicit form labels, associated error/help text, and at least 44 × 44 px touch targets.
- Respect reduced-motion preferences.
- Preserve the canonical 1440 px desktop, 1280 px laptop, and 390 px mobile constraints where the screen supports them.
- Candidate and Recruiter workspace screens should retain readable, role-appropriate density. Administrator tables and records may be denser without compromising operability.
- The live runtime is desktop/laptop-first; do not promise a redesigned mobile runtime beyond the canonical degradation/support constraints.

## 8. Screen and artifact taxonomy

The authoritative screen classification is the staging contract:

| Classification | Meaning | Inventory treatment |
|---|---|---|
| `DRAW` | Major navigable page or meaningful user-opened subview | Canonical design target and navigation-flow node |
| `DOC-ONLY` | Legitimate UI subview, panel, drawer, modal, or confirmation | Canonical design target, omitted from navigation-flow drawing |
| `NON-SCREEN` | Internal system or automated function | Documented only as behavior; no screen target |
| `REMOVE` | Contradicted legacy concept | Historical/provenance only; never a canonical target |

The terms `TOP-LEVEL SCREEN`, `SUPPORTING UX STATE`, and `PROCESS STATE` may be used descriptively inside a screen note, but must not create additional deliverables beyond the 70 retained `DRAW`/`DOC-ONLY` records.

## 9. Artifact handoff and historical-artifact policy

The canonical targets are the screen records marked `EXISTING / NEEDS CONTENT SYNC` or `TO DESIGN` in [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md). A target path is a future handoff location, not authorization to generate or replace an image during this pass.

- Existing `screens/**/*.png`, `flows/**/*.png`, `references/open-design/*.webp`, `brand/*`, and `references/open-design/source-system/*` remain preserved.
- A historical artifact may retain good visual language while no longer represent current product scope. It must be labelled `HISTORICAL / STALE` rather than silently reused.
- No HTML, CSS, React, Figma, Stitch output, image regeneration, or implementation artifact is a result of this documentation phase.

## 10. Screen notes and flow documentation

[`SCREEN-NOTES.md`](./SCREEN-NOTES.md) records only the canonical frame name, target path, classification, purpose, primary action, important information, navigation, UX constraints, and design status. A `TO DESIGN` note intentionally does not prescribe a new layout.

[`flows/NOTES.md`](./flows/NOTES.md) describes the current Candidate, Recruiter, Administrator, Personal 3D Avatar, and interview/application lifecycles. It does not authorize regeneration of the preserved flow PNGs.
