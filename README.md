# Scanners — Delivery Note Processing and Archiving

A document-processing application that receives scanned supplier delivery notes, extracts their information and organizes the resulting documents into a searchable archive.

Administrative teams can process batches of scanned delivery notes without manually separating every PDF and filing every document. Automated extraction is paired with a review workflow for uncertain supplier matches, duplicates and documents requiring correction.

## Users

| Role | Use |
|---|---|
| Reader | Search, inspect and download authorized delivery notes. |
| Operator | Import scans, review processing results and correct filing problems. |
| Administrator | Manage supplier records, naming policies, retention and operational diagnostics. |

## Main features

- **Scan intake.** Receive PDFs from an input location or a controlled import.
- **Document extraction.** Combine OCR and model-assisted extraction to identify delivery-note information.
- **Splitting and filing.** Separate delivery notes and organize them under the appropriate supplier.
- **Search and inspection.** Browse document spaces, search across them and inspect PDFs and provenance.
- **Exception handling.** Review suspected duplicates, rejected documents and unresolved supplier matches.
- **Archive management.** Move, rename, export, restore and manage documents through controlled operations.

## Typical workflow

1. Submit a scanned PDF or batch to the input area.
2. Follow extraction, document separation and supplier matching.
3. Review uncertain results and resolve document conflicts.
4. Find the archived note through supplier browsing or search.

## Project structure

```text
scanners-public-version/
├── delivery-note-archive/
│   ├── backend/
│   │   ├── src/
│   │   │   └── document_archive/
│   │   └── tests/
│   ├── config/
│   ├── deploy/
│   │   ├── systemd/
│   │   └── test/
│   ├── docs/
│   │   ├── decisions/
│   │   │   └── README.md
│   │   ├── guides/
│   │   ├── issue/
│   │   ├── module-006/
│   │   ├── module-007/
│   │   ├── module-010/
│   │   │   └── runs/
│   │   └── specifications/
│   ├── issues/
│   │   ├── epics/
│   │   ├── features/
│   │   ├── tasks/
│   │   └── README.md
│   ├── module-009/
│   ├── packaging/
│   ├── registry_api/
│   │   ├── src/
│   │   │   └── registry_api/
│   │   ├── tests/
│   │   ├── pyproject.toml
│   │   ├── README.md
│   │   └── requirements.txt
│   ├── registry_ui/
│   │   ├── src/
│   │   │   ├── __tests__/
│   │   │   ├── api/
│   │   │   ├── components/
│   │   │   ├── styles/
│   │   │   └── utils/
│   │   ├── tests/
│   │   ├── package.json
│   │   └── README.md
│   ├── scripts/
│   ├── pyproject.toml
│   ├── README.md
│   └── requirements.txt
├── docs/
│   └── design/
│       ├── decisions.md
│       ├── requirements.md
│       └── verification.md
├── ARCHITECTURE.md
└── README.md
```

[Complete directory structure](docs/design/structure.md)

| Area | Responsibility |
|---|---|
| Processing backend | Python ingestion, OCR, extraction and document-classification services. |
| Registry API | FastAPI access to document records, operations and administration. |
| Registry interface | React/TypeScript browsing, search, review and settings screens. |
| Document storage | Private PDFs, processing outputs and supplier-organized archive locations. |
| Extraction adapters | Tesseract and server-side AI integration. |

## Technology

Python, FastAPI, React, TypeScript, Tesseract OCR, model-assisted extraction and Docker.

## Engineering

- [Architecture](ARCHITECTURE.md)
- [Product requirements](docs/design/requirements.md)
- [Design decisions](docs/design/decisions.md)
- [Verification strategy](docs/design/verification.md)

OCR and extracted information can be incomplete or incorrect. Review queues and access-controlled document operations remain necessary.

---

Source code, operational configuration and project-specific data are withheld for confidentiality.
