---
name: export-gedcom-7
description: Project accepted, export-eligible private family claims into a GEDCOM 7 package without leaking blocked people, sources, media, or internal governance data.
---

# Export GEDCOM 7

## Rules

1. Require explicit human export confirmation and an authenticated family scope.
2. Include only accepted claims marked export-eligible for the requesting actor.
3. Preserve source citations and original-language names where the format allows.
4. Exclude disputed, unresolved, withdrawn, child-restricted, and scope-ineligible content.
5. Keep consent, audit, private policy, and succession metadata in the encrypted companion export, not public GEDCOM extensions.
6. Generate a manifest, checksum, format version, export time, and restore instructions.

GEDCOM is an interoperability projection, not the canonical authorization model.
