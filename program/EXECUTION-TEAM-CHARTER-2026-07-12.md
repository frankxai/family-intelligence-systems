# Family Intelligence System — Specialist Execution Charter

Status: staged for dispatch; machine admission currently holds new swarms.

This charter turns the Family Intelligence System foundation into bounded, independently-verifiable work. It does not authorize production access, real family-data ingestion, external outreach, DNS, secrets, spend, legal conclusions, or destructive Git history changes.

## Operating model

The program uses a conductor model: the Family Intelligence Lead integrates decisions and owns cross-repository sequencing; each delivery lane has one writer at a time and an independent verifier. A worker never verifies its own release-affecting output.

| Lane | Primary repository | Team | Sequence |
| --- | --- | --- | --- |
| Governance and safety kernel | `family-intelligence-systems` | coordinator, family-systems architect, Guardian/security reviewer, test/verifier | First |
| Secure runtime and steward workflow | `family-intelligence-os` | coordinator, backend-data engineer, AI-evaluation engineer, security/privacy reviewer, QA/SRE verifier | Second |
| FrankX privacy containment | `frankx.ai-vercel-website` | coordinator, frontend engineer, security/privacy reviewer, QA/SRE verifier | Before public release |
| FrankX public experience | `frankx.ai-vercel-website` | coordinator, frontend engineer, UX/design specialist, QA/SRE verifier | After containment |
| Pilot onboarding and continuity | `family-intelligence-os` plus private local seed | coordinator, backend-data engineer, Guardian, QA/SRE verifier | Only after identity and storage gates |

The runtime team was selected from the Starlight Platform profile for `api`, `security`, and `ai-engineering`; it resolves to coordinator, backend-data engineer, AI-evaluation engineer, security/privacy reviewer, and independent QA/SRE verifier. The FrankX work splits privacy and design into separate lanes to prevent overlapping writers and to preserve independent review.

## Work orders

### FIS-01 — Governance, consent, and threat-model completion

- Owner: family-systems architect.
- Reviewer: Guardian/security reviewer, then independent test/verifier.
- Write scope: `canon/**`, `protocols/**`, `schemas/**`, `threat-models/**`, `agents/**`, `skills/**`, `templates/**`.
- Deliver: DPIA-ready data map, living-person and child-data boundary tests, explicit source-grade matrix, consent revocation flow, dispute escalation policy, German steward guidance, and an approved-schema changelog.
- Done condition: every state transition is attributable, auditable, consent-aware, export-aware, and denies unsafe publication by default.
- Stop condition: legal determination, real-person evidence, genetic/health data, public naming, or trademark decision.

### FIO-01 — Tenant identity and authorization kernel

- Owner: backend-data engineer.
- Reviewer: security/privacy reviewer, then QA/SRE verifier.
- Write scope: runtime authentication, tenant/family scope, server authorization, RLS policies, audit-event writer, and tests; never the public demo data set.
- Deliver: passkey-ready account abstraction, invitation and recovery design, self/household/core/extended/guardian/advisor role matrix, server-side authorization in all handlers, and tenant-isolation tests.
- Done condition: no route, server action, MCP handler, or export operation relies on proxy-only authorization; cross-tenant access fails mechanically.
- Stop condition: provider credentials, production identity configuration, real account migration, or permissions that affect live users.

### FIO-02 — Secure intake, evidence quarantine, and steward queue

- Owner: backend-data engineer with AI-evaluation engineer.
- Reviewer: Guardian/security reviewer, then QA/SRE verifier.
- Write scope: claim/evidence/consent packages, worker contracts, intake routes, policy tests, eval fixtures, and audit receipts.
- Deliver: one-time intake-token protocol, attachment type/size policy, malware-scan adapter boundary, provenance-preserving extraction, duplicate-candidate review, and human-only accept/dispute/reject/publication transitions.
- Done condition: an inbound submission can create a quarantined case but cannot create an accepted fact or public artifact.
- Stop condition: mailbox connection, object-storage credential, automated relationship inference, or use of real evidence.

### FX-01 — Privacy containment for legacy family routes

- Owner: frontend engineer.
- Reviewer: security/privacy reviewer, then independent QA/SRE verifier.
- Write scope: `app/familie/**`, `app/family/tree/**`, `lib/familie/**`, `scripts/check-family-private-boundary.mjs`, route metadata, robots/sitemap, and the privacy release gate.
- Deliver: server-side session enforcement, generic locked metadata, noindex/nocache protection, tests that reject public names in protected routes, and a rollback plan.
- Done condition: unauthenticated visitors cannot retrieve protected route content; search engines receive no discoverable private-tree surface.
- Stop condition: production merge, real family data migration, public Git history rewrite, or changes to external identity providers.

### FX-02 — German-first public explanation, starter kit, and visual quality

- Owner: frontend engineer and UX/design specialist, serialized through the coordinator.
- Reviewer: independent QA/SRE verifier.
- Write scope: `app/family/**`, `app/family-intelligence-system/**`, `app/familien-intelligenz-system/**`, `components/family-intelligence/**`, `public/downloads/family-intelligence-starter-kit/**`, and design evidence.
- Deliver: accessible bilingual public routes, public-safe download, Vercel template link, v0 prompt link, responsive visual evidence, reduced-motion treatment, and a 26/30+ design score.
- Done condition: public content explains the product without presenting family claims, child data, private contacts, or legal promises.
- Stop condition: social/email send, analytics tracking changes, paid asset/license decision, trademark/brand decision, or production promotion.

### FIO-03 — Private pilot, export restore, and continuity drill

- Owner: backend-data engineer.
- Reviewer: Guardian/security reviewer and independent QA/SRE verifier.
- Write scope: private tenant persistence, encrypted-export implementation, GEDCOM projection, continuity policy tests, and restore-drill evidence.
- Deliver: synthetic-family end-to-end pilot, encrypted export, restore procedure, guardian quorum simulation, and German steward onboarding.
- Done condition: a synthetic family can invite a member, submit a claim, receive steward review, export, and restore without any autonomous release.
- Stop condition: real family onboarding, emergency or death-trigger implementation against real users, retention/deletion execution, or legal/financial data.

## Dispatch order and gates

1. Complete and independently verify FIS-01 and FX-01.
2. Complete FIO-01, then FIO-02; do not connect real mailbox, storage, or identity providers.
3. Complete FX-02 only after visual QA admission is available and evidence reaches 26/30 or higher.
4. Complete FIO-03 with synthetic data and a restore drill.
5. Create a separate human approval packet for private-store migration, production promotion, DNS, inbound email, real-family invitations, and any history-purge proposal.

Every job must use its own branch/worktree, record a durable report, run the relevant fast local gates, open a draft PR, and obtain an independent verifier verdict before it can become ready. Queue jobs must include an integer priority, bounded `maxMinutes`, explicit done condition, evidence path, and no `allowDangerous` flag unless Frank grants that authority.

## Current resource guard

At charter creation, `pp preflight --workload swarm` returned HOLD: 3.6 GB free RAM versus 10 GB required, 30 active task runtimes versus an 8-runtime budget, and maintenance posture. The coordinator may prepare contracts and read-only review, but must not dispatch new workers, local builds, browser QA, or unattended loops until a fresh preflight allows the workload.

## Evidence and next handoff

- Program receipt: `program/WORK-ITEM-2026-07-12.md`
- Governance architecture: `canon/naming-and-domain-architecture.md`, `canon/family-circles-and-guardianship.md`, and `protocols/`
- Runtime implementation PR: `family-intelligence-os#1`
- Public experience and privacy containment PR: `frankx.ai-vercel-website#266`
- Release evidence must document test results, verifier verdict, preview URL, known gaps, and a rollback path.
