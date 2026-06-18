# Family Roles And Permissions

Roles:

- `family_owner`
- `family_admin`
- `adult_member`
- `teen_member`
- `child_member`
- `elder_member`
- `trusted_advisor`
- `guest`
- `agent`
- `service_account`

Every tool call is evaluated against family ID, actor ID, actor role, target resource, sensitivity, action type, confirmation requirement, and audit requirement.

Default rules:

- Guests cannot access high or critical data.
- Child members cannot access finance, legal, medical, credential, or high-risk child data controls.
- Agents cannot write without explicit confirmation.
- Service accounts act only inside connector scope.
- Unknown action or sensitivity is blocked.

