# Product Requirements

A document-processing application that receives scanned supplier delivery notes, extracts their information and organizes the resulting documents into a searchable archive.

## Users

| Role | Expected outcome |
|---|---|
| Reader | Search, inspect and download authorized delivery notes. |
| Operator | Import scans, review processing results and correct filing problems. |
| Administrator | Manage supplier records, naming policies, retention and operational diagnostics. |

## Functional scope

| Capability | User outcome |
|---|---|
| Scan intake | Receive PDFs from an input location or a controlled import. |
| Document extraction | Combine OCR and model-assisted extraction to identify delivery-note information. |
| Splitting and filing | Separate delivery notes and organize them under the appropriate supplier. |
| Search and inspection | Browse document spaces, search across them and inspect PDFs and provenance. |
| Exception handling | Review suspected duplicates, rejected documents and unresolved supplier matches. |
| Archive management | Move, rename, export, restore and manage documents through controlled operations. |

## Main user journey

1. Submit a scanned PDF or batch to the input area.
2. Follow extraction, document separation and supplier matching.
3. Review uncertain results and resolve document conflicts.
4. Find the archived note through supplier browsing or search.

## Acceptance priorities

- A multi-page input is separated without losing document pages.
- Uncertain supplier matches remain visible for review.
- A duplicate decision preserves a comprehensible document history.
- Interrupted file operations leave a recoverable, visible state.

## Product constraint

OCR and extracted information can be incomplete or incorrect. Review queues and access-controlled document operations remain necessary.
