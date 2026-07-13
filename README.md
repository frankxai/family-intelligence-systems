# Family Intelligence Systems

Canonical doctrine, registry, security posture, playbooks, prompts, MCP specs, and implementation backlog for the Family Intelligence System initiative.

Families are not disorganized because they lack apps. They are disorganized because memory, documents, relationships, responsibilities, rituals, assets, and decisions live in separate systems. This repo makes the architecture legible before code is absorbed.

## Architecture Position

This repository is not the deployable product. It is the intelligence layer:

- canon and operating doctrine
- upstream app and MCP registry
- adapter and connector specifications
- security and license posture
- setup and review playbooks
- Codex implementation backlog
- Guardian, organizer, documentation, research, contact-steward, elder-support, and personal-hub agent doctrine

The runtime lives in `family-intelligence-os`.

## Claims And Continuity Kernel

The July 2026 foundation adds the missing governance layer around family memory:

- `adrs/ADR-001-claims-not-facts.md`
- `protocols/claims/v1.md`
- `protocols/evidence/v1.md`
- `protocols/consent/v1.md`
- `protocols/publication/v1.md`
- `protocols/disputes/v1.md`
- `protocols/succession/v1.md`
- `protocols/identity/v1.md`
- `protocols/export-restore/v1.md`
- `protocols/intake/v1.md`
- `schemas/*.schema.json`
- `canon/family-circles-and-guardianship.md`
- `canon/private-family-tenant-topology.md`
- `canon/german-family-portal.md`
- `canon/data-classification-and-processing-map.md`
- `templates/de/`
- `skills/`

The family tree is a view over accepted, scope-appropriate claims. Agents can extract and compare; only authorized humans accept claims, resolve sensitive disputes, approve publication, or release succession access.

The private pilot uses one governed tenant with resource-scoped circles. Household, kinship, guardianship, godparent relationships, and access are modeled independently; no child's name belongs in a hostname, URL, public fixture, screenshot, or repository.

## Founding Proof

The public-safe pilot is the **Riemer-Gorte Living Archive** / **Lebendiges Familienarchiv Riemer-Gorte**. Real family records stay outside this public repository. Living people are private by default, and children never appear in public fixtures, screenshots, analytics, or examples.

## Hard Rules

- Absorb capabilities, not code.
- Prefer API adapters, MCP tools, Docker recipes, and playbooks over vendoring upstream apps.
- Treat family data as high-trust infrastructure.
- Default to read-only and deny-by-default policies.
- Review license, security, and maintainability before any fork or vendored dependency.
- Keep private archival availability separate from public publication.
- Treat `noindex` and hidden URLs as discoverability hints, never authorization.

## Guardian Network

The next layer is the Family Guardian Network: narrow agents for privacy, documentation, research, food and household life, gatherings, elder support, contact stewardship, and personal family hubs. See `canon/family-guardian-network.md`, `canon/family-hubs-and-libraries.md`, `registry/agents.yaml`, and `registry/hermes-swarm.family-guardian.json`.
