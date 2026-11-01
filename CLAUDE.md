# CLAUDE.md — foodDeliverychefAtHome

Food Delivery & Chef-at-Home platform built from **BRD-FD-001 v1.0** (`docs/brd/`).
Two services, one kit model: **Food Order** (hub cooks, rider delivers) and **Food with Chef**
(chef brings sealed kits and cooks at the customer's home).

## Start of every session
1. Read `docs/PROGRESS.md` (where we are, what's next) and `docs/DECISIONS.md` (decisions already made).
2. For the task at hand, read only the relevant BRD section via `docs/brd/README.md`. Do not load the whole BRD.
3. Plan before editing anything that touches more than one file. Wait for approval of the plan.

## Stack (decided — do not swap without an entry in docs/DECISIONS.md)
- Monorepo: **pnpm workspaces + Turborepo**, TypeScript `strict` everywhere.
- `apps/api` — **NestJS** REST API, **Prisma** + **PostgreSQL 16 with PostGIS**, **Redis + BullMQ** for jobs.
- `apps/dashboard` — **React + Vite + TanStack Query/Router** (hub manager, support, finance, super admin).
- `apps/customer` — **Expo (React Native)** Customer app.
- `apps/partner` — **Expo (React Native)** Partner app (chef and rider screens by approved role).
- `packages/shared` — Zod schemas, enums, order/booking state machines, money & time helpers. Used by all apps.
- `packages/config` — shared tsconfig / ESLint / Prettier.
- Local infra: `docker compose up -d` (Postgres+PostGIS on 5432, test DB on 5433, Redis on 6379).

## Commands (keep this list current)
- `pnpm install` · `pnpm dev` · `pnpm build`
- `pnpm lint` · `pnpm typecheck` · `pnpm test` · `pnpm test:integration` (needs Docker)
- `pnpm --filter api prisma migrate dev --name <change>` · `pnpm --filter api prisma studio`

## Definition of done (every task)
- `pnpm lint && pnpm typecheck && pnpm test` pass. Never say "done" without running them and showing the result.
- Business rules have tests named after their IDs, e.g. `it('BR-007 price snapshot: later price change does not alter order')`.
- `docs/PROGRESS.md` updated (what changed, what's next, any open issue).
- New decisions recorded in `docs/DECISIONS.md`.
- Suggest a Conventional Commit message (`feat(api): …`, `fix(partner): …`). The human commits.

## Hard rules — never break these
1. **Never hardcode a business value that the BRD marks configurable or open (OD-xx).** Minimum order,
   fees, hold time, slot length, buffers, cancellation cut-offs, OTP length, feature flags etc. come from the
   layered settings service (platform → city → hub, BRD §4.3). Seeds may hold placeholder defaults.
2. **Hold before payment.** Kits (and chef time) are held when the customer proceeds to pay; the order is
   confirmed only after the gateway verifies payment; unpaid holds expire automatically (BR-005, FR-OPS-009).
3. **No overselling, no double-booking — enforced in the database**, not only in code:
   kit holds use atomic conditional updates inside a transaction; chef time uses a Postgres exclusion
   constraint on a `tstzrange` (btree_gist). Concurrency tests (UAT-08) must exist for both.
4. **Idempotency.** Payment creation and gateway webhooks use idempotency keys / event-ID dedupe.
   A retry must never create a second order or charge (FR-OPS-003, UAT-09). Verify webhook signatures.
5. **Money is integer paise** (`amountPaise: number`), never floats. Format only in the UI.
6. **Time is stored as UTC `timestamptz`**, displayed in `Asia/Kolkata`. Never use local server time.
7. **Price snapshot.** Order lines copy price, fees and tax at confirmation; invoices read the snapshot (BR-007).
8. **Explicit state machines** (in `packages/shared`). Order/booking status and payment/refund status are
   separate fields (FR-OPS-004). Invalid transitions throw. Every transition writes a timestamped history row.
9. **Access control.** Every query for hub data is scoped to the user's hubs. Partners see only assigned jobs;
   customer address/phone visible to partners only during the active job (BRD §5).
10. **Audit log** for changes to prices, menus, stock, zones, policies, refunds, partner approvals and roles (BR-019).
11. **Every third-party service sits behind an interface with a Fake implementation** used in dev and tests:
    payments, OTP/SMS, maps/geocoding, push, WhatsApp, masked calling, delivery company. Providers are not chosen
    yet (OD-08, BRD §16) — never import a vendor SDK outside its adapter folder.
12. **Secrets** live only in `.env` (git-ignored). Update `.env.example` when adding a variable. Never print secrets.
13. **Migrations:** create a new Prisma migration for every schema change. Never edit or delete a migration that
    is already committed. Never run `prisma migrate reset` or drop data without asking.
14. **Scope:** anything not in the BRD is a change request (§19). Out of scope (§17.3): marketplace, payouts,
    supplier portals, subscriptions, loyalty, multi-drop routing, IoT/POS. Ask before adding features.
15. Use the BRD glossary terms in code: Hub, Kit, Dish, ServiceZone, Order (Food Order), Booking (Food with Chef),
    Slot, Hold, Assignment, Exception, VisitOtp, Partner.

## Conventions
- API modules mirror domains: `auth`, `users`, `geo` (cities/hubs/zones), `settings`, `catalogue`, `inventory`,
  `holds`, `orders`, `bookings`, `scheduling`, `dispatch`, `payments`, `refunds`, `invoices`, `notifications`,
  `support`, `audit`, `reports`.
- Validate all input with Zod schemas from `packages/shared`; the same schema types the mobile/web clients.
- Controllers stay thin; logic lives in services; DB access via Prisma (PostGIS queries in one `geo` repository using `$queryRaw`).
- Errors: typed domain errors mapped to HTTP codes; user-facing messages in plain words (FR-CUS-008).
- Tests: unit tests next to the code (`*.spec.ts`); integration tests hit the real test DB from Docker.
- Keep files under ~300 lines; split when larger. No `any` without a comment explaining why.
- Windows dev machine: keep LF line endings (`.gitattributes`), use cross-platform npm scripts (no bash-only syntax).

## When unsure
Check `docs/DECISIONS.md`, then the BRD section. If still unclear, ask one specific question —
don't guess on money, holds, permissions, or anything listed in BRD §20.
