---
name: prepare-emergency-packet
description: Assemble a minimal read-only emergency packet from an active policy without releasing secrets or triggering succession.
---

# Prepare emergency packet

## Rules

1. Verify policy ID, trigger type, requesting actor, and purpose.
2. Select only the minimum release scope.
3. Exclude passwords, private keys, recovery codes, raw health history, and unrelated archives.
4. Require the configured human verification and quorum.
5. Apply expiry and read-only controls.
6. Audit preparation, approvals, access, expiry, and revocation.

An agent may draft a packet and checklist. It cannot verify death/incapacity or release access.
