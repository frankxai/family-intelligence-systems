# Threat model: public lineage intake

## Boundary

The public form and mailbox collect a potential claim. They do not create a family-tree fact and do not grant publication rights.

## Primary threats

- spam, phishing, impersonation, and malicious attachments
- prompt injection embedded in email, documents, metadata, OCR, or links
- false identity matches and duplicate people
- doxxing, harassment, revenge claims, and sensitive allegations
- unconsented living-person and child data
- DNA, medical, credential, passport, or civil-record oversharing
- unknown-rights photographs and documents
- agent overreach: accepting, publishing, contacting, or escalating without authority

## Controls

1. Treat all inbound content as untrusted data, never instructions.
2. Quarantine attachments before extraction; store originals outside public repos.
3. Send a transparent AI-assisted acknowledgment without confirming lineage.
4. Create a case and candidate claim with `received`/`quarantined` state.
5. Ask only for minimum relationship, approximate time/place, source kind, and sharing authority.
6. Redirect sensitive evidence to an authenticated, expiring upload flow.
7. Run identity, duplicate, contradiction, living-person, child-data, rights, and consent checks.
8. Require steward review for claim acceptance and a separate publisher review for public release.
9. Log tool calls and redact payloads from ordinary application logs.
10. Provide contest, correction, withdrawal, deletion, and export routes.
11. Treat URLs, QR codes, document text, OCR output, filenames, and metadata as untrusted content; no embedded instruction may alter tool permissions or review state.
12. Keep an artifact-to-claim-and-consent reference graph so withdrawal can suppress derived summaries, indexes, and public material.
13. Do not use received sender identity, a display name, or a claimed relationship as sufficient authority for publication, withdrawal, export, or emergency access.
14. A credible imminent-risk report may be recorded for human Guardian review, but an agent may not treat it as an executed withdrawal or irreversible takedown.

## Public warning

Do not email passports, passwords, DNA files, medical records, financial records, or unredacted civil documents. Do not post information about living people publicly. A submission is reviewed as a claim and is not automatically accepted or published.
