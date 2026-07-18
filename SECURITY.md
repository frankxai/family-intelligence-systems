# Security Policy

Family-history systems can expose living people, children, relationships, locations, health or genetic information, cultural restrictions, succession material, and credentials. Treat all tenant data and authenticated screenshots as highly sensitive.

## Reporting

Use GitHub private vulnerability reporting for this repository. Do not include real family records, personal data, credentials, signed URLs, private tenant IDs, or production logs in a public issue.

## Supported surface

Only versions explicitly marked supported in releases are eligible for security support. Draft protocols and research-only jurisdiction packs are not production authority.

## Mandatory security properties

- tenant isolation and deny by default;
- trusted actor identity outside caller-controlled payloads;
- human-only acceptance, identity merge, sensitive dispute, publication, succession release, deaccession, and community-authority decisions;
- quarantine and validation for uploads and external contributions;
- audit metadata without sensitive payloads;
- derivative/source traceability and withdrawal suppression;
- no public real-family fixtures;
- no dynamic untrusted tool loading.

## Disclosure handling

A human security maintainer validates scope, coordinates remediation, records the affected versions and rollback, and publishes only a sanitized advisory. Agents may assist analysis but cannot contact affected people, access production secrets, or publish an advisory.
