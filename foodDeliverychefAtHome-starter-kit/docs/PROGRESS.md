# Progress

Claude updates this file at the end of every task (via `/finish-task`). Keep it short: the newest entry on top,
older entries trimmed to one line each once a phase is finished.

## Current phase
**P0 — Foundation** (see `docs/brd/README.md` for phases and gates)

## Next up
- [ ] P0.1 Scaffold monorepo: pnpm workspaces, Turborepo, `packages/config`, `packages/shared`, root scripts
- [ ] P0.2 `apps/api` NestJS skeleton + Prisma connected to Docker Postgres + health endpoint + first test
- [ ] P0.3 Testing setup: unit tests, integration tests against the test DB (port 5433)
- [ ] P0.4 GitHub Actions CI: install, lint, typecheck, test (with Postgres/Redis service containers)
- [ ] P0.5 Settings service (platform → city → hub layering, BRD §4.3) with tests
- [ ] P0.6 Audit log module + auth skeleton (mobile OTP via `FakeOtpSender`, roles from BRD §5)
- [ ] P0.7 `apps/dashboard`, `apps/customer`, `apps/partner` empty shells that call the health endpoint

## Phase checklist
- [ ] P0 Foundation
- [ ] P1 Core ops — gate: UAT-01, UAT-07, UAT-08 (kits)
- [ ] P2 Food Order — gate: UAT-02, 09, 10, 16
- [ ] P3 Chef at home — gate: UAT-03, 04, 13, 14, 08 (chef)
- [ ] P4 Hardening & pilot — gate: UAT-01…19

## Log
<!-- newest first. Format:
### YYYY-MM-DD — <task>
- Done: …
- Tests: lint ✅ typecheck ✅ test ✅ (n passing)
- Next: …
- Open issues: …
-->

### 2026-11-01 — Project setup
- Done: repo created, starter kit added (CLAUDE.md, docs/brd, DECISIONS, PROGRESS, docker-compose).
- Next: P0.1.
