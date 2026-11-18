# Delivery migration plan — audited, not bulk-copied

Updated 2026-11-19 (Asia/Bangkok)

## Objective
The owner reports a completed internship Human Body Extraction project, but their original VS Code/SSH workspace (historically `~/folk/Human-Body-Extraction`, verify on target host) is mixed: research experiments, actual runtime, unused tests, full data and temporary outputs. The five clean workstream repositories are **new handoff containers**, not clones of all local files.

## Verified initial setup
- Created workstream repos:
  1. [YOLO-Instance-Segmentation](https://github.com/folklazy/YOLO-Instance-Segmentation) — public
  2. [Human-Parsing](https://github.com/folklazy/Human-Parsing) — public
  3. [Clothing-Color-Extraction](https://github.com/folklazy/Clothing-Color-Extraction) — public
  4. [CCTV-Ground-Truth-Dataset](https://github.com/folklazy/CCTV-Ground-Truth-Dataset) — private
  5. [Human-Body-Extraction-Web-Platform](https://github.com/folklazy/Human-Body-Extraction-Web-Platform) — private
- Existing [Project Hub](https://github.com/folklazy/Human-Body-Extraction) and [Final End-to-End](https://github.com/folklazy/A-Comparative-Study-of-YOLO-Based-Instance-Segmentation) remain separate.
- Each new repo has README, AGENTS, scope, source inventory, quality gates, first active task, changelog and gitignore.
- No original source code, checkpoints, CCTV images/annotations or historical benchmark metrics were transferred in this initialization phase.

## Phase 1 — Inventory with the original SSH workspace (read-only)
1. Check workspace and all relevant source git branches, uncommitted changes, symlinks and `AGENTS.md`.
2. Map actual modules used by deployed/demo runtime, not merely newest folder names.
3. Classify each file as shipping code, canonical evidence, derived documentation, exploratory, unused, generated cache, external/restricted asset or secret.
4. Record SHA256/commit, path, dependency, origin, rights and reason to include/exclude.
5. Ask owner to resolve ambiguity; never delete originals to “clean up”.

## Phase 2 — Curated workstream handoff
- Migrate approved **source code + minimal configs + tests + necessary documentation** into each new repo; keep canonical research evidence accessible through links and summaries.
- Validate that measured values are unchanged; reports must distinguish original and newly derived analysis.
- Preserve selected weights/checkpoint manifests and licenses. Do not automatically upload multi-GB weights or proprietary material.
- Use consistent README summary, methodology, detailed findings, qualitative visual reasoning, limitations and evidence index.
- For private CCTV dataset, maintain a data card, manifest, QA/splits and safe private storage strategy; approval required before moving company footage even into a private repo.

## Phase 3 — Cross-component contracts
- Freeze versioned YOLO→Parsing and Parsing→Color interfaces (RGB/BGR, W×H, mask coordinate system, taxonomy, missing/unknown attributes).
- Verify Web API/DB input-output schema against actual app.
- Record exact commits and hash manifests in the project Hub.

## Phase 4 — Final end-to-end release
- Assemble only chosen and tested module versions in Final repo; do not mirror all experiments.
- Include deployment, install, model retrieval, config examples, valid input sample (permission-cleared), API docs, DB migration and user guide.
- Run smoke/integration/end-to-end tests and record real integrated latency/FPS/VRAM with identified hardware and fixture counts.
- Protect data/secret rights; only mark a release “complete” with evidence.

## Phase 5 — Academic handoff
- Use original experiment reports to prepare research narrative, tables and visual qualitative analyses; keep versioned references.
- Link final report, proposal, test evidence, known limitations and deployment guide without duplicated canon.
- Preserve Hub registry/status/decisions and handoff notes.

## Agent task lifecycle
Each workstream has `tasks/ACTIVE_TASK.md` that instructs the first inventory/curation pass. It is **not** deleted upon reading. After code/tests/documentation are checked and owner accepts the handoff, preserve conclusions in permanent docs/CHANGELOG, then delete only this temporary task file. Permanent `AGENTS.md` and audit evidence remain.

## Non-negotiable scientific and privacy rules
- Original benchmark files and dataset originals remain untouched unless independently authorized.
- Measured values changed? `false` unless an explicitly approved new measurement with provenance.
- No automatic training, full inference reruns, unapproved dependency upgrades, license circumvention or publication of restricted images.
- Do not expose private credentials or sensitive company video/GT in a public repository.
- Status labels: `CREATED` (repo), `AUDITED` (inventory), `CURATED` (reviewed migration), `VALIDATED` (tests passed), `RELEASED` (accepted final delivery) are independent.
