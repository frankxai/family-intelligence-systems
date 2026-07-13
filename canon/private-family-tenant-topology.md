# Private family tenant topology

Status: pilot architecture

Date: 2026-07-13

## Decision

Start with one private family tenant and multiple policy circles. Do not create a separate deployment, repository, subdomain, or database for every household or branch.

The tenant is the durable governance boundary. Every resource inside it—claim, document, interview, contact, task, learning path, emergency instruction, or publication candidate—receives its own scope, purpose, affected-person list, retention rule, and consent state.

Kinship and access are separate graphs. Being a parent, sibling, cousin, partner, descendant, godparent, or family steward never grants automatic access.

## Naming model

| Concept | German member-facing name | English system name | Purpose |
| --- | --- | --- | --- |
| Personal space | Mein Bereich | Self space | Private memory, preferences, owned documents, drafts |
| Current household | Haushalt | Household | Shared daily life for people who currently operate one household |
| Closest trusted people | Engster Kreis | Core circle | Explicitly invited, resource-scoped trusted relationships |
| Wider relatives | Großfamilie | Extended family | Branches, aunts/uncles, cousins, adult relatives; low sensitivity by default |
| Next generation | Nachkommen & Patenschaften | Descendants & guardianship | Guardian-managed child and godchild spaces, age transition required |
| Professional help | Vertrauenspersonen | Trusted advisers | Time-bounded, purpose-limited legal, care, archival, or technical access |
| Deliberately public | Öffentliches Archiv | Public archive | Separately reviewed and explicitly published material |

`Patenonkel` translates to **godfather**. If the person is also biologically an uncle, use **uncle and godfather**. A godparent relationship expresses care and continuity; it does not imply custody, legal guardianship, or data authority.

## Circle rules

### Mein Bereich

- Default scope for every new personal resource.
- The subject can propose a later share but no agent may widen the scope.
- Emergency and succession designations remain separate from ordinary sharing.

### Haushalt

- Contains only people who explicitly operate a current household together.
- Partnership, residence, and family lineage are not inferred from one another.
- Household access can be revoked without altering the family tree.

### Engster Kreis

- Used for individually invited parents, siblings, partners, or chosen trusted people.
- Membership alone reveals no resource; every sensitive resource still needs a grant.
- A member can be in the core circle for coordination but excluded from medical, financial, dispute, or succession material.

### Großfamilie

- Suitable for reunion planning, approved history, recipes, traditions, public-record research, and low-sensitivity contact coordination.
- Sensitive information about living people is denied by default.
- Branch stewards may propose corrections but cannot accept claims about another branch without review.

### Nachkommen & Patenschaften

- No public discoverability and no child profile in source code, analytics, demo data, screenshots, hostnames, or URLs.
- A verified guardian defines purpose, circle, duration, and contributors.
- The child receives age-appropriate notice and participation as capacity develops.
- A godparent can contribute memories or learning material only through an explicit guardian grant.
- A scheduled age-transition review transfers access, export, correction, and withdrawal authority to the person when appropriate.

## Private pilot route model

Use opaque identifiers in all storage and links. Human names are display data loaded only after authorization.

```text
familie.frankx.ai/
├── ich
├── haushalt
├── kreise
├── stammbaum
├── geschichte
├── interviews
├── nachkommen-und-patenschaften
├── vorsorge
└── steward
```

The route is not the authorization boundary. Each server request resolves account, family tenant, membership, role, resource scope, purpose, consent state, and any guardian constraint before reading data.

## Domain and repository model

| Surface | Address | Data rule |
| --- | --- | --- |
| Founder story | `frankx.ai/family` | Public-safe narrative and lineage call only |
| Product category | `frankx.ai/family-intelligence-system` | Public explanation, starter kit, template links |
| German product category | `frankx.ai/familien-intelligenz-system` | Public German explanation |
| German gateway | `frankx.ai/familie` | Generic locked shell, no family records |
| Private pilot | `familie.frankx.ai` | Human-approved DNS; authenticated tenant runtime |
| Generic hosted product | `app.<cleared-brand-domain>` | Separate naming, trademark, RDAP, cost, and security review |
| Family tenant | `<opaque-family-slug>.app.<cleared-brand-domain>` | No child names, full legal names, or lineage claims in hostnames |

Public Git contains protocols, schemas, user-interface shells, synthetic fixtures, and adapters. Private family records live in an encrypted tenant store and leave it only through a scoped, auditable export.

## Pilot activation order

1. Create a synthetic tenant and pass cross-tenant, revocation, export, and restore tests.
2. Connect one adult steward account with passkey-ready recovery.
3. Create circle policies without adding relatives.
4. Import a minimal, explicitly approved private record set.
5. Invite one adult at a time and verify their effective grants.
6. Add guardian-managed child spaces only after guardian consent, age policy, deletion, and transition tests pass.
7. Enable emergency or succession configuration only after a human quorum drill and verified restore.

Production promotion, DNS, mailbox intake, real-family invitations, and history rewriting remain separate human approvals.
