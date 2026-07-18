# Jurisdiction Packs

Jurisdiction packs are versioned, source-backed operational research. They are not legal advice and are inactive until a qualified human reviewer records approval.

## Runtime rule

- `reviewed` and unexpired: evaluate alongside every other plausibly applicable pack.
- `research_only`, expired, missing, conflicting, or unsupported: `block_pending_review`.
- User locale, citizenship, source language, or a selected country cannot by itself determine applicability.
- Community-authority restrictions and consent are evaluated independently and may be stricter.

## Initial research packs

| Pack | Scope | Status |
|---|---|---|
| `eu-GDPR/v1.json` | EU living-person data baseline | Research only |
| `nl-NL/v1.json` | Dutch civil-register transfer periods | Research only |
| `de-DE/v1.json` | German civil-status continuation periods | Research only |

## Contribution requirements

Every change must cite a current authoritative source, state the exact operational effect, update `review_due`, retain prior versions when decisions depend on them, and pass independent privacy/governance review. Do not submit personal family examples.
