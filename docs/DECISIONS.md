# Architecture decision log

## ADR-001 — Seven delivery repositories
**Decision:** Five implementation/research workstream repos; one `Human-Body-Extraction` project hub; one `A-Comparative-Study-of-YOLO-Based-Instance-Segmentation` final integrated repository.

**Rationale:** Separate evaluation evidence by domain while offering a single deployable final deliverable. "End-to-End Integration & Evaluation" is a responsibility of the final repo, not an eighth repo.

## ADR-002 — New curated delivery repos, old archives preserved
**Decision:** Organize fresh delivery repositories instead of bulk copying the mixed original VS Code workspace. Original code and experiment repos remain as provenance sources until independently reviewed.

**Rationale:** Some older files are useful, some exploratory, some obsolete; the project is reported complete and now requires professional handoff packaging.

## ADR-003 — Temporary agent work briefs
**Decision:** `AGENTS.md` and project documentation are permanent. `tasks/ACTIVE_TASK.md` is temporary, removed **only after** validation and durable handoff records. A reusable template remains.

## ADR-004 — Separate platform and final integration
**Decision:** Web App + API + Database share one platform repo; Final repo owns the pinned integrated application and E2E evaluation. They must avoid mirrored histories and uncontrolled duplicated source copies.

## ADR-005 — Privacy-first data handling
**Decision:** Keep raw company CCTV and its sensitive annotations out of public repos until explicit dissemination rights are verified. Private defaults recommended for CCTV and Platform workstreams. No secrets or credentials in git.

## ADR-006 — Research measurement integrity
**Decision:** Existing canonical metrics/results are frozen unless a separately scoped rerun is approved. Always distinguish standalone model benchmarks from full integrated system performance; label inferred/derived values.
