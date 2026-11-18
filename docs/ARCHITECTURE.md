# System architecture and integration boundaries

## Functional pipeline

CCTV frame/image/video → YOLO instance segmentation per person → person-aware human parsing → body/clothing mask (upper/lower etc.) → garment-color extraction → structured per-person attributes → Web/API persistence, display and attribute search.

## Ownership

- **YOLO repository:** individual person boundaries, confidence, mask coordinates and image dimensions.
- **Parsing repository:** body/clothing part taxonomies, masks, class mapping, uncertainty.
- **Color repository:** upper/lower garment color semantics, single/multi-color and unknown handling.
- **Dataset repository:** image provenance, annotations, splits, QA and permitted fixtures.
- **Web Platform repository:** application endpoints, UI, database schema, storage lifecycle and errors.
- **Final repository:** validated interface contracts, pinned component versions, integrated runtime and end-to-end tests.
- **Hub:** records relationships and decisions; no implementation duplication.

## Required cross-module contracts (verify before freezing)

1. Input RGB/BGR convention and original W×H metadata.
2. Bounding-box coordinate system, instance IDs, pixel-aligned native-resolution masks and handling of overlaps.
3. Parser taxonomy/version and mapping of parts to clothing categories.
4. Per-person attribute schema including uncertain/unknown and confidence semantics.
5. API JSON and persistence schema/version; note if output is frame-level rather than tracked across frames.
6. GPU/CPU deployment assumptions, batch mode, model hashes and release-specific timings.

No module may silently rename labels, normalize colors or shift mask coordinates without versioning and regression tests.

## Safety / scope

The system describes visible attributes; it does **not** claim identification of individuals, identity verification or cross-camera tracking. Any company CCTV footage, person imagery and identity-linked data need documented publication approval prior to public commits.
