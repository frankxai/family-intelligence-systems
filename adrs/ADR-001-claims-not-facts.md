# ADR-001: Model family history as claims, not facts

Status: accepted

Date: 2026-07-12

## Context

A statement such as “A is the parent of B” can be a memory, interpretation, document transcription, disputed allegation, or verified relationship. A plain family-tree edge hides who asserted it, what supports it, whose privacy is affected, and whether it may be shared.

## Decision

The canonical lineage object is a `FamilyClaim`. A claim stores the assertion, source references, provenance, confidence, affected living people, consent receipts, review state, disputes, supersession, and a separate publication state.

AI may extract candidate claims, find possible duplicates, identify contradictions, and prepare research summaries. AI may not accept, reject, publish, or resolve a sensitive relationship claim. Those state changes require an authorized human steward and an audit event.

## Lifecycle

```text
received
-> quarantined
-> normalized
-> possible_duplicate
-> evidence_reviewed
-> consent_reviewed
-> steward_reviewed
-> accepted | disputed | rejected | unresolved
-> privately_available
-> publication_review
-> publicly_published
```

Not every claim traverses every state. Rejected and unresolved claims remain auditable and are not silently deleted.

## Consequences

- The family tree is a view over accepted, scope-appropriate claims.
- GEDCOM 7 is an import/export format, not the complete internal governance model.
- Public biographies are generated only from publication-approved claims and must cite source artifacts.
- Corrections create a superseding claim or decision; they do not rewrite history without trace.
