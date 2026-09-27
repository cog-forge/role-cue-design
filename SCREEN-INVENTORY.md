# RoleCue Canonical Screen Inventory

This is the repository manifest synchronized to the finalized navigation/screen contract at `/home/dorriss/Documents/SEP490/99_Inbox/2026-09-27-navigation-screen-contract-pruned.md`.

## Contract scope and status legend

- **Canonical screen count: 70** retained user-facing screens and subviews: **48 `DRAW`** and **22 `DOC-ONLY`**.
- `DRAW` records are navigation-flow nodes. `DOC-ONLY` records are user-facing panels, modals, drawers, or confirmations excluded from the flow drawing for clarity.
- Automated AI extraction, hidden Blueprint generation, payment callbacks, GLB-to-VRM processing, and runtime orchestration are `NON-SCREEN`; they have no visual deliverable.
- A target PNG path is a future production handoff location. It is not a request to generate an image during this contract sync.

| Design status | Meaning |
|---|---|
| `EXISTING / NEEDS CONTENT SYNC` | A preserved PNG is conceptually compatible but may carry stale product copy or scope. It remains untouched in this phase. |
| `TO DESIGN` | Retained canonical target with no current approved PNG. The path is reserved for the later screen-design production phase. |
| `HISTORICAL / STALE` | Preserved artifact contradicted by scope or no longer a canonical standalone deliverable. It is not counted above. |

## Canonical retained screen manifest

| ID | Classification | Section / canonical frame | Role | Route or product mapping | Concise purpose | Target PNG path | Status |
|---|---|---|---|---|---|---|---|
| `PUB-01` | `DRAW` | Public / Public Landing Page | Guest | `/` | Introduce RoleCue and provide permitted account entry. | `screens/shared/marketing/landing-desktop-1440.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `AUTH-01` | `DRAW` | Authentication / Account Registration | Guest | `/register` | Register a Candidate or Recruiter account. | `screens/shared/auth/register-desktop.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `AUTH-01-SUB1` | `DOC-ONLY` | Authentication / Email Verification Notice | Guest | Registration journey | Confirm verification dispatch and support resend. | `screens/shared/auth/verify-email.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `AUTH-02` | `DRAW` | Authentication / Account Login | Registered user | `/login` | Authenticate and resolve the user to the appropriate workspace. | `screens/shared/auth/login-desktop.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `AUTH-03` | `DRAW` | Authentication / Forgot Password Request | Registered user | `/forgot-password` | Initiate the single password-recovery journey. | `screens/shared/auth/forgot-password.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `AUTH-03-SUB1` | `DOC-ONLY` | Authentication / Password Reset Link Dispatched Notice | Registered user | Forgot Password journey | Confirm recovery-link dispatch without exposing account existence. | `screens/shared/auth/forgot-password-dispatched.png` | `TO DESIGN` |
| `AUTH-04` | `DRAW` | Authentication / Set New Password | Registered user | `/reset-password` | Set a replacement password through the recovery journey. | `screens/shared/auth/reset-password.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `SHARED-01` | `DRAW` | Account / User Profile | Registered user | `/profile` | View and update personal profile and role metadata. | `screens/shared/account/user-profile.png` | `TO DESIGN` |
| `SHARED-02` | `DRAW` | Account / Account Security & Password | Registered user | `/settings` | Manage security settings, password, and eligible 2FA. | `screens/shared/account/account-security.png` | `TO DESIGN` |
| `SHARED-02-SUB1` | `DOC-ONLY` | Account / Change Password Modal | Registered user | Within account security | Replace a known password. | `screens/shared/account/change-password-modal.png` | `TO DESIGN` |
| `SHARED-02-SUB2` | `DOC-ONLY` | Account / Two-Factor Authentication Setup Modal | Registered user | Within account security | Set up 2FA where enabled by the canonical contract. | `screens/shared/account/two-factor-setup-modal.png` | `TO DESIGN` |
| `CAN-01` | `DRAW` | Candidate Workspace / Candidate Dashboard | Candidate | `/dashboard` | Launch practice, review recent work, and surface application status. | `screens/candidate/dashboard.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `CAN-02` | `DRAW` | Target JD / Target JD Library | Candidate | Candidate Target JD workspace | Manage private, reviewed Target JDs for practice. | `screens/candidate/jd-empty-state.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `CAN-03` | `DRAW` | Target JD / Add Target JD | Candidate | `/interviews/new/job-description` | Paste raw JD text or upload a PDF for extraction. | `screens/candidate/jd-add-job-description.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `CAN-04` | `DRAW` | Target JD / Review & Refine Extracted JD | Candidate | `/interviews/new/skills` | Review extracted technical information, refine it, and confirm it. | `screens/candidate/jd-review-and-edit-skills.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `CAN-04-SUB1` | `DOC-ONLY` | Target JD / Refinement Notes Panel | Candidate | Within extracted-JD review | Add natural-language instructions that influence hidden preparation. | `screens/candidate/jd-refinement-notes-panel.png` | `TO DESIGN` |
| `CAN-05` | `DRAW` | Personal 3D Avatar / Personal 3D Avatar Studio | Candidate | Candidate avatar workspace | Launch creation and manage Candidate-owned persisted avatars. | `screens/candidate/personal-avatar-studio.png` | `TO DESIGN` |
| `CAN-05-SUB1` | `DRAW` | Personal 3D Avatar / Avaturn Embedded Experience | Candidate | Within avatar studio | Host the free Avaturn experience for its owned creation steps. | `screens/candidate/avaturn-embedded-experience.png` | `TO DESIGN` |
| `CAN-05-SUB2` | `DOC-ONLY` | Personal 3D Avatar / Personal Avatar Confirmation & Preview | Candidate | Post-Avaturn handoff | Confirm a successfully converted, Candidate-owned VRM avatar. | `screens/candidate/personal-avatar-confirmation.png` | `TO DESIGN` |
| `CAN-06` | `DRAW` | Interview Configuration / Configure Interview Session | Candidate | Candidate interview setup | Configure available interviewer, Voice Profile, environment, difficulty, and duration/question budget in one composite experience. | `screens/candidate/configure-interview-session.png` | `TO DESIGN` |
| `CAN-07` | `DRAW` | Interview Simulation / Test Audio & Interview Readiness | Candidate | `/interviews/new/preflight` | Verify microphone, audio, and rendering readiness before the runtime. | `screens/candidate/preflight-ready.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `CAN-07-SUB1` | `DOC-ONLY` | Interview Simulation / Readiness Device Error Dialog | Candidate | Within readiness | Give recovery guidance for microphone, permission, or device failure. | `screens/candidate/preflight-permission-required.png` | `EXISTING / NEEDS CONTENT SYNC` |
| `CAN-08` | `DRAW` | Interview Runtime / Live 3D Interview Room | Candidate | `/interviews/[id]/room` | Conduct the real-time spoken interview using the generic Question loop. | `screens/candidate/live-3d-interview-room.png` | `TO DESIGN` |
| `CAN-08-SUB1` | `DRAW` | Interview Runtime / Interview Session Pause / Exit Modal | Candidate | Within live room | Pause, resume, or explicitly end an active session. | `screens/candidate/interview-pause-exit-modal.png` | `TO DESIGN` |
| `CAN-08-SUB2` | `DOC-ONLY` | Interview Runtime / 2D Waveform Fallback View | Candidate | Within live room | Continue spoken interaction when 3D/WebGL is unavailable. | `screens/candidate/interview-2d-waveform-fallback.png` | `TO DESIGN` |
| `CAN-09` | `DRAW` | Evaluation / Interview Performance Report | Candidate | `/reports/[id]` | Review stored scores, feedback, and learning roadmap. | `screens/candidate/interview-performance-report.png` | `TO DESIGN` |
| `CAN-09-SUB1` | `DOC-ONLY` | Evaluation / Turn Critiques & Model Answers | Candidate | Within performance report | Inspect turn-level critique and benchmark guidance. | `screens/candidate/turn-critiques-model-answers.png` | `TO DESIGN` |
| `CAN-09-SUB2` | `DOC-ONLY` | Evaluation / Actionable Learning Roadmap | Candidate | Within performance report | Review prioritized learning recommendations and practice actions. | `screens/candidate/actionable-learning-roadmap.png` | `TO DESIGN` |
| `CAN-09-SUB3` | `DRAW` | Evaluation / Export Report Dialog | Candidate | Within performance report | Select an export and download a stored report. | `screens/candidate/export-report-dialog.png` | `TO DESIGN` |
| `CAN-10` | `DRAW` | History / Interview History | Candidate | `/history` | Browse previous interview sessions and reopen reports. | `screens/candidate/interview-history.png` | `TO DESIGN` |
| `CAN-11` | `DRAW` | Job Board / Job Board (Browse Postings) | Candidate | Candidate job board | Search and filter approved Recruiter Job Postings. | `screens/candidate/job-board.png` | `TO DESIGN` |
| `CAN-12` | `DRAW` | Job Board / Job Posting Detail | Candidate | Selected approved Job Posting | Inspect requirements, company-defined interviewer/voice, and application entry. | `screens/candidate/job-posting-detail.png` | `TO DESIGN` |
| `CAN-13` | `DRAW` | Applications / Job Application & CV Upload | Candidate | Approved Job Posting application | Provide application information and CV before the required locked interview. | `screens/candidate/job-application-cv-upload.png` | `TO DESIGN` |
| `CAN-13-SUB1` | `DOC-ONLY` | Applications / Application Submitted Confirmation | Candidate | After completed application | Confirm CV and Interview Result submission to the Recruiter. | `screens/candidate/application-submitted-confirmation.png` | `TO DESIGN` |
| `CAN-14` | `DRAW` | Applications / My Applications Tracking | Candidate | Candidate applications | Track pending, approved, or rejected submitted applications. | `screens/candidate/my-applications-tracking.png` | `TO DESIGN` |
| `CAN-14-SUB1` | `DOC-ONLY` | Applications / Application Dossier & Result Viewer | Candidate | Within application tracking | View own submitted details and the attached Interview Result. | `screens/candidate/application-dossier-result-viewer.png` | `TO DESIGN` |
| `CAN-15` | `DRAW` | Membership / Membership & Billing | Candidate | `/billing` | View membership status, renewal, and available subscription options. | `screens/candidate/membership-billing.png` | `TO DESIGN` |
| `CAN-15-SUB1` | `DOC-ONLY` | Membership / Payment Gateway Checkout Redirect | Candidate | Membership checkout | Hand off checkout to the external payment gateway. | `screens/candidate/payment-gateway-checkout-redirect.png` | `TO DESIGN` |
| `CAN-15-SUB2` | `DRAW` | Membership / Unsubscribe Confirmation Dialog | Candidate | Within membership | Confirm cancellation of recurring membership renewal. | `screens/candidate/unsubscribe-confirmation-dialog.png` | `TO DESIGN` |
| `CAN-15-SUB3` | `DOC-ONLY` | Membership / Payment Transaction History | Candidate | Within membership | View own membership-payment transaction history. | `screens/candidate/payment-transaction-history.png` | `TO DESIGN` |
| `REC-01` | `DRAW` | Recruiter Workspace / Recruiter Dashboard | Recruiter | Recruiter workspace | View own posting/application summary and primary actions. | `screens/recruiter/recruiter-dashboard.png` | `TO DESIGN` |
| `REC-02` | `DRAW` | Job Posting Management / My Job Postings Management | Recruiter | Recruiter Job Postings | Search and manage own postings across their allowed statuses. | `screens/recruiter/my-job-postings-management.png` | `TO DESIGN` |
| `REC-02-SUB1` | `DOC-ONLY` | Job Posting Management / Archive Job Posting Dialog | Recruiter | Within own postings | Confirm archival of an inactive or filled own posting. | `screens/recruiter/archive-job-posting-dialog.png` | `TO DESIGN` |
| `REC-03` | `DRAW` | Job Posting Management / Create Job Posting | Recruiter | Recruiter Job Postings | Draft a Job Posting from JD-like content and prepare it for approval. | `screens/recruiter/create-job-posting.png` | `TO DESIGN` |
| `REC-03-SUB1` | `DOC-ONLY` | Job Posting Management / AI Extraction Review & Confirmation | Recruiter | Within create posting | Review and confirm extracted technical information before submission. | `screens/recruiter/job-posting-ai-extraction-review.png` | `TO DESIGN` |
| `REC-03-SUB2` | `DOC-ONLY` | Job Posting Management / Configure Company 3D Interviewer & Voice | Recruiter | Within create posting | Select the company interviewer model and Voice Profile required for applicants. | `screens/recruiter/configure-company-interviewer-voice.png` | `TO DESIGN` |
| `REC-04` | `DRAW` | Job Posting Management / Edit Job Posting | Recruiter | Own Job Posting | Update an own Job Posting's requirements or metadata. | `screens/recruiter/edit-job-posting.png` | `TO DESIGN` |
| `REC-05` | `DRAW` | Application Review / Received Applications List | Recruiter | Recruiter applications | Search and filter completed applications to own postings. | `screens/recruiter/received-applications-list.png` | `TO DESIGN` |
| `REC-06` | `DRAW` | Application Review / Application Detail & Review | Recruiter | Selected own-posting application | Inspect candidate information, CV, and attached Interview Result. | `screens/recruiter/application-detail-review.png` | `TO DESIGN` |
| `REC-06-SUB1` | `DRAW` | Application Review / Attached Interview Result Viewer | Recruiter | Within application detail | Inspect attached Performance Report and session transcript. | `screens/recruiter/attached-interview-result-viewer.png` | `TO DESIGN` |
| `REC-06-SUB2` | `DOC-ONLY` | Application Review / Application Adjudication Dialog | Recruiter | Within application detail | Record the final binary Approve or Reject decision. | `screens/recruiter/application-adjudication-dialog.png` | `TO DESIGN` |
| `ADM-01` | `DRAW` | Administration / Admin Governance Console | Administrator | `/admin` | Enter platform governance across permitted operations. | `screens/admin/admin-governance-console.png` | `TO DESIGN` |
| `ADM-02` | `DRAW` | Account Governance / Account Governance (User List) | Administrator | `/admin/users` | Search and inspect Candidate and Recruiter accounts. | `screens/admin/account-governance-user-list.png` | `TO DESIGN` |
| `ADM-03` | `DRAW` | Account Governance / Account Detail & Lock/Unlock | Administrator | Selected account | Inspect an account and lock or unlock it. | `screens/admin/account-detail-lock-unlock.png` | `TO DESIGN` |
| `ADM-04` | `DRAW` | Content Moderation / Job Posting Moderation Queue | Administrator | Admin Job Posting moderation | Review Recruiter postings awaiting publication moderation. | `screens/admin/job-posting-moderation-queue.png` | `TO DESIGN` |
| `ADM-05` | `DRAW` | Content Moderation / Job Posting Review & Approval | Administrator | Selected pending Job Posting | Inspect and approve or reject a submitted Job Posting. | `screens/admin/job-posting-review-approval.png` | `TO DESIGN` |
| `ADM-05-SUB1` | `DOC-ONLY` | Content Moderation / Moderation Decision Dialog | Administrator | Within Job Posting review | Record approval or rejection with the required reason note. | `screens/admin/moderation-decision-dialog.png` | `TO DESIGN` |
| `ADM-06` | `DRAW` | Session Oversight / Interview Sessions Oversight | Administrator | `/admin/interviews` | Search, filter, and monitor platform interview sessions. | `screens/admin/interview-sessions-oversight.png` | `TO DESIGN` |
| `ADM-07` | `DRAW` | Session Oversight / Interview Session Detail | Administrator | Selected interview session | Inspect operational session metadata and error flags. | `screens/admin/interview-session-detail.png` | `TO DESIGN` |
| `ADM-08` | `DRAW` | Configuration / Interview Feature Configuration | Administrator | Admin interview configuration | Configure permitted platform-wide interview parameters and toggles. | `screens/admin/interview-feature-configuration.png` | `TO DESIGN` |
| `ADM-09` | `DRAW` | AI Calibration / AI Behaviour Management | Administrator | Admin AI configuration | Manage system prompt templates and generic Question guidance. | `screens/admin/ai-behaviour-management.png` | `TO DESIGN` |
| `ADM-09-SUB1` | `DOC-ONLY` | AI Calibration / Prompt Template Editor Drawer | Administrator | Within AI behaviour management | Edit a conversational system prompt template. | `screens/admin/prompt-template-editor-drawer.png` | `TO DESIGN` |
| `ADM-10` | `DRAW` | AI Calibration / Evaluation Criteria Calibration | Administrator | Admin evaluation configuration | Calibrate evaluation criteria, rubric templates, and weights. | `screens/admin/evaluation-criteria-calibration.png` | `TO DESIGN` |
| `ADM-10-SUB1` | `DOC-ONLY` | AI Calibration / Rubric Template Editor Drawer | Administrator | Within evaluation calibration | Edit a technical rubric template and scoring weights. | `screens/admin/rubric-template-editor-drawer.png` | `TO DESIGN` |
| `ADM-11` | `DRAW` | Voice Management / Voice Profile Catalog | Administrator | `/admin/voices` | Curate supported provider-sourced TTS Voice Profiles. | `screens/admin/voice-profile-catalog.png` | `TO DESIGN` |
| `ADM-11-SUB1` | `DOC-ONLY` | Voice Management / Delete Voice Profile Dialog | Administrator | Within Voice Profile Catalog | Confirm deactivation or deletion of an obsolete profile. | `screens/admin/delete-voice-profile-dialog.png` | `TO DESIGN` |
| `ADM-12` | `DRAW` | Voice Management / Fetch Voice Profiles Modal | Administrator | Within Voice Profile Catalog | Fetch supported profiles from TTS providers for curation. | `screens/admin/fetch-voice-profiles-modal.png` | `TO DESIGN` |
| `ADM-13` | `DRAW` | Financial Governance / Payment Transactions Ledger | Administrator | `/admin/billing` | Inspect recorded Candidate membership payment transactions. | `screens/admin/payment-transactions-ledger.png` | `TO DESIGN` |
| `ADM-14` | `DRAW` | Financial Governance / Revenue Report Generator | Administrator | Admin financial governance | Generate aggregate membership-revenue reports. | `screens/admin/revenue-report-generator.png` | `TO DESIGN` |
| `ADM-15` | `DRAW` | Financial Governance / Update Membership Price Modal | Administrator | Admin financial governance | Update the active Candidate membership price. | `screens/admin/update-membership-price-modal.png` | `TO DESIGN` |

## Preserved visual artifacts that remain semantically compatible

The 19 paths below support retained current screens. The two candidate-shell references remain useful visual scaffolding but are not an extra canonical screen. None are modified by this pass.

| Current contract mapping | Preserved compatible artifact(s) | Treatment |
|---|---|---|
| `PUB-01` | `screens/shared/marketing/landing-desktop-1440.png`, `screens/shared/marketing/landing-mobile-390.png` | Existing target/viewport variant; content sync later. |
| `AUTH-01` | `screens/shared/auth/register-desktop.png`, `screens/shared/auth/register-mobile.png` | Existing target/viewport variant; content sync later. |
| `AUTH-01-SUB1` | `screens/shared/auth/verify-email.png`, `screens/shared/auth/email-verified.png` | Existing verification-journey states; content sync later. |
| `AUTH-02` | `screens/shared/auth/login-desktop.png`, `screens/shared/auth/login-mobile.png` | Existing target/viewport variant; content sync later. |
| `AUTH-03` | `screens/shared/auth/forgot-password.png` | Existing target; content sync later. |
| `AUTH-04` | `screens/shared/auth/reset-password.png` | Existing target; content sync later. |
| `CAN-01` | `screens/candidate/dashboard.png`, `screens/candidate/dashboard-empty-new-user.png`, `screens/candidate/dashboard-returning-user.png` | Existing dashboard and compatible state variants; content sync later. |
| `CAN-02` | `screens/candidate/jd-empty-state.png` | Existing compatible library-empty state; content sync later. |
| `CAN-03` | `screens/candidate/jd-add-job-description.png` | Existing target; content sync later. |
| `CAN-04` | `screens/candidate/jd-review-and-edit-skills.png` | Existing target; content sync later to include refinement-note semantics. |
| `CAN-07` | `screens/candidate/preflight-ready.png` | Existing target; content sync later. |
| `CAN-07-SUB1` | `screens/candidate/preflight-permission-required.png`, `screens/candidate/preflight-failed-check.png` | Existing compatible error variants; content sync later. |
| Workspace visual scaffolding, not an additional screen ID | `screens/candidate/shell-desktop-1440.png`, `screens/candidate/shell-laptop-1280.png` | Retained visual references for the Candidate workspace shell. |

## Historical / stale artifacts kept for provenance

These 14 preserved artifacts are not current design targets and are excluded from the 70-screen count.

| Preserved artifact | Why it is historical / stale |
|---|---|
| `screens/shared/marketing/pricing-desktop.png` | Public pricing and credit-package scope are removed. |
| `screens/shared/marketing/pricing-mobile.png` | Public pricing and credit-package scope are removed. |
| `screens/candidate/jd-analyzing.png` | AI extraction processing is not a retained standalone screen. |
| `screens/candidate/jd-analysis-result.png` | Replaced by the retained Candidate review/refinement contract; not a standalone screen. |
| `screens/candidate/setup-general.png` | Former fragmented setup; superseded by composite `CAN-06` Configure Interview Session. |
| `screens/candidate/setup-interviewer.png` | Former fragmented setup; superseded by composite `CAN-06` Configure Interview Session. |
| `screens/candidate/setup-voice.png` | Former fragmented setup; superseded by composite `CAN-06` Configure Interview Session. |
| `screens/candidate/setup-credits-gate.png` | Credit-gate model is removed. |
| `screens/candidate/blueprint-generation.png` | Blueprint generation is internal/non-screen. |
| `screens/candidate/blueprint-preview-confirmation.png` | Candidates never view, edit, or confirm a Blueprint. |
| `screens/candidate/preflight-checking.png` | Readiness processing is not a retained standalone screen. |
| `flows/00-system-overview.png` | Shows former Candidate/Admin-only topology and stale credits/admin domains. |
| `flows/01-candidate-flow.png` | Shows exposed Blueprint generation/preview. |
| `flows/02-admin-flow.png` | Shows obsolete avatar-related administration and lacks current moderation/recruiter topology. |

## Explicit non-screen and removed boundaries

- **Non-screen:** raw JD normalization, AI extraction orchestration, internal Interview Blueprint generation, GLB-to-VRM conversion/persistence, payment callbacks, generic Question selection, evaluation processing, and abandoned-session cleanup.
- **Removed from canonical UX:** Candidate Blueprint Builder/Preview/Confirmation; credit wallet, credit packs, credit gates, and public pricing; Administrator 3D Avatar Catalog and Interview Background/Environment Catalog; separate Corporate JD; organizations/tenants; full ATS workflows.
