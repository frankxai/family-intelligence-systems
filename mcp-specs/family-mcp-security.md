# Family MCP Security

Required controls:

- no unauthenticated remote MCP
- no dynamic untrusted tool loading
- static allowlist of tools
- signed or checked tool manifests where possible
- tool description review
- least privilege per connector
- output sanitization
- prompt-injection aware boundaries
- confirmation gates for writes
- rate limiting
- per-family tenant isolation
- audit logs
- environment variable isolation
- deny-by-default policy

