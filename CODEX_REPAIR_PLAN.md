# Codex recovery plan (review-only)

This is a PUBLIC repository for the independent AI Empire product, **not** the Foundation/MONAD production codebase. Do not copy private Foundation source, user records, keys, or credentials here. The changes in this branch are documentation only and are NOT deployed.

## Priority and actual findings

P0 — Namecheap production cron points to missing `scripts/run-monad-grant-cycle.sh` in the production source. Confirm exact current cron command, working directory, log permissions, cron execution receipts, and actual scheduler implementation; restore via tested replacement after full source backup and isolated staging test. The backup script `scripts/db-backup.sh` exists, but no scheduled verified backup or isolated restore proof has been established. Avoid running retention-based deletion until recovery copies and checksums are secured.

P0 — MONAD diagnostics recorded two failed probes, identities unverified. Extract individual failures from the true health records; account for missing daily run since October 14 without conflating distinct schedulers. Developer repair adapter is not connected: treat its controls as proposals, never autonomous execution.

P0 — Deploy fail-closed private MONAD policy enforcement (Prime Directive v2.1) within authenticated private server tool dispatchers, with explicit per-action approval, audit and rollback receipts. Maintain separation between consumer AI Empire entitlements and internal Foundation tools.

P1 — Foundation `api/health` currently checks `SMTP_HOST` and `SMTP_USER` but labels it simply `email`; this is not Gmail OAuth status. Clarify as `smtp_configuration` while preserving backward-compatible documented fields, and report Gmail read/draft/send health separately only through authenticated internal checks.

P1 — Public `/ai-empire` route is missing in Foundation source. Add an audited public redirect to the independently hosted AI Empire landing after confirming approved URL and public menu. Test product inventory, donations, checkout and digital-download fulfillment in sandbox. Stripe restricted-key balance 403 does not establish payment-processing failure.

P1 — Reconcile two Gmail account OAuth reads versus untested sending; ensure explicit approved outbound sends and idempotent receipts. Verify application intake, PHA openings, grants, and vendor workflows with timestamped evidence.

P2 — Accessibility, mobile experience, controlled media learning, avatar, scanner and Habitat Halo inventor materials; preserve confidential design information.

## Codex execution gates
1. Use the real private production repository and exact deployed release, not this public placeholder.
2. Record immutable source checksum, safe database backup and isolated restore test.
3. Build and run unit/integration tests; verify outbound transactions only in sandbox.
4. Stage patches and review diff; validate source, infrastructure and user authorization.
5. Deploy only from the verified current source with rollback; retain deployment receipts.
6. Final report must separate VERIFIED / IMPLEMENTED ONLY / BLOCKED / DEPLOYED.

Owner's Abacus credits are exhausted: do not introduce a paid Abacus execution dependency. No secrets or infrastructure auth material belong in this public repository.