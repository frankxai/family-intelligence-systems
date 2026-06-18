# Family Contact Stewardship Pattern

Contact data is living family infrastructure. The goal is not to scrape or centralize everyone aggressively; it is to help each person keep their own contact record accurate and share only what they approve.

## Data Classes

- Identity: legal name, preferred name, family relation.
- Reachability: email, phone, mailing address, preferred channel.
- Availability: timezone, quiet hours, visit preferences.
- Care context: accessibility needs, dietary constraints, emergency contacts.
- Provenance: who supplied the data, when it was verified, and by whom.
- Consent: who can see it and for what purpose.

## Maintenance Loop

- Ask the owner to verify stale fields.
- Mark unverified fields as stale rather than overwriting.
- Keep conflicting values with provenance until resolved.
- Never infer sensitive relationships from messages or photos without confirmation.

