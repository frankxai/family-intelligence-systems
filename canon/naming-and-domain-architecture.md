# Naming and domain architecture

Status: working decision

Date: 2026-07-12

## Product-language decision

Use `Family Intelligence System` and `Familien-Intelligenz-System` as descriptive category language, not as a cleared trademark. Use `Family Intelligence Infrastructure` for the protocol and governance layer. Use **Founding Family Living Archive** / **Lebendiges Familienarchiv des Gründungstenants** as an explicitly synthetic public reference label; the real founding-family identity remains private.

“FamilyOS” is crowded across active household, parenting, and logistics products. “The Family Intelligence System” is also used by a parenting product. A separate brand name needs a naming and trademark review before purchase, launch, or paid promotion.

## Domain layers

| Layer | Recommended address | Decision |
|---|---|---|
| Founder story and lineage call | `frankx.ai/family` | Build now; public-safe |
| Category, product, and starter kit | `frankx.ai/family-intelligence-system` | Build now; public-safe |
| German category and product explainer | `frankx.ai/familien-intelligenz-system` | Build now; public-safe |
| German private family gateway | `frankx.ai/familie` | Authentication gateway; noindex; no private data in the unlocked shell |
| Private family pilot | `familie.frankx.ai` or a dedicated verified host | DNS and security approval required |
| Generic hosted product | future cleared brand domain with `app.<domain>` | Naming, RDAP, trademark, cost, and DNS review required |
| Family tenants | `<family-slug>.app.<domain>` or custom domain | Hosted phase; tenant and certificate automation required |

Do not publish or depend on a private family domain from this doctrine repository. Domain ownership, SSL, identity mapping, and redirect behavior belong to the private estate registry and require human verification.

## Email

Use an address only after the domain, mailbox, retention, and controller notice are verified. Recommended public aliases after approval are `family@`, `familie@`, `stammbaum@`, and `lineage@`. Email is an intake transport, never the canonical record and never the preferred path for passports, DNA files, medical records, passwords, or unredacted civil documents.
