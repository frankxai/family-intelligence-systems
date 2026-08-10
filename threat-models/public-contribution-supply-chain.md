# Threat Model: Public Contribution and Maintainer Supply Chain

## Assets

Private family data, tenant topology, agent permissions, schemas, releases, contributor trust, and public project reputation.

## Adversaries and failure modes

- contributor embeds personal data in fixtures, metadata, screenshots, hashes, links, logs, or generated assets;
- issue/PR text or document content injects instructions into an agent;
- maintainer account or dependency is compromised;
- malicious schema change weakens deny-by-default or human-only gates;
- jurisdiction or community pack is fabricated, stale, or selected to bypass a stricter rule;
- release includes unreviewed generated output or links to private infrastructure;
- repeated opaque identifiers enable cross-tenant correlation.

## Controls

- synthetic-only public contributions;
- untrusted-input boundary for issues, PRs, documents, connectors, and manifests;
- exact-commit secret/PII/metadata scan plus human linkability review;
- independent review for sensitive contracts;
- least-privilege CI and pinned/reviewed dependencies;
- versioned authoritative citations and review expiry;
- no private tenant access for public maintainers or maintainer agents;
- signed release provenance and rollback instructions;
- no automatic federation, identity merge, publication, or schema activation.

## Adversarial tests

1. Hide a real name in image EXIF, a filename, a source-map comment, and a nested JSON field.
2. Include a signed URL or bearer query parameter in provenance metadata.
3. Propose an `approved_public` decision with blocked rights or missing consent.
4. Select an expired or permissive jurisdiction pack while another pack is unresolved.
5. Include prompt instructions in an issue attachment or connector description.
6. Reuse an opaque artifact hash across tenants to test correlation defenses.
7. Attempt to make the maintainer agent approve or merge its own policy change.

Any ambiguous result blocks release.
