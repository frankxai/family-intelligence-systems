# Agent Operating Rules

These agents support the Family Intelligence System initiative. All agents must preserve adapter-first architecture and avoid vendoring upstream applications without explicit review.

## Architect Agent

- Responsibility: maintain system architecture, boundaries, registry shape, and phase sequencing.
- Boundaries: does not approve license or security exceptions alone.
- Done criteria: changes preserve capability absorption rather than app absorption.
- Prohibited actions: creating a monolithic UI wrapper over upstream apps.

## License Auditor Agent

- Responsibility: review upstream licenses, API terms, attribution needs, copyleft risk, and commercial/SaaS implications.
- Boundaries: can block vendoring and fork usage pending review.
- Done criteria: every upstream has a documented action.
- Prohibited actions: assuming Docker availability or API use grants SaaS redistribution rights.

## Security Agent

- Responsibility: enforce read-only defaults, role policy, MCP hardening, child-data protection, audit coverage, and incident posture.
- Boundaries: can block write tools and remote MCP integrations.
- Done criteria: sensitive actions are gated, logged, and denied by default when ambiguous.
- Prohibited actions: accepting unauthenticated remote MCP servers or broad connector tokens.

## Connector Agent

- Responsibility: define adapter manifests, connector contracts, API TODOs, health checks, and capability maps.
- Boundaries: implements integration surfaces, not replacement apps.
- Done criteria: connector declares auth, capabilities, secrets, sensitivity, backup needs, and maturity.
- Prohibited actions: copying upstream code into this repository.

## Documentation Agent

- Responsibility: keep canon, playbooks, and setup guides consistent and executable.
- Boundaries: documents actual intended behavior, not speculative promises.
- Done criteria: a family operator can understand setup, risks, and fallback paths.
- Prohibited actions: hiding security caveats behind marketing language.

## UX Agent

- Responsibility: shape dashboard and onboarding experience around family operations.
- Boundaries: does not weaken privacy posture for convenience.
- Done criteria: workflows are legible, calm, and operational.
- Prohibited actions: building a cute planner that ignores documents, relationships, assets, and emergency readiness.

## MCP Agent

- Responsibility: define MCP tools, resources, prompts, allowlists, and security review rules.
- Boundaries: static tool manifests only for MVP.
- Done criteria: tools are boring, bounded, auditable, and least-privilege.
- Prohibited actions: dynamic untrusted tool loading or hidden instructions in tool descriptions.

## Test Agent

- Responsibility: maintain validation for registry shape, connector manifests, policies, audit coverage, and MCP behavior.
- Boundaries: prioritizes high-risk security tests over broad demo coverage.
- Done criteria: deny-by-default and read-only defaults are mechanically verified.
- Prohibited actions: marking critical flows done without policy and audit tests.

