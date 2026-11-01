# BRD index — read only the section you need

Source of truth: `BRD-FD-001.pdf` (v1.0, 28 Oct 2026). Each section is also split into its own
markdown file so Claude can load just the part a task needs instead of the whole document.

| Section | File | Read it when working on |
|---|---|---|
| 1 Executive summary | `01-executive-summary.md` | Orientation only |
| 2 Objectives & measures | `02-objectives-and-success-measures.md` | Reports, KPIs |
| 3 Glossary | `03-glossary.md` | Naming entities and fields (use these exact terms in code) |
| 4 Business model & scope | `04-business-model-and-scope.md` | Hubs, **config layering (4.3)** |
| 5 Stakeholders & roles | `05-stakeholders-and-roles.md` | Auth, RBAC, access limits |
| 6 End-to-end journeys | `06-end-to-end-service-journeys.md` | Checkout, holds, **exceptions (6.3)** |
| 7 Order & booking lifecycle | `07-order-and-booking-lifecycle.md` | State machines |
| 8 Functional requirements | `08-functional-requirements.md` | Any feature (FR-CUS / PTR / CHF / RID / HUB / ADM / OPS) |
| 9 Business rules | `09-business-rules-and-operating-policies.md` | Rules BR-001 … BR-019 |
| 10 Notifications | `10-notifications.md` | Notification events and channels |
| 11 Trust & food safety | `11-trust-safety-and-food-safety.md` | Visit OTP, SOS, kit sealing, cold chain |
| 12 Data & catalogue | `12-data-and-catalogue-management.md` | Prisma schema, entities |
| 13 Reporting & controls | `13-reporting-and-operational-controls.md` | Reports, second approvals |
| 14 Non-functional reqs | `14-non-functional-requirements.md` | Performance, security, backups |
| 15 Compliance (India) | `15-compliance-considerations-india.md` | GST, FSSAI, DPDP Act, DLT SMS |
| 16 External dependencies | `16-external-services-and-dependencies.md` | Adapters (payments, SMS, maps…) |
| 17 Assumptions & scope | `17-assumptions-constraints-and-out-of-scope.md` | Before adding anything "extra" |
| 18 Acceptance & UAT | `18-acceptance-criteria-and-uat-scenarios.md` | Writing tests (UAT-01 … UAT-19) |
| 19 Milestones | `19-milestones-pilot-launch-and-change-contr.md` | Planning |
| 20 Open decisions | `20-open-questions-and-decisions.md` | OD-01 … OD-24 (see `docs/DECISIONS.md`) |
| 21 Risks | `21-key-risks-and-mitigations.md` | — |
| 22 Sign-off | `22-approval-and-sign-off.md` | — |

## Build phases → requirements → UAT gates

| Phase | Covers | Main requirement IDs | Gate (must pass) |
|---|---|---|---|
| P0 Foundation | Monorepo, Docker, CI, auth skeleton | NFR-005, NFR-008 groundwork | Lint, typecheck, tests green in CI |
| P1 Core ops (BRD M3) | Cities, hubs, zones, settings, catalogue, kits, daily kit plan, stock, roles, partner onboarding, audit | FR-ADM-001…012, FR-HUB-007…010, BR-003, BR-019 | UAT-01, UAT-07, UAT-08 (kits) |
| P2 Food Order (BRD M4) | Serviceability, cart, pricing, holds, payments, invoices, notifications, kitchen queue, rider screens | FR-CUS-001…013/016/020, FR-OPS-001…010, FR-HUB-001…005, FR-RID-*, BR-001/002/005/006/007 | UAT-02, 09, 10, 16 |
| P3 Chef at home (BRD M5) | Slots, chef holds, kit packing, visit OTP, SOS, chef screens | FR-CUS-009/014/015, FR-CHF-*, FR-PTR-*, FR-HUB-004/006/012, BR-008/009/013/014/015 | UAT-03, 04, 13, 14, 08 (chef) |
| P4 Hardening & pilot (BRD M6) | Full UAT, security, load, restore drill, store builds | NFR-001…013, remaining Should items | UAT-01…19 all pass |
