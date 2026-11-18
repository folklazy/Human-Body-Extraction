# Agent rules — Human Body Extraction Project Hub

## Mission
Keep the *project registry and decisions* accurate across seven delivery repositories. This hub is not a workspace for experimental code, raw CCTV footage or weight files.

## Mandatory read order
1. `README.md`
2. `REPOSITORY_REGISTRY.md`
3. `PROJECT_STATUS.md`
4. `docs/DECISIONS.md`
5. `docs/HANDOFF_STANDARD.md`
6. `tasks/ACTIVE_TASK.md` **only when present**

## Never assume
- That a previous experiment repo, source file, model or checkpoint was chosen for release merely because it exists.
- That user-reported completed work is already packaged, verified and publicly distributable.
- That a historical benchmark metric equals measured end-to-end latency.
- That company CCTV footage or derived GT may be committed to a public repository.

## Changes and safety
- Inspect existing files, git state, code, reports and provenance before edits.
- Preserve canonical CSV/JSON, reports, hashes and result artifacts; do not fabricate or silently recompute metrics.
- Update the registry, project status, decisions and links only with evidence.
- Scope changes to the current task; request approval for destructive actions, rights/visibility changes, external publication or significant new downloads.
- Prefer links to source research repositories over copying datasets or logs.
- Record blockers explicitly instead of writing a plausible but unsupported claim.
- Do not copy secrets, credentials or real CCTV sample images to public repos.

## Completion
- Validate changed links and file layout.
- Record durable conclusions in `PROJECT_STATUS.md`, `docs/DECISIONS.md` or an evidence note.
- Add a concise change summary and source references.
- Delete only the **temporary** `tasks/ACTIVE_TASK.md` after the work is accepted and durable conclusions are recorded; never delete `AGENTS.md`, reports, audit results, or the task's proof.
