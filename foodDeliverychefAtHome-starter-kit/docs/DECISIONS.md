# Decisions log

Two parts: **(A) technical decisions** we made, and **(B) client decisions** from BRD §20 (OD-01 … OD-24).
Claude reads this file at the start of every session. Add a row whenever something is decided — never delete
old rows; mark them superseded instead.

## A. Technical decisions (ADR-lite)

| # | Date | Decision | Why | Status |
|---|---|---|---|---|
| T-01 | 2026-11-01 | TypeScript monorepo: pnpm workspaces + Turborepo | One language and shared types across API, dashboard and both apps | Accepted |
| T-02 | 2026-11-01 | NestJS + Prisma + PostgreSQL 16/PostGIS + Redis/BullMQ | Modular domains; strong transactions for holds; PostGIS for service zones; delayed jobs for hold expiry | Accepted |
| T-03 | 2026-11-01 | Expo (React Native) for Customer and Partner apps; EAS for store builds | One codebase per app for Android + iOS; iOS builds from Windows via EAS cloud | Accepted |
| T-04 | 2026-11-01 | React + Vite dashboard | Internal tool; no SEO needs; simple SPA calling the API | Accepted |
| T-05 | 2026-11-01 | Kit holds = atomic conditional UPDATE in a transaction; chef time = exclusion constraint on tstzrange | Database guarantees no overselling / double-booking (UAT-08) | Accepted |
| T-06 | 2026-11-01 | All vendors behind adapters with Fake implementations | Providers undecided (OD-08, §16); lets us build and test now | Accepted |
| T-07 | 2026-11-01 | Money in integer paise; timestamps UTC, shown in Asia/Kolkata | Avoid rounding and timezone bugs | Accepted |

## B. Client decisions (BRD §20)

"Working default" = placeholder we build against until the client decides. Every working default must be a
setting (platform/city/hub), never a constant, so the real answer is a config change, not a code change.

| ID | Decision | Working default (until client confirms) | Client answer | Date |
|---|---|---|---|---|
| OD-01 | Minimum-order rule | Rule type is a setting (`GUESTS`, `VALUE`, `EITHER`, `BOTH`); default `EITHER`: 2 guests or ₹1,200 | — | — |
| OD-02 | Launch city and first hubs | One seeded test city + one hub | — | — |
| OD-03 | Chef visit fee and length | Fee model is a setting; default flat fee per booking; length from dishes + guests | — | — |
| OD-04 | Chef booking rules | Next-day only, 24h notice, 30-min travel buffer (all settings) | — | — |
| OD-05 | Cancellation, no-show, refunds | Policy matrix table by service × stage; seeded with sample values | — | — |
| OD-06 | Rider model | In-house riders on Partner app; `DeliveryCompany` adapter interface stubbed | — | — |
| OD-07 | Zones and tie-breaker | Support radius, polygon and postal codes; tie-breaker setting, default `NEAREST` | — | — |
| OD-08 | Payment gateway | `FakePaymentGateway` with success/failure/late-webhook modes | — | — |
| OD-09 | What customer provides at home | Editable checklist text per city | — | — |
| OD-10 | After the visit | Editable policy text | — | — |
| OD-11 | Substitutions | Disabled; any substitution requires customer consent | — | — |
| OD-12 | Partner verification | Admin records verification status + date manually | — | — |
| OD-13 | Scheduled Food Orders | ASAP only (FR-CUS-024 is a Should) | — | — |
| OD-14 | Large and event bookings | Max guests per chef as a setting | — | — |
| OD-15 | Pricing and tax display | Prices shown excluding tax, tax lines itemised | — | — |
| OD-16 | Languages and support | English only; i18n keys from day one | — | — |
| OD-17 | Target volumes | Load-test target to be set | — | — |
| OD-18 | Permissions and approval limits | Refund approval limit as a setting | — | — |
| OD-19 | Account ownership | Client-owned (per §16) | — | — |
| OD-20 | Post-launch support | — | — | — |
| OD-21 | Brand and app names | Placeholder names | — | — |
| OD-22 | Visit OTP and delivery proof | OTP length setting, default 4; lock after 5 wrong tries; delivery proof = OTP | — | — |
| OD-23 | Checkout hold time | 10 minutes (setting) | — | — |
| OD-24 | Partners with both roles | Partner has a `roles` array; allowing both is a setting | — | — |
