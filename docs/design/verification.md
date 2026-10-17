# Verification Strategy

## Critical behaviors

- A multi-page input is separated without losing document pages.
- Uncertain supplier matches remain visible for review.
- A duplicate decision preserves a comprehensible document history.
- Interrupted file operations leave a recoverable, visible state.

## Test layers

| Layer | Focus |
|---|---|
| Unit | Domain rules, validation and state changes without live external dependencies. |
| Integration | Consistency across application services and their storage or external-service adapters. |
| User journey | A complete path from a user action to its visible outcome, including failure states. |

## Environment checks

OCR and extracted information can be incomplete or incorrect. Review queues and access-controlled document operations remain necessary.
