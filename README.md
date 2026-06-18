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

## Hard Rules

- Absorb capabilities, not code.
- Prefer API adapters, MCP tools, Docker recipes, and playbooks over vendoring upstream apps.
- Treat family data as high-trust infrastructure.
- Default to read-only and deny-by-default policies.
- Review license, security, and maintainability before any fork or vendored dependency.

## Guardian Network

The next layer is the Family Guardian Network: narrow agents for privacy, documentation, research, food and household life, gatherings, elder support, contact stewardship, and personal family hubs. See `canon/family-guardian-network.md`, `canon/family-hubs-and-libraries.md`, `registry/agents.yaml`, and `registry/hermes-swarm.family-guardian.json`.
