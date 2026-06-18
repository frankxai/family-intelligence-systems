# License Audit

Default stance:

- API adapters are allowed unless the upstream license, API terms, or documentation says otherwise.
- Docker Compose references are allowed as deployment guidance, subject to attribution.
- Forking may be legally allowed under the project license, but is not strategically wise by default.
- Vendoring is blocked until explicit license, security, maintainability, and scope review.
- Commercial SaaS packaging requires explicit review for copyleft licenses.

| Upstream | License | API adapter | Docker reference | Fork | Vendor | Attribution | SaaS/copyleft risk | Action |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| candiddev/homechart | Unknown/NOASSERTION | Review | Review | Review | Blocked | Review | Unknown | Manifest only until license confirmed |
| ulsklyc/yuvomi | MIT | Allowed | Allowed | Allowed | Review | Required | Low | Adapter-first |
| monicahq/monica | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Adapter-only until SaaS review |
| nextcloud/server | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Adapter-only |
| paperless-ngx/paperless-ngx | GPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | Medium/High | Adapter-only |
| immich-app/immich | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Adapter-only |
| grocy/grocy | MIT | Allowed | Allowed | Allowed | Review | Required | Low | High-priority adapter |
| mealie-recipes/mealie | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Adapter-only |
| TomBursch/kitchenowl | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Adapter-only |
| donetick/donetick | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Optional adapter |
| actualbudget/actual | MIT | Allowed | Allowed | Allowed | Review | Required | Low | High-priority adapter |
| firefly-iii/firefly-iii | AGPL-3.0 | Allowed | Allowed | Allowed by license | Blocked | Required | High | Adapter-only |
| dani-garcia/vaultwarden | AGPL-3.0 | Restricted review | Allowed | Allowed by license | Blocked | Required | Critical | Emergency-access adapter only after security review |
| home-assistant/core | Apache-2.0 | Allowed | Allowed | Allowed | Review | Required | Low | High-priority home adapter |
| BookStackApp/BookStack | MIT | Allowed | Allowed | Allowed | Review | Required | Low | Knowledge adapter |
| outline/outline | Unknown/NOASSERTION | Review | Review | Review | Blocked | Review | Unknown | Manifest only until license confirmed |
| modelcontextprotocol/servers | Unknown/NOASSERTION | Reference only | Reference only | Review | Blocked | Review | Supply-chain risk | Use patterns, not dynamic import |
| modelcontextprotocol/typescript-sdk | Unknown/NOASSERTION | Dependency review | N/A | Review | N/A | Review | Medium | Use official SDK after package license confirmation |
| github/github-mcp-server | MIT | Reference only | Reference only | Allowed | Blocked | Required | Medium | Reference implementation only |

