# Design Decisions

## 1. Uncertain extraction enters a review path

**Benefit.** Operators can distinguish verified filing from results that still need attention.

**Trade-off.** Automation must carry uncertainty and provenance through the user interface.

## 2. Separate document processing from archive interaction

**Benefit.** Users can consult the archive while background intake continues.

**Trade-off.** Processing state and registry state must remain consistent.

## 3. Make destructive operations explicit

**Benefit.** Operators can inspect the intended scope before changing archive contents.

**Trade-off.** Operations require confirmation, progress reporting and interruption recovery.
