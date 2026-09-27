# RoleCue flow contract notes

This file documents current product topology. It does not authorize generation, replacement, renaming, or deletion of any flow PNG.

## Current public and account flow

Guest scope is limited to the public landing page and registration. A registered user reaches Login, Forgot Password, Set New Password, Profile, and Account Security according to the finalized authentication contract. Registration selects Candidate or Recruiter; role resolution leads to the appropriate workspace. Public pricing, credit-package routes, and anonymous interview demos are not canonical flow nodes.

## Current Candidate practice flow

```text
Candidate Dashboard
→ Target JD Library or Add Target JD
→ Raw JD input/PDF upload
→ AI extraction (non-screen)
→ Review & Refine Extracted JD, including optional refinement notes
→ Configure Interview Session
→ internal Blueprint generation (non-screen and hidden)
→ Test Audio & Interview Readiness
→ Live 3D Interview Room
→ Interview Performance Report
→ History / repeat configuration
```

- A Target JD is private Candidate practice data, distinct from a Recruiter Job Posting.
- The Candidate confirms extracted JD information and can add natural-language notes such as excluding a technology/topic.
- The Interview Blueprint is generated internally from approved inputs. It is never shown, edited, or confirmed by the Candidate.
- `Configure Interview Session` is one composite capability. Its allowed interviewer option, Voice Profile, environment, difficulty, and duration/question budget remain inside that experience.
- The runtime uses a generic `Question` loop. It does not surface Core Question or Follow-up Question paths.
- The live room includes pause/exit handling and a 2D waveform fallback where 3D/WebGL cannot be used.

## Current Personal 3D Avatar flow

```text
Candidate opens Personal 3D Avatar Studio
→ embedded free Avaturn experience
→ Avaturn-owned capture, validation/retake, preview, customization, and GLB generation
→ final GLB handed to RoleCue
→ RoleCue GLB-to-VRM handling and persistence
→ Candidate-owned personal avatar available in the studio
```

RoleCue does not control the Avaturn capture/customization flow and does not use Avaturn Pro API orchestration for it. The Administrator does not manage a 3D Avatar Catalog or environment catalog.

## Current Job Posting and Application flow

```text
Recruiter creates Job Posting from JD-like content
→ optional AI extraction review and confirmation
→ Recruiter configures company 3D interviewer and Voice Profile
→ submits Job Posting for Admin approval
→ Admin approves or rejects
→ approved Job Posting is available on Candidate Job Board
→ Candidate views posting and applies
→ Candidate uploads CV/resume
→ Candidate completes required locked interview
→ Interview Result is attached to completed Application
→ completed Application becomes available to Recruiter
→ Recruiter records Approve or Reject
```

- A Recruiter Job Posting is the company Job Description; there is no separate Corporate JD product entity.
- For a Job Posting interview, the Recruiter's company interviewer model and Voice Profile are fixed. The Candidate cannot override them.
- Recruitment stops at binary Application Approve / Reject. There is no shortlist Kanban, multi-stage ATS, scheduling, offer, or onboarding flow.
- Recruiters directly own their Job Postings and received applications. There is no company tenancy or tenant switching.

## Current Administrator operations flow

Administrator operations start at the Governance Console and cover:

- Candidate/Recruiter account governance and lock/unlock.
- Job Posting moderation queue and approve/reject review.
- Interview-session oversight and operational detail.
- Interview feature configuration, AI Behaviour Management, and evaluation-criteria calibration.
- Provider-sourced Voice Profile viewing/fetching/curation.
- Membership payment transaction ledger, revenue report generation, and membership-price updates.

Administrator operations do **not** include 3D Avatar Catalog management, background/environment catalog management, a credit-wallet operation, or full ATS governance.

## Preserved historical flow PNGs

| Path | Status | Reason |
|---|---|---|
| `flows/00-system-overview.png` | `HISTORICAL / STALE` | Represents former Candidate/Admin-only topology and stale credit/admin assumptions. |
| `flows/01-candidate-flow.png` | `HISTORICAL / STALE` | Represents exposed Blueprint generation/preview/confirmation. |
| `flows/02-admin-flow.png` | `HISTORICAL / STALE` | Represents obsolete avatar-related administration and omits current Recruiter/moderation topology. |

The current business-flow documentation above is the contract source for later diagram production. The preserved PNGs remain historical assets only.
