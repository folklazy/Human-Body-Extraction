# Repository registry

**Seven delivery roles**. New delivery repositories 1–5 are **planned** until created and populated. Existing experiment repos remain unchanged. Status is not a claim of implementation parity.

| Role | Delivery repository | Status | Existing source candidates |
|---|---|---|---|
| 1. YOLO | [YOLO-Instance-Segmentation](https://github.com/folklazy/YOLO-Instance-Segmentation) | Planned | [MOTS20 study](https://github.com/folklazy/YOLO_Instance_Segmentation_MOTS20_Scaling_Study), [CCTV600 study](https://github.com/folklazy/YOLO_Instance_Segmentation_CCTV600_Scaling_Study), historical per-size benchmarks |
| 2. Parsing | [Human-Parsing](https://github.com/folklazy/Human-Parsing) | Planned | [Human_Parsing_Study](https://github.com/folklazy/Human_Parsing_Study), [CCTV600 benchmark](https://github.com/folklazy/Human_Parsing_CCTV600_Benchmark) |
| 3. Color | [Clothing-Color-Extraction](https://github.com/folklazy/Clothing-Color-Extraction) | Planned | [Garment-Color-Extractor](https://github.com/folklazy/Garment-Color-Extractor) |
| 4. CCTV GT | [CCTV-Ground-Truth-Dataset](https://github.com/folklazy/CCTV-Ground-Truth-Dataset) | Planned; PRIVATE recommended | [CCTV_Dataset_Development](https://github.com/folklazy/CCTV_Dataset_Development), [CCTV-Human-Parsing-600-Dataset](https://github.com/folklazy/CCTV-Human-Parsing-600-Dataset) |
| 5. Platform | [Human-Body-Extraction-Web-Platform](https://github.com/folklazy/Human-Body-Extraction-Web-Platform) | Planned; PRIVATE recommended | `folklazy/Body-Extraction-Human-WebApp` (private) |
| 6. Hub | [Human-Body-Extraction](https://github.com/folklazy/Human-Body-Extraction) | Documentation setup | This repository |
| 7. Final | [A-Comparative-Study-of-YOLO-Based-Instance-Segmentation](https://github.com/folklazy/A-Comparative-Study-of-YOLO-Based-Instance-Segmentation) | Packaging / validation pending | Outputs selected from 1–5 after audit |

## Registry maintenance contract

For each delivery repository, record: owner, visibility, purpose, canonical source(s), selected code commit/tag, selected checkpoint ID/hash, interface contract version, release status, relevant test report, known blockers and update date.

Do not invent values. Use **TBD / not verified** until audited. Never mirror all experimental data into the delivery repo. Source repositories remain archives of original evidence.

## Cohort and scientific boundary

- YOLO comparative research used multiple family/size combinations; prior user selection: YOLO26x-Seg.
- The actual final parser and color-method selection must be read from verified final records before any pinning.
- CCTV annotation and source footage may have publication restrictions even when a dataset documentation repo is public.
