---
description: Verify, record progress and propose a commit for the current task
---

1. Run `pnpm lint`, `pnpm typecheck` and `pnpm test` (and `pnpm test:integration` if the database or holds,
   payments, scheduling or inventory changed). Show the results. If anything fails, fix it and run again.
2. Check the diff against the hard rules in `CLAUDE.md` (hardcoded business values, money as paise, UTC time,
   idempotency, hub scoping, audit log, migrations, secrets). Report anything that breaks a rule.
3. Update `docs/PROGRESS.md`: add a log entry (done, test results, next, open issues) and tick the task.
4. Add any new decision to `docs/DECISIONS.md`.
5. If commands, folders or conventions changed, update `CLAUDE.md` (keep it short).
6. Propose a Conventional Commit message. Do not commit or push — I will.
