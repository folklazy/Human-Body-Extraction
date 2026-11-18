# Standard operating procedure for Codex / external agents

## Permanent files

Every delivery repo should contain:
- `README.md`: purpose, navigation, status, sample outputs, links
- `AGENTS.md`: read-first rules, permissions, prohibited actions, reproducibility policy
- `docs/SCOPE.md`, `docs/ARCHITECTURE.md` or `docs/METHODOLOGY.md` as appropriate
- `docs/RESULTS.md` and `docs/EVIDENCE_INDEX.md` for empirical components
- `docs/DECISIONS.md` and `CHANGELOG.md`
- Code/tests/config/lockfile/manifests when verified

## Temporary files

`tasks/ACTIVE_TASK.md` should identify:
1. objective and scope;
2. current audited source location/commit;
3. source files allowed to inspect and outputs to create;
4. constraints, privacy classification and out-of-scope changes;
5. validation commands/tests and explicit Definition of Done;
6. cleanup rule and destination of durable conclusions.

## Required workflow

Read → Inspect actual files and git state → Make bounded changes → Validate and review → Save provenance, decisions and final task report → Obtain acceptance when required → Delete **only** completed temporary active task.

Never delete files simply because they are considered "understood"; history, reproducibility and audit artifacts must survive.

## Agent deliverable summary format

- Scope / sources inspected
- Changed files and why
- Results and links
- Tests/evidence
- Unresolved risks and assumptions
- Explicit flags: measured_values_changed, inference_rerun, original_dataset_modified, secrets_present
- Migration status: verified / partial / blocked

## Verification gates

Separate (a) creation of a clean documentation skeleton, (b) audited code selection/migration and (c) reproducible release signoff. Never treat (a) as proof of (b) or (c).
