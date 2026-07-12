# Family Intelligence Data Classification and Processing Map

This is a product-design map for privacy engineering and DPIA preparation. It is not legal advice and does not replace jurisdiction-specific counsel.

## Classification

| Class | Examples | Default scope | Core handling rule |
| --- | --- | --- | --- |
| Operational | tenant IDs, feature flags, non-identifying metrics | system | minimize, redact ordinary logs, retain only what supports operations |
| Family claims and sources | relationship assertion, letter, photograph, timeline source | private family | claims are not facts; preserve provenance and publication state |
| Living-person data | contact details, current location, personal story, account profile | self by default | share only through purpose-specific, revocable consent |
| Child and dependent data | child profile, school, image, learning material, guardian relationship | guardian-managed private scope | no public discoverability; guardian authority is purpose-limited |
| Special or high-risk data | genetic, health, disability, religion, ethnicity, abuse, finance, legal records | blocked from MVP intake | require a separately approved product, legal, and security path |
| Access and continuity data | recovery codes, emergency packet, guardian quorum, estate instructions | restricted private scope | no AI or timer can release access; human quorum and audit are required |
| Security and audit data | authorization decision, tool invocation, consent state change | restricted system scope | retain minimal metadata; redact payloads and allow cryptographic payload deletion |

## Processing activities

| Activity | Permitted input | Output | Mandatory controls |
| --- | --- | --- | --- |
| Public inquiry | minimum contact and claimed connection | quarantined case | anti-spam, attachment quarantine, no lineage confirmation |
| Evidence intake | authenticated, expiring upload with declared authority | private evidence record | malware/content scan adapter, provenance, rights, sensitivity, encrypted storage |
| AI assistance | approved, minimum necessary source excerpt | candidate extraction or source-grounded summary | tool approval, model/data boundary, citations, no autonomous acceptance or publication |
| Steward review | claims, evidence, consent, dispute context | human decision | conflict review, audit event, separate publication decision |
| Private family view | accepted, scope-appropriate claims | tree, timeline, library | server-side tenant and audience authorization |
| Public archive | approved redacted material | public page or download | Guardian/publisher review, consent receipt, noindex for any private route |
| Export and restore | export-eligible private records | encrypted family package | explicit request, recipient confirmation, manifest, restore drill |
| Continuity drill | synthetic or specifically designated minimum packet | verified drill receipt | quorum simulation, cooling/revocation, no inactivity-only release |

## Non-negotiable boundaries

1. A relationship is never an access grant.
2. A source is never an accepted fact.
3. Consent to store is not consent to publish, train, export, or share with an agent.
4. A public URL, `noindex`, or email address is not authorization.
5. Private originals, prompts, and retrieved content do not enter public repositories, telemetry payloads, or arbitrary remote tools.
6. Every retained derivative must point to source, consent, scope, and review references so it can be suppressed or re-evaluated.

## DPIA evidence pack

Before a hosted pilot begins, maintain a versioned record of: processing purpose; data classes; user groups; jurisdictions; vendors and subprocessors; data-flow diagram; retention and deletion behavior; access roles; transfer locations; threat assessment; mitigations; residual risk; owner; reviewer; and review date. Any change to high-risk data, public publication, identity, export, or continuity requires a new review.
