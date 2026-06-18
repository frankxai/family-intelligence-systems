# Security Posture

Family data is more sensitive than ordinary productivity data. A family system can contain children, health, legal, finance, identity, home, relationship, and emergency records in one operational graph. Security is therefore a product requirement, not a deployment add-on.

## Doctrine

- Read-only first.
- Least privilege for every connector.
- Deny-by-default for unknown action or unknown sensitivity.
- Audit every meaningful action.
- No unauthenticated remote MCP.
- No dynamic untrusted tool loading.
- Child data is protected as critical by default.
- Credentials and emergency access require explicit security review.
- Raw sensitive data stays in family-owned systems where possible.

## MCP Controls

- Static allowlist of tools.
- Tool description review.
- Scoped connector tokens.
- Output sanitization.
- Prompt-injection aware boundaries for documents, email, web pages, and notes.
- Confirmation gates for writes and exports.
- Per-family tenant isolation.
- Rate limiting.
- Environment variable isolation.
- Audit events for success, failure, blocked, and confirmation-required outcomes.

## Threats

- Tool poisoning.
- Prompt injection from documents, email, websites, notes, and file metadata.
- Cross-family data leakage.
- Overly broad connector tokens.
- Accidental export of private data.
- Tool definition shadowing or rug-pull changes.
- Supply-chain risk from upstream MCP servers.
- Backups that are readable by unintended parties.

## Incident Response

1. Disable affected connector or MCP tool.
2. Rotate scoped tokens and secrets.
3. Preserve audit events.
4. Identify affected families, actors, resources, and time windows.
5. Notify owners with practical remediation steps.
6. Add regression tests and update the security posture.

