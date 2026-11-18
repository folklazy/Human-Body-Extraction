# Human Body Extraction — Project Hub

ศูนย์กลางสำหรับเชื่อมโยง ตรวจสอบสถานะ และส่งต่องานของโปรเจกต์ **Human Body Extraction from CCTV** โดยเป็นดัชนีของผลงานและการตัดสินใจ **ไม่ใช่ที่รวบรวม Source Code หรือ Dataset ทั้งหมด**.

> สถานะ: ผู้พัฒนาแจ้งว่างานทดลองและระบบต้นแบบเสร็จแล้ว; ขณะนี้อยู่ระหว่างจัด Repository ชุดส่งมอบและทำเอกสาร. ข้อความนี้ไม่ใช่การรับรองว่าการย้ายไฟล์หรือ release validation เสร็จสิ้น.

## 7 repositories

1. [YOLO Instance Segmentation](https://github.com/folklazy/YOLO-Instance-Segmentation) — curated research, benchmarks, selected model. **Planned**
2. [Human Parsing](https://github.com/folklazy/Human-Parsing) — parsing models, taxonomy, comparative evaluation. **Planned**
3. [Clothing Color Extraction](https://github.com/folklazy/Clothing-Color-Extraction) — color methods and evaluation. **Planned**
4. [CCTV Ground Truth Dataset](https://github.com/folklazy/CCTV-Ground-Truth-Dataset) — annotation policy, QA and metadata; raw company data private. **Planned**
5. [Web Application + API + Database](https://github.com/folklazy/Human-Body-Extraction-Web-Platform) — web, API, persistence, deployment. **Planned**
6. **This repository** — project registry, cross-component decisions, status and handoffs.
7. [A Comparative Study of YOLO-Based Instance Segmentation](https://github.com/folklazy/A-Comparative-Study-of-YOLO-Based-Instance-Segmentation) — final integrated, version-pinned end-to-end product and delivery documentation. **Packaging in progress**

**Existing experimental repositories stay intact.** They are historical sources of truth; do not bulk-copy or rewrite their canonical metrics. See [REPOSITORY_REGISTRY.md](REPOSITORY_REGISTRY.md).

## What the system does

CCTV image/video → selected YOLO instance segmentation → person-specific human parsing → upper/lower garment color analysis → structured person attributes → Web/API/Database display and retrospective attribute search.

Scope excludes person identity verification and cross-camera identity tracking.

## Read first

- [Repository registry](REPOSITORY_REGISTRY.md) — existing source links versus new delivery repos
- [Status](PROJECT_STATUS.md) — verified/pending boundaries
- [Architecture](docs/ARCHITECTURE.md) — integration contracts and evidence
- [Decisions](docs/DECISIONS.md) — agreed repo split and protection policy
- [Handoff standard](docs/HANDOFF_STANDARD.md) — how Codex agents should work
- [AGENTS.md](AGENTS.md) — non-negotiable instructions

## Safety

Public documents must not expose original company CCTV images, annotations derived from restricted footage, personal data, API keys, database connection strings or proprietary checkpoints. Publishing rights are unconfirmed. Every numerical result must cite a verified report and its version.
