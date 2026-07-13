# Schema changelog

## 2026-07-13

- Added `intake-token.schema.json` for single-use, family-scoped secure submission links.
- Added `intake-case.schema.json` to keep transport and quarantine state separate from claim acceptance.
- Added `private-tenant-manifest.schema.json` for policy-only private-pilot configuration without personal records or secrets.

## 2026-07-12

- Added claim, evidence, consent receipt/withdrawal, publication decision, succession policy, family circle, and export manifest schemas.
- Established JSON Schema draft 2020-12 and fail-closed `additionalProperties: false` as the v1 baseline.
